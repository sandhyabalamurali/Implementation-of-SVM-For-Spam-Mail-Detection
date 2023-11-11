# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required libraries .


2.Read the data frame using pandas.


3.Get the information regarding the null values present in the dataframe.


4.Apply label encoder to the non-numerical column inoreder to convert into numerical values.


5.Determine training and test data set.


6.Apply SVM for spam mail detection

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: SANDHYA B N
RegisterNumber:  212222040144

import chardet 
file='spam.csv'
with open(file, 'rb') as rawdata: 
    result = chardet.detect(rawdata.read(100000))
result
import pandas as pd
data = pd.read_csv("spam.csv",encoding="Windows-1252")
data.head()
data.info()
data.isnull().sum()

X = data["v1"].values
Y = data["v2"].values
from sklearn.model_selection import train_test_split
X_train,X_test,Y_train,Y_test = train_test_split(X,Y,test_size=0.2, random_state=0)

from sklearn.feature_extraction.text import CountVectorizer
cv = CountVectorizer()
X_train = cv.fit_transform(X_train)
X_test = cv.transform(X_test)

from sklearn.svm import SVC
svc=SVC()
svc.fit(X_train,Y_train)
Y_pred = svc.predict(X_test)
print("Y_prediction Value: ",Y_pred)

from sklearn import metrics
accuracy=metrics.accuracy_score(Y_test,Y_pred)
accuracy
*/
```

## Output:

![9 1](https://github.com/sandhyabalamurali/Implementation-of-SVM-For-Spam-Mail-Detection/assets/115525118/9df43e88-560a-4911-8648-76685475ed7a)

## data.head():

![9 2](https://github.com/sandhyabalamurali/Implementation-of-SVM-For-Spam-Mail-Detection/assets/115525118/b14e0f54-5cc5-431f-857f-047b273f0db5)


## data.info()

![9 3](https://github.com/sandhyabalamurali/Implementation-of-SVM-For-Spam-Mail-Detection/assets/115525118/3c4a70b6-4bbe-483d-90c4-66b3bf1ba04a)

## data.isnull().sum():


![9 4](https://github.com/sandhyabalamurali/Implementation-of-SVM-For-Spam-Mail-Detection/assets/115525118/2be6a751-f09e-4bff-8545-1ae829edece5)



![9 4 1](https://github.com/sandhyabalamurali/Implementation-of-SVM-For-Spam-Mail-Detection/assets/115525118/f60830ad-b87d-4696-a779-1e20f4f982bd)

## Y_prediction Value:


![9 5](https://github.com/sandhyabalamurali/Implementation-of-SVM-For-Spam-Mail-Detection/assets/115525118/2bbbbde8-b060-4b13-bc68-06ea3b9f5a20)


## Accuracy Value:


![9 6](https://github.com/sandhyabalamurali/Implementation-of-SVM-For-Spam-Mail-Detection/assets/115525118/745ca0be-8036-4085-8dd3-2ce4b15a44d0)


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
