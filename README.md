# 🚀 Purchase Order Tracking Dashboard

A comprehensive open-source dashboard to simulate a real-world procurement environment and track purchase order lifecycles, supplier performance, spend analytics, and delivery using Python, Plotly, and HTML in Google Colab.

![Status-Active](https://img.shields.io/badge/Status-Active-brightgreen) ![Python-3.8+](https://img.shields.io/badge/Python-3.8%2B-blue) ![License-MIT](https://img.shields.io/badge/License-MIT-yellow) ![Colab](https://img.shields.io/badge/Google-Colab-F9AB00)

## 📊 Project Overview

This dashboard helps procurement and operations teams:
- Monitor end-to-end **Purchase Order (PO) lifecycle** from creation to delivery  
- Benchmark **supplier performance** (on-time delivery, delays, ratings)  
- Analyze **spend** by category, supplier, and period  
- Identify **risk** and **optimization** opportunities (cycle times, cost savings)  
- Forecast **demand** and predict **delivery delays** with machine learning  

## 🔗 Dataset

We use the **Brazilian E-Commerce Public Dataset by Olist** from Kaggle (100k orders, 2016–2018):

Kaggle: https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

**Files** (CSV):  
1. `olist_customers_dataset.csv`  
2. `olist_geolocation_dataset.csv`  
3. `olist_order_items_dataset.csv`  
4. `olist_order_payments_dataset.csv`  
5. `olist_order_reviews_dataset.csv`  
6. `olist_orders_dataset.csv`  
7. `olist_products_dataset.csv`  
8. `olist_sellers_dataset.csv`  
9. `product_category_name_translation.csv`  

## 🎯 Key Modules

### 1. Environment Setup & Drive Mount  
- Install interactive table formatter (`itables`)  
- Mount Google Drive and set `DATA_DIR`  

### 2. Imports & Utility Functions  
- Core libraries: `pandas`, `numpy`, `datetime`, `IPython.display`  
- `styled_df()` for colored, interactive DataFrame styling  

### 3. Data Loading  
- Read all CSV files into Pandas DataFrames  
- Display schema and preview for validation  

### 4. Data Cleaning & Parsing  
- Standardize datetime columns in `orders`  
- Handle missing values and convert types  

### 5. Feature Engineering & Joins  
- Merge product translations, customer, seller, payment, review, and geolocation data  
- Compute **delivery_delay** (days) & extract **order_month**  

### 6. KPI Calculations  
- **Total Orders**, **Total Spend**, **Avg. Cycle Time**, **On-Time Rate** displayed via HTML KPI cards  

### 7. Supplier Performance Scorecard  
- Top 10 suppliers by spend, orders count, avg delay, on-time rate  

### 8. Trend & Breakdown Analysis  
- **Monthly Trend**: Orders, Spend & Cycle Time  
- **Category Spend**: Spend by product category  

### 9. Interactive Visualizations (8 Charts)  
1. Monthly Orders vs. Spend (dual-axis Plotly)  
2. Spend vs. Delivery Delay (scatter)  
3. Spend Heatmap by Category × Month  
4. Top 10 Sellers: Volume & On-Time Rate (bar)  
5. Delivery Delay Distribution by Category (box)  
6. Histogram of Delivery Delays  
7. Geographic Scatter of Orders on Map  
8. HTML KPI Card Panel  

### 10. Predictive Models  
- **Demand Forecasting**: Linear Regression on monthly order counts, 6-month forecast  
- **Delivery Delay Classification**: Random Forest to predict on-time vs. delayed  

## 🛠️ Technology Stack

- **Python 3.8+**  
- **Pandas**, **NumPy** – Data wrangling  
- **Plotly** – Interactive visualizations  
- **scikit-learn** – Predictive modeling  
- **IPython.display.HTML** – HTML KPI and card panels  
- **Google Colab** – Cloud notebook environment  

## 🚀 Quick Start

### Google Colab (Recommended)  
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/your-username/po-tracking-dashboard/blob/main/PO_Tracking_Dashboard.ipynb)

1. Click the **Open In Colab** badge  
2. Update `DATA_DIR` to your Google Drive folder path  
3. Run all cells sequentially (Runtime → Run all)  
4. Explore interactive tables, charts, and machine learning results  



