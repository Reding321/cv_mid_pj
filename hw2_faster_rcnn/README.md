# Faster R-CNN


## 环境配置：
* Python3.6/3.7/3.8
* Pytorch1.7.1
* pycocotools
* 最好使用GPU训练
* 详细环境配置见`requirements.txt`


## 数据集，本例程使用的是PASCAL VOC2007数据集
* 使用ResNet50+FPN以及迁移学习在VOC2007数据集上得到的权重

## 训练方法
* 确保提前准备好数据集
* 确保提前下载好对应预训练模型权重
* 直接使用train_resnet50_fpn.py训练脚本

## 注意
预训练权重（放入backbone文件夹中）

Model Path(放入save_weights文件夹中)

见课程报告的百度云地址
