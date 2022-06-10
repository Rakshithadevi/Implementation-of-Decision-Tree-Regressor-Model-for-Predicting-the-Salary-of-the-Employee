# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.Import pandas as pd and import the required dataset.
2.Calculate the null values in the dataset.
3.Import the LabelEncoder from sklearn.preprocessing
4.Convert the string values to numeric values.
5.Import train_test_split from sklearn.model_selection.
6.Assign the train and test dataset.
7.Import DecisionTreeRegressor from sklearn.tree.
8.Import metrics from sklearn.metrics.
9.Calculate the MeanSquareError.
10.Apply the metrics to the dataset.
11.Predict the output for the required values.
## Program:
```

Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: RAKSHITHA DEVI J
RegisterNumber: 212221230082

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
y=data["Salary"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred)
mse
r2=metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])

```

## Output:
## data.head():
![image](https://user-images.githubusercontent.com/94165326/173088297-ede45bc9-690f-4ea4-8d68-ccda259a3c57.png)


## data.info():
![image](https://user-images.githubusercontent.com/94165326/173088343-5192c32b-1c13-4de2-bce2-de132cd1688e.png)


## data.isnull():
![image](https://user-images.githubusercontent.com/94165326/173088392-95e5a517-b303-4b0f-8c25-3c97b1e0f4ef.png)


## data.head() using labelencoder:
![image](https://user-images.githubusercontent.com/94165326/173088429-7800fa18-77bd-4b3e-8f95-f1615c585837.png)


## Mean squared error:
![image](https://user-images.githubusercontent.com/94165326/173088634-013a754f-3362-4d07-8370-9795d5507b60.png)


## R2:
![image](https://user-images.githubusercontent.com/94165326/173088669-556a4a6b-be87-48bb-92b6-328f15ea8939.png)


## prediction:
![image](https://user-images.githubusercontent.com/94165326/173088717-5cf102b8-2d91-493f-88fb-126b9758e9df.png)




## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
