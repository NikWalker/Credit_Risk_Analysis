# Credit_Risk_Analysis
Supervised Machine Learning 

## Overview of the Analysis
### Purpose

Fast-Lending is a peer-to-peer lending service company. They are interested in using machine learning to predict credit risk to lower the default rate of potential customers. They would like to provide a quicker and more reliable loan service by using a machine learning model that can accurately identify low and high-risk borrowers. 
In this analysis, Python was used to build six different machine learning models to predict credit risk. Each models’ performance will be evaluated. The following machine learning models were created using different algorithms:

* Naive Random Oversampling and SMOTE algorithms were used to oversample the data
* Cluster Centroids algorithm was used to under-sampling the data
* SMOTEENN algorithm was used for a combination of over and under-sampling 
* Balanced Random Forest Classifier and Easy Ensemble AdaBoost classifier algorithms were used to reduce bias 


### Resources
* Python     
* Jupyter Notebook
* Pandas
* Scikit-learn
* Data Source: ![LoanStats_2019Q1.csv](https://github.com/NikWalker/Credit_Risk_Analysis/blob/ca575f4c5d586c0284e6867a9f01f5fa05a1a60f/Starter_Code/LoanStats_2019Q1.csv)    


## Results
Balanced Accuracy Scores, Confusion Matrixes, and Imbalanced Classification Reports


### Naive Random Oversampling 

* #### Accuracy Score
![naive_random_oversampling_accuracy_score](png/naive_random_oversampling_accuracy_score.png)

* #### Confusion Matrix
![naive_random_oversampling_confusion_matrix](png/naive_random_oversampling_confusion_matrix.png)

* #### Classification Report
![naive_random_oversampling_precision.](png/naive_random_oversampling_precision.png)

* Accuracy: The model correctly predicts 66.1% of the high-risk classifications.
* Precision: The high-risk precision is about 1%. This means if a customer is flagged as high-risk, the probability of them actually being high-risk is very low. 
* Recall: The model's recall is 72%, meaning that actual high-risk applicants were identified by the model. Alternatively, 28% of actual high-risk customers were not identified.

### SMOTE Oversampling 

* #### Accuracy Score
![smote_oversampling_accuracy](png/smote_oversampling_accuracy.png)

* #### Confusion Matrix
![smote_confusion_matrix](png/smote_confusion_matrix.png)

* #### Classification Report
![smote_classification](png/smote_classification.png)

* Accuracy: The model correctly predicts 65.8% of the high-risk classifications.
* Precision: The high-risk precision is about 1%. This means if a customer is flagged as high-risk, the probability of them actually being high-risk is very low. 
* Recall: The model's recall is 62%, meaning that actual high-risk applicants were identified by the model. Alternatively, 38% of actual high-risk customers were not identified.

### Under-sampling with Cluster Centroids 

* #### Accuracy Score
![cluster_undersampling_accuracy](png/cluster_undersampling_accuracy.png)

* #### Confusion Matrix
![cluster_undersampling_confusion_matrix](png/cluster_undersampling_confusion_matrix.png)

* #### Classification Report
![cluster_undersampling_classification](png/cluster_undersampling_classification.png)

* Accuracy: The model correctly predicts 54.4% of the high-risk classifications.
* Precision: The high-risk precision is about 1%. This means if a customer is flagged as high-risk, the probability of them actually being high-risk is very low. 
* Recall: The model's recall is 69%, meaning that actual high-risk applicants were identified by the model. Alternatively, 31% of actual high-risk customers were not identified.


### SMOTEENN Combination Sampling 

* #### Accuracy Score
![smoteenn_accuracy](png/smoteenn_accuracy.png)

* #### Confusion Matrix
![smoteenn_confusion_matrix](png/smoteenn_confusion_matrix.png)

* #### Classification Report
![smoteenn_classification](png/smoteenn_classification.png)

* Accuracy: The model correctly predicts 67.1% of the high-risk classifications.
* Precision: The high-risk precision is about 1%. This means if a customer is flagged as high-risk, the probability of them actually being high-risk is very low. 
* Recall: The model's recall is 77%, meaning that actual high-risk applicants were identified by the model. Alternatively, 23% of actual high-risk customers were not identified.

### Balanced Random Forest Classifier

* #### Accuracy Score
![balanced_random_forest_accuracy](png/balanced_random_forest_accuracy.png)

* #### Confusion Matrix
![balanced_random_forest_confusion_matrix](png/balanced_random_forest_confusion_matrix.png)

* #### Classification Report
![balanced_random_forest_classification](png/balanced_random_forest_classification.png)

* Accuracy: The model correctly predicts 87.3% of the high-risk classifications.
* Precision: The high-risk precision is about 3%. This means if a customer is flagged as high-risk, the probability of them actually being high-risk is very low. 
* Recall: The model's recall is 70%, meaning that actual high-risk applicants were identified by the model. Alternatively, 30% of actual high-risk customers were not identified.


### Easy Ensemble AdaBoost Classifier

* #### Accuracy Score
![eec_accuracy](png/eec_accuracy.png)

* #### Confusion Matrix
![eec_confusion_matrix](png/eec_confusion_matrix.png)

* #### Classification Report
![eec_classification](png/eec_classification.png)

* Accuracy: The model correctly predicts 93.2% of the high-risk classifications.
* Precision: The high-risk precision is about 9%. 
* Recall: The model's recall is 92%, meaning that actual high-risk applicants were identified by the model. Alternatively, 8% of actual high-risk customers were not identified.

## Summary

The machine learning model that performed the best used the Easy Ensemble AdaBoost Classifier algorithm. This model correctly predicted 93.2% of the high-risk classifications. The recall for this model was 92%, meaning that 8% of customers that were actually high risk were approved for the loan.  Although the precision of this model was better by at least three times over other models, it was still only able to produce a precision of 9%. This means that the model often incorrectly flagged a low risk customer as high risk. This can be bad in the banking field as this could be seen as discriminatory selection.  

Although the Easy Ensemble AdaBoost Classifier model performed the best, it would still be recommended that either this model be reconfigured to boost performance, or Fast-Lending should find an alternative route to predicting credit risk. The precision is far too low. This puts the loan provider at risk of flagging low-risk clients as high-risk. The recall should also be higher since 8% of actual high-risk clients were approved for the loan, which is not ideal for reducing the loan default rate. Fast-Lending would want a recall closer to 99% when high dollar loans are involved.


