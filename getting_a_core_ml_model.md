[Apple原文链接](https://developer.apple.com/documentation/coreml/getting_a_core_ml_model)

### 获取一个Core ML 模型

获取Core ML 模型, 以便能在你的应用程序当中使用.

##

### 概述

Core ML 支持多种机器学习模型，其中包括了神经网络、集成树、支持向量机以及广义线性模型.Core ML 的运行需要使用 Core ML 模型格式（也就是以 .mlmodel 扩展名结尾的模型）

Apple 提供了一些常见的开源[模型](https://developer.apple.com/machine-learning)供大家使用, 这些模型已经使用了 Core ML 模型格式. 您可以自行下载这些模型, 然后就可以开始在应用中使用它们了. 此外, 其他的研究机构和大学都发布了不少机器学习模型和训练数据, 这些往往都不是以 Core ML 模型格式发布出来的. 如果您打算使用这些模型的话, 需要对它们进行转换, 具体内容详见[将已训练模型转换为 Core ML](https://developer.apple.com/documentation/coreml/converting_trained_models_to_core_ml).

### 参见
##
#### 第一步
[集成一个Core ML 模型 到你的应用程序当中](https://developer.apple.com/documentation/coreml/integrating_a_core_ml_model_into_your_app)

向应用程序添加一个简单的模型, 通过对模型输入数据, 并对模型的预测值进行处理.
