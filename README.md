# COGS118B_finalProject

This is the group repo for Team Ten's final project for COGS118B.
In this project, we have used the data from this [Kaggle](https://www.kaggle.com/heesoo37/120-years-of-olympic-history-athletes-and-results) dataset which contains information about the gender, age, height, weight, country, and year of Olympic athletes. This includes a selection of Games from Athens 1896 to Rio 2016 and, as the author of the dataset states, was scraped from [here](http://www.sports-reference.com/).

We aim to test the effectiveness of online and offline K-means algorithms by grouping this data across different time periods and seeing if the resulting cluster assignments differ with the introduction of more data or if there is a noticable difference between the clustering of online versus offline K-means algorithms.

## Algorithms used
### Offline K-Means Clustering
`runKMeans(K, array)`
Passes the argument array into the offline K-means algorithm and returns the final distributions in the form of a graph displaying the individual clusters and cluster centers. 

`returnOfflineCenters(K, array)`
Passes the argument array into the offline K-means algorithm and returns only the coordinates of the cluster centers.
- `K`: Represents the number of cluster centers intitialized. In our case, comparing heigths and weights between genders, `K = 2`
- `array`: Represents the dataset used to plot the data

### Sequential (Online) K-Means Clustering
`runSequentialKMeans(weight, frequency, array)`
Passes the argument array into the sequential K-means algorithm and, based on the frequency argument, returns a number of graphs displaying the movement of the cluster centers paired with the introduction of new data.
- `weight`: Takes values greater than 0 and less than or equal to 1. Represents how much the cluster center should be moved towards the new point, calculated by taking a fraction of its total distance from that cluster center.
- `frequency`: Represents how often the algorithm displays the graph containing datapoints and cluster centers.
- `array`: Represents the dataset used to plot the data
