# 🛒 E-Commerce Sales & Customer Behavior Analysis

An intermediate-level **Data Analysis and Business Intelligence project** analyzing e-commerce sales, customer behavior, product performance, purchasing patterns, profitability, delivery performance, and customer trends using Python and Power BI.

The project combines **data cleaning, exploratory data analysis (EDA), statistical analysis, business insights, data visualization, and an interactive Power BI dashboard**.

---

## 📌 Project Overview

The goal of this project is to analyze an e-commerce dataset covering transactions from **2021–2025** and identify meaningful patterns in:

* Sales performance
* Customer behavior
* Product and category performance
* Purchasing patterns
* Discounts and profitability
* Delivery performance
* Customer ratings
* Seasonal sales trends
* Customer segmentation
* Customer concentration

The analysis was performed using **Python/Jupyter Notebook**, while **Power BI** was used to create an interactive business dashboard.

---

## 🎯 Business Objectives

This project aims to answer questions such as:

1. Which product categories generate the highest sales?
2. Which products contribute most to revenue?
3. How do sales change over time?
4. Are there seasonal sales patterns?
5. How does purchase quantity relate to order value?
6. How do discounts affect profitability?
7. Are late deliveries associated with lower customer ratings?
8. How do different customer segments behave?
9. Is revenue concentrated among a small group of customers?
10. What business insights can be obtained from the data?

---

## 🗂️ Dataset

The project uses an e-commerce dataset containing information about:

* Customers
* Orders
* Products
* Order items
* Sales
* Discounts
* Profit
* Delivery
* Customer ratings
* Customer reviews
* Marketing channels
* Customer segments

### Dataset Files

```text
customer_master.csv
dataset_statistics.csv
ecommerce_sales_customer_analytics_150k.csv
order_items.csv
product_catalog.csv
```

### Main dataset relationships

```text
customer_master
       │
       │ customer_id
       ▼
ecommerce_sales_customer_analytics_150k
       │
       │ order_id
       ▼
order_items
       │
       │ product_id
       ▼
product_catalog
```

---

# 🧹 Data Cleaning & Preparation

The data was inspected and prepared before performing the analysis.

### Data preparation included:

* Missing-value analysis
* Duplicate detection
* Data type validation
* Date conversion
* Time conversion
* Numerical data inspection
* Outlier analysis
* Profit validation
* Derived feature creation

### Derived features

The following analytical features were created:

```text
Year
Month
Month_Name
Day
Day_Name
Quarter
Quarter_Name
Profit_Per_Item
Discount_Percentage
Order_Hour
Delivery_Difference
Discount_Band
Delivery_Performance
```

The cleaned dataset was exported for Power BI:

```text
data/processed/ecommerce_cleaned.csv
```

---

# 📊 Exploratory Data Analysis

The project includes several stages of exploratory analysis.

## 1. Univariate Analysis

Individual variables were analyzed using:

* Histograms
* Count plots
* Box plots
* Distribution plots
* Category frequency analysis

Topics included:

* Sales distribution
* Profit distribution
* Quantity distribution
* Customer age
* Ratings
* Discounts
* Delivery days
* Customer segments

---

## 2. Bivariate Analysis

Relationships between two variables were investigated using:

* Scatter plots
* Bar charts
* Box plots
* Grouped comparisons

Examples:

* Quantity vs Net Sales
* Discount vs Profit
* Delivery performance vs Customer Rating
* Customer segment vs sales
* Category vs sales

---

## 3. Multivariate Analysis

Multiple variables were analyzed together to identify more complex patterns.

Examples included:

* Category + sales + quantity
* Customer segment + sales + profit
* Delivery performance + ratings + order volume

---

# 📈 Statistical Analysis

Descriptive statistics were calculated for important numerical variables.

The analysis included:

* Mean
* Median
* Standard deviation
* Minimum
* Maximum
* Quartiles
* Correlation analysis
* Distribution analysis
* Group comparisons

---

# 👥 Customer Analysis

Customer behavior was analyzed using:

* Customer type
* Customer segment
* Repeat customer status
* Customer order count
* Customer lifetime value
* Customer spending
* Customer concentration

The dataset contains approximately **24,911 unique customers**.

The analysis also compared:

* New vs returning customers
* Business vs Consumer vs Premium vs VIP customers
* High-value vs lower-value customers

---

# 🛍️ Product & Category Analysis

