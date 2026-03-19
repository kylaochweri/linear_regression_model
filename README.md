# 🧠 Mental Health Risk Prediction (Linear Regression Task)

## 📌 Project Overview

This project focuses on predicting mental health risk (depression levels) among youth using machine learning regression models. The goal aligns with the mission of reducing mental health cases among young people by identifying key contributing factors such as lifestyle, academic pressure, and social habits.

---

## 🎯 Objective

To build and evaluate regression models that can predict depression levels based on various personal, academic, and lifestyle features.

---

## 📊 Dataset

* **Name:** Student Depression Dataset
* **Source:** Kaggle
* **Author:** Shodolamu Opeyemi

### 🎯 Target Variable:

* **Depression**

---

## 🧹 Data Preprocessing

The following preprocessing steps were performed:

* Removed unnecessary column: `id`
* Handled missing values by dropping null entries
* Converted categorical variables into numerical format using Label Encoding
* Standardized features using StandardScaler to improve model performance

---

## 📈 Exploratory Data Analysis

* Data structure and types were inspected using `.info()`
* Missing values were analyzed and handled
* Relationships between variables were explored

---

## 🤖 Models Implemented

The following regression models were trained and evaluated:

1. **Linear Regression**
2. **Decision Tree Regressor**
3. **Random Forest Regressor**
4. **SGD Regressor (Gradient Descent Optimization)**

---

## 📉 Model Evaluation

Models were evaluated using **Mean Squared Error (MSE)**.

### Results:

| Model             | MSE    |
| ----------------- | ------ |
| Linear Regression | 0.1192 |
| Decision Tree     | 0.2378 |
| Random Forest     | 0.1186 |

---

## 🏆 Best Model

* **Random Forest Regressor** achieved the lowest error and was selected as the best-performing model.

---

## 📊 Visualizations

### ✔ Loss Curve

* Plotted training and testing loss using Gradient Descent (SGDRegressor)
* Showed how the model improves over iterations and stabilizes

### ✔ Scatter Plot

* Compared actual vs predicted values
* Demonstrated the model’s prediction accuracy

---

## ⚙️ Feature Engineering

* Irrelevant column (`id`) was removed
* Categorical variables were encoded
* Features contributing to mental health (e.g., sleep, academic pressure, financial stress) were retained

---

## 💾 Model Saving

The best-performing model (Random Forest) was saved using `joblib`:

```python
joblib.dump(rf, "best_model.pkl")
```

---

## 🔮 Prediction Function

A function was created to make predictions using the trained model:

```python
def predict_new(data):
    return rf.predict([data])
```

---

## 🧠 Conclusion

The project successfully demonstrates how machine learning can be used to predict mental health risk levels. The Random Forest model performed best, indicating that non-linear relationships between features play a significant role in predicting depression.

This model can be used as a foundation for building tools to support early detection and intervention in youth mental health.

---

## 🚀 Next Step (Task 2)

The saved model will be deployed using FastAPI to create an API for real-time predictions.

---
