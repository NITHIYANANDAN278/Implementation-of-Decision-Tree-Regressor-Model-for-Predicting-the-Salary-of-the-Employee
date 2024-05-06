# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the libraries and read the data frame using pandas
2.Calculate the null values present in the dataset and apply label encoder.
3.Determine test and training data set and apply decison tree regression in dataset.
4.calculate Mean square error,data prediction and r2. 

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: NITHIYANANDAN N
RegisterNumber:212222230099  
*/
```
```
import pandas as pd
data=pd.read_csv("/content/Salary.csv")
data.head()
data.info()
data.isnull().sum()
```
```
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()

x=data[["Position","Level"]]
x.head()
y=data["Salary"]

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)

from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred) 
mse

r2=metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])
```

## Output:
### data.head()
![image](https://github.com/NITHIYANANDAN278/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/121784636/da8a4ebc-c3f6-4d28-a599-e142226aeab5)
### data.info()
![image](https://github.com/NITHIYANANDAN278/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/121784636/3308c4d2-36b8-4132-9d53-13c0704c57d5)
### isnull() and sum()
![image](https://github.com/NITHIYANANDAN278/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/121784636/11fe98d8-ab83-48f4-a35f-4a70a6d2569b)
### data.head() for salary
![image](https://github.com/NITHIYANANDAN278/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/121784636/d4729600-3a8a-4b0a-9fc6-36bd369c050e)
### MSE value
![image](https://github.com/NITHIYANANDAN278/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/121784636/3e660d38-762f-4c64-82c8-28c4bf5efeaa)
### r2 value
![image](https://github.com/NITHIYANANDAN278/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/121784636/c6f120b2-a6cd-4210-a83b-7b7e23b13330)
### data prediction
![image](https://github.com/NITHIYANANDAN278/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/121784636/97046e82-35e7-4004-9e07-b5a263c88e5d)




## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