Product-level and category-level performance were analyzed using the product and order-item datasets.

The analysis examined:

* Product sales
* Product quantity
* Product pricing
* Product profitability
* Product categories
* Top-performing products

---

# ⏰ Time-Based Analysis

Sales were analyzed across different time dimensions:

* Year
* Quarter
* Month
* Day
* Day of week
* Order hour

This helped identify seasonal and temporal purchasing patterns.

---

# 💡 Key Business Insights

## 1. Electronics generated the highest sales

Electronics generated approximately **41.15M** in total sales, the highest among the analyzed categories.

The category did not have unusually high average purchase quantities. Instead, it contained several relatively high-value products, with many top-selling products having average prices above 1,200.

For example, products such as gaming consoles, TVs, tablets, and smart watches generated more than 850K in sales despite moderate quantities.

This suggests that **product value and pricing played an important role** in the strong revenue contribution of Electronics.

---

## 2. November and December showed strong seasonal sales

The analysis identified a recurring seasonal pattern where **November and December generated the highest monthly sales**, while February recorded the lowest.

For example, in 2021:

| Month    | Total Sales | Average Sales/Order | Orders |
| -------- | ----------: | ------------------: | -----: |
| February |       1.91M |            1,217.52 |  1,565 |
| November |       4.23M |            1,349.05 |  3,139 |
| December |       4.90M |            1,373.59 |  3,568 |

The year-end peak was associated with both **higher order volume and higher average order value**.

---

## 3. Annual sales remained relatively stable

Annual net sales remained around **35M per year** from 2021 to 2025.

| Year | Total Sales | Average Sales/Order | Orders |
| ---- | ----------: | ------------------: | -----: |
| 2021 |      35.72M |            1,296.46 | 27,554 |
| 2022 |      35.33M |            1,281.67 | 27,564 |
| 2023 |      35.53M |            1,285.76 | 27,632 |
| 2024 |      35.47M |            1,277.24 | 27,768 |
| 2025 |      35.09M |            1,271.44 | 27,598 |

Order volume remained remarkably stable while average sales per order gradually declined.

Therefore, the data indicates **stable purchasing volume with a modest decline in average order value**.

---

## 4. Higher quantities were associated with higher order value

A positive relationship was observed between quantity purchased and net sales.

Examples:

| Quantity | Average Net Sales |
| -------: | ----------------: |
|        1 |            250.84 |
|        5 |          1,175.59 |
|       10 |          2,243.41 |
|       15 |          2,926.27 |
|       20 |          3,486.52 |

The correlation between **Quantity and Net Sales was approximately 0.595**, indicating a moderate positive relationship.

However, high-quantity orders were much less frequent. Therefore, larger orders generated higher value per order but represented a relatively small portion of total orders.

---

## 5. Higher discounts were generally associated with lower profitability

Average profit generally decreased as discount levels increased.

| Discount | Average Profit |
| -------- | -------------: |
| 0–5%     |         678.69 |
| 5–10%    |         632.43 |
| 10–15%   |         578.70 |
| 15–20%   |         494.17 |
| 20–30%   |         506.00 |
| 30–40%   |         421.99 |
| 40–50%   |         200.76 |
| 50–60%   |         -24.40 |

The correlation between **Discount % and Profit was approximately -0.237**.

The 50–60% discount group recorded negative average profit, suggesting that very high discounts can result in losses.

The relationship was not perfectly linear, so the finding is described as a **general association rather than a rule that every discount increase reduces profit**.

---

## 6. Late deliveries were associated with lower customer ratings

Delivery performance showed a noticeable relationship with customer ratings.

| Delivery Performance | Average Rating |
| -------------------- | -------------: |
| 2+ days early        |           4.01 |
| 1 day early          |           4.02 |
| On time              |           3.73 |
| 1 day late           |           3.22 |
| 2 days late          |           3.23 |
| 3+ days late         |           3.22 |

The correlation between **Delivery Difference and Customer Rating was approximately -0.386**.

Late deliveries were associated with lower customer ratings. However, the analysis does not establish that delivery delays alone caused the lower ratings.

---

## 7. Customer segments showed relatively similar average behavior

Average order values were relatively close across customer segments:

| Customer Segment | Average Net Sales |
| ---------------- | ----------------: |
| Business         |          1,289.13 |
| Consumer         |          1,285.12 |
| VIP              |          1,282.74 |
| Premium          |          1,274.10 |

