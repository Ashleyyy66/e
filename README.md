# Echo Classification Using Unsupervised Learning
This project aims at classifying sea ice and lead using Sentinel-3 data altimetry data. The echo classification will be quantified against the ESA official classification using a confusion matrix. The mean unsupervised classification methods used in this projects are K-means and Gaussian Mixture Methods (GMM) clustering.
## Introduction to Unsupervised Learning Methods ([Bishop, 2006](https://example.com)) Christopher M Bishop and Nasser M Nasrabadi. Pattern recognition and machine learning. Volume 4. Springer, 2006.
### Methods Used
- K-Means Clustering
- Gaussian Mixture Models (GMM)
- Confusion Matrix Evaluation
#### K-Means Clustering
K-means clustering is a type of unsupervised learning algorithm used for partitioning a dataset into a set of k groups (or clusters), where k represents the number of groups pre-specified by the analyst. It classifies the data points based on the similarity of the features of the data ([MacQueen and others, 1967])James MacQueen and others. Some methods for classification and analysis of multivariate observations. In Proceedings of the fifth Berkeley symposium on mathematical statistics and probability, volume 1, 281–297. Oakland, CA, USA, 1967.. The basic idea is to define k centroids, one for each cluster, and then assign each data point to the nearest centroid, while keeping the centroids as small as possible.
#### Why K-means for Clustering?
K-means clustering is particularly well-suited for applications where:

- **The structure of the data is not known beforehand:** K-means doesn’t require any prior knowledge about the data distribution or structure, making it ideal for exploratory data analysis.

- **Simplicity and scalability:** The algorithm is straightforward to implement and can scale to large datasets relatively easily.

#### Key Components of K-means
- **Choosing K**: The number of clusters (k) is a parameter that needs to be specified before applying the algorithm.

- **Centroids Initialization**: The initial placement of the centroids can affect the final results.

- **Assignment Step**: Each data point is assigned to its nearest centroid, based on the squared Euclidean distance.

- **Update Step**: The centroids are recomputed as the center of all the data points assigned to the respective cluster.

Here is my image:





![hi](RF_image2_sample3_22075867.png)

Isn’t it amazing?
