# Cryptocurrencies

# Overview of Project

You and Martha have done your research. You understand what unsupervised learning is used for, how to process data, how to cluster, how to reduce your dimensions, and how to reduce the principal components using PCA. It’s time to put all these skills to use by creating an analysis for your clients who are preparing to get into the cryptocurrency market.

Martha is a senior manager for the Advisory Services Team at Accountability Accounting, one of your most important clients. Accountability Accounting, a prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. The company, however, is lost in the vast universe of cryptocurrencies. So, they’ve asked you to create a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment.

The data Martha will be working with is not ideal, so it will need to be processed to fit the machine learning models. Since there is no known output for what Martha is looking for, she has decided to use unsupervised learning. To group the cryptocurrencies, Martha decided on a clustering algorithm. She’ll use data visualizations to share her findings with the board.

# Deliverables:

This new assignment consists of three technical analysis deliverables and a written report.

### Deliverable 1: Preprocessing the Data for PCA
### Deliverable 2: Reducing Data Dimensions Using PCA
### Deliverable 3: Clustering Cryptocurrencies Using K-means
### Deliverable 4: Visualizing Cryptocurrencies Results

Deliverables:
This new assignment consists of three technical analysis deliverables and a proposal for further statistical study:

Data Source: crypto_data.csv
Data Tools: crypto_clustering_starter_code.ipynb.
Software: Python 3.9, Visual Studio Code 1.50.0, Anaconda 4.8.5, Jupyter Notebook 6.1.4 and Pandas

