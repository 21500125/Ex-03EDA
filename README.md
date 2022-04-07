# Ex-03EDA

## AIM
To perform EDA on the given data set. 

# Explanation
The primary aim with exploratory analysis is to examine the data for distribution, outliers and 
anomalies to direct specific testing of your hypothesis.
 

# ALGORITHM
### STEP 1: Create a new file in jupyter notebook.
### STEP 2: Upload the given csv file.
### STEP 3: Write codes for Data Analysis (EDA).
### STEP 4: Plot the result in various formats.
### STEP 5: End the program.

# CODE
import pandas as pd
import numpy as np
import seaborn as sns
df=pd.read_csv("titanic_dataset.csv")
df.info()
df.head()
df.isnull().sum()
df["Age"]=df["Age"].fillna(df["Age"].median())
df.boxplot()
df.isnull()
df["Embarked"]=df["Embarked"].fillna(df["Embarked"].mode()[0])
df["Embarked"].value_counts()
df["Pclass"].value_counts()
df["Survived"].value_counts()
sns.countplot(x="Survived",data=df)
sns.countplot(x="Pclass",data=df)
df.info()
sns.displot(df["Fare"])
sns.countplot(x="Pclass",hue="Survived",data=df)
sns.countplot(x="Sex",hue="Survived",data=df)
sns.displot(df[df["Survived"]==0]["Age"])
sns.displot(df[df["Survived"]==1]["Age"])
pd.crosstab(df["Pclass"],df["Survived"])
pd.crosstab(df["Sex"],df["Survived"])
df.corr()
sns.heatmap(df.corr(),annot=True)
# OUPUT
![h1](https://user-images.githubusercontent.com/94219582/162116231-439fc740-3b1d-491d-8566-c14252f889c9.PNG)
![h2](https://user-images.githubusercontent.com/94219582/162116251-471692d0-140f-4811-8c1a-7474557f441f.PNG)
![h3](https://user-images.githubusercontent.com/94219582/162116265-fa4a7e54-e147-49d3-b51e-e0fbdc24c293.PNG)
![h4](https://user-images.githubusercontent.com/94219582/162116277-657e465e-df92-438f-b6e9-415989e0933e.PNG)
![h5](https://user-images.githubusercontent.com/94219582/162116301-9e761460-b6be-40be-8781-0eb4fe375b43.PNG)
![h6](https://user-images.githubusercontent.com/94219582/162116316-8ca261c1-8d27-46d3-a5d1-7a88b776a532.PNG)
![h7](https://user-images.githubusercontent.com/94219582/162116329-bb4eb758-9076-468b-8f8b-419ed377f2e7.PNG)
![h8](https://user-images.githubusercontent.com/94219582/162116351-910b0c88-2aee-499f-8a2e-db3b8dbbf3d9.PNG)
![h9](https://user-images.githubusercontent.com/94219582/162116363-b2f4d246-2b54-4e29-8014-8f5693059e91.PNG)
![h10](https://user-images.githubusercontent.com/94219582/162116382-8f0ff806-6464-4493-85de-e35dfefd9d8b.PNG)
![h11](https://user-images.githubusercontent.com/94219582/162116398-9382517f-44df-44ed-9bc9-fb3860155985.PNG)
# RESULT
Thus the data of the dataset is analyzed using Exploratory data analysis


