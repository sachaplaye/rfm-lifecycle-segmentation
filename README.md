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

With the UK Domestic market generating most of the cash but APAC and EMEA providing more revenue on a per customer basis, there is opportunity to allocate targeted acquisition budget toward B2B outbound sales in APAC and EMEA. This would allow us to expand our presence in those markets whilst mitigating the risk of over exposure to any negative economical headwinds in the UK market place.


#### Customer Net Gain View - Year over Year (YoY):
![Base By Region](notebooks/images/B2B_Net_Gain_View.png)

- **Net Customer View** shows a growth of 1.3% in customer volume year over year, driven by strong acquisition figures for Key accounts and Core accounts. This is accompanied by a 4.7% growth in Net Revenue to £8.2m, with 2/3<sup>rd</sup>s of the incremental revenue driven by Key accounts. 
- **Existing Customer View:** Growing customers (set at 4.5% monthly threshold) are outperforming Declining customers. However, the health of the Stable base is deteriorating. We are seeing a net contraction of (3.2%) in-life revenue year over year. A significant proportion of this is caused by an erosion in value of Core accounts and Standard accounts, which brings Net Retained Revenue down to 84% YoY for existing customers
- **Customer Churn Rate** at 36.1% year over year is high. Key accounts are doing well at only 3.4% Churn. However, we are stuggling to retain Core accounts and Standard accounts that make up a significant portion of the base. This is coupled with high shrinkage in net retained revenue of 60% for Core accounts and 41% for Standard accounts.
- **One-Time Purchases:** These one-off transactions make up 23% of the customer base by volume. Net Growth in this segment is flat YoY, in that we are not really making more of these potential customers stick versus prior year.

Acquisition and retention of large customers is 
the bottom line driving the business forward
I NEED TO FINISH THIS PART OFF

---
---
## Customer Value & Lifecycle
[back to top](#-table-of-contents)
#### B2B Customer Lifecycle in the last 12 months:
![Customer Lifecycle](notebooks/images/RFM_Model.png)

COMMENTARY HERE

#### Customer Value:
![Customer Value](notebooks/images/Pareto_Revenue.png)

COMMENTARY HERE

---
---
## Buying Behaviour & Customer Profile
[back to top](#-table-of-contents)

#### Basket Spread Analysis:
![Basket Spread Analysis](notebooks/images/Basket_Spread.png)

COMMENTARY HERE

#### Basket Density View:
<img src="notebooks/images/Basket_Density.png" width="65%">

COMMENTARY HERE

This needs reworking on the personas

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

---