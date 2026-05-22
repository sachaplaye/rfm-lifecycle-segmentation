# B2B Customer Lifecycle & Value Segmentation

> **Information Source:** This portfolio uses the [Online Retail II UCI dataset from Kaggle](https://www.kaggle.com/datasets/mashlyn/online-retail-ii-uci/data). For the purpose of the analysis, this dataset is treated as a B2B online retailer, *(testing was done to confirm)*. We extract end-to-end commercial analytics and provide strategic recommendations for senior-leadership. *(Guest checkouts are excluded from this view. See [ETL pipeline](https://github.com/sachaplaye/rfm-lifecycle-segmentation/blob/main/notebooks/1_data_staging.ipynb) for data preparation steps).*
---
## 📑 Table of Contents
Information is as of close of business 30<sup>th</sup> Nov 2011.
- [1. Executive Summary & Commercial Recommendations](#executive-summary--commercial-recommendations)
- [2. High-Level Business Performance](#high-level-business-performance)
- [3. Customer Value & Lifecycle](#customer-value--lifecycle)
- [4. Buying Behaviour & Customer Profile](#buying-behaviour--customer-profile)
- [5. Predictive Analytics & Churn Prevention](#predictive-analytics--churn-prevention)


---
---
## Executive Summary & Commercial Recommendations
[back to top](#-table-of-contents)

wer


---
---
## High-Level Business Performance
[back to top](#-table-of-contents)
<!-- <img src="notebooks/images/Base_By_Region.png" width="90%"> -->
#### B2B Customer Base by Region in the last 12 months:
![Base By Region](notebooks/images/Base_By_Region.png)

- **UK Domestic** provides a high-volume foundation for the business, accounting for 90% of the customer base and 83% of total revenue.
- **International View:** While customer volume is lower, both APAC and EMEA deliver significantly higher average revenue per customer. If we strip out whale accounts (>£30k annual spend), APAC averages £3.9k per customer (2.5 times the UK average of £1.4k). EMEA, which accounts for 9% of the customer base by volume and 15% of total revenue, provides 40% more revenue per customer (at £2.0k).

**Diversify the Base:** With the UK Domestic market generating most of the net revenue but APAC and EMEA providing more revenue on a per customer basis, there is opportunity to allocate targeted acquisition budget toward B2B outbound sales in APAC and EMEA. This would allow us to expand our presence in those markets whilst mitigating the risk of over exposure to any negative macro economic headwinds in the UK market place.


#### Customer Net Gain View - Year over Year (YoY):
![Base By Region](notebooks/images/B2B_Net_Gain_View.png)

- **Net Customer View** shows a growth of 1.3% in customer volume year over year, driven by strong acquisition figures for Key accounts and Core accounts. This is accompanied by a 4.7% growth in Net Revenue to £8.2m, with 2/3<sup>rd</sup>s of the incremental revenue driven by Key accounts. 
- **Existing Customer View:** Growing customers (set at 4.5% monthly threshold) are outperforming Declining customers. However, the health of the Stable base is deteriorating. We are seeing a net contraction of (3.2%) in-life revenue year over year. A significant proportion of this is caused by an erosion in value of Core accounts and Standard accounts, which brings Net Retained Revenue down to 84% YoY for existing customers
- **Customer Churn Rate** at 36.1% year over year is high. Key accounts are doing well at only 3.4% Churn. Yet, we are struggling to retain Core accounts and Standard accounts that make up a significant portion of the base. This is coupled with high shrinkage in net retained revenue of 60% for Core accounts and 41% for Standard accounts.
- **One-Time Purchases:** These one-off transactions make up 23% of the customer base by volume. Net Growth in this segment is flat YoY, in that we are not really making more of these potential customers stick versus prior year.

**We are performing strongly** in terms of Acquisition and Retention of our main customers, with a churn rate of 3.4% and 95% revenue retention with £6.5m yearly net revenue making up 80% of total revenue.

**We need to target** 823 accounts in decline which contribute (£837k) reduction in yearly revenue. The majority of customers in the declining segment are 435 Core accounts and 297 Key accounts, which are leaking (£661k) of revenue.

**We can look at** One-Time Purchases separately, as we need to gauge value and the return on investment if allocating spend on this cohort.

---
---
## Customer Value & Lifecycle
[back to top](#-table-of-contents)
#### B2B Customer Lifecycle in the last 12 months:
![Customer Lifecycle](notebooks/images/RFM_Model.png)

As we show later, 50% of these customers are non-seasonal year round purchasers and 62% traded with us two years running, of which 20% are year on year seasonal repeat purchasers:

- **We have a U-shaped distribution** between Lost and Champions both making up 22% of the base. £5.5m, (68%) of total revenue spend is provided by 933 accounts. If we include Loyal and 'Cannot lose them' customers, we see the business is serving 1.4k customers really well and the other 3k customers contribute relatively little revenue.
- **There is a big drop from Champion to Loyal**. We need to understand if these £2.6k spend customers are smaller businesses or larger resellers with potential for upsell as this will determine whether we target growth of existing base or acquisition of new customers. We look at this in more detail in the customer profiling summary.
- **23% are hibernating / Lost:** With 1.1 mth average frequency these 966 customers are made up in majority of the 913 One-Time Purchasers. With an average revenue of £294 per customer contributing £284k overall revenue this may not be worth the marketing spend for reactivation campaigns. 

#### Customer Value:
![Customer Value](notebooks/images/Pareto_Revenue.png)

- **If we split Lifecycle by Pareto distribution** and look at total net revenue, there is a clear revenue risk in the bottom left quadrant for Key and Core accounts.
- **Between the 'About to Sleep' and 'At Risk'** segments, there is £688k revenue risk for 643 customers who are slipping away.
- **Combining this with £340k revenue risk** from 116 Key accounts we 'can not lose' and we have a total of over £1m in high-tier revenue currently showing signs of Churn.

**We need to understand the customer profile** and build out a churn risk model first to better serve and target these customers.

---
---
## Buying Behaviour & Customer Profile
[back to top](#-table-of-contents)
<!-- ![Basket Spread Analysis](notebooks/images/Basket_Spread.png) -->
#### Basket Density of Customers on the left & Basket Density of Revenue on the right:
<img src="notebooks/images/Basket_Density.png" width="47%">
<img src="notebooks/images/Basket_Revenue.png" width="47%">

**On a per basket basis:** Where the distribution of customers are might not be where our revenue is coming from. We need to check this before profiling our customers to corroborate the findings.

Now i just need to say what the above is saying before diving into the customer profiles.

oh and spell out the obvious stuff from that scatter like the columns which look like restockers. so i could also say that we are covering basic profiles here since there are clear columns and they should be split out as a type of customer some do more some do less but we don't go to that level of intricacy in this first pass.


i need to mention this axis split thing between count of custoemr and revnue it is like a bar but we can say they are close in this example so we can use the cuteorm profile matrix i put next. ie just say the custoemr quantity is middle and the revenue goes a bit centre right but is close enough to middle we can use the next matrix to profile customers 


---
---
## Predictive Analytics & Churn Prevention
[back to top](#-table-of-contents)

maybe it should be churn since what strategy is there in this other than churn prevention?

can I plot a graph of risk against seasonality
and also risk against persona


---
---
*NB this is a product only view which excludes re-keys, postage fees, additional charges and such like.* PUT ALL THE DATA CAVEATS HERE
- This is a figure it all out yourself dataset, normally I figure it out first, then I reach out to the business to understand all the intricacies and dynamics I might have missed before I try making assumptions on things, so this work is a guideline but might not be totally on point. review this ... coallesce the figure and people bit

---