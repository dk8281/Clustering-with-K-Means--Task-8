# Clustering-with-K-Means--Task-8
## 📌 Objective
Perform unsupervised learning on the **Mall Customers dataset** using **K-Means clustering** to segment customers into distinct groups for targeted marketing.

---

## 📂 Dataset
**Mall_Customers.csv** contains:
- `CustomerID` (unique identifier, not used for clustering)
- `Gender` (Male/Female → encoded as 0/1)
- `Age`
- `Annual Income (k$)`
- `Spending Score (1–100)`

---

## ⚙️ Steps Performed
1. **Data Preprocessing**
   - Encoded `Gender` as numeric (Male=0, Female=1).
   - Selected features: `Gender`, `Age`, `Annual Income`, `Spending Score`.
   - Scaled features using **StandardScaler**.

2. **Finding Optimal Number of Clusters**
   - **Elbow Method**: Suggested an inflection point around **k=5**.  
     ![Elbow Plot](images/elbow.png)  
   - **Silhouette Score**: Highest score (~0.42) at **k=10**.  
     ![Silhouette Plot](images/silhouette.png)

3. **Clustering**
   - Performed **K-Means** with the chosen cluster count.
   - Applied **PCA (2D)** to visualize clusters.  
     ![Clusters](images/clusters.png)

4. **Evaluation**
   - **Silhouette Score** for k=10 → 0.42 (moderate structure).  
   - **Business-friendly choice**: Used **k=5 clusters** for better interpretability.

---

## 📊 Results
- **k=10** (Silhouette optimal): Highest separation, but too many clusters to be practical.  
- **k=5** (Elbow + interpretability): Balanced solution, easier to explain to business teams.  

### 🔑 Final Recommendation
👉 Use **5 customer segments** for business applications, while noting that silhouette analysis suggested 10.  

---

## 📌 Learnings
- Difference between **technical optimal (Silhouette)** and **practical optimal (Elbow/business needs)**.  
- Importance of **scaling** and **PCA visualization** in clustering.  
- Trade-off between **accuracy** and **interpretability** in unsupervised learning.  

---

## 🛠 Tools Used
- Python (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn)
