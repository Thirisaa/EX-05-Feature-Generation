# EX-05 Feature generation

## AIM

   To read the given data and perform Feature Generation process and save the data to a file. 

# ALGORITHM

### STEP 1

Read the given Data

### STEP 2

Clean the Data Set using Data Cleaning Process

### STEP 3

Apply Feature Generation techniques to all the feature of the data set

### STEP 4

Save the data to the file


# CODE

import pandas as pd

df=pd.read_csv('/content/Encoding Data.csv')

df.head()

df['ord_2'].unique()

from sklearn.preprocessing import LabelEncoder,OrdinalEncoder

climate = ['Cold','Warm','Hot']

en= OrdinalEncoder(categories = [climate])

df['ord_2']=en.fit_transform(df[["ord_2"]])

df

le = LabelEncoder()

df['Nom_0'] = le.fit_transform(df[["nom_0"]])

df

!pip install --upgrade category_encoders

from category_encoders import BinaryEncoder

be = BinaryEncoder()

data = be.fit_transform(df['bin_1'])

df  = pd.concat([df,data],axis=1)

df

be = BinaryEncoder()

data = be.fit_transform(df['bin_2'])

df  = pd.concat([df,data],axis=1)

df

df1 = pd.read_csv("/content/data.csv")

df1.head()

df1['Ord_1'].unique()

climate = ['Cold','Warm','Hot','Very Hot']

en= OrdinalEncoder(categories = [climate])

df1['Ord_1']=en.fit_transform(df1[["Ord_1"]])

df1

df1['Ord_2'].unique()

cl = ['High School','Diploma','Bachelors','Masters','PhD']

en= OrdinalEncoder(categories = [cl])

df1['Ord_2']=en.fit_transform(df1[["Ord_2"]])
df1

le = LabelEncoder()

df1['City'] = le.fit_transform(df1[["City"]])
df1

from category_encoders import BinaryEncoder

be = BinaryEncoder()

dat = be.fit_transform(df1['bin_1'])

df1  = pd.concat([df1,dat],axis=1)
df1

from category_encoders import BinaryEncoder

be = BinaryEncoder()

data1 = be.fit_transform(df1['bin_2'])

df1  = pd.concat([df1,data1],axis=1)
df1

df2 = pd.read_csv("/content/titanic_dataset.csv")

df2.head()

be = BinaryEncoder()

data2 = be.fit_transform(df2['Sex'])

df2  = pd.concat([df2,data2],axis=1)
df2

df2 = pd.get_dummies(df2, prefix=['Embarked'] ,columns=['Embarked'])
df2

# OUPUT
![op1](https://user-images.githubusercontent.com/112301582/232964244-940c0c3a-b20c-46c8-816a-0126d4ff1f0e.png)

![op2](https://user-images.githubusercontent.com/112301582/232964264-ed89748e-a09c-46cf-a73e-d92d6f1ab7a7.png)

![op3](https://user-images.githubusercontent.com/112301582/232964286-4b64d3ca-aeb1-4f67-9b88-111803757396.png)

![op4](https://user-images.githubusercontent.com/112301582/232964297-08c21030-e486-4f15-809f-32f922605823.png)
![op5](https://user-images.githubusercontent.com/112301582/232964302-feda8af7-78b9-4d3f-8b17-1e8269869d45.png)
![op6](https://user-images.githubusercontent.com/112301582/232964311-6f566fa4-82b3-4450-8458-8c1502de10c5.png)
![op7](https://user-images.githubusercontent.com/112301582/232964321-6bb7bdc4-3316-4e38-8144-7c5418c879ae.png)
![op8](https://user-images.githubusercontent.com/112301582/232964335-0b237d0d-5941-4742-bf67-c3b5114e5b03.png)
![op9](https://user-images.githubusercontent.com/112301582/232964346-faa42ad0-130f-460e-a968-d6f529717f68.png)
![op10](https://user-images.githubusercontent.com/112301582/232964361-e013ed18-a0b4-4917-bb9e-7e07348b3c1d.png)
![op111](https://user-images.githubusercontent.com/112301582/232964727-b19cb961-ed1f-4129-822c-d4c9405dcb20.png)
![op12](https://user-images.githubusercontent.com/112301582/232964479-fb1dbbfa-35dc-4c21-a4eb-46fafc70867f.png)
![op13](https://user-images.githubusercontent.com/112301582/232964507-cbe3ee82-f12f-49d7-bcc1-d92b1e165795.png)
![op14](https://user-images.githubusercontent.com/112301582/232964527-74011eae-4914-4287-8cfc-379cda363469.png)

# RESULT
Thus feature generation process was performed successfully on the given dataset 
