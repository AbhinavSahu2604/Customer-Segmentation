# Customer-Segmentation
 Data Analysis | Clustering | Python 

Customer Segmentation for AllLife Bank
Overview
This project involves developing customer segmentation to provide personalized recommendations for products like savings plans, loans, and wealth management. By analyzing the credit card usage behavior of 9000 customers over six months, we aim to identify patterns and group customers into meaningful segments using clustering techniques.

Objective
Create customer segments based on credit card behavior.
Provide actionable insights and recommendations tailored to each segment.
Dataset Description
The dataset summarizes the usage behavior of approximately 9000 active credit card holders. It includes 18 behavioral variables that capture details such as balance, payments, purchases, and transaction frequency.

Attribute Information
Attribute	Description
CUSTID	Identification of Credit Card holder (Categorical)
BALANCE	Balance amount left in the account
BALANCEFREQUENCY	Frequency of balance updates (0 to 1)
PURCHASES	Total amount of purchases made
ONEOFFPURCHASES	Maximum purchase amount in a single transaction
INSTALLMENTSPURCHASES	Total amount of installment purchases
CASHADVANCE	Total cash advance taken
PURCHASESFREQUENCY	Frequency of purchases (0 to 1)
ONEOFFPURCHASESFREQUENCY	Frequency of one-off purchases (0 to 1)
PURCHASESINSTALLMENTSFREQUENCY	Frequency of installment purchases (0 to 1)
CASHADVANCEFREQUENCY	Frequency of cash advances (0 to 1)
CASHADVANCETRX	Number of cash advance transactions
PURCHASESTRX	Number of purchase transactions
CREDITLIMIT	Credit card limit
PAYMENTS	Total amount of payments made
MINIMUM_PAYMENTS	Minimum amount of payments made
PRCFULLPAYMENT	Percentage of full payments made
TENURE	Tenure of credit card service (in months)
Steps and Workflow
1. Importing Libraries
Essential libraries like pandas, numpy, matplotlib, and clustering tools (K-Means, DBSCAN, etc.) were imported for data processing, visualization, and clustering.

2. Loading the Dataset
The dataset was imported using pandas, and a preview of the first five records was displayed to understand its structure and contents.

3. Exploratory Data Analysis (EDA) & Data Cleaning
Data was analyzed for missing values, duplicates, and outliers.
Null values in MINIMUM_PAYMENTS and CREDIT_LIMIT were replaced with the column mean.
The CUST_ID column, which is not relevant for clustering, was dropped.
Outliers were detected and removed for specific attributes like BALANCE, CREDIT_LIMIT, and PAYMENTS.
4. Correlation Analysis
A correlation matrix was generated to identify highly correlated attributes, which include:

PURCHASES and ONEOFF_PURCHASES (0.86)
PURCHASES_FREQUENCY and PURCHASES_INSTALLMENT_FREQUENCY (0.85)
CASH_ADVANCE_TRX and CASH_ADVANCE_FREQUENCY (0.81)
5. Data Scaling
To ensure equal importance for all attributes, the dataset was standardized using StandardScaler, making it suitable for clustering algorithms.

6. Dimensionality Reduction
To visualize the dataset in a two-dimensional space, Principal Component Analysis (PCA) was applied. The first two components were extracted for clustering visualization.

7. Optimal Clusters (Elbow Method)
The Elbow Method was used to determine the optimal number of clusters by plotting inertia against the number of clusters.

8. Model Building and Clustering
K-Means clustering was applied with the optimal number of clusters (n_clusters=4).
Clusters were visualized using the first two PCA components.
9. Cluster Analysis
Each cluster was analyzed based on behavioral attributes. Key insights:

Cluster 1 (Transactors): Customers with low balances, low cash advances, and frequent full payments.
Cluster 2 (Revolvers): Customers with high balances, high cash advances, and low full payments.
Cluster 3 (VIP/Prime): Customers with high credit limits, high full payment rates, and potential for increased spending.
Cluster 4 (Low Tenure): Customers with low tenure and moderate balances.
Results
Identified 4 customer segments with distinct behavior patterns.
Generated recommendations for personalized financial products and services based on cluster characteristics. 
