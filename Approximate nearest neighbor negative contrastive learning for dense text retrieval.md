
# Approximate nearest neighbor negative contrastive learning for dense text retrieval
## summary
- 问题：uninformative negatives sampled locally in batch, 导致yield diminishing gradient norms, large stochastic gradient variances, slow learning convergence。
- 解决：提出approximate nearest neighbor negative contrastive learning (ANCE)，一种学习机制，用于从全部语料中选择hard training negatives。
- 实验：web search，question answering，commercial search
- code：https://aka.ms/ance
- url：https://arxiv.org/pdf/2007.00808

## dense retrieval vs sparse retrieval
- 难点：负样本（不相关文档数量远远多于相关文档）负样本negative sampling
- base：基于BM25检索的文档集，进行负样本采样[1]
- constrastive learning：在local mini-batches内采样负例[2][3][4]

## sparse retrieval
- term weighting [5]
- query expansion [6]
- document expansion [7]

## ANCE
- 在第k步，基于第k-1步的模型，采用ANN在所有语料文档上召回query的相关文档，并提出真是的相关文档，构成负例（hard negatives），训练第k步的模型
- 特点：每步采用的是global negagives

## references
- [1] Sparse, dense, and attentional representations for text retrieval, 2020.
- [2] Representation learning with contrastive predictive coding, 2018.
- [3] A simple framework for contrastive learning of visual representations, 2020.
- [4] Dense passage retrieval for open-domain question answering, 2020.
- [5] Deeper text understanding for ir with contextual neural language modeling, 2019.
- [6] Bert-qe: contextualized query expansion for document re-ranking, 2020.
- [7] Passage re-ranking with bert, 2019.
