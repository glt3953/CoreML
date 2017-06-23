[Apple原文链接](https://developer.apple.com/documentation/coreml/mlmodel)



### MLModel

对机器学习模型的所有细节的封装

---

### 概述

在许多情况下，您可以直接使用Core ML，而无需访问MLModel类。而自动生成的模型类（以.mlmodel文件命名）为程序员提供了一个友好的界面，你应该使用它。

不管怎样，你如果创建自己的MLFeatureProvider，你需要直接使用MLModel [prediction(from:)](https://developer.apple.com/documentation/coreml/mlmodel/2880280-prediction).

可以通过创建自动生成的类并访问类的模型属性来得到MLModel实例。



### 主题

---

#### 创建一个模型

[init(contentsOf:)](https://developer.apple.com/documentation/coreml/mlmodel/2880279-init)

-创建一个Core ML模型，只在不使用Xcode自动生成的界面时使用。

---

#### 预测输出值

[func prediction(from: MLFeatureProvider)](https://developer.apple.com/documentation/coreml/mlmodel/2880280-prediction)

- 使用给定的特征值，对输出值进行预测。

--- 

#### 内省模型

[var modelDescription: MLModelDescription](https://developer.apple.com/documentation/coreml/mlmodel/2879179-modeldescription)

- 模型的元数据，也显示在模型的Xcode视图中。

[class MLModelDescription](https://developer.apple.com/documentation/coreml/mlmodeldescription)

- 模型的信息，主要是预测的输入和输出格式，以及附加的可选元数据。



### 相关

#### 继承自 [NSObject](NSObject)

#### 遵循的协议 [CVarArg](https://developer.apple.com/documentation/swift/cvararg), [Equatable](https://developer.apple.com/documentation/swift/equatable), [Hashable](https://developer.apple.com/documentation/swift/hashable)

