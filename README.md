# K-Means Clustering on Country Data 🌍📊

This project applies **K-Means Clustering**, an unsupervised machine learning algorithm, to group countries based on socio-economic and health indicators.  
The analysis helps identify clusters of countries with similar characteristics and can be used to explore patterns of development, income, and resource distribution.

---

## 🧠 Project Overview

This notebook demonstrates:
- Loading and exploring a dataset of world countries  
- Performing data preprocessing and normalization  
- Applying **K-Means Clustering** to segment the countries  
- Determining the optimal number of clusters using the **Elbow Method**  
- Visualizing results using scatter plots and cluster analysis  

The main goal is to understand how unsupervised algorithms can reveal hidden structure in complex datasets.

---

## 📂 Files Included

| File | Description |
|------|--------------|
| `Kmeans_task.ipynb` | Jupyter notebook implementing the K-Means clustering analysis |
| `Country-data.csv` | Dataset containing socio-economic and health indicators of countries |
| `README.md` | Project documentation (this file) |

---

## 📊 Dataset Description

The **Country-data.csv** file contains multiple numerical indicators representing the economic and health conditions of each country.

| Column | Description |
|---------|-------------|
| `country` | Name of the country |
| `child_mort` | Deaths of children under 5 years per 1,000 live births |
| `exports` | Exports as a percentage of GDP |
| `health` | Health expenditure as a percentage of GDP |
| `imports` | Imports as a percentage of GDP |
| `income` | Net income per person |
| `inflation` | Annual inflation rate |
| `life_expec` | Life expectancy in years |
| `total_fer` | Fertility rate (children per woman) |
| `gdpp` | GDP per capita |

---

## ⚙️ Installation and Dependencies

Ensure Python 3.8+ is installed, and then install the required packages:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

---

## 🚀 How to Run the Project

1. Clone this repository:
   ```bash
   git clone https://github.com/adnanaltimeemy/KMeans_CountryClustering.git
   cd KMeans_CountryClustering
   ```

2. Launch Jupyter Notebook:
   ```bash
   jupyter notebook "Kmeans_task.ipynb"
   ```

3. Run all cells to see the clustering process, evaluation, and visualizations.

---

## 🧩 Model Explanation

### 🔹 What is K-Means?
**K-Means** is an unsupervised learning algorithm used to partition data into *k* distinct clusters based on feature similarity.  
It minimizes the variance within each cluster and maximizes the variance between clusters.

### 🔹 Key Steps
1. Data normalization using `StandardScaler` to ensure equal feature weighting  
2. Selection of the optimal number of clusters using the **Elbow Method**  
3. Training the K-Means model using:
   ```python
   from sklearn.cluster import KMeans
   kmeans = KMeans(n_clusters=3, random_state=42)
   kmeans.fit(X_scaled)
   ```
4. Adding cluster labels back to the original dataset  
5. Visualization of clusters using scatter plots (e.g., GDP vs Life Expectancy)

---

## 📈 Results and Visualisations

### ✅ Clustering Summary
- Optimal clusters determined using the **Elbow Method** (typically *k = 3*)  
- Countries were grouped into low, medium, and high development clusters  
- Indicators like `gdpp`, `life_expec`, and `child_mort` strongly influenced the clustering

### 🌍 Example Findings
| Cluster | Description | Typical Countries |
|----------|--------------|-------------------|
| **0** | High income, low child mortality, high life expectancy | e.g., USA, Germany |
| **1** | Moderate income, average health metrics | e.g., Brazil, China |
| **2** | Low income, high child mortality, low life expectancy | e.g., Sudan, Nepal |

### 📊 Visualisations
The notebook includes:
- **Elbow curve** for selecting `k`
- **Scatter plots** showing GDP vs Life Expectancy by cluster
- **Pair plots** for multivariate analysis
- **Cluster centroids** highlighting key features of each group

---

## 🔮 Future Improvements

- Apply **PCA** (Principal Component Analysis) to reduce dimensionality before clustering  
- Explore **Hierarchical Clustering** or **DBSCAN** for comparison  
- Add **interactive visualizations** using Plotly  
- Perform deeper socio-economic analysis per cluster  

---

## 🤝 Contributing

Contributions are welcome!  
1. Fork this repository  
2. Create a new branch (`git checkout -b feature-update`)  
3. Commit your changes (`git commit -m "Enhanced cluster visualisation"`)  
4. Push and submit a Pull Request  

---

## 🪪 License

This project is licensed under the **MIT License**.  
You are free to use, modify, and distribute it for educational or research purposes.

---

## 🙏 Acknowledgements

- Dataset Source: [Kaggle – Country Data for Clustering](https://www.kaggle.com/datasets/rohan0301/unsupervised-learning-on-country-data)  
- Developed by **Adnan Altimeemy**  
  Data Scientist  
  Educational purpose: introducing students to unsupervised learning and K-Means clustering using Python.
