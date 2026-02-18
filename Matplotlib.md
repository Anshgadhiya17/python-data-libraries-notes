# 📊 Matplotlib Notes

## 📌 Introduction

Matplotlib is a Python library used for:

- Data visualization
- Creating graphs and charts
- Plotting statistical data
- Visualizing trends and patterns

It is commonly used with NumPy and Pandas.

---

## 📦 Installation & Import

```bash
pip install matplotlib
```

```python
import matplotlib.pyplot as plt
import numpy as np
```

---

# 🔹 Basic Line Plot

```python
x = [1, 2, 3, 4]
y = [10, 20, 25, 30]

plt.plot(x, y)
plt.show()
```

Output:
- A simple line graph connecting the points.
- X-axis → [1,2,3,4]
- Y-axis → [10,20,25,30]

---

# 🔹 Adding Title and Labels

```python
plt.plot(x, y)
plt.title("Sample Line Chart")
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.show()
```

Output:
- Graph with title and axis labels.

---

# 🔹 Adding Markers & Line Style

```python
plt.plot(x, y, marker='o', linestyle='--')
plt.show()
```

Output:
- Dashed line with circular markers.

---

# 🔹 Multiple Lines

```python
y2 = [5, 15, 20, 25]

plt.plot(x, y)
plt.plot(x, y2)
plt.show()
```

Output:
- Two lines displayed on same graph.

---

# 🔹 Legend

```python
plt.plot(x, y, label="Line 1")
plt.plot(x, y2, label="Line 2")

plt.legend()
plt.show()
```

Output:
- Graph with legend showing Line 1 and Line 2.

---

# 🔹 Grid

```python
plt.plot(x, y)
plt.grid(True)
plt.show()
```

Output:
- Graph with background grid lines.

---

# 🔹 Bar Chart

```python
categories = ["A", "B", "C"]
values = [10, 20, 15]

plt.bar(categories, values)
plt.show()
```

Output:
- Vertical bar chart.

---

# 🔹 Horizontal Bar Chart

```python
plt.barh(categories, values)
plt.show()
```

Output:
- Horizontal bar chart.

---

# 🔹 Scatter Plot

```python
x = [1,2,3,4,5]
y = [10,15,13,17,20]

plt.scatter(x, y)
plt.show()
```

Output:
- Dots representing data points.

---

# 🔹 Histogram

```python
data = [1,2,2,3,3,3,4,4,5]

plt.hist(data, bins=5)
plt.show()
```

Output:
- Frequency distribution graph.

---

# 🔹 Pie Chart

```python
labels = ["Python", "Java", "C++"]
sizes = [50, 30, 20]

plt.pie(sizes, labels=labels, autopct='%1.1f%%')
plt.show()
```

Output:
- Circular pie chart with percentage values.

---

# 🔹 Subplots

```python
x = [1,2,3,4]
y = [10,20,30,40]

plt.subplot(1,2,1)
plt.plot(x, y)

plt.subplot(1,2,2)
plt.bar(x, y)

plt.show()
```

Output:
- Two plots in one figure (side by side).

---

# 🔹 Figure Size

```python
plt.figure(figsize=(6,4))
plt.plot(x, y)
plt.show()
```

Output:
- Graph with custom width and height.

---

# 🔹 Saving Graph

```python
plt.plot(x, y)
plt.savefig("chart.png")
plt.show()
```

Output:
- Graph saved as chart.png file.


# ✅ Summary

Matplotlib is mainly used for:

✔ Data visualization  
✔ Showing trends  
✔ Comparing categories  
✔ Displaying statistical data  
✔ Creating reports and dashboards  

---
