# House-Price-Prediction-ML
Official implementation of the paper "AI in Real Estate: Forecasting House Prices with Advanced Machine Learning Models" (DAML 2024).
# 🏠 AI in Real Estate: Forecasting House Prices with Advanced Machine Learning Models

[![Conference](https://img.shields.io/badge/Conference-DAML%202024-blue.svg)](https://#)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Library-Scikit_Learn-orange)](https://scikit-learn.org/)
[![XGBoost](https://img.shields.io/badge/Library-XGBoost-green)](https://xgboost.readthedocs.io/)

> **Official Implementation** of the paper accepted by the *2024 2nd International Conference on Data Analysis and Machine Learning (DAML 2024)*.

## 📖 Overview
This repository contains the dataset, preprocessing pipeline, and model training code for our research on real estate price forecasting. We systematically evaluated the performance of four machine learning models to capture complex patterns within housing data.

## 📊 Methodology
Based on the Kaggle dataset (1,460 samples, 81 features), our pipeline includes:
- **Data Preprocessing:** Handled missing values (median for numerical, mode for categorical), applied One-Hot Encoding, and normalized numerical features using `StandardScaler`.
- **Feature Selection:** Mitigated multicollinearity by dropping highly correlated features based on a heatmap analysis (e.g., dropping `GarageArea` in favor of `GarageCars`).
- **Modeling:** Implemented and compared **Linear Regression**, **Decision Tree**, **Random Forest**, and **XGBoost**.

## 🏆 Quantitative Results
The evaluation on the test set demonstrates that the **XGBoost** model is the most effective in predicting house prices, achieving the lowest Mean Squared Error (MSE) and the highest R² score, successfully preventing the overfitting issue observed in the Decision Tree model.

| Model | MSE | R² Score |
| :--- | :--- | :--- |
| **XGBoost** | **685,000,624** | **0.9106** |
| Random Forest | 850,798,837 | 0.8891 |
| Linear Regression | 873,794,723 | 0.8861 |
| Decision Tree | 1,858,389,542 | 0.7577 |

## 🚀 Quick Start
To reproduce the results, you can run the Jupyter Notebook locally:
1. Clone this repository.
2. Ensure you have the required libraries installed: `pip install pandas scikit-learn xgboost`
3. Run the `House_Price_Prediction.ipynb` notebook.

## 📄 Citation
If you find this code or our paper useful in your research, please consider citing:
```text
Jiashuo Cui, Zhitong Liu, Yinghan Ma. "AI in Real Estate: Forecasting House Prices with Advanced Machine Learning Models." Proceedings of the 2024 2nd International Conference on Data Analysis and Machine Learning (DAML 2024).
