
![image](https://github.com/Annbelbella/Credit_Risk-Classification/assets/124645643/1dc9c378-73f1-4395-bfe9-834135d05834)

This project is based on the use of various techniques to train and evaluate a model based on loan risk to build a model that can identify the creditworthiness of borrowers.

## Purpose
The dataset comes from a financial institution and includes a number of features for users who currently have loans. The classification goal is to predict a healthy loan (0/0) or a high risk loan (1/0).

For our y variable(target), we have a very imbalanced sample. The value count is shown below;
- 0	- 75036
- 1	- 2500

### Stages of the machine Learning process for this analysis:
For the machine learning process, we split our data into train set and test set to prepare our data for two different phases of machine learning modeling: training and testing. Ideally, no information from the test data should be used to scale the training data or should be used to direct the training process of a machine learning model.

![image](https://github.com/Annbelbella/Credit_Risk-Classification/assets/124645643/97be318d-0f5a-4f34-9035-fc921835caba)

## Logistic regression with Original data
Essentially, predicting if a loan is considered high risk or not is a classification task. Our dataset contains more instances that correspond to "a healthy loan" status than instances corresponding to "risky loan" status. Specifically, out of 690 instances, there are 75036 (96.7%) applications that are healthy loans and 2500 (0.032%) applications that are risky loans. 

![image](https://github.com/Annbelbella/Credit_Risk-Classification/assets/124645643/460a9416-5b4e-42ad-8896-907c10d469a1)

### Performance of the Model 
I evaluated the model on the test set with respect to classification accuracy. I also took the model's confusion matrix. In the case of high risk or healthy loans, it is equally important to see if our machine learning model is able to predict the loan status accurately. 

![image](https://github.com/Annbelbella/Credit_Risk-Classification/assets/124645643/de4373b2-361e-46d9-8cbe-696ba2096c26)

### Results 
- **Precision** Measuring our model’s accuracy told us overall how many times we were correct when predicting the status. of the loans. For the "healthy loan" class, the precision is 1.00, indicating that the model predicts this label with perfect precision. For the "high-risk loan" class, the precision is 0.87, meaning that 87% of the predicted high-risk loans are correct.

- **Recall**, also known as sensitivity or true positive rate tells you how many times the model was able to detect a specific  label. The recall for the "healthy loan" class is 1.00, indicating that the model captures all the actual healthy loans. The recall for the "high-risk loan" class is 0.89, meaning that the model identifies 89% of the high-risk loans correctly.

- The **F1-score** is the mean of precision and recall and provides a balanced measure of the model's performance. For the "healthy loan" class, the F1-score is 1.00, indicating perfect performance. The F1-score for the "high-risk loan" class is 0.88, representing a good balance between precision and recall for this label.

- The **accuracy score** is 99%, 99 correct predictions out of 100 predictions made.

## Machine Learning Model 2:
### Resampling method
Resampling helps to generate new data points in the dataset by randomly picking data points. This is important when a data set is imbalanced, and i want to improve accuracy and overall results.

![image](https://github.com/Annbelbella/Credit_Risk-Classification/assets/124645643/e96112e1-e49c-4187-a68b-38de91ccc429)

### Description of Model 2 Results 

![image](https://github.com/Annbelbella/Credit_Risk-Classification/assets/124645643/67c422b9-8871-4c3b-8f68-f207d106a1ed)

- **Precision**. For the "healthy loan" labels, the precision is 1.00, indicating that the model predicts this label with perfect precision. For the "high-risk loan" label, the precision is 0.87, meaning that 87% of the predicted high-risk loans are correct.

- The recall for both the "healthy loan" and "high-risk loan" labels is 1.00, indicating that the model captures all the actual instances for both labels.

- **F1-Score**.For the "healthy loan" class, the F1-score is 1.00, indicating excellent performance. The F1-score for the "high-risk loan" class is 0.93, representing a good balance between precision and recall for this label.

- The accuracy score is 100%, thus our model performs exceptionally well.



# Conclusion
Based on the above factors, the "logistic regression model fit with oversampled data" would be preferred over the "logistic regression model fit with the original data. This is because after resampling, the second model performs better. We do see the number of false negatives significantly declining from 67 to 2. The false positives are also more by 11 in the second model than the first model. Our most undesirable outcome for these models is having someone predicted negative when they are actually a high-risk defaulter. The second model limits that.

The second model also has a slightly better accuracy than the first model 

It is more important to predict a high risk loan(1) than a none risk one because those are the ones which put a financial institution at risk.


# Project Outline
In this Challenge, you’ll use various techniques to train and evaluate a model based on loan risk. You’ll use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

## Instructions
The instructions for this Challenge are divided into the following subsections:

- Split the Data into Training and Testing Sets

- Create a Logistic Regression Model with the Original Data

- Write a Credit Risk Analysis Report

### Split the Data into Training and Testing Sets

- Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.

- Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.

NOTE
A value of 0 in the “loan_status” column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.

- Split the data into training and testing datasets by using train_test_split.

- Create a Logistic Regression Model with the Original Data
  
Use your knowledge of logistic regression to complete the following steps:

- Fit a logistic regression model by using the training data (X_train and y_train).

- Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.

- Evaluate the model’s performance by doing the following:

- Generate a confusion matrix.

- Print the classification report.

- Answer the following question: How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

### Write a Credit Risk Analysis Report
- Write a brief report that includes a summary and analysis of the performance of the machine learning models that you used in this homework. You should write this report as the README.md file included in your GitHub repository.

- Structure your report by using the report template that Starter_Code.zip includes, ensuring that it contains the following:

An overview of the analysis: Explain the purpose of this analysis.

The results: Using a bulleted list, describe the accuracy score, the precision score, and recall score of the machine learning model.

A summary: Summarize the results from the machine learning model. Include your justification for recommending the model for use by the company. If you don’t recommend the model, justify your reasoning.
