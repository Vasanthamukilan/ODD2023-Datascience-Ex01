# Ex-01_DS_Data_Cleansing
## AIM:
To read the given data and perform data cleaning and save the cleaned data to a file. 

## Explanation:
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

## ALGORITHM:
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file
## Code:
### LOAN_DATA.CSV
```python
import pandas as pd
df=pd.read_csv("Loan_data.csv")
print(df)
df.head(10)
df.info()
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
```
### DATA_SET.CSV
```python
import pandas as pd
df=pd.read_csv("Data_set.csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()

df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()

df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()

df.info()
df.isnull()
df.isnull().sum()
```
## Output:
### FOR LOAN_DATA:
### Data
```python
import pandas as pd
df=pd.read_csv("Loan_data.csv")
print(df)
df.head(10)
```
![1 1](https://github.com/Vasanthamukilan/ODD2023-Datascience-Ex01/assets/119559694/eadc1ed1-8c22-4367-a50d-cb7bbb11fa8e)
### NON NULL BEFORE
```python
df.info()
```
![1 2](https://github.com/Vasanthamukilan/ODD2023-Datascience-Ex01/assets/119559694/80db8bfd-390c-4ec5-b436-620a002a5624)
### MODE
```python
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()
```
![1 3](https://github.com/Vasanthamukilan/ODD2023-Datascience-Ex01/assets/119559694/aa8602a7-a4be-47ed-8c29-1d019ea4a49c)

### MEAN
```python
df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()
```
![1 4](https://github.com/Vasanthamukilan/ODD2023-Datascience-Ex01/assets/119559694/c4990fdb-e71f-4bd6-8cd5-5fc6bf0fa668)

### MEDIAN
```python
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()
```
![1 5](https://github.com/Vasanthamukilan/ODD2023-Datascience-Ex01/assets/119559694/3fd1e15c-6d85-4b5d-a41e-7101f3589367)

### NON NULL AFTER
```python
df.info()
```
![1 6](https://github.com/Vasanthamukilan/ODD2023-Datascience-Ex01/assets/119559694/4273f8e3-da35-4afe-bee6-22fe752af874)

```python
df.isnull().sum()
```
![1 7](https://github.com/Vasanthamukilan/ODD2023-Datascience-Ex01/assets/119559694/857b4bf2-0475-4147-9b1c-0ae02e56ccbe)

## FOR DATA_SET
### DATA
```python
import pandas as pd
df=pd.read_csv("Data_set.csv")
print(df)
df.head(10)
```
![2 1](https://github.com/Vasanthamukilan/ODD2023-Datascience-Ex01/assets/119559694/1b10fed1-4474-401a-92f0-47203823f938)

### NON NULL BEFORE
```python
df.info()
```
![2 2](https://github.com/Vasanthamukilan/ODD2023-Datascience-Ex01/assets/119559694/f32f670e-0166-4806-8a5c-2c6854b0a108)

```python
df.isnull()
```
![2 3](https://github.com/Vasanthamukilan/ODD2023-Datascience-Ex01/assets/119559694/ca58253c-e7a2-426f-a3a2-9407742a38b9)

```python
df.isnull().sum()
```
![2 4](https://github.com/Vasanthamukilan/ODD2023-Datascience-Ex01/assets/119559694/53e73a76-04ca-4a76-ab9d-d827e280fc02)

### MODE
```python
df['show_name']=df['show_name'].fillna(df['aidf['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()red_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
```
![2 5](https://github.com/Vasanthamukilan/ODD2023-Datascience-Ex01/assets/119559694/bd18f09a-bf65-4014-a684-bca12a5f5296)

### MEAN
```python
df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
```
![2 6](https://github.com/Vasanthamukilan/ODD2023-Datascience-Ex01/assets/119559694/411e0cd7-7fb7-4ede-be7d-662a15cbf8ee)

### MEDIAN
```python
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()
```
![2 7](https://github.com/Vasanthamukilan/ODD2023-Datascience-Ex01/assets/119559694/918c76e1-d3c9-42dc-8004-3697e6a01262)

### NON NULL AFTER
```python
df.info()
```
![2 8](https://github.com/Vasanthamukilan/ODD2023-Datascience-Ex01/assets/119559694/8ec224a0-e7fc-41bd-a738-85460d0a4049)

```python
df.isnull()
```
![2 9](https://github.com/Vasanthamukilan/ODD2023-Datascience-Ex01/assets/119559694/823f7018-bc7a-47cc-9f91-fa80ef9aafad)

```python
df.isnull().sum()
```
![2 10](https://github.com/Vasanthamukilan/ODD2023-Datascience-Ex01/assets/119559694/c735e201-1745-41c4-ac3c-1633a9ba028a)

## RESULT
Thus,the given data is read,cleansed and the cleaned data is saved into the file.
