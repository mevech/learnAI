# Indexing for Efficient Search

A raw collection of vectors is inefficient to search. Indexing creates a structure that allows for rapid retrieval of the most relevant vectors without comparing the query to every single vector in the database. Once you have your chunks, they are converted into vector embeddings. The vector store then needs to index these embeddings for fast retrieval. The choice of indexing strategy is a trade-off between search speed, accuracy, and storage cost.

## Indexing Approaches

### Flat Index (Brute-Force/Exact Search)
This is the most basic approach, where the query vector is directly compared to every other vector in the database. It guarantees finding the absolute nearest neighbors (most similar vectors) but is very slow for large datasets.

### Approximate Nearest Neighbor (ANN) Search
For large datasets, exact search is impractical. ANN algorithms provide a highly efficient way to find "good enough" matches without the computational overhead. Common ANN indexing techniques include:

#### Inverted File (IVF) Index
This method clusters the vectors and creates a "list" of vectors for each cluster (or only searches within the clusters closest to the query vector). When a search is performed, the query vector is first compared to the cluster centroids, and then only the vectors within the most similar clusters are searched. This significantly speeds up the process and offers a good balance of speed and accuracy.

#### Locality-Sensitive Hashing (LSH)
LSH uses hash functions to group similar vectors together. It's very fast for high-dimensional data but can sometimes be less accurate than other methods.

#### Hierarchical Navigable Small World (HNSW) Index
This is a more complex but highly efficient graph-based indexing technique. It builds a multi-layered graph where vectors are nodes, and edges connect similar vectors. The top layers have long-range connections for quick navigation, and the bottom layers have short-range connections for fine-grained search. HNSW is known for its excellent balance of search speed and accuracy, making it a very popular choice for vector databases.
