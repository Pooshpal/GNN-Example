# GNN-Example
An Example notebook

# Problem Statement
The Education Minister of India has access to the data of all engineering students in India. They want to gain insights on which Branch of Engineering is popular and which branch of engineering a new student might choose (or might have more demand) so that you can accordingly increase the intake for that branch. Instead of gaining insights from a boring table, you're given a fancy graph of the interaction between all students in the country and the courses they take :)

##### Your task is to predict which branch of engineering a particular student in the graph has taken.
# What you need to do :
Considering the above mentioned graph, there are few nodes who have are not labeled to have a class (As shown in the image 20% didn't have labels). You will have to predict the branch for the Node IDs present in sample_submission.csv. You will have to make a graph from the nodes and edges list provided in Data, run Traditional ML and Graph Learning techniques to classify their Branch, based on some attributes of the nodes which describe their connectivity between other students.

# General framework of steps to be followed:

1. Creating a networkx graph from a given edge list and node list
2. Generate features (ensure to save them as methods like node2vec, random walk etc. require high compute resources so you should not have to regenrate them)
3. Converting networkx graph to Pytorch geometric graph (or any other suitable format for your GNN)
4. For the pytorch geometric graph, add the features given in features.pt and concatenate any additional features you wish to generate
5. Use a GNN (ex: GCN) and train on the graph. Use the train and test masks as needed when defining the accuracy and to predict for the GNNs
6. The final output required is the prediction value of branch for the test nodes only

You are free to experiment with traditional ML using graph features as input, or using diff GNN architectures, etc.
