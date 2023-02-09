# BerkeleyML_Module_17

Data for 18 campaigns was analyzed. The goal is to develop a model that can predict the outcome of a contact, specifically whether a client will subscribe to a deposit.  

Results obtained before GridSearchCV (simple models) are presented in the table below:
  
|index|model|Train Time|Train Accuracy|Test Accuracy|
|---|---|---|---|---|
|0|Baseline|0\.01810598373413086|0\.8873458288821987|0\.8873458288821987|
|0|Logistic Regression|0\.4761533737182617|0\.8873458288821987|0\.8873458288821987|
|0|SVM|88\.07465100288391|0\.8880903823120002|0\.8864717878993882|
|0|KNN|0\.13619256019592285|0\.8910685960312065|0\.8772457997474993|
|0|Decision Tree|0\.8143112659454346|0\.9177754038393059|0\.8668544236185297|

As we can see the best model in terms of test accuracy was LogisticRegression, it is also worth to mention that this model had also a good performance in terms of fitting time. However, it did not performed better than the baseline model.

After conducting the GridSearchCV in order to improver performance, despite LogisticRegression remained as the best performing model. The performance was not improved. Processing time increased considerably for knn with a degradataion of performance. A more detailed study of the gridsearch parameters seems adequate to improve results.

|index|model|Accuracy|Time|
|---|---|---|---|
|0|GridSearch Logistic Regression|0\.8873458288821987|30\.361032962799072|
|0|GridSearch Decision Tree|0\.8873458288821987|599\.8790147304535|
|0|GridSearch KNN|0\.8872163413291897|1649\.7819254398348|
|0|GridSearch Decision Tree|0\.8864717878993882|65\.09175658226012|

