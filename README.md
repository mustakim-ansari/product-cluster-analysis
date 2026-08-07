# 🛍️ Product Clustering Analysis Using Machine Learning

---

# 📌 Project Overview

Analyzing thousands of products based on their historical sales activity can make inventory planning, purchasing, and product management challenging.

This project applies **Unsupervised Machine Learning and Clustering techniques** to group products with similar historical sales behavior.

By identifying products with similar purchasing and sales patterns, organizations can better understand product activity, optimize inventory, improve purchasing decisions, and manage their product portfolio.

The complete workflow includes:

* Data Collection
* Data Cleaning
* Exploratory Data Analysis (EDA)
* Product-Level Data Aggregation
* Feature Engineering
* Feature Selection
* Data Preprocessing
* Feature Scaling
* Clustering
* Optimal Cluster Selection
* Cluster Analysis
* Cluster Profiling
* Business Insights

---

# 🎯 Business Problem

Organizations often manage thousands of products with different sales patterns. Analyzing each product individually can make inventory management and purchasing decisions difficult.

Product clustering helps identify groups of products with similar sales behavior, allowing businesses to understand product activity and make data-driven decisions.

The clustering results can support:

* Inventory Management
* Stock Optimization
* Purchasing Decisions
* Product Portfolio Management
* Sales Planning
* Product Performance Analysis

---

# 📊 Dataset Information

The dataset contains historical warehouse and retail sales information for products recorded between **2017 and 2020**.

The original dataset contains:

* **307,645 records**
* **9 features**

After aggregating the historical sales data at the product level, the analysis contains:

* **34,056 unique products**

The original dataset includes:

* Year
* Month
* Supplier
* Item Code
* Item Description
* Item Type
* Retail Sales
* Retail Transfers
* Warehouse Sales

---

# 🧮 Product-Level Features

Historical transactions were aggregated at the product level to create meaningful features for clustering.

The final product-level dataset includes:

* Total Retail Sales
* Total Retail Transfers
* Total Warehouse Sales
* Average Retail Sales
* Average Retail Transfers
* Average Warehouse Sales
* Standard Deviation of Retail Sales
* Standard Deviation of Retail Transfers
* Standard Deviation of Warehouse Sales
* Total Sales
* Active Months

These features represent the overall sales activity, consistency, and product engagement across the historical period.

---

# 🛠 Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

---

# ⚙ Machine Learning Workflow

1. Data Collection
2. Data Cleaning
3. Exploratory Data Analysis
4. Product-Level Aggregation
5. Feature Engineering
6. Feature Selection
7. Feature Scaling
8. Clustering
9. Optimal Cluster Selection
10. Cluster Analysis
11. Cluster Profiling
12. Data Visualization
13. Business Insights

---

# 📈 Exploratory Data Analysis

Exploratory Data Analysis was performed to understand product sales behavior and identify important patterns before applying clustering algorithms.

The analysis includes:

* Sales Distribution Analysis
* Retail Sales Analysis
* Warehouse Sales Analysis
* Retail Transfer Analysis
* Total Sales Distribution
* Active Months Analysis
* Feature Correlation Analysis
* Outlier Detection
* Product Activity Analysis

---

# 📊 Project Visualizations

## Sales Distribution

Visualization of product-level sales distributions to understand the variation in sales activity across products.

---

## Correlation Heatmap

A correlation heatmap was used to identify relationships between product-level sales features and determine highly related variables.

---

## Product Activity Analysis

Analysis of total sales and active months helps identify products with different levels of historical activity.

---

## Cluster Visualization

Products are visualized based on their clustering results to understand similarities and differences between product groups.

---

## Cluster Profiles

Each cluster is analyzed using its aggregated sales characteristics to understand the behavior of products belonging to that group.

---

# 🤖 Clustering Algorithms Evaluated

The project evaluates unsupervised machine learning techniques to identify groups of products with similar sales behavior.

The clustering algorithms include:

* K-Means Clustering
* Agglomerative Clustering
* MiniBatch K-Means

