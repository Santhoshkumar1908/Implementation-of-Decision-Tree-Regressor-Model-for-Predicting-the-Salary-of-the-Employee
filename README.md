# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import pandas
2. Import Decision tree classifier
3. Fit the data in the model
4. Find the accuracy score

## Program:
```

Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: SANTHOSHKUMAR J
RegisterNumber: 212225230249 

```
~~~
import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
~~~
~~~
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
~~~
~~~
x=data[["Position","Level"]]
x.head()
y=data["Salary"]
y.head()
~~~
~~~
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
~~~
~~~
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred
from sklearn.metrics import r2_score
r2=r2_score(y_test,y_pred)
~~~
~~~
R2 score:  0.48611111111111116
~~~
~~~
dt.predict([[5,6]])
~~~

## Output:

<img width="1120" height="345" alt="Screenshot 2026-05-17 202435" src="https://github.com/user-attachments/assets/2a100498-5833-4325-aafb-b1c4509d0f71" />


<img width="536" height="256" alt="Screenshot 2026-05-17 202443" src="https://github.com/user-attachments/assets/03c9c8f4-bc76-4665-b3ae-a94f39391de3" />


<img width="933" height="171" alt="Screenshot 2026-05-17 202452" src="https://github.com/user-attachments/assets/af41d654-8e9e-47ce-b22b-0605df62bf93" />


<img width="432" height="49" alt="Screenshot 2026-05-17 202502" src="https://github.com/user-attachments/assets/91fa4bee-8ed5-4259-9548-5a9bc4332354" />


<img width="254" height="35" alt="Screenshot 2026-05-17 202507" src="https://github.com/user-attachments/assets/96b09ee4-708d-4aa7-84eb-ad51362c0499" />



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
