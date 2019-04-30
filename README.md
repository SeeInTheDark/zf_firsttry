# 关于slam的一些点
## 无监督
underwater环境与平常环境有所不同，难点如下，一是环境与空气环境不同，包含大量的noise，blur，haze。
另一方面，水下数据集几乎不可能有准确的label。因此，一个无监督的学习框架基本上是必须的。
* Unsupervised Learning of Depth and Ego-Motion from Video
这一篇论文比较早，2017年cvpr，然而后续的GEO-net用到了，所以一探究竟。
这里比较重要的geo-motion，其实就是个6Dof的转移矩阵。以及场景结构--其实就是深度图。一些场景比如纹理不明显的场景，往往导致错误的相机运动估计
以及深度图估计，因此真实世界的连续性假设可以使得训练的过程无监督。
网络输入为一小段视频片段。