These algorithms were compared based on clustering quality and their ability to create meaningful product segments.

---

# 📏 Cluster Evaluation

Since clustering is an unsupervised learning problem, traditional classification accuracy cannot be used to evaluate the models.

The clustering performance was evaluated using:

* Silhouette Score
* Cluster Separation
* Cluster Interpretability
* Business Relevance

A higher Silhouette Score indicates that products are more appropriately grouped within their respective clusters while remaining separated from other clusters.

---

# 🏆 Clustering Results

The clustering algorithms were evaluated and compared to identify the most suitable approach for segmenting products based on historical sales behavior.

The final clustering solution was selected by considering both:

* Quantitative clustering performance
* Practical business interpretability

The resulting clusters represent groups of products with similar historical sales characteristics.

---

# 🔎 Cluster Analysis

The identified product clusters can be interpreted based on their sales activity.

Typical product segments may include:

### High-Activity Products

Products with high total sales and strong historical activity.

Potential business use:

* Maintain sufficient inventory
* Prioritize stock availability
* Monitor demand regularly

### Medium-Activity Products

Products with moderate sales activity that contribute consistently to overall sales.

Potential business use:

* Maintain balanced inventory
* Monitor sales trends
* Optimize replenishment levels

### Low-Activity Products

Products with relatively low historical sales activity.

Potential business use:

* Reduce excess inventory
* Review purchasing frequency
* Consider product portfolio optimization

---

# 💼 Business Impact

Product clustering can help organizations convert large amounts of historical sales data into actionable product segments.

Potential applications include:

* Inventory Optimization
* Stock Level Planning
* Purchasing Strategy
* Product Portfolio Management
* Demand Analysis
* Sales Planning
* Identification of High-Activity Products
* Identification of Low-Activity Products

By grouping products with similar sales behavior, businesses can apply different strategies to different product segments instead of treating every product equally.

---

# 🎯 Key Achievements

* Analyzed **307,645 historical sales records**.
* Aggregated transaction-level data into **34,056 unique products**.
* Created meaningful product-level sales and activity features.
* Performed exploratory data analysis to understand product behavior.
* Applied feature engineering for unsupervised learning.
* Compared multiple clustering algorithms.
* Evaluated clustering quality using Silhouette Score.
* Identified meaningful product segments based on historical sales behavior.
* Derived business insights from the resulting product clusters.

---

# 📁 Repository Structure

```text
product-clustering-analysis/
│
├── Product_Clustering_Analysis.ipynb
├── README.md
├── requirements.txt
├── .gitignore
├── LICENSE
│
├── images/
│
└── data/
```

---

# 🚀 How to Run

```bash
git clone https://github.com/mustakim-ansari/product-clustering-analysis.git

cd product-clustering-analysis

pip install -r requirements.txt

jupyter notebook
```

Open:

```text
Product_Clustering_Analysis.ipynb
```

Run all cells.

---

# 🔮 Future Improvements

* Deploy the clustering solution using Streamlit
* Add real-time product segmentation
* Incorporate additional product attributes
* Integrate inventory and stock-level information
* Experiment with DBSCAN and advanced clustering techniques
* Develop an interactive product segmentation dashboard
* Automate cluster-based inventory recommendations
* Apply dimensionality reduction techniques such as PCA for visualization

---

# 📌 Conclusion

This project demonstrates how **Unsupervised Machine Learning** can be used to segment thousands of products based on their historical sales behavior.

By transforming transaction-level sales data into meaningful product-level features and applying clustering algorithms, products can be grouped into segments with similar characteristics.

These segments can provide valuable support for inventory management, purchasing decisions, product portfolio optimization, and sales planning.

---

# 👨‍💻 Author

**Mustakim Ansari**

📧 [ansarimustakim278@gmail.com](mailto:ansarimustakim278@gmail.com)

🔗 LinkedIn:

https://www.linkedin.com/in/mustakim-ansari/

⭐ If you found this project useful, consider giving the repository a star.
