# credit-risk-classification
## Overview of the Analysis

* The project aims to utilize various machine learning techniques to train and evaluate a model for assessing loan risk.
* The dataset used is derived from historical lending activity of a peer-to-peer lending services company. The goal is to build a model capable of identifying the creditworthiness of borrowers based on the provided dataset.
* `loan_status` column was used to better predict healthy loans vs high-risk loans.
* Following are the stages of the machine learning process went through as part of this analysis:
  - Read `lending_data.csv` into a Pandas DataFrame.
  - Create labels set (y) from the “loan_status” column and features (X) DataFrame from the remaining columns.
  - Split the data into training and testing datasets using `train_test_split`.
  - Fit a logistic regression model using the training data (X_train and y_train).
  - Save predictions for the testing data labels using the fitted model.
  - Evaluate the model’s performance:
    - Calculate the accuracy score.
    - Generate a confusion matrix.
    - Print the classification report.
* Methods `LogisticRegression` and `RandomOverSampler` were used to better fit the model and make predictions.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* **Machine Learning Model 1:**
  * Model 1 Logistic Regression with `Original data`.
    - **Accuracy Score:** 95%
    - **Precision Score:** 100% precision with healthy loans and 85% precision with high-risk loans.
    - **Recall Score:** 99% of recall score for healthy loans and 91% of recall score for high-risk loans.

* **Machine Learning Model 2:**
  * Model 2 Logistic Regression with `RandomOverSampler`.
    - **Accuracy Score:** 99%
    - **Precision Score:** 100% precision with healthy loans and 84% precision with high-risk loans.
    - **Recall Score:** 99% of recall score for healthy loans and 99% of recall score for high-risk loans.

## Summary

The machine learning model demonstrated high accuracy, indicating credit risk classification is highly interpreted. Both the models perform well; however, the `RandomOverSampler` model does give a better recall score. The accuracy score reflects the overall correctness of predictions, precision highlights the model's ability to avoid false positives, and recall emphasizes its effectiveness in capturing true positives.

**Recommendation:**
Based on the model's performance, it is recommended for use by the company. The high accuracy score suggests confidence in its ability to make correct predictions. The high precision score indicates the level of false positive risk is very low, while the recall score signifies over 90% how well the model captures true positives.

**Justification:**
This model's strengths align with the company's goals for predicting healthy loans. There are few limitations and areas of improvement for high-risk loans where the model may not be suitable for practical because it is prediction for high-risk loans is low.

## Conclusion 

This analysis provides valuable insights into credit risk prediction, and the recommendation to use the model is grounded in its observed performance and alignment with the company's objectives. Further considerations may include potential improvements or areas for future exploration.
