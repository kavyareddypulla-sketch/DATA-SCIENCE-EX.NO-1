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
```
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

     dfd = df.dropna(axis=1)
     print("AFTER DROPNA")
     print(dfd)

     dfd=df.dropna(axis=1,inplace=True)

     print("AFTER DROPNA") dfd=df.dropna(axis=0)
     print("AFTER DROPNA")
     print(dfd)

     import pandas as pd
     # Read the dataset
     data = pd.read_csv("C:/Users/acer/Downloads/Data_set (1).csv")
     # Convert into DataFrame
     df = pd.DataFrame(data)
     # Fill missing values using forward fill method
     dfd = df.fillna(method="ffill")
     # Display output
     print("AFTER FILLNA")
     print(dfd)

     import pandas as pd
     import matplotlib.pyplot as plt
     import numpy as np
     data = pd.read_csv("C:/Users/acer/Downloads/iris.csv")
      df = pd.DataFrame(data)
     print(df)
     x = df["petal_length"]
     y = df["sepal_length"]
     plt.hist(x)
    plt.show()
    plt.hist(y)
    plt.show()

    import pandas as pd
    import matplotlib.pyplot as plt
    import numpy as np
    data = pd.read_csv("iris.csv")
    df = pd.DataFrame(data)
    print(df)
    x = df["petal_length"]
    y = df["sepal_length"]
    plt.xlabel('X-axis')
    plt.ylabel('Y-axis')
    plt.plot(x, y)
    plt.show()

    import pandas as pd
    import matplotlib.pyplot as plt
    import numpy as np
    # Read dataset
    data = pd.read_csv("iris.csv")
     # Convert into DataFrame
    df = pd.DataFrame(data)
    # Display dataset
     print(df)
     # Create boxplot
     dff = plt.boxplot(df["petal_width"])
     # Display graph
     plt.show()
     print(dff)

     \import pandas as pd
     import numpy as np
     from scipy import stats
    data = pd.read_csv("iris.csv")
    df = pd.DataFrame(data)
    z_scores = np.abs(stats.zscore(df.select_dtypes(include=[np.number])))
    df_cleaned = df[(z_scores < 3).all(axis=1)]
    print(df_cleaned)

    import pandas as pd
    import numpy as np
    data = pd.read_csv("C:/Users/acer/Downloads/iris (1).csv")
    df = pd.DataFrame(data)
    Q1 = df["sepal_width"].quantile(0.25)
    Q3 = df["sepal_width"].quantile(0.75)
    IQR = Q3 - Q1
    lower_bound = Q1 - 1.5 * IQR
    upper_bound = Q3 + 1.5 * IQR
    print("The Original DataSet")
    print(df)
    outliers = df[
    (df['sepal_width'] < lower_bound) |
    (df['sepal_width'] > upper_bound)
    ]
    print("The Outliers")
    print(outliers)
    df_clean = df[
    (df['sepal_width'] >= lower_bound) &
    (df['sepal_width'] <= upper_bound)
    ]
    print("The Dataset after removing the outliers")
    print(df_clean)
    ```
     


            
# Result
THUS DATA CLEANING IS PERFORMED
