# Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE
```
Developed by yugendhar
Register number:212220040184
```
```python
## Data_set Code:
import pandas as pd
df = pd.read_csv("Data_set.csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['show_name'] = df['show_name'].fillna(df['aired_on'].mode()[0]) 
df['aired_on'] = df ['aired_on'].fillna(df ['aired_on'].mode()[0]) 
df[ 'original_network' ] = df['original_network'].fillna(df['aired_on'].mode()[0]) 
df.head()
df ['rating'] = df['rating'].fillna(df['rating'].mean())
df['current_overall_rank'] = df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
df[ 'watchers']=df["watchers"].fillna (df['watchers'].median()) 
df.head()
df.info()
df.isnull().sum()
```
```python
## Loan_data Code:
import pandas as pd
df=pd.read_csv("Loan_data.csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df.head()
df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df.head()
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()
df.info()
df.isnull().sum()
```

# OUTPUT
## DATA - 1 :

![1](https://user-images.githubusercontent.com/129398164/229765188-a03fc70f-4c38-4e19-a8b9-1fad40d2cc6f.png)

## NON NULL BEFORE :
![2](https://user-images.githubusercontent.com/129398164/229765187-61abc2e5-d770-4298-ac2f-a81d96c33ff3.png)

## MODE :
![3](https://user-images.githubusercontent.com/129398164/229765221-44a0c666-b356-44c6-b614-767968841bd9.png)


## MEAN :
![4](https://user-images.githubusercontent.com/129398164/229765227-b6b3ecd8-e1be-4ea0-b6a9-79f62789672b.png)


## MEDIAN :
![5](https://user-images.githubusercontent.com/129398164/229765238-7080bc28-d56e-442e-84dc-a811bb4706de.png)


## NON NULL AFTER:
![6](https://user-images.githubusercontent.com/129398164/229765242-0c539e25-f153-4e6d-8b61-96d122909623.png)


## DATA - 2 :

![7](https://user-images.githubusercontent.com/129398164/229765251-85bf9679-7877-4b7a-969e-b84844dc76f5.png)

## NON NULL BEFORE :

![8](https://user-images.githubusercontent.com/129398164/229765292-bbfdb1a4-ed21-48e3-8d4b-d0e7554d98ac.png)
## MODE :
![9](https://user-images.githubusercontent.com/129398164/229765282-c0b2de4e-daa8-4999-be6d-3d802c9b2397.png)

## MEAN :
![11](https://user-images.githubusercontent.com/129398164/229765789-4c0cf596-76eb-47da-836d-31a97132fb4f.png)

## MEDIAN :

![12](https://user-images.githubusercontent.com/129398164/229765802-50b11920-f6ed-4667-81ad-cf62fc1ed65f.png)


## NON NULL AFTER :


![10](https://user-images.githubusercontent.com/129398164/229765272-31d7e43b-5a44-443f-901e-9215dede1712.png)

# RESULT
Thus the given data is readed and data cleaning is performed on it and the cleaned data is saved into the file.
