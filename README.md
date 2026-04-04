<div align="center">

# 🛒 E-Commerce Customer Churn Analysis

**Uncovering why customers leave — and how to bring them back**

![SQL](https://img.shields.io/badge/SQL-MySQL%20%7C%20PostgreSQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-28a745?style=for-the-badge)
![Domain](https://img.shields.io/badge/Domain-E--Commerce-orange?style=for-the-badge)

</div>

---

## 📌 Project Overview

Customer churn is one of the biggest challenges in e-commerce. This project uses **SQL** to deeply analyze churn patterns, identify at-risk customer segments, and surface actionable retention strategies from raw transactional data.

> _"It costs 5x more to acquire a new customer than to retain an existing one."_  
> — This project helps answer **why customers churn** and **how to stop it.**

---

## 🎯 Objectives

- 🔍 Identify customer segments with the **highest churn rates**
- 📦 Analyze **purchase history** to detect loyalty patterns
- 📉 Understand **behavioral signals** that precede churn
- 💡 Derive **data-driven strategies** for improving customer retention

---

## 🛠️ Tools & Skills Used

| Skill | Description |
|-------|-------------|
| 🗄️ SQL (MySQL / PostgreSQL) | Core analysis language |
| 🔗 Joins & Subqueries | Combining multi-table data |
| 📊 Aggregations & Grouping | Summarizing churn metrics |
| 🧹 Data Cleaning | Handling nulls, duplicates, formatting |
| 🧠 Exploratory Data Analysis | Pattern discovery via queries |

---

## 📊 Key Insights

- 🚨 Identified customer segments with **significantly high churn rates** based on purchase frequency and recency
- 🛍️ Customers with **fewer than 3 purchases** showed the highest churn probability
- 📅 Churn was more prevalent among customers with **longer gaps** between orders
- 💳 High-value customers had **lower churn rates**, highlighting loyalty correlation with spend

---

## 📂 Repository Structure
```
E-Commerce-Customer-Churn-Analysis/
│
├── 📄 E-Commerce Customer churn db.sql   # Full SQL script — schema + analysis queries
└── 📄 README.md                          # Project documentation
```

---

## 🔍 SQL Concepts Used
```sql
-- Sample: Identifying churned customers (no purchase in 90+ days)
SELECT 
    customer_id,
    MAX(order_date) AS last_purchase,
    DATEDIFF(CURDATE(), MAX(order_date)) AS days_since_purchase,
    CASE 
        WHEN DATEDIFF(CURDATE(), MAX(order_date)) > 90 THEN 'Churned'
        ELSE 'Active'
    END AS churn_status
FROM orders
GROUP BY customer_id;
```

**Techniques covered:**
- `JOINS` — linking customers, orders, and product tables
- `GROUP BY` + `HAVING` — segment-level aggregations
- `CASE WHEN` — churn classification logic
- `SUBQUERIES` — nested filtering for retention analysis
- `CTEs` — clean, readable multi-step queries

---

## 🚀 How to Run

1. **Clone the repository**
```bash
   git clone https://github.com/gokulkriszz/E-Commerce-Customer-Churn-Analysis.git
```

2. **Open your SQL environment** (MySQL Workbench, pgAdmin, DBeaver, etc.)

3. **Import and run the script**
```bash
   source E-Commerce\ Customer\ churn\ db.sql
```

4. **Execute queries step by step** to reproduce all churn analysis findings

---

## 💡 Business Recommendations

Based on the SQL analysis:

| Finding | Recommendation |
|---------|---------------|
| High churn in low-frequency buyers | Launch re-engagement email campaigns |
| Long gaps between purchases | Set up automated reminder notifications |
| High-value customers churn less | Build a VIP loyalty rewards program |
| New customers churn fastest | Improve onboarding & first-purchase experience |

---

## 🙋‍♂️ Author

<div align="center">

**Gokul Krishnan**

[![GitHub](https://img.shields.io/badge/GitHub-gokulkriszz-181717?style=for-the-badge&logo=github)](https://github.com/gokulkriszz)

_"Turning customer data into retention strategies."_

</div>
