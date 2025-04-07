# 🧠 Retail Analytics Project: Profitability Prediction, Customer Segmentation & CLTV Forecasting

## 📌 Project Overview

This two-part data science project is designed to extract actionable insights from a large retail dataset (~180,000 transactions) by applying predictive modeling, clustering techniques, and probabilistic survival analysis. It provides deep visibility into profitability drivers, customer behavior, and long-term value—empowering business stakeholders to make data-driven marketing and operational decisions.

---

## 🔍 Part 1: Order Profitability Prediction & Customer Segmentation

### 💸 1. **Order Profitability Prediction (Regression Analysis)**

#### Objective:
To identify key features influencing order profitability and build a robust regression model to predict profit per order.

#### Key Steps:
- **Data Cleaning & Preprocessing:** Handled missing values, converted date formats, and created new features like *Shipping Delay (Days)*.
- **EDA:** Explored correlations between `Profit`, `Sales`, `Discount Rate`, `Product Price`, etc., before and after outlier removal.
- **Feature Engineering:** Introduced interaction terms (e.g., `Discount × Item Total`), created margin-related features, and extracted time-based metrics.
- **Time-Series Analysis:** Tracked order volume, profits, and customer activity by month/quarter to uncover trends (e.g., a notable dip post-Q3 2017).
- **Modeling:** Trained and evaluated an `XGBoostRegressor` model, achieving:
  ```
  R² Score: 0.9997 ✅
  RMSE:    0.70
  MAE:     0.44
  ```

### 🧍 2. **Customer Segmentation (Clustering)**

#### Objective:
To segment customers based on behavior (RFM, location, and order traits) and visualize group separations.

#### Key Steps:
- **Feature Selection:** Created features using RFM metrics and categorical encodings for `Region`, `Market`, etc.
- **Scaling & KMeans Clustering:** Applied StandardScaler and determined optimal K using the Elbow Method.
- **Segmentation:** Clustered customers into 4 distinct segments and labeled them accordingly.
- **Visualization:** Applied PCA to reduce dimensionality and plotted clusters in a 2D scatter plot for interpretation.

---

## 🔁 Part 2: CLTV Forecasting & Survival Analysis

### 📈 3. **Customer Lifetime Value (CLTV) Prediction**

#### Objective:
To forecast expected revenue from individual customers over the next 6 months using probabilistic models.

#### Models Used:
- **BG/NBD (Beta Geometric Negative Binomial Distribution):** To predict future transactions.
- **Gamma-Gamma Model:** To estimate average profit per transaction.

#### Key Outputs:
- Predicted purchase frequency per customer.
- Expected average profit.
- Combined 6-month CLTV score (`CLTV_6m`), adjusted using a discount factor.

#### Bonus:
- Tiered customers into **High**, **Mid**, and **Low CLTV segments** for targeted marketing.

### ⏳ 4. **Churn Prediction (Survival Analysis)**

#### Objective:
To understand and model customer churn risk using survival analysis techniques.

#### Key Steps:
- **Kaplan-Meier Estimator:** To visualize the probability of customer retention over time.
- **Cox Proportional Hazards Model:** To quantify the impact of features like `Region`, `Segment`, and `Profit` on churn risk.
- **Prediction:** Estimated *Time to Churn* per customer and visualized risk groups using survival curves.

---

## 📦 Tools & Technologies

- **Languages:** Python
- **Libraries:** pandas, numpy, matplotlib, seaborn, lifetimes, lifelines, scikit-learn, xgboost
- **Environment:** Jupyter Notebook, Anaconda
- **Modeling:** BG/NBD, Gamma-Gamma, KMeans, XGBoost, CoxPH, PCA

---

## 💼 Business Applications

- **Profit Optimization:** Understand profitability drivers and reduce losses from over-discounting.
- **Customer Retention:** Predict churn and proactively retain high-value customers.
- **Personalized Marketing:** Segment customers for targeted campaigns based on CLTV and behavior.
- **Revenue Forecasting:** Predict future income streams from the existing customer base.

---

## 🎯 Final Takeaway

This project isn’t just about models—it’s a **full-stack customer analytics pipeline** that transforms raw retail data into strategic insight. Whether it’s predicting profits, uncovering hidden customer segments, or estimating customer value, this project delivers real-world impact and business intelligence.


# Also you can check the description.ipynb in this file there are some snippets and working parts of the project
