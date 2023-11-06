# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: Palleri Yogi
RegisterNumber: 212220040108
*/

import pandas as pd
data = pd.read_csv('/content/Employee[1].csv')
data.head()

data.info()
data.isnull().sum()
data["left"].value_counts()

from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
data["salary"] = le.fit_transform(data["salary"])
data.head()

data["Departments "] = le.fit_transform(data["Departments "])
data.head()
data.info()

x = data[["satisfaction_level"	,"last_evaluation",	"number_project",	"average_montly_hours",	"time_spend_company",	"Work_accident", "promotion_last_5years",	"Departments ", "salary"]]
x.info()

y = data[["left"]]
y.info()

from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test = train_test_split(x,y,test_size = 0.2, random_state=100)
x_train.shape

y_train.shape

from sklearn.tree import DecisionTreeClassifier
dt = DecisionTreeClassifier(criterion = "entropy")
dt.fit(x_train, y_train)
y_pred = dt.predict(x_test)
y_pred

from sklearn import metrics
accuracy = metrics.accuracy_score(y_test,y_pred)
accuracy

dt.predict([[]])
```

## Output:

Data Head:

![image](https://github.com/YogiReddy117/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/123739437/800d39b7-d82a-4a8f-9058-56951334e275)

Dataset Info:

![image](https://github.com/YogiReddy117/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/123739437/682b6dc8-cfb6-43cf-9b5a-b65ce669e118)

Null dataset:

![image](https://github.com/YogiReddy117/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/123739437/6e91f96f-81db-42c5-883a-7fb872499301)

Value counts in left column:

![image](https://github.com/YogiReddy117/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/123739437/6b430211-f170-4ed3-8583-3c601ee8ec92)

Dataset transformed Head:

![image](https://github.com/YogiReddy117/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/123739437/0cb351a1-ebea-48a6-b3bc-8ef7beffeb54)

x.head:

![image](https://github.com/YogiReddy117/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/123739437/dc8f482e-dd6e-4c5d-945d-9ba6d29a83ce)

Accuracy:

![image](https://github.com/YogiReddy117/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/123739437/f538ba93-522c-4731-87c5-8dff56016c73)

Data Prediction:

![image](https://github.com/YogiReddy117/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/123739437/c8032bc2-7e50-4ac0-995a-f2cd2e5a76d7)

## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
