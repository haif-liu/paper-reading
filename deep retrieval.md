
# Approximate nearest neighbor negative contrastive learning for dense text retrieval
## dense retrieval vs sparse retrieval
- 难点：负样本（不相关文档数量远远多于相关文档）负样本negative sampling
- base：基于BM25检索的文档集，进行负样本采样[1]
- constrastive learning：在local mini-batches内采样负例[2][3][4]

## references
- [1] Sparse, dense, and attentional representations for text retrieval, 2020.
- [2] Representation learning with contrastive predictive coding, 2018.
- [3] A simple framework for contrastive learning of visual representations, 2020.
- [4] Dense passage retrieval for open-domain question answering, 2020.
