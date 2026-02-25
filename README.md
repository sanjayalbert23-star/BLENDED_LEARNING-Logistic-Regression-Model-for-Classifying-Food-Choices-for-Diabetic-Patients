# BLENDED_LEARNING
# Implementation of Logistic Regression Model for Classifying Food Choices for Diabetic Patients

## AIM:
To implement a logistic regression model to classify food items for diabetic patients based on nutrition information.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Data Collection and Preprocessing Load the food nutrition dataset, handle missing values, encode categorical labels, and normalize the nutritional features using scaling techniques.

2. Data Splitting Split the dataset into training and testing sets using an appropriate ratio (e.g., 80% training and 20% testing).

3. Model Training Train a Logistic Regression model using the training dataset to learn the relationship between nutritional features and diabetic suitability.

4. Model Evaluation and Prediction Test the model on the testing dataset and evaluate performance using accuracy, precision, recall, F1-score, and confusion matrix. Use the trained model to classify food items as suitable or unsuitable for diabetic patients.

## Program:
```
/*
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression
from sklearn.preprocessing import LabelEncoder, MinMaxScaler
from sklearn.metrics import accuracy_score, precision_score, recall_score, f1_score, confusion_matrix, classification_report
import seaborn as sns
import matplotlib.pyplot as plt
#Load the dataset
df = pd.read_csv('food_items (1).csv')
#Inspect the dataset
print('Name : SANJAY A')
print('Reg. No: 212225040367')
print("Dataset Overview:")
print(df.head())
print("\nDataset Info:")
print(df.info())

X_raw = df.iloc[:, :-1]

y_raw = df.iloc[:, -1:]

scaler = MinMaxScaler()

# Scaling the raw input features

X = scaler.fit_transform(X_raw)

# Create a LabelEncoder object

label_encoder = LabelEncoder()

#Encode the target variable

y = label_encoder.fit_transform(y_raw.values.ravel())

#Note that ravel() function flattens the vector.

#First, let's split the training and testing dataset

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, stratify=y, random_state = 123)

#L2 penalty to shrink coefficients without removing any features from the model

penalty= 'l2'

# Our classification problem is multinomial

multi_class = 'multinomial'

#Use lbfgs for L2 penalty and multinomial classes

solver = 'lbfgs'

#Max iteration 100e

max_iter = 1000

#Define a logistic regression model with above arguments

l2_model = LogisticRegression (random_state=123, penalty=penalty, multi_class=multi_class, solver=solver, max_iter=max_iter)

l2_model.fit(X_train, y_train)

y_pred = l2_model.predict(X_test)

# Evaluate the model

print('Name : SANJAY A')

print('Reg. No : 212225040367')

print("\nModel Evaluation:")

print("Accuracy:", accuracy_score(y_test, y_pred))

print("\nClassification Report:")

print(classification_report(y_test, y_pred))

#Confusion Matrix conf_matrix confusion_matrix(y_test, y_pred) print(conf_matrix)

conf_matrix=confusion_matrix(y_test,y_pred)
print(conf_matrix)
Developed by:SANJAY A
RegisterNumber: 212225040367 
*/
```

## Output:

![alt text](<Screenshot 2026-02-25 220214.png>)
![alt text](<Screenshot 2026-02-25 220227.png>)


## Result:
Thus, the logistic regression model was successfully implemented to classify food items for diabetic patients based on nutritional information, and the model's performance was evaluated using various performance metrics such as accuracy, precision, and recall.
