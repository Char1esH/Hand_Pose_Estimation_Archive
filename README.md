# 2018-2021手势识别相关论文整理

## CVPR 2021
### Semi-Supervised 3D Hand-Object Poses Estimation with Interactions in Time
**基于半监督学习 提供手-物品实时交互 的3D手势识别**  
首先训练全监督的3D手部、物体识别网络  
然后将视频投入网络，获得假标签  
设计统一的框架 捕捉手部和物体的关系

**创新点**  
1. 完整的3D手势识别框架
2. 半监督学习，利用大量无标注的视频数据
3. 在手部-物体识别上获得明显的性能提升

***  
## CVPR 2020
### HOPE-Net: A Graph-based Model for Hand-Object Pose Estimation
**基于图卷积网络的人-物体识别网络HOPE-Net**
提出轻量化的网络HOPE-Net，在2D和3D空间下预测手-物体  
首先使用detection method检测2D坐标，然后使用regression回归3D坐标  

**创新点**
1. HOPE-Net从单张RGB图片检测2D和3D人-物体坐标，都有很高准确率
2. 提出了自适应图U-Net，将2D的坐标转换为3D的坐标，它相比之前的U-Net更加稳定和robust
3. 实验准确度打败了手-物体检测的STOA，同时检测具有实时性

### Monocular Real-time Hand Shape and Motion Capture using Multi-modal Data
**使用多种模型数据 实现单目实时手势识别与运动捕捉**  
文章提出了两个网络DETNet和IKNet  
DETNet首先从单张图片检测二维坐标，然后回归三维坐标  
IKNet从三维坐标中预测手部关节的角度信息，还原手部工程建模

***创新点***  
1. 模型训练可以利用到各种数据：二维标注的图片，三维标注的图片，无图片的手部模型数据
2. 精度高，速度也非常快，高达100fps
3. 提出的IKNet可以将3D的关键点数据转换为关节旋转角度数据，这样的数据对计算机图形学和计算机视觉有着更加直接的应用价值

***  
## Neurocomputing 2020
### Pose Guided Structured Region Ensemble Network for Cascaded Hand Pose Estimation
**Pose-Ren通过级联迭代的方式进行手部检测**  
从CNN中获取更多的手部特征，根据手部的拓扑结构对识别区域进行层次集成  
直接回归三维的手部姿态，通过迭代级联的方式得到最终的姿态  

**创新点**  
1. 提出了新的手部特征提取方法
2. 通过迭代级联的方式获取最终的手部姿态
3. 根据手的结构进行区域划分，并且在后期整合

***  
## ICCV 2019
### Aligning Latent Spaces for 3D Hand Pose Estimation
**对齐潜在空间的三维手势识别**  
通过利用图像的深度信息，辅助基于RGB图像的人体手势识别  
结合了多种输入提高准确率

**创新点**  
1. 在三种不同的输入下进行人体手部识别
2. 充分利用各种输入提高准确率


### SO-HandNet: Self-Organizing Network for 3D Hand Pose Estimation with Semi-supervised Learning
**SO-HandNet：半监督的 手势识别 自组织网络**  
使用半监督的方式 直接从3D点云中回归出手的三位点坐标  
半监督，使用带有GT的数据训练网络，使用无标注的数据优化网络  

**创新点**  
1. 使用半监督的方式 能够利用更多的训练数据
2. 提出了一种encoder-decoder的架构 直接从3D点阵图中回归手部坐标
3. 相比其他半监督或全监督的方法，有着更好的准确率

***  
## CVPR 2019
