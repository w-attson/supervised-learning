# Supervised Learning Financial Modelling

### Purpose of the Analysis.
The primary objective of this analysis is to investigate if machine learning can be utilised to predict credit risk. Analysis of credit risk is a primary function of the financial sector than ensures that lending can be offered in a safe manner for both the lender and the borrower. 

### Financial information the data was on, and what you needed to predict.

The following items are some of the variables that created the dataset for the machine learning modelling:
* Loan size
* Interest Rate
* Borrower income
* Debt to income ratio
* Number of accounts
* Derogatory Marks
* Total Debt

### Prediction Aim
The primary goal was to predict the loan status, indicating whether a loan is likely to be of high risk or is healthy. This can be quantified by the (value_counts) of the (loan_status) column.

### Stages of the machine learning process
* Data Preprocessing: This step involved cleaning and preparing the data, which included handling missing values, encoding categorical variables, and scaling numerical variables.
* Feature Selection and Splitting: The relevant features were selected and the data was split into training and testing datasets.
* Model Training: The training data was fed into the model to "teach" it.
* Model Testing and Validation: The testing data was used to evaluate the model's performance. This included computing metrics like accuracy, precision, recall and other metrics
* Resampling (if required): To address class imbalances, techniques like oversampling were employed.
* Model Iteration: Based on the model's performance, necessary adjustments were made, and the model was retrained if needed.

### Methods used

The primary model employed for this analysis was LogisticRegression, which is well-suited for binary classification problems like credit risk prediction. Given that our dataset might have had class imbalances, resampling techniques were considered. The RandomOverSampler method was used to balance out the number of high-risk and healthy loans in the dataset.


## Results

### Machine Learning Model 1 (Logistic Regression)
* Healthy Loan Predictions
    * Precision: 1.00 – This means that when the model predicts a loan is healthy, it's correct 100% of the time.
    * Recall: 0.99 – This indicates that the model correctly identified 99% of all actual healthy loans.
    * Specificity: 0.91 – This shows that the model correctly identified 91% of the high-risk loans when trying to identify healthy loans.
    * F1-score: 1.00 – The harmonic mean of precision and recall, suggesting that the model has a balanced performance in predicting healthy loans.
    * Geometric Mash: 0.95 - With this value, the model has shown a balanced performance in classifyng healthy loans with 95%. 
    * Index of Balanced Accuracy: 0.91 - The model has requires some improvement when classifying healthy loans. But, overall the model can be seen as satisfactory. 

* High-Risk Loan Predictions
    * Precision (pre): 0.85 – When the model predicts a loan is high-risk, it's correct 85% of the time.
    * Recall (rec): 0.91 – The model correctly identified 91% of all actual high-risk loans.
    * Specificity (spe): 0.99 – The model correctly identified 99% of the healthy loans when trying to identify high-risk loans.
    * F1-score (f1): 0.88 – This suggests a balanced performance in predicting high-risk loans, though slightly lower than for healthy loans.
    * Geometric Mash: 0.95 - With this value, the model has shown a balanced performance in classifyng healthy loans with 95%. 
    * Index of Balanced Accuracy: 0.90 - The model has requires some improvement when classifying high-risk loans. 



### Machine Learning Model 2 (Logistic Regression w/Oversampling):
* Healthy Loan Predictions
    * Precision (pre): 1.00 – This means that when the model predicts a loan is healthy, it's correct 100% of the time.
    * Recall (rec): 0.99 – This indicates that the model correctly identified 99% of all actual healthy loans.
    * Specificity (spe): 0.99 – This shows that the model correctly identified 99% of the high-risk loans when trying to identify healthy loans.
    * F1-score (f1): 1.00 – The harmonic mean of precision and recall, suggesting that the model has a very balanced performance in predicting healthy loans.
    * Geometric Mash: 0.99 - The oversampled model performed very well with a 99%. This indicates a well balanced performance.
    * Index of Balanced Accuracy: 0.99 - The oversampled model performed very well with a 99%.

* High-Risk Loan Predictions
    * Precision (pre): 0.84 – When the model predicts a loan is high-risk, it's correct 84% of the time.
    * Recall (rec): 0.99 – The model correctly identified 99% of all actual high-risk loans.
    * Specificity (spe): 0.99 – The model correctly identified 99% of the healthy loans when trying to identify high-risk loans.
    * F1-score (f1): 0.91 – This suggests a balanced performance in predicting high-risk loans.
    * Geometric Mash: 0.99 - The oversampled model performed very well with a 99%. This indicates a well balanced performance.
    * Index of Balanced Accuracy: 0.99 - The oversampled model performed very well with a 99%. 


## Summary

Both models demonstrated capabilities in classifying loans. While the first model provided a reasonable baseline, the second oversampling model effectively countered the class imbalance and elevated the detection rate for high-risk loans.

Greater Performer: Drawing from the evaluated metrics, and particularly the heightened recall for high-risk loans, the second machine learning model utilising oversampling is better.

Evaluating Performance: The emphasis on the importance of recall stems from the nature of the problem. In the context of credit risk, false negatives (misclassifying high-risk loans as healthy) can be more costly than false positives (misclassifying healthy loans as high-risk). Therefore, a model with higher recall for high-risk loans would be preferable.

Considering the potential financial implications surrounding loan allocations, Machine Learning Model 2 is the recommended choice. It is more capable at predicting high-risk loans and demonstrates higher performance overall. 
