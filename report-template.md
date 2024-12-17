# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).
* 
 Ans:
  The purpose of this analysis was to evaluate machine learning models for predicting loan risk, specifically identifying whether a loan is high-risk or healthy. The dataset provided             financial information on loans, where each loan was classified as either a healthy loan (denoted by '0') or a high-risk loan (denoted by '1'). The task was to develop a model that             could predict whether a loan would be high-risk or healthy based on various financial features.
      
  The target variable we were trying to predict is the loan risk category, represented by the loan_status variable, with two possible values: '0' (healthy) and '1' (high-risk). The dataset is    highly imbalanced, with significantly more healthy loans than high-risk loans.
      
  Variables:
     Loan Status: The target variable. Values: 0 (healthy loan), 1 (high-risk loan).
     Other features in the dataset include financial indicators such as loan amount, interest rate, payment history, and income.
  Stages of the Machine Learning Process:
     Data Preprocessing: The dataset was cleaned to remove any missing or irrelevant data. We also addressed the class imbalance problem using techniques such as over-sampling and under-            sampling.
  Model Selection: Various machine learning models were considered, and we chose logistic regression for its simplicity and interpretability.
  Model Training: We split the dataset into training and test sets to evaluate the model’s performance.
  Model Evaluation: The models were evaluated using metrics such as accuracy, precision, recall, and F1-score to assess their effectiveness in predicting both healthy and high-risk loans.
 

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    * Description of Model 1 Accuracy, Precision, and Recall scores.

Ans:
 
Machine Learning Model 1: Logistic Regression
Accuracy: 0.99 - The model correctly predicted 99% of the total loan status.

Precision for '0' (Healthy Loans): 1.00 - The model perfectly identified healthy loans, with no false positives.

Recall for '0' (Healthy Loans): 1.00 - The model successfully identified all healthy loans.

Precision for '1' (High-Risk Loans): 0.87 - The model predicted 87% of the high-risk loans correctly, with some false positives.

Recall for '1' (High-Risk Loans): 0.95 - The model identified 95% of the actual high-risk loans, showing strong recall.

F1-Score for '0' (Healthy Loans): 1.00 - Perfect balance between precision and recall for healthy loans.

F1-Score for '1' (High-Risk Loans): 0.91 - Strong performance in balancing precision and recall for high-risk loans.

Macro Average:
Precision: 0.94
Recall: 0.97
F1-Score: 0.95

Weighted Average:
Precision: 0.99
Recall: 0.99
F1-Score: 0.99


## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.

Ans:
The logistic regression model demonstrated excellent performance, particularly in predicting healthy loans (with perfect precision and recall). While the model performed well in identifying high-risk loans (with recall of 0.95), its precision for high-risk loans (0.87) suggests there were some false positives. However, the high recall for high-risk loans means that it correctly identifies a large proportion of high-risk loans, which is critical in minimizing financial losses.

The model performs exceptionally well overall, with an accuracy of 99%. It is highly recommended for use by the company, particularly for its ability to accurately predict healthy loans and identify high-risk loans with a good balance of precision and recall.

Recommendation: The logistic regression model is recommended for use by the company, as it provides a reliable and efficient approach for predicting both healthy and high-risk loans. If further improvement is needed for high-risk loan predictions, the model could be tuned or other algorithms explored. However, given the strong results, this model is a solid choice for the task.

