# 📦 Product Cluster Analysis Using Machine Learning






---

# 📌 Project Overview

Understanding product sales behavior is important for effective inventory management, purchasing decisions, and product portfolio planning.

This project develops an end-to-end Machine Learning clustering pipeline to group products based on their historical retail, transfer, and warehouse sales patterns.

The primary objective is to identify meaningful product segments based on sales activity and provide actionable insights that can support inventory optimization, purchasing decisions, and product portfolio management.

The complete workflow includes:

- Data Collection
- Data Cleaning
- Exploratory Data Analysis (EDA)
- Product-Level Feature Engineering
- Data Transformation
- Data Preprocessing
- K-Means Clustering
- Cluster Evaluation
- PCA Visualization
- Cluster Profiling
- Model Testing
- Business Insights

---

# 🎯 Business Problem

Businesses managing thousands of products need to understand which products have high sales activity and which products have relatively low activity.

Analyzing every product individually can make inventory planning, purchasing, and product portfolio management difficult.

This project applies unsupervised Machine Learning to automatically group similar products based on their historical sales behavior.

The clustering results can support:

- Inventory Management
- Stock Optimization
- Purchasing Decisions
- Product Portfolio Management
- Sales Planning
- Identification of High-Activity Products
- Identification of Low-Activity Products

---

# 📊 Dataset Information

The dataset contains historical warehouse and retail sales information recorded between **2017 and 2020**.

The original dataset contains:

- **307,645 records**
- **9 features**
- **396 suppliers**
- **34,056 unique item codes**
- **8 item types**
- Monthly data from **January to December**

### Original Dataset Features

- YEAR
- MONTH
- SUPPLIER
- ITEM CODE
- ITEM DESCRIPTION
- ITEM TYPE
- RETAIL SALES
- RETAIL TRANSFERS
- WAREHOUSE SALES

The transaction-level dataset was aggregated at the product level to understand the overall sales behavior of each product.

The resulting product-level dataset contains **34,056 unique products**.

### Product-Level Features

The following features were created:

- Total Retail Sales
- Total Retail Transfers
- Total Warehouse Sales
- Average Retail Sales
- Average Retail Transfers
- Average Warehouse Sales
- Standard Deviation of Retail Sales
- Standard Deviation of Retail Transfers
- Standard Deviation of Warehouse Sales
- Total Sales
- Active Months

---

# 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

---

# ⚙ Machine Learning Workflow

1. Data Collection
2. Data Cleaning
3. Exploratory Data Analysis
4. Product-Level Feature Engineering
5. Data Transformation
6. Feature Preprocessing
7. Selecting Optimal Number of Clusters
8. K-Means Clustering
9. Cluster Evaluation
10. PCA Visualization
11. Cluster Profiling
12. Model Testing
13. Business Insights

---

# 📈 Exploratory Data Analysis

The notebook includes:

- Dataset Structure Analysis
- Data Type Analysis
- Missing Value Analysis
- Duplicate Check
- Unique Value Analysis
- Negative Value Analysis
- Zero Value Analysis
- Sales Feature Distribution Analysis
- Product-Level Sales Analysis
- Cluster Distribution Analysis
- Cluster Comparison

The analysis identified a large number of zero values and skewed sales distributions, which were considered during feature transformation and preprocessing.

---

# 🔧 Feature Engineering & Data Preprocessing

The original transaction-level data was aggregated to create a product-level dataset.

For each product, historical sales behavior was summarized using:

- Total sales
- Average sales
- Sales standard deviation
- Active months

The resulting product-level dataset contained:

**34,056 products × 14 features**

Sales features showed significant skewness and extreme values.

A transformation was applied to improve the distribution of the numerical features before clustering.

Categorical variables were encoded and numerical features were standardized as part of the preprocessing pipeline.

The modeling feature matrix changed from:

**12 original modeling features → 19 processed features**

---

# 🤖 Clustering Model

## K-Means Clustering

K-Means Clustering was selected as the primary unsupervised Machine Learning algorithm.

The algorithm groups products based on similarity in their processed sales and activity features.

Different values of K were tested using the Silhouette Score.

| Number of Clusters (K) | Silhouette Score |
| ----------------------- | ---------------: |
| 2 | **0.5890** |
| 3 | 0.4089 |
| 4 | 0.3919 |
| 5 | 0.3912 |
| 6 | 0.3719 |
| 7 | 0.3086 |
| 8 | 0.3250 |

The highest Silhouette Score was obtained with **K = 2**.

Therefore, **2 clusters** were selected for the final K-Means model.

