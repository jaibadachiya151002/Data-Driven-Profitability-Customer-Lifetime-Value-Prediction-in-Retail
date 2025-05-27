# 🧠 Retail Analytics Project: Profitability Optimization & Customer Insights
## 🧩 Problem Statement

In the rapidly evolving retail landscape, maintaining consistent profitability while retaining valuable customers is critical to long-term success. In this business case, a large retail company experienced an alarming **48% drop in sales and a 32% decline in profit** during **Q4 of 2017**, despite achieving its **highest-ever order volume (6,041 orders)** in the same quarter. This counterintuitive trend raised urgent concerns among business stakeholders regarding the sustainability of their sales strategy, customer retention, and overall operational effectiveness.

### Core Business Questions

1. **Why did profitability decline so significantly in Q4 2017 despite a spike in order volume?**
2. **Which discounting and pricing strategies may have led to margin erosion?**
3. **What customer behaviors or market dynamics contributed to this pattern?**
4. **How can the business predict future order profitability and reduce discount waste?**
5. **Which customers should be prioritized for retention and upselling based on their long-term value?**
6. **What is the expected churn behavior of different customer segments, and how can it be mitigated?**

### Business Objectives

* **Diagnose the root cause** behind the Q4 2017 profit drop using data-driven exploration and statistical analysis.
* **Develop predictive models** to forecast order-level profitability and customer lifetime value (CLTV).
* **Segment customers** meaningfully to enable personalized marketing, retention campaigns, and pricing strategies.
* **Quantify churn risk** and estimate the average duration of activity for different customer groups.
* **Deliver actionable KPIs and business recommendations** to guide decision-making in pricing, customer engagement, and channel strategy.

### Data Landscape

* \~180,000 transactional records including order details, discount rates, customer IDs, shipping times, geolocation, and profit.
* Quarterly trends from 2014 to 2017, offering rich time-series insights into sales, discounting, and customer behavior.
---

## Analytics:

### IN 2017 Q4 – DROP ANALYSIS 

#### Why is the **Total Discount Value** low (\~210K) while the **Average Discount** is high (\~33.15%)?

#### 1. **Spike in Order Count does not translate to higher Sales**

* **Order Count in 2017 Q4**: **6041** (highest among all quarters).
* But **Total Sales** dropped sharply to **\~1.51 million**, down from **\~2.90 million in 2017 Q3**.
* This suggests that although **more orders were placed**, they were likely of **low value or deeply discounted**, which reduced total revenue.

#### 2. **Extremely High Average Discount (\~33.15%)**

* This is **the highest discount average** across all quarters.
* A high average discount combined with low sales suggests **intensive discounting campaigns**, possibly on **less expensive items**.

#### 3. **Low Total Discount Value (\~210K)**

* Despite the higher average discount, the **Total Discount Value** dropped from **\~727K in Q3** to **\~210K in Q4**.
* This can be explained by:

  * Lower priced products being sold (less absolute discount per item).
  * Discounts applied to a narrower set of products.
  * Customers possibly buying **only highly discounted items**, reducing gross discount totals even further.

#### 4. **Drop in Total Profit**

* **Total Profit** fell from **\~551K in Q3** to **\~372K in Q4**, showing reduced profitability—likely due to **aggressive discounting without sufficient sales volume**.

### Summary

In **2017 Q4**, the business appears to have run **heavy discounting campaigns**. However, this did **not lead to higher sales volume or revenue**. The high average discount reflects the intensity of markdowns, but the lower total sales and discount value suggest that customers either:

* Bought fewer or cheaper items, or
* Took advantage of steep discounts on a limited number of products.

**Recommendation**: Review Q4 discounting strategy—consider whether the depth of discounts was justified and whether it targeted the right products and segments to drive profitable growth.

## Recommendations to Improve Future Quarters (Up to Q4 2017)

### 1. **Customer Retention & Loyalty**

**Observation:** Although Order Count increased sharply in Q4 2017, Total Sales and Profit dropped significantly, indicating potentially low-value or one-time buyers.

**Recommendation:**

* Develop **loyalty programs** to encourage repeat purchases and increase customer lifetime value.
* Implement **email remarketing** targeting customers who bought during Q4 with tailored offers.
* Promote **subscription models** or **product bundles** to incentivize more frequent purchases.


### 2. **Refine Discount Strategy**

**Observation:** Q4 2017 had the highest average discount (\~33%) but saw a large drop in total sales and total discount value.

**Recommendation:**

* Use **targeted discounting** — offer higher discounts to price-sensitive segments while protecting margins on loyal or premium customers.
* Avoid blanket steep discounts that erode profitability; focus on **dynamic pricing** aligned with inventory and demand.
* Experiment with **time-limited offers** to create urgency without sacrificing overall profitability.


