# credit-risk-classification

## Overview of the Analysis

**Explain the purpose of the analysis.** <br>
The purpose of this analysis is to use historic lending data to assess the accuracy of a machine learning model in identifying healthy/creditworthy loans and unhealthy/un-creditworthy loans. This model is meant to assist financial institutions in easily and accurately identifying if lending to a customer presents a risk of default and a financial loss. <br>
**Explain what financial information the data was on, and what you needed to predict.** <br>
The dataset included the size of the loan, the interest rate, the borrower's income, the borrower's debt to income ratio, the number of accounts the borrower held, the number of deragatory marks on the borrorwer's credit file, and the borrorwer's total debt. <br>
**Provide basic information about the variables you were trying to predict (e.g., `value_counts`).** <br>
The variables predicted in this model were credit risk associated with a loan. Variable *loan_status: 0* were healthy loans, and variable *loan_status 1* were unhealthy loans. <br>
**Describe the stages of the machine learning process you went through as part of this analysis.** <br>
- Load the data from a CSV into a Pandas DataFrame
- Split the data into *features (x)* and *target (y)* variables
- Utlizied the logistic regression algorithm to classify loans as healthy or unhealthy
- Evaluated the model's performance based on the historic lending data
- Interpreted the accuracy and usefulness of the model <br><br>

**Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).** <br>
This model uses logistic regression to separate loans into one of two binary categories, healthy or unhealthy. 
## Results
**Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.** <br>
For healthy loans:
-    Precision: 1.00
-    Recall: 0.99
For unhealthy loans:
-    Precision: 0.85
-    Recall: 0.91
<br>
These results indicate that the model accurately assigned the "healthy" loan label to only healthy loans 100% of the time, and the model correctly identified 99% of healthy loans. 
The model assigned the "unhealthy" loan label to healthy loans 15% of the time and identified 91% of unhealthy loans in the dataset. 

## Summary
We only used one model in this assignment. The model excelled at avoiding false-negative healthy loans, meaning it did not label unhealthy loans as healthy. The model was very conservative in the assessment of unhealthy loans, and had a 15% rate of false-positives, labeling healthy loans as unhealthy. If that 15% of consumers have protected traits in common, such as race, gender, age, religious affiliation, etc, this could lead to significant issues for a lender using the model. Before using the model to make lending decisions, I would recommend a manual review of a random sample of the 15% of false-positive loans to determine what characteristics these consumers have in common to refine the model. 
