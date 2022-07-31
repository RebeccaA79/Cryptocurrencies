# Cryptocurrencies

## Overview

An investment bank is considering adding cryptocurrency as a new portfolio option for its customers. Before they proceed, a better understanding of what cryptocurrencies are trading on the market is needed. 

An analysis was performed on a cryptocurrency database using unsupervised machine learning. The four parts of the analysis include:

1. Preprocessing the Data for Principal Component Analysis (PCA)
2. Reducing Data Dimensions Using PCA
3. Clustering Cryptocurrencies Using K-means
4. Visualizing Cryptocurrencies Results  

The following details include a summary of the analysis which will show the investment bank how to group cryptocurrency to create a new classification system for the new investment portfolio.

## Results

### Deliverable 1: Preprocessing the Data for PCA

The crypto_data.csv file was retrieved from CryptoCompare and loaded into a Pandas Dataframe. The following image shows the updated dataframe after completing the preprocessing steps. There are 532 Cryptocurrencies remaining for analysis.

![crypto_df](https://github.com/RebeccaA79/Cryptocurrencies/blob/main/images/crypto_dataframe.png)

### Deliverable 2: Reducing Data Dimensions Using PCA

The PCA algorithm reduced the dimensions of the data down to three principal components (PC 1, PC 2, PC 3 as shown in the image below).

![pcs_df](https://github.com/RebeccaA79/Cryptocurrencies/blob/main/images/pcs_dataframe.png)

### Deliverable 3: Clustering Cryptocurrencies Using K-means

An Elbow curve using hvplot was created to find the best value of K from the pcs dataframe created in Deliverable 2. The best value of K = 4 as shown in the image below.

![elbow_curve](https://github.com/RebeccaA79/Cryptocurrencies/blob/main/images/elbow%20curve.png)


A new dateframe called clustered_df was then created by concatenating the crypto_df and pcs_df DataFrames and adding a new column to hold the coin names and classes as shown below.

![clustered_df](https://github.com/RebeccaA79/Cryptocurrencies/blob/main/images/clustered_df.png)

### Deliverable 4: Visualizing Cryptocurrencies Results

A 3D scatter plot was created to plot the three clusters from the clustered_df Dataframe. Each data point shows the CoinName and Algorithm when hovering over the image.

![scatter_plot](https://github.com/RebeccaA79/Cryptocurrencies/blob/main/images/3D%20Scatter%20with%20Clusters.png)

A table was created using hvplot.table() showing tradable cryptocurrencies as shown below

![tradable crypto tables](https://github.com/RebeccaA79/Cryptocurrencies/blob/main/images/tradable_crypto_table.png)

Total Coins Mined and Total Coin Supply were plotted in an hvPlot scatter plot as shown in the following image.

![hvPlot scatter plot](https://github.com/RebeccaA79/Cryptocurrencies/blob/main/images/plot_df.hvplot.scatter.png)

### Summary

This analysis provides information about relationships between each cryptocurrency and serves as a good starting point for the investment bank on how to group and market new cryptocurrency portfolios to the public. It is recommended that a deeper analysis is taken to understand the costs, benefits, and risks of this type of investment.
