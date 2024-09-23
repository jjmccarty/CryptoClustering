# Module 11 Challenge (CryptoClustering)

This challenge applies the K-Means algorithm and Principal Component Analysis (PCA) to provided price fluctuations in cryptocurrency data.

## Section 1 - Preparing Data & finding the best K values

This section will utilizes the ```StandardScaler()``` from the ```scikit-learn``` library to normalize the data provided in the starter .csv file. 

To find the best value for 'k' we will review the inertia for each of 10 test values for 'k'.  From this data the elbow curve will be plotted and the values for 'k' evaluated. 

> Note that it was noticed the routine for identifying the 'k' value data for the elbow what utilized multiple times.  In this case a function was created called ```get_kmeans_elbow_data``` to reduce code duplication. 

Once the best fit for 'k' is identified the information is plotted to view the clusters defined. 

## Section 2 - Optimizing with PCA

To see if we can further refine the clusters we then apply principal Component Analysis to the data.  The variance of the principal components is viewed across a new dataframe describing the variance for each component. 

We then find the new k-means for the PCA filtered data and plot the predicted to clusters to determine if using fewer features gives us a better clustering.

The weight of each feature is evaluated to determine the most positive and negative influces on the features. 