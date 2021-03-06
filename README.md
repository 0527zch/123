# 123

第一章 概述 

1.3 节互联网的组成 

(1)边缘部分由所有连接在互联网上的主机组成。这部分是直接使用的，用来进行通信和资 源共享。 

(2)核心部分 由大量网络和连接这些网络的路由器组成。这部分是为边缘部分提供服务的。 

1.5.2 计算机网络按照作用范围分类 

(1)广域网WAN，作用范围通常为几十到几千公里，有时也称为远程网。 

(2)城域网MAN，作用范围一般是一个城市，可跨越几个街区甚至整个城市，其作用距离约为 5~50km。 

(3)局域网LAN，作用范围局限在较小的范围（如1km左右)。 

(4)个人区域网PAN，也常称为无线个人区域网WPAN，其作用范围大约在10m左右。 

1.6 性能指标中“速率”与 2.2.3 会结合考查 数据的传送速率（比特率）和码元传输速率 （波特率）的概念区别 ·

比特率：连接在计算机网络上的主机在数字信道上传送数据的速率，是指每秒传送的比特数，单位是比特 bit/s，比特率越高，每秒传送数据就越多。

波特率：波特率表示每秒通过信道传输的码元个数，单位是波特，是衡量数据传送速率 的指标。 

1.7.2 网络协议的三个要素 

(1)语法：即数据与控制信息的结构或格式； 

(2)语义：即需要发出何种控制信息，完成何种动作以及做出何种响应； 

(3)同步：即事件实现顺序的详细说明； 

1.7.3 图1-18 计算机网络的体系结构（OSI 七层模型 TCP/IP 四层协议 具有 5 层协议的体系 结构）

应用层：通过应用进程间的交互来完成特定网络应用。
运输层：负责向两台主机中进程之间的通信提供通用的数据传输服务。
应用层利用该服务传送应用层报文。 

主要用到以下两种协议： 

(1)传输控制协议TCP——提供面向连接的、可靠的数据传输服务，其数据传输的单位是报文段。

(2)用户数据报协议UDP——提供无连接的，尽最大努力的数据传输服务，其数据传 输的单位是用户数据报。

网络层：负责为分组交换网上的不同主机提供服务。在发送数据时，网络层把运输层 产生的报文段或用户数据报封装分组或包进行传送。由于网络层使用IP协议，因此分组也 叫IP数据报。 

数据链路层：数据链路层简称为链路层。两台主机之间的数据传输，总是在一段一段 的链路上传送的，这就需要专门的链路层协议。数据链路层将网络层交下来的IP数据包封装成帧，在两个相邻节点的链路上传输。

物理层：在物理层上所传数据的单位是比特。发送方发送1或0时，接收方应当收到1或 0。因此物理层要考虑用多大的电压代表1或0，以及接收方如何识别发送方所发送的比特。 

1.7.4 实体、协议、服务的相关概念

实体：表示任何可发送或接收信息的硬件或软件进程。 
协议：控制两个对等实体进行通信的规则的集合。
服务：在协议的控制下，两个对等实体间的通信使得本层能够向上一层提供服务。要实现本层协议，还需要使用下面一层所提供的服务。
服务访问点：同一系统中相邻两层实体进行交互的地方。 （协议是“水平的” 服务是“垂直的”） 

第二章 物理层 

2.2.1 数据通信系统的模型（调制与解调的作用分别是什么） 数据通信系统划分为三大部分，即源系统、传输系统和目的系统。 

源系统包括：源点、发送器、接收器、终点 

发送器：通常源点生成的数字比特流要通过发送器编码后才能够在传输系统中进行传输。典型的发送器就是调制器。
接收器：接收传输系统传送过来的信号，并把它转换为能够被目的设备处理的信息。 典型的接收器就是解调器。 

调制解调的作用：

调制能够把要传输的模拟信号或数字信号变换成适合信道传输的信号，这就意味着把基带信号(信源)转变为一个相对基带频率而言频率非常高的带通信号。该信号称为已调信号，而基带信号称为调制信号。
调制可以通过使高频载波随信号幅度的变化而改变载波的 幅度、相位或者频率来实现。调制过程用于通信系统的发端。

解调能够在接收端需将已调信号还原成要传输的原始信号，也就是将基带信号从载波中提 取出来以便预定的接受者(信宿)处理和理解。 

2.2.2 常用的编码方式（着重看曼彻斯特编码和差分曼彻斯特编码） 

不归零制：正电平代表1，负电平代表0；
归零制：正脉冲代表1，负脉冲代表0； 
曼彻斯特编码：位周期中心的向上跳变代表0，位周期中心的向下跳变代表1； 
差分曼彻斯特：每一位的中心处都有跳变。位开始边界有跳变代表0，位开始边界没有跳 变代表1。

2.2.3 信道的极限容量（着重看） C=W log2(1+S/N)(bit/s) 

2.3 常用的物理层下的传输媒体主要有哪些？ 

导引型传输媒体（双绞线 同轴电缆 光缆）和非导引型传输媒体，在导引型传输媒体中，电磁波被导引沿着固体媒体传播，而非导引型传输媒体就是指自由空间，在非导引型传输媒体中电磁波的传输常称为无线传输。 

