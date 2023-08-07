# Awesome-Federated-Learning [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
A curated list of resources on federated learning, especially focusing on the **theoretical** perspectives. 

**Note:**          
- This is a curated list of resources on federated learning that primarily focuses on the theoretical perspectives of distributed machine learning. Only a select few highly representative practical papers will be included. To the best of our knowledge, this is the first github repository that has this design. 
- The list is mainly sorted by topics instead of publishing year, although papers in each topic will be sorted chronologically.
- The list will not only include published papers, but will also cover selected unpublished arXiv papers.
- Note that this list does not cover every good paper in federated learning and emphasizes interesting papers that the author has read. Necessary comments will be added to some papers. As such, this list may contain personal biases and preferences.
- The list will be continuously updated to include the latest developments in federated learning research.

## Contents
- [Local Training (LT) Methods](#lt-methods)
  -  [First Generation (Heuristic)](#lt-heuristic)
  -  [Second Generation (Homogeneous)](#lt-homogeneous)
  -  [Third Generation (Sublinear)](#lt-sublinear)
  -  [Fourth Generation (Linear)](#lt-linear)
  -  [Fifth Generation (Accelerated)](#lt-accelerated)
-  [Personalized Federated Learning](#todo)

## Local Training (LT) Methods
The main idea behind Local Training (LT) is to optimize the local model multiple times and then aggregate the final local output to the server. LT is an efficient technique that helps reduce the communication complexity in distributed machine learning. Over time, researchers have developed various generations of local training methods, starting from simple empirical approaches and evolving to sophisticated techniques that offer better communication complexity than gradient descent (GD) under standard assumptions. For instance, ProxSkip-VR provides insights into the five generations of local training methods. 

### First Generation (Heuristic)
This generation only contains empirical results. 

- **LocalSGD:** Daniel Povey, Xiaohui Zhang, and Sanjeev Khudanpur. Parallel training of DNNs with natural gradient and parameter averaging. ICLR Workshop, 2015. 
- **SparkNet:** Philipp Moritz, Robert Nishihara, Ion Stoica, and Michael I. Jordan. SparkNet: Training deep networks in Spark. ICLR, 2016.
- **FedAvg:** H Brendan McMahan, Eider Moore, Daniel Ramage, Seth Hampson, and Blaise Agüera y Arcas. Communication-efficient learning of deep networks from decentralized data. AISTATS, 2017.

### Second Generation (Homogeneous)
The algorithms in this generation have theories but they are built on top of very strict assumptions that violate the motivation of federated learning. We will elaborate with specific papers. 

- **FedAvg:** Xiang Li, Kaixuan Huang, Wenhao Yang, Shusen Wang, and Zhihua Zhang. On the convergence of FedAvg on non-IID data. ICLR, 2020.
- **LFGD:** Farzin Haddadpour and Mehrdad Mahdavi. On the convergence of local descent methods in federated learning. arXiv, 2019.

### Third Generation (Sublinear)
This generation has standard assumptions, including strong convexity and smoothness, but the communication complexity rate is sublinear. 

- **LGD:** Ahmed Khaled, Konstantin Mishchenko, and Peter Richtárik. The first analysis of local GD on heterogeneous data. In NeurIPS Workshop on Federated Learning for Data Privacy and Confidentiality, 2019.
- **LSGD:** Ahmed Khaled, Konstantin Mishchenko, and Peter Richtárik. Tighter theory for local SGD on identical and heterogeneous data. AISTATS, 2020.

### Fourth Generation (Linear)
This generation has linear communication complexity under standard assumptions, but the rate is worse than GD.

- **Scaffold:** Sai Karimireddy, Satyen Kale, Mehryar Mohri, Sashank Reddi, Sebastian Stich, and Ananda Suresh. SCAFFOLD: Stochastic controlled averaging for on-device federated learning. ICML, 2020.
- **S-Local-GD:** Eduard Gorbunov, Filip Hanzely, and Peter Richtárik. Local SGD: unified theory and new efficient methods. NeurIPS, 2020.
- **FedLin:** Aritra Mitra, Rayana Jaafar, George Pappas, and Hamed Hassani. Linear convergence in federated learning: Tackling client heterogeneity and sparse gradients. NeurIPS, 2021.

### Fifth Generation (Accelerated)
This generation, the most recent one, successfully achieved an accelerated communication complexity rate, which is better than GD. 
- **Scaffnew:** Konstantin Mishchenko, Grigory Malinovsky, Sebastian Stich, and Peter Richtárik. ProxSkip: Yes! Local gradient steps provably lead to communication acceleration! Finally. ICML, 2022.
- **ProxSkip-VR:** Grigory Malinovsky, Kai Yi, and Peter Richtárik. Variance reduced proxskip: Algorithm, theory, and application to federated learning. NeurIPS, 2022.
- **5GCS:** Michał Grudzien, Grigory Malinovsky, and Peter Richtárik. Can 5th-generation local training methods support client sampling? yes!. AISTATS, 2023. 
- **CompressedScaffnew:** Laurent Condat, Ivan Agarsky, and Peter Richtárik. Provably doubly accelerated federated learning: The first theoretically successful combination of local training and compressed communication. arXiv, 2022.
- **GradSkip:** Artavazd Maranjyan, Mher Safaryan, and Peter Richtárik. Gradskip: Communication-accelerated local gradient methods with better computational complexity. arXiv, 2022.
- **Scafflix:** Kai Yi, Laurent Condat, Peter Richtárik. Explicit Personalization and Local Training: Double Communication Acceleration in Federated Learning. [[paper]](https://arxiv.org/abs/2305.13170) [[code]](https://github.com/WilliamYi96/Scafflix)

## Personalized Federated Learning
- **pFedGate:** Daoyuan Chen, Liuyi Yao, Dawei Gao, Bolin Ding, Yaliang Li. Efficient Personalized Federated Learning via Sparse Model-Adaptation. *ICML23*. (bounded diversity) [[paper]](https://arxiv.org/abs/2305.02776) [[code (no implementation of pFedGate)]](https://github.com/alibaba/FederatedScope/)
- **FedCR:** Hao Zhang, Chenglin Li, Wenrui Dai, Junni Zou, Hongkai Xiong. FedCR: Personalized Federated Learning Based on Across-Client Common Representation with Conditional Mutual Information Regularization. *ICML23*. [[paper(not standard convergence theory)]](https://openreview.net/pdf?id=YDC5jTS3LR) [[code]](https://github.com/haozzh/FedCR)
- **pFedGraph:** Rui Ye, Zhenyang Ni, Fangzhao Wu, Siheng Chen, Yanfeng Wang. Personalized Federated Learning with Inferred Collaboration Graphs. *ICML23*. [[paper(no theory) ]](https://openreview.net/forum?id=33fj5Ph3ot) [[code (under preparation)]](https://github.com/MediaBrain-SJTU/pFedGraph)
- **FED-PUB:** Jinheon Baek, Wonyong Jeong, Jiongdao Jin, Jaehong Yoon, Sung Ju Hwang. Personalized Subgraph Federated Learning. *ICML23*. [[paper(no theory)]](https://arxiv.org/pdf/2206.10206.pdf) [[code (not standard datasets)]](https://github.com/JinheonBaek/FED-PUB)
- **FedGMM:** Yue Wu, Shuaicheng Zhang, Wenchao Yu, Yanchi Liu, Quanquan Gu, Dawei Zhou, Haifeng Chen, Wei Cheng. [[paper (no standard convergence theory)]](https://arxiv.org/pdf/2305.01068.pdf) [[no code]]
- **PerFedMask:** Mehdi Setayesh, Xiaoxiao Li, Vincent W.S. Wong. PerFedMask: Personalized Federated Learning with Optimized Masking Vectors. *ICLR23*. (bounded variance) [[paper]](https://openreview.net/forum?id=hxEIgUXLFF) [[code]](https://github.com/MehdiSet/PerFedMask)
- **FedPAC:** Jian Xu, Xinyi Tong, Shao-Lun Huang. Personalized Federated Learning with Feature Alignment and Classifier Collaboration. *ICLR23*[[paper]](https://openreview.net/forum?id=SXZr8aDKia) [[code]](https://github.com/JianXu95/FedPAC)
- **AdaMix/AdaPeD:** Kaan Ozkara, Antonious M. Girgis, Deepesh Data, Suhas Diggavi. A Statistical Framework for Personalized Federated Learning and Estimation: Theory, Algorithms, and Privacy. *ICLR23*. [[paper]](https://openreview.net/forum?id=FUiDMCr_W4o) [[no code]]()
