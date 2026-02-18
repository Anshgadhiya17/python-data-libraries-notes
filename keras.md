# 🧠 Keras – Complete Beginner Guide

Keras is a high-level Deep Learning API built on top of TensorFlow.

It is used for:
✔ Building Neural Networks  
✔ Training Deep Learning Models  
✔ Fast Prototyping  
✔ Easy Model Deployment  

---

# 📦 Installation

If TensorFlow installed, Keras already included.

```bash
pip install tensorflow
```

---

# 📥 Import Keras

```python
from tensorflow import keras
from tensorflow.keras import layers
```

---

# 🔥 Why Use Keras?

✔ Easy to use  
✔ Less code  
✔ Beginner friendly  
✔ Runs on CPU & GPU  
✔ Production ready  

Keras = Simple + Powerful Deep Learning

---

# 🏗️ Ways to Build Model in Keras

1️⃣ Sequential API  
2️⃣ Functional API  

---

# 1️⃣ Sequential API (Most Common)

Used when layers are stacked one after another.

---

## 🧱 Build Simple Neural Network

```python
from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import Dense

model = Sequential()

model.add(Dense(64, activation='relu', input_shape=(4,)))
model.add(Dense(32, activation='relu'))
model.add(Dense(1, activation='sigmoid'))

model.summary()
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

# 🔮 Prediction

```python
predictions = model.predict(X_test)
```

Single prediction:

```python
model.predict([[5.1, 3.5, 1.4, 0.2]])[0]
```

---

# 2️⃣ Functional API (Advanced)

Used when:
✔ Multiple inputs  
✔ Multiple outputs  
✔ Complex architecture  

---

## Example:

```python
from tensorflow.keras import Input, Model
from tensorflow.keras.layers import Dense

inputs = Input(shape=(4,))
x = Dense(64, activation='relu')(inputs)
x = Dense(32, activation='relu')(x)
outputs = Dense(1, activation='sigmoid')(x)

model = Model(inputs, outputs)
```

---

# 🧠 Important Layers in Keras

## Dense Layer
Fully connected layer

```python
Dense(units=64, activation='relu')
```

---

## Dropout Layer
Used to reduce overfitting

```python
from tensorflow.keras.layers import Dropout

model.add(Dropout(0.5))
```

---

## Flatten Layer
Used in CNN models

```python
from tensorflow.keras.layers import Flatten
```

---

# 🎯 Activation Functions

- relu → Hidden layers
- sigmoid → Binary output
- softmax → Multi-class output
- linear → Regression

---

# 📉 Loss Functions

Binary Classification:
- binary_crossentropy

Multi-Class:
- categorical_crossentropy
- sparse_categorical_crossentropy

Regression:
- mse (mean squared error)

---

# ⚡ Optimizers

- SGD
- Adam (Most popular)
- RMSprop
- Adagrad

Example:

```python
from tensorflow.keras.optimizers import Adam

optimizer = Adam(learning_rate=0.001)
```

---

# 📦 Save & Load Model

## Save:

```python
model.save("my_model.h5")
```

## Load:

```python
from tensorflow.keras.models import load_model

model = load_model("my_model.h5")
```

---

# 📊 Callbacks

Used to control training process.

## Early Stopping:

```python
from tensorflow.keras.callbacks import EarlyStopping

early_stop = EarlyStopping(monitor='val_loss', patience=3)

model.fit(X_train, y_train,
          validation_data=(X_val, y_val),
          epochs=20,
          callbacks=[early_stop])
```

---

# 📈 Model Summary

```python
model.summary()
```

Shows:
✔ Number of layers  
✔ Parameters  
✔ Output shape  

---

# 🧠 Keras vs TensorFlow

| Feature | Keras | TensorFlow |
|----------|--------|------------|
| Level | High-level | Low-level + High-level |
| Ease of Use | Very Easy | Moderate |
| Customization | Limited | Advanced |
| Backend | Runs on TensorFlow | Core framework |

---

# 🚀 Final Summary

✔ Keras is high-level Deep Learning API  
✔ Very beginner friendly  
✔ Built on TensorFlow  
✔ Used for building Neural Networks easily  
✔ Supports CPU & GPU  

Keras = Fast & Easy Deep Learning Development
