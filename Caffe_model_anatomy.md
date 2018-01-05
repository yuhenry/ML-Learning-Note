# Caffe模型解剖
* Blob：标准数组，统一存储界面
* Layer：模型和计算的基础
* Net：Layer的链接和集合
* SLover：将模型和优化分离

## Blob——存储和传输
* Caffe数据的封装，后台同步CPU和GPU，本质是N维数组
* 图像数据：N（图像数量）* K（通道数）* H（高）* W（宽）

## Layer——计算和连接
### 三种计算
* Setup：初始化Layer及其连接
* Forward：由输入自底Bottom向上Top计算输出
* Backward：计算梯度Gradient传回底层Bottom

## Net——定义与运行
* DAG（directed acyclic graph）有向非循环图
* 输入数据层
* 输出损失层（Loss）

## 模型格式
* 模型定义： *.prototxt
* 已学习的模型： *.caffemodel