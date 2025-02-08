# AllLife-Bank-Credit-Card-Customer-Segmentation
 Data Analysis | Clustering | Python 


## Overview
This project involves developing customer segmentation to provide personalized recommendations for products like savings plans, loans, and wealth management. By analyzing the credit card usage behavior of 9000 customers over six months, we aim to identify patterns and group customers into meaningful segments using clustering techniques.

## Objective
Create customer segments based on credit card behavior.
Provide actionable insights and recommendations tailored to each segment.
Dataset Description
The dataset summarizes the usage behavior of approximately 9000 active credit card holders. It includes 18 behavioral variables that capture details such as balance, payments, purchases, and transaction frequency.

## Attribute Information
![image](https://github.com/user-attachments/assets/e530fe67-63a3-4187-b2cb-940d5453e37d)


## 📌 Steps and Workflow

🔹 **1. Importing Libraries**  
   Essential libraries like `pandas`, `numpy`, `matplotlib`, and clustering tools (**K-Means, DBSCAN, etc.**) were imported for **data processing, visualization, and clustering**.

🔹 **2. Loading the Dataset**  
   The dataset was **imported using `pandas`**, and a preview of the first five records was displayed.

🔹 **3. Exploratory Data Analysis (EDA) & Data Cleaning**  
   - 🟢 **Handled missing values, duplicates, and outliers**  
   - 🟢 Null values in `MINIMUM_PAYMENTS` and `CREDIT_LIMIT` were replaced with the column mean.  
   - 🟢 The `CUST_ID` column was dropped as it is **not relevant for clustering**.  

🔹 **4. Correlation Analysis**  
   - **`PURCHASES` and `ONEOFF_PURCHASES`** (**0.86**)  
   - **`PURCHASES_FREQUENCY` and `PURCHASES_INSTALLMENT_FREQUENCY`** (**0.85**)  
   - **`CASH_ADVANCE_TRX` and `CASH_ADVANCE_FREQUENCY`** (**0.81**)  

🔹 **5. Data Scaling**  
   📊 **Standardized** the dataset using `StandardScaler` to ensure equal importance for all attributes.

🔹 **6. Dimensionality Reduction**  
   🏷️ Applied **PCA** for visualizing data in a **two-dimensional space**.

🔹 **7. Optimal Clusters (Elbow Method)**  
   📈 Used the **Elbow Method** to determine the **optimal number of clusters**.

🔹 **8. Model Building and Clustering**  
   🚀 Applied **K-Means clustering** with **4 clusters (`n_clusters=4`)**.

🔹 **9. Cluster Analysis**  
   - 🎯 **Cluster 1 (Transactors):** Customers with **low balances, low cash advances, and frequent full payments**.  
   - 🎯 **Cluster 2 (Revolvers):** Customers with **high balances, high cash advances, and low full payments**.  
   - 🎯 **Cluster 3 (VIP/Prime):** Customers with **high credit limits, high full payment rates, and potential for increased spending**.  
   - 🎯 **Cluster 4 (Low Tenure):** Customers with **low tenure and moderate balances**.  

## Results
Identified 4 customer segments with distinct behavior patterns.
Generated recommendations for personalized financial products and services based on cluster characteristics. 
