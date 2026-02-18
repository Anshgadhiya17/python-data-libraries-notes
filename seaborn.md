# 📊 Seaborn Library 

Seaborn is a Python data visualization library built on top of Matplotlib.

It provides:
✔ Beautiful default themes  
✔ Easy statistical plots  
✔ Better integration with Pandas DataFrame  

---

# 📦 Installation

```bash
pip install seaborn
```

---

# 📥 Import Library

```python
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
```

---

# 🎨 Built-in Themes

```python
sns.set_style("darkgrid")
sns.set_style("whitegrid")
sns.set_style("dark")
sns.set_style("white")
sns.set_style("ticks")
```

---

# 📚 Load Built-in Dataset

```python
tips = sns.load_dataset("tips")
print(tips.head())
```

Other datasets:
- iris
- titanic
- flights
- diamonds

---

# 📊 1️⃣ Scatter Plot

```python
sns.scatterplot(x="total_bill", y="tip", data=tips)
plt.show()
```

With hue:

```python
sns.scatterplot(x="total_bill", y="tip", hue="sex", data=tips)
plt.show()
```

---

# 📈 2️⃣ Line Plot

```python
sns.lineplot(x="total_bill", y="tip", data=tips)
plt.show()
```

---

# 📊 3️⃣ Bar Plot

```python
sns.barplot(x="day", y="total_bill", data=tips)
plt.show()
```

---

# 📦 4️⃣ Histogram

```python
sns.histplot(tips["total_bill"], kde=True)
plt.show()
```

kde=True → adds smooth density curve

---

# 📉 5️⃣ Box Plot

```python
sns.boxplot(x="day", y="total_bill", data=tips)
plt.show()
```

Used to detect:
✔ Outliers  
✔ Median  
✔ Quartiles  

---

# 🎻 6️⃣ Violin Plot

```python
sns.violinplot(x="day", y="total_bill", data=tips)
plt.show()
```

Combination of:
- Boxplot
- Density plot

---

# 🔥 7️⃣ Count Plot

```python
sns.countplot(x="sex", data=tips)
plt.show()
```

Used for:
✔ Counting categorical values

---

# 🧊 8️⃣ Heatmap

```python
corr = tips.corr(numeric_only=True)
sns.heatmap(corr, annot=True, cmap="coolwarm")
plt.show()
```

Used for:
✔ Correlation matrix visualization  

---

# 🧬 9️⃣ Pair Plot

```python
sns.pairplot(tips)
plt.show()
```

Shows:
✔ All numerical column relationships  

---

# 🎯 10️⃣ Joint Plot

```python
sns.jointplot(x="total_bill", y="tip", data=tips, kind="scatter")
plt.show()
```

Other kinds:
- hex
- kde
- reg

---

# 🧪 11️⃣ Regression Plot

```python
sns.regplot(x="total_bill", y="tip", data=tips)
plt.show()
```

Adds regression line automatically.

---

# 🎨 Change Color Palette

```python
sns.set_palette("Set2")
```

Other palettes:
- deep
- muted
- pastel
- bright
- dark
- colorblind

---

# 📊 Figure Size Change

```python
plt.figure(figsize=(8,5))
sns.barplot(x="day", y="total_bill", data=tips)
plt.show()
```

---

# 🔹 Difference: Matplotlib vs Seaborn

| Feature | Matplotlib | Seaborn |
|----------|------------|----------|
| Styling | Basic | Beautiful default |
| Statistical plots | Manual | Built-in |
| DataFrame support | Limited | Excellent |
| Heatmap | Manual | Simple |

---

# 🚀 When to Use Seaborn?

✔ Data Analysis  
✔ EDA (Exploratory Data Analysis)  
✔ Correlation visualization  
✔ Categorical comparison  
✔ Statistical plotting  

---

# 🔥 Final Summary

✔ Seaborn is built on Matplotlib  
✔ Best for statistical visualization  
✔ Works great with Pandas  
✔ Very useful for EDA  

Seaborn = Beautiful + Simple + Powerful visualization library
