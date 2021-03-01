# Deep Retrieval: An End-to-End Learnable Structure Model for Large-Scale Recommendations
## summary
- 问题：用户和商品，线性时间、有效、精确召回，第一步，内积模型，第二步，最大内积搜索（maximum inner product search MIPS）。内积和检索分离的二步方案，优化目标不一致。
- 解决：端到端；代替树结构，采用空间结构矩阵D\*K，每条路径表示一个或者多个商品，只要利用正向样本（如用户和点击的商品）学习空间结构的节点向量和每个softmax的参数矩阵。 
- code：https://aka.ms/ance
- url：https://arxiv.org/pdf/2007.00808

## recommendation
- collaborative filtering: User-CF, Item-CF
- vector-based recommendation：MF, FM, DeepFM, FFM。内积表示匹配，检索/推理，采用maximum inner product search MIPS 或者 approximate nearest neibhbors ANN。如tree-based[1][2], locality sensitive hashing LSH[3][4], product quantization PQ[5][6], hierarchical navigable small world graphs HNSW[7]。

## references
- [1] Scalable nearest neighbor algorithms for high dimensional data, 2014.
- [2] Rank-based similarity search: Reducing the dimensional dependence, 2014.
- [3] Asymmetric lsh (alsh) for sublinear time maximum inner product search (mips), 2014.
- [4] A new unbiased and efficient class of lsh-based samplers and estimators for partition function compuration in log-linear models, 2017.
- [5] Product quantization for nearest neighbor search, 2010.
- [6] Optimized product quantization, 2013.
- [7] Efficient and robust approximate nearest neighbor search using heirarchical navigable small world graphs, 2018.
