# Social Media Engagement Forecasting

Predicting Instagram post impressions and viral potential using 
machine learning. Trained 5 regression models and identified that 
saves and follower growth matter more than likes for reach.

**Best Model:** Ridge Regression — R² 0.9485, CV R² 0.8210

---

## The Problem

Content creators have no way to know in advance which posts will 
perform well. Likes and follower count alone don't explain why some 
posts reach 10x more people than others, making content strategy 
largely guesswork.

**Goal:** Predict post impressions from engagement signals so 
creators can make data-backed content decisions.

---

## Assumptions

- Past engagement patterns are stable enough to predict future 
  post performance on the same account
- Saves and follower conversions are stronger signals of algorithmic 
  amplification than passive reactions like likes
- Viral Score is a derived metric (linear combination of features), 
  not an independent target — confirmed by perfect R² = 1.000

---

## Approach

### 1. Feature Engineering
Created three derived features to capture behavioral patterns raw 
counts miss:
- Engagement Rate
- Save-to-Like Ratio  
- Follower Conversion Rate

### 2. Models Trained
| Model | R² | CV R² | MAE |
|-------|----|-------|-----|
| **Ridge** ✅ | **0.9485** | **0.8210** | 936.78 |
| Lasso | 0.9374 | 0.8057 | 1015.60 |
| Linear Regression | 0.9360 | 0.8053 | 1026.58 |
| Gradient Boosting | 0.9061 | 0.6435 | 743.21 |
| Random Forest | 0.8670 | 0.6646 | 1062.64 |

### 3. Validation
- 80/20 train-test split
- 5-fold cross-validation for generalization check
- StandardScaler for feature normalization

---

## Trade-offs

**Why not Gradient Boosting?**  
It had the lowest MAE (743.21) but its CV R² dropped to 0.6435 — 
a sign of overfitting. Ridge generalized far better.

**Why not Random Forest?**  
Underperformed across both tasks. The data has mostly linear 
relationships, so a complex ensemble wasn't needed.

**Feature engineering risk:**  
Derived ratios improve accuracy but assume consistent engagement 
behavior — may not generalize to accounts with very different 
audience sizes.

---

## Key Finding

Saves and follower growth are stronger predictors of reach than 
likes or comments. Instagram's algorithm appears to reward content 
that earns bookmarks and attracts new followers — not just passive 
reactions.

---



