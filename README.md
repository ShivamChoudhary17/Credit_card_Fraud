# Credit_card_Fraud

> - _______________________________________________________________________________________________________________________________________________________________________________

![](https://www.xenonstack.com/wp-content/uploads/xenonstack-credit-card-fraud-detection.png)

> - _______________________________________________________________________________________________________________________________________________________________________________

### [DataSet](https://www.kaggle.com/mlg-ulb/creditcardfraud)
> - _______________________________________________________________________________________________________________________________________________________________________________
### Content
The datasets contains transactions made by credit cards in September 2013 by european cardholders.
This dataset presents transactions that occurred in two days, where we have **492 frauds out of 284,807 transactions**. The dataset is **highly unbalanced**, the positive class (frauds) account for 0.172% of all transactions.

It contains only numerical input variables which are the result of a PCA transformation. Unfortunately, due to confidentiality issues, we cannot provide the original features and more background information about the data. Features **V1, V2, … V28 are the principal components obtained with PCA**, the only features which have **not been transformed with PCA are 'Time' and 'Amount'**. Feature 'Time' contains the seconds elapsed between each transaction and the first transaction in the dataset. The feature 'Amount' is the transaction Amount, this feature can be used for example-dependant cost-senstive learning. **Feature 'Class' is the response** variable and it takes value **1 in case of fraud and 0 otherwise**.

> - _______________________________________________________________________________________________________________________________________________________________________________

### Machine Learning-Based Approaches
Below is a brief overview of popular machine learning-based techniques for anomaly detection.

> Density-Based Anomaly Detection
Density-based anomaly detection is based on the k-nearest neighbors algorithm.

Assumption: Normal data points occur around a dense neighborhood and abnormalities are far away.

The nearest set of data points are evaluated using a score, which could be Eucledian distance or a similar measure dependent on the type of the data (categorical or numerical). They could be broadly classified into two algorithms:

. K-nearest neighbor: k-NN is a simple, non-parametric lazy learning technique used to classify data based on similarities in distance metrics such as Eucledian, Manhattan, Minkowski, or Hamming distance.

. Relative density of data: This is better known as local outlier factor (LOF). This concept is based on a distance metric called reachability distance.

> Clustering-Based Anomaly Detection
Clustering is one of the most popular concepts in the domain of unsupervised learning.

Assumption: Data points that are similar tend to belong to similar groups or clusters, as determined by their distance from local centroids.

. K-means is a widely used clustering algorithm. It creates 'k' similar clusters of data points. Data instances that fall outside of these groups could potentially be marked as anomalies.

> Support Vector Machine-Based Anomaly Detection
A support vector machine is another effective technique for detecting anomalies.
A SVM is typically associated with supervised learning, but there are extensions (OneClassCVM, for instance) that can be used to identify anomalies as an unsupervised problems (in which training data are not labeled).
The algorithm learns a soft boundary in order to cluster the normal data instances using the training set, and then, using the testing instance, it tunes itself to identify the abnormalities that fall outside the learned region.
Depending on the use case, the output of an anomaly detector could be numeric scalar values for filtering on domain-specific thresholds or textual labels (such as binary/multi labels).
In this jupyter notebook we are going to take the credit card fraud detection as the case study for understanding this concept in detail using the following Anomaly Detection Techniques namely

> Isolation Forest Anomaly Detection Algorithm
Isolation forest detects anomalies by randomly partitioning the domain space. Yeah, you’re heard me right- It works similar to Decision trees algorithm, where we start with a root node and keep on partitioning the space. In Isolation forest we partition randomly, unlike Decision trees where the partition is based on Information gain.
Partitions are created by randomly selecting a feature and then randomly creating a split value between the maximum and the minimum value of the feature. We keep on creating the partitions until we isolate all the points(in most cases we also set a limit on number of partitions/height of the tree).
> Density-Based Anomaly Detection (Local Outlier Factor)Algorithm
> Support Vector Machine Anomaly Detection Algorithm
