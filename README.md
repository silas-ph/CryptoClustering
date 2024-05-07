# CryptoClustering

## Analyzing Cryptocurrencies with K-Means and PCA 

This project uses K-Means clustering and Principal Component Analysis (PCA) to uncover patterns in cryptocurrency data.

**Key Steps:**

1. **Find the Best Value for k (Original Data)**
   * Use the elbow method to determine the optimal number of clusters ('k') on your original scaled dataset.
   * **Question:** What's the best 'k'? **4**

2. **Cluster Cryptocurrencies (Original Data)**
   * Initialize a K-Means model with the best 'k'.
   * Fit the model on the original scaled data.
   * Create a visualization to see the groupings.

3. **Optimize with PCA**
   * Perform PCA on the original scaled data.
   * Reduce features to 3 principal components.
   * **Question:** What is the total explained variance of these components? **89.5%**

4. **Find the Best Value for k (PCA Data)**
   * Repeat the elbow method with the PCA transformed data. 
   * **Questions:** What's the best 'k' now? Does it differ from before? **4 was the best choice again and did not change.**

5. **Cluster Cryptocurrencies (PCA Data)**
   * Initialize K-Means with the new best 'k' for PCA data.
   * Fit the model and visualize the clusters on your PCA components.
   * **Question:** How do the PCA clusters compare to the original clusters?

6. **Determine Feature Weights**
   * Create a DataFrame showing how much each original feature contributes to each principal component.
   * Identify the features with the strongest influence.
    
    PC1:

    * **Strongest Positive: price_change_percentage_200d**
    * **Strongest Negative: price_change_percentage_24h**

    PC2:

    * **Strongest Positive: price_change_percentage_30d**
    * **Strongest Negative: price_change_percentage_1y**

    PC3:

    * **Strongest Positive: price_change_percentage_7d**
    * **Strongest Negative: price_change_percentage_60d**

    
    **Resources**
* I relied heavely on the in class work on Module 11 Unsupervised Learning

    **Prerequisites**
* Python environment 
* Libraries: pandas, NumPy, matplotlib, scikit-learn 
* Cryptocurrency dataset


