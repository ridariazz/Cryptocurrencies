# Overview

In this project, we learned the process data through unsupervised learning. Moreover, we also learned how to cluster, reduce our dimensions and reduce the principal components using PCA. In our analysis, our client is interested in offering a new cryptocurrency investment portfolio for its customers, so we created a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment. 

We processed the data to fit the machine learning models, specifcally we used unsupervised models as we don't really know what output we're looking for. To group cryptocurrencies, we decided on using a clustering algorithm. 

## Results 

### Deliverable 1: Preprocessing the Data for PCA

For this deliverable, we created a new data frame that stores all cryptocurrency names from the CoinName column and retains the index from the crypto_df. 

**Figure 1** 

(add figure1)

Next, we used the get_dummies() method to create variables for the text features and then standardized them using the StandardScaler fit_transform() function.

**Figure 1.1**

(add fig 1.1 and 1.1.1)

### Deliverable 2: Reducing Data Dimensions Using PCA

In this section, we reduced the dimensions of the X data frame down to three principal components using the PCA algorithm. Moreover, we created a new data frame, pcs_df, that has the columns "PC 1, PC 2, and PC 3"

**Figure 2**

(add Figure 2)

### Deliverable 3: Clustering Cryptocurrencies Using K-means

We created an Elbow Curve using the hvPlot function to find the best value for K from the pcs_df data frame. Then, we ran the K-algorithm to predict the K clusters for the cryptocurrencies' data. 

**Figure 3**

(add fig 3)

Then, we created a new data frame including the predicted clusters and cryptocurrencies features. 

**Figure 3.1**

(add fig 3.1)

### Deliverable 4: Visualizing Cryptocurrencies Results

Lastly, we created visualizations related to our findings from the overall analysis. We plotted distinct groups that correspond to the three principal components. 

**Figure 4**

(add fig4)

Moreover, we also created a table with all the currently tradable cryptocurrencies using the hvplot.table() function. 

**Figure 4.1**

(add fig 4.1)

We continued further with our analysis by creating a data frame that contains our clustered_df index, the scaled data and the CoinName and Class columns. 

**Figure 4.2**

(add fig 4.2)

Finally, a hvplot scatter plot is created where the X-axis is "TotalCoinsMined", the Y-axis is "TotalCoinSupply", the data is ordered by "Class", and it shows the CoinName when we hover over the data point.

**Figure 4.3**

(add fig 4.3)