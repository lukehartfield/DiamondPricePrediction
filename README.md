# 💎 Predicting Diamond Prices Using Machine Learning

*Data Science Project – University of Texas at Austin*

---

### 📍 Overview

This project explored how **physical characteristics and quality attributes** of diamonds (e.g., carat, cut, clarity, color, dimensions) influence pricing. Using a dataset of **53,940 diamonds**, we applied multiple machine learning models to predict price and uncover feature importance.

Our goal was twofold:

1. Understand which features most strongly influence diamond prices.
2. Build a highly accurate regression model to predict future prices.

---

### 🧠 Problem Framing

> Research Question: Can we accurately predict the price of a diamond using its physical and quality attributes?
> 

We framed this as a **supervised regression** task using historical data and evaluated multiple ML models based on **RMSE**, **R²**, and residual analysis.

---

### 🧪 Data Science Methods Used

| Category | Techniques Applied |
| --- | --- |
| **EDA** | Visualizations (pairplot, correlation matrix, bar charts) |
| **Feature Engineering** | Ordinal encoding (cut, color, clarity), calculated volume (length × width × depth) |
| **ML Models** | Linear Regression, Decision Tree, Pruned Tree, Bagging, Random Forest, XGBoost |
| **Evaluation Metrics** | RMSE, MSE, R², Actual vs. Predicted Scatter Plots |
| **Validation Strategy** | 80/20 Train/Test Split |

---

### 📊 Modeling Results

| Model | RMSE | R² |
| --- | --- | --- |
| ❌ Linear Regression | 1204.86 | 0.91 |
| ⚠️ Decision Tree (Pruned) | 1333.14 | 0.89 |
| ✅ Random Forest | **535.14** | **0.98** |
| ✅ XGBoost | 542.84 | 0.88 |

> 📌 Random Forest was the best-performing model, with 98% R² and $535 average error in predictions.
> 

---

### 📈 Feature Insights

Using feature importance analysis, we discovered:

- **Carat and Volume** are the strongest predictors of price.
- **Clarity and Color** also significantly impact pricing.
- Surprisingly, **Cut**, **Depth**, and **Table Size** had minimal influence.

---

### 🛠️ Key Skills Gained

| Category | Skills & Tools |
| --- | --- |
| **Data Prep** | Feature engineering, outlier handling, encoding categorical data |
| **Modeling** | Scikit-learn, XGBoost, tree-based ensemble methods |
| **Evaluation** | Interpreting RMSE/R², error diagnostics, comparing model robustness |
| **ML Thinking** | Handling overfitting, using ensembling (bagging/boosting), pruning trees |
| **Team Collaboration** | Co-authoring analysis, discussing model tradeoffs, version control with Jupyter/IPython |

---

### 📌 Takeaways

- Raw features (carat, clarity) don't tell the full story—*derived features* like volume add value.
- Simpler models (like linear regression) struggled due to nonlinear interactions and multicollinearity.
- **Tree-based models** (Random Forest & XGBoost) captured complex patterns and outperformed linear approaches by a wide margin.
- Even in high-dimensional but structured datasets, **model interpretability and domain logic** remain crucial.

---

### 💡 Impact

This model could help:

- **Consumers** avoid overpaying for low-value stones
- **Sellers** price more competitively
- **Marketplaces** improve transparency and pricing consistency

The approach is generalizable to other luxury goods or any domain with **structured, numeric, and ordinal features** driving price.
