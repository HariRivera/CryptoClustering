# CryptoClustering

Project Summary
This project aims to perform a clustering analysis on cryptocurrencies to identify natural groupings within the cryptocurrency market. We utilize machine learning techniques such as K-means and Principal Component Analysis (PCA) to cluster the cryptocurrencies based on their market characteristics.

Code Description
Data Preparation:

Import the necessary libraries (pandas, hvplot, sklearn) and load the cryptocurrency market data from a CSV file.
Normalize the data using StandardScaler from sklearn to standardize the features to a common scale.

Find the Best Value for k Using the Original Data:

Use the Elbow Method to determine the optimal number of clusters (k).
Plot the elbow curve to visually identify the best value for k, which turned out to be 4.

Cluster the Cryptocurrencies with K-means Using the Original Data:

Initialize the K-means model with k=4 and fit the model using the normalized data.
Predict the clusters and add the predicted cluster column to the original data.
Visualize the clusters in a scatter plot using hvplot.

Optimize the Clusters with Principal Component Analysis (PCA):

Reduce the features to three principal components using PCA.
Calculate the explained variance for each principal component, obtaining a total explained variance of 89.5%.
Create a new DataFrame with the PCA data and set the coin_id index from the original DataFrame.

Find the Best Value for k Using the PCA Data:

Repeat the Elbow Method using the PCA data to find the best value for k, which again was 4.
Plot the elbow curve for the PCA data for visual comparison.

Cluster the Cryptocurrencies with K-means Using the PCA Data:

Initialize and fit the K-means model using the PCA data.
Predict the clusters and visualize them in a scatter plot using hvplot.

Visualize and Compare the Results:

Create composite plots to compare the elbow curves and the clusters obtained using the original data and the PCA data.
Visually analyze the impact of using fewer features to cluster the data using K-means.
Graphical Results

Elbow Curves:

The elbow curves showed that the best value for k is 4 for both the original data and the PCA data.

Cryptocurrency Clusters:

The clusters formed using the original data are more dispersed compared to the more compact and clearly defined clusters obtained using the PCA data.
This indicates that dimensionality reduction with PCA helps capture significant variance and improves cluster separation.
Conclusion
Using PCA not only simplifies the clustering process by reducing the dimensionality of the data but also enhances the clarity and definition of the resulting clusters. This demonstrates the effectiveness of PCA in improving clustering analysis for cryptocurrencies.