# Credit Risk Classification

This project determines two different machine learning models to predict the if a persons financial variables can predict their loan approval capabilities. 

The project is stepped out through the following steps:

## Split the Data into Training and Testing Sets
* Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.
* Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.
* A value of 0 in the “loan_status” column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.
* Check the balance of the labels variable (y) by using the value_counts function.
* Split the data into training and testing datasets by using train_test_split.



### Create a Logistic Regression Model with the Original Data
* Fit a logistic regression model by using the training data (X_train and y_train).
* Save the predictions on the testing data labels by using the testing feature data (X_test) and the fitted model.
* Evaluation of the model’s performance by doing the following:
  * Calculate the accuracy score of the model.
  * Generate a confusion matrix.
  * Print the classification report.

### Predict a Logistic Regression Model with Resampled Training Data
* Use the RandomOverSampler module from the imbalanced-learn library to resample the data. Be sure to confirm that the labels have an equal number of data points.
* Use the LogisticRegression classifier and the resampled data to fit the model and make predictions.
* Evaluate the model’s performance by doing the following:
* Calculate the accuracy score of the model.
  * Generate a confusion matrix.
  * Print the classification report.

### Report on Machine Learning Modelling
* A brief report that includes a summary and an analysis of the performance of both machine learning models is written under:
  * Supervised Learning Financial Modelling
