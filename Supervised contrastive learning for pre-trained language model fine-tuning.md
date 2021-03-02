# Supervised contrastive learning for pre-trained language model fine-tuning
## summary
- 问题：cross entroyp可能导致sub-optimal generalization and instability
- intuition：good generalization requires capturing the similarity between examples in one class and contrasting them with examples in other class
- idea：supervised contrastive learning (SCL) loss + cross entropy loss
- 结论：对比roberta-large，glue效果更好

## schema
- ![](https://latex.codecogs.com/svg.latex?L=(1-\lambda)%20\cdot%20L_{CE}%20+%20\lambda%20L_{SCL})
- ![](https://latex.codecogs.com/svg.latex?L_{CE}%20=%20-\frac{1}{N}%20\sum_{i=1}^{N}y_i%20\cdot%20\log(\hat{y_i})%20+%20(1-y_i)%20\cdot%20\log(1-\hat{y_i}))
- ![](https://latex.codecogs.com/svg.latex?L_{SCL}%20=%20\sum_{i=1}^{N}-\frac{1}{N_{y_i}-1}%20\sum_{j=1}^{N}%20\mathbf{1_{i%20\neq%20j}}%20\mathbf{1_{y_i%20\neq%20y_j}}%20\log\frac{\exp(\Phi(x_i)%20\cdot%20\Phi(x_j)%20/%20\tau)}{\sum_{k=1}^{N}\mathbf{1_{i%20\neq%20k}}\exp(\Phi(x_i)%20\cdot%20\Phi(x_k)%20/%20\tau)})
