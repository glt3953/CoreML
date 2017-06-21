[Apple原文链接](https://developer.apple.com/documentation/coreml/core_ml_api)

### Core ML API

直接使用Core ML API来支持自定义工作流和高级用例.

### 概述
在大多数情况下，你只和模型的动态的界面进行交互，这个界面是当您向Xcode项目添加模型时，Xcode自动创建的. 在需要支持自定义工作流或高级用例的情况下，你可以直接在案例中使用Core ML API。 例如，如果您需要在将输入数据异步收集到自定义结构体中时进行预测，则可以使用该结构体通过采用 [MLFeatureProvider](https://developer.apple.com/documentation/coreml/mlfeatureprovider) 协议为模型提供输入特征.


### 主题
---
#### 模型(Model)
> [class MLModel](https://developer.apple.com/documentation/coreml/mlmodel)
- 对机器学习模型的所有细节的封装
---

#### 模型特征(Model Features)
> [protocol MLFeatureProvider](https://developer.apple.com/documentation/coreml/mlfeatureprovider)
- 表示模型的特征值集合的接口

> [class MLDictionaryFeatureProvider](https://developer.apple.com/documentation/coreml/mldictionaryfeatureprovider)
- 将给定的数据字典包装成一个便利器

> [class MLFeatureValue](https://developer.apple.com/documentation/coreml/mlfeaturevalue)
- 表示特征类型和值的不可变实例.

> [class MLFeatureDescription](https://developer.apple.com/documentation/coreml/mlfeaturedescription)
- 特征描述.

> [class MLMultiArray](https://developer.apple.com/documentation/coreml/mlmultiarray)
- 用做模型的输入或输出的多维数组.
---
#### 错误
> [struct MLModelError](https://developer.apple.com/documentation/coreml/mlmodelerror)
- Core ML 的错误代码.
