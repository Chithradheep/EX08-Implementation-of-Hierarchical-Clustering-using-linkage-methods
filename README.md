# EX8-Implementation of Hierarchical Clustering using linkage methods
## DATE:
## AIM:
To implement Hierarchical Clustering using single and complete linkage method

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Initialize each data point as its own cluster.
2. Compute pairwise distances between clusters and create a distance matrix.
3. Iterate: Find the pair of clusters with the smallest distance based on the chosen linkage method (e.g., single, complete, average).
4. Merge the closest pair of clusters and update the distance matrix.
5. Repeat steps 3 and 4 until all points are in a single cluster or the desired number of clusters is reached.

## Program:
```
/*
Program to implement Hierarchical Clustering using single and complete linkage method
Developed by: Chithradheep R
RegisterNumber:  2305002003

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
from scipy.cluster.hierarchy import dendrogram, linkage, fcluster
from sklearn.cluster import AgglomerativeClustering
from sklearn.preprocessing import StandardScaler
df=pd.read_csv("/content/Hclus_EX8.csv")
df.head()
x=df[['StudentID','Marks']].values
x
Z=linkage(x,method='complete')
plt.figure(figsize=(5,2))
plt.title('Dendrogram for student segmentation')
labels=range(1,len(df)+1)
dendrogram(Z,labels=labels)
plt.xlabel("Student ID")
plt.ylabel("Marks")
plt.show()
Z=linkage(x,method='single')
plt.figure(figsize=(5,2))
plt.title('Dendrogram for student segmentation')
labels=range(1,len(df)+1)
dendrogram(Z,labels=labels)
plt.xlabel("Student ID")
plt.ylabel("Marks")
plt.show()
max_clusters=2
clusters=fcluster(Z,max_clusters,criterion='maxclust')
clusters
plt.figure(figsize=(5,2))
plt.scatter(x[:,0],x[:,1],c=clusters,cmap='rainbow',s=100)
plt.title("Student segmented (Hierarchial Clustering)")
plt.xlabel("Student ID")
plt.ylabel("Marks")
plt.show()
*/
```

## Output:
![Screenshot 2024-11-07 101545](https://github.com/user-attachments/assets/1fcccd56-6922-4fe3-bd93-c74431b1ea45)
![Screenshot 2024-11-07 101603](https://github.com/user-attachments/assets/ff988a45-b06c-46cc-9b69-a6e67a43a847)
![Screenshot 2024-11-07 101624](https://github.com/user-attachments/assets/f42a120b-2727-44b2-ab90-5428e28b5093)
![Screenshot 2024-11-07 101642](https://github.com/user-attachments/assets/9452297f-0356-4d69-8371-d69e3855878e)
![Screenshot 2024-11-07 101658](https://github.com/user-attachments/assets/208e3c4b-f1a2-4f5b-80f6-c2d23bb048d5)



## Result:
Thus the implementation of Hierarchical Clustering using single and complete linkage method in python programming and verified successfully.
