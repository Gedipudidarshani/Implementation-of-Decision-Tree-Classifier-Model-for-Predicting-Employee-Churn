# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
```
1. Start the program by importing required libraries.
2. Include the required dataset for the experiment.
3. Get the info of the data.
4. Split the given data as training and testing data
5. Import DecisionTreeClassifier to find y_pred,accuracy
6. End the program
```
## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: Gedipudi Darshani
RegisterNumber:212223230062  
*/
```
```
import pandas as pd 
data=pd.read_csv('Employee.csv')
data.head()
```
## Output:
![image](https://github.com/user-attachments/assets/84336748-62e5-4402-9e20-000e558bb906)
```
data.info()
```
## Output:
![image](https://github.com/user-attachments/assets/8bd94649-dc2c-4354-bf54-826ec4ff827e)
```
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["salary"]=le.fit_transform(data['salary'])
data.head()
```
## Output:
![image](https://github.com/user-attachments/assets/a7a615c1-c59d-4e0b-9d61-873cf5e86e5e)
```
x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","Work_accident","promotion_last_5years","salary"]]
x.head()
```
## Output:
![image](https://github.com/user-attachments/assets/214bb260-f400-4c6d-8d99-cf07c42db169)
```
y=data["left"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
```
```
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn.metrics import accuracy_score
accuracy=accuracy_score(y_test,y_pred)
accuracy
```
## Output:
![image](https://github.com/user-attachments/assets/758d49fe-1220-4e3a-81aa-343416ce9b38)
```
dt.predict([[0.5,0.8,9,260,6,0,2]])
```
## Output:
![image](https://github.com/user-attachments/assets/b5b2cfa5-f448-47e5-8af0-eadb335779ba)

## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
