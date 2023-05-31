# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import pandas and matplot libraries.


2.import Kmeans algorithm to solve customer segmentation.


3.Using the for loop cluster the given data


4.Predict the output and plot data graphs.


5.Display the outputs
## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: DIVAKAR R
RegisterNumber: 212222240026

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
plt.title("Customer segments")
*/
```

## Output:


data.head() function


![ml-801](https://github.com/divakar618/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/118708040/8e900a9c-54bc-4d0b-921f-48ba9275667a)



data.info


![ml802](https://github.com/divakar618/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/118708040/e3f7fe34-5b79-40b0-a215-3cd52492e673)


data.isnull().sum() function


![ml803](https://github.com/divakar618/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/118708040/0677bbc0-3f72-4c32-ad2d-14101bfd20e0)


Elbow Method Graph



![ml804](https://github.com/divakar618/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/118708040/cfb9a577-1912-4cde-b3f9-16a22b712d3f)



KMeans clusters



![ml805](https://github.com/divakar618/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/118708040/aaf31097-7014-4af4-bb08-6a0ba2910ba7)




array()





![ml806](https://github.com/divakar618/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/118708040/cc561b93-1b2b-48d3-8be9-6fb69240c3ed)





Customers segments Graph



![ml807](https://github.com/divakar618/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/118708040/ded43827-bacf-4ee7-8410-b33928601af5)







## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
