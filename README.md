# Credit Risk Classification

![Credit Risk](12-homework-image.png)

## Background

Credit risk poses a classification problem that’s inherently imbalanced. This is because healthy loans easily outnumber risky loans. In this work, I used various techniques to train and evaluate models with imbalanced classes. I used a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

I used a logistic regression model to compare two versions of the dataset. First, I used the original dataset. Second, I resampled the data by using the `RandomOverSampler` module from the imbalanced-learn library.

For both cases, I get the count of the target classes, train a logistic regression classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.

## Steps

This activity consists of the following subsections:

* Split the Data into Training and Testing Sets

* Create a Logistic Regression Model with the Original Data

* Predict a Logistic Regression Model with Resampled Training Data

* Write a Credit Risk Analysis Report

### Split the Data into Training and Testing Sets

1. Read the `lending_data.csv` data into a Pandas DataFrame.

2. Create the labels set (`y`)  from the “loan_status” column, and then create the features (`X`) DataFrame from the remaining columns.

    > A value of 0 in the “loan_status” column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.

3. Check the balance of the labels variable (`y`)

4. Split the data into training and testing datasets by using `train_test_split`.

### Create a Logistic Regression Model with the Original Data

1. Fit a logistic regression model

2. Save the predictions on the testing data labels

3. Evaluate the model’s performance by:

    * Calculate the accuracy score of the model.

    * Generate a confusion matrix.

    * Print the classification report.

### Predict a Logistic Regression Model with Resampled Training Data

Here, I resampled the training data and then reevaluate the model. Specifically, I used `RandomOverSampler`.

I completed the following steps:

1. Used the `RandomOverSampler` module from the imbalanced-learn library to resample the data. 

2. Used the `LogisticRegression` classifier and the resampled data to fit the model and make predictions.

3. Evaluated the model’s performance by doing the following:

    * Calculate the accuracy score of the model.

    * Generate a confusion matrix.

    * Print the classification report.

