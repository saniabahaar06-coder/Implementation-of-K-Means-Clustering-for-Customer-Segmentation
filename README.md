# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the necessary packages using import statement.

2.Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head().

3.Import KMeans and use for loop to cluster the data.

4.Predict the cluster and plot data graphs.

5.Print the outputs and end the program
## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: sania bahaar r
RegisterNumber:  21225240135

import pandas as pd
import matplotlib.pyplot as plt
data = pd.read_csv(r"Mall_Customers.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.cluster import KMeans
wcss = []
for i in range(1,11):
    kmeans = KMeans(n_clusters = i,init = "k-means++",n_init=10)
    kmeans.fit(data.iloc[:,3:])
    wcss.append(kmeans.inertia_)
plt.plot(range(1,11),wcss)
plt.xlabel("No. of Clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")
km = KMeans(n_clusters=5, n_init=10)
km.fit(data.iloc[:, 3:])
y_pred = km.predict(data.iloc[:,3:])
y_pred
km = KMeans(n_clusters=5, n_init=10)
km.fit(data.iloc[:, 3:])
y_pred = km.predict(data.iloc[:,3:])
y_pred
data["cluster"] = y_pred
df0 = data[data["cluster"]==0]
df1 = data[data["cluster"]==1]
df2 = data[data["cluster"]==2]
df3 = data[data["cluster"]==3]
df4 = data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster1")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="black",label="cluster2")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="blue",label="cluster3")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster4")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="magenta",label="cluster5")
plt.legend()
plt.title("Customer Segments")
*/
```

## Output:
![K Means Clustering for Customer Segmentation](sam.png)
<img width="710" height="297" alt="image" src="https://github.com/user-attachments/assets/03dfdaff-d2ff-416b-8e05-144b85a497e3" />
<img width="687" height="335" alt="image-1" src="https://github.com/user-attachments/assets/78761dad-3b9c-4137-96d7-ad1462297deb" />
<img width="348" height="218" alt="image-2" src="https://github.com/user-attachments/assets/d6bfe3de-a767-4a9b-a0d6-9f5d9dea64b9" />
<img width="808" height="823" alt="image-3" src="https://github.com/user-attachments/assets/0de0a6a1-2349-4fed-a404-6d639fe42c4d" />
<img width="804" height="438" alt="image-4" src="https://github.com/user-attachments/assets/b539ad8c-162c-447d-9a48-30e1c14b387d" />
<img width="833" height="744" alt="image-5" src="https://github.com/user-attachments/assets/f0e3465c-77de-442b-9a39-d112e060dfdc" />


## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
