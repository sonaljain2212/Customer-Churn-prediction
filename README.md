# Customer-Churn-prediction


Churn analysis is the evaluation of a company’s customer loss rate in order to reduce it. Also referred to as customer attrition rate, churn can be minimized by assessing your product and how people use it.


In this project, I aim to predict retention rate for a job board dataset. The proportion of custormer churned and retained is 26.9 to 73.1 %. The shape of the dataset is (37757, 15).

![Alt text](https://github.com/sonaljain2212/Customer-Churn-prediction/blob/main/images/imbalance.PNG "Optional title")

It is a classification problem and I have used two standard baseline models to observe the model performance with the unbalanced dataset. The aim is the predict the retention rate for the models:

- Logistic Regression
- Random Forest

Logistic Regression: From the confustion matrix of logistic regression, we can say that we are getting a very high true postive rate (97 %) but we also have a high False positive rate (63 %) and a very low true negative rate (37 %). The aim should be to decrease false positive and increase true negative.

Random Forest: We are getting much better results using random forest. We were able to decrese false positiive and increase true negatives. Our true positive rate slightly decreased with random forest.


![Alt text](https://github.com/sonaljain2212/Customer-Churn-prediction/blob/main/images/Confustionmatrix_logistic.PNG "Optional title")

![Alt text](https://github.com/sonaljain2212/Customer-Churn-prediction/blob/main/images/CM_RF.PNG "Optional title")

I am also going to check with adaboost classifier. Boosting algorithms combine multiple low accuracy models to create a high accuracy model. AdaBoost is example of Boosting algorithm. The important advantages of AdaBoost Low generalization error, easy to implement, works with a wide range of classifiers, no parameters to adjust. Especial attention is needed to data as this algorithm is sensitive to outliers.

![CM_Adaboost](https://user-images.githubusercontent.com/51110015/113242776-c5aec800-927f-11eb-92cd-60933c9edf91.PNG)

To handle the imbalance, I further used oversampling techinque such as SMOTE to synthetically create minority class samples and got much better reslts for Random Forest classifier then normal classification without oversampling.

![CM_Smote_RF](https://user-images.githubusercontent.com/51110015/113242940-06a6dc80-9280-11eb-99c0-e186108e91bf.PNG)



