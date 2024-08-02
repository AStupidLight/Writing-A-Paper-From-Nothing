对序列模型的神经网络。

RNN是一个序列模型，将一个序列映射到另一个序列。

单向循环：考虑当前的输出和上一个记忆单元

双向循环：还考虑未来的记忆单元。需要把所有内容全部输出进去才能开始输出，速度非常慢。

delayRNN：首三帧输出值不要，从第四帧开始输出。可以在首次输出的过程中也有比较好的序列效果。

# 优点

可以处理变长序列

模型大小与序列长度无关（只与输入通道数和隐含单元数有关）

考虑历史信息

便于流式输出（边输入边输出）

# 缺点

不能并行计算

无法获取太长的历史信息（梯度消失）





潜变量回归模型

![image-20240801150400943](C:/Users/lenovo/AppData/Roaming/Typora/typora-user-images/image-20240801150400943.png)

其中的，生成一个系列h，每一个ht都和前一个ht-1和输入xt-1有关。

隐变量：hidden variable，是连接输入x和输出output中间的一个隐藏的表示

![image-20240801150857434](C:/Users/lenovo/AppData/Roaming/Typora/typora-user-images/image-20240801150857434.png)



h是由前一个Ht-1和输入Xt-1共同决定的，而输出o直接由ht决定。$\Phi$是一个激活函数，b是偏置。Whh来存储所有的时序信息



![image-20240801151149886](C:/Users/lenovo/AppData/Roaming/Typora/typora-user-images/image-20240801151149886.png)

目的是：我现在有一段话，我要预测接下来的内容。我输入“你”，我就希望可以直接输出一个“好”。当前时刻的输出是预测下一个观察。通过比较当前预测和实际情况来调整参数。

![image-20240801152045278](C:/Users/lenovo/AppData/Roaming/Typora/typora-user-images/image-20240801152045278.png)

# Pytorch RNN

![image-20240802133351310](C:/Users/lenovo/AppData/Roaming/Typora/typora-user-images/image-20240802133351310.png)

![image-20240802133500609](C:/Users/lenovo/AppData/Roaming/Typora/typora-user-images/image-20240802133500609.png)



![image-20240802133650313](C:/Users/lenovo/AppData/Roaming/Typora/typora-user-images/image-20240802133650313.png)
