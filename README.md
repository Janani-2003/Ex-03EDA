# Ex-03EDA

## AIM
To perform EDA on the given data set. 

# Explanation
The primary aim with exploratory analysis is to examine the data for distribution, outliers and 
anomalies to direct specific testing of your hypothesis.
 
# ALGORITHM
### STEP 1
Import the built libraries required to perform EDA and outlier removal

### STEP 2
Use seaborn the bar graph comparison of data can be viewed.

### STEP 3
Using crosstab the numerical data on the dataset can be compared and viewed

### STEP 4
The heatmap is used to represent the difference between the values

# CODE
```
import pandas pd
import numpy as np
import seaborn as sns
df=pd.read_csv("titanic_dataset.csv")
df.info()
df.head()
df.isnull().sum()
df.drop("Cabin",axis=1,inplace=True)
df.info()
df.isnull().sum()
df["Age"]=df["Age"].fillna(df["Age"].median())
df.boxplot()
df.isnull().sum()
df["Embarked"]=df["Embarked"].fillna(df["Embarked"].mode()[0])
df["Embarked"].value_counts()
df["Pclass"],value_counts()
df["Survived"].value_counts()
sns.countplot(x="Survived",data=df)
sns.countplot(x="Pclass",data=df)
sns.countplot(x="sex",data=df)
df.info()
sns.displot(df["Fare"])
sns.countplot(x="Pclass",hue="Survived",data=df)
sns.countplot(x="Sex",hue="Survived",data=df)
sns.displot(df[df["Survived"]==0]["Age"])
sns.displot(df[df["Survived"]==1]["Age"])
pd.crosstab(df["Pclass"],df["Survived"])
pd.crosstab(df["sex"],df["Survived"])
df.corr()
sns.heatmap(df.corr(),annot=True)
```
# OUTPUT
![output](./s.png)
![output](./s1.png)
![output](./s2.png)
![output](./s3.png)
![output](./s4.png)
![output](./s5.png)
![output](./s6.png)
![output](./s7.png)
![output](./s8.png)
![output](./s9.png)
![output](./s11.png)
![output](./s12.png)
![output](./s13.png)
![output](./s14.png)
![output](./s15.png)
![output](./s16.png)
