# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Load the employee dataset using Pandas and convert categorical data into numerical format using one-hot encoding.
2.Separate the dataset into input features (X) and target variable (y), then split it into training and testing sets.
3.Train a DecisionTreeClassifier model using the training data and predict the results for the test data.
4.Evaluate the model accuracy using accuracy_score() and visualize the decision tree using plot_tree() with Matplotlib.

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: Krithik kiran .S
RegisterNumber:  212225230145
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeClassifier, plot_tree
from sklearn.metrics import accuracy_score
data = pd.read_csv("Employee.csv")
data = pd.get_dummies(data, drop_first=True)
X = data.iloc[:, :-1]
y = data.iloc[:, -1]
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)
model = DecisionTreeClassifier(random_state=42)
model.fit(X_train, y_train)
y_pred = model.predict(X_test)
print("Accuracy:", accuracy_score(y_test, y_pred))
plt.figure(figsize=(20,10))

plot_tree(
    model,
    feature_names=X.columns,
    filled=True
)

plt.show()
*/
```

## Output:
<img width="1378" height="709" alt="WhatsApp Image 2026-05-13 at 9 28 33 AM" src="https://github.com/user-attachments/assets/5b1a28f3-f18b-407a-aef6-e0c70365d681" />



## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
