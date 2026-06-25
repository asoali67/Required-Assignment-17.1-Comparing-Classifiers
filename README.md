# Required-Assignment-17.1-Comparing-Classifiers

## Introduction
The objective of this analysis is to use different classification models to select the best model using models scoring on the data. The banking data has many features to determin applicats eligibility for a loan. 


1. First i analyzed the data and i found out that the target is very unbalanced 

<img width="685" height="839" alt="image" src="https://github.com/user-attachments/assets/3150ffaf-f79d-4898-9cd9-44f78b351fd1" />

2. Then i ran the data on models with default parameter and without any haper parameters. To do a basic comparison of the models scores
   
| Model        | Train Time | Train Accuracy | Test Accuracy | Test Precision | Test Recall | Test f1 |
| -----        | ---------- | -------------  | -----------   | ----------     | ----------  | -----------   |
|Decision Tree | 0.143      | 1.000          | 0.880         | 0.465          | 0.451       |  0.458 |
|SVM           | 4.418      | 0.923          | 0.908         | 0.686	      |0.335       |  0.450|
| KNN          |   0.027    |   0.924        | 0.901         | 0.602          | 0.355       | 0.446         |
|Logistic Regression|   0.046  |   0.911     | 0.906         | 0.668          | 0.327       | 0.439         |

From the above performance data. Decision Tree has the best f1 score, however with Training accuracy of one implies that there was an overfitting. 
SVM has the second best f1 score but with the largest training time and that would be an issue big data’s but it is the best model for current data. 
KNN has performed third best and specially would be my choice model with default settings and specially for big data’s.
The target data is very unbalanced and i have doubt about the Logistic regression results

3. I ran gird serach on the models to fined the best hyperparameters for each model

| Model        | Train Time | Train Accuracy | Test Accuracy | Test Precision | Test Recall | Test f1 |
| -----        | ---------- | -------------  | -----------   | ----------     | ----------  | -----------   |
|Decision Tree | 0.057      | 0.917          | 0.909         | 0.633          | 0.449       |  0.526     |
|SVM           | 30.529     | 0.913          | 0.908         | 0.698	      |0.327       |  0.445     |
|Logistic Regression|   0.063 |   0.911     | 0.906         | 0.668          | 0.323       | 0.436         |
| KNN          |   0.022    |   0.904        | 0.903         | 0.696          | 0.244       | 0.361         |

Looking at the final comparison with models have hyperparameters, Decision tree had the highest f1 score and test accuracy, and low training time. 
And it’s a best model to be used, i do not believe there is an overfitting in this scenario.
SVM had second best f1 score and Test accuracy but with very bad training time, and Logistic regression and KNN did not perform 
as good as Decision Tree. 

4. to check the ROC curves for each model i ploted the Tru positive Rate agaist the False Positive Rate
   <img width="564" height="453" alt="image" src="https://github.com/user-attachments/assets/deafc313-134b-4d11-ab7d-6c8899a9e980" />


## Recomendations
From looking at the ROC curve, all models seem to be having curve close to each other. Considering other scoring factors and training time. 
I do select Decision Tree and KNN as two models to be used to predict future classifications.
I do have discarded SVM because of the big training time, and unless there is a big scoring advantage of using SVM i would for now discard this model.
For Logistic Regression model, as i indicated before, the target data is very unbalanced and it would predict majority class. Therefore, i did not select this model for given data.


