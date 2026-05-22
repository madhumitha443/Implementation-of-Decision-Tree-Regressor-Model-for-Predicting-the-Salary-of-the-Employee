# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the standard libraries from python.

2.Upload the dataset and check for any null values using .isnull() function.

3.Import LabelEncoder and encode the dataset.

4.Import DecisionTreeRegressor from sklearn and apply to the model from the dataset.

5.Predict the values of the arrays.

6.Import metrics from sklearn and calculate the MSE and R2 of the model from the dataset.

7.Predict the values of array

8.Apply it to the new unknown values

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: MADHUMITHA R
RegisterNumber:  212225230158
*/
import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
x=data[["Position","Level"]]
x.head()
y=data["Salary"]
y.head()
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred
from sklearn.metrics import r2_score
r2=r2_score(y_test,y_pred)
dt.predict([[5,6]])
```

## Output:
<img width="687" height="152" alt="Screenshot 2026-05-22 131825" src="https://github.com/user-attachments/assets/3264828b-bc63-4a97-abc3-73a9d8b7fe40" />
<img width="423" height="177" alt="Screenshot 2026-05-22 131747" src="https://github.com/user-attachments/assets/00d0ed66-3f35-45f4-845e-a306db41c5a0" />
<img width="540" height="261" alt="Screenshot 2026-05-22 131816" src="https://github.com/user-attachments/assets/dfc5a590-5866-47bc-886a-b869a7a0a018" />

<img width="263" height="37" alt="Screenshot 2026-05-22 131756" src="https://github.com/user-attachments/assets/f6a5c355-bfca-4a03-b2f5-3399bcf87db7" />



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
