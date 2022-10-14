# Cryptocurrencies
## Overview
In this project, we are going to use unsupervised machine learning to analyze a database of cryptocurrencies, create a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment.

## Resources
Data Source: crypto_data.csv<br/>
Software: Python 3.7.6 ,  Jupyter Notebook 6.4.8

## Results
### Preprocessing the data for PCA
Preprocess the dataset in order to perform PCA in next steps, then create variables for the text features and finally standardize the data.

### Reducing data dimensions using PCA
Reduce the dimensions of the DataFrame to three principal components using the Principal Component Analysis (PCA) algorithm and place these dimensions in a new DataFrame.

### Clustering cryptocurrencies using K-means
Create an elbow curve to find the best value for K, and then run the K-means algorithm to predict the K clusters for the cryptocurrencies’ data.<br/>
![Elbow Curve](https://user-images.githubusercontent.com/107179765/195776837-124c58d7-ffc7-43a3-97c3-41e1145f3f0f.png)<br/>
The line starts as a steep vertical slope that breaks at point 4, then shifts to a horizontal line that reaches to point 10. So we choose 4 as the best K-value to run the K-means algorithm.

### Visualizing cryptocurrencies results
Visualize the distinct groups that correspond to the three principal components which created in step 2, then create a table with all the currently tradable cryptocurrencies.
#### 3D-Scatter with the PCA data and the clusters
![3D-Scatter with the PCA data and the clusters](https://user-images.githubusercontent.com/107179765/195776853-29814cd5-ba8e-4a0c-90df-9d288c5c3b6d.png)<br/>
This plot shows that the 4 classes were significantly showed by the three principal components.
#### Tradable cryptocurrencies table
![table](https://user-images.githubusercontent.com/107179765/195776862-08b52ebd-f191-4644-86de-51b737df2a32.png)<br/>
There are 532 tradable cryptocurrencies.
#### 2D-Scatter plot with TotalCoinMined vs TotalCoinSupply
![hvplot scatter plot](https://user-images.githubusercontent.com/107179765/195776873-1eda0e56-03e8-42ab-a9ee-4870e9430701.png)<br/>
This plot uses two main features to plot the clusters. From the picture we can see that it does not efficiently segregate the different classes. So, using the PCA algorithm is the right method for better visualizations.

## Summary
In this project, we have identified 532 tradable cryptocurrencies based on the given data and grouped them into 4 clusters. Further analyses need to be done on each group to eventually determine the performance of each type of cryptocurrency and then offer a new cryptocurrency investment portfolio for the customers.
