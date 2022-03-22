# Credit_Risk_Analysis

### Supervised Machine Learning and Credit Risk

## Overview of the Loan Prediction Risk Analysis

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Different techniques were used to train and evaluate models with unbalanced classes. Various libraries and algorithms were used to build and evaluate models using resampling including:

* imbalanced-learn
* scikit-learn
* RandomOverSampler
* SMOTE algorithms
* ClusterCentroids algorithm
* SMOTEENN algorithm
* BalancedRandomForestClassifier (bias reduction model)
* EasyEnsembleClassifier (bias reduction model)

The purpose of this analysis is to:

1. Explain how a machine learning algorithm is used.
2. When given a dataset be able to create training and test groups.
3. Implement the logistical regression, decision tree, random forest, and support vector machine algorithms.
4. Interpret the results.
5. Compare the advantages and disadvantages of each supervised learning algorithm.
6. Determine which supervised learning algorithm is best used for a given data set or scenario.
7. Use ensemble and resampling techniques to improve model performance.

## Results

### Naive Random Oversampling

<img width="903" alt="Random Oversampling" src="https://user-images.githubusercontent.com/94575416/159394591-16128396-f1f3-4f5c-9bba-3fcedc435c71.png">

* Accuracy_score (r_squared)= .65
* Precision: The precision is low for High-risk loans and is high for Low-risk loans.
* Recall: High/Low risk = .61/.68

### Smote Oversampling

<img width="731" alt="Smote Oversampling" src="https://user-images.githubusercontent.com/94575416/159394835-bb5a7175-7bdb-495d-a7e6-5949eb1779a4.png">

* Accuracy_score (r_squared)= .62
* Precision: The precision is low for High-risk loans and is high for Low-risk loans.
* Recall: High/Low risk = .61/.64

### Undersampling

<img width="897" alt="Undersampling" src="https://user-images.githubusercontent.com/94575416/159395061-17f4bb4e-6607-4e7f-958f-921ce0075810.png">

* Accuracy_score (r_squared)= .62
* Precision: The precision is low for High-risk loans and is high for Low-risk loans.
* Recall: High/Low risk = .61/.43

### Combination Under-Over Sampling

<img width="890" alt="Combination Sampling" src="https://user-images.githubusercontent.com/94575416/159395221-63e81361-bb8f-49fb-9de6-5aa36222a3ba.png">

* Accuracy_score (r_squared): 0.52
* Precision: The precision is low for High-risk loans and is high for Low-risk loans.
* Recall: High/Low risk = .70/.58

### Balanced Random Forest Classifier

<img width="625" alt="Balanced Random Forest Classifier" src="https://user-images.githubusercontent.com/94575416/159395307-cd389db0-680f-49ed-9948-454eb7e1e538.png">

Accuracy_score (r_squared): 0.79
Precision: The precision is low for High-risk loans and is high for Low-risk loans.
Recall: High/Low risk = .91/.94

### Easy Ensemble AdaBoost Classifier

<img width="918" alt="Easy Ensemble AdaBooster Classifier" src="https://user-images.githubusercontent.com/94575416/159395501-3ae84906-c855-4cb3-a2be-22aeab9d5d6b.png">

* Accuracy_score (r_squared): 0.93
* Precision: The precision is low for High-risk loans and is high for Low-risk loans.
* Recall: High/Low risk = .91/.94

## Summary

When working with balanced accuracy, the highest compared accuracy between 0 and 1 and is closest to 1 is the best machine learning model. In the first four models we undersampled, oversampled and did a combination of both to try and determine which model is best at predicting which loans are the highest risk. For the credit card data set, the Easy Ensemble AdaBoost Classifier is the best model to choose with its .93 balanced accuracy. In our first four models our accuracy score is not as high as the ensemble classifiers and the recall in the oversampling/undersampling/mixed models is low as well. Typically in your models you want a good balance of recall and precision which is why I recommend the ensemble classifiers over the first four models. It appears that the Easy Ensemble had the best balance of all the models because of it's high accuracy score and good balance of precision and recall scores.