![image](https://user-images.githubusercontent.com/86340630/138238734-5ecf3211-6944-461f-8452-c6e0b407d6a2.png)

# Deliverable 1:

Preprocessing the Data for PCA

## Deliverable Requirements:

Using your knowledge of Pandas, you’ll preprocess the dataset in order to perform PCA in Deliverable 2

To Deliver.

Follow the instructions below:

Follow the instructions below and use the crypto_clustering_starter_code.ipynb file to complete Deliverable 1.

Open the crypto_clustering_starter_code.ipynb file, rename it crypto_clustering.ipynb, and save it to your Cryptocurrencies GitHub folder.

1. Read in the crypto_data.csv to the Pandas DataFrame named crypto_df.

NOTE The crypto_data.csv was retrieved from CryptoCompare.

2. Keep all the cryptocurrencies that are being traded.
3. Keep all the cryptocurrencies that have a working algorithm.
4. Drop the IsTrading column.
5. Remove rows that have at least one null value.
6. Filter the crypto_df DataFrame so it only has rows where coins have been mined.
7. Create a new DataFrame that holds only the cryptocurrency names, and use the crypto_df DataFrame index as the index for this new DataFrame.
8. Remove the CoinName column from the crypto_df DataFrame since it's not going to be used on the clustering algorithm.
9. Take a moment to check that your crypto_df DataFrame looks like the image below:

![image](https://user-images.githubusercontent.com/86340630/138239390-49632d63-9018-41c3-8933-8a10e2926d8f.png)

9. Use the get_dummies() method to create variables for the two text features, Algorithm and ProofType, and store the resulting data in a new DataFrame named X.
10. Use the StandardScaler fit_transform() function to standardize the features from the X DataFrame.

IMPORTANT Using the StandardScaler() sklearn library to standardize the features is required before attempting Deliverables 2 and 3.

Save your crypto_clustering.ipynb file to your Cryptocurrencies folder.

### Deliverable 1 Requirements

* The following six preprocessing steps have been performed on the crypto_df DataFrame:
  
  ° All cryptocurrencies that are not being traded are removed
  
  ° All cryptocurrencies that do not have a defined algorithm are removed
  
  ° The IsTrading column is dropped
  
  ° All the rows that have at least one null value are removed
  
  ° All the rows that do not have coins being mined are removed
  
  ° The CoinName column is dropped

* A new DataFrame is created that stores all cryptocurrency names from the CoinName column and retains the index from the crypto_df DataFrame
* The get_dummies() method is used to create variables for the text features, which are then stored in a new DataFrame, X
* The features from the X DataFrame have been standardized using the StandardScaler fit_transform() function

## DELIVERABLE RESULTS:

### Deliverable 1

Preprocessing the Data for PCA
The following was done to preprocess the data:

1. Remove cryptocurrencies not being traded.
2. Keep all the cryptocurrencies that have a working algorithm
3. The IsTrading column it was dropped.
4. Rows that have null value were dropped.
5. Filter dataset with only mined coins.
6. Create a new DataFrame CoinNames, and use the index from the previous dataset as the index for this new DataFrame cc_names_df

![Captura de pantalla (917)](https://user-images.githubusercontent.com/86340630/138243129-9c493a69-7d31-4439-8d5e-d03ab68340c0.png)

7. Remove CoinName unnecessary column from the DataFrame crypto_df

![Captura de pantalla (921)](https://user-images.githubusercontent.com/86340630/138244688-833d52e2-569e-4ca3-87e2-699b31a632e4.png)

8. From get_dummies() method over columns Algorithm and ProofType and using the StandardScaler fit_transform() function to standardize the features.

![Captura de pantalla (920)](https://user-images.githubusercontent.com/86340630/138244072-69bfae47-4946-45f6-9f4f-cc225ae3a20d.png)

9. The features from the X DataFrame have been standardized using the StandardScaler fit_transform() function

![Captura de pantalla (923)](https://user-images.githubusercontent.com/86340630/138245508-88f03607-c80b-4e7f-b1c9-5f79b0cd9e1a.png)

# Deliverable 2:

Reducing Data Dimensions Using PCA
Deliverable Requirements:
Using your knowledge of how to apply the Principal Component Analysis (PCA) algorithm, you’ll reduce the dimensions of the X DataFrame to three principal components and place these dimensions in a new DataFrame.

To Deliver.

Follow the instructions below:

Follow the instructions below and use the information in the crypto_clustering_starter_code.ipynb file to complete Deliverable 2.

  1. Continue using the crypto_clustering.ipynb file from Deliverable 1 where you’ve already performed the preprocessing steps.
  2. Using the information we’ve provided, apply PCA to reduce the dimensions to three principal components.
 
 If you’d like a hint on how to use the PCA algorithm, that’s totally okay. If not, that’s great too. You can always revisit this later if you change your mind.

  3. Create a new DataFrame named pcs_df that includes the following columns, PC 1, PC 2, and PC 3, and uses the index of the crypto_df DataFrame as the index.
  
 Your DataFrame should look like the image below:
  
 ![image](https://user-images.githubusercontent.com/86340630/138245911-8a560d56-33bc-4020-adfc-8299b38704f9.png)

Save your crypto_clustering.ipynb file to your Cryptocurrencies folder.

### Deliverable 2 Requirements

* The PCA algorithm reduces the dimensions of the X DataFrame down to three principal components
* The pcs_df DataFrame is created and has the following three columns, PC 1, PC 2, and PC 3, and has the index from the crypto_df DataFrame

## DELIVERABLE RESULTS:

### Deliverable 2

### Reducing Data Dimensions Using PCA

The next steps involve, applying PCA to reduce the dimensions to 3 principal components.

The analysis from DataFrame, pcs_df includes columns PC 1, PC 2, and PC 3, and uses the index of the crypto_df DataFrame as the index.

![Captura de pantalla (925)](https://user-images.githubusercontent.com/86340630/138246704-80c9a69a-d495-4422-a43b-da673f93f3cc.png)

# Deliverable 3:

### Clustering Cryptocurrencies Using K-means

### Deliverable Requirements:
Using your knowledge of the K-means algorithm, you’ll create an elbow curve using hvPlot to find the best value for K from the pcs_df DataFrame created in Deliverable 2. Then, you’ll run the K-means algorithm to predict the K clusters for the cryptocurrencies’ data.

To Deliver.

Follow the instructions below:

Follow the instructions below and use the information in the crypto_clustering_starter_code.ipynb file to complete Deliverable 3.

1. Continue using the crypto_clustering.ipynb file that you used in Deliverable 2 to reduce the dataset to three dimensions.
2. Using the pcs_df DataFrame, create an elbow curve using hvPlot to find the best value for K.
3. Next, use the pcs_df DataFrame to run the K-means algorithm to make predictions of the K clusters for the cryptocurrencies’ data. If you’d like a hint on how to use the K-means algorithm, that’s totally okay. If not, that’s great too. You can always revisit this later if you change your mind.
4. Create a new DataFrame named clustered_df by concatenating the crypto_df and pcs_df DataFrames on the same columns. The index should be the same as the crypto_df DataFrame.
5. Add the CoinName column that holds the names of the cryptocurrencies, which you created in Step 7 of Deliverable 1, to the clustered_df.
6. Add another new column to the clustered_df named Class that holds the predictions, i.e., model.labels_, from Step 3.

Your clustered_df DataFrame should look like the image below:

![image](https://user-images.githubusercontent.com/86340630/138247305-2824126f-4526-457c-8ec4-3164ed8a862b.png)

Save your crypto_clustering.ipynb file to your Cryptocurrencies folder.

### Deliverable 3 Requirements

* The K-means algorithm is used to cluster the cryptocurrencies using the PCA data, where the following steps have been completed:

° An elbow curve is created using hvPlot to find the best value for K

° Predictions are made on the K clusters of the cryptocurrencies’ data

° A new DataFrame is created with the same index as the crypto_df DataFrame and has the following columns: Algorithm, ProofType, TotalCoinsMined, TotalCoinSupply, PC 1, PC 2, PC 3, CoinName, and Class

### DELIVERABLE RESULTS:

### Deliverable 3

### Clustering Cryptocurrencies Using K-means

Run analysis of clusters for the dataset pcs_df, including plotting an elbow curve with hvplot to find the value for K.

![Captura de pantalla (927)](https://user-images.githubusercontent.com/86340630/138247969-b59ad9ef-0045-4809-9fab-84d4f6a41ccf.png)

Using the dataset and analysis we found that 4 clusters is the initial point.

By running an analysis using K=4 and applying the K-means algorithm, got the below results:

![Captura de pantalla (929)](https://user-images.githubusercontent.com/86340630/138248131-f473a2b4-79f7-43be-8049-d522331d5ac3.png)

Build a new dataframe names: clustered_df

* Adding the CoinNames column from the cc_names_df dataset created.
* Merging the crypto_df and pcs_df DataFrames with the same index.

![Captura de pantalla (931)](https://user-images.githubusercontent.com/86340630/138248378-568ea1ea-abe1-4c72-90f5-132149e99334.png)

# Deliverable 4:

Visualizing Cryptocurrencies Results
Deliverable Requirements:
Using your knowledge of creating scatter plots with Plotly Express and hvplot, you’ll visualize the distinct groups that correspond to the three principal components you created in Deliverable 2, then you’ll create a table with all the currently tradable cryptocurrencies using the hvplot.table() function.

To Deliver.

Follow the instructions below:

Follow the instructions below and use the information in the crypto_clustering_starter_code.ipynb file to complete Deliverable 4.

1. Continue using the crypto_clustering.ipynb file from Deliverable 3 where you have predicted the K clusters for the cryptocurrencies’ data.
2. Create a 3D scatter plot using the Plotly Express scatter_3d() function to plot the three clusters from the clustered_df DataFrame.
3. Add the CoinName and Algorithm columns to the hover_name and hover_data parameters, respectively, so each data point shows the CoinName and Algorithm on hover.

If you’d like a hint on how to add additional parameters to a Plotly Express 3D scatter plot, that’s totally okay. If not, that’s great too. You can always revisit this later if you change your mind.

4. Create a table with tradable cryptocurrencies using the hvplot.table() function.

If you’d like a hint on how to use the hvplot.table() function, that’s totally okay. If not, that’s great too. You can always revisit this later if you change your mind.

Your table should look like the table in the image below:

![image](https://user-images.githubusercontent.com/86340630/138249212-19bc6adc-ead7-40a6-9aba-b36a82e61139.png)

5. Print the total number of tradable cryptocurrencies in the clustered_df DataFrame.
6. Use the MinMaxScaler().fit_transform method to scale the TotalCoinSupply and TotalCoinsMined columns between the given range of zero and one.

If you’d like a hint on how to use the MinMaxScaler().fit_transform method to scale the "TotalCoinSupply" and "TotalCoinsMined" columns, that’s totally okay. If not, that’s great too. You can always revisit this later if you change your mind.

7. Create a new DataFrame using the clustered_df DataFrame index that contains the scaled data you created in Step 5.
8. Add the CoinName column from the clustered_df DataFrame to the new DataFrame.
9. Add the Class column from the clustered_df DataFrame to the new DataFrame.

Your new DataFrame should look similar to the image below:

![image](https://user-images.githubusercontent.com/86340630/138249498-b0e0f30a-d745-40e6-bb66-5f17fe32e76d.png)

10. Create an hvplot scatter plot with x="TotalCoinsMined", y="TotalCoinSupply", and by="Class", and have it show the CoinName when you hover over the the data point.

If you’d like a hint on how to add the CoinName column data when you hover over a data point, that’s totally okay. If not, that’s great too. You can always revisit this later if you change your mind.

Your scatter plot should look similar to the image below:

![image](https://user-images.githubusercontent.com/86340630/138249786-a8981194-d907-4e49-817d-9039122eab3e.png)

Save your crypto_clustering.ipynb file to your Cryptocurrencies folder.

### Deliverable 4 Requirements

* The clusters are plotted using a 3D scatter plot, and each data point shows the CoinName and Algorithm on hover
* A table with tradable cryptocurrencies is created using the hvplot.table() function
* The total number of tradable cryptocurrencies is printed
* A DataFrame is created that contains the clustered_df DataFrame index, the scaled data, and the CoinName and Class columns
* A hvplot scatter plot is created where the X-axis is "TotalCoinsMined", the Y-axis is "TotalCoinSupply", the data is ordered by "Class", and it shows the CoinName when you hover over the data point

### DELIVERABLE RESULTS:

### Deliverable 4

### Visualizing Cryptocurrencies Results

![Captura de pantalla (935)](https://user-images.githubusercontent.com/86340630/138250452-34733f09-719e-47f3-b930-1234e9b62764.png)

A table is created featuring the tradable cryptocurrencies using the hvplot.table().

![Captura de pantalla (933)](https://user-images.githubusercontent.com/86340630/138250580-3f41deef-ce46-48af-8a10-511f51966378.png)

A 2D hvplot scatter plot with x="TotalCoinsMined_scaled", y="TotalCoinSupply_scaled", and by="Class" with the CoinName displayed.

![Captura de pantalla (937)](https://user-images.githubusercontent.com/86340630/138250832-c7dc26ff-8cd2-4da5-b40e-fcbf67d61bdb.png)

![Captura de pantalla (939)](https://user-images.githubusercontent.com/86340630/138251050-25ec9fd0-bb37-4a37-a162-aa4fd2d711a0.png)




























