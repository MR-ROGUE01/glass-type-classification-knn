<div align="center">

# 🔬 Glass Type Classification using K-Nearest Neighbors

### End-to-End Machine Learning Classification Project

<img src="https://img.shields.io/badge/Python-3.11-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/Scikit--Learn-KNN-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white"/>
<img src="https://img.shields.io/badge/Accuracy-76.74%25-success?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge"/>

</div>

---

## 🎯 Project Objective

The objective of this project is to classify different types of glass based on their chemical composition and refractive index using the **K-Nearest Neighbors (KNN)** algorithm.

The project follows a complete machine learning workflow including data preprocessing, outlier handling, feature scaling, model training, and performance evaluation.

---

## 📊 Dataset Overview

The dataset contains physicochemical properties of glass samples used for multiclass classification.

### Features

| Feature | Description      |
| ------- | ---------------- |
| RI      | Refractive Index |
| Na      | Sodium           |
| Mg      | Magnesium        |
| Al      | Aluminum         |
| Si      | Silicon          |
| K       | Potassium        |
| Ca      | Calcium          |
| Ba      | Barium           |
| Fe      | Iron             |

### Target Variable

```text
Type
```

---

## ⚙️ Machine Learning Pipeline

```text
Data Collection
      │
      ▼
Data Cleaning
      │
      ▼
Duplicate Removal
      │
      ▼
Outlier Analysis
      │
      ▼
IQR-Based Capping
      │
      ▼
Train-Test Split
      │
      ▼
Feature Scaling
      │
      ▼
KNN Training
      │
      ▼
K Optimization
      │
      ▼
Model Evaluation
```

---

## 🧹 Data Preprocessing

### ✔ Missing Value Analysis

* Verified dataset integrity
* No missing values found

### ✔ Duplicate Handling

```python
df.drop_duplicates(inplace=True)
```

### ✔ Outlier Treatment

Applied **IQR-Based Outlier Capping** on the training dataset and used identical thresholds on the test dataset to prevent data leakage.

### ✔ Feature Scaling

```python
StandardScaler()
```

Since KNN is distance-based, feature scaling was essential for optimal performance.

---

## 🤖 Model Development

### Baseline Model

```python
KNeighborsClassifier(n_neighbors=5)
```

### K Value Optimization

Evaluated multiple K values ranging from:

```text
1 → 15
```

and selected the best-performing configuration based on test accuracy.

---

## 📈 Performance Metrics

### Final Results

| Metric             | Score      |
| ------------------ | ---------- |
| Accuracy           | **76.74%** |
| Weighted Precision | **0.77**   |
| Weighted Recall    | **0.77**   |
| Weighted F1 Score  | **0.76**   |
| Macro F1 Score     | **0.69**   |

---

### Class-wise Performance

| Glass Type | Precision | Recall | F1 Score |
| ---------- | --------- | ------ | -------- |
| 1          | 0.83      | 0.71   | 0.77     |
| 2          | 0.74      | 0.93   | 0.82     |
| 3          | 0.50      | 0.33   | 0.40     |
| 5          | 1.00      | 0.67   | 0.80     |
| 6          | 0.50      | 0.50   | 0.50     |
| 7          | 0.83      | 0.83   | 0.83     |

---

## 🛠️ Technology Stack

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn

---

## 📂 Repository Structure

```text
glass-type-classification-knn/
│
├── glass.csv
├── Day_91.ipynb
├── README.md
├── requirements.txt
```

---

## 🎓 Key Learnings

* K-Nearest Neighbors (KNN)
* Distance-Based Classification
* Outlier Detection & Treatment
* Data Leakage Prevention
* Feature Scaling using StandardScaler
* Classification Metrics
* Model Evaluation Techniques
* K Value Selection Strategy

---

## 🚀 Future Enhancements

* Hyperparameter Tuning with GridSearchCV
* Logistic Regression Comparison
* Decision Tree Comparison
* Cross Validation
* Model Deployment using Streamlit

---

<div align="center">

### ⭐ If you found this project useful, consider giving it a star.

Built with Python & Machine Learning 🚀

</div>
