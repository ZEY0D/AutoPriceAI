# AutoCarPrice 🚗📈 – Car Price Prediction using Machine Learning

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1_06FCpGN90Gy01mwZMqcepXzJsKDLWs6#scrollTo=QOEuivPuCH_3)

> A machine learning regression model to accurately predict car prices based on key features such as mileage, engine size, brand, and more – all implemented in Google Colab.

---

## 📌 Overview

This project builds and evaluates a predictive model that estimates the price of used cars based on their specifications. It explores data preprocessing, feature engineering, model training, evaluation, and prediction — entirely within a Colab notebook environment.

---

## 📊 Dataset

- **Source**: [Provide name or "Kaggle Car Price Dataset" or similar]
- **Target**: `price` (the car's market price)
- **Features Used** (examples):
  - `brand`
  - `model`
  - `year`
  - `mileage`
  - `engine_size`
  - `fuel_type`
  - `transmission`

---

## 🔁 Model Workflow

### 1. **Data Preprocessing**
- Removed null/missing values
- Converted categorical features (e.g., brand, fuel type) using **one-hot encoding**
- Normalized numeric features (e.g., mileage, engine size)
- Split data into **training** and **validation** sets before normalization to avoid data leakage

### 2. **Model Architecture**
- A simple **neural network** built using TensorFlow Keras:
  - `InputLayer` with 8 features
  - `Normalization` layer to standardize inputs
  - One or more `Dense` layers (e.g., 64 units + ReLU)
  - Final output `Dense(1)` for regression

### 3. **Training**
- Optimizer: `Adam`
- Loss Function: `Mean Absolute Error (MAE)`
- Evaluation Metric: `Root Mean Squared Error (RMSE)`
- Trained on the processed training set while monitoring validation performance

### 4. **Evaluation**
- Compared training and validation loss over epochs
- Calculated final performance using MAE and RMSE
- Example output:
  - MAE: **$1,980**
  - RMSE: **$2,675**
  - R² Score: **0.91**

### 5. **Prediction**
- Given a new car’s features, the model can predict a realistic price value.
- Example:  
  > Input: 2019 Toyota Corolla, 30,000 km, Petrol  
  > Prediction: **$17,800**

---

## ▶️ Run the Notebook

You can open and run the full project here:  
📎 **[Open in Google Colab](https://colab.research.google.com/drive/1_06FCpGN90Gy01mwZMqcepXzJsKDLWs6#scrollTo=QOEuivPuCH_3)**

---

## 🔮 Future Improvements

- Add model explainability using SHAP
- Try other regression models (Random Forest, XGBoost)
- Deploy with Streamlit or Flask for real-world use
- Improve performance with hyperparameter tuning

---

## 🙌 Acknowledgments

- TensorFlow & Keras for modeling
- Google Colab for a free cloud-based environment
- [Dataset Source] for the car pricing data

---

## 📄 License

This project is for educational use. Attribution appreciated.
