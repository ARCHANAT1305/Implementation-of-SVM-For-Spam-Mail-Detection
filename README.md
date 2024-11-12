# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm  
1. Import pandas.  
2. Define CSV file path.  
3. Read CSV into DataFrame, specifying detected encoding.  
4. Display first few DataFrame rows and information.  
5. Check for missing values in the DataFrame.
6. Split data into training and testing sets, train SVC model, predict labels, and calculate accuracy score.

## Program:
```

Program to implement the SVM For Spam Mail Detection..
Developed by: ARCHANA T
RegisterNumber: 212223240013

import pandas as pd
data=pd.read_csv("spam.csv",encoding='latin-1')
data.head()
data.info()
data.isnull().sum()
x=data["v1"].values
y=data["v2"].values
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
from sklearn.feature_extractiaon.text import CountVectorizer
cv=CountVectorizer()
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)
from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy


```

## Output:

![image](https://github.com/user-attachments/assets/3a3566cd-8b00-4b5a-9082-331df112f087)
![image](https://github.com/user-attachments/assets/a433c85a-0d7f-4a66-9127-bfe7ca19944c)
![image](https://github.com/user-attachments/assets/a2f9cb40-dd5b-450a-a34b-492abefeb60d)
![image](https://github.com/user-attachments/assets/18bab365-6131-4bcc-a10b-ef2d6b64319f)
![image](https://github.com/user-attachments/assets/cf7310d1-3071-48aa-9914-6a05112f216d)


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
