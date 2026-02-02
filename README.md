# Customer Churn Prediction - Machine Learning Project

A comprehensive machine learning project that predicts customer churn for a telecommunications company using the Telco Customer Churn dataset.

## 📊 Project Overview

This project implements a complete ML pipeline to predict whether customers will churn (leave the service). The analysis includes:

- **Exploratory Data Analysis (EDA)** with visualizations
- **Feature Engineering** and preprocessing
- **Multiple ML Models** comparison
- **Hyperparameter Tuning** for optimal performance
- **Detailed Model Evaluation** with comprehensive metrics

## 🎯 Business Problem

Customer churn is a critical metric for subscription-based businesses. Predicting which customers are likely to churn allows companies to:

- Implement targeted retention strategies
- Reduce customer acquisition costs
- Improve customer satisfaction
- Increase lifetime customer value

## 📈 Dataset Information

**Source**: Telco Customer Churn Dataset

**Size**: 7,043 customers with 21 features

**Target Variable**: Churn (Yes/No)

**Churn Rate**: 26.54%

### Features Include:

**Customer Demographics:**
- Gender
- Senior Citizen status
- Partner status
- Dependents

**Account Information:**
- Tenure (months with company)
- Contract type (Month-to-month, One year, Two year)
- Payment method
- Paperless billing
- Monthly charges
- Total charges

**Services:**
- Phone service
- Multiple lines
- Internet service type
- Online security
- Online backup
- Device protection
- Tech support
- Streaming TV
- Streaming movies

## 🔧 Technical Implementation

### Technologies Used

- **Python 3.x**
- **Libraries**:
  - `pandas` - Data manipulation
  - `numpy` - Numerical computing
  - `scikit-learn` - Machine learning models
  - `matplotlib` & `seaborn` - Visualizations

### Machine Learning Models

Five different models were trained and evaluated:

1. **Logistic Regression**
   - Accuracy: 79.70%
   - F1 Score: 58.79%
   - ROC AUC: 84.32%

2. **Decision Tree**
   - Accuracy: 75.44%
   - F1 Score: 50.57%
   - ROC AUC: 76.09%

3. **Random Forest**
   - Accuracy: 78.28%
   - F1 Score: 54.73%
   - ROC AUC: 81.29%

4. **Gradient Boosting** ⭐ (Best Model)
   - Accuracy: 79.77%
   - F1 Score: 56.88%
   - ROC AUC: 84.46%

5. **Support Vector Machine (SVM)**
   - Accuracy: 78.64%
   - F1 Score: 54.46%
   - ROC AUC: 79.88%

### Model Selection

**Gradient Boosting** was selected as the best model based on ROC AUC score (84.46%), which is critical for this imbalanced classification problem.

After hyperparameter tuning:
- **Improved ROC AUC**: 84.63%
- **Best Parameters**: 
  - learning_rate: 0.05
  - max_depth: 3
  - min_samples_split: 5
  - n_estimators: 100

## 📊 Key Findings

### Top Predictive Features

1. **Tenure** (29.3% importance) - Longer customer relationships reduce churn
2. **Fiber Optic Internet** (19.6% importance) - Higher churn among fiber optic users
3. **Electronic Check Payment** (12.3% importance) - Payment method impacts churn
4. **Two-Year Contract** (7.9% importance) - Longer contracts reduce churn
5. **Total Charges** (6.7% importance) - Financial relationship indicator

### Business Insights

- **Contract Type**: Month-to-month contracts have significantly higher churn rates
- **Internet Service**: Fiber optic customers churn more than DSL customers
- **Tenure**: New customers (0-12 months) are at highest risk of churning
- **Payment Method**: Electronic check users churn more than automatic payment users
- **Support Services**: Customers without online security and tech support churn more

## 📁 Project Structure

```
customer-churn-prediction/
│
├── customer_churn_prediction.py    # Main analysis script
├── README.md                        # Project documentation
├── requirements.txt                 # Python dependencies
├── results_summary.txt             # Model performance summary
│
└── plots/                          # Visualization outputs
    ├── churn_distribution.png
    ├── numerical_features_churn.png
    ├── categorical_features_churn.png
    ├── correlation_heatmap.png
    ├── confusion_matrix.png
    ├── roc_curves.png
    ├── model_comparison.png
    └── feature_importance.png
```

## 🚀 How to Run

### Prerequisites

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

### Execution

```bash
python customer_churn_prediction.py
```

### Output

The script will:
1. Load and explore the data
2. Perform feature engineering
3. Train multiple ML models
4. Generate visualizations (saved to `plots/` directory)
5. Display model performance metrics
6. Save results summary

## 📉 Model Performance Metrics

### Confusion Matrix (Gradient Boosting)

|              | Predicted No | Predicted Yes |
|--------------|--------------|---------------|
| **Actual No**    | 933          | 102           |
| **Actual Yes**   | 183          | 191           |

### Classification Report

|          | Precision | Recall | F1-Score | Support |
|----------|-----------|--------|----------|---------|
| No Churn | 0.83      | 0.90   | 0.87     | 1,035   |
| Churn    | 0.66      | 0.50   | 0.57     | 374     |
| **Accuracy** |       |        | **0.80** | 1,409   |

## 💡 Recommendations

Based on the analysis, here are actionable recommendations:

### 1. **Contract Optimization**
- Encourage month-to-month customers to upgrade to annual contracts
- Offer incentives for longer-term commitments

### 2. **Early Intervention**
- Focus retention efforts on customers in first 12 months
- Implement onboarding programs for new customers

### 3. **Service Quality**
- Investigate fiber optic service quality issues
- Improve customer experience for high-speed internet users

### 4. **Payment Experience**
- Promote automatic payment methods
- Reduce friction in payment processes

### 5. **Value-Added Services**
- Bundle online security and tech support
- Demonstrate value of premium services

## 🔮 Future Improvements

1. **Advanced Models**: Try XGBoost, LightGBM, or Neural Networks
2. **Feature Engineering**: Create interaction features and time-based features
3. **Cost-Sensitive Learning**: Account for different costs of false positives vs false negatives
4. **Ensemble Methods**: Combine multiple models for better predictions
5. **Real-time Scoring**: Deploy model for real-time churn prediction
6. **A/B Testing**: Test retention strategies on predicted high-risk customers

## 📚 Learning Outcomes

This project demonstrates:

- ✅ Complete ML pipeline development
- ✅ Handling imbalanced classification problems
- ✅ Feature engineering and selection
- ✅ Model comparison and evaluation
- ✅ Hyperparameter tuning
- ✅ Business-focused data analysis
- ✅ Professional visualization and reporting

## 📝 License

This is an educational project using publicly available data for learning purposes.

## 👤 Author

Created as a comprehensive machine learning demonstration project.

---

**Note**: This project is designed for learning purposes and demonstrates best practices in machine learning project development, from data exploration to model deployment considerations.
