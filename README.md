# 📦 Product Cluster Analysis Using Machine Learning






---

# 📌 Project Overview

Understanding product sales behavior is important for effective inventory management, purchasing decisions, and product portfolio planning.

This project develops an end-to-end Machine Learning clustering pipeline to group similar products based on their historical retail, transfer, and warehouse sales patterns.

The primary objective is to identify meaningful product segments based on sales activity and generate actionable insights that can support inventory optimization, purchasing decisions, and product portfolio management.

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

Product clustering helps businesses group products with similar sales behavior and make more informed operational decisions.

Potential applications include:

- Inventory Management
- Stock Optimization
- Purchasing Decisions
- Product Portfolio Management
- Sales Planning
- Product Prioritization

---

# 📊 Dataset Information

The dataset contains historical warehouse and retail sales information recorded between **2017 and 2020**.

The original dataset contains:

- 307,645 records
- 9 features
- 396 suppliers
- 34,056 unique item codes
- 8 item types
- Monthly records from January to December

The dataset includes information such as:

- Year
- Month
- Supplier
- Item Code
- Item Description
- Item Type
- Retail Sales
- Retail Transfers
- Warehouse Sales

The transaction-level data was aggregated at the product level to understand the overall sales behavior of each product.

After aggregation, the product-level dataset contains:

**34,056 unique products**

### Product-Level Features

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
3. Product-Level Feature Engineering
4. Exploratory Data Analysis
5. Data Transformation
6. Feature Preprocessing
7. Optimal Cluster Selection
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
- Missing Value Analysis
- Duplicate Check
- Unique Product Analysis
- Negative Value Analysis
- Zero Value Analysis
- Sales Feature Distribution
- Product-Level Sales Analysis
- Cluster Distribution
- Cluster Comparison

The analysis identified skewed sales distributions and a large number of zero values within the sales-related features.

These characteristics were considered during the feature transformation and preprocessing stages.

---

# 🔧 Feature Engineering

The original transaction-level dataset was converted into a product-level dataset.

Historical sales information was aggregated for each product using:

- Total Sales
- Average Sales
- Standard Deviation of Sales
- Active Months

The resulting product-level dataset contained:

**34,056 products × 14 features**

After feature selection and preprocessing:

**Original Feature Shape:** 34,056 × 12

**Processed Feature Shape:** 34,056 × 19

A transformation was applied to reduce the impact of highly skewed sales values before clustering.

Categorical features were encoded and numerical features were standardized as part of the preprocessing pipeline.

---

# 📊 Project Visualizations

## Sales Feature Distribution



---

## Optimal Number of Clusters

Silhouette Scores were calculated for different values of K to determine the most suitable number of clusters.



---

## Cluster Distribution



---

## PCA Cluster Visualization

Principal Component Analysis was used to reduce the processed feature space to two dimensions for visualization.

The first two principal components explained:

**85.49% of the total variance**



---

## Cluster Comparison



---

# 🤖 Clustering Model

## K-Means Clustering

K-Means Clustering was selected as the final clustering algorithm for segmenting products based on their historical sales behavior.

Different values of K were evaluated using the Silhouette Score.

| K | Silhouette Score |
| - | ----------------: |
| 2 | **0.5890** |
| 3 | 0.4089 |
| 4 | 0.3919 |
| 5 | 0.3912 |
| 6 | 0.3719 |
| 7 | 0.3086 |
| 8 | 0.3250 |

The highest Silhouette Score was obtained with:

**K = 2**

Therefore, two product clusters were selected for the final model.

---

# 🏆 Model Evaluation

The final clustering model was evaluated using:

- Silhouette Score
- Davies-Bouldin Index
- Calinski-Harabasz Score

---

## 📈 Model Performance

The final **K-Means Clustering** model achieved the following results:

| Metric | Value |
| ------ | ----: |
| Silhouette Score | **0.5890** |
| Davies-Bouldin Index | **0.8166** |
| Calinski-Harabasz Score | **33,697.27** |
| Number of Clusters | **2** |

The Silhouette Score of **0.5890** indicates reasonably good separation between the identified product groups.

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

Cluster 0 contains the majority of products.

These products show relatively lower sales activity and shorter active periods.

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

Cluster 1 contains a smaller number of products but demonstrates significantly higher sales activity.

These products also remain active for a substantially longer period.

---

# 🧪 Model Testing

The trained K-Means model was tested using real product observations from the dataset.

The model successfully assigned products to the learned product segments based on their historical sales behavior.

### Test Results

- Low-activity product → **Low-Activity Products**
- High-activity product → **High-Activity Products**

This demonstrates that the trained clustering model can be used to segment products into meaningful activity groups.

---

# 🎯 Key Achievements

- Built an end-to-end Machine Learning clustering pipeline for product segmentation.
- Analyzed **307,645 historical sales records**.
- Identified **34,056 unique products**.
- Created meaningful product-level sales features.
- Applied feature transformation to handle skewed sales distributions.
- Applied categorical encoding and numerical preprocessing.
- Compared multiple cluster sizes using Silhouette Score.
- Selected **K = 2** as the optimal number of clusters.
- Achieved a **Silhouette Score of 0.5890**.
- Achieved a **Davies-Bouldin Index of 0.8166**.
- Achieved a **Calinski-Harabasz Score of 33,697.27**.
- Applied PCA for cluster visualization.
- Identified Low-Activity and High-Activity product segments.
- Tested the clustering model using real product observations.
- Generated actionable insights for inventory and product management.

---

# 💼 Business Impact

Product clustering can help businesses understand their product portfolio and make data-driven operational decisions.

Potential applications include:

- Inventory Management
- Stock Replenishment
- Purchasing Optimization
- Product Portfolio Management
- Sales Planning
- Inventory Prioritization
- Product Performance Analysis

High-activity products can receive greater attention during inventory planning and replenishment, while low-activity products can be reviewed for inventory optimization and purchasing decisions.

---

# 📁 Repository Structure

```text
product-cluster-analysis/
│
├── Product_Cluster_Analysis.ipynb
├── README.md
├── requirements.txt
├── .gitignore
├── LICENSE
│
├── images/
│
└── data/
---
```
# 🚀 How to Run

```bash
git clone https://github.com/mustakim-ansari/product-cluster-analysis.git

cd product-cluster-analysis

pip install -r requirements.txt

jupyter notebook

Run:

Product_Cluster_Analysis.ipynb

Run all cells sequentially to reproduce the complete product clustering analysis.

---
```

# 🔮 Future Improvements

- Deploy the clustering model using Streamlit
- Build an interactive product segmentation dashboard
- Experiment with DBSCAN and Agglomerative Clustering
- Compare multiple clustering algorithms
- Incorporate additional product and customer-level features
- Develop automated inventory recommendations based on cluster membership
- Monitor product clusters as new sales data becomes available
- Integrate clustering results into an inventory management system

---

# 💼 Business Impact

Product clustering can help businesses understand their product portfolio and make data-driven operational decisions.

Potential applications include:

- Inventory Management
- Stock Replenishment
- Purchasing Optimization
- Product Portfolio Management
- Sales Planning
- Inventory Prioritization
- Product Performance Analysis

---

# 👨‍💻 Author

Mustakim Ansari

📧 ansarimustakim278@gmail.com

🔗 LinkedIn:

https://www.linkedin.com/in/mustakim-ansari-b60846343/

🔗 GitHub:

https://github.com/mustakim-ansari

⭐ If you found this project useful, consider giving the repository a star.
