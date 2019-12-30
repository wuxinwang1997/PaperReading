## 行人重识别(Person Re-identification)
### 2019.10.20

**综述论文**：[A_survey_of_approaches_and_trends_in_person_re-identification](./A_survey_of_approaches_and_trends_in_person_re-identification/A_survey_of_approaches_and_trends_in_person_re-identification.pdf)

**笔记**：[A_survey_of_approaches_and_trends_in_person_re-identification_Note](https://zhuanlan.zhihu.com/p/94554289)

**理解**：该论文是2014年的综述论文，没有涉及到深度学习的东西。行人重识别就是一个图像匹配的问题，对于传统方法，难点主要在于特征的选取，还有就是分类的度量方法也比较困难。

推荐一个综述：[知呼行人重识别专栏](https://zhuanlan.zhihu.com/p/26168232)

### 2019.10.21

**论文**：[Beyond_Part_Models_Person_Retrieval_with_Reﬁned_Part_Pooling](https://arxiv.org/pdf/1711.09349.pdf)

**笔记**：[Beyond_Part_Models_Person_Retrieval_with_Reﬁned_Part_Pooling_Note](https://zhuanlan.zhihu.com/p/94576148)

**理解**：该论文是孙凡逸和郑良的一个基线代码的论文，对PCB算法进行了改进。针对人体特征，将CNN学习到的特征分为条带，然后使用Refined Part Pooling机制提高PCB模型的mAP。可以作为行人重识别的baseline

### 2019.10.29

**论文**：[Learning_Discriminative_Features_with_Multiple_Granularities](https://arxiv.org/pdf/1804.01438.pdf)

**笔记**：[Learning_Discriminative_Features_with_Multiple_Granularities_Note](https://zhuanlan.zhihu.com/p/94576602)

**理解**：该论文集合全局特征与局部特征分三个分支学习，对于全局特征使用tripletloss，对于局部特征使用stride=1的策略保留细节，同时用softxmaxloss

### 2019.10.31

**论文**：[Pedestrian_Alignment_Network_for_Large-scale_Person_Re-identification](https://arxiv.org/pdf/1707.00408.pdf)

**笔记**：[Pedestrian_Alignment_Network_for_Large-scale_Person_Re-identification_Note](https://zhuanlan.zhihu.com/p/94577169)

**理解**：该论文提出使用两个分支，一个用传统的CNN方法提取descriptor。一个先对浅层特征对准人物，双线性插值到原feature map大小，与高层特征网格化结合，再用变换矩阵纠正图像形态，然后提取descriptor。最后两个descriptor联合起来进行Re-ID。baseline是80%多的水平，所以最终效果也只是80%多，但是思路有借鉴意义

### 2019.12.1
**论文**：[Omni-Scale_Feature_Learning_for_Person_Re-Identification](https://arxiv.org/pdf/1905.00953.pdf)

**笔记**：[Omni-Scale_Feature_Learning_for_Person_Re-Identification_Note](https://zhuanlan.zhihu.com/p/94577433)

**理解**：采用卷积分解降低计算复杂度，多流处理达到全尺度特征学习的目的。在ReID等任务中达到SOTA的水准

### 2019.12.2
**论文**：[Pose_Invariant_Embedding_for_Deep_Person_Re-identification](https://arxiv.org/abs/1701.07732)

**笔记**：[Pose_Invariant_Embedding_for_Deep_Person_Re-identification_Note](https://zhuanlan.zhihu.com/p/94876524)

**理解**：本文使用姿态估计对行人图片进行对齐，提高ReID准确率
### 2019.12.12

**论文**：[Person_Re-identification_Past_Present_and_Future](https://arxiv.org/pdf/1610.02984.pdf)

**笔记**：[Person_Re-identification_Past_Present_and_Future_Npte](https://zhuanlan.zhihu.com/p/97138236]

**理解**：一片很好的综述文章，需要反复看

### 2019.12.15
**论文**：[Bag_of_Tricks_and_A_Strong_Baseline_for_Deep_Person_Re-identification](https://arxiv.org/pdf/1905.00953.pdf)

**笔记**：[Bag_of_Tricks_and_A_Strong_Baseline_for_Deep_Person_Re-identification_Note](https://zhuanlan.zhihu.com/p/97495006)

**理解**：罗浩大佬使用ResNet50+warmup+REA+LabelSmooth+BNNeck+sride=1+centerloss实现的strong baseline

## 步态识别(Gait Recognition)
### 2019.10.15

**论文**：[On_Learning_Disentangled_Representations_for_Gait_Recognition](https://arxiv.org/pdf/1909.03051v1.pdf)

**笔记**： [On_Learning_Disentangled_Representations_for_Gait_Recognition_Note](https://zhuanlan.zhihu.com/p/94581510)

**理解**：针对步态的三种主要特征进行学习再综合起来，效果的到大幅度提升，其中有GEI的影子，也有LSTM提取动态特征。最大的特点是作者提出的三种损失函数的分类方法

### 2019.10.16

**论文**：[Review_on_Vision-Based_Gait_Recognition_Representations_Classification_Schemes_and_Datasets](https://pdfs.semanticscholar.org/e4c5/6224e55160c550cb54f5201a999ea322a694.pdf)

**笔记**：[Review_on_Vision-Based_Gait_Recognition_Representations_Classification_Schemes_and_Datasets_Note](https://zhuanlan.zhihu.com/p/94580835)

**理解**：步态特征设计主要为对人体建模以及非建模方式，且非建模大多沿用能量图的思路。传统特征设计主要集中于动态特征、外观特征上

### 2019.10.18

**论文**：[GaitSet_Regarding_Gait_as_a_Set_for_Cross-View_Gait_Recognition](https://arxiv.org/pdf/1811.06186.pdf)

**笔记**：[GaitSet_Regarding_Gait_as_a_Set_for_Cross-View_Gait_Recognition_Note](https://zhuanlan.zhihu.com/p/94581955)

**理解**：使用集合的思想，池化对象从单张图片变为一个集合的图片，提取了集合方面的特征。对人体分块的思想可以针对不同区域提取不同特征。
