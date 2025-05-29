# Project: Influence of physics paper clustering on published journals using NLP and unsupervised learning

## Context and Problem Statement
- This project was performed to cluster physics papers based on their title and abstract in order to find the right journal for publication with high approval.
- The physics paper dataset was labelled by using clustering algorithms including K-means, Hierarchical agglomerative, Mean shift, and DBSCAN.
- Firstly, the textual data was converted to numerical data by using NLP techniques such as Tokenization, Vectorization, Removing stop words and punctuation, Stemming, and Lemmatization.
- Then, I visualized the most common words by using bar plot, tree plot and word cloud.
- Finally I used dimensionality reduction techniques for visualization.

## Data source
ArXiv dataset: - open access to scholarly articles in scientific fields (physics, mathematics, computer science, quantitative biology, quantitative finance, statistics, electrical engineering and systems science, and economics)
               - operated by Cornell University
               - provides only a metadata file in the json format

Features: - id: ArXiv ID (can be used to access the paper, see below)
          - submitter: Who submitted the paper
          - authors: Authors of the paper
          - title: Title of the paper
          - comments: Additional info, such as number of pages and figures
          - journal-ref: Information about the journal the paper was published in
          - doi: [https://www.doi.org](Digital Object Identifier)
          - abstract: The abstract of the paper
          - categories: Categories / tags in the ArXiv system
          - versions: A version history

## Algorithms
### 1. K-means
- K-means computes the distance between data points to shape the clusters.
- This algorithm is easy to implement and suitable for large datasets.

### 2. Hierarchical agglomerative
- Hierarchical agglomerative finds the closest pair and merges them into a cluster.
- This algorithm is suitable for many clusters with different sizes.

### 3. Mean shift
- Mean shift assigns points to the nearest cluster centroid. Centroid refers to a point of highest local density.
- This algorithm can find a lot of clusters with uneven sizes.

### 4. DBSCAN (Density-Based Spatial Clustering of Application with Noise)
- DBSCAN finds core points in high density regions and expands clusters from them. 
- Only points that are in a certain distance from the core points will be classified as belonging to a corresponding cluster, otherwise they will be classified as noise.
- This algorithm can find uneven cluster sizes and outliers. It can also be used for large datasets with non-flat geometry.

## Process
1. Import data
2. Perform EDA and feature engineering
3. Text preprocessing using NLP >>> tokenization, remove stop words and punctuation, stemming, lemmatization, and vectorization
4. Visualization of most common words by bar plot, tree plot and word cloud
5. Vectorization >>> convert text data into numerical data using TF-IDF matrix
6. Dimensionality reduction with Non-Negative Matrix Factorization (NMF)
7. Clustering using K-means
8. Clustering using Hierarchical agglomerative
9. Clustering using Mean shift
10. Clustering using DBSCAN
11. Visualization using t-SNE
12. Visualization using UMAP
