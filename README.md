# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import pandas and matplot libraries.
2. import Kmeans algorithm to solve customer segmentation.
3. Using the for loop cluster the given data
4. Predict the output and plot data graphs.
5. Display the outputs

## Program:
```

Program to implement the K Means Clustering for Customer Segmentation.
Developed by: KARTHIKEYAN R
RegisterNumber:  212222240046


import pandas as pd

import matplotlib.pyplot as plt

data=pd.read_csv("/content/Mall_Customers (1) (1).csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.cluster import KMeans
WCSS=[]

for i in range(1,11):
  kmeans=KMeans(n_clusters=i,init="k-means++")
  kmeans.fit(data.iloc[:,3:])
  WCSS.append(kmeans.inertia_)

  plt.plot(range(1,11), WCSS)
plt.xlabel("No. of clusters")
plt.ylabel("WCSS")
plt.title("Elbow Method")

km=KMeans(n_clusters=5)
km.fit(data.iloc[:,3:])

y_pred=km.predict(data.iloc[:,3:])
y_pred

data["cluster"] = y_pred
df0 = data[data["cluster"]==0]

df1 = data[data["cluster"]==1]

df2 = data[data["cluster"]==2]

df3 = data[data["cluster"]==3]

df4 = data[data["cluster"]==4]

plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")

plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="black",label="cluster1")

plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="blue",label="cluster2")

plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster3")

plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="magenta",label="cluster4")

plt.legend()
plt.title("Customer segments")
```

## Output:
### data.head() function
![K Means Clustering for Customer Segmentation](ml-801.png)
### data.info
![K Means Clustering for Customer Segmentation](ml802.png)

### data.isnull().sum() function
![K Means Clustering for Customer Segmentation](ml803.png)

### Elbow Method Graph
![K Means Clustering for Customer Segmentation](ml804.png)

### KMeans clusters
![K Means Clustering for Customer Segmentation](ml805.png)

### array()
![K Means Clustering for Customer Segmentation](ml806.png)
### Customers segments Graph
![K Means Clustering for Customer Segmentation](ml807.png)



## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
