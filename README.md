# Ex03-Univariate-Analysis
# Aim:

To read the given data and perform the univariate analysis with different types of plots.

# Explanation:

Univariate analysis is basically the simplest form to analyze data. Uni means one and this means that the data has only one kind of variable. The major reason for univariate analysis is to use the data to describe. The analysis will take data, summarise it, and then find some pattern in the data.

# Algorithm:

# Step1:

Read the given data.

# Step2:

Get the information about the data.

# Step3:

Remove the null values from the data.

# Step4:

Mention the datatypes from the data.

# Step5:

Count the values from the data.

# Step6:

Do plots like boxplots,countplot,distribution plot,histogram plot.

# Program:
Reg no:212222230030

Name:D.Dhanumalya
```
## SuperStore Data

import pandas as pd
import numpy as np
import seaborn as sns
df=pd.read_csv('SuperStore.csv')
df

df.head()

df.info()

df.describe()

df.isnull().sum()

df.dtypes

df['Customer Name'].value_counts()

sns.boxplot(x='Sales', data=df)

sns.countplot(x='State',data=df)

sns.distplot(df["Row ID"])

sns.histplot(x='State',data=df)

import matplotlib.pyplot as plt
df_count = df.groupby(by=["Category"]).count()
df_sum = df.groupby(by=["Category"]).sum()
labels=[]
for i in df_count.index:
     labels.append(i)
plt.figure(figsize=(5,8))
colors = sns.color_palette('pastel')
myexplode = [0.1,0.1,0.1]
plt.pie(df_count["Sales"], colors = colors,explode = myexplode, labels=labels, autopct = "%0.0f%%",shadow = True) 
plt.show()

## Diabetes Data

import pandas as pd
import numpy as np
import seaborn as sns
df=pd.read_csv('diabetes.csv')
df

df.head()

df.info()

df.describe()

df.isnull().sum()

df.dtypes

df['DiabetesPedigreeFunction'].value_counts()

sns.boxplot(x='BloodPressure', data=df)

sns.countplot(x='BMI',data=df)

sns.distplot(df["Outcome"])

sns.histplot(x='Age',data=df)

```
## Output:

## SUPERSTORE:

## Dataset:
![Screenshot from 2023-03-29 23-56-29](https://user-images.githubusercontent.com/119218812/228638014-2abd461d-4eb1-4579-9fb4-74b22f447c0c.png)

## Head:
![Screenshot from 2023-03-29 23-56-56](https://user-images.githubusercontent.com/119218812/228638174-8cfec8e8-25fc-44b5-9d93-5e3f489f78fb.png)

## Info:
![Screenshot from 2023-03-29 23-57-20](https://user-images.githubusercontent.com/119218812/228638239-edd0b532-113f-4def-999d-75b64a63a525.png)

## Describe:
![Screenshot from 2023-03-29 23-57-31](https://user-images.githubusercontent.com/119218812/228638250-7c6a3ca6-c44f-4ae1-b3d8-f9bc8cd0e325.png)

## Isnull:
![Screenshot from 2023-03-29 23-57-41](https://user-images.githubusercontent.com/119218812/228638285-29fc9471-6882-4d82-a287-fb5b70b6a51d.png)

## dtypes:
![Screenshot from 2023-03-29 23-57-48](https://user-images.githubusercontent.com/119218812/228638292-0c3134a2-d150-4824-8296-7c8011d15b55.png)

## Valuecount:
![Screenshot from 2023-03-29 23-57-56](https://user-images.githubusercontent.com/119218812/228638329-98d24ce3-2785-43bc-811a-b711f1ac836d.png)

## Boxplot:
![Screenshot from 2023-03-29 23-58-07](https://user-images.githubusercontent.com/119218812/228638354-fb12c46d-fe24-47ee-be3f-032ad6ce6b47.png)

## Countplot:
![Screenshot from 2023-03-29 23-58-18](https://user-images.githubusercontent.com/119218812/228638374-d36ef500-7515-48f6-ab5d-2fbaa653a816.png)

## Distribution plot:
![Screenshot from 2023-03-29 23-58-35](https://user-images.githubusercontent.com/119218812/228638417-5a69f040-29af-4290-b23e-54a70f640b66.png)

## Histogram plot:
![Screenshot from 2023-03-29 23-58-45](https://user-images.githubusercontent.com/119218812/228638419-c340673a-f297-4e3d-80ff-677c9a49d4f4.png)

## Pie-Chart:
![Screenshot from 2023-03-29 23-59-03](https://user-images.githubusercontent.com/119218812/228638436-94e5c8a6-cdb0-4995-a058-74bdd61d510e.png)

## DIABETES:

## Dataset:
![Screenshot from 2023-03-29 23-59-46](https://user-images.githubusercontent.com/119218812/228638484-a582fac0-635a-4846-8ed7-85b79ab846f2.png)

## Head:
![Screenshot from 2023-03-29 23-59-59](https://user-images.githubusercontent.com/119218812/228638506-f487da59-34c3-4246-8287-5d4b9f3a97cd.png)

## Info:
![Screenshot from 2023-03-30 00-00-08](https://user-images.githubusercontent.com/119218812/228638537-613fa9b6-968d-45ea-9da1-1f9282657313.png)

## Describe:
![Screenshot from 2023-03-30 00-00-18](https://user-images.githubusercontent.com/119218812/228638552-90512ad0-6637-4c9c-bfce-a8e6829b8b9d.png)

## Isnull:
![Screenshot from 2023-03-30 00-00-34](https://user-images.githubusercontent.com/119218812/228638587-fe8697ca-40f8-4cc8-871d-0086a665a858.png)

## dtypes:
![Screenshot from 2023-03-30 00-00-41](https://user-images.githubusercontent.com/119218812/228638751-ee07d7b2-f65f-422f-8e86-d769c2993731.png)

## Valuecount:
![Screenshot from 2023-03-30 00-00-58](https://user-images.githubusercontent.com/119218812/228638752-2deb42ca-2690-459d-b505-0464787eb522.png)

## Boxplot:
![Screenshot from 2023-03-30 00-01-18](https://user-images.githubusercontent.com/119218812/228638767-4101e71f-bc79-4c0e-be3d-ab639e222398.png)

## Countplot:
![Screenshot from 2023-03-30 00-01-27](https://user-images.githubusercontent.com/119218812/228638806-ee137cfc-0fd6-40c0-ac65-9852535896c0.png)

## Distribution plot:
![Screenshot from 2023-03-30 00-01-41](https://user-images.githubusercontent.com/119218812/228638808-c706f2d4-d2bf-4471-a5cf-9fcfee3a3b70.png)

## Histogram plot:
![Screenshot from 2023-03-30 00-01-49](https://user-images.githubusercontent.com/119218812/228638835-fa2ae1c7-2433-459e-b783-6f6401d66389.png)

## Result:

Thus we have read the given data and performed the univariate analysis with different types of plots.
