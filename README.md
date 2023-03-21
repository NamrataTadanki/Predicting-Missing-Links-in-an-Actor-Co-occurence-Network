# Predicting Missing Links in an Actor Co-occurence Network

Repository for Machine Learning in Network Science project to perform link prediction on an actor co-occurence network.

## Task
The goal is to accurately reconstruct the initial co-occurence network using both graph-theoretical and node feature information.

Two nodes represent actors and edges between two nodes stand for co-occurrence on the same Wikipedia page. This is a proxy for their joint participation in the same movie, for their personal relation, for their level of fame, etc. In addition to the graph structure, each node (i.e., actor) is also associated with textual information processed from its wikipedia page, from which some keywords were extracted.

The goal is to utilize information from both the underlying actor network and the processed wikipedia description in order to accurately predict missing edges.
