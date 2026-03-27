# CryptoClustering with K-Mean & PCA

## Overview
This project applies **unsupervised learning** to group cryptocurrencies based on their short-term price changes. Using **Python, scikit-learn, and PCA**, we analyze how 24-hour and 7-day price changes influence clustering and explore dimensionality reduction to optimize clustering performance.

The workflow includes data preparation, clustering with K-Means, principal component analysis (PCA), and visualization of cryptoccurrency groups.

## Project Workflow
1. Prepare the Data
  * Import crypocurrency data from CSV
  * Normalized features using `StandardScaler`
  * Created a scaled DataFrame with `coin_id` as the index
2. Find the Best k Using the Scaled DataFrame
  * Used the **elbow method** to determine optimal clusters
  * Tested k-values from 1 to 11
  * Computed inertia and plotted the elbow curve
3. Cluster Cryptocurrencies Using K-Means
  * Applied K-Means to the scaled DataFrame
  * Added cluster labels to the DataFrame
  * Created an interactive scattor plot with **hvPlot:**
    * **x-axis:** `price_change_percentage_24h`
    * **y-axis:** `price_change_percentage_7d`
    * Points colord by cluster
    * Hover shows `coin_id`

## **Findings**

After executing both approaches, K-Means and PCA resulted in the ideal number of clusters being 4. Upon further analysis of the individual cluster charts created for each approach, it is evident that PCA is a more suitable. The impact of using fewer features to cluster the data improves the clustering performance by producing clearer visualizations and more comprehensible. In addition, it also reduces the number of outliers and irrelevant data that could potentially confuse the clustering algorithm.
