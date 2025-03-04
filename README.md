

# Echo Classification Using Unsupervised Learning
This project aims at classifying sea ice and lead using Sentinel-3 data altimetry data. The echo classification will be quantified against the ESA official classification using a confusion matrix. The mean unsupervised classification methods used in this projects are K-means and Gaussian Mixture Models (GMM) clustering.

![hi](classification.png)
## Introduction to Unsupervised Learning Methods ([Bishop, 2006])

### K-Means Clustering
K-means clustering is a type of unsupervised learning algorithm used for partitioning a dataset into a set of k groups (or clusters), where k represents the number of groups pre-specified by the analyst. It classifies the data points based on the similarity of the features of the data ([MacQueen and others, 1967]). The basic idea is to define k centroids, one for each cluster, and then assign each data point to the nearest centroid, while keeping the centroids as small as possible.
#### Why K-means for Clustering?
K-means clustering is particularly well-suited for applications where:

- **The structure of the data is not known beforehand:** K-means doesn’t require any prior knowledge about the data distribution or structure, making it ideal for exploratory data analysis.

- **Simplicity and scalability:** The algorithm is straightforward to implement and can scale to large datasets relatively easily.

#### Key Components of K-means
- **Choosing K**: The number of clusters (k) is a parameter that needs to be specified before applying the algorithm.

- **Centroids Initialization**: The initial placement of the centroids can affect the final results.

- **Assignment Step**: Each data point is assigned to its nearest centroid, based on the squared Euclidean distance.

- **Update Step**: The centroids are recomputed as the center of all the data points assigned to the respective cluster.

#### The Iterative Process of K-means
The assignment and update steps are repeated iteratively until the centroids no longer move significantly, meaning the within-cluster variation is minimised. This iterative process ensures that the algorithm converges to a result, which might be a local optimum.

#### Advantages of K-means
- **Efficiency**: K-means is computationally efficient.

- **Ease of interpretation**: The results of k-means clustering are easy to understand and interpret.

### Gaussian Mixture Models (GMM) [Bishop and Nasrabadi, 2006]
Gaussian Mixture Models (GMM) are a probabilistic model for representing normally distributed subpopulations within an overall population. The model assumes that the data is generated from a mixture of several Gaussian distributions, each with its own mean and variance [Reynolds and others, 2009]. GMMs are widely used for clustering and density estimation, as they provide a method for representing complex distributions through the combination of simpler ones.

#### Why Gaussian Mixture Models for Clustering?
Gaussian Mixture Models are particularly powerful in scenarios where:

- **Soft clustering is needed**: Unlike K-means, GMM provides the probability of each data point belonging to each cluster, offering a soft classification and understanding of the uncertainties in our data.

- **Flexibility in cluster covariance**: GMM allows for clusters to have different sizes and different shapes, making it more flexible to capture the true variance in the data.

#### Key Components of GMM
- **Number of Components (Gaussians)**: Similar to K in K-means, the number of Gaussians (components) is a parameter that needs to be set.

- **Expectation-Maximization (EM) Algorithm**: GMMs use the EM algorithm for fitting, iteratively improving the likelihood of the data given the model.

- **Covariance Type**: The shape, size, and orientation of the clusters are determined by the covariance type of the Gaussians (e.g., spherical, diagonal, tied, or full covariance).

#### The EM Algorithm in GMM
The Expectation-Maximization (EM) algorithm is a two-step process:

- **Expectation Step (E-step)**: Calculate the probability that each data point belongs to each cluster.

- **Maximization Step (M-step)**: Update the parameters of the Gaussians (mean, covariance, and mixing coefficient) to maximize the likelihood of the data given these assignments.

This process is repeated until convergence, meaning the parameters do not significantly change from one iteration to the next.

#### Advantages of GMM
- **Soft Clustering**: Provides a probabilistic framework for soft clustering, giving more information about the uncertainties in the data assignments.

- **Cluster Shape Flexibility**: Can adapt to ellipsoidal cluster shapes, thanks to the flexible covariance structure.

## Before getting started...
### Installation

Below are the packages needed for this project:

```bash
!pip install rasterio
!pip install netCDF4
!pip install basemap
!pip install cartopy
```
### Mount Google Colab to Google drive
```bash
from google.colab import drive # Mount to your own google drive
drive.mount('/content/drive')
```


## Contact

**Boxuan Li** - [zcqsbli@ucl.ac.uk](mailto:zcfbabi@ucl.ac.uk) / [ashleyyyy6615@gmail.com](mailto:ashleyyyy6615@gmail.com)

**Project Link:** [https://github.com/Ashleyyy66/e](https://github.com/Ashleyyy66/e)


## Acknowledgments
This project is Week4 assignment for module GEOL0069 in Earth Sciences department of UCL.


