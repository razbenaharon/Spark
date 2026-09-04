> [!NOTE]
> **This repository has moved and is archived (read-only).**
>
> The project now lives in
> **[razbenaharon/academic-projects/distributed-database-spark](https://github.com/razbenaharon/academic-projects/tree/main/distributed-database-spark)**,
> alongside the rest of my Technion coursework. Continue there.


# 📌 Distributed Database Management - Spark  

This project focuses on **data preprocessing, dimensionality reduction, clustering, and real-time streaming analysis** using **Apache Spark**.  
The goal is to segment households based on viewing habits and derive meaningful insights from large-scale demographic data.  

---

## 🔹 Key Components  

### **1️⃣ Data Preprocessing**  
✅ **Normalized numerical variables** and applied **one-hot encoding** to categorical variables.  
🔹 Ensures **fair comparison** between features and prevents misinterpretation of categorical data.  
🔹 Crucial for **accurate modeling and analysis**, especially with diverse demographic datasets.  

---

### **2️⃣ Dimensionality Reduction**  
✅ Used **Singular Value Decomposition (SVD)** to project feature vectors onto a **2D space**.  
🔹 Revealed **principal components** with the largest singular values, capturing **maximum variance**.  
🔹 Helped identify **three main clusters**, providing **initial insights into household groupings**.  

---

### **3️⃣ Clustering**  
✅ Applied **K-means clustering** with **8 clusters**.  
🔹 Allowed for targeted analysis of **household characteristics and viewing habits**.  
🔹 The choice of **8 clusters** was an **initial approach**, with further evaluation planned.  

---

### **4️⃣ Visualization of Clusters**  
✅ Used **PCA for 2D reduction** and created a **color-coded scatter plot**.  
🔹 Revealed **varying levels of cluster overlap**, indicating possible **cluster refinements**.  
🔹 Identified that **reducing to 6 clusters** might provide **more distinct groupings**,  
   demonstrating an analytical approach to methodology improvement.  

---

### **5️⃣ Viewing Analysis**  
✅ Calculated **'diff rank'** for stations in each cluster/subset.  

🔹 **Purpose**: Measures how **viewing preferences in each cluster differ** from the general population.  

🔹 **Findings**:  
   - 'Diff rank' values were generally **low (below 0.8)**, indicating **no strong preferences**  
     for particular stations across clusters.  
   - Suggests that household **viewing patterns may be more uniform** than initially expected.  

---

### **6️⃣ Streaming Analysis**  
✅ Used **Spark Streaming** to process **real-time viewing data from Kafka**.  
🔹 **Demonstrates real-time data processing**, crucial for **keeping recommendations current**.  

🔹 **Findings**:  
   - **High similarity in Top-10 stations** across different time triggers.  
   - Suggests **consistent viewing patterns** within clusters over time.  

---

## 📊 Key Insights & Observations  

🔹 **Cluster Consistency**  
   - **High similarity in results** across different subset types indicates **stable viewing preferences**  
     as data volume increases.  

🔹 **Decreasing 'Diff Rank' Over Time**  
   - Observed a **gradual decline** in 'diff rank' across triggers.  
   - Suggests that **cluster-specific viewing habits** were converging toward general population trends.  

🔹 **Visualization Strategy**  
   - Implemented **multi-panel visualizations** for **efficient data analysis**.  
   - Demonstrates the ability to **present complex data clearly and meaningfully**.  

---

## 🚀 Tech Stack  
🔹 **Apache Spark (PySpark)** – Big Data Processing  
🔹 **Kafka** – Real-Time Streaming  
🔹 **Pandas & NumPy** – Data Preprocessing  
🔹 **Matplotlib & Seaborn** – Visualization  
🔹 **K-Means, SVD, PCA** – Machine Learning  
