## 行人重识别(Person Re-identification)
### 2019.10.20

**综述论文**：[A survey of approaches and trends in person re-identification](./A_survey_of_approaches_and_trends_in_person_re-identification/A_survey_of_approaches_and_trends_in_person_re-identification.pdf)

**笔记**：[A survey of approaches and trends in person re-identification Note](https://zhuanlan.zhihu.com/p/94554289)

**理解**：该论文是2014年的综述论文，没有涉及到深度学习的东西。行人重识别就是一个图像匹配的问题，对于传统方法，难点主要在于特征的选取，还有就是分类的度量方法也比较困难。

推荐一个综述：[知呼行人重识别专栏](https://zhuanlan.zhihu.com/p/26168232)

### 2019.10.21

**论文**：[Beyond Part Models Person Retrieval with Reﬁned Part Pooling](https://arxiv.org/pdf/1711.09349.pdf)

**笔记**：[Beyond Part Models Person Retrieval with Reﬁned Part Pooling Note](https://zhuanlan.zhihu.com/p/94576148)

**理解**：该论文是孙凡逸和郑良的一个基线代码的论文，对PCB算法进行了改进。针对人体特征，将CNN学习到的特征分为条带，然后使用Refined Part Pooling机制提高PCB模型的mAP。可以作为行人重识别的baseline

### 2019.10.29

**论文**：[Learning Discriminative Features with Multiple Granularities](https://arxiv.org/pdf/1804.01438.pdf)

**笔记**：[Learning Discriminative Features with Multiple Granularities Note](https://zhuanlan.zhihu.com/p/94576602)

**理解**：该论文集合全局特征与局部特征分三个分支学习，对于全局特征使用tripletloss，对于局部特征使用stride=1的策略保留细节，同时用softxmaxloss

### 2019.10.31

**论文**：[Pedestrian Alignment Network for Large-scale Person Re-identification](https://arxiv.org/pdf/1707.00408.pdf)

**笔记**：[Pedestrian Alignment Network for Large-scale Person Re-identification Note](https://zhuanlan.zhihu.com/p/94577169)

**理解**：该论文提出使用两个分支，一个用传统的CNN方法提取descriptor。一个先对浅层特征对准人物，双线性插值到原feature map大小，与高层特征网格化结合，再用变换矩阵纠正图像形态，然后提取descriptor。最后两个descriptor联合起来进行Re-ID。baseline是80%多的水平，所以最终效果也只是80%多，但是思路有借鉴意义

### 2019.12.1
**论文**：[Omni-Scale_ Feature Learning for Person Re-Identification](https://arxiv.org/pdf/1905.00953.pdf)

**笔记**：[Omni-Scale Feature Learning for Person Re-Identification Note](https://zhuanlan.zhihu.com/p/94577433)

**理解**：采用卷积分解降低计算复杂度，多流处理达到全尺度特征学习的目的。在ReID等任务中达到SOTA的水准

### 2019.12.2
**论文**：[Pose Invariant Embedding for Deep Person Re-identification](https://arxiv.org/abs/1701.07732)

**笔记**：[Pose Invariant Embedding for Deep Person Re-identification Note](https://zhuanlan.zhihu.com/p/94876524)

**理解**：本文使用姿态估计对行人图片进行对齐，提高ReID准确率
### 2019.12.12

**论文**：[Person Re-identification Past Present and Future](https://arxiv.org/pdf/1610.02984.pdf)

**笔记**：[Person Re-identification Past Present and Future Note](https://zhuanlan.zhihu.com/p/97138236)

**理解**：一片很好的综述文章，需要反复看

### 2019.12.15
**论文**：[Bag of Tricks and A Strong Baseline for Deep Person Re-identification](https://arxiv.org/pdf/1905.00953.pdf)

**笔记**：[Bag of Tricks and A Strong Baseline for Deep Person Re-identification Note](https://zhuanlan.zhihu.com/p/97495006)

**理解**：罗浩大佬使用ResNet50+warmup+REA+LabelSmooth+BNNeck+sride=1+centerloss实现的strong baseline

### 2019.12.28
**论文**：[Pyramidal Person Re-IDentification via Multi-Loss Dynamic Training](http://openaccess.thecvf.com/content_CVPR_2019/papers/Zheng_Pyramidal_Person_Re-IDentification_via_Multi-Loss_Dynamic_Training_CVPR_2019_paper.pdf)

**笔记**：[Pyramidal Person Re-IDentification via Multi-Loss Dynamic Training Note](https://zhuanlan.zhihu.com/p/100159357)

**理解**：多尺度分块特征的结合，提出一种动态采样dataloader的方法

### 2019.12.30
**论文**：[Batch DropBlock Network for Person Re-identification and Beyond](https://arxiv.org/pdf/1811.07130.pdf)

**笔记**：[Batch DropBlock Network for Person Re-identification and Beyond Note](https://zhuanlan.zhihu.com/p/99725199)

**理解**：对ResNet第4个stage的特征图做batchdrop以提高模型对局部特征的关注

### 2020.1.3
**论文**：[Beyond Human Parts: Dual Part-Aligned Representations for Person Re-Identification](https://arxiv.org/abs/1910.10111)

**笔记**：[Beyond Human Parts: Dual Part-Aligned Representations for Person Re-Identification](https://zhuanlan.zhihu.com/p/100830237)

**理解**：本文针对人体部件的attention提出一种self-attention机制，可以解决part-misaligned的问题

### 2020.1.7
**论文**：[Mixed High-Order Attention Network for Person Re-Identification](https://arxiv.org/pdf/1908.05819.pdf)

**笔记**：[Mixed High-Order Attention Network for Person Re-Identification Note](https://zhuanlan.zhihu.com/p/101480931)

**理解**：提出mixed-order attention，整合channel attention和spatial attention的优势，对不同捕获难易程度的特征进行整合

## 步态识别(Gait Recognition)
### 2019.10.15

**论文**：[On Learning Disentangled Representations for Gait Recognition](https://arxiv.org/pdf/1909.03051v1.pdf)

**笔记**： [On Learning Disentangled Representations for Gait Recognition_Note](https://zhuanlan.zhihu.com/p/94581510)

**理解**：针对步态的三种主要特征进行学习再综合起来，效果的到大幅度提升，其中有GEI的影子，也有LSTM提取动态特征。最大的特点是作者提出的三种损失函数的分类方法

### 2019.10.16

**论文**：[Review on Vision-Based Gait Recognition Representations Classification Schemes and Datasets](https://pdfs.semanticscholar.org/e4c5/6224e55160c550cb54f5201a999ea322a694.pdf)

**笔记**：[Review on Vision-Based Gait Recognition Representations Classification Schemes and Datasets Note](https://zhuanlan.zhihu.com/p/94580835)

**理解**：步态特征设计主要为对人体建模以及非建模方式，且非建模大多沿用能量图的思路。传统特征设计主要集中于动态特征、外观特征上

### 2019.10.18

**论文**：[GaitSet Regarding Gait as a Set for Cross-View Gait Recognition](https://arxiv.org/pdf/1811.06186.pdf)

**笔记**：[GaitSet Regarding Gait as a Set for Cross-View Gait Recognition Note](https://zhuanlan.zhihu.com/p/94581955)

**理解**：使用集合的思想，池化对象从单张图片变为一个集合的图片，提取了集合方面的特征。对人体分块的思想可以针对不同区域提取不同特征。
