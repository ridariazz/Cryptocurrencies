# Overview

In this project, we learned the process data through unsupervised learning. Moreover, we also learned how to cluster, reduce our dimensions and reduce the principal components using PCA. In our analysis, our client is interested in offering a new cryptocurrency investment portfolio for its customers, so we created a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment. 

We processed the data to fit the machine learning models, specifcally we used unsupervised models as we don't really know what output we're looking for. To group cryptocurrencies, we decided on using a clustering algorithm. 

## Results 

### Deliverable 1: Preprocessing the Data for PCA

For this deliverable, we created a new data frame that stores all cryptocurrency names from the CoinName column and retains the index from the crypto_df. 

**Figure 1** 

![fig1](https://user-images.githubusercontent.com/106577074/196821932-0e6eae91-b73f-4e46-b2a9-523b6574d35a.png)

Next, we used the get_dummies() method to create variables for the text features and then standardized them using the StandardScaler fit_transform() function.

**Figure 1.1**

![fig1 1](https://user-images.githubusercontent.com/106577074/196822006-cc1bb5f5-54bd-44d2-9a31-1faae50e1b29.png)

![fig1 1 1](https://user-images.githubusercontent.com/106577074/196822016-dd1f78fb-282f-4b3d-9225-bacc19ece87b.png)

### Deliverable 2: Reducing Data Dimensions Using PCA

In this section, we reduced the dimensions of the X data frame down to three principal components using the PCA algorithm. Moreover, we created a new data frame, pcs_df, that has the columns "PC 1, PC 2, and PC 3"

**Figure 2**

![fig2](https://user-images.githubusercontent.com/106577074/196822053-72bca2a1-2b6d-4a88-bd85-be5278f2aa97.png)

### Deliverable 3: Clustering Cryptocurrencies Using K-means

We created an Elbow Curve using the hvPlot function to find the best value for K from the pcs_df data frame. Then, we ran the K-algorithm to predict the K clusters for the cryptocurrencies' data. 

**Figure 3**

![fig3](https://user-images.githubusercontent.com/106577074/196822081-d37476f2-8dab-41e5-b6b5-54fd47bd3b00.png)

Then, we created a new data frame including the predicted clusters and cryptocurrencies features. 

**Figure 3.1**

![fig 3 1](https://user-images.githubusercontent.com/106577074/196822096-27d1c39f-ad92-4015-b08c-e07c4d6938f8.png)

### Deliverable 4: Visualizing Cryptocurrencies Results

Lastly, we created visualizations related to our findings from the overall analysis. We plotted distinct groups that correspond to the three principal components. 

**Figure 4**

![fig4](https://user-images.githubusercontent.com/106577074/196822116-95d1cdc6-54f2-4975-b1a1-829e6ddf02c0.png)

Moreover, we also created a table with all the currently tradable cryptocurrencies using the hvplot.table() function. 

**Figure 4.1**

![fig4 1](https://user-images.githubusercontent.com/106577074/196822132-4c802f93-1d99-42da-abaa-3577083e655a.png)

We continued further with our analysis by creating a data frame that contains our clustered_df index, the scaled data and the CoinName and Class columns. 

**Figure 4.2**

![fig4 2](https://user-images.githubusercontent.com/106577074/196822178-03295d8a-4b01-4336-b7b6-d5a2682b991c.png)

Finally, a hvplot scatter plot is created where the X-axis is "TotalCoinsMined", the Y-axis is "TotalCoinSupply", the data is ordered by "Class", and it shows the CoinName when we hover over the data point.

**Figure 4.3**

![fig4 3](https://user-images.githubusercontent.com/106577074/196822193-5ef79759-cba9-4553-8237-7e5f816227ee.png)
