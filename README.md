# Customer Segmentation & Marketing Analytics Dashboard

## Project Overview
An end-to-end marketing analytics project designed to evaluate customer purchasing behavior, category revenue generation, and high-value customer segments using SQL and Power BI.

## Tools & Technologies
* **Database & Querying:** MySQL (Aggregations, Grouping, Filtering)
* **Data Visualization:** Power BI (KPI Cards, Bar Charts, Donut Charts, DAX)

## SQL Queries Used
### 1. Overall Category Performance
```sql
SELECT 
    preferred_category,
    COUNT(id) AS total_customers,
    ROUND(AVG(income), 2) AS avg_income,
    ROUND(AVG(spending_score), 2) AS avg_spending_score,
    ROUND(SUM(last_purchase_amount), 2) AS total_revenue
FROM customer_segmentation_data
GROUP BY preferred_category
ORDER BY total_revenue DESC;
