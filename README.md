<H3>NAME: SNEHA BASYAL M</H3>
<H3>REGISTER NO: 212222240101</H3>
<H3>EX.NO.1</H3>
<H3>DATE:</H3>
<H1 ALIGN =CENTER> Introduction to Kaggle and Data preprocessing</H1>

## AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

## EQUIPMENTS REQUIRED:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

**Kaggle :**
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

**Data Preprocessing:**

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

**Need of Data Preprocessing :**

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:
STEP 1:Importing the libraries<BR>
STEP 2:Importing the dataset<BR>
STEP 3:Taking care of missing data<BR>
STEP 4:Encoding categorical data<BR>
STEP 5:Normalizing the data<BR>
STEP 6:Splitting the data into test and train<BR>
</br>

##  PROGRAM:
```
#import libraries
from google.colab import files
import pandas as pd
import io
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split

#Read the dataset from drive
df=pd.read_csv("/content/Churn_Modelling.csv")
df

df.isnull().sum()

#check for duplication
df.duplicated()

print(df['CreditScore'].describe())

df.info()

df.drop(['Surname','Geography','Gender'],axis=1,inplace=True)
df

Scaler=MinMaxScaler()
df1=pd.DataFrame(Scaler.fit_transform(df))
df1

X = df1.iloc[:, :-1].values
print(X)

y = df1.iloc[:,-1].values
print(y)

X_train,X_test,y_train,y_test=train_test_split(X,y,test_size=0.2,random_state=25)

print(X_train)
print(len(X_train))

print(X_test)
print(len(X_test))
```
</br>

## OUTPUT:

### Reading The Dataset
![EX-1-NN](nn1.png)
</br>

### Finding Missing values
![EX-1-NN](nn2.png)
</br>

### Checking Duplicates
![EX-1-NN](nn3.png)
</br>

### Describing a column
![EX-1-NN](nn4.png)
</br>

### Info
![EX-1-NN](nn5.png)
</br>

### Dropping columns
![EX-1-NN](nn6.png)
</br>

### Normalizing the data
![EX-1-NN](nn7.png)
</br>

### Values of X
![EX-1-NN](nn8.png)
</br>

### Values of Y
![EX-1-NN](nn9.png)
</br>

### X_train
![EX-1-NN](nn10.png)
</br>

### X_test
![EX-1-NN](nn11.png)
</br>

## RESULT:
Thus, Implementation of Data Preprocessing is done in python using a data set downloaded from Kaggle.


