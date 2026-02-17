# 🤖 Scikit-Learn (sklearn) Notes

## 📌 Introduction

Scikit-Learn (sklearn) is a popular Python library used for:

- Machine Learning
- Classification
- Regression
- Clustering
- Model evaluation
- Data preprocessing

It works well with NumPy and Pandas.

---

## 📦 Installation & Import

```bash
pip install scikit-learn
```

```python
import numpy as np
import pandas as pd
from sklearn.model_selection import train_test_split
```

---

# 🔹 Machine Learning Workflow

1. Load dataset  
2. Split into X (features) and y (target)  
3. Split into train & test  
4. Train model  
5. Predict  
6. Evaluate  

---

# 🔹 Train Test Split

```python
X = [[1], [2], [3], [4], [5]]
y = [2, 4, 6, 8, 10]

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

print(X_train)
print(X_test)
```

Output:
```
[[5], [3], [1], [4]]
[[2]]
```

---

# 🔹 Linear Regression (Regression Example)

```python
from sklearn.linear_model import LinearRegression

model = LinearRegression()
model.fit(X_train, y_train)

prediction = model.predict(X_test)
print(prediction)
```

Output:
```
[4.]
```

---

# 🔹 Logistic Regression (Classification Example)

```python
from sklearn.linear_model import LogisticRegression

X = [[1], [2], [3], [4]]
y = [0, 0, 1, 1]

model = LogisticRegression()
model.fit(X, y)

print(model.predict([[2.5]]))
```

Output:
```
[0]
```

---

# 🔹 K-Nearest Neighbors (KNN)

```python
from sklearn.neighbors import KNeighborsClassifier

X = [[1], [2], [3], [4]]
y = [0, 0, 1, 1]

model = KNeighborsClassifier(n_neighbors=3)
model.fit(X, y)

print(model.predict([[3]]))
```

Output:
```
[1]
```

---

# 🔹 Decision Tree

```python
from sklearn.tree import DecisionTreeClassifier

model = DecisionTreeClassifier()
model.fit(X, y)

print(model.predict([[2]]))
```

Output:
```
[0]
```

---

# 🔹 Model Evaluation

## Accuracy Score

```python
from sklearn.metrics import accuracy_score

y_true = [0, 1, 1]
y_pred = [0, 1, 0]

print(accuracy_score(y_true, y_pred))
```

Output:
```
0.6666666666666666
```

---

## Confusion Matrix

```python
from sklearn.metrics import confusion_matrix

print(confusion_matrix(y_true, y_pred))
```

Output:
```
[[1 0]
 [1 1]]
```

---

## Classification Report

```python
from sklearn.metrics import classification_report

print(classification_report(y_true, y_pred))
```

Output:
- Precision
- Recall
- F1-score
- Support

---

# 🔹 Standardization (Feature Scaling)

```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()
X_scaled = scaler.fit_transform([[1], [2], [3]])

print(X_scaled)
```

Output:
```
[[-1.22474487]
 [ 0.        ]
 [ 1.22474487]]
```

---

# 🔹 Label Encoding

```python
from sklearn.preprocessing import LabelEncoder

le = LabelEncoder()
labels = le.fit_transform(["cat", "dog", "cat"])

print(labels)
```

Output:
```
[0 1 0]
```

---

# 🔹 K-Means Clustering

```python
from sklearn.cluster import KMeans

X = [[1,2], [1,4], [10,2], [10,4]]

kmeans = KMeans(n_clusters=2, random_state=42)
kmeans.fit(X)

print(kmeans.labels_)
```

Output:
```
[1 1 0 0]
```

# ✅ Common Algorithms in sklearn

- Linear Regression
- Logistic Regression
- KNN
- Decision Tree
- Random Forest
- SVM
- KMeans
- Naive Bayes

---

# 🚀 Summary

Scikit-Learn is mainly used for:

✔ Building Machine Learning models  
✔ Classification problems  
✔ Regression problems  
✔ Clustering  
✔ Model evaluation  
✔ Data preprocessing  

---

