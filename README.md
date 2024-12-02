# Machine Learning Credit Risk Analysis

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

The purpose of this analysis is to develop a Machine Learning model using Logistic Regression to help identify at-risk loans in our dataset. The analysis used the following columns to train the model:

- loan_size
- interest_rate	
- borrower_income	
- debt_to_income	
- num_of_accounts
- derogatory_marks
- total_debt

We began by loading the CSV file provided, after which the dataset was split into two subsets: one for training and one for testing. This was accomplished using the train_test_split function from the sklearn.model_selection library. The training dataset was used to fit the Logistic Regression model, while the testing dataset served to evaluate its performance.

After training the model, we introduced a new, unseen dataset to test how well the model could predict values for this data.


## Results

- Healthy Loans (0): The model is perfect here. It predicts every healthy loan correctly, without any mistakes.

- High-Risk Loans (1): The model is very good but not perfect:

    - It correctly identifies 95% of all high-risk loans.
    - Out of the loans it predicts as high-risk, 87% are actually high-risk.
    - It balances these two measures well, with an overall score of 91% for high-risk loans.
    - Overall, the model is 99% accurate, and it handles both loan types very well, even though there's a small chance it could predict some healthy loans as high-risk.

```
Confusion Matrix:
|          |   Predicted 0 |   Predicted 1 |
|:---------|--------------:|--------------:|
| Actual 0 |         18673 |            86 |
| Actual 1 |            32 |           593 |

Classification Report:
              precision    recall  f1-score   support

           0       1.00      1.00      1.00     18759
           1       0.87      0.95      0.91       625

    accuracy                           0.99     19384
   macro avg       0.94      0.97      0.95     19384
weighted avg       0.99      0.99      0.99     19384
```


## Summary

This analysis focused on developing a Logistic Regression model to identify at-risk loans using key financial features such as loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt. The dataset was prepared, split into training and testing sets, and evaluated for its predictive performance on unseen data. The model demonstrated strong overall accuracy and effectively handled the classification of both healthy and high-risk loans.