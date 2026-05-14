#EX.NO:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output
     import pandas as pd
     df=pd.read_csv('D:Data_set (1).csv')
     print(df)
     print(data)     
     df.describe()
     df=pd.DataFrame(df)
     print(df.isnull())
     import pandas as pd
     data = pd.read_csv("C:/Users/acer/Downloads/Data_set (1).csv")
     df = pd.DataFrame(data)
    dfd = df.dropna()
    print("AFTER DROPNA")
    print(dfd)

            
# Result
          <<include your Result here>>
