# Meta-programming neural network 元编程神经网络

Compile-time matrix constructions, headonly 构造编译期矩阵以及数据传递代码

Usage, the process is very simple 使用方法，过程极其简单
```cpp
/// 1. Create a neural network with an input layer two hide layers and an output layer 创建一个输入层，两个隐含层，一个输出层的神经网络 
mtl::BPNN<20, 30, 20, 2> bpnn;

/// 2. initialization 初始化
bpnn.init(0.001, 0.8);

/// 3. enter your matrix data... 录入你的矩阵数据
mtl::Matrix<double, 1, 20> inMatrix;
mtl::Matrix<double, 1, 2> outMatrix;
///    ... 

/// 4. training 训练 
bpnn.train(inMatrix, outMatrix, 100);

/// 5. simulation 仿真
bpnn.simulat(inMatrix, outMatrix);
```
