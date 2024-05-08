# Credit Risk Classification Through Logistic Regression #


## Overview ##

The objective of the credit risk classification analysis was to develop a machine learning model capable of predicting the creditworthiness of borrowers by assessing the likelihood of loans being healthy or high-risk based on borrowers' financial attributes. The selected dataset is comprised of various financial features, including loan amount, interest rate, borrower annual income, debt-to-income ratio, number of accounts, derogatory marks, and total debt. The main target variable, 'loan_status', indicates whether a loan is healthy or high-risk.

To gain insight into the distribution of healthy and high-risk loans, basic information about the target variable was obtained using the value_counts() method. Logistic Regression was chosen as the baseline model due to its simplicity and interpretability.

The logistic regression process involved several stages:
  - Data Preprocessing: Creating labels set (y) and features set (X) from the dataset columns.
  - Data Splitting: Partitioning the dataset into training and testing sets using the train_test_split function.
  - Model Training: Utilizing the training data to train the logistic regression model.
  - Model Prediction: Utilizing the testing data to obtain predictions from the logistic regression model.
  - Model Evaluation: Assessing the model's performance using various metrics, including accuracy, precision, recall, and F1-score on the testing data.

## Process ##

1. Split the Data into Training and Testing Sets
    - Read the lending_data.csv data from the Resources folder into a Pandas DataFrame
    - Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns
    - Split the data into training and testing datasets by using the train_test_split function
2. Create a Logistic Regression Model with the Original Data
    - Fit a logistic regression model by using the training data (X_train and y_train)
    - Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model
    - Evaluate the model’s performance by:
        - Generation of a confusion matrix
        - Printing the classification report 

## Results ##

Machine Learning Model: Logistic Regression
  - This model achieved an accuracy score of 0.99, indicating that it correctly predicted the loan status (healthy or high-risk) for 99% of the test samples.
  - Healthy Loans:
    - Precision for healthy loans (label 0) was 1.00, indicating that when the model predicted a loan as healthy, it was correct 100% of the time.
    - The recall score for healthy loans was also 1.00, demonstrating that the model captured all actual healthy loans in the dataset.
  - High-Risk Loans:
    - For high-risk loans (label 1), the precision score was 0.87, implying that when the model predicted a loan as high-risk, it was correct about 87% of the time.
    - The recall score for high-risk loans was 0.89, suggesting that the model identified 89% of the actual high-risk loans.
  - The macro-averaged F1-score for the model was 0.94, indicating a balanced performance across both classes.

Overall, the evaluation metrics show that the model exhibited high accuracy and balanced precision and recall scores for both healthy and high-risk loans, indicating its effectiveness in predicting loan statuses.


## Summary ##

The Logistic Regression model appears to perform best, based on its high accuracy and balanced precision and recall scores, for both healthy and high-risk loans. It demonstrates robust performance in predicting loan statuses. However, the choice of the best-performing model in this situation may depend on the specific goals and priorities of the problem being solved:
  - If the primary concern is identifying high-risk loans (label 1), models with higher recall for label 1 may be preferred, as it's crucial to capture as many high-risk loans as possible to mitigate potential financial losses.
  - If minimizing false positives (precision for label 1) is critical to avoid misclassifying healthy loans as high-risk, models with higher precision for label 1 may be prioritized.

In conclusion, while the Logistic Regression model demonstrates strong overall performance, the decision on the best model to use in this analysis should consider the specific objectives and priorities of the problem, such as the importance of correctly predicting healthy and high-risk loans.

