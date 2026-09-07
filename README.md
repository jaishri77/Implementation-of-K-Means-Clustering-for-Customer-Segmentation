# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Load the customer dataset and select relevant features such as Annual Income and Spending Score.
2. Initialize the K-Means algorithm with a suitable number of clusters.
3. Assign customers to clusters based on the nearest cluster centroid and update the centroids.
4. Repeat until the centroids stabilize and display the customer segments using a scatter plot.

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: Jayasree T S
RegisterNumber: 212224040135 
*/
```
```
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans
data = pd.read_csv("Mall_Customers (1).csv")
X = data.iloc[:, [3, 4]].values
kmeans = KMeans(n_clusters=5, random_state=0)
y_kmeans = kmeans.fit_predict(X)
plt.scatter(X[:, 0], X[:, 1], c=y_kmeans, s=100)
plt.scatter(kmeans.cluster_centers_[:, 0],
            kmeans.cluster_centers_[:, 1],
            s=200,
            marker='X')
plt.xlabel("Annual Income")
plt.ylabel("Spending Score")
plt.title("Customer Segmentation using K-Means")
plt.show()

```

## Output:
<img width="1245" height="687" alt="image" src="https://github.com/user-attachments/assets/77af8c98-d97b-48e0-a59a-b0a5948f5cd6" />


## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
