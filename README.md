# 🚲 Bike Sharing Demand Prediction & Analysis

## 📌 Project Overview

This project analyzes bike rental demand using a real-world dataset and applies multiple machine learning techniques, including exploratory data analysis (EDA), supervised learning, unsupervised clustering, and ensemble methods.

The goal is to understand the factors affecting bike usage and build models that accurately predict rental demand.

---

## 📊 Dataset

* **Name:** Bike Sharing Dataset
* **Source:** Kaggle
* **Link:** https://www.kaggle.com/datasets/lakshmi25npathi/bike-sharing-dataset
* **License:** Public dataset

The dataset contains hourly records of bike rentals along with weather conditions, time-related variables, and usage statistics. It was chosen because it provides a rich set of features suitable for both regression and clustering tasks.

---

## 🧠 Project Structure

```
BikeSharing-ML-project/
│
├── data/
│   ├── raw/hour.csv
│   ├── cleaned.csv
│   └── clustered.csv
│
├── models/
│   └── supervised_best.pkl
│
├── notebooks/
│   ├── T1_EDA.ipynb
│   ├── T2_Supervised.ipynb
│   ├── T3_Unsupervised.ipynb
│   └── T4_Ensemble.ipynb
│
├── reports/
│   ├── t1_*.png
│   ├── t3_*.png
│   ├── t4_*.png
│   └── t4_model_comparison.csv
│
├── requirements.txt
└── README.md
```

---

## 🔍 Task 1 — Exploratory Data Analysis (EDA)

* Cleaned and prepared the dataset
* Analyzed relationships between variables such as:

  * Hour of the day
  * Weather conditions
  * Temperature
* Identified patterns in bike rental demand
* Exported cleaned dataset (`cleaned.csv`)

---

## 📈 Task 2 — Supervised Learning

* **Task:** Regression (predict `cnt` — total bike rentals)
* Created new features:

  * Peak hours indicator
  * Weather × temperature interaction
* Models used:

  * Linear Regression
  * Decision Tree

### 📊 Evaluation Metrics:

* RMSE
* MAE
* R²

👉 Best model: **Decision Tree**

---

## 🧩 Task 3 — Unsupervised Learning

* Selected key features: `temp`, `hum`, `windspeed`, `hr`, `workingday`, `cnt`

* Applied clustering:

  * K-Means
  * Agglomerative Clustering

* Used **Elbow Method** to select number of clusters

* Applied **PCA** for visualization

### 🔎 Cluster Interpretation:

* Low demand periods
* Medium demand (normal usage)
* High demand (peak hours & good weather)

👉 Saved dataset with clusters (`clustered.csv`)

---

## 🚀 Task 4 — Ensemble Learning

* Added `cluster_label` as a feature
* Models used:

  * Random Forest
  * Gradient Boosting

### 📊 Results:

* Ensemble models significantly improved performance
* Random Forest achieved the best results

### 📈 Key insights:

* `cluster_label` is highly important
* Time-related features (hour) are strong predictors
* Weather variables have moderate influence

---

## 📊 Final Results

| Model             | RMSE     | MAE        | R²      |
| ----------------- | -------- | ---------- | ------- |
| Random Forest     | Best     | Best       | Highest |
| Gradient Boosting | Good     | Good       | High    |
| Decision Tree     | Moderate | Moderate   | Good    |
| Linear Regression | Weak     | High error | Low     |

---

## 📁 Reports

All key outputs are saved in `/reports`:

* EDA visualizations
* Clustering plots
* Feature importance
* Learning curves
* Model comparison table

---

## 🛠️ Technologies Used

* Python
* Pandas, NumPy
* Matplotlib, Seaborn
* Scikit-learn

---

## 📌 Conclusion

This project demonstrates how combining supervised, unsupervised, and ensemble learning improves predictive performance. The inclusion of clustering as an additional feature helped capture hidden patterns in the data and significantly boosted model accuracy.

## 👤 Author

Amirkhan Issakulov
Alikhan Aubakir