第三章 数据链路层 

3.1.2 数据链路层要解决的三个基本问题（重点看差错检测中的 CRC 循环冗余检验） 

封装成帧：添加首尾部

透明传输：帧定界符SOH和EOT，不管在键盘上输入什么字符都可以放在这样的帧里传过去

差错检测：循环冗余检验CRC 余数R=0无差错，R≠0有差错丢弃

3.2 ppp 协议中涉及到“零比特填充” 

PPP协议用在SONET/SDH链路时，使用同步传输而不是一部传输。在这种情况下，PPP协议采用零比特填充方法来实现透明传输。 

零比特填充的具体做法是：在发送端，先扫描整个信息字段。只要发现有5个连续1，则立即 填入一个0.因此经过这种零比特填充后的数据，就可以保证在信息字段中不会出现6个连续1。 
接收端在收到一个帧时，先找到标志字段F已确定一个帧的边界，接着再用硬件对其中的比 特流进行扫描。每当发现5个连续1时，就把这5个连续1后的一个0删除，以还原成原来信息比特流。
这样就保证了透明传输：在所传送的数据比特流中可以传送任意组合的比特流，而不会引起对帧边界的错误判断。 

3.3.1 适配器（网卡的作用） 

(1)进行数据串行传输和并行传输的转换 
(2)实现以太网协议 

3.3.2 着重看 CSMA/CD 协议 （简述该协议原理）

每个节点都共享网络传输信道，在每个站要发送数据之前，都会检测信道是否空闲，如果空闲则发送，否则就等待；在发送出信息后，则对冲突进行检测，当发现冲突时，则取消发送。

(1)多点接入：总线型网络，许多计算机以多点接入的方法连接在一根总线上 
(2)载波监听：不管在发送前还是发送中，每个站都必须不停的检测信道 
(3)碰撞检测：边发送边监听 3.3.5 以太网的 MAC 层（MAC 地址考查）

3.4 数据链路层的主要设备用了哪些？
网桥 交换式集线器(以太网交换机 实质上是多接口的网桥) 

第四章 网络层 

4.1 网络层的主要服务是什么 

1.虚电路VC 
2.网络层向上提供简单灵活的、无连接的、尽量大努力交付的数据报服务 

4.2 网际协议 IP 

(1)地址解析协议ARP 
(2)网际控制报文协议ICMP
(3)网际组管理协议IGMP 

4.2.2 IP 地址表示方法和 IP 地址主要分类 

A类：前8位网络号 24位主机号 1~126 
B类：前16位网络号 16位主机号 128~191 
C类：前24位网络号 8位主机号 192~223 

4.2.3 IP 地址与硬件地址的关系 MAC地址是数据链路层和物理层使用的地址，是物理地址，而IP地址是网络层和以上各层 使用的地址，是一种逻辑地址。 
IP数据报使用IP地址向上传输，传输到数据链路层就被封装成了MAC帧，MAC帧在传送时使 用的源地址和目的地址都是MAC地址，这两个MAC地址都被封装在MAC帧的首部。 
总而言之，IP地址放在IP数据报的首部，MAC地址放在MAC帧的首部。 

4.2.4 地址解析协议ARP 
从网络层使用的IP地址，解析出在数据链路层使用的硬件地址 在主机ARP高速缓存中存放一个从IP地址到硬件地址的映射表，并不断更新

4.4 网际控制报文协议ICMP的主要作用
网际控制报文协议ICMP的作用是提供一些管理和维护工作，检测出某些错误、获取信息， 使得能够更有效的转发IP数据报和提高交付成功的机会。
ICMP为内部IP层通信提供一个维护， 诊断和测试框架。 
ICMP报文作为IP数据报的数据部分，加上首部，组成IP数据报发出去。

ICMP分为：ICMP差错报告报文、ICMP询问报文 

4.5 路由算法（重点考查距离向量算法 RIP） 

距离向量算法特点： 1 完整正确 2 计算简单 3 能够适应通信量和网络拓扑的变化 4 具有稳定性 5 公平 6 最佳（相对较为合理） 

两类路由选择协议： 
·内部网关协议IGP：RIP和OSPF 
·外部网关协议EGP：BGP-4 

基于距离向量的路由选择算法 

RIP: RIP协议让一个自治系统中的所有路由器都和自己的相邻路由器，并不断更新其路由表， 使得从每一个路由器到每一个目的网络的路由都是最短的。 
网络中的每一个路由器都要维护从他自己到其他每一个目的网络的距离记录。 
从一路由器到直连网络的距离定为1，从一路由器到非直连网络的距离定为（经过的路由 器数+1）距离16即不可达，RIP只适用于小型互联网。 

距离向量的路由选择算法协议特点：

·仅和相邻路由器交换信息 
·路由器交换的信息是当前本路由器所知道的全部信息，即自己现在的路由表 
·按固定的时间间隔交换路由信息，如30s

第五章 传输层 

5.2.1 用户数据报协议UDP的特点

