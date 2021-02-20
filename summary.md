# focal loss
- 对于正样本，预测概率越小的样本，会乘以更大的权重，扩大loss；对于负样本，预测概率越大的样本，会乘以更大的权重，扩大loss；即对低预测概率样本进行加权，提高预测概率。
- 正样本：![](https://latex.codecogs.com/svg.latex?-(1-y_p)\log(y_p))
- 负样本: ![](https://latex.codecogs.com/svg.latex?-y_p\log(1-y_p))

# logit adjustment loss
- 概率建模互信息，loss采用交叉熵
- https://zhuanlan.zhihu.com/p/158638078
