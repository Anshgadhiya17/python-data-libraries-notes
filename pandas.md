# 🐼 Pandas Notes

## 📌 Introduction

Pandas is an open-source Python library used for:

- Data analysis
- Data manipulation
- Data cleaning
- Handling structured data (tables)

It is built on top of NumPy and is widely used in Data Science, AI/ML, and Data Analytics.

---

## 📦 Installation & Import

```bash
pip install pandas
```

```python
import pandas as pd
```

---

# 🔹 Core Data Structures

## 1️⃣ Series

A one-dimensional labeled array.

```python
import pandas as pd

data = [10, 20, 30, 40]
s = pd.Series(data)
print(s)
```

With custom index:

```python
s = pd.Series(data, index=["a", "b", "c", "d"])
print(s)
```

---

## 2️⃣ DataFrame

A two-dimensional labeled data structure (rows & columns).

```python
data = {
    "Name": ["Ansh", "Rahul", "Priya"],
    "Age": [20, 21, 19],
    "Marks": [85, 90, 88]
}

df = pd.DataFrame(data)
print(df)
```

---

# 🔹 Reading & Writing Files

## Read CSV

```python
df = pd.read_csv("data.csv")
```

## Write CSV

```python
df.to_csv("output.csv", index=False)
```

## Read Excel

```python
df = pd.read_excel("data.xlsx")
```

## Write Excel

```python
df.to_excel("file.xlsx", index=False)
```

---

# 🔹 Basic Data Inspection

```python
df.head()        # First 5 rows
df.tail()        # Last 5 rows
df.shape         # (rows, columns)
df.columns       # Column names
df.info()        # Summary
df.describe()    # Statistical summary
```

---

# 🔹 Selecting Data

## Select Column

```python
df["Name"]
df[["Name", "Age"]]
```

## Select Rows (Index Based)

```python
df.iloc[0]          # First row
df.iloc[0:2]        # First two rows
```

## Select Rows (Label Based)

```python
df.loc[0]
df.loc[0:2]
```

---

# 🔹 Filtering Data

```python
df[df["Age"] > 20]
df[df["Marks"] >= 85]
```

Multiple conditions:

```python
df[(df["Age"] > 20) & (df["Marks"] > 80)]
```

---

# 🔹 Adding & Modifying Columns

## Add New Column

```python
df["Grade"] = ["A", "A+", "A"]
```

## Modify Column

```python
df["Marks"] = df["Marks"] + 5
```

---

# 🔹 Dropping Data

## Drop Column

```python
df.drop("Age", axis=1, inplace=True)
```

## Drop Row

```python
df.drop(0, axis=0, inplace=True)
```

---

# 🔹 Handling Missing Values

```python
df.isnull()            # Check null values
df.isnull().sum()      # Count null values
df.dropna()            # Remove null rows
df.fillna(0)           # Replace null with 0
```

---

# 🔹 Sorting

```python
df.sort_values("Marks")
df.sort_values("Marks", ascending=False)
```

---

# 🔹 GroupBy

```python
df.groupby("Age")["Marks"].mean()
```

---

# 🔹 Merge & Concatenate

## Merge

```python
pd.merge(df1, df2, on="id")
```

## Concatenate

```python
pd.concat([df1, df2])
```

---

# 🔹 Apply Function

```python
df["Marks"] = df["Marks"].apply(lambda x: x + 2)
```

---

# 🔹 Value Counts

```python
df["Age"].value_counts()
```

---

# 🔹 Unique Values

```python
df["Age"].unique()
df["Age"].nunique()
```

---

# 🔹 Rename Columns

```python
df.rename(columns={"Name": "Student_Name"}, inplace=True)
```

---

# 🔹 Reset Index

```python
df.reset_index(drop=True, inplace=True)
```

---

# 🔹 Duplicate Handling

```python
df.duplicated()
df.drop_duplicates()
```

---

# 🔹 Data Type Conversion

```python
df["Age"] = df["Age"].astype(int)
```

---

# 🔹 String Operations

```python
df["Name"].str.upper()
df["Name"].str.lower()
df["Name"].str.contains("A")
```

---



# ✅ Summary

Pandas is mainly used for:

✔ Data cleaning  
✔ Data transformation  
✔ Data analysis  
✔ Handling CSV / Excel files  
✔ Preparing data for Machine Learning  

---
