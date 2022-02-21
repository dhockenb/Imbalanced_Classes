# Credit Risk Classification by Statisical Resampling

## This Jupyter notebook application uses machine learning approaches to analyze historical loan data from a peer-to-peer lending services company for classification of credit risk by logistic regression. The available data included detailed information on >77,000 loans, including debt to income ratio, loan size, interest rate, derogatory marks on account as features and a binary label for loan status. The binary label data was severely imbalanced, with only 3.3% high-risk loans. The data was first split into training and testing sets, and the training dataset was used to fit a logistic regression model. The fitted model was then used to generate predictions for the testing dataset. Next, in view of the small number of high-risk loans, an oversampling strategy was employed. The performance of the two logistic regression models was compared by accuracy scores, confusion matrices and classification reports. Algorithms for data splitting and logistic regression were imported from scikit-learn.org and oversampling and imbalanced performance metrics from imbalanced-learn.org

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Balanced accuracy score 0.95 
  * Precision score (healthy loans) 1.00 
  * Precision score (high-risk loans) 0.85
  * Recall score (healthy loans) 0.99
  * Recall score (high-risk loans) 0.91 


* Machine Learning Model 2:
  * Balanced accuracy score 0.99
  * Precision score (healthy loans) 1.00
  * Precision score (high-risk loans) 0.84
  * Recall score (healthy loans) 0.99 
  * Recall score (high-risk loans) 0.99

## Summary

Machine Learning Model 2 with oversampling is preferred in this project. The geometric mean score reported in the classification report (imbalanced) is the root of the product of class-wise sensitivity (recall) and indicates very high recall for both classes in Machine Learning Model 2 compared to Machine Learning Model 1. The precision for the '0' class (healthy loans) is slightly lower with oversampling in Machine Learning Model 2, but this is likely a good trade-off for peer-to-peer lending. In other words, the higher recall for high-risk loans in Machine Learning Model 2 indicates greater sensitivity to predict high-risk loans with the trade-off of slightly lower sensitivity to predict healthy loans. Since high-risk loans represent potential losses, this is the preferred model. 



