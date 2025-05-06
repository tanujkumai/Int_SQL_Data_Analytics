# 📊 Intermediate SQL - Sales Analysis

## 🧾 Overview
Analysis of customer behavior, retention, and lifetime value for an e-commerce company using SQL. The goal is to uncover insights to improve retention and maximize revenue.

---

## ❓ Business Questions

1. **Customer Segmentation:** Who are our most valuable customers?  
2. **Cohort Analysis:** How do different customer groups generate revenue?  
3. **Retention Analysis:** Which customers haven't purchased recently?

---

## 🧹 Data Preparation

**🖥️ Query:** [`0_create_view.sql`](./0_create_view.sql)

- Combined customer and transaction tables
- Calculated first purchase dates for cohort analysis
- Created a reusable view with sales, revenue, and customer info

---

## 📈 Analysis

### 1. 🧮 Customer Segmentation

**🖥️ Query:** [`1_customer_segmentation.sql`](./1_customer_segmentation.sql)

- Categorized customers by Lifetime Value (LTV)
- Segmented into High, Mid, and Low-value groups
- Calculated total revenue contribution per group

**📊 Visualization:**

<img src="../Resources/images/6.3_customer_segementation.png" alt="Customer Segmentation" width="50%">

**🔍 Key Findings:**

| Segment      | % of Customers | Revenue Share | Total Revenue |
|--------------|----------------|----------------|----------------|
| High-Value   | 25%            | 66%            | $135.4M        |
| Mid-Value    | 50%            | 32%            | $66.6M         |
| Low-Value    | 25%            | 2%             | $4.3M          |

💡 **Insights:**

- **High-Value:** Launch a premium loyalty program for 12,372 top customers.
- **Mid-Value:** Encourage upgrades with tailored promotions (opportunity: $66.6M → $135.4M).
- **Low-Value:** Target with price-sensitive or frequency-boosting campaigns.

---

### 2. 📆 Customer Revenue by Cohort

**🖥️ Query:** [`2_cohort_analysis.sql`](./2_cohort_analysis.sql)

- Grouped customers by year of first purchase (cohorts)
- Tracked revenue and size trends across cohorts
- Normalized data for fair time-based comparisons

**📊 Visualizations:**

Customer Revenue by Cohort (Normalized):
<img src="../Resources/images/5.2_customer_revenue_normalized.png" alt="Customer Revenue Normalized" width="50%">

3-Month Rolling Average Revenue & Customers:
<img src="../Resources/images/5.2_monthly_revenue_customers_3mo.png" alt="Monthly Revenue & Customer Trends" width="50%">

**🔍 Key Findings:**

- Revenue per customer declined: older cohorts (2016–2018) spent ~$2,800+, 2024 cohort dropped to ~$1,970.
- 2022–2023 were peak years for customers and revenue; both declining in 2024.
- Significant volatility — especially in 2020 and 2024 — indicating retention challenges.

💡 **Insights:**

- Target recent cohorts (2022–2024) with retention offers.
- Apply successful tactics from high-revenue cohorts (2016–2018).
- Use loyalty programs to smooth out revenue drops.

---

### 3. 🔁 Customer Retention

**🖥️ Query:** [`3_retention_analysis.sql`](./3_retention_analysis.sql)

- Calculated last purchase dates per customer
- Flagged customers at risk of churn
- Analyzed cohort-specific retention patterns

**📊 Visualization:**

<img src="../Resources/images/7.3_customer_churn_cohort_year.png" alt="Customer Churn by Cohort Year" width="50%">

**🔍 Key Findings:**

- After 2–3 years, churn stabilizes at ~90%.
- Consistent long-term retention (~8–10%) across all cohorts.
- New cohorts (2022–2023) show similar churn trajectories as past ones.

💡 **Insights:**

- Focus engagement efforts in first 1–2 years with onboarding and loyalty rewards.
- Prioritize high-value win-back campaigns over generic reactivation.
- Use churn prediction indicators for proactive customer recovery.

---

## 📌 Strategic Recommendations

### 1. 🏆 Customer Value Optimization (Segmentation)
- Launch VIP program for top 12,372 customers (66% of revenue).
- Design upgrade flows for mid-tier segment.
- Activate low-tier customers with promotions or tailored offers.

### 2. 📈 Cohort Performance Strategy
- Personalize re-engagement for recent cohorts (2022–2024).
- Introduce loyalty or subscription-based programs.
- Apply winning strategies from 2016–2018 cohorts to current ones.

### 3. 🛡️ Retention & Churn Prevention
- Focus on first 1–2 years for engagement and retention.
- Develop win-back campaigns for high-LTV churned customers.
- Use churn prediction models to intervene early.

---

## ⚙️ Technical Details

- **Database:** PostgreSQL  
- **Tooling:** DBeaver for querying  
- **Visualization:** Generated using [ChatGPT](https://chat.openai.com)

---

> ✍️ This project is part of my self-learning journey to build stronger SQL analytics skills using real-world datasets.  

---
## 🔗 Connect With Me

- 💼 [LinkedIn](https://www.linkedin.com/in/tanujkumai/)
- 💻 [GitHub](https://github.com/tanujkumai)
- 📧 Email: [tanujkumai21@gmail.com](mailto:tanujkumai21@gmail.com)

Thanks for checking out my work!
