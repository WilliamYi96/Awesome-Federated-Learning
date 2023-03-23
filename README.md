# Awesome-Federated-Learning [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
A curated list of resources on federated learning, especially focusing on the **theoretical** perspectives. 

**Note:**          
- This is a curated list of resources on federated learning that primarily focuses on the theoretical perspectives of distributed machine learning. Only a select few highly representative practical papers will be included. To the best of our knowledge, this is the first github repository that has this design. 
- The list is mainly sorted by topics instead of publishing year, although papers in each topic will be sorted chronologically.
- The list will not only include published papers, but will also cover selected unpublished arXiv papers.
- Note that this list does not cover every good paper in federated learning and emphasizes interesting papers that the author has read. Necessary comments will be added to some papers. As such, this list may contain personal biases and preferences.
- The list will be continuously updated to include the latest developments in federated learning research.

## Contents
- [Local Training (LT) Methods](#lt_methods)

## Local Training (LT) Methods
The main idea behind Local Training (LT) is to optimize the local model multiple times and then aggregate the final local output to the server. LT is an efficient technique that helps reduce the communication complexity in distributed machine learning. Over time, researchers have developed various generations of local training methods, starting from simple empirical approaches and evolving to sophisticated techniques that offer better communication complexity than gradient descent (GD) under standard assumptions. For instance, ProxSkip-VR provides insights into the five generations of local training methods. 

### First Generation (Heuristic)
This generation only contains the empirical results. 

- **LocalSGD:**
- **SparkNet:**
- **FedAvg:**

### Second Generation (Homogeneous)
The algorithms in this generation have theories but they are built on top of very strict assumptions that violate the motivation of federated learning. We will ellaborate with specific papers. 

- **FedAvg:**
- **LFGD:**

### Third Generation (Sublinear)
This generation has standard assumptions including strongly convexity and smoothness, but the communication complexity rate is sublinear. 

- **LGD:**
- **LSGD:**

### Fourth Generation (Linear)
This generation has linear communication complexity under standard assumptions but the rate is worse than GD.

- **Scaffold:**
- **S-Local-GD:**
- **FedLin:**

### Fifth Generation (Accelerated)
This generation, the most recent one, sucessfully achieved accelerated communication complexity rate which is better than GD. 
- **Scaffnew:**
- **ProxSkip-VR:**
