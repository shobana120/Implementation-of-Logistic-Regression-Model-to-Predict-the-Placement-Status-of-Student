# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required packages and print the present data
2. Print the placement data and salary data.
3. Find the null and duplicate values.
4. Using logistic regression find the predicted values of accuracy , confusion matrices.
## Program:
```
/*
Developed by: SHOBANA B
RegisterNumber: 212224230262

import pandas as pd
data=pd.read_csv("C:/Users/admin/Downloads/Midhun/Placement_Data.csv")
data.head()

data1=data.copy()
data1=data1.drop(["sl_no","salary"],axis=1)#Browses the specified row or column
data1.head()

data1.isnull().sum()

data1.duplicated().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data1["gender"]=le.fit_transform(data1["gender"])
data1["ssc_b"]=le.fit_transform(data1["ssc_b"])
data1["hsc_b"]=le.fit_transform(data1["hsc_b"])
data1["hsc_s"]=le.fit_transform(data1["hsc_s"])
data1["degree_t"]=le.fit_transform(data1["degree_t"])
data1["workex"]=le.fit_transform(data1["workex"])
data1["specialisation"]=le.fit_transform(data1["specialisation"] )     
data1["status"]=le.fit_transform(data1["status"])
data1 

x=data1.iloc[:,:-1]
x

y=data1["status"]
y

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.linear_model import LogisticRegression
lr=LogisticRegression(solver="liblinear")
lr.fit(x_train,y_train)
y_pred=lr.predict(x_test)
y_pred

from sklearn.metrics import accuracy_score
accuracy=accuracy_score(y_test,y_pred)
accuracy

from sklearn.metrics import confusion_matrix
confusion=confusion_matrix(y_test,y_pred)
confusion

from sklearn.metrics import classification_report
classification_report1 = classification_report(y_test,y_pred)
print(classification_report1)

lr.predict([[1,80,1,90,1,1,90,1,0,85,1,85]])

*/
```

## Output:
TOP 5 ELEMENTS

<img width="1221" height="226" alt="image" src="https://github.com/user-attachments/assets/6d42b7e9-94e1-4571-baec-6e61db494180" />

<img width="1091" height="240" alt="image" src="https://github.com/user-attachments/assets/485ec001-d7ef-43e4-a3e5-0e25c31dddec" />

<img width="982" height="497" alt="image" src="https://github.com/user-attachments/assets/da55221c-d5a5-4006-8054-d73ba3dc3544" />

DATA DUPLICATE

<img width="61" height="48" alt="image" src="https://github.com/user-attachments/assets/b5f4e515-59df-496a-ad30-eb6cb0d641d9" />

PRINT DATA

<img width="982" height="502" alt="image" src="https://github.com/user-attachments/assets/dc0ef4fd-1bc0-48fd-8d8a-c9876d1e9bbe" />

DATA STATUS

<img width="922" height="510" alt="image" src="https://github.com/user-attachments/assets/8a3a791e-1d56-4956-9463-e134b2e4f4b6" />

Y_PREDDICTION ARRAY

<img width="586" height="263" alt="image" src="https://github.com/user-attachments/assets/2e600070-8bf4-4df9-b86a-193b24456922" />

CONFUSION ARRAY

<img width="762" height="71" alt="image" src="https://github.com/user-attachments/assets/667eae17-3e93-4104-a0f0-59dce057866a" />

ACCURACY VALUE

<img width="210" height="51" alt="image" src="https://github.com/user-attachments/assets/f5e8b1f5-c93f-482f-a7ba-c12c958095ce" />

CLASSIFICATION REPORT

<img width="582" height="176" alt="image" src="https://github.com/user-attachments/assets/e3576764-688f-4168-9a54-2b24b7fdfbad" />

PREDICTION 

<img width="303" height="33" alt="image" src="https://github.com/user-attachments/assets/95715da9-b338-4679-a579-ab5d43650880" />








## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
