# Credit_Risk_Analysis
Supervised Machine Learning 

## Overview of the Analysis
### Purpose

Fast-Lending is a peer-to-peer lending service company. They are interested in using machine learning to predict credit risk to lower the default rate of potential customers. They would like to provide a quicker and more reliable loan service by using a machine learning model that can accurately identify low and high-risk borrowers. 
In this analysis, Python was used to build six different machine learning models to predict credit risk. Each models performance will be evaluated. The following machine learning models were created using different algorithms:

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
Balanced Accuracy Scores, Confusion Matrixes and Imbalanced Classification Reports


### Naive Random Oversampling 

* #### Accuracy Score
![naive_random_oversampling_accuracy_score](png/naive_random_oversampling_accuracy_score.png)

* #### Confusion Matrix
![naive_random_oversampling_confusion_matrix](png/naive_random_oversampling_confusion_matrix.png)

* #### Classification Report
![naive_random_oversampling_precision.](png/naive_random_oversampling_precision.png)

* Accuracy: The model correctly predicts 66.1% of the high risk classifications.
* Precison: The high_risk precision is about 1%. This means if a customer is flagged as high-risk, the probabilty of them actually being high-risk is very low. 
* Recall: The model's recall is 72%, meaning that actual high-risk applicants were identified by the model. Alternativley, 28% of acutal high-risk customers were not identified.

### SMOTE Oversampling 

* #### Accuracy Score
![smote_oversampling_accuracy](png/smote_oversampling_accuracy.png)

* #### Confusion Matrix
![smote_confusion_matrix](png/smote_confusion_matrix.png)

* #### Classification Report
![smote_classification](png/smote_classification.png)

* Accuracy: The model correctly predicts 65.8% of the high risk classifications.
* Precison: The high_risk precision is about 1%. This means if a customer is flagged as high-risk, the probabilty of them actually being high-risk is very low. 
* Recall: The model's recall is 62%, meaning that actual high-risk applicants were identified by the model. Alternativley, 38% of acutal high-risk customers were not identified.

### Undersampling with Cluster Centroids 

* #### Accuracy Score
![cluster_undersampling_accuracy](png/cluster_undersampling_accuracy.png)

* #### Confusion Matrix
![cluster_undersampling_confusion_matrix](png/cluster_undersampling_confusion_matrix.png)

* #### Classification Report
![cluster_undersampling_classification](png/cluster_undersampling_classification.png)

* Accuracy: The model correctly predicts 54.4% of the high risk classifications.
* Precison: The high_risk precision is about 1%. This means if a customer is flagged as high-risk, the probabilty of them actually being high-risk is very low. 
* Recall: The model's recall is 69%, meaning that actual high-risk applicants were identified by the model. Alternativley, 31% of acutal high-risk customers were not identified.


### SMOTEENN Combination Sampling 

* #### Accuracy Score
![smoteenn_accuracy](png/smoteenn_accuracy.png)

* #### Confusion Matrix
![smoteenn_confusion_matrix](png/smoteenn_confusion_matrix.png)

* #### Classification Report
![smoteenn_classification](png/smoteenn_classification.png)

* Accuracy: The model correctly predicts 67.1% of the high risk classifications.
* Precison: The high_risk precision is about 1%. This means if a customer is flagged as high-risk, the probabilty of them actually being high-risk is very low. 
* Recall: The model's recall is 77%, meaning that actual high-risk applicants were identified by the model. Alternativley, 23% of acutal high-risk customers were not identified.

### Balanced Random Forest Classifier

* #### Accuracy Score
![balanced_random_forest_accuracy](png/balanced_random_forest_accuracy.png)

* #### Confusion Matrix
![balanced_random_forest_confusion_matrix](png/balanced_random_forest_confusion_matrix.png)

* #### Classification Report
![balanced_random_forest_classification](png/balanced_random_forest_classification.png)

* Accuracy: The model correctly predicts 87.3% of the high risk classifications.
* Precison: The high_risk precision is about 3%. This means if a customer is flagged as high-risk, the probabilty of them actually being high-risk is very low. 
* Recall: The model's recall is 70%, meaning that actual high-risk applicants were identified by the model. Alternativley, 30% of acutal high-risk customers were not identified.


### Easy Ensemble AdaBoost Classifier

* #### Accuracy Score
![eec_accuracy](png/eec_accuracy.png)

* #### Confusion Matrix
![eec_confusion_matrix](png/eec_confusion_matrix.png)

* #### Classification Report
![eec_classification](png/eec_classification.png)

* Accuracy: The model correctly predicts 93.2% of the high risk classifications.
* Precison: The high_risk precision is about 9%. 
* Recall: The model's recall is 92%, meaning that actual high-risk applicants were identified by the model. Alternativley, 8% of acutal high-risk customers were not identified.

## Summary

