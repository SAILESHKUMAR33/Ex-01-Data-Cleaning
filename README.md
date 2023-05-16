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

Name :Saileshkumar A

Register Number : 212222230126

import pandas as pd

df=pd.read_csv("/content/Loan_data (1).csv")

print(df)

df.head(10)

df.info()

df.isnull()

df.isnull().sum()

df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])

df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])

df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])

df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])

df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])

df.head()

df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())

df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())

df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())

df.head()

df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())

df.head()

df.info()

df.isnull().sum()

# OUPUT

![image](https://github.com/SAILESHKUMAR33/Ex-01-Data-Cleaning/assets/113497410/15964a90-8a74-45f6-ab3f-7135f21a9738)

# df.info:

![image](https://github.com/SAILESHKUMAR33/Ex-01-Data-Cleaning/assets/113497410/04b4870e-1250-4e12-aff0-92467bbdfd22)

# MODE:

![image](https://github.com/SAILESHKUMAR33/Ex-01-Data-Cleaning/assets/113497410/2485f187-80aa-4b82-9dd0-517e5570a542)


# MEAN:

![image](https://github.com/SAILESHKUMAR33/Ex-01-Data-Cleaning/assets/113497410/11a7600b-519f-47c7-a2a3-0a5951e3b225)

# MEDIAN:

![image](https://github.com/SAILESHKUMAR33/Ex-01-Data-Cleaning/assets/113497410/6b3ea824-d6f4-4528-a22d-5f8b9f9058d4)


# df.info:

![image](https://github.com/SAILESHKUMAR33/Ex-01-Data-Cleaning/assets/113497410/fe83fc6c-ac1f-46ec-bcaa-0607e46243bc)

# df.isnull().sum():


![image](https://github.com/SAILESHKUMAR33/Ex-01-Data-Cleaning/assets/113497410/6fe17083-fdcf-47e6-a9a6-b318dea8e59d)


# RESULT:

Thus,the given data is read,cleansed and the cleaned data is saved into the file.