只在IP数据报服务基础上增加了很少的功能，即复用、分用、差错检测功能。 

(1)UDP是无连接的，即发送数据之前不需要建立连接，因此减少了开销和发送数据之前的 时延。
(2)UDP使用尽最大努力交付，即不保证可靠交付，因此主机不需要维持复杂的连续状态表。 
(3)UDP是面向报文的。发送方的UDP对应用程序交下来的报文，在添加首部后就向下交付 IP层。
(4)UDP没有拥塞控制，网络出现的拥塞不会使源主机的发送率降低。允许在网络拥塞时丢 失一些数据，却不允许数据有太大时延，如IP电话、实时视频会议等适用。 
(5)UDP支持一对一、一对多、多对一和多对多的交互通信。 (6)UDP首部开销小，只有8个字节。

IP数据报的检验和只检验IP数据包的首部，而UDP的检验和是把首部和数据报一起检验。 (不会求检验和（二进制反码运算求和）) 

5.3.1 传输控制协议TCP的特点 

(1)TCP是面向连接的运输层协议 
(2)每一条TCP连接只能有两个端点，每一条TCP连接只能是点对点的 
(3)TCP提供可靠交付的服务 
(4)TCP提供全双工通信 
(5)面向字节流 

5.6 TCP可靠传输实现机制 

·以字节为单位的滑动窗口 

·超时重传时间的选择 
RTT：报文的往返时间 
RTTs ：加权平均往返时间（平滑往返时间） 
RTTD ：偏差的加权平均值
RTO：超时重传时间
  新的 RTTs =(1-α)×(旧的 RTTs )+α×(新的RTT样本) 
  新的 RTTD =(1-β)×(旧的 RTTD )+β×| RTTs -新的RTT样本| 
  RTO= RTTs +4× RTTD 
Karn：在计算加权平均 RTTs 时，只要报文段重传了，就不采用其往返时间样本，这样得出 的加权平均 RTTs 和RTO就比较准确。 

·选择确认SACK 

5.7.1 TCP 流量控制机制 

流量控制就是让发送方的发送速率不要太快，要让接收方来得及接受 
利用滑动窗口机制实现流量控制：发送方的发送窗口不能超过接收方给出的接收窗口的数值。 
（为了解决死锁局面，使用持续计数器，时间到期就发送一个零窗口探测报文段） 

5.9.2 TCP 的连接和释放（着重看5.9.1连接建立 TCP三次握手） 

TCP运输连接三个阶段：连接建立（客户、服务器）、数据传送、连接释放。 

连接建立（三次握手）：

步骤：
1.建立连接时，客户端发送SYN包到服务器（SYN=1，seq=x），其中x为随机生成的x，进入SYN-SENT状态，等待服务器确认
2.服务器收到SYN确认包，同时发送SYN包和ACK确认包，其中ack为从客户端发送过来的序列号+1，同时生成一个自己的序列号发送过去，进入SYN-RECV状态
3.客户端接收到服务端发送过来的SYN和ACK包之后，向服务器发送一个ACK包来确认连接，此后进入ESTAB-LISHED状态

第六章 应用层 

6.1.1 分布式域名系统DNS（着重看DNS 解析的含义） 

DNS是互联网使用的命名系统，把域名转化为IP地址。 
域名-->IP地址解析过程： 当一个应用进程需要把主机名解析为IP地址时，该应用进程就调用解析程序，并成为DNS 的一个客户，
把待解析的域名放在DNS的请求报文中，以UDP用户数据报的方式发给本地域名 服务器（使用UDP是为了减少开销）。
本地域名服务器在查找域名以后，把对应的IP地址放 在回应报文中返回。
应用进程获得目的主机IP地址后即可进行通信。 

6.4.1 万维网概述 

万维网是一个大规模的、联机式的信息储藏所，用链接的方法能非常方便地从互联网上地一 个站点访问另一个站点，从而主动的按需获取信息。 
万维网是一个分布式的超媒体系统，是超文本系统的扩充。 
万维网以客户服务器方式工作。客户程序向服务器程序发出请求，服务器程序向客户程序送 回客户所要的万维网文档。 

6.4.2 统一资源定位符URL格式 

用来表示从互联网上得到的资源位置和访问这些资源的方法。

URL给资源的位置提供一种抽 象的识别方法，并用这种方法给资源定位。 

URL标志万维网上的各种文档，实际上就是在互联网上资源的地址，使得每一个文档在互联 网范围内具有唯一的标识符URL。 

URL格式：<协议>://<主机>:<端口>/<路径> <协议>：指使用什么协议来获取该万维网文档。最常用的协议是HTTP，其次是FTP（文件传输 协议）。 

://：是规定的格式。 <主机>：它指出这个万维网是在哪一台主机上。这里的主机指的是该主机在互联网上的域名。 

端口、路径：有时可省略。 HTTP的URL格式：http://<主机>:<端口>/<路径> 

6.4.3 超文本传输协议HTTP（HTTP的操作过程）

本章将结合前 4 章的内容共同考查：主机访问一个网页的具体过程。主要考查访问一个网 页的过程中具体能用到哪些协议。
