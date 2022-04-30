# Cryptocurrencies
Use unsupervised machine learning techniques to analyze cryptocurrency data

## Overview
You and Martha have done your research. You understand what unsupervised learning is used for, how to process data, how to cluster, how to reduce your dimensions, and how to reduce the principal components using PCA. It’s time to put all these skills to use by creating an analysis for your clients who are preparing to get into the cryptocurrency market.

Martha is a senior manager for the Advisory Services Team at Accountability Accounting, one of your most important clients. Accountability Accounting, a prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. The company, however, is lost in the vast universe of cryptocurrencies. So, they’ve asked you to ***create a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment.***

The data Martha will be working with is not ideal, so it will need to be processed to fit the machine learning models. Since there is no known output for what Martha is looking for, she has decided to use unsupervised learning. To group the cryptocurrencies, Martha decided on a clustering algorithm. She’ll use data visualizations to share her findings with the board.


## Deliverable 1

**Directions:**
1. Read in the `crypto_data.csv` to the Pandas DataFrame named crypto_df.
2. Keep all the cryptocurrencies that are being traded.
3. Drop the `IsTrading` column.
4. Remove rows that have at least one null value.
5. Filter the `crypto_df` DataFrame so it only has rows where coins have been mined.
6. Create a new DataFrame that holds only the cryptocurrency names, and use the `crypto_df` DataFrame index as the index for this new DataFrame.
7. Remove the `CoinName` column from the `crypto_df` DataFrame since it's not going to be used on the clustering algorithm.

> Results:

<img width="669" alt="D1-1" src="https://user-images.githubusercontent.com/95068439/166083210-216a9c67-c2cf-40c6-81f5-de596e7cd631.png">

<img width="710" alt="D1-2" src="https://user-images.githubusercontent.com/95068439/166083215-3ca1952d-ff33-423d-9b41-91f8ebe42c5b.png">

<img width="639" alt="D1-3" src="https://user-images.githubusercontent.com/95068439/166083218-284d1973-dcaa-499a-8a41-c9d4cf03bab6.png">

<img width="1101" alt="D1-4" src="https://user-images.githubusercontent.com/95068439/166083228-bcf1412b-2f71-4013-b05d-496a4ce6601f.png">

## Deliverable 2

**Directions:**
1. Using the information we’ve provided, apply PCA to reduce the dimensions to three principal components.
2. Create a new DataFrame named `pcs_df` that includes the following columns, `PC 1`, `PC 2`, and `PC 3`, and uses the index of the `crypto_df` DataFrame as the index.

> Results:
 
<img width="912" alt="D2" src="https://user-images.githubusercontent.com/95068439/166083351-e2c64986-e923-4138-8ee4-953dd9d5d115.png">

## Deliverable 3

**Directions:**
1. Using the pcs_df DataFrame, create an elbow curve using hvPlot to find the best value for K.
2. Next, use the pcs_df DataFrame to run the K-means algorithm to make predictions of the K clusters for the cryptocurrencies’ data.
3. Create a new DataFrame named clustered_df by concatenating the crypto_df and pcs_df DataFrames on the same columns. The index should be the same as the crypto_df DataFrame.
4. Add the CoinName column that holds the names of the cryptocurrencies, which you created in Step 7 of Deliverable 1, to the clustered_df.
5. Add another new column to the clustered_df named Class that holds the predictions, i.e., model.labels_, from Step 3.

> Results:

<img width="1018" alt="D3-1" src="https://user-images.githubusercontent.com/95068439/166083770-a1e1cf6a-9c7a-4a83-9e70-0fbfa456ad83.png">

<img width="1114" alt="D3-2" src="https://user-images.githubusercontent.com/95068439/166083771-53ad3125-1cd1-4471-b2b2-b7f323e277d8.png">

## Deliverable 4

**Directions:**
1. Create a 3D scatter plot using the Plotly Express `scatter_3d()` function to plot the three clusters from the `clustered_df` DataFrame.
2. Add the `CoinName` and `Algorithm` columns to the `hover_name` and `hover_data` parameters, respectively, so each data point shows the CoinName and Algorithm on hover.
3. Create a table with tradable cryptocurrencies using the `hvplot.table()` function.
4. Print the total number of tradable cryptocurrencies in the `clustered_df` DataFrame.
5. Use the `MinMaxScaler().fit_transform` method to scale the `TotalCoinSupply` and `TotalCoinsMined` columns between the given range of zero and one.

> Results

<img width="1081" alt="Screen Shot 2022-04-29 at 20 44 00" src="https://user-images.githubusercontent.com/95068439/166084099-e4858411-694f-42ef-8f21-a5ccd3f3b3ec.png">

<img width="937" alt="Screen Shot 2022-04-29 at 20 48 16" src="https://user-images.githubusercontent.com/95068439/166084101-f8db2971-6a84-41e4-823e-9243af7170a2.png">

<img width="1143" alt="Screen Shot 2022-04-29 at 20 49 23" src="https://user-images.githubusercontent.com/95068439/166084104-75611692-c6d7-44fa-8eae-250ab3614654.png">

<img width="1061" alt="Screen Shot 2022-04-29 at 20 49 58" src="https://user-images.githubusercontent.com/95068439/166084109-08ad20f0-94e3-4f66-8d26-bf887314b7ee.png">

<img width="1116" alt="Screen Shot 2022-04-29 at 20 50 27" src="https://user-images.githubusercontent.com/95068439/166084111-8d5eb292-f7ca-481b-afe6-3435752928da.png">

> LinkedIn: https://www.linkedin.com/in/wilson-alexei/

> Email: wils.alexei@gmail.com
