# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import necessary libraries
2.Check the dataset for missing values and make necessary changes.
3.Split the dataset for Training and Testing purpose.
4.Implement SVM for the splitted datasets.

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: PRATHIKSHA R
RegisterNumber:  212224040244
import chardet 
file = "spam.csv"
with open(file,'rb') as rawdata:
    result = chardet.detect(rawdata.read(100000))
result
import pandas as pd

data = pd.read_csv("spam.csv",encoding = 'windows-1252')
data.head()
data.info()
data.isnull().sum()

x = data['v1'].values
y = data['v2'].values

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.feature_extraction.text import CountVectorizer
cv = CountVectorizer()
x_train = cv.fit_transform(x_train)
x_test = cv.transform(x_test)

from sklearn.svm import SVC
svc = SVC(kernel = 'linear')
svc.fit(x_train,y_train)
y_pred = svc.predict(x_test)
y_pred

from sklearn import metrics
accuracy = metrics.accuracy_score(y_pred,y_test)
accuracy
*/
```

## Output:
![image](https://github.com/user-attachments/assets/f6fa2707-ee8e-41e4-9647-16b69589fa57)
![image](https://github.com/user-attachments/assets/06ccd565-2cf9-49d7-a369-e0d94e0ce211)
![image](https://github.com/user-attachments/assets/733462e7-0b68-4a22-9cfe-010e222f8868)
![image](https://github.com/user-attachments/assets/24f9ef3f-92d0-4a21-a8ac-010c714c8d1b)
![image](https://github.com/user-attachments/assets/4d87707d-b1cd-4e24-beed-58441fb5d60f)


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
