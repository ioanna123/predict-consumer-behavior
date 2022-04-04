# predict-consumer-behavior

Using machine learning to understand customers behavior

## Problem statement
One of the most common financial decisions that each of
us makes on a nearly daily basis involves the purchasing
of various products, goods, and services. In some cases the
decision on whether or not to make a purchase is based
largely on price but in many instances the purchasing decision is 
more complex, with many more considerations affecting the 
decision-making process before the final commitment is made. 
Retailers understand this well and attempt to make use of it in an 
effort to gain an edge in a highly competitive market. 


The goal of the present work is to examine using data driven
machine learning, whether specific objective and readily measurable factors 
influence customers’ decisions.


### Dataset collection
For the present work data were collected from kaggle
https://www.kaggle.com/datasets/akram24/mall-customers.
In order to perform the experiments, dataset should be stored into a pandas dataframe 

### Data exploration
It is crucial to explore the data to check the quality of the data and the distribution of the variables
* check that if there is any missing value
* check if there are duplicated rows
* check the type of categorical variables (transform the categorical variables)
* check information and statistics
* check correlation between the variables

### Clustering

Before clustering, we are going to select from the dataset all the useful columns. 
Customer ID is not a useful feature and Genre will split it into two binaries categories. 

#### K-means clustering

In order to cluster data, we need to determine if two data points are similar. 
A proximity measure characterizes the similarity or dissimilarity that exists between objects based on distance.
There are various distances that a clustering algorithm can use: 
* Manhattan distance
* Minkowski distance
* Euclidean distance etc

K-means typically uses Euclidean distance to determine how similar (or dissimilar) two points are.

The basic idea behind k-means consists of defining k clusters such that total within-cluster variation (or error) is minimum.
A cluster center is the representative of its cluster. The squared distance between each point and its cluster center is the 
required variation. The aim of k-means clustering is to find these k clusters and their centers while reducing the total error.

Two popular methods that can be useful to find k in k-Means
These methods are:
* The Elbow Method
* The Silhouette Method

##### The Elbow Method
Calculate the Within-Cluster-Sum of Squared Errors (WSS) for different values of k, and choose the k for which WSS 
becomes first starts to diminish. In the plot of WSS-versus-k, this is visible as an elbow.

##### The Silhouette Method
The silhouette value measures how similar a point is to its own cluster (cohesion) compared to other clusters 
(separation).
