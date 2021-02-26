# Contrastive Learning (对比学习)
- 例子说明：一张真实的美元钞票，一张画出来的美元钞票，尽管不是一模一样，但是我们依旧可以轻易地辨别出钞票。这意味着，表示学习算法并不一定要关注到样本的每一个细节，只要学到的特征能够使其和其他样本区别开就行。
- 数据：一个样本x，有1个正例和N-1个负例
- 最终目标：![](https://latex.codecogs.com/svg.latex?s(f(x),f(x^+))>>s(f(x),f(x^-)))
- loss1：N个样本的交叉熵，InfoNCE，![](https://latex.codecogs.com/svg.latex?-\log(\frac{e^{f(x)^Tf(x^+)}}{e^{f(x)^Tf(x^+)}+e^{f(x)^Tf(x^-)}}))
- loss2：triplet loss，![](https://latex.codecogs.com/svg.latex?-y_p\log(1-y_p))


- contrastive representation learning: a framework and review

# CV
- Momentum Contrast for Unsupervised Visual Representation Learning
- A Simple Framework for Contrastive Learning of Visual Representations
- Representation Learning with Contrastive Predictive Coding

# NLP
- CERT: Contrastive Self-supervised Learning for Language Understanding
- Supervised Contrastive Learning for Pre-trained Language Model Fine-tuning
- Approximate Nearest Neighbor Negative Contrastive Learning for Dense Text Retrieval
