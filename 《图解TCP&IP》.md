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



### 4.1 中继器--物理层

![image-20210712232719067](C:\Users\Forever\AppData\Roaming\Typora\typora-user-images\image-20210712232719067.png)

* 对减弱的信号进行方法和发送
* 通过物理层的连接延长网络
* 即使在数据链路层出现某些错误，中继器仍然转发数据
* 中继器无法改变传输速率



### 4.2 网桥（2层交换机）——数据链路层

* 在OSI模型的第2层（数据链路层），连接两个网络；
* 将数据帧临时存储于内存，再重新生成信号作为一个全新的帧转发给相连的另一个网段；
* 数据帧中有一位叫FCS，用以校验数据是否正确送达目的地；
* 根据MAC地址进行处理。

![image-20210712234345237](C:\Users\Forever\AppData\Roaming\Typora\typora-user-images\image-20210712234345237.png)

![image-20210712234940360](C:\Users\Forever\AppData\Roaming\Typora\typora-user-images\image-20210712234940360.png)

* 以太网等网络中经常使用的交换集线器（Hub）,现在也属于网桥的一种；交换集线器中连接电缆的每个端口都能提供类似网桥的功能。

  

## 4.3 路由器（3层交换机）--网络层

* **网桥根据物理地址（MAC地址）进行处理**，路由器则根据IP地址进行处理;
* 路由器可以连接两个不同的网络；
* 路由器还分担网络负荷，甚至有的路由器还具备一定的网络安全功能。

### 4.4 4-7层交换机

* 处理OSI模型中从传输层到应用层的数据。
* 举例：负载均衡器（多台服务器来分担访问压力）、带宽控制（优先处理及时性要求较高的通信请求，放缓处理及时性不高的要求）、广域网加速器、特殊应用访问加速和防火墙

## 4.5 网关

![img](https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fwww.elecfans.com%2Fbaike%2FUploadPic%2F2010-4%2F20104315148597.jpg&refer=http%3A%2F%2Fwww.elecfans.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1628724847&t=0ed7170b53839305cf55d13849c59803)

* **协议的转换**和**数据的转发**；

* 在两个不能进行直接通信的协议之间进行翻译，最终实现两者之间的通信；

* 手机和互联网设置了一层网关；

  **网关举例**：

  代理服务器：为了控制流量以及处于安全的考虑，这种叫做应用网关。

  防火墙：针对不同应用提高了安全性。