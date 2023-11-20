# Predicting Missing Links in an Actor Co-occurence Network

Repository for Machine Learning in Network Science project to perform link prediction on an actor co-occurence network.

## Task
The goal is to accurately reconstruct the initial co-occurence network using both graph-theoretical and node feature information.

Two nodes represent actors and edges between two nodes stand for co-occurrence on the same Wikipedia page. This is a proxy for their joint participation in the same movie, for their personal relation, for their level of fame, etc. In addition to the graph structure, each node (i.e., actor) is also associated with textual information processed from its wikipedia page, from which some keywords were extracted.

The goal is to utilize information from both the underlying actor network and the processed wikipedia description in order to accurately predict missing edges.

## Dataset
The dataset comprises three files: a training set, a test set, and a node information file. The training set includes 10,000 labeled node pairs, while the test set contains 3,498 pairs. Node information consists of 932 features for each node, representing the textual information from each actor's Wikipedia page.

## Features
We utilized various similarity metrics based on node information, including:
1. Cosine similarity
2. Euclidean distance
3. Hamming distance
4. Manhattan distance
Additionally, we used graph-based features such as degree centrality, preferential attachment, and Jaccard similarity. Node embeddings were generated using the Node2Vec approach.

## Models Implemented
1. **Logistic Regression**: Two models with an L2 penalty and 'saga' solver, and one with Node2Vec embeddings.
2. **XGBoost**: Trained on both node and graph features along with embedded features.
3. **Unsupervised Learning Approaches**: Including MLPRegressor and similarity metrics like cosine, euclidean, and pearson distance.


## Model Evaluation
We evaluated the models using ROC AUC, precision, recall, and F1 score. Our evaluation process involved splitting the data into training, validation, and test sets. The best results were achieved using Logistic Regression models combined logically.

## Community Detection
We also applied the Greedy Modularity Algorithm for community detection, creating a feature to indicate whether the source and target nodes belong to the same community.

## Other Attempts
1. Principal Component Analysis (PCA) was used to reduce dimensionality.
2. Experimentation with different features and models to improve prediction quality.
