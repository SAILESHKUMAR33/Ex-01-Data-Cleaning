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
import pandas as pd
df=pd.read_csv("/content/Loan_data.csv")
print(df)

df.head(5)

df.tail(5)

df.describe()

df.info()

df.isnull().sum()

df=df[~df.duplicated()]
print(df)

df['Gender'].fillna(value=df['Gender'].mode())

df['LoanAmount'].fillna(value=df['LoanAmount'].median())
# OUPUT

![226175971-feb08341-5c1e-45a2-8d57-66bc1bce8981](https://user-images.githubusercontent.com/113497410/228141861-b491420f-61d3-4e20-8a67-ebd5b3e3b275.png)
![226176000-ea5c964c-6c16-4bbd-8839-67d57d618635](https://user-images.githubusercontent.com/113497410/228141865-541cd7da-7768-4e04-a1b3-0fa1bcad8413.png)
![226176067-66d59b15-bc04-4ee4-95ef-d8d44dfef950](https://user-images.githubusercontent.com/113497410/228141863-ccd81b1c-7b38-4076-b0dd-07157648caef.png)
![226176220-22300b8c-27b7-49d5-9cf6-91ee68472052](https://user-images.githubusercontent.com/113497410/228141864-06c146f9-763d-44de-9361-928add902e82.png)
![Data](https://user-images.githubusercontent.com/113497410/228141862-368cdd8d-285b-43a0-8327-18b8185c7faa.png)