---

# 🏆 Model Evaluation

Since this is an unsupervised learning problem, traditional classification metrics such as Accuracy, Precision, Recall, and F1 Score are not applicable.

The clustering model was evaluated using:

- Silhouette Score
- Davies-Bouldin Index
- Calinski-Harabasz Score

## 📈 Final Clustering Performance

| Metric | Value |
| ------ | ----: |
| Silhouette Score | **0.5890** |
| Davies-Bouldin Index | **0.8166** |
| Calinski-Harabasz Score | **33,697.27** |

The Silhouette Score of **0.5890** indicates that the resulting product clusters have reasonable separation and cohesion.

---

# 📊 Project Visualizations

## Sales Feature Distribution

The distribution analysis was performed to understand the behavior and skewness of the major sales features before transformation.



---

## Optimal K Selection

Silhouette Scores were compared across different values of K to identify the most suitable number of clusters.



---

## Cluster Distribution

The final K-Means model produced two product segments:

- **Low-Activity Products:** 28,452
- **High-Activity Products:** 5,604



---

## PCA Cluster Visualization

Principal Component Analysis (PCA) was applied to reduce the processed feature space to two dimensions for visualization.

The first two principal components explain approximately:

**85.49% of the total variance**



---

## Cluster Sales Comparison

The identified clusters were compared based on their retail sales, retail transfers, warehouse sales, total sales, and active months.



---

# 📌 Cluster Analysis

## Cluster 0 — Low-Activity Products

**Number of Products:** 28,452

| Feature | Average Value |
| ------- | ------------: |
| Total Retail Sales | 2.19 |
| Total Retail Transfers | 1.57 |
| Total Warehouse Sales | 17.73 |
| Total Sales | 21.49 |
| Active Months | 6.83 |

Cluster 0 represents the majority of the product portfolio.

These products show relatively low sales activity and are active for a shorter period compared with the high-activity segment.

---

## Cluster 1 — High-Activity Products

**Number of Products:** 5,604

| Feature | Average Value |
| ------- | ------------: |
| Total Retail Sales | 374.46 |
| Total Retail Transfers | 372.83 |
| Total Warehouse Sales | 1,298.62 |
| Total Sales | 2,045.90 |
| Active Months | 20.23 |

Cluster 1 represents a smaller portion of the product portfolio but contains products with substantially higher sales activity.

These products also remain active for a significantly longer period.

---

# 🧪 Model Testing

The trained K-Means model was tested using real product observations from the dataset.

The testing demonstrated that the model could assign products to the learned segments based on their sales behavior.

### Test Results

- Real low-activity product → **Low-Activity Products**
- Real high-activity product → **High-Activity Products**

This provides a practical demonstration of how the trained clustering model can be used to segment product observations.

---

# 🎯 Key Achievements

- Built an end-to-end unsupervised Machine Learning pipeline for product segmentation.
- Analyzed **307,645 historical sales records**.
- Aggregated the data into **34,056 unique products**.
- Created product-level sales and activity features.
- Applied feature transformation to handle skewed sales distributions.
- Applied preprocessing and feature encoding.
- Compared multiple cluster sizes using Silhouette Score.
- Selected **K = 2** for the final clustering model.
- Achieved a **Silhouette Score of 0.5890**.
- Achieved a **Davies-Bouldin Index of 0.8166**.
- Achieved a **Calinski-Harabasz Score of 33,697.27**.
- Used PCA to visualize the cluster structure.
- Identified Low-Activity and High-Activity product segments.
- Tested the trained model using real product observations.
- Generated actionable business insights from the clustering results.

---

# 💼 Business Impact

The identified product segments can provide businesses with a simple framework for understanding product activity and improving operational decisions.

Potential applications include:

- Inventory Management
- Stock Replenishment Planning
- Purchasing Optimization
- Product Portfolio Management
- Sales Planning
- Product Prioritization
- Inventory Optimization

### High-Activity Products

High-activity products can receive greater attention during:

- Stock replenishment
- Inventory planning
- Purchasing decisions
- Sales forecasting

### Low-Activity Products

Low-activity products can be reviewed for:

- Overstocking risks
- Inventory optimization
- Reduced purchasing priority
- Product portfolio evaluation

The clustering approach therefore converts historical sales data into practical product segments that can support data-driven business decisions.

---

# 📁 Repository Structure

```text
product-cluster-analysis/
│
├── Product_Cluster_Analysis.ipynb
├── README.md
├── requirements.txt
│
├── images/
│
└── data/

---


