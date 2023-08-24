# CryptoClustering

## Prepare the Data
- I used the StandardScaler() module from scikit-learn to normalize the data from the CSV file we were given
- Next I created a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame

## Find the Best Value for k Using the Original Scaled DataFrame
- I used the elbow method to find the best value for k while using the original scaled DataFrame which was 4

## Cluster Cryptocurrencies with K-means Using the Original Scaled Data
- I clustered the cryptocurrencies for the best value for k on the original scaled data
- I created a scatter plot using hvPlot as follows:
  - Set the x-axis as "PC1" and the y-axis as "PC2"
  - Colored the graph points with the labels found using K-means
  - Added the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point

 ## Optimize Clusters with Principal Component Analysis
 - Used the original scaled DataFrame and performed a PCA and reduced the features to three principal components
 - I retrieved the explained variance to determine how much information can be attributed to each principal component which was 89.5%
 - Created a new DataFrame with the PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame

## Find the Best Value for k Using the PCA Data
- Used the elbow method on the PCA data to find the best value for k which was 4
- The k value did not differ from the k value found using the original data

## Cluster Cryptocurrencies with K-means Using the PCA Data
- I clustered the cryptocurrencies for the best value for k on the PCA data
- I created a scatter plot using hvPlot as follows:
  - Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d"
  - Colored the graph points with the labels found using K-means
  - Added the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point

 ## The impact of using fewer features to cluster the data using K-Means
 - I found that reducing the number of features significantly narrows the distribution of data points in a scatter plot designed to represent clusters. This also enhances the clarity of the clusters when plotted across two columns. The inertia is also diminished in the elbow visualization used to determine the optimal K, but overall it doesn't influence the position of the elbow point.
 
  
