# BritishAirways_InternshipTask2
The data set provided holds a set of features which helps to find if a customer makes a booking or not.
This is an imbalanced data set as out of the 50,000 rows of data we have only 7000 rows of data with target as 'booking_complete' = 1 
but the remaining hold 'booking_complete' = 0.

#Data analysis
There were 9 numeric columns and 9 categorical columns
Total of 50,000 rows of data of which 42522 did not complete booking and 7478 completed booking making it a highly imbalanced dataset.
Heatmaps shows there is no correlation between input features  and no correlation between target and input features.
Bar plot shows that most of the data(80%) had ‘trip_type’ as ‘Round trip’ and ‘sales_channel’ as ‘Internet’

#Model Building
The categorical features were transformed using label encoders and the numerical features were standardised using the standard scaler.
This data is used to build the four classification models Gradient boosting, Random forest, Decision classifier and Logistic regression. 
Metrics like F1, accuracy, precision, recall & roc. The Gradient boost model had the highest ROC of 80%.
Also, cross validation technique was used to improve the performance. ROC metric was used as a measure since the data was highly imbalanced.

Model Building
The categorical features were transformed using label encoders and the numerical features were standardised using the standard scaler. 
This data is used to build the four classification models Gradient boosting, Random forest, Decision classifier and Logistic regression.
Metrics like F1, accuracy, precision, recall & roc. The Gradient boost model had the highest ROC of 80%. 
Also, cross validation technique was used to improve the performance. ROC metric was used as a measure since the data was highly imbalanced.


#Snippet on executing the code:
                     f1     roc_auc  accuracy precision recall 
DecisionTree       0.315298 0.598872 0.786613 0.305136 0.331434 
LogisticRegression 0.181977 0.789338 0.847840 0.466286 0.113153 
RandomForest       0.235507 0.793168 0.852347 0.516597 0.152176 
Gradient Boosting  0.162341 0.803854 0.853467 0.561761 0.094977 

Best Model per Metric
F1: DecisionTree 
Roc_auc: Gradient Boosting 
Accuracy: Gradient Boosting 
Precision: Gradient Boosting 
Recall: DecisionTree


#Model Building
The categorical features were transformed using label encoders and the numerical features were standardised using the standard scaler. SMOTE NC was used to make the imbalanced dataset as a balanced one making the original data set of 50,000 rows of data to 85044 of which 42522 completes booking and 42522 does not complete booking.

This data is used to build the four classification models Gradient boosting, Random forest, Decision classifier and Logistic regression. Metrics like F1, accuracy, precision, recall & roc. The Random forest model had the highest accuracy of 91%. Also, cross validation technique was used to improve the performance. Accuracy metric was used as a measure since the data is balanced now.

#Snippet on executing the code:
DecisionTree        0.861256  0.859695  0.860167   0.855248  0.865542
LogisticRegression  0.758968  0.823225  0.757929   0.755696  0.762284
RandomForest        0.906675  0.965613  0.910399   0.943810  0.872221
Gradient Boosting   0.893798  0.960207  0.898421   0.936409  0.854912

#Best Model per Metric
F1: DecisionTree 
Roc_auc: Gradient Boosting 
Accuracy: Gradient Boosting 
Precision: Gradient Boosting 
Recall: DecisionTree

#Conclusion
The random forest model provides better accuracy and hence considered as the most recommended model for predicting if a user will complete booking or not. Also, would highlight that most important features like fare, customer holds any loyalty points could be considered to have features which has more correlation.




