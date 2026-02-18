# 🤖 TensorFlow – Complete Beginner Guide

TensorFlow is an open-source Deep Learning library developed by Google.

It is used for:
✔ Neural Networks  
✔ Deep Learning  
✔ Computer Vision  
✔ NLP  
✔ AI Applications  

---

# 📦 Installation

```bash
pip install tensorflow
```

---

# 📥 Import TensorFlow

```python
import tensorflow as tf

print(tf.__version__)
```

---

# 🧠 What is TensorFlow?

TensorFlow is used to:

- Build Neural Networks
- Train Models
- Deploy AI Models
- Work with GPUs

It supports:
✔ CPU  
✔ GPU  
✔ TPU  

---

# 🏗️ Core Concepts

## 1️⃣ Tensor

Tensor = Multi-dimensional array

Examples:

```python
import tensorflow as tf

# Scalar (0D)
a = tf.constant(5)

# Vector (1D)
b = tf.constant([1, 2, 3])

# Matrix (2D)
c = tf.constant([[1, 2], [3, 4]])

print(c)
```

---

## 2️⃣ Data Types

```python
tf.float32
tf.int32
tf.string
```

Example:

```python
x = tf.constant([1, 2, 3], dtype=tf.float32)
```

---

## 3️⃣ Tensor Operations

```python
a = tf.constant(10)
b = tf.constant(20)

print(tf.add(a, b))
print(tf.multiply(a, b))
```

---

# 🔥 Keras in TensorFlow

Keras is high-level API inside TensorFlow.

```python
from tensorflow import keras
from tensorflow.keras import layers
```

---

# 🏗️ Build Simple Neural Network

```python
model = keras.Sequential([
    layers.Dense(64, activation='relu'),
    layers.Dense(32, activation='relu'),
    layers.Dense(1, activation='sigmoid')
])
```

---

# ⚙ Compile Model

```python
model.compile(
    optimizer='adam',
    loss='binary_crossentropy',
    metrics=['accuracy']
)
```

---

# 🏋 Train Model

```python
model.fit(X_train, y_train, epochs=10, batch_size=32)
```

---

# 📊 Evaluate Model

```python
model.evaluate(X_test, y_test)
```

---

# 🔮 Make Prediction

```python
predictions = model.predict(X_test)
```

Single prediction:

```python
model.predict([[5.1, 3.5, 1.4, 0.2]])[0]
```

---

# 🎯 Activation Functions Used

- relu → Hidden layers
- sigmoid → Binary output
- softmax → Multi-class output

---

# 📉 Loss Functions

Binary classification:
- binary_crossentropy

Multi-class:
- categorical_crossentropy

Regression:
- mse (mean squared error)

---

# ⚡ Optimizers

- SGD
- Adam (Most popular)
- RMSprop

Example:

```python
optimizer = tf.keras.optimizers.Adam(learning_rate=0.001)
```

---

# 🧪 Example: Full Simple Model

```python
import tensorflow as tf
from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import Dense

model = Sequential()

model.add(Dense(64, activation='relu', input_shape=(4,)))
model.add(Dense(32, activation='relu'))
model.add(Dense(1, activation='sigmoid'))

model.compile(optimizer='adam',
              loss='binary_crossentropy',
              metrics=['accuracy'])

model.fit(X_train, y_train, epochs=10)
```

---

# 🧠 TensorFlow vs Other Libraries

| Feature | TensorFlow |
|----------|------------|
| Developed By | Google |
| High Level API | Keras |
| GPU Support | Yes |
| Production Ready | Yes |
| Mobile Deployment | Yes (TensorFlow Lite) |

---

# 📱 TensorFlow Tools

- TensorFlow Lite → Mobile deployment
- TensorFlow.js → Browser ML
- TensorBoard → Visualization tool

---

# 📊 TensorBoard Example

```python
tensorboard_callback = tf.keras.callbacks.TensorBoard(log_dir="./logs")

model.fit(X_train, y_train, epochs=10,
          callbacks=[tensorboard_callback])
```

---


# 🚀 Final Summary

✔ TensorFlow is powerful Deep Learning framework  
✔ Keras makes it easy to build models  
✔ Supports GPU acceleration  
✔ Used in real-world AI systems  

TensorFlow = Build + Train + Deploy Deep Learning Models
