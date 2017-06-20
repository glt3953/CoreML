[Apple原文链接](https://developer.apple.com/documentation/coreml/integrating_a_core_ml_model_into_your_app)



### 将 Core ML 模型集成到你的App中

向应用程序添加一个简单的模型, 将输入数据传递给模型, 并处理模型的预测. 

[DownLoad](https://docs-assets.developer.apple.com/published/51ff0c1668/IntegratingaCoreMLModelintoYourApp.zip)

##      

### 概述

这个示例程序使用一个经过训练的模型，MarsHabitatPricer.mlmodel 来预测火星上的栖息地的价格。



### 添加一个模型到你的XCode中

通过将模型拖放到项目管理器的方式添加一个模型到你的Xcode项目中。

你可以通过打开XCode中的模型来查看模型的信息——包括模型类型及其预期输入和输出。

模型的输入是太阳能电池板和温室的数量，以及栖息地的面积（英亩）.模型的输出是栖息地的预测价格。



![](https://docs-assets.developer.apple.com/published/bc34b3e6c2/6b4f8b26-1cd0-4d9e-8b54-54dac16a808c.png)



### 在代码中创建模型



XCode还使用关于模型输入和输出的信息来自动生成模型的自定义程序界面，用于与代码中的模型进行交互。对于MarsHabitatPricer.mlmodel，XCode生成用于代表模型（MarsHabitatPricer），模型输入（MarsHabitatPricerInput）和模型输出（MarsHabitatPricerOutput）的界面。

使用生成的MarsHabitatPricer类的初始化方法来创建模型：



```

let model = MarsHabitatPricer()

```



### 获取输入值传递给模型

这个示例程序使用一个UIPickerView从用户这里获取模型的输入值：



```

func selectedRow(for feature: Feature) -> Int {

    return pickerView.selectedRow(inComponent: feature.rawValue)

}



let solarPanels = pickerDataSource.value(for: selectedRow(for: .solarPanels), feature: .solarPanels)

let greenhouses = pickerDataSource.value(for: selectedRow(for: .greenhouses), feature: .greenhouses)

let size = pickerDataSource.value(for: selectedRow(for: .size), feature: .size)

```



### 使用模型进行预测

MarsHabitatPricer类有一个生成的预测的方法（solarPanels：greenhouses：size :)，用于根据模型的输入值预测价格 - 在这个例子中，输入值指的是太阳能电池板的数量，温室的数量和栖息地的大小（ 英亩）。 该方法的结果是一个MarsHabitatPricerOutput实例，marsHabitatPricerOutput。



```

guard let marsHabitatPricerOutput = try? model.prediction(solarPanels: solarPanels, greenhouses: greenhouses, size: size) else {

    fatalError("Unexpected runtime error.")

}

```



通过marsHabitatPricerOutput的price属性去获得预测的价格值，并在应用程序的界面上显示结果。



```

let price = marsHabitatPricerOutput.price

priceLabel.text = priceFormatter.string(for: price)

```



> ### 注意：

> 生成预测的方法可能会抛出异常。在使用Core ML 时最常见的错误发生在你传递给该方法的输入数据类型与所期望的模型的输入类型不匹配。例如，格式错误的图像。在这个示例程序中，输入的类型都是Double类型，任何不匹配的类型会在编译的时候被捕获到，如果发生错误，示例程序将发生致命错误。



### 构建并运行一个Core ML 应用程序

XCode将Core ML 模型编译成为经过优化的，并且可以在设备上运行的资源。Core ML模型的优化包含在你的应用程序的Bundle中，并且在应用程序的运行过程中进行预测。



### 参见

##    

### 第一步

[获取一个Core ML模型](https://developer.apple.com/documentation/coreml/getting_a_core_ml_model)

- 获取一个Core ML模型在你的应用程序里面使用它





#### 