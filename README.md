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

### Linear Regression (Baseline)
* Simple statistical model establishing linear relationships between features and reach.
* Efficient for interpretability but limited in capturing complex non-linear engagement patterns.
* Provides baseline performance metrics and feature importance insights.

### Gradient Boosting Regressor (Improved)
* Advanced ensemble technique building trees sequentially to correct previous errors.
* Robust to outliers and effective for social media data with varying distributions.
* Better handles viral posts and extreme values through iterative optimization.

### Additional Models Evaluated
* **Ridge Regression**: Regularized linear model with L2 penalty for handling multicollinearity.
* **Lasso Regression**: Regularized linear model with L1 penalty for automatic feature selection.
* **Random Forest Regressor**: Ensemble method combining multiple decision trees to capture non-linear relationships.
