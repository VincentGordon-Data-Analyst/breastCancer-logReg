# Logistic Regression Model on Breast Cancer Data

The purpose of this project was to predict weather a patient would have breast cancer or not given certain parameters(1 = 'Malignant', 0 = 'Benign') . This dataset was found on [kaggle.com]([https://www.kaggle.com/datasets/yasserh/titanic-dataset](https://www.kaggle.com/datasets/yasserh/breast-cancer-dataset)). 

This file shows how:
  1. The data was cleaned.
  2. What features were kept and which ones were dropped.
  3. Encoding certain columns.
  4. Splitting the data into training and testing sets.
  5. Finding the predicted values.
  6. Then seeing how well our model works.


## Process

### Cleaning
The data was read in using pandas dataframe. With this we are then able to manipulate the data so that it can be used for machine learning. After inspecting the dataframe it was found that only the 'id' column had to be dropped becuase it would not aid in how well the model would perform.

## Encoding
The dataframe that was left over only needed the target column (diagnosis) to be converted from being categorical data to numerical data. This was done by using scikit's preprocessing library, Label Ecoder. After this process, the machine learning model coverted any rows where the diagnosis was M (Malignant) to a 1 and B (Bening) to a 0. The final dataframe was used for splitting the dataframe columns to either being features or a target.

## Splitting
There are two key components needed for machine learning, the target value (y) and the features (X). Features are considered to be any coulmn that will influence the target value. The target value is the column that shows what the outcome has been. The data was split in a way were 20% of the data was  used for training and %80 was used for testing. 

## Findings
A confusion matrix was used to evaluate the accuracy of the model. The following values were give:
  - True Positives (TP): The number of patients correctly predicted as 'Bening' (70).
  - True Negatives (TN): The number of patients correctly predicted as "Malignant" (39).
  - False Positives (FP): The number of patients incorrectly predicted as "Bening" instead of "Malignant" (1).
  - False Negatives (FN): The number of patients incorrectly predicted as "Malignant" instead of "Bening" (4).


