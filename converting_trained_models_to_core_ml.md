[Apple原文链接](https://developer.apple.com/documentation/coreml/converting_trained_models_to_core_ml)



### 转换训练模型为Core ML

通过第三方的机器学习扩展工具将创建的训练模型转换成Core ML模型的格式.

##  

### 概述

如果你的模型是使用受支持的第三方机器学习工具创建和训练的，则可以使用[Core ML Tools](https://pypi.python.org/pypi/coremltools)将模型转换为Core ML模型的格式。表1列出了支持的模型和第三方工具。

> 注意

> Core ML Tools 是一个Python package（coremltools），托管在Python package的主页上（PyPI），关于Python package的有关信息，请参阅[Python package用户指南](https://packaging.python.org/)



表一 Core ML Tools支持的模型和第三方工具    



|  模型类型  |  支持的模型  |  支持的工具  |
| :----:   | :----: | :----: |
| Neural networks（神经网络）|	Feedforward（正反馈）,convolutional（卷积）,recurrent（回归）| Caffe  Keras 1.2.2 |
| Tree ensembles（集成树）| Random forests（随机森林）,boosted trees（提升树）,decision trees（决策树） | scikit-learn 0.18 XGBoost 0.6 | 
| Support vector machines（支持向量机） |  Scalar regression（梯度回归）,multiclass classification（多类分类） | scikit-learn 0.18 LIBSVM 3.22 |
| Generalized linear models（广义线性模型） |  Linear regression（线性回归）,logistic regression（逻辑回归） |  scikit-learn 0.18 |
| Feature engineering（特征工程） |  Sparse vectorization（稀疏向量矢量化）,dense vectorization（稠密向量矢量化）, categorical processing（分类处理）|  scikit-learn 0.18 |
| Pipeline models（管道模型） | Sequentially chained models（顺序链模型）|  scikit-learn 0.18 |


### 转换模型

使用与模型的第三方工具相对应的Core ML 转换器，来转换模型。通过转换器的convert方法，将生成的模型保存为Core ML模型格式(.mlmodel).

例如，你的模型是用Caffe创建的，请将Caffe模型（.caffemodel）传递给coremltools.converters.caffe.convert方法。

```

import coremltools

coreml_model = coremltools.converters.caffe.convert('my_caffe_model.caffemodel')

```

然后将生成的模型保存为Core ML模型格式。

```

coreml_model.save('my_model.mlmodel')

```



根据你的模型，你可能需要更新输入、输出和标签，或者你可能需要声明图像的名称，类型和格式。转换器包含了更多的文档，这些文档因工具不同而异。如果想知道更多关于Core ML Tools的信息，请参阅[Package Documentation](https://pythonhosted.org/coremltools/).

### 或者，编写自定义转换器

当你需要转换的模型不是表1所列的工具支持的格式时，可以创建自己的转换器。

编写自己的转换器包括将模型的输入、输出和架构的表示形式转换为Core ML 模型格式。你可以通过定义模型架构的每一层，以及每一层和其他层之间的联系来实现转换器。你可以使用[Core ML Tools](https://pypi.python.org/pypi/coremltools)提供的转换器作为参考样例。这个参考样例演示了如何从第三方工具创建的各种模型类型转换为Core ML模型格式。

> 注意

> Core ML模型格式由一组protocol buffe files（协议缓冲）定义，更多说明请参考[Core ML Model Specification](https://developer.apple.com/machine-learning).
