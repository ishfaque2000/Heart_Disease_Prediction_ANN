# 🫀 Heart Disease Prediction using ANN

![Python](https://img.shields.io/badge/Python-3.10-blue?style=flat-square&logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Keras-orange?style=flat-square&logo=tensorflow)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-lightgrey?style=flat-square)

> **Assignment 2 — Artificial Neural Networks**  
> Course: Machine Learning   
> University: Sukkur IBA University   
> Semester: 6   
> Instructor: **Atiqa Aiman**

---

## 📌 Overview

This project implements an **Artificial Neural Network (ANN)** to predict whether a patient is at risk of heart disease based on clinical and lifestyle features. Built using **TensorFlow / Keras** on a Kaggle dataset with 20+ features including cholesterol, BMI, stress level, and blood pressure.

---

## 📂 Project Structure

```
📦 heart-disease-ann
 ┣ 📓 ANN_Heart_Disease.ipynb    # Main notebook
 ┣ 📄 heart_disease.csv          # Dataset (from Kaggle)
 ┣ 📄 ANN_Heart_Disease_Report.pdf  #Full Documentation Report
 ┗ 📄 README.md
```

---

## 📊 Dataset

| Property | Details |
|---|---|
| **Source** | Kaggle — Heart Disease Dataset |
| **Task** | Binary Classification |
| **Target** | `Heart Disease Status` (Yes / No) |
| **Features** | Age, Gender, Blood Pressure, Cholesterol, BMI, Smoking, Diabetes, Stress Level, Sleep Hours, CRP Level, and more |
| **Size** | 500+ samples, 21 columns |

---

## ⚙️ Workflow

```
Data Loading
    ↓
EDA (distributions, correlations, class balance)
    ↓
Preprocessing (fill nulls → encode categoricals → StandardScaler)
    ↓
Train / Test Split  (80% / 20%)
    ↓
ANN Model (Input → Dense 64 → Dropout → Dense 32 → Dropout → Sigmoid)
    ↓
Training (50 epochs, Adam, Binary Crossentropy)
    ↓
Evaluation (Accuracy, F1, Confusion Matrix)
```

---

## 🧠 Model Architecture

```
Input Layer     →   21 features
Dense(64)       →   ReLU activation
Dropout(0.3)    →   Regularization
Dense(32)       →   ReLU activation
Dropout(0.2)    →   Regularization
Dense(1)        →   Sigmoid (binary output)
```

**Optimizer:** Adam  
**Loss:** Binary Crossentropy  
**Epochs:** 50 | **Batch Size:** 32

---

## 📈 Results

| Metric | No Disease | Disease | Overall |
|---|---|---|---|
| **Accuracy** | — | — | **79.95%** |
| **Precision** | 0.80 | 0.40 | — |
| **Recall** | 1.00 | 0.01 | — |
| **F1-Score** | 0.89 | 0.01 | — |

> **Note:** The model performs well on the majority class (No Disease) but struggles with Disease detection due to class imbalance (1600 vs 400 samples). Improvements like class weighting or oversampling (SMOTE) could boost minority class recall significantly.
---

## 🚀 How to Run

```bash
# 1. Clone the repo
git clone https://github.com/ishfaque2000/heart-disease-ann.git
cd heart-disease-ann

# 2. Install dependencies
pip install tensorflow pandas numpy matplotlib seaborn scikit-learn

# 3. Open the notebook
jupyter notebook ANN_Heart_Disease.ipynb
```

> Make sure `heart_disease.csv` is in the same directory as the notebook.

---

## 🛠 Tech Stack

- **Python 3.10**
- **TensorFlow / Keras** — ANN model
- **Scikit-learn** — preprocessing & evaluation
- **Pandas / NumPy** — data handling
- **Matplotlib / Seaborn** — visualization

---

## 👤 Author

**Ishfaque Ahmed**  
BS Mathematics — Semester 6 | Sukkur IBA University  
STHP Scholar | Data Scientist & ML Engineer  

[![LinkedIn](https://img.shields.io/badge/LinkedIn-ishfaque2090-blue?style=flat-square&logo=linkedin)](https://linkedin.com/in/ishfaque2090)
[![GitHub](https://img.shields.io/badge/GitHub-ishfaque2000-black?style=flat-square&logo=github)](https://github.com/ishfaque2000)

---

*Submitted as part of ML coursework — Sukkur IBA University, 2026*
