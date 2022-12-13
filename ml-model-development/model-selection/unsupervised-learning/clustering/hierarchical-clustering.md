# Hierarchical Clustering

### What is it?

Hierarchical clustering is a type of clustering algorithm that creates a hierarchy of clusters, where each cluster is defined as a group of data points that are more similar to each other than they are to points in other clusters. This hierarchy of clusters is represented as a tree-like structure, with the clusters at the bottom of the tree being the most specific (i.e. containing the smallest number of data points) and the clusters at the top of the tree being the most general (i.e. containing the largest number of data points). Hierarchical clustering algorithms typically use a measure of similarity, such as Euclidean distance, to determine how similar two data points are, and then iteratively merge the most similar clusters until a hierarchy of clusters is formed. There are two main types of hierarchical clustering: agglomerative, which starts with each data point in its own cluster and merges clusters together, and divisive, which starts with all data points in a single cluster and divides the cluster into smaller sub-clusters.

### How does it work?

The hierarchical clustering algorithm works by iteratively merging the most similar clusters until a hierarchy of clusters is formed. Here is how it works in more detail:

1. The algorithm starts by considering each data point as its own cluster. This means that if we have N data points, there will be N initial clusters.
2. The algorithm then computes the similarity between each pair of clusters, using some measure of similarity such as the Euclidean distance between the points in each cluster.
3. The algorithm then merges the two most similar clusters into a single cluster, creating a new cluster that contains the points from both of the original clusters.
4. The algorithm repeats steps 2 and 3 until there is only a single cluster left, at which point the algorithm stops and the hierarchy of clusters is complete.

This process results in a hierarchy of clusters, where each cluster is defined as a group of data points that are more similar to each other than they are to points in other clusters. The hierarchy is represented as a tree-like structure, with the clusters at the bottom of the tree being the most specific (i.e. containing the smallest number of data points) and the clusters at the top of the tree being the most general (i.e. containing the largest number of data points). This allows us to analyze the relationships between the data points at different levels of the hierarchy, and to identify natural groupings in the data.

### Example

Here is a simple example of how hierarchical clustering might be used to group a collection of documents into clusters based on their similarity:

```python
# Import the required libraries
from sklearn.feature_extraction.text import TfidfVectorizer
from scipy.cluster.hierarchy import dendrogram, linkage

# Load the data
documents = ["this is a sentence",
             "this is another sentence",
             "yet another sentence",
             "this is the final sentence"]

# Use the TfidfVectorizer to compute the tf-idf vectors for each document
vectorizer = TfidfVectorizer()
vectors = vectorizer.fit_transform(documents)

# Use the linkage function to compute the distances between clusters
Z = linkage(vectors.toarray(), method="ward")

# Plot the dendrogram
plt.figure()
dendrogram(Z)
plt.show()
```

This code will first use the TfidfVectorizer to compute the tf-idf vectors for each document in the collection, which will represent the relative importance of each word in each document. It will then use the linkage function to compute the distances between the documents based on their tf-idf vectors, and then plot a dendrogram showing the hierarchy of clusters. The dendrogram will show how the documents are grouped into clusters at different levels of the hierarchy, with the most similar documents being grouped together first and the least similar documents being grouped together last. In this example, you should see four clusters at the bottom of the dendrogram, with each cluster containing documents that contain similar words and phrases.
