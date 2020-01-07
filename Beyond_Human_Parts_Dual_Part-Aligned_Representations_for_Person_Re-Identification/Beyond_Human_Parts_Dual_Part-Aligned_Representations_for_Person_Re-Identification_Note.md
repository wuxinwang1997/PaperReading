# Beyond Human Parts: Dual Part-Aligned Representations for Person Re-Identification

论文地址：http://arxiv.org/abs/1910.10111

本文针对人体部件的attention提出一种self-attention机制，可以解决part-misaligned的问题

使用人体解析模型CE2P构建dual part-aligned block(DPB)对ResNet50每个stage的输出进行一次操作再输入下一个stage，对特征图进行了信息增强

![Fig2](Fig2.png)

DPB包括两个分支，一个分支获取K个人体部件mask，一个分支获取N个潜在相关的部件mask，最后再叠加到stage的特征图中

![Table5](Table5.png)