Average profit was also relatively similar.

Consumer customers generated the highest total sales, mainly because they accounted for the largest number of orders rather than because their individual orders were dramatically more valuable.

Premium and VIP customers purchased slightly more items per order on average.

---

## 8. Sales were broadly distributed across customers

The analysis found that revenue was not heavily concentrated among a small number of customers.

| Customer Group | Share of Total Sales |
| -------------- | -------------------: |
| Top 10         |               0.158% |
| Top 50         |               0.706% |
| Top 100        |               1.328% |
| Top 500        |               5.518% |

The dataset contains approximately **24,911 customers**.

The median customer spending was approximately **6,516.90**, while the mean was approximately **7,110.68**.

This indicates that overall revenue was distributed across a relatively broad customer base rather than being dominated by a small number of customers.

---

# 📊 Power BI Dashboard

An interactive Power BI dashboard was created to allow users to explore the results dynamically.

### Dashboard includes:

### KPI Cards

* Total Sales
* Total Orders
* Total Customers
* Average Order Value
* Total Quantity

### Visualizations

* Sales Trend
* Sales by Product Category
* Top 10 Products
* Sales by Customer Type
* Sales by Region
* Monthly Sales Trend

### Interactive Filters

* Order Date
* Category
* Product
* Region
* Customer Type

Users can select a category such as **Electronics**, and the dashboard updates the relevant visuals and KPIs.

---

# 🛠️ Technologies & Tools

### Programming & Data Analysis

* Python
* Pandas
* NumPy

### Data Visualization

* Matplotlib
* Seaborn

### Business Intelligence

* Microsoft Power BI

### Development Environment

* Jupyter Notebook
* VS Code

### Dataset Source

* Kaggle

---

# 📁 Project Structure

```text
E-Commerce-Customer-Sales-Analysis/
│
├── data/
│   ├── raw/
│   │   ├── customer_master.csv
│   │   ├── dataset_statistics.csv
│   │   ├── ecommerce_sales_customer_analytics_150k.csv
│   │   ├── order_items.csv
│   │   └── product_catalog.csv
│   │
│   └── processed/
│       ├── ecommerce_cleaned.csv
│       ├── category_sales.csv
│       └── product_summary.csv
│
├── notebooks/
│   └── ecommerce_analysis.ipynb
│
├── visualizations/
│   └── dashboard.png
│
├── powerbi/
│   └── ecommerce_dashboard.pbix
│
└── README.md
```

---

# 🔬 Analysis Workflow

The project followed this workflow:

```text
1. Dataset Selection
        ↓
2. Dataset Understanding
        ↓
3. Data Loading
        ↓
4. Data Quality Inspection
        ↓
5. Missing Value Analysis
        ↓
6. Duplicate Detection
        ↓
7. Data Type Conversion
        ↓
8. Feature Engineering
        ↓
9. Univariate Analysis
        ↓
10. Bivariate Analysis
        ↓
11. Multivariate Analysis
        ↓
12. Descriptive Statistics
        ↓
13. Customer Analysis
        ↓
14. New vs Returning Customer Analysis
        ↓
15. Product Analysis
        ↓
16. Time-Based Analysis
        ↓
17. Day-of-Week Analysis
        ↓
18. Correlation Analysis
        ↓
19. Distribution Analysis
        ↓
20. Group Comparisons
        ↓
21. Business Insights
        ↓
22. Power BI Dashboard
        ↓
23. Interactive Dashboard Testing
```

---

# 📌 Conclusion

This project demonstrates an end-to-end **data analysis and business intelligence workflow**, from raw e-commerce data through cleaning, exploratory analysis, statistical analysis, visualization, business insight generation, and interactive dashboard development.

The analysis identified important patterns related to:

* Product value
* Seasonal purchasing
* Stable order volume
* Quantity and order value
* Discount and profitability
* Delivery performance and customer satisfaction
* Customer segments
* Customer revenue concentration

The Power BI dashboard provides an interactive way to explore these patterns using multiple filters and business-focused visualizations.

---

## 👩‍💻 Author

**Hirushi Fernando**

BSc (Hons) Computer Science — Upper Second Class Honours (2:1)

**Areas of Interest:**
Data Science | Artificial Intelligence | Machine Learning | Data Analytics

---

⭐ If you find this project useful, feel free to explore the notebook and Power BI dashboard.
