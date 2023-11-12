# Ex-01_DS_Data_Cleansing


## AIM
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

# CODE and OUTPUT
## CODE:
```
### Developed by: Sabitha P
### Register number:212222040137
```
```python
import pandas as pd
df=pd.read_csv("/content/Loan_data.csv")
df

df.head()

df.tail()

df.shape

df.describe()

df.info()

df.isnull().sum()

df.dropna(how="any").shape

df.dropna(how="any")

df.dropna(how="all").shape

x=df.dropna(how="all")
x

amt=df.dropna(subset=['LoanAmount'],how='any')
amt

M=df.dropna(subset=['LoanAmount','Loan_Amount_Term'],how='any')
M

df.fillna(0)

df

df.fillna(method='ffill')

df.fillna(method="bfill")

df.interpolate()

mn=df.LoanAmount.mean()
mn

l=df.LoanAmount.interpolate()
l

df.LoanAmount.fillna(mn,inplace=True)
df

df.isnull()

df.notnull()

df.dropna()

df.duplicated()

df.drop_duplicates(inplace=True)
df

md=df.LoanAmount.median()
md

mode=df.LoanAmount.mode()
mode

for x in df.index:
  if df.loc[x,'LoanAmount']>100:
    df.drop(x,inplace=True)
df


```
## OUTPUT:
![image](https://github.com/sabithapaulraj/ODD2023-Datascience-Ex01/assets/118343379/4d788dd7-d9be-4951-a240-92815492a1f0)
![image](https://github.com/sabithapaulraj/ODD2023-Datascience-Ex01/assets/118343379/33f16af2-298e-4e52-ada8-b4e65f565d04)
![image](https://github.com/sabithapaulraj/ODD2023-Datascience-Ex01/assets/118343379/0c49d2c1-cd23-4c9f-b9f1-426225fc55f2)
![image](https://github.com/sabithapaulraj/ODD2023-Datascience-Ex01/assets/118343379/f3ae3e09-664c-44f9-8259-24edd0e4bdd4)
![image](https://github.com/sabithapaulraj/ODD2023-Datascience-Ex01/assets/118343379/9fe4cd26-9dc5-4cbb-827d-52272edbe82f)
![image](https://github.com/sabithapaulraj/ODD2023-Datascience-Ex01/assets/118343379/bbc12b85-17d0-4a2f-9541-99c8a620f341)
![image](https://github.com/sabithapaulraj/ODD2023-Datascience-Ex01/assets/118343379/f97746d7-d9ff-4a97-9f53-41af8f99aee4)
![image](https://github.com/sabithapaulraj/ODD2023-Datascience-Ex01/assets/118343379/a7ae3db8-7830-426c-8745-b49947db78fe)
![image](https://github.com/sabithapaulraj/ODD2023-Datascience-Ex01/assets/118343379/d8d1d414-b1f5-4470-9a66-13f50db9803f)
![image](https://github.com/sabithapaulraj/ODD2023-Datascience-Ex01/assets/118343379/a97a7364-12e7-494e-b910-be51e2da515a)
![image](https://github.com/sabithapaulraj/ODD2023-Datascience-Ex01/assets/118343379/e8ada439-7e02-432e-8177-bac12c365375)
![image](https://github.com/sabithapaulraj/ODD2023-Datascience-Ex01/assets/118343379/9012dd55-b885-4e9d-9fcd-b882df0ef571)
![image](https://github.com/sabithapaulraj/ODD2023-Datascience-Ex01/assets/118343379/dd5179cb-c599-4556-9575-3c04dcfcfa90)
![image](https://github.com/sabithapaulraj/ODD2023-Datascience-Ex01/assets/118343379/2e8f52a0-bfc6-4243-b934-d20625ef16cd)
![image](https://github.com/sabithapaulraj/ODD2023-Datascience-Ex01/assets/118343379/cfbb30b5-eccc-4205-b735-74e9f32d6fbe)
![image](https://github.com/sabithapaulraj/ODD2023-Datascience-Ex01/assets/118343379/4c8d5953-5a4c-4895-a9c8-d232b7316c21)
![image](https://github.com/sabithapaulraj/ODD2023-Datascience-Ex01/assets/118343379/089eafe4-313c-47a4-b1fe-579cb830b7ec)
![image](https://github.com/sabithapaulraj/ODD2023-Datascience-Ex01/assets/118343379/a418b454-be6e-4055-a901-1a466468a8a7)
![image](https://github.com/sabithapaulraj/ODD2023-Datascience-Ex01/assets/118343379/c0bdcd66-cf1f-4552-89e6-d98646df7b87)
![image](https://github.com/sabithapaulraj/ODD2023-Datascience-Ex01/assets/118343379/5b3f35d0-329c-44b9-b254-4e5ac790b8fc)
![image](https://github.com/sabithapaulraj/ODD2023-Datascience-Ex01/assets/118343379/743d29b4-c46f-4f9e-8461-7b02034c1c97)
![image](https://github.com/sabithapaulraj/ODD2023-Datascience-Ex01/assets/118343379/d4039a77-ed80-4281-8bf7-0f8860c770a3)
![image](https://github.com/sabithapaulraj/ODD2023-Datascience-Ex01/assets/118343379/e553eb78-35cb-49fa-a192-b5a67fa967b7)


## RESULT:
Thus data cleaning is performed on the given dataset.


