# Social-Media-Engagement-Forecasting
ML-powered Instagram analytics predicting post performance before publishing. Analyzes engagement patterns to forecast reach and viral potential with 90%+ accuracy. Trained 5 models identifying follower growth and saves as key metrics more important than likes alone. Enables content optimization and strategy. Python, scikit-learn, NumPy
## Overview
This project focuses on predicting Instagram post reach and identifying viral content patterns using machine learning techniques. Reach prediction helps understand what drives engagement and enables data-driven content optimization for better audience connection and growth.

Two approaches were explored and compared —
**Linear Regression** as the baseline statistical model, and **PassiveAggressiveRegressor** as an online learning approach for enhanced prediction accuracy with evolving patterns.

The proposed method integrates feature engineering and correlation analysis to identify key engagement drivers and build interpretable models that provide actionable insights for content creators.

## Objectives
* Developing a machine learning-based prediction system for Instagram post reach.

* Identifying key features that contribute to viral content and high engagement.

* Comparing multiple regression algorithms quantitatively for optimal performance.

* Evaluating performance using R² Score, Mean Absolute Error, and prediction accuracy metrics.

* Providing actionable insights for content optimization and audience growth strategies.
## Model Architecture

## Model Architecture

### Linear Regression (Baseline)
* Simple statistical model establishing linear relationships between features and reach.
* Efficient for interpretability but limited in capturing complex non-linear engagement patterns.
* Provides baseline performance metrics and feature importance insights.

### Ridge Regression (Best Model)
* Regularized linear model with L2 penalty achieving the highest R² of 0.9485 for impressions prediction.
* Effectively handles multicollinearity between correlated engagement features.
* Outperforms all models with the highest CV R² of 0.8210, confirming strong generalization on unseen data.

### Additional Models Evaluated
* **Lasso Regression**: Regularized linear model with L1 penalty for automatic feature selection.
* **Gradient Boosting Regressor**: Sequential ensemble technique — lower MAE but overfits with CV R² of only 0.6435.
* **Random Forest Regressor**: Ensemble method capturing non-linear relationships and feature interactions.

## Quantitative Results

### Impressions Prediction — Model Rankings

| **Rank** | **Model** | **R²** | **MAE** | **RMSE** | **CV R²** |
|----------|-----------|--------|---------|----------|-----------|
| 🥇 1 | **Ridge** | **0.9485** | **936.78** | **1414.19** | **0.8210** |
| 🥈 2 | Lasso | 0.9374 | 1015.60 | 1559.64 | 0.8057 |
| 🥉 3 | Linear Regression | 0.9360 | 1026.58 | 1577.19 | 0.8053 |
| 4 | Gradient Boosting | 0.9061 | 743.21 | 1909.36 | 0.6435 |
| 5 | Random Forest | 0.8670 | 1062.64 | 2272.85 | 0.6646 |

### Viral Score Prediction — Model Rankings

| **Rank** | **Model** | **R²** | **MAE** | **RMSE** | **CV R²** |
|----------|-----------|--------|---------|----------|-----------|
| 🥇 1 | **Linear Regression** | **1.0000** | **1.28e-14** | **1.75e-14** | **1.0000** |
| 🥈 2 | Ridge | 0.9999 | 5.58e-02 | 1.23e-01 | 0.9998 |
| 🥉 3 | Lasso | 0.9805 | 1.26 | 2.08 | 0.9478 |
| 4 | Gradient Boosting | 0.8297 | 2.90 | 6.15 | 0.8819 |
| 5 | Random Forest | 0.7685 | 3.48 | 7.16 | 0.8707 |

### Key Observations

* **Ridge Regression** is the best model for **Impressions Prediction** (R² = 0.9485, CV R² = 0.8210).
* **Linear Regression** achieves a **perfect R² = 1.000** for Viral Score Prediction, indicating the viral score is a direct linear combination of input features.
* **Gradient Boosting** achieves the lowest MAE (743.21) for impressions but lower CV R², suggesting mild overfitting.
* **Random Forest** underperforms across both tasks, indicating linear relationships dominate in this dataset.



