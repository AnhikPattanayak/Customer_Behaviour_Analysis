# 🛍️ Customer Shopping Behavior Analysis

A data analytics project exploring transactional shopping data to uncover insights into customer spending patterns, product preferences, subscription behavior, and customer segmentation — using **Python**, **MySQL (SQL)**, and **Power BI**.

---

## 📌 Project Overview

This project analyzes **3,900 customer transactions** across multiple product categories. The goal is to derive actionable business insights that guide marketing strategies, discount policies, and customer retention efforts.

---

## 📂 Dataset Summary

| Property | Details |
|---|---|
| Total Rows | 3,900 |
| Total Columns | 18 |
| Missing Data | 37 values in `Review Rating` column |

**Key Features:**
- **Customer Demographics** — Age, Gender, Location, Subscription Status
- **Purchase Details** — Item Purchased, Category, Purchase Amount, Season, Size, Color
- **Shopping Behavior** — Discount Applied, Previous Purchases, Frequency of Purchases, Review Rating, Shipping Type

---

## 🔧 Tools & Technologies

| Tool | Purpose |
|---|---|
| Python (pandas) | Data cleaning & feature engineering |
| MySQL | SQL-based business analysis |
| Power BI | Interactive dashboard & visualization |

---

## 🧹 Data Preparation (Python)

- **Data Loading** — Imported dataset using `pandas`
- **Missing Data Handling** — Imputed missing `review_rating` values using the median rating per product category
- **Column Standardization** — Renamed all columns to `snake_case`
- **Feature Engineering**
  - `age_group` — binned customer ages into segments
  - `purchase_frequency_days` — derived from purchase frequency data
- **Data Consistency Check** — Verified redundancy between `discount_applied` and `promo_code_used`; dropped `promo_code_used`
- **Database Integration** — Loaded cleaned DataFrame into PostgreSQL for SQL analysis

---

## 🗄️ SQL Analysis (MySQL)

Ten business questions were answered using structured SQL queries:

1. **Revenue by Gender** — Male customers generated $157,890 vs. Female customers at $75,191
2. **High-Spending Discount Users** — 839 customers used discounts yet spent above the average purchase amount
3. **Top 5 Products by Rating**

   | Rank | Product | Avg Rating |
   |---|---|---|
   | 1 | Gloves | 3.86 |
   | 2 | Sandals | 3.84 |
   | 3 | Boots | 3.82 |
   | 4 | Hat | 3.80 |
   | 5 | Skirt | 3.78 |

4. **Shipping Type Comparison** — Express shipping ($60.48 avg) slightly outperforms Standard ($58.46 avg)
5. **Subscribers vs. Non-Subscribers** — Subscribers (1,053) avg spend: $59.49 | Non-subscribers (2,847) avg spend: $59.87
6. **Discount-Dependent Products** — Hat (50%), Sneakers (49.66%), Coat (49.07%), Sweater (48.17%), Pants (47.37%)
7. **Customer Segmentation** — Loyal: 3,116 | Returning: 701 | New: 83
8. **Top 3 Products per Category** — Jewelry, Blouse, Sandals, and Jacket lead in Accessories, Clothing, Footwear, and Outerwear respectively
9. **Repeat Buyers & Subscriptions** — Among customers with >5 purchases: 2,518 are non-subscribers vs. 958 subscribers
10. **Revenue by Age Group** — Young Adults lead at $62,143, followed by Middle-aged ($59,197), Adult ($55,978), Senior ($55,763)

---

## 📊 Power BI Dashboard

An interactive **Customer Behavior Dashboard** was built featuring:
- KPI cards: Total Customers (3.9K), Average Purchase Amount ($59.76), Average Review Rating (3.75)
- Subscription status breakdown (Yes 27% / No 73%)
- Revenue and Sales by Category
- Revenue and Sales by Age Group
- Filter slicers for Subscription Status, Gender, Category, and Shipping Type

---

## 💡 Business Recommendations

- **Boost Subscriptions** — Promote exclusive perks and benefits to grow the subscriber base beyond the current 27%
- **Customer Loyalty Programs** — Reward repeat buyers to convert Returning customers into the Loyal segment
- **Review Discount Policy** — Balance discount-driven sales with margin control, especially for high-dependency products like Hats and Sneakers
- **Product Positioning** — Feature top-rated products (Gloves, Sandals, Boots) prominently in marketing campaigns
- **Targeted Marketing** — Prioritize Young Adults and Express shipping users, who represent the highest revenue segments

---

## 📁 Project Structure

```
├── data/
│   └── customer_shopping_behavior.csv
├── notebooks/
│   └── Customer_Behaviour_Analysis.ipynb
├── sql/
│   └── SQL file.sql
├── dashboard/
│   └── customer_behavior_analysis.pbix
└── README.md
```

---
