# 🛍️ CloudCart: E-Commerce Analytics using AWS  

![dashboard](https://github.com/user-attachments/assets/f45c7d28-fc0f-4950-89d5-d742a55c2c04)


---

## 📌 Table of Contents  
- [Overview](#overview)  
- [Business Problem](#business-problem)  
- [Dataset](#dataset)  
- [Tools & Technologies](#tools--technologies)  
- [Project Structure](#project-structure)  
- [Data Cleaning & Preparation](#data-cleaning--preparation)  
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)  
- [Research Questions & Key Findings](#research-questions--key-findings)  
- [Dashboard](#dashboard)  
- [How to Run This Project](#how-to-run-this-project)  
- [Final Recommendations](#final-recommendations)  
- [Author & Contact](#author--contact)  

---

## Overview  
This project demonstrates an **end-to-end E-Commerce Analytics System** powered by **Amazon Web Services (AWS)**. It enables real-time sales, customer, and performance tracking through an automated data pipeline built using AWS services such as **S3, Glue, Athena**.  

The solution helps e-commerce teams uncover **revenue trends, customer insights, and product performance** while improving **marketing ROI** and **operational efficiency** through interactive Tableau dashboards.  

---

## Business Problem  
Modern e-commerce platforms collect large volumes of customer and sales data from multiple sources. Without proper automation, these datasets remain siloed and underutilized, limiting business intelligence.  

This project aims to solve key challenges by:  
1. Building a **cloud-based data pipeline** to automate ETL (Extract-Transform-Load) using AWS.  
2. Enabling **real-time analytics** with Athena and QuickSight.  
3. Identifying **top-selling products, regions, and customer segments**.  
4. Providing a **data-driven dashboard** to improve strategic decisions.  

---

## Dataset  
- **Sales Data:** Product ID, category, units sold, total revenue, and region.  
- **Customer Data:** Customer ID, age group, gender, country, purchase frequency.  
- **Marketing Data:** Campaign spend, conversion rate, and ROI metrics.  
- Raw CSV data files are stored in **Amazon S3** and processed using **AWS Glue** before being queried via **Athena**.  

---

## Tools & Technologies  
- **Amazon S3** → Cloud storage for raw and processed data  
- **AWS Glue** → Automated ETL and data transformation  
- **AWS Athena** → Serverless SQL-based data querying  
- **AWS QuickSight** → Interactive dashboard and KPI visualization  
- **Python (Pandas, NumPy, Boto3)** → Custom scripts for data prep  
- **GitHub** → Version control and documentation  

---

## 📂 Project Structure  

```
ecommerce-aws-analytics/
│
├── README.md                  # Project documentation
├── requirements.txt            # Python dependencies
├── .gitignore                  # Ignore credentials/system files
│
├── data/                       # Raw & processed data (CSV/Parquet)
│   ├── sales.csv
│   ├── customers.csv
│   └── marketing.csv
│
├── scripts/                    # Python ETL & S3 interaction scripts
│   ├── data_upload_s3.py
│   ├── glue_etl_script.py
│   └── athena_queries.sql
│
├── glue_jobs/                  # AWS Glue transformation scripts
│   └── ecommerce_etl_job.py
│
├── notebooks/                  # EDA & validation notebooks
│   ├── exploratory_analysis.ipynb
│   └── sales_forecasting.ipynb
│
├── dashboard/                  # QuickSight screenshots or links
│   └── ecommerce_dashboard.png
│
├── reports/                    # Project reports and documentation
│   └── analytics_summary.pdf
│
└── logs/                       # Glue & Athena logs
```
---

## Data Cleaning & Preparation

- Removed duplicate transactions and missing order IDs.

- Standardized currency and date formats.

- Derived new metrics (profit margin, conversion rate, customer lifetime value).

- Partitioned processed data in S3 for optimized Athena queries.

---

## Exploratory Data Analysis (EDA)

- Category Trends: Electronics and Apparel lead in total sales volume.

- Customer Insights: Repeat purchase rate = 38%; high-value customers prefer Express Delivery.

- Seasonality: Sales peaks in November (Holiday Season).

- Marketing ROI: 23% uplift in conversions after campaign optimization.

---

## Research Questions & Key Findings

1.Which product categories generate the most revenue?
- Electronics & Fashion contribute 57% of total revenue.

2.Which region has the highest conversion rate?
- GCC region shows 1.4× higher conversion compared to APAC.

3.Does marketing spend correlate with sales growth?
- Strong positive correlation (r = 0.82).

4.Which customer segments drive profitability?
- Loyal customers with ≥3 purchases per quarter deliver 65% of profits.

---

## Dashboard

The AWS QuickSight Dashboard provides:

- KPI Overview: Sales, Profit, Orders, Conversion Rate

- Category & Region Performance: Dynamic filters and drill-downs

- Customer Insights: Retention trends and churn analysis

- Marketing ROI: Spend vs Return breakdown

---

## How to Run This Project

1.Clone the Repository
- git clone https://github.com/yourusername/ecommerce-aws-analytics.git
- cd ecommerce-aws-analytics

2.Install Dependencies
- pip install -r requirements.txt

3.Upload Data to AWS S3
- Create an S3 bucket (e.g., ecommerce-data-raw)

4.Upload your CSV files from /data/
- Run AWS Glue ETL Job

5.Use /glue_jobs/ecommerce_etl_job.py to process and clean data.
- Store processed outputs in S3 (/processed/).

6.Query with AWS Athena
- Configure Athena to read processed data.

7.Execute queries from /scripts/athena_queries.sql.
- Open Dashboard

8.Import data into Tableau.
- Visualize using the prebuilt dashboard template (/dashboard/).

---

## Final Recommendations

- Automate ETL jobs daily with AWS Glue & CloudWatch triggers.

- Track customer churn using retention analysis and loyalty scores.

- Increase marketing spend in high-conversion regions.

- Expand personalized recommendations using ML-based models.

- Deploy real-time monitoring for top 10 product categories.


---
## 👤 Author & Contact

Sandra Raj P
Data Analyst 

📧 Email: sandraraj36@gmail.com

🔗 LinkedIn: [linkedin.com/in/sandrarajp]

📂 Portfolio: [https://sandra-zvtm.vercel.app/]
