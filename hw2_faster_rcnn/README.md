# Faster R-CNN


## 环境配置：
* Python3.6/3.7/3.8
* Pytorch1.7.1
* pycocotools
* 最好使用GPU训练
* 详细环境配置见`requirements.txt`

## 文件结构：
```
  ├── backbone: 特征提取网络，可以根据自己的要求选择
  ├── network_files: Faster R-CNN网络（包括Fast R-CNN以及RPN等模块）
  ├── train_utils: 训练验证相关模块（包括cocotools）
  ├── my_dataset.py: 自定义dataset用于读取VOC数据集
  ├── train_resnet50_fpn.py: 以resnet50+FPN做为backbone进行训练
  ├── predict.py: 简易的预测脚本，使用训练好的权重进行预测测试
  ├── validation.py: 利用训练好的权重验证/测试数据的COCO指标，并生成record_mAP.txt文件
  └── pascal_voc_classes.json: pascal_voc标签文件
```

## 数据集，本例程使用的是PASCAL VOC2007数据集
* 使用ResNet50+FPN以及迁移学习在VOC2007数据集上得到的权重

## 训练方法
* 确保提前准备好数据集
* 确保提前下载好对应预训练模型权重
* 直接使用train_resnet50_fpn.py训练脚本

## 注意
预训练权重（放入backbone文件夹中）
Model Path(放入save_weights文件夹中)


