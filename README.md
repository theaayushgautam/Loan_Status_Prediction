# Loan Status Prediction Using Machine Learning 🚀

# Overview 📋
This end-to-end machine learning project predicts loan approval status based on customer profiles. Using Python and scikit-learn, the project includes data preprocessing, feature scaling, model training, evaluation, and hyperparameter tuning. A GUI was also built for easy user interaction.

# Project Workflow 🔧
1. Data Loading
2. Exploratory Data Analysis (EDA)
3. Data Cleaning & Missing Value Handling
4. Feature Engineering (Encoding Categorical Features)
5. Feature Scaling
6. Model Training and Evaluation
7. Hyperparameter Tuning
8. Cross-Validation (K-Fold)
9. Model Deployment & GUI

## Breakdown of Key Concepts in the Code

1. Feature Scaling:

What was done:
Used StandardScaler to bring all numerical features (e.g., income, loan amount) to the same scale.
Feature scaling was essential for models like Logistic Regression and SVC that rely on distances for calculations.

2. Feature Encoding
To use categorical data in machine learning models, the categorical features were converted into numeric features using Label Encoding. Each category was replaced with a corresponding numeric value. For example:

"Yes" → 1, "No" → 0
"Male" → 1, "Female" → 0
"Urban", "Semi-Urban", "Rural" → 2, 1, 0


3. K-Fold Cross Validation:

What was done:
Applied 5-Fold Cross-Validation using cross_val_score to evaluate model performance.
Cross-validation ensures the model generalizes well and avoids overfitting.

4. Hyperparameter Tuning:

What was done:
Tuned parameters for models using RandomizedSearchCV to optimize model performance.
Example: Logistic Regression and SVC were fine-tuned for hyperparameters like C (regularization).

# Insights from the Project

1. Key Influencing Features:

Credit history was the most important factor for loan approvals.
Applicant and co-applicant incomes were also major drivers for the decision.

2. Model Performance:

Default Models: Logistic Regression and SVC performed decently but needed hyperparameter tuning.
Post-Tuning:
Random Forest: Achieved the highest accuracy (~80%) post hyperparameter tuning.
SVC: Improved performance but still fell short of Random Forest.

3. Missing Values Strategy:

Columns with <5% missing data (e.g., gender, dependents) were dropped.
Columns like self_employed and credit_history were imputed with their most frequent values(mode).

4. Feature Scaling:

Ensured features like income, loan amount, and loan term were on the same scale, preventing features with large magnitudes from dominating.

5. Cross-Validation Insight:
5-Fold Cross Validation proved essential in assessing model performance, showing that Random Forest generalizes well across multiple folds.
