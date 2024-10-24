# credit-risk-classification

### Overview of the Analysis

The purpose of this analysis was to build a machine learning model to predict the likelihood of loan default based on historical lending data. Identifying high-risk loans is essential to minimize losses and make informed lending decisions.

The dataset included multiple features such as loan amount, borrower income, and interest rates. The target variable, loan status, indicates whether a loan was:

- 0: Repaid (healthy loan)
- 1: Defaulted (high-risk loan)

The goal was to develop a predictive model to classify loans into these two categories.

#### Machine Learning Process
Below are the key steps involved in building and evaluating the model:

- Data Preprocessing:
Splitting the dataset into a feature matrix (X) and target variable (y).
- Data Splitting:
Using train_test_split to divide the data into 80% training and 20% testing sets.
- Model Selection:
Logistic Regression was chosen as it is a straightforward and efficient algorithm for binary classification.
- Model Training:
The Logistic Regression model was trained on the training data to identify patterns.
- Model Evaluation:
Predictions were made on the test set, followed by a confusion matrix and classification report to assess the model's performance.

### Results
Below is the performance summary of the Logistic Regression model based on the classification report:

#### Accuracy
- Overall Accuracy: 0.99
  - The model correctly predicted the loan status for 99% of all loans.

#### Precision
- Class 0 (Healthy Loan - Repaid): 1.00
  - Every loan predicted as repaid was indeed repaid.

- Class 1 (High-Risk Loan - Defaulted): 0.86
  - 86% of loans predicted as defaults were correct. The remaining 14% were flagged incorrectly as high-risk despite being reliable borrowers.

#### Recall
- Class 0 (Healthy Loan - Repaid): 0.99
  - The model identified 99% of the loans that were repaid.

- Class 1 (High-Risk Loan - Defaulted): 0.94
  - The model correctly detected 94% of the actual defaulters, missing only 6% of defaults.

#### F1-Score
- Class 0 (Healthy Loan - Repaid): 1.00
- Class 1 (High-Risk Loan - Defaulted): 0.90
  - This score balances precision and recall, showing strong overall performance but indicating that further improvements could enhance the identification of defaulters.

### Summary
The Logistic Regression model performed exceptionally well, achieving 99% accuracy with strong precision and recall for both healthy and high-risk loans.

### Key Metrics for Loan Prediction
- Most Important Metric:
  -Recall for Class 1 (high-risk loans) is critical. Missing a defaulter (false negative) could result in significant financial loss. In this case, the model’s recall of 0.94 shows strong effectiveness in identifying risky borrowers.

- Is Precision Important for Defaults?
  - While precision for defaults (0.86) reveals some false positives, this is less critical than recall. Lenders may prefer to reject a few reliable borrowers rather than approve risky loans.

### Recommendation
The Logistic Regression model offers reliable predictions for managing credit risk with:

- High accuracy (0.99)
- Strong recall for defaulters (0.94)

### Next Steps
Explore advanced models like Random Forest or XGBoost to improve precision for defaulters.
Fine-tune the classification threshold to achieve a better trade-off between precision and recall.
Based on its current performance, the model is recommended for deployment to support lending decisions and minimize loan defaults.