# Cryptocurrencies

## Overview of Analysis
The purpose of this analysis is to use unsupervised machine learning models to generate classification groups of market-available tradable cryptocurrencies. 

The inital dataset was cleaned, and transformed to be used as numerical information prior to scaling and fitting to the PCA (Principal Component Analysis) model. The dataset was then fit to the KMeans model to determine the optimal number of clusters in the dataset, and finally predictions of the model clusters were computed.

The computed clusters were then visualized for ease of interpretability.

## Results
![Elbow Curve](https://github.com/JorMerr/Cryptocurrencies/blob/main/img/KMeans_Elbow.JPG)

The above image shows the Elbow Curve derived from the PCA model analysis. The steep horizontal shift at 4 clusters indicated a suitable number of clusters for initializing the KMeans model to determine class predictions.

![Scatter 3D](https://github.com/JorMerr/Cryptocurrencies/blob/main/img/cluster_3DScatter.JPG)

The Principal Components have been plotted to a 3D Scatter plot, wherein each cryptocurrency datapoint will show the Coin Name and Algorithm used to mine it when the point is hovered over by a mouse cursor. The 3D Scatter plot shows high concentration of classes 3 and 0 from our dataset, while relatively low instances of class 1, and a single datapoint of class 2.

![HV Table](https://github.com/JorMerr/Cryptocurrencies/blob/main/img/clustered_hvtable.JPG)

The 532 tradable cryptocurrencies have been placed within an HV Table to allow for interactivity with the cleaned dataset clusters.

![MinMaxScaler DataFrame](https://github.com/JorMerr/Cryptocurrencies/blob/main/img/MinMaxScaler_plot_df.JPG)

The dataset was then scaled once more for the Total Coin Supply and Total Coins Mined columns from the clustered data and assigned to a new DataFrame with Coin Name and predicted Classes.

![MinMaxScaler Scatter](https://github.com/JorMerr/Cryptocurrencies/blob/main/img/MinMaxScaler_scatter.JPG)

The data was finally plotted to an HV Scatter plot to indicate the clusters by class.
