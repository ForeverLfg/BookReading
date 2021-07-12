# 《图解TCP/IP》

## 1.OSI模型

![image-20210711231605561](C:\Users\Forever\AppData\Roaming\Typora\typora-user-images\image-20210711231605561.png)

* 发送端和接收端的处理流程正好**相反**，就像收发快递一样。发送方执行的是打包的操作，接收方则执行拆包操作。

* 数据每向下传输一层，就加一层标签；同样的，没向上传递一层，就拆一层标签。

## 2.传输方式的分类

### 2.1 面向有连接型和面向无连接型

  ![image-20210711235046362](C:\Users\Forever\AppData\Roaming\Typora\typora-user-images\image-20210711235046362.png)

###     2.2 电路交换与分组交换

![image-20210712001203066](C:\Users\Forever\AppData\Roaming\Typora\typora-user-images\image-20210712001203066.png)

![image-20210712001441804](C:\Users\Forever\AppData\Roaming\Typora\typora-user-images\image-20210712001441804.png)

## 3. 地址

* 网络通信中，每一层协议所使用的地址不尽相同。

* MAC地址和IP地址在标识一个通信主体时虽然都具有唯一性，但是他妈当中只有**IP地址**具有唯一性。

* **地址转发表**：MAC寻址所参考的表；**路由控制表**：IP寻址参考的表。

  ![image-20210712224202415](C:\Users\Forever\AppData\Roaming\Typora\typora-user-images\image-20210712224202415.png)

## 4.网络的构成要素

![image-20210712230140999](C:\Users\Forever\AppData\Roaming\Typora\typora-user-images\image-20210712230140999.png)

* 从严格意义上讲，各种传输媒介中信号的流动速度是恒定的。
* 传输速率高并不是指单位数据流动的速度有多快，而是指单位时间内传输的数据量有多少。
* 低速数据链路就如同车道较少无法让很多车同时通过；高速速率相当于有多个车道，一次允许更多车辆行驶的道路。
* 主机之间实际的额传输速率被称做吞吐量，单位为bps(每秒比特数)；吞吐量不仅衡量贷款，也衡量主机的CPU处理能力、网络的拥堵程度、报文中数据字段的占有份额。