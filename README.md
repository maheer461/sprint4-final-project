# sprint4-final-project
# Olist E-Commerce Customer Behavior Analysis

## Project Overview

This project performs a comprehensive Exploratory Data Analysis (EDA) on the Olist Brazilian E-Commerce dataset. The analysis examines customer behavior, order trends, product category performance, geographic distribution, and the relationship between delivery speed and customer satisfaction. The goal is to provide data-driven business recommendations to improve operational efficiency and customer experience.

### Dataset

The analysis uses 7 CSV files from the Olist e-commerce platform:

| File | Description |
|------|-------------|
| olist_orders_dataset.csv | Orders with timestamps and status (99,441 rows) |
| olist_order_items_dataset.csv | Items per order with price and freight (112,650 rows) |
| olist_customers_dataset.csv | Customer ID, city, state (99,441 rows) |
| olist_products_dataset.csv | Products with category and dimensions (32,951 rows) |
| olist_order_reviews_dataset.csv | Review scores 1-5 stars (99,224 rows) |
| olist_order_payments_dataset.csv | Payment type and value (103,886 rows) |
| product_category_name_translation.csv | Portuguese to English category names (71 rows) |

### Tools & Technologies

- Python 3.11
- pandas (data manipulation)
- SQLite (in-memory database for SQL queries)
- matplotlib (visualization)
- Google Colab (development environment)

---

## Methodology

### 1. Data Inspection & Cleaning
- Examined data shapes, column types, and missing values
- Converted timestamp columns to datetime format for time-based analysis
- Handled missing values in Age and Embarked columns

### 2. SQL Analysis
- Queried order status distribution using aggregation
- Joined orders and items tables to identify highest-revenue orders
- Aggregated customer counts by geographic state

### 3. pandas Analysis
- Merged products with translation table for English category names
- Combined items, products, and reviews for category-level revenue and satisfaction analysis
- Created pivot tables for multidimensional aggregation

### 4. Visualization
- Bar chart: Top 10 customer states
- Line chart: Monthly order volume trends
- Bar chart: Average delivery days by review score

### 5. Statistical Analysis
- Calculated correlation between delivery days and review scores
- Grouped average delivery times by review score (1-5 stars)

---

## Key Findings

### Business Health
- **97% delivery rate** (96,478 of 99,441 orders successfully delivered)
- Only **0.6% cancellation rate**
- Monthly orders grew from **800 (Jan 2017)** to **7,544 (Nov 2017)** – an **843% increase**
- Sustained volume of **6,000–7,500 orders per month** throughout 2018

### Top Product Categories
| Category | Revenue | Avg Review Score |
|----------|---------|------------------|
| Health & Beauty | $1.45M | 4.14 ⭐ |
| Watches & Gifts | $1.31M | 4.02 ⭐ |
| Bed & Bath | $1.26M | 3.90 ⭐ |
| Sports & Leisure | $1.16M | 4.11 ⭐ |
| Cool Stuff | $0.72M | 4.15 ⭐ |

### Customer Geography
- **São Paulo (SP)** dominates with **42% of all customers** (41,746 customers)
- Top 3 states (SP, RJ, MG) account for **66% of customer base**
- Significant concentration in Southeast region

### Delivery Speed vs. Customer Satisfaction
- **Correlation: -0.334** (moderate negative relationship)
- **5-star reviews:** 10.2 average delivery days
- **1-star reviews:** 20.8 average delivery days
- Customers waiting 10+ additional days are significantly more likely to leave low ratings

---

## Recommendations

**Invest in a regional fulfillment center in São Paulo (SP).**

- 42% of customers are concentrated in one state
- Reducing delivery time from 20+ days to under 10 days could raise review scores by 1-2 stars
- Improved satisfaction directly impacts customer retention and repeat purchase rates

---

## How to Run This Project

1. Clone the repository
2. Open the notebook in Google Colab or Jupyter Notebook
3. Run cells sequentially from setup through Question 10

```bash
git clone https://github.com/maheer461/sprint4-final-project
