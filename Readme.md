# 🛒 Customer Segmentation Analysis Using RFM & K-Means Clustering

## 📋 Project Overview

This project implements **customer segmentation analysis** using **RFM (Recency, Frequency, Monetary) analysis** combined with **K-Means clustering** to identify distinct customer groups and provide actionable business insights for targeted marketing strategies.

The analysis transforms raw transactional data into meaningful customer segments, enabling businesses to:
- Identify high-value customers (VIPs)
- Detect at-risk customers for retention campaigns  
- Optimize marketing spend through targeted strategies
- Improve customer lifetime value

## 🎯 Business Problem

Understanding customer behavior is crucial for business success. This project addresses:
- **Customer Retention**: Identifying customers at risk of churning
- **Revenue Optimization**: Focusing efforts on high-value customer segments
- **Marketing Efficiency**: Tailoring campaigns to specific customer profiles
- **Resource Allocation**: Prioritizing customer relationship management efforts

## 📊 Dataset

The analysis uses **Online Retail Dataset** containing:
- **536,641 transactions** from December 2010 to December 2011
- **4,338 unique customers** across multiple countries
- **Key Features**: InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country

### Data Quality & Preprocessing
- Removed negative quantities and prices (returns/adjustments)
- Handled missing CustomerID values
- Created TotalAmount feature (Quantity × UnitPrice)
- Applied data cleaning and validation steps

## 🔧 Technical Implementation

### **RFM Analysis**
The core methodology involves calculating three key metrics for each customer:

- **Recency (R)**: Days since last purchase (lower = better)
- **Frequency (F)**: Total number of unique transactions (higher = better)  
- **Monetary (M)**: Total amount spent (higher = better)

### **Machine Learning Pipeline**
1. **Data Preprocessing**: StandardScaler normalization
2. **Dimensionality Reduction**: PCA (Principal Component Analysis) 
3. **Clustering Algorithm**: K-Means with optimal k selection via Elbow Method
4. **Validation**: Silhouette Score analysis for cluster quality

### **Key Technologies**
- **Python Libraries**: pandas, numpy, scikit-learn, matplotlib, seaborn, plotly
- **Clustering**: K-Means Algorithm
- **Dimensionality Reduction**: PCA (3 components)
- **Visualization**: Interactive plots and statistical charts

## 📈 Results & Customer Segments

### 🔹 **Cluster 0: Loyal Mid-Tier Customers** (🟢)
- **Recency**: ~44 days (recent & active)
- **Frequency**: ~5 purchases (moderate repeaters)  
- **Monetary**: ~$1,535 total spend (medium value)
- **Strategy**: Upsell/cross-sell opportunities to increase spend

### 🔹 **Cluster 1: Regular Low-Spenders** (🟡)  
- **Recency**: ~47 days (fairly recent)
- **Frequency**: ~4.5 purchases (moderate activity)
- **Monetary**: ~$1,214 total spend (lower value)
- **Strategy**: Bundle offers and discounts to increase basket size

### 🔹 **Cluster 2: At-Risk/Lost Customers** (🔴)
- **Recency**: ~257 days (inactive for 8+ months)
- **Frequency**: ~1.5 purchases (almost one-time buyers)
- **Monetary**: ~$357 total spend (low value)  
- **Strategy**: Win-back campaigns and reactivation offers

### 🔹 **Cluster 3: VIP Customers** (🌟)
- **Recency**: ~3 days (extremely recent)
- **Frequency**: ~86 purchases (highly frequent)
- **Monetary**: ~$35,223 total spend (premium value)
- **Strategy**: Loyalty rewards, exclusive offers, premium service

## 📊 Key Insights & Business Impact

### **Revenue Distribution**
- **Cluster 3 (VIPs)** represents only **0.6%** of customers but contributes **~60%** of total revenue
- **Cluster 2 (At-Risk)** represents **39%** of customers but only **6%** of revenue


---
⭐ **If you found this project helpful, please give it a star!** ⭐
