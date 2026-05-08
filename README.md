# End-to-End Scalable Customer Behavioral Segmentation

## 📌 Project Overview
This project focuses on segmenting a large-scale retail dataset (>1 million records) into distinct customer personas. By combining **Big Data Engineering** (PySpark) and **Machine Learning** (K-Means++), 
we derived actionable insights to optimize marketing budget allocation and customer retention strategies, specifically tailored for banking or retail environments.

## 🛠️ Technical Stack
- **Data Engineering:** Apache Spark (PySpark) for distributed data processing.
- **Data Science:** Scikit-Learn (PowerTransformer, K-Means++, PCA, GMM).
- **Visualization:** Matplotlib, Seaborn, and **Power BI** for executive dashboards.
- **Environment:** VS Code, Jupyter Notebook.

## 🚀 Data Pipeline & Methodology
1. **ETL & Cleaning:** Processed 1M+ raw transaction logs using PySpark. Handled dirty data (type coercion) and aggregated daily logs into customer-level metrics.
2. **Feature Engineering:** Beyond standard RFM, I engineered behavioral features: `Avg_Discount_Percent`, `Avg_Session_Duration`, and `Coupon_Usage_Rate`.
3. **Preprocessing:** Applied **Yeo-Johnson Power Transformation** to handle extreme skewness and outliers in financial data.
4. **Clustering:** Implemented **K-Means++** with $K=4$ (optimized via Elbow Method and Silhouette Analysis).

## 📊 Business Personas & Insights
Through the clustering process, 4 strategic segments were identified:
- **Cluster 0 (Premium Spenders):** High monetary value (~$514), low discount sensitivity. *Strategy: VIP/Priority banking offers.*
- **Cluster 1 (Bargain Hunters):** High coupon usage (100%) and high discount rate (13%). *Strategy: Flash sales and cashback incentives.*
- **Cluster 2 (Recent Organics):** New active users with 0% coupon usage. *Strategy: Loyalty point onboarding.*
- **Cluster 3 (Dormant Customers):** High recency (inactive for >500 days). *Strategy: Re-engagement/Win-back campaigns.*

## 📁 Repository Structure
- `src/01_data_pipeline.py`: PySpark script for data cleaning and aggregation.
- `src/02_modeling.ipynb`: Jupyter notebook for ML modeling and evaluation.
- `data/`: Folder for raw and processed datasets (ignored in .gitignore).
