# 🧠 Intermediate SQL - Sales Analysis

## 📌 Overview
Analysis of customer behavior, retention, and lifetime value for an e-commerce company to improve customer retention and maximize revenue.

---

## ❓ Business Questions
1. **Customer Segmentation:** Who are our most valuable customers?
2. **Cohort Analysis:** How do different customer groups generate revenue?
3. **Retention Analysis:** Which customers haven't purchased recently?

---

## 🧼 Data Preparation

**📄 Query:** [`0_create_view.sql`](0_create_view.sql)
- Aggregated sales and customer data into revenue metrics  
- Calculated first purchase dates for cohort analysis  
- Created view combining transactions and customer details  

---

## 📊 Analysis

### 1. 🏷️ Customer Segmentation

**📄 Query:** [`1_customer_segmentation.sql`](1_customer_segmentation.sql)
- Categorized customers based on total lifetime value (LTV)  
- Assigned customers to High, Mid, and Low-value segments  
- Calculated key metrics like total revenue  

**📈 Visualization:**  
<img src="../Resources/images/6.3_customer_segementation.png" alt="Customer Segmentation" width="50%">

**🔍 Key Findings:**
- High-value segment (25%) generates **66% of revenue ($135.4M)**  
- Mid-value (50%) brings in **32% of revenue ($66.6M)**  
- Low-value (25%) contributes just **2% of revenue ($4.3M)**  

**💡 Insights:**
- **High-Value:** Launch VIP program for 12,372 top customers  
- **Mid-Value:** Personalize upgrades to move customers up  
- **Low-Value:** Re-engage with price-sensitive promotions  

**🛠️ Skills Used:**
- `CASE` statements  
- Window functions (`NTILE`, `RANK`)  
- CTEs, Aggregations  

---

### 2. 📆 Customer Revenue by Cohort

**📄 Query:** [`2_cohort_analysis.sql`](2_cohort_analysis.sql)
- Tracked revenue and customer count by yearly cohorts  
- Normalized revenue based on customer tenure  
- Analyzed trends across time  

**📈 Visualizations:**

Customer Revenue Normalized  
<img src="../Resources/images/5.2_customer_revenue_normalized.png" width="50%">

Monthly Revenue & Customers (3-Month Rolling Avg)  
<img src="../Resources/images/5.2_monthly_revenue_customers_3mo.png" width="50%">

**🔍 Key Findings:**
- Older cohorts (2016–2018) spend ~$2,800+, newer cohorts (2024) down to ~$1,970  
- 2022–2023 saw revenue/customer peak; both are declining in 2024  
- Spikes & drops indicate unstable retention  

**💡 Insights:**
- Personalize re-engagement for 2022–2024 cohorts  
- Stabilize with loyalty/subscription programs  
- Apply 2016–2018 strategies to new customers  

**🛠️ Skills Used:**
- Cohort grouping (`DATE_TRUNC`, `MIN`)  
- Revenue normalization  
- Rolling average with window functions  

---

### 3. ⏳ Customer Retention

**📄 Query:** [`3_retention_analysis.sql`](3_retention_analysis.sql)
- Flagged at-risk and churned customers  
- Measured retention by cohort  
- Analyzed last purchase behavior  

**📈 Visualization:**  
<img src="../Resources/images/7.3_customer_churn_cohort_year.png" width="50%">

**🔍 Key Findings:**
- Churn stabilizes at ~90% after 2–3 years  
- Retention rates consistently low (8–10%)  
- New cohorts following same churn path  

**💡 Insights:**
- Strengthen onboarding and early loyalty programs  
- Prioritize win-back for high-value churned users  
- Predict churn with behavioral signals  

**🛠️ Skills Used:**
- Date difference calculations  
- `CASE` for churn flags  
- CTEs for cohort-level metrics  

---

## 🎯 Strategic Recommendations

### 1. 🥇 Customer Value Optimization
- Launch VIP membership for top 25% customers (66% revenue)  
- Personalize upgrades for mid-value segment  
- Re-engage low-value users with targeted campaigns  

### 2. 📈 Cohort Performance Strategy
- Focus retention efforts on recent cohorts (2022–2024)  
- Stabilize revenue with loyalty/subscription plans  
- Apply successful old cohort strategies to new customers  

### 3. 🔁 Retention & Churn Prevention
- Strengthen 1st-year engagement and onboarding  
- Win-back high-value churned users  
- Predict and intervene early for at-risk users  

---

## ⚙️ Technical Stack

| Category        | Tools Used             |
|----------------|------------------------|
| **Database**    | PostgreSQL             |
| **SQL Client**  | DBeaver                |
| **Languages**   | SQL                    |
| **Skills**      | Window Functions, CTEs, Aggregations, Conditional Logic |
| **Visualization** | Generated via ChatGPT |

---

> 📂 This project is part of my hands-on learning journey into intermediate SQL with a focus on real-world business analysis.  
> 🎯 Feedback or collaboration ideas are welcome!
