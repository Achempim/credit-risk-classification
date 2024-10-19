# credit-risk-classification

### Overview of the Analysis

The purpose of this analysis was to build a machine learning model to predict the likelihood of loan default based on historical lending data. In financial contexts, identifying high-risk loans is critical to minimizing losses and making informed lending decisions.
The dataset used included several features, such as loan amounts, borrower income, and interest rates. The target variable was loan status, which indicates whether a loan was repaid (represented as 0) or defaulted (represented as 1). The goal was to develop a predictive model to classify loans into these two categories.

The machine learning process involved these key stages:

•	Data Preprocessing: Splitting the dataset into a feature matrix (X) and target variable (y),
•	Data Splitting: Using train_test_split to divide the data into 80% training and 20% testing sets,
•	Model Selection: We chose Logistic Regression, a straightforward and efficient algorithm for binary classification,
•	Model Training: The logistic regression model was trained on the training data to learn the patterns, and
•	Model Evaluation: Predictions were made on the test data, and we generated a confusion matrix and classification report to assess the model’s performance.

### Results

Below is the performance of the Logistic Regression model based on the classification report:

Machine Learning Model: Logistic Regression
•	Accuracy: 0.99
This metric measures the overall correctness of the model’s predictions. The model correctly predicted 99% of all loan statuses.
•	Precision:
o	For Class 0 (Loans Repaid): 1.00
All loans predicted to be repaid were indeed repaid.
o	For Class 1 (Loans Defaulted): 0.86
Out of all loans predicted to default, 86% were correct. This shows that some borrowers who were flagged as defaulters were reliable borrowers.
•	Recall:
o	For Class 0 (Loans Repaid): 0.99
The model successfully identified 99% of the loans that were repaid.
o	For Class 1 (Loans Defaulted): 0.94
The model correctly identified 94% of the loans that defaulted, meaning it missed 6% of the actual defaults.
•	F1-Score:
The F1-score, which balances precision and recall, was 1.00 for loans repaid and 0.90 for loans defaulted. This shows strong overall performance, with some room for improvement in identifying defaulters more accurately.

#### Summary

The Logistic Regression model performed exceptionally well, achieving 99% accuracy with strong precision and recall scores for both classes. Below is a summary of its strengths and considerations:

### Which metric is most important?

For a loan prediction model, recall for Class 1 (loans defaulted) is crucial. Missing a potential defaulter (false negative) could result in financial loss for the lender. In this case, the recall for loans defaulted was 0.94, which is quite high.

### Is precision for defaults important?

While precision for Class 1 (0.86) indicates some false positives (loans incorrectly predicted to default), this is less concerning than missing actual defaulters. The lender might reject a few reliable borrowers, but this trade-off is often preferable to approving risky loans.

### Recommendation

The Logistic Regression model performs very well with a high recall and accuracy. However, if further improvement is needed—especially in precision for defaulters—it might be worth exploring more advanced models like Random Forest or XGBoost. 

Fine-tuning the classification threshold in future analysis could also help achieve a better balance between precision and recall.
Given the high accuracy (0.99) and strong recall for defaulters (0.94), this model is recommended for deployment. It provides reliable predictions for managing credit risk and minimizing loan defaults.
