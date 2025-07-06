# 🚗 Sensor Fault Detection in Intelligent Transportation Systems (ITS) using Bi-LSTM

A deep learning project to detect faults in NSPAS3 manifold absolute pressure sensors used in smart mobility systems. The solution leverages Bi-LSTM models and synthetic data generation to improve real-time diagnostics and vehicle reliability.

---

## 🧩 Problem

In modern Intelligent Transportation Systems (ITS), **sensor faults can lead to inaccurate system behavior**, delayed response, or even vehicle failure. Pressure, voltage, and temperature sensors are crucial, but rare faults are hard to detect in real-time.

---

## 🔎 Exploration

### 📁 Dataset

Collected multivariate time-series sensor data from:

- **Pressure Sensors**
- **Temperature Sensors**
- **Voltage Measurements**

Each entry included:
- Timestamp
- Sensor ID
- Measurement values
- Fault label (Normal / Faulty)

To simulate rare failure modes, **synthetic data was generated using CTGAN** to balance the dataset.

---

## 🧠 Approach

### 🧪 Model: Bi-LSTM

Used a **Bidirectional LSTM** to capture temporal patterns in both forward and backward directions. This is well-suited for time-series fault prediction.

### 🔁 Data Augmentation

Used **CTGAN (Conditional GAN)** to generate synthetic samples of rare faults and improve model generalization.

---

## 📊 Analysis & Metrics

| Metric                | Value            |
|-----------------------|------------------|
| Validation Accuracy   | **83.21%**       |
| Loss Function         | Binary Crossentropy |
| Optimizer             | Adam             |
| Epochs                | 50               |
| Batch Size            | 32               |

---

## 📉 Architecture Overview

- Input: 3D tensor (samples, time steps, features)
- Bi-LSTM Layer (128 units)
- Dropout (to avoid overfitting)
- Dense layer with sigmoid activation for binary classification

---

## 📦 Tools & Libraries Used

- ✅ **Python**
- ✅ **TensorFlow / Keras**
- ✅ **Pandas, NumPy**
- ✅ **Matplotlib, Seaborn** for plots
- ✅ **CTGAN** for synthetic data generation
- ✅ **Jupyter Notebook**

---

## 📈 Key Insights

- Real-time fault detection is achievable with Bi-LSTM architectures
- Synthetic data boosts performance in rare-class prediction
- CTGAN helped simulate edge cases that improved model robustness
- System can be extended to other automotive sensors for predictive maintenance

---
