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

df=pd.read_csv("/content/Data_set.csv")

print(df)

df.head(5)

df.info()

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

df.isnull().sum()

# OUPUT
![image](https://user-images.githubusercontent.com/121303741/228143951-f0c42ff6-3b43-4636-971a-47dad9865c9f.png)


![image](https://user-images.githubusercontent.com/121303741/228144282-84e2d116-0804-4233-8328-6bb1d3e66d74.png)


![image](https://user-images.githubusercontent.com/121303741/228144260-cc386d8b-142a-4204-8e84-d910731fd16a.png)


![image](https://user-images.githubusercontent.com/121303741/228144321-622f11f3-a007-4281-86ea-cb227e14e16d.png)


![image](https://user-images.githubusercontent.com/121303741/228144354-24586f56-cb7c-49b0-a3d7-510a76027810.png)


![image](https://user-images.githubusercontent.com/121303741/228144388-05cefdb3-2180-4ed9-a812-aa941440c308.png)


![image](https://user-images.githubusercontent.com/121303741/228144404-2a349635-b386-4740-b661-fbec853b7f8f.png)


![image](https://user-images.githubusercontent.com/121303741/228144435-ec9cd634-8112-452f-a345-670bddf5efe6.png)


##Result
Hence the given data is read and perform data cleaning and save the cleaned data to a file.




