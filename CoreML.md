[原文链接](https://developer.apple.com/documentation/coreml)

### Core ML

### 集成机器学习模型到你的app里面
##
### 概述
结合Core ML, 你可以集成训练机器学习模型到你的app里面.
![Alt text](https://docs-assets.developer.apple.com/published/72e22672fd/c35ebf2d-ee94-4448-8fae-16420e7cc4ed.png)

训练模型是将机器学习算法应用于一组训练数据的结果. 该模型基于新的输入数据进行预测. 例如, 根据某个地区的历史房价进行训练的模型, 可能能够在给予卧室和浴室的数量时预测房子的价格.

Core ML是特定领域的基础框架和功能库. Core ML支持视觉图像分析, 基础的自然语言处理(例如,  NSLinguisticTagger 类) 以及 GameplayKit 评估学习决策树. Core ML本身建立在诸如:  Accelerate 和 BNNS 以及 Metal Performance Shaders之类的底层库之上.
![Alt text](https://docs-assets.developer.apple.com/published/bc34b3e6c2/db81e861-1e06-4d14-8915-90707d9b114c.png)

Core ML针对设备性能进行了优化, 最大限度地减少了内存占用和功耗. 严格按照设备运行确保用户数据的隐私, 并确保您的应用程序在网络连接不可用时保持功能和响应.



## 主题
### 第一步
[获取一个Core ML模型](https://developer.apple.com/documentation/coreml/getting_a_core_ml_model)
- 获取一个Core ML模型在你的应用程序里面使用它

[集成一个Core ML模型到你的应用程序里面](https://developer.apple.com/documentation/coreml/integrating_a_core_ml_model_into_your_app)
- 向应用程序添加一个简单的模型, 将输入数据传递给模型, 并处理模型的预测. 


##
### 模型转换
[转换训练模型到Core ML](https://developer.apple.com/documentation/coreml/converting_trained_models_to_core_ml)
- 通过第三方的机器学习扩展工具将创建的训练模型转换成Core ML模型的格式.

##
### Core ML 接口
[Core ML 接口](https://developer.apple.com/documentation/coreml/core_ml_api)
- 使用Core ML API 直接支持自定义工作流和先进的用例.
