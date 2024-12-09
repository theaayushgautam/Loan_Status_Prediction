# Loan_Status_Prediction 🕵️‍♂️

## Breakdown of Key Concepts in the Code

1. Feature Scaling:

What was done:
Used StandardScaler to bring all numerical features (e.g., income, loan amount) to the same scale.
Feature scaling was essential for models like Logistic Regression and SVC that rely on distances for calculations.

2. K-Fold Cross Validation:

What was done:
Applied 5-Fold Cross-Validation using cross_val_score to evaluate model performance.
Cross-validation ensures the model generalizes well and avoids overfitting.

3. Hyperparameter Tuning:

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
