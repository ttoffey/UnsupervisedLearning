# UnsupervisedLearning - Cryptocurrency Clusters

## Background

### Objective: A prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. The company, however, is lost in the vast universe of cryptocurrencies. Create a report that includes what cryptocurrencies are on the trading market and determine whether they can be grouped to create a classification system for this new investment.

#### Data: Process the raw data provided by the investment bank to fit the machine learning models.Use unsupervised learning to create a classification system. Utilize several clustering algorithms to explore whether the cryptocurrencies can be grouped together with other similar cryptocurrencies. Provide data visualization to share your findings with the investment bank. (The dataset was obtained from [CryptoCompare](https://min-api.cryptocompare.com/data/all/coinlist).

### Instructions

#### Data Preparation

* Discard all cryptocurrencies that are not being traded. In other words, filter for currencies that are currently being traded. Drop the `IsTrading` column from the dataframe.

* Remove all rows that have at least one null value.

* Filter for cryptocurrencies that have been mined. That is, the total coins mined should be greater than zero.

* Delete the `CoinName` from the original dataframe.

* Your next step in data preparation is to convert the remaining features with text values, `Algorithm` and `ProofType`, into numerical data. 

* Standardize your dataset so that columns that contain larger values do not unduly influence the outcome.

#### Dimensionality Reduction

* Perform dimensionality reduction with PCA. Preserve 90% of the explained variance in dimensionality reduction.

* Next, further reduce the dataset dimensions with t-SNE and visually inspect the results. Then create a scatter plot of the t-SNE output. 

#### Cluster Analysis with k-Means

* Create an elbow plot to identify the best number of clusters. Use a for-loop to determine the inertia for each `k` between 1 through 10. Determine, if possible, where the elbow of the plot is, and at which value of `k` it appears.

### Recommendation

After running TSNE, there is one distinct cluster. Based on the elbow curve (while slight), the number of clusters was set at 5 and most of the data falls into Class 0 (out of 532 data points, 528 fall into Class 0 and 1 falls into each of the other four classes.) I do not think you can cluster cryptocurrencies because most of the data points fell into one cluster.