# **CryptoClustering**
Module 19 Cluster Challenge

For this week's challenge, a dataset was provided containing different cryptocurrencies and their price changes over a certain time period. Our goal was to predict using unsupervised learning if currencies were affected by the price change over a 24 hour period or a 7 day period. 


## **Section 1: Prepare the Data**

Import the data from the resources folder. Once completed, using StandardScalar() from scikitlearn import, the data becomes scaled.


## **Section 2: Find the Best Value for k Using the Scaled DataFrame**

Now that there is a new scaled data frame, we are going to fit the k.model according to this new dataframe. On completion, an elbow curve  
was generated in order to compare K versus Inertia values to find the most optimal K value. According to the graph the best value for K equals 4.

### Question: What is the best value for `k`?
### Answer: According to the graph the most optimal k-value should be 4


## **Section 3: Cluster Cryptocurrencies with K-means Using the Scaled DataFrame**

Initialize the K-means model with the best K-value that was found. Next, fit the model with the scaled dataframe. After, predict the clusters of cryptocurrencies then
add this column to the dataframe. Lastly, create a scatterplot of the clusters to visual how the cryptocurrencies are grouped based on the price change over the 24 hour period
versus the 7 day period.

## **Section 4: Optimize Clusters with Principal Component Analysis**

This step a PCA is performed on the orginal scaled DataFrame to find total explained variance of the three principal components and create a new DataFrame with the 
scaled PCA data.

### Question: What is the total explained variance of the three principal components?
### Answer: The total explained variance ratio is: 0.8950316570309841

## **Section 5: Find the Best Value for k Using the PCA DataFrame**

Similar to section two but this time performed the same code for the PCA dataframe that was created. This allowed us to perform another elbow curve and find again that the most optimal 
K-value was 4.

### Question: What is the best value for `k` when using the PCA data?
### Answer: Again the graph seems like a k value of 4 is the best.

### Question: Does it differ from the best k value found using the original data?
### Answer: No it does not.

## **Section 6: Cluster Cryptocurrencies with K-means Using the PCA DataFrame**

Repeat of section 3, again this time using the PCA dataframe and comparing PCA1 versus PCA2 columns then performing a scattterplot for the clusters.

## **Section 7: Visual and Compare the Results** 
In this section, we plotted the two elbow curves and the two scatter plots against each other. 
![image](https://github.com/user-attachments/assets/659102c6-b290-4e9d-ac90-4fccb244596f)

![image](https://github.com/user-attachments/assets/68ffebff-d246-44fb-804d-cd9c02d69923)

### Question:   After visually analyzing the cluster analysis results, what is the impact of using fewer features to cluster the data using K-Means?
### Answer:   I believe if fewer clusters were used those random outliers that formed their own one point cluster would be apart of a different cluster group and make the data 
look cleaner.

