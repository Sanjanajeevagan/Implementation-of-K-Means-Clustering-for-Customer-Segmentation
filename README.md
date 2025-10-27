# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import libraries (pandas, matplotlib, sklearn) and load the customer dataset using read_csv()
2. Check data for null values and general information using info() and isnull().sum()
3. Find optimal clusters by applying K-Means for k = 1 to 10 and plotting the Elbow Method using WCSS values.
4. Train final K-Means model with 5 clusters and predict the cluster labels for each customer.
5. Visualize the clusters using a scatter plot of Annual Income vs. Spending Score for all 5 groups.

## Program:
```PY
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: Sanjana J 
RegisterNumber:  212224230240


import pandas as pd

import matplotlib.pyplot as plt

data=pd.read_csv("/content/Mall_Customers (1).csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.cluster import KMeans

wcss=[]

for i in range(1,11):

kmeans=KMeans(n_clusters=i,init="k-means++")

kmeans.fit(data.iloc[:,3:])

wcss.append(kmeans.inertia_)

plt.plot(range(1,11),wcss)

plt.xlabel("No_of_Clusters")

plt.ylabel("wcss")

plt.title("Elbow Method")

km=KMeans(n_clusters=5)

km.fit(data.iloc[:,3:])

y_pred=km.predict(data.iloc[:,3:])

y_pred

data["cluster"]=y_pred

df0=data[data["cluster"]==0]

df1=data[data["cluster"]==1]

df2=data[data["cluster"]==2]

df3=data[data["cluster"]==3]

df4=data[data["cluster"]==4]

plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")

plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="black",label="cluster1")

plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="blue",label="cluster2")

plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster3")

plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="magenta",label="cluster4")

plt.legend()

plt.title("Customer Segment")

*/
```

## Output:
1. DATA.HEAD()

<img width="753" height="266" alt="image" src="https://github.com/user-attachments/assets/296ce335-2f2b-4184-8e71-d8f16cd2b225" />

2.DATA.INFO()

<img width="464" height="203" alt="image" src="https://github.com/user-attachments/assets/d3f72018-b4a7-4bfd-953f-a2446c00ebac" />

3.DATA.ISNULL().SUM()

<img width="461" height="148" alt="image" src="https://github.com/user-attachments/assets/3c36afb5-a449-4c42-ab4f-ec879ed35e11" />

4.PLOT USING ELBOW METHOD

<img width="456" height="322" alt="image" src="https://github.com/user-attachments/assets/849375bc-0f9a-4808-8269-e55e7997d062" />

5.K-MEANS CLUSTERING

<img width="473" height="185" alt="image" src="https://github.com/user-attachments/assets/711e9928-52ff-45d2-be67-4204a7a44bf0" />

6.Y_PRED ARRAY

<img width="889" height="269" alt="image" src="https://github.com/user-attachments/assets/7a975d0e-a4a6-45cc-88d0-0bdff0a6bbfc" />


7.CUSTOMER SEGMENT

<img width="807" height="642" alt="image" src="https://github.com/user-attachments/assets/a4a079db-f705-4eb2-a1d9-3d2a0f1304c3" />


## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
