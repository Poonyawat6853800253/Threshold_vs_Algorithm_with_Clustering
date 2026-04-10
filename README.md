# Threshold_vs_Algorithm_with_Clustering
This project compares simple threshold-based grouping with clustering algorithms on India crime data. It applies KMeans, Agglomerative Clustering, and DBSCAN, evaluates them with silhouette scores, and uses PCA for visualization. Created to study clustering quality and compare rule-based vs algorithmic grouping.

# Threshold vs Clustering Algorithms on Crime Data

This project compares a simple threshold-based grouping approach with clustering algorithms on crime-related data. The notebook uses state-level property crime statistics from India and evaluates how different grouping methods separate the data.

## Purpose
This notebook was created to explore the difference between:
- **manual rule-based grouping** using a threshold
- **unsupervised learning methods** using clustering algorithms

The goal is to understand whether a simple threshold on one feature can perform as well as clustering methods that consider multiple features together.

## What the project does
- Loads and preprocesses crime data
- Aggregates crime statistics by state/area
- Selects key numerical features:
  - Cases of property stolen
  - Value of property stolen
  - Cases of property recovered
  - Value of property recovered
- Standardizes the features
- Applies multiple grouping methods:
  - Threshold-based split
  - KMeans
  - Agglomerative Clustering
  - DBSCAN
- Compares methods using **Silhouette Score**
- Uses **Elbow Method** to inspect possible values of k
- Optimizes:
  - the number of clusters for KMeans
  - the threshold value for manual grouping
- Visualizes clusters using **PCA**

## Methods Compared

### 1. Threshold-based grouping
A simple rule is created using a threshold on one selected feature.  
This is useful as a baseline because it is easy to understand, but it may ignore relationships among multiple variables.

### 2. KMeans
Partitions the data into k clusters by minimizing within-cluster distance.  
This method is useful when the data has relatively compact groups.

### 3. Agglomerative Clustering
Builds clusters hierarchically by merging similar groups step by step.  
This helps show structure without relying on centroid updates like KMeans.

### 4. DBSCAN
Groups points based on density and can identify noise points.  
This is useful when cluster shapes are irregular or when outliers may exist.

## Evaluation
The main evaluation metric used is:

- **Silhouette Score**

This score measures how well-separated the clusters are:
- higher score = better separation
- lower score = more overlap between groups

## Visualization
The notebook includes:
- feature histograms
- boxplots
- elbow method plot
- PCA projection of clustered states
- scree plot
- PCA loadings
- cluster separation plots

## Why this project is useful
This project is useful for:
- learning the difference between rule-based and algorithmic grouping
- understanding clustering performance on real-world data
- studying how feature scaling affects clustering
- comparing clustering algorithms with a simple baseline
- practicing evaluation and visualization of unsupervised learning models

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## Dataset
- India crime dataset
- Focused on property stolen and recovered statistics by area/state

## Key Learning Outcome
A simple threshold may be easy to interpret, but clustering algorithms can often capture richer structure because they use multiple features together. This notebook helps demonstrate when algorithmic clustering provides better grouping than a manual threshold rule.

## Future Improvements
Possible extensions:
- test more crime categories
- compare more clustering methods
- use additional validation metrics
- apply dimensionality reduction before clustering
- experiment with feature selection and outlier handling
