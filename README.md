# 🚀 Key Features

### Data Preprocessing
- ✅ Outlier detection and removal using IQR method
- ✅ Handling missing values (none found in dataset)
- ✅ Encoding categorical variables (Gender, Geography)
- ✅ Feature scaling using StandardScaler

### Handling Class Imbalance
- Dataset has ~20% churn rate (imbalanced)
- **SMOTE (Synthetic Minority Over-sampling Technique)** used to create synthetic samples of the minority class
- Balanced training data: 50/50 split after SMOTE

### Models Implemented

#### 1. Logistic Regression
- **Accuracy**: 72.99%
- **AUC-ROC**: 0.8015
- **Pros**: Simple, interpretable, fast
- **Cons**: High false positives (415)

#### 2. Random Forest 🌲 (Best Model)
- **Accuracy**: 85.07%
- **AUC-ROC**: 0.8642
- **Pros**: Higher accuracy, lower false positives (128)
- **Feature Importance**: Identifies key churn factors

## 📊 Results & Performance

### Model Comparison

| Metric | Logistic Regression | Random Forest |
|--------|---------------------|---------------|
| Accuracy | 72.99% | **85.07%** |
| AUC-ROC | 0.8015 | **0.8642** |
| Precision (Churn) | 0.41 | **0.64** |
| Recall (Churn) | 0.73 | 0.60 |
| F1-Score (Churn) | 0.52 | **0.62** |
| False Positives | 415 | **128** |
| False Negatives | 106 | **96** |

### ROC Curve Comparison
![ROC Curve Comparison](images/roc_curve_comparison.png)

### Feature Importance (Random Forest)
![Feature Importance](images/feature_importance.png)

## 🔑 Key Insights

1. **Age is the strongest predictor** of churn - older customers are more likely to leave
2. **Account balance** positively correlates with churn
3. **Number of products** has negative correlation - customers with more products are more loyal
4. **Geography matters** - customers from Germany show higher churn rates
5. **Active members** are significantly less likely to churn

## 🏁 Getting Started

### Prerequisites
```bash
pip install numpy pandas matplotlib seaborn scikit-learn imbalanced-learn jupyter


