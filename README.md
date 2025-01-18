# Loan_Approval_Prediction

## Objective
The objective of this project is to develop a machine learning model that predicts the loan approval status for a customer's loan application. The goal is to help financial institutions minimize the risk of potential defaults and ensure that approved loans are more likely to be repaid.

## Dataset
The dataset used for this project is from one of the competition datasets on [Kaggle](https://www.kaggle.com/competitions/playground-series-s4e10/data?select=test.csv). It contains a total of 97,742 rows and 13 dimensions. The data is split into two datasets:
- **Training dataset:** 58,645 rows and 13 columns
- **Test dataset:** 13 columns

## Models and Results
After running 3 different machine learning models with varying hyperparameters and cross-validation, the Random Forest model was selected as the champion model. Here is a summary of the results:

- **Random Forest Model:**
  - Modified hyperparameters: `{'max_depth': None, 'max_features': 0.6, 'max_samples': 0.7, 'n_estimators': 100}`
  - Achieved a high precision score of **92%**
  - Prioritized for its high precision score, indicating a higher accuracy in predicting the positive class of customers whose loans should be approved.

- **XGBoost Model:**
  - Achieved a better recall score but lower precision score compared to the Random Forest model.

    
## Rationale for Model Selection
The context of the problem required prioritizing the precision score as the primary model evaluation metric. The cost of approving a loan that should be rejected (false positive) is comparatively higher than the cost of rejecting a loan application that should be approved (false negative). Therefore, the Random Forest model, which achieved a high precision score, was selected to minimize the approval of risky loans.

## Conclusion
The Random Forest model, with a precision score of 92%, aligns with the financial institution's objective of minimizing the approval of risky loans. This model effectively helps in predicting the loan approval status, thereby reducing the potential risk of defaults and improving the overall loan approval process.

## Acknowledgments
Special thanks to Kaggle for providing the dataset used in this project. 

## Author
- [Nibin Joseph](https://github.com/nibinjoseph)



