# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
Step 1: Start the program.

Step 2: Import the required packages.

Step 3: Import the dataset to operate on.

Step 4: Split the dataset.

Step 5: Predict the required output.

Step 6: End the program.
## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: Priyadharshini E
RegisterNumber: 212223230159

import chardet
file='spam.csv'
with open(file,'rb') as rawdata:
    result=chardet.detect(rawdata.read(100000))
result

import pandas as pd
data=pd.read_csv('spam.csv',encoding='Windows-1252')
data.head()
data.isnull().sum()
data.info()
x=data["v2"].values
y=data["v1"].values
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)
x_train
x_test
from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
cm=metrics.confusion_matrix(y_test,y_pred)
cm
cf=metrics.classification_report(y_test,y_pred)
cf

```

## Output:
<img width="715" height="214" alt="image" src="https://github.com/user-attachments/assets/3c13518d-d529-48b7-81f9-f02ccc49ba8a" />

data.head:

<img width="704" height="316" alt="image" src="https://github.com/user-attachments/assets/de8de3d5-5c0c-4695-850d-a3151494c370" />

data.isnull:

<img width="721" height="206" alt="image" src="https://github.com/user-attachments/assets/bfb32ec2-ca78-46ca-bc34-779f4d207a54" />



<img width="717" height="296" alt="image" src="https://github.com/user-attachments/assets/bb7090ff-4121-4818-8255-e85c670754c0" />



Accuracy Score:

<img width="732" height="196" alt="image" src="https://github.com/user-attachments/assets/e9e6a2c2-cb2b-4ba7-a393-583277c3a1c0" />

Confusion matric :

<img width="722" height="449" alt="image" src="https://github.com/user-attachments/assets/e7b7830d-649c-4e59-8658-c27d03c93892" />


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
