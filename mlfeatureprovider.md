[Apple原文链接](https://developer.apple.com/documentation/coreml/mlfeatureprovider)



### 协议
### MLFeatureProvider

一个表示模型的特征值集合的接口

### 概述
如果您有更复杂的数据源, 请考虑将此协议添加到数据源.  该接口是直接实现的, 主要是功能值的访问器.  通过实现协议, 您可以允许MLModel在不构建单独的输入实例的情况下查询数据源.  如果您的数据是异步收集的, 请在数据结构上实现此协议.  或者，如果使用自动生成的界面导致复制过多的数据，请使用此协议将数据直接与MLModel集成.


### 主题
---
#### 读取值
> [func featureValue(for: String)](https://developer.apple.com/documentation/coreml/mlfeatureprovider/2879185-featurevalue)
- 通过特征的名称读取特征的值
- Required(需要)

> [var featureNames: Set<String>](https://developer.apple.com/documentation/coreml/mlfeatureprovider/2879184-featurenames)
- 特征名称的集合
- Required(需要)


### 关系
---
#### 被收集
> [MLDictionaryFeatureProvider](https://developer.apple.com/documentation/coreml/mldictionaryfeatureprovider)


### 还可以看看
--- 
#### 模型特征
> [class MLDictionaryFeatureProvider](https://developer.apple.com/documentation/coreml/mldictionaryfeatureprovider)

- 将字典数据包装成便利器

> [class MLFeatureValue](https://developer.apple.com/documentation/coreml/mlfeaturevalue)

- 表示特征类型和值的不可变实例.
Beta
> [class MLFeatureDescription](https://developer.apple.com/documentation/coreml/mlfeaturedescription)
- 特征描述


> [class MLMultiArray](https://developer.apple.com/documentation/coreml/mlmultiarray)

- 用作模型的输入或输出的多维数组.

### 相关文档
---
> [Core ML API](https://developer.apple.com/documentation/coreml/core_ml_api)
- 直接使用Core ML API来支持自定义工作流和高级用例
