<!--# Customer Churn Prediction - Machine Learning Project

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

**Note**: This project is designed for learning purposes and demonstrates best practices in machine learning project development, from data exploration to model deployment considerations. -->

# 🤖 Customer Churn Prediction using Machine Learning

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-orange?logo=scikitlearn)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Computing-013243?logo=numpy)
![License](https://img.shields.io/badge/License-MIT-green)

An end-to-end **Machine Learning classification project** that predicts customer churn for a telecommunications company using the **IBM Telco Customer Churn Dataset**. The project demonstrates the complete machine learning lifecycle, including data preprocessing, exploratory data analysis, feature engineering, model comparison, hyperparameter tuning, and business insight generation.

---

# 📌 Project Overview

Customer churn is one of the most important business challenges faced by subscription-based companies. Acquiring a new customer is often significantly more expensive than retaining an existing one. Being able to accurately identify customers who are likely to leave allows businesses to take proactive retention actions.

This project develops a supervised machine learning solution capable of predicting customer churn based on customer demographics, account information, subscription services, and billing behavior.

The project covers every stage of a real-world machine learning workflow, including:

- Data Cleaning & Preprocessing
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Model Development
- Model Evaluation
- Hyperparameter Tuning
- Business Recommendations

---

# 🎯 Business Problem

Telecommunication companies lose thousands of customers every year due to service dissatisfaction, pricing issues, contract flexibility, and competitive alternatives.

Without predictive analytics, companies often react **after** a customer has already decided to leave.

The objective of this project is to build a predictive machine learning model capable of identifying high-risk customers before churn occurs, enabling businesses to improve customer retention and reduce revenue loss.

---

# 💡 Solution

A complete machine learning pipeline was developed to classify customers into two categories:

- **No Churn**
- **Churn**

The solution includes:

- Cleaning and preprocessing customer data
- Encoding categorical variables
- Feature engineering
- Training multiple classification algorithms
- Comparing model performance using multiple evaluation metrics
- Selecting the best-performing model
- Identifying the most influential churn factors
- Generating business recommendations based on model insights

---

# 📊 Dataset Information

This project uses the **IBM Telco Customer Churn Dataset**, one of the most widely used benchmark datasets for customer retention modeling.

| Attribute | Details |
|------------|---------|
| Domain | Telecommunications |
| Customers | 7,043 |
| Features | 21 |
| Target Variable | Churn |
| Problem Type | Binary Classification |

The dataset contains customer demographic information, subscription services, billing details, contract information, payment methods, and customer tenure.

---

# 🎯 Project Objectives

The primary objectives of this project are to:

- Predict whether a customer is likely to churn
- Compare multiple machine learning algorithms
- Identify the most important factors influencing customer churn
- Evaluate classification performance using industry-standard metrics
- Generate actionable business recommendations
- Demonstrate a complete end-to-end machine learning workflow

---

# 🏗 Machine Learning Workflow

![Workflow](plots/machinelearningwrokflow.png)

This project follows a standard supervised machine learning pipeline:

```text
IBM Telco Customer Dataset
        │
        ▼
Data Cleaning & Preprocessing
        │
        ▼
Exploratory Data Analysis
        │
        ▼
Feature Engineering
        │
        ▼
Model Training
        │
        ▼
Model Evaluation
        │
        ▼
Hyperparameter Tuning
        │
        ▼
Business Insights & Recommendations
```

---

# 📊 Exploratory Data Analysis (EDA)

Exploratory Data Analysis was performed to better understand customer behavior, identify relationships between variables, detect class imbalance, and uncover the primary drivers of customer churn.

The analysis focused on:

- Customer demographics
- Contract types
- Internet service usage
- Payment methods
- Monthly and total charges
- Customer tenure
- Feature correlations
- Churn distribution

EDA helped identify important business patterns that later contributed to feature engineering and model development.

---

# 📉 Customer Churn Distribution

![Customer Churn](plots/churn-distribution.png)

The dataset shows a clear class imbalance, with the majority of customers remaining active while approximately one-quarter of customers have churned.

Understanding this imbalance is important because evaluation metrics such as **ROC-AUC**, **Precision**, and **Recall** become more meaningful than relying solely on accuracy.

---

# 📈 Numerical Feature Analysis

![Numerical Analysis](plots/numerical-analysis.png)

Numerical variables such as **tenure**, **Monthly Charges**, and **Total Charges** were analyzed to understand how customer behavior differs between churned and retained customers.

Key observations include:

- Customers with shorter tenure exhibit significantly higher churn rates.
- Customers paying higher monthly charges are more likely to leave.
- Long-term customers generally demonstrate stronger loyalty.

---

# 📊 Categorical Feature Analysis

![Categorical Analysis](plots/categorical-analysis.png)

Categorical variables such as **Contract Type**, **Internet Service**, **Payment Method**, and **Gender** were examined to identify relationships with customer churn.

The analysis revealed that customer churn is strongly influenced by subscription type, contract duration, and payment preferences.

---

# 🔥 Correlation Analysis

![Correlation Heatmap](plots/correlation-heatmap.png)

Correlation analysis was used to identify relationships among numerical and encoded categorical variables.

Although customer churn depends on multiple interacting factors, several variables such as tenure, contract type, monthly charges, and payment method demonstrated meaningful relationships with churn behavior.

---

# 💻 Technology Stack

| Category | Technologies |
|-----------|--------------|
| Programming Language | Python 3.x |
| Machine Learning | Scikit-Learn |
| Data Manipulation | Pandas, NumPy |
| Data Visualization | Matplotlib, Seaborn |
| Model Evaluation | ROC-AUC, Accuracy, Precision, Recall, F1-Score |
| Development Environment | Jupyter Notebook |
| Dataset | IBM Telco Customer Churn Dataset |

---

# 📁 Repository Structure

```text
Customer-Churn-Analytics/
│
├── assets/
│   └── ml-workflow.png
│
├── plots/
│   ├── churn-distribution.png
│   ├── numerical-analysis.png
│   ├── categorical-analysis.png
│   ├── correlation-heatmap.png
│   ├── feature-importance.png
│   ├── model-comparison.png
│   ├── confusion-matrix.png
│   └── roc-curves.png
│
├── Customer_Churn_Analytics.ipynb
├── README.md
├── requirements.txt
├── results_summary.txt
└── LICENSE
```

---

# 🚀 Getting Started

## Prerequisites

Install the required Python packages.

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

---

## Clone Repository

```bash
git clone https://github.com/rudrasave/Customer-Churn-Analytics.git

cd Customer-Churn-Analytics
```

---

## Run the Notebook

```bash
jupyter notebook Customer_Churn_Analytics.ipynb
```

Run all notebook cells sequentially to reproduce the complete machine learning pipeline, visualizations, and model evaluation.

---

# 📈 Results Summary

The final Gradient Boosting model achieved strong predictive performance on unseen customer data.

| Metric | Value |
|---------|-------|
| Dataset Size | 7,043 Customers |
| Features | 21 |
| Best Model | Gradient Boosting |
| Accuracy | 79.77% |
| ROC-AUC | 84.46% |
| Classification Problem | Binary |

The model successfully identifies high-risk customers while maintaining strong overall predictive performance.

---

# 🎯 Business Impact

This project demonstrates practical Machine Learning and Business Analytics capabilities including:

- End-to-End Machine Learning Pipeline
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Customer Segmentation
- Classification Modeling
- Hyperparameter Tuning
- Predictive Analytics
- Business Intelligence
- Customer Retention Strategy
- Data-Driven Decision Making

---

# 🔮 Future Improvements

Potential enhancements for future versions include:

- XGBoost and LightGBM implementation
- Explainable AI using SHAP values
- Customer Lifetime Value (CLV) prediction
- Streamlit web application deployment
- Docker containerization
- Real-time churn prediction API
- Automated model retraining pipeline
- Cloud deployment using Azure or AWS

---

# 📜 License

This project is licensed under the **MIT License**.

---

# 👨‍💻 Author

**Rudra Save**

📧 Email: **rudrasave1709@gmail.com**

🔗 LinkedIn:
https://www.linkedin.com/in/rudra-save-a90749358/

💻 GitHub:
https://github.com/rudrasave

---

## ⭐ Support

If you found this project helpful, consider giving it a **⭐ Star** on GitHub.

It helps others discover the project and supports future open-source work.

