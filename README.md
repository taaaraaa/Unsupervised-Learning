# mini-project-III
Repo with the instructions for the Mini Project III.


### Topics
This mini project is dedicated to following topics:
- Data Wrangling
- Data Visualization
- Data Preparation and Feature Engineering
- Dimensionality Reduction
- Unsupervised Learning

### Data
We will be using old data about different financial transactions. You can download the data from [here](https://drive.google.com/file/d/1zAjnf936aHkwVCq_BmA47p4lpRjyRzMf/view?usp=sharing). The data contains following tables:

- twm_customer - information about customers
- twm_accounts - information about accounts
- twm_checking_accounts - information about checking accounts (subset of twm_accounts)
- twm_credit_accounts - information about checking accounts (subset of twm_accounts)
- twm_savings_accounts - information about checking accounts (subset of twm_accounts)
- twm_transactions - information about financial transactions
- twm_savings_tran - information about savings transactions (subset of twm_transactions)
- twm_checking_tran - information about savings transactions (subset of twm_transactions)
- twm_credit_tran - information about credit checking (subset of twm_transactions)


### Output

In this miniproject, we will:

1.  create two separate customer segmentations (using clustering) to split them into 3-5 clusters: 
    - based on demographics (only on the information from twm_customer)
    - based on their banking behavior. We can take following things into consideration as banking behavior:
        - do they have savings account? How much do they save?
        - do they have credit account? How much do they live in debt?
        - are they making lot of small transactions or few huge ones?
2. visualize the created clusters using [radar charts](https://plotly.com/python/radar-chart/) and compare them agains each other
3. visualize segmentations using scatter plot. We will have to use PCA to be able to plot our observations in 2D.
4. (stretch) visualize in 2D how our clusters are evolving in each iteration of KMeans (for at least 20 iterations).
    - we will need to create own implementation of kmeans so we can see what is happening with the clusters during the iterations.


### Goal:
The purpose of this project is to group a large dataset of customer data into distinct segments based on their demographics and transaction behavior.
Data Preprocessing:
The dataset was used contained a bank customer records in nine separate tables, including information on their age, gender, marital status, location, income and banking history. We aggregated the tables and preprocessed the data by removing any missing values, handling outliers, encoding categorical variables and standardizing the numerical variables.

### Methodology:
To perform the clustering, we used the K-means++ algorithm with different values of k and evaluated the results using Elbow plot for model inertia  and also the silhouette score. After experimenting with different values of k, we settled on a value of k=3, which provided the best balance of cluster separation and interpretability.

### Clustering Results:
 The clustering results showed clear separation between the three clusters. Each cluster had distinct characteristics in terms of age, gender, location, and banking behavior. 

### PC Analysis:
Once the clusters were identified, PCA was performed on the dataset to reduce the dimensionality of the data while retaining as much of the original variation as possible. The first two principal components were used to create a 2D scatter plot that visualized the clusters.
The PCA reduced the dimensionality of the dataset to two principal components, which explained approximately 80% of the total variation in the data. The 2D scatter plot showed clear separation between the three clusters, with each cluster having its own distinct pattern of customer behavior.
The results of the PCA and clustering analysis provided valuable insights into the customer and their behavior. The 2D scatter plot allowed for a clear visualization of the clusters and their distinct characteristics. 

### Radar Chart:
We also plotted radar chart for different clusters. It can be seen the average of customer saving is about $1200. 


