## 📊 Credit Risk Analysis & Default Prediction (Lending Club Dataset)

## 📖 Overview
This project analyzes borrower data to identify key factors associated with loan default and builds a predictive model to classify high-risk borrowers.

The goal is to simulate a real-world credit risk analysis process used in financial institutions.

## 🧠 Objective
- Analyze borrower characteristics related to default risk
- Identify key risk indicators (income, interest rate, grade, DTI)
- Build a classification model to predict loan default

## 📦 Dataset
- Source: Lending Club Loan Data (Kaggle)
- Size used: ~50,000 rows
- Target variable:
  0 = Fully Paid
  1 = Charged Off (Default)

##🧹 Data Cleaning
- Selected relevant financial features
- Converted percentage columns (int_rate, revol_util) to numeric
- Extracted numeric values from text fields (term, emp_length)
- Filtered dataset to include only valid loan statuses
- Handled missing values using imputation

##📊 Exploratory Data Analysis (EDA)
Key visualizations:
- Default distribution
- Interest Rate vs Default
- Grade vs Default
- Income vs Default
- Debt-to-Income (DTI) vs Default

##🔍 Key Insights
- Borrowers with higher interest rates are more likely to default
- Lower credit grades (E–G) show significantly higher default rates
- Borrowers with lower income tend to default more frequently
- Higher DTI (debt-to-income ratio) is strongly associated with default risk
- Data contains skewed distributions and outliers (especially income)

##🤖 Model Building
Model used: Logistic Regression
Steps:
- One-hot encoding for categorical variables
- Train-test split (80/20)
- Model training and prediction

##📈 Model Performance

Accuracy: 78.4%

Confusion Matrix:
[[6741   241]
 [1656   163]]

##⚠️ Model Evaluation
- The model performs well in predicting non-default loans
- However, it struggles to identify default cases (high false negatives)
- This limitation is critical in financial risk management

##🧠 Business Interpretation
- Missing a default (false negative) is more costly than misclassifying a safe borrower
- Model improvement should focus on increasing recall for default class
- Potential improvements:
    - Handling class imbalance
    - Trying advanced models (Random Forest, XGBoost)

##🛠️ Tools & Technologies
- Python
- pandas
- seaborn / matplotlib
- scikit-learn

##🚀 Conclusion
This project demonstrates an end-to-end data analysis workflow:
- Data cleaning
- Exploratory analysis
- Insight generation
- Predictive modeling

It reflects practical skills required for a Data Analyst role in the finance domain.

##📁 Project Structure
credit-risk-analysis/
│
├── credit-risk-analysis.ipynb
├── README.md
└── data/
    └── accepted_2007_to_2018Q4.csv 
