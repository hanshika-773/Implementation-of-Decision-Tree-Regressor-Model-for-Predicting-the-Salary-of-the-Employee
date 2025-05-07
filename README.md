# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Load the dataset Salary.csv using pandas and view the first few rows.

2.Check dataset information and identify any missing values.

3.Encode the categorical column "Position" into numerical values using LabelEncoder.

4.Define feature variables x as "Position" and "Level", and target variable y as "Salary".

5.Split the dataset into training and testing sets using an 80-20 split.

6.Create a DecisionTreeRegressor model instance.

7.Train the model using the training data.

8.Predict the salary values using the test data.

9.Evaluate the model using Mean Squared Error (MSE) and R² Score.

10.Use the trained model to predict salary for a new input [5, 6].

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Hanshika Varthini R
RegisterNumber:  212223240046

import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()

data.info

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()

x=data[["Position","Level"]]
x.head()

y=data[["Salary"]]

from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test=train_test_split(x,y,test_size=0.2,random_state=2)

from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)

from sklearn import metrics
mse=metrics.mean_squared_error(y_test, y_pred)
mse

r2=metrics.r2_score(y_test,y_pred)
r2

dt.predict([[5,6]])
*/
```

## Output:
## data.head()
![437741419-5c0b07fe-e1f7-4d34-b1b3-41a986d4d759](https://github.com/user-attachments/assets/c0d96a29-ead3-40cc-a07e-e0530f830350)
## data.info()
![437741498-b2aed347-5f2e-448a-9c16-7fc4d5d2c37b](https://github.com/user-attachments/assets/c4cd9824-f061-4c99-aef8-e76b72a58bb1)
## isnull
![437742322-c92a80f1-09b2-4c82-9013-cfb78775f660](https://github.com/user-attachments/assets/e1f7968d-b42a-41b1-9459-0b19fefb09a0)
## data position
![437742417-5617d73f-7a4a-46e0-bea2-5f34d399ceb1](https://github.com/user-attachments/assets/d395a539-3beb-4626-942e-760389778ed7)
## x.head()
![437742491-0ac1ba2f-b8de-4ad6-8414-feb860e5922d](https://github.com/user-attachments/assets/39f28ba0-46fb-4a5f-b119-8411ccb330e3)
## Mean Square Error
![437742726-6917b25d-080a-477a-9774-47ef0b3ad7d7](https://github.com/user-attachments/assets/bec60a6b-26af-4467-acd8-7e6bd4973b10)
## R2
![Screenshot 2025-05-07 092831](https://github.com/user-attachments/assets/43ae6c81-ede5-4242-a430-f5aa1f050f31)
## Prediction
![437742951-ddbcf3e7-9406-416e-a388-efca483af755](https://github.com/user-attachments/assets/ccbf21be-c182-41da-be53-82b35696953a)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
