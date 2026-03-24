# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required libraries.

2.Upload and read the dataset.

3.Check for any null values using the isnull() function.

4.From sklearn.tree import DecisionTreeClassifier and use criterion as entropy.

5.Find the accuracy of the model and predict the required values by importing the required module from sklearn

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Kamaleshwaran S
RegisterNumber:  212225040165
*/
import pandas as pd
from IPython.display import display


data = pd.read_csv("Employee.csv")
print("===== DATA HEAD (5 ROWS) =====")
display(data.head())

print("\n===== DATA INFO =====")
print(data.info())

print("\n===== MISSING VALUES =====")
display(data.isnull().sum().to_frame("Missing Values"))

from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
data["salary"] = le.fit_transform(data["salary"])
print("\n===== X HEAD (5 ROWS) =====")
display(x.head())

from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test = train_test_split(
    x, y, test_size=0.2, random_state=100
)

from sklearn.tree import DecisionTreeClassifier
dt = DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train, y_train)


y_pred = dt.predict(x_test)

from sklearn import metrics
accuracy = metrics.accuracy_score(y_test, y_pred)
print("\n===== MODEL ACCURACY =====")
print("Accuracy:", accuracy)

# Prediction for new employee record
print("\n===== PREDICTION =====")
print(dt.predict([[0.5, 0.8, 9, 260, 6, 0, 1, 2]]))
```

## Output:
<img width="1424" height="284" alt="image" src="https://github.com/user-attachments/assets/62dad57c-8d3a-48c8-b148-7351a462ce23" />
<img width="585" height="423" alt="image" src="https://github.com/user-attachments/assets/33915aed-6fa8-4184-804b-233d2916109c" />
<img width="441" height="428" alt="image" src="https://github.com/user-attachments/assets/706a1350-59a9-48d2-89d2-73eff26d5cd1" />
<img width="469" height="77" alt="image" src="https://github.com/user-attachments/assets/592ed7d1-d126-47b6-a737-3fc99a22a8b8" />
<img width="1266" height="266" alt="image" src="https://github.com/user-attachments/assets/274f15ff-7180-4c91-8caa-63b064de00d5" />
<img width="385" height="142" alt="image" src="https://github.com/user-attachments/assets/cf8a275c-d7e6-42a2-90b7-769cc3b9f8a1" />








## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
