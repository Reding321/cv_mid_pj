# Faster R-CNN

## 该项目主要是来自
* https://github.com/WZMIAOMIAO/deep-learning-for-image-processing/tree/master/pytorch_object_detection/faster_rcnn

## 环境配置：
* Python3.6/3.7/3.8
* Pytorch1.7.1(注意：必须是1.6.0或以上，因为使用官方提供的混合精度训练1.6.0后才支持)
* pycocotools(Linux:`pip install pycocotools`; Windows:`pip install pycocotools-windows`(不需要额外安装vs))
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

## 预训练权重下载地址（下载后放入backbone文件夹中）：
* [ResNet50+FPN backbone](https://pan.baidu.com/s/1wO5jCPaeN2y02LtPLfslnw?pwd=hcnr)
 
## 数据集，本例程使用的是PASCAL VOC2012数据集
* Pascal VOC2012 train/val数据集下载地址：http://host.robots.ox.ac.uk/pascal/VOC/voc2012/VOCtrainval_11-May-2012.tar
* 使用ResNet50+FPN以及迁移学习在VOC2012数据集上得到的权重: 同上的百度云链接

## 训练方法
* 确保提前准备好数据集
* 确保提前下载好对应预训练模型权重
* 直接使用train_resnet50_fpn.py训练脚本

## Model Path(下载后放入save_weights文件夹中)
* [resNetFpn-model-14.pth](https://pan.baidu.com/s/1wO5jCPaeN2y02LtPLfslnw?pwd=hcnr)

## Faster RCNN框架图
![Faster R-CNN](fasterRCNN.png) 

## 结果可视化(mAP=0.783)
![train_loss](train_loss.png) 
![mAP](mAP.png) 