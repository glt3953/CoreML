 [Apple原文链接](https://developer.apple.com/machine-learning/)

![Alt text](https://developer.apple.com/assets/elements/icons/core-ml/core-ml-128x128_2x.png)

### 通过机器学习(machine learning)构建更多的智能应用程序


利用Core ML, 这是一种用于苹果产品的新的基础机器学习框架, 包括Siri，Camera和QuickType. Core ML提供快速的性能，轻松集成机器学习模型，使您能够使用几行代码构建具有智能新功能的应用程序.


### 概述

Core ML允许您将各种各样的机器学习模型类型集成到您的应用程序中. 除了支持30多种类型的广泛深入学习外，它还支持诸如树组合，支持向量机(SVM)和广义线性模型之类的标准模型. 由于它基于 Metal 和 Accelerate 等低级技术，Core ML 无缝利用CPU和GPU来提供最高的性能和效率.  您可以在设备上运行机器学习模型，因此数据不需要离开要进行分析的设备.

### 视觉

您可以轻松地将计算机视觉机器学习功能构建到您的应用程序中. 支持的功能包括面部跟踪，人脸检测，地标，文本检测，矩形检测，条形码检测，对象跟踪和图像配准.

### 自然语言处理

基本框架(Foundation)中的自然语言处理API使用机器学习深入了解文本，使用语言识别，标记化，词汇化，词性化和命名实体识别等功能。

### 使用模型

使用以下可用的Core ML模型构建您的应用程序，或使用Core ML Tools轻松将模型转换为Core ML格式.

### 模型

#### Places205-GoogLeNet | ResNet50
> 从205个类别检测图像的场景，如机场，卧室，森林，海岸等. [查看原始模型详情](https://developer.apple.com/machine-learning/model-details/Places205-GoogLeNet.txt)

> [下载Core ML模型(文件大小: 24.5 M)](https://docs-assets.developer.apple.com/coreml/models/GoogLeNetPlaces.mlmodel)


#### ResNet50
> 从1000个类别（如树木，动物，食物，车辆，人物等）中检测出图像中的主要物体. [查看原始模型详情](https://developer.apple.com/machine-learning/model-details/ResNet50.txt)

> [下载Core ML模型(文件大小: 102.6 M)](https://docs-assets.developer.apple.com/coreml/models/Resnet50.mlmodel)

#### Inception v3
> 从1000个类别（如树木，动物，食物，车辆，人物等）中检测出图像中的主要物体. [查看原始模型详情](https://developer.apple.com/machine-learning/model-details/Inception-v3.txt)

> [下载Core ML模型(文件大小: 94.7 M)](https://docs-assets.developer.apple.com/coreml/models/Inceptionv3.mlmodel)


#### VGG16
> 从1000个类别（如树木，动物，食物，车辆，人物等）中检测出图像中的主要物体. [查看原始模型详情](https://developer.apple.com/machine-learning/model-details/VGG16.txt)

> [下载Core ML模型(文件大小: 553.5 M)](https://docs-assets.developer.apple.com/coreml/models/VGG16.mlmodel)


### Core ML Tools
Core ML Tools是一个可以用于将模型从机器学习工具库转换为Core ML格式的python软件包.
> [获取Core ML Tools](https://pypi.python.org/pypi/coremltools)

> [Core ML Model 说明书](https://docs-assets.developer.apple.com/coreml/documentation/mlmodel_specification.zip)
