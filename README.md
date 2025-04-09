# 🏠 Bangalore House Price Prediction using Linear Regression

Predict house prices in Bangalore with machine learning! This project uses Linear Regression, Ridge, Lasso, and Polynomial Regression models to estimate housing prices based on features like location, square footage, and amenities.

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange)
![Jupyter](https://img.shields.io/badge/Environment-Jupyter_Notebook-red)

## 📂 Dataset
- **Source**: [Kaggle](https://www.kaggle.com/datasets/amitabhajoy/bengaluru-house-price-data) (Preprocessed)
- **Features**:
  - Numerical: `bath`, `balcony`, `total_sqft_int`, `bhk`, `price_per_sqft`
  - Categorical (One-Hot Encoded): `area_type`, `availability`, and 105 location columns.
- **Rows**: 7,120 | **Columns**: 108

## 🛠️ Methodology
1. **Data Splitting**: 80% training, 20% testing (`random_state=51`).
2. **Standardization**: Applied `StandardScaler` to normalize features.
3. **Models Evaluated**:
   - **Linear Regression**: Baseline model.
   - **Regularization**: Ridge (L2) and Lasso (L1) to prevent overfitting.
   - **Polynomial Regression**: Degree=2 for non-linear relationships.

## 📊 Results
| Model                | R² Score (Test) | RMSE    |
|----------------------|-----------------|---------|
| Linear Regression    | 0.79            | 64.90   |
| Ridge (α=1)          | 0.79            | -       |
| Lasso (α=1)          | 0.80            | -       |
| **Lasso (α=2)**      | **0.82**        | -       |
| Polynomial (Degree=2)| 0.999*          | -       |

*⚠️ Polynomial Regression likely overfits due to near-perfect R².*
