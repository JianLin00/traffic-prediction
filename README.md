# 🚦 Traffic Congestion Prediction using Crowdsourced Data  

## 📌 Overview  
This research project focuses on developing a machine learning–based model for **traffic congestion prediction** using **crowdsourced navigation data** (Waze).  
The study is aligned with **Sustainable Development Goal (SDG) 11: Sustainable Cities and Communities**, aiming to support smarter urban mobility and improved traffic management strategies.  

---

## 🎯 Research Objectives  
- To explore the crowdsourced data integration methods with traffic prediction system.
- To predict traffic congestion based on data from crowdsourced platforms using machine learning models.
- To evaluate the performance of various models in terms of MAE, RMSE, R² and MAPE.

---

## 📂 Dataset  
- **Source**: Waze for Cities Program – Brno, Czech Republic  
- **Provider**: European Open Data Portal  
- **Date Range**: March 6, 2024 – March 7, 2025  
- **Size**: ~10,000 rows × 17 columns  

---

## 🛠️ Methodology  
### 1. Data Preprocessing  
- Handled missing values (imputation and dropping).  
- Removed irrelevant variables (`blockingAlertUuid`, `type`).  
- Winsorization to reduce skewness in delay distributions.  
- Encoded categorical variables and created engineered features.  

### 2. Models Tested  
- Random Forest (RF)  
- k-Nearest Neighbors (KNN)  
- Linear Regression (LR)  
- XGBoost (XGB)  

### 3. Feature Selection & Tuning  
- **RFECV** used for feature selection.  
- **GridSearchCV (5-fold CV)** for hyperparameter tuning.  
- Evaluation metric: **R²**.  

### 4. Evaluation Metrics  
- Root Mean Squared Error (RMSE)  
- Mean Absolute Error (MAE)  
- Mean Absolute Percentage Error (MAPE)  
- R² Score  

---

## 📊 Results  
- **Tree-based models (XGBoost, Random Forest)** outperformed linear and instance-based models.  
- **XGBoost** achieved the best performance:  
  - R² = **0.893**  
  - MAE = **9.20 seconds**  
  - RMSE = **15.69 seconds**  
  - MAPE = **8.56%**  
- SHAP analysis showed **trip length, speed, and congestion level** as the most important features.  

---

## 🚀 Deployment  
The best model (**XGBoost**) was deployed using a **Streamlit dashboard**, providing:  
- Real-time traffic delay prediction based on user input (road type, traffic level, speed, trip length, etc.).  
- **Feature contribution visualization** using SHAP plots.  
- Interactive map display showing predicted traffic conditions.  

---
