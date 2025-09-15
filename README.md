# EXNO2DS
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT
import pandas as pd
import numpy as np
import seaborn as sns
df=pd.read_csv('titanic_dataset.csv')
df
<img width="1412" height="632" alt="image" src="https://github.com/user-attachments/assets/5fb141f3-d65c-42c0-84fe-7c5f81cdf660" />
df.info()
<img width="1400" height="471" alt="image" src="https://github.com/user-attachments/assets/a525efc9-ac10-47c9-bcdd-0768e5ad1831" />
df.describe()
<img width="1392" height="357" alt="image" src="https://github.com/user-attachments/assets/10fe056c-955d-4b88-9794-f2128750ab6b" />
df.dtypes
<img width="1398" height="361" alt="image" src="https://github.com/user-attachments/assets/970ddd04-8983-480f-a4f9-d4dfc2362124" />
df.shape()
<img width="1406" height="88" alt="image" src="https://github.com/user-attachments/assets/bc82b14b-2aab-4b63-b86e-b617ad1cc2de" />
df.value_counts()
<img width="1398" height="628" alt="image" src="https://github.com/user-attachments/assets/f0ae0da5-8bbd-4e24-8a63-1dc577836d6e" />
df['Age'].value_counts()
<img width="1410" height="343" alt="image" src="https://github.com/user-attachments/assets/d4bf4dd2-d38d-4661-a6ef-f059d0101373" />
df.set_index('PassengerId')
<img width="1399" height="529" alt="image" src="https://github.com/user-attachments/assets/246957f7-b244-4a94-bd19-df61bcd1a9af" />
df
<img width="1411" height="500" alt="image" src="https://github.com/user-attachments/assets/c893a7b0-95c6-44b8-b721-2536274e335b" />
df.set_index('PassengerId',inplace=True)
df
<img width="1355" height="590" alt="image" src="https://github.com/user-attachments/assets/68f62c8e-53b9-450f-82c7-43f4ac39333f" />
df.nunique()
<img width="1404" height="338" alt="image" src="https://github.com/user-attachments/assets/d6d25626-d809-4385-afe0-b42e346c6193" />
sns.countplot(data=df,x='Age')
<img width="1399" height="647" alt="image" src="https://github.com/user-attachments/assets/75fac308-81a3-4096-b731-39b89e56daf0" />
df.rename(columns={'Gneder':'Gender'},inplace=True)
<img width="1413" height="577" alt="image" src="https://github.com/user-attachments/assets/0f879788-815a-49ad-8482-e71cc21a4e23" />
sns.catplot(x='Gender',col='Survived',kind='count',data=df)
<img width="1255" height="635" alt="image" src="https://github.com/user-attachments/assets/7cbf148a-a3ab-4b7a-b5b4-67d373a06b0d" />
df.boxplot(column='Age',by='Survived')
<img width="1255" height="610" alt="image" src="https://github.com/user-attachments/assets/e24ac672-d0c9-48f2-a63d-84c6dfd5feac" />
sns.scatterplot(x=df['Age'],y=df['Fare'])
<img width="1391" height="644" alt="image" src="https://github.com/user-attachments/assets/178c0d74-bb9d-4cf6-8706-f03bdb91e07d" />
plt=sns.boxplot(x='Pclass',y='Age',hue='Gender',data=df)
<img width="1397" height="611" alt="image" src="https://github.com/user-attachments/assets/f54c494f-7d7b-4300-9060-67f3fd17b1e6" />
sns.catplot(x='Pclass',y='Age',hue='Gender',col='Survived',kind='box',data=df)
<img width="1398" height="647" alt="image" src="https://github.com/user-attachments/assets/ebe6f789-7af2-4937-9f10-02520d2fd187" />
corr=df.corr(numeric_only=True)
sns.heatmap(corr,annot=True)
<img width="1391" height="654" alt="image" src="https://github.com/user-attachments/assets/00018065-1362-4e5d-a023-d6dbefe7cf4d" />
sns.heatmap(corr)
<img width="1383" height="612" alt="image" src="https://github.com/user-attachments/assets/5d824017-ed43-437b-ae3f-a1dc78f33674" />

# RESULT
        <<INCLUDE YOUR RESULT HERE>>