### 3. **Product & Sales Focus**

**Observation:** Significant drop in Total Sales and Profit despite high order volume.

**Recommendation:**

* Identify **best-selling and highest-margin products** and prioritize promotions around them.
* Consider phasing out or repricing **low-margin or slow-moving SKUs** to optimize inventory.
* Conduct an **ABC analysis** to allocate resources effectively.


### 4. **Shipping & Delivery Improvements**

**Observation:** Average shipping delay remained fairly consistent (\~3.45 days) but could be a competitive factor.

**Recommendation:**

* Introduce **faster or guaranteed shipping options** to improve customer satisfaction.
* Enhance **post-purchase communication** and tracking transparency.
* Use shipping experience as a **competitive differentiator** in marketing.


### 5. **Sales Channel Optimization**

**Observation:** Despite more orders in Q4 2017, sales value dropped, possibly due to shifts in customer acquisition.

**Recommendation:**

* Audit marketing and sales channels for efficiency — are channels driving quality traffic and conversions?
* Invest in **seasonal paid promotions** and social media campaigns tailored for Q4 demand.
* Optimize **mobile and web experiences** to reduce friction and increase conversion rates.


### 6. **Predictive Analytics & Seasonal Planning**

**Observation:** Q4 2017 shows unusual patterns in sales and discounting.

**Recommendation:**

* Develop **forecasting models** to anticipate seasonal trends and prepare inventory and marketing strategies accordingly.
* Plan **seasonal campaigns** to maximize sales during peak quarters and mitigate drop-offs.
* Use historical data to fine-tune discount levels and product assortments by season.


### 7. **Customer Feedback Collection**

**Observation:** Data lacks insight into *why* customers behaved this way in Q4 2017.

**Recommendation:**

* Deploy **customer surveys** and feedback tools to understand satisfaction drivers.
* Use **Net Promoter Scores (NPS)** or exit surveys to gather qualitative insights.
* Leverage feedback to improve product offerings, pricing, and customer experience.

## 🔍 Key Components

### 1. 📉 Profitability Root Cause Analysis

* Uncovered 48% drop in sales (Q3 to Q4 2017) despite record order volume (6,041 orders).
* Identified steep average discounts (\~33%) on low-value items as main contributor.
* Validated quarterly profit variance using ANOVA (F=81.56, p<0.001).

### 2. 🤖 Profit Prediction (XGBoost)

* Engineered features like shipping delays, discount interactions, and time trends.
* Achieved:

  ```
  R² = 0.9997 | RMSE = 0.70 | MAE = 0.44
  ```
* Enabled proactive pricing and margin strategy per order.

### 3. 🧍‍♂️ Customer Segmentation (KMeans)

* Segmented customers into 4 groups using RFM and geolocation data.
* Visualized clusters via PCA for marketing personalization.

### 4. 💸 CLTV Forecasting (BG/NBD + Gamma-Gamma)

* Predicted 6-month revenue per customer and classified into High/Mid/Low tiers.
* Informed budget allocation and loyalty strategy.

### 5. ⏳ Churn Risk Modeling (Survival Analysis)

* Kaplan-Meier and CoxPH models used to estimate time-to-churn and key risk drivers.

---

## 📊 KPIs & Recommendations

| **Area**              | **Action**                        | **Impact**                              |
| --------------------- | --------------------------------- | --------------------------------------- |
| Discounting           | Segment/time-limited offers       | Protects margins, targets value-seekers |
| Engagement            | Loyalty + remarketing campaigns   | Boosts CLTV, encourages repeat buying   |
| Product Focus         | Promote high-margin, ABC analysis | Prioritizes profitable items            |
| Logistics             | Improve delivery & UX             | Enhances satisfaction, retention        |
| Channel Strategy      | Audit/refine ad spend             | Increases quality traffic               |
| Seasonality Forecasts | ML-based demand planning          | Reduces overstock/stockouts             |

---

## ⚙️ Tech Stack

**Languages**: Python
**Libraries**: pandas, scikit-learn, xgboost, lifetimes, lifelines, matplotlib, seaborn
**Models**: XGBoost, KMeans, BG/NBD, Gamma-Gamma, CoxPH, ANOVA
**Environment**: Jupyter Notebook

---

## 💼 Business Impact

* Diagnosed profitability drop with 33%+ discount leakage on low-value items.
* Built forecasting models for profits, churn, and customer value.
* Provided actionable KPIs to refine discounts, campaigns, and growth levers.

---

## 📁 Explore the Code

See `description.ipynb` for code snippets and insights used throughout the project.

