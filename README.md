# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
Step 1: Start.

Step 2: Import required libraries.

Step 3: Add the csv file with the data. 

Step 4: Process the data before training using Label Encoder.

Step 5: Specify x and y values.

Step 6: Split your data for training and testing.

Step 7: Train your model with inbuilt function DecisionTreeRegressor().

Step 8: Find y predicted value and mean squared error.

Step 9: Print the required values.

Step 10: End.

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Cynthia Mehul J
RegisterNumber: 212223240020
*/
import pandas as pd
data=pd.read_csv("C:/Users/admin/Downloads/Salary.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["position"]=le.fit_transform(data["Position"])
data.head()
x=data[["Position","Level"]]
y=data["Salary"]
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
Y predicted Value: 
![image](https://github.com/user-attachments/assets/9f67fc58-1a5d-478a-afeb-e76ce50d2d9a)

Mean Squared Error: 
![image](https://github.com/user-attachments/assets/60d0c468-f3d9-4aa2-a0fc-aa8068429037)

r2 Score:
![image](https://github.com/user-attachments/assets/8ef3be8f-94dd-4df5-a72b-f2b7e0b4c05c)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
