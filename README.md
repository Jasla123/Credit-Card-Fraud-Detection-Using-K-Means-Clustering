# Credit-Card-Fraud-Detection-Using-K-Means-Clustering

Project Overview:

This project uses K-Means Clustering, an unsupervised machine learning technique, to detect anomalous (potentially fraudulent) credit card transactions.
Since fraudulent transactions are very rare compared to normal transactions, credit card fraud detection can be treated as an anomaly detection problem.
The top 1% of transactions with the largest distance from their cluster centroid are identified as anomalies.
_ _ _

Objective:

To use K-Means clustering to identify anomalous credit card transactions and evaluate how well the detected anomalies match the actual fraudulent transactions.
_ _ _

Dataset:

The dataset contains credit card transactions with:
284,807 transactions
31 columns
Time
V1 to V28
Amount
Class


Data set link:  https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud⁠�
_ _ _

Class:

0 → Normal transaction
1 → Fraudulent transaction
The dataset is highly imbalanced because fraudulent transactions are very rare.
_ _ _

Technologies Used:

Python
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn
Jupyter Notebook

_ _ _ 

Methodology:

1. Data Understanding
   
Loaded the dataset

Checked dataset shape

Examined column names and data types

Checked missing values

Analyzed the distribution of the Class column

2. Data Preprocessing
 
 Removed Time from the clustering features
 
 Removed Class from the training data
 
 Selected V1 to V28 and Amount
 
 Applied StandardScaler for feature scaling

3. K-Means Clustering
   
 Used the Elbow Method to determine the number of clusters
 
 Selected K = 4
 
 Trained the K-Means clustering model
 
 Assigned each transaction to a cluster

4. Anomaly Detection

 Calculated the distance of each transaction from its assigned cluster centroid
 
 Used the 99th percentile as the anomaly threshold
 
 Identified the top 1% farthest transactions as anomalies

5. Evaluation
 
 The detected anomalies were compared with the actual fraud labels using:
 
 Confusion Matrix
 
 Precision
 
 Recall

6. Visualization

PCA was used to reduce the features to two dimensions.

Visualizations include:

 Elbow Method
 
 K-Means Clusters
 
 Anomalies vs Normal Transactions
 
 Confusion Matrix
_ _ _ 

Evaluation Metrics:


 Precision:
 
Precision measures how many of the transactions predicted as anomalies were actually fraudulent.

Recall:

Recall measures how many of the actual fraudulent transactions were successfully detected as anomalies.

_ _ _

Key Insights:

 The dataset is highly imbalanced.
 
 Fraudulent transactions represent only a very small portion of the dataset.
 
 K-Means was applied without using the Class column during training.
 
 Transactions farther from their cluster centroids were considered more likely to be anomalous.
 
 The top 1% farthest transactions were classified as anomalies.
 
 The detected anomalies were compared with actual fraud cases using Precision, Recall, and a Confusion Matrix.
 
 PCA helped visualize the clusters and detected anomalies in two dimensions.

 _ _ _

   
Conclusion:

K-Means clustering was successfully applied as an unsupervised anomaly detection technique for credit card transactions.
The model identified potentially unusual transactions based on their distance from cluster centroids. These detected anomalies were then compared with actual fraudulent transactions using a Confusion Matrix, Precision, and Recall.
Overall, K-Means can be used as an initial approach for detecting potentially fraudulent transactions, although some normal transactions may also be classified as anomalies.
