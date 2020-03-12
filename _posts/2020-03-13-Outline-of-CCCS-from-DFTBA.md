---
layout:     post                    # 使用的布局（不需要改）
title:      "Amazing Story of Computer Science"           # 标题 
subtitle:   "Outlines of Crash Course Computer Science from DFTBA" #副标题
date:       2020-03-10              # 时间
header-img: "img/cccs.png"          #这篇文章标题背景图片
---

I watched this fantasitic course [Crash Course Computer Science](https://www.bilibili.com/video/av21376839/) in last few days. It was quite a ENJOY！

In case I might forget all about it in the future, I decided to make a outline of it.

Thanks to the effort of [计算机速成课 | Crash Course 字幕组](https://github.com/1c7/crash-course-computer-science-chinese), I extract this outline from the README.md of their repo.

## 第 1 集：计算机早期历史  

提到的设备：算盘 → 步进计算器 → 差分机 → 分析机 → 打孔卡片制表机  

提到的人名：Charles Babbage, Ada Lovelace  

最早的计算设备是算盘，举例如何使用  

Computer 从指代职业变成指代机器  

机器里有名的是：步进计算器。第一个可以做加减乘除的机器  

炮弹为了精准，要计算弹道，二战是查表来做。但每次改设计了就需要做一张新表  

Charles Babbage 提出了 "差分机", 在构造差分机期间，想出了分析机, 分析机是通用计算机  

Lovelace 给分析机写了假想程序，因此成为了第一位程序员  

人口普查 10 年一次.  Herman Hollerith 的打孔卡片制表机大大提升了效率  


## 第 2 集：电子计算机  

提到的设备：继电器 → 真空管 → 晶体管  

20世纪的发展要求更强的计算能力。柜子大小的计算机发展到房间大小  

哈佛  Mark 1 号，IBM 1944 年做的  

继电器，继电器一秒最多 50 次开关  

继电器出 bug （LiuZiyu：真的虫子！）

1904 年，热电子管出现，第一个真空管。改进后变成和继电器的功能一样  

"巨人1号" 计算机在英国 布莱切利园 首次大规模使用真空管。但编程麻烦，还要配置  

1946 年，宾夕法尼亚大学的 ENIAC 是第一个通用可编程计算机  

1947 年，贝尔实验室做出了晶体管，晶体管有诸多好处，IBM 很快全面转向晶体管  

硅谷的典故：很多晶体管和半导体的开发都是这里做的。而生产半导体最常见的材料是硅  

肖克利半导体 → 仙童半导体 → 英特尔  


## 第 3 集：布尔逻辑和逻辑门  

什么是二进制, 为什么用二进制, 布尔逻辑  

3个基本操作：NOT，AND，OR  

解释3个基本操作  

XOR 异或  


## 第 4 集：二进制  

用十进制举例二进制的原理，演示二进制加法。存储单位 MB GB TB 等  

正数，负数，整数，浮点数的表示  

美国信息交换标准代码 - ASCII, 用来表示字符  

UNICODE 1992 年诞生，是字符编码标准， 解决 ASCII 不够表达所有语言的问题  


## 第 5 集：算数逻辑单元 - ALU  

简单介绍 ALU ，英特尔 74181  

ALU 有 2 个单元，1 个算术单元和 1 个逻辑单元  

算术单元  

半加器 (处理1个 bit，2个输入)  

全加器 (处理1个 bit，3个输入)  

8 bit 加法 (1个半加器，7个全加器）  

溢出的概念，吃豆人的例子  

乘法除法  

逻辑单元  

检测数字是否为 0 的电路（一堆 OR 门最后加个 NOT 门）  

ALU 抽象成一个 V 符号  

Flag 标志（是否相等，是否小于，是否溢出等等）  


##第 6 集：寄存器和内存  

本集重点是 Memory （存储 / 内存 两种含义）  

存 1 位  (Gated Latch - 锁存器）  

存 8 位  (Register - 寄存器)  

16x16 的矩阵存 256 位  

数据选择器/多路复用器 (Multiplexer) 解码 8 位地址，定位到单个锁存器  

4 位代表行， 4 位代表列  

组合 256 位内存 + 多路复用器  

可寻址的 256 字节 内存  

一条1980年代的内存，1M 大小  

8个模块，每个模块有32个小方块，  

每个小方块有 4 个小块，每个小块是 128 位 x 64 位  


## 第 7 集：中央处理器（CPU)  

重点  

1. 拼个 CPU 出来  
2. CPU 怎么执行命令  

RAM + 寄存器 + ALU  做个 CPU  

解释  "取指令→解释→执行" 这个循环  

时钟是什么, 时钟速度和赫兹  

超频提升性能, 降频省电  


## 第 8 集：指令和程序  

本集重点：一步步带你运行一遍程序  

回顾上集的例子程序，一步步讲解。介绍”指令集”的概念  

LOAD_A，LOAD_B，SUB，JUMP，ADD，HALT 等指令  

带条件跳转，JUMP NEGATIVE 是负数才跳转，还有其他类型的 JUMP  

真正现代 CPU 用更多指令集。位数更长。  

1971年的英特尔 4004 处理器，有 46 个指令  

如今英特尔酷睿 i7, 有上千条指令  



## 第 9 集：高级 CPU 设计  

早期是加快晶体管切换速度，来提升 CPU 速度  

给 CPU 专门的除法电路 + 其他电路来做复杂操作，比如游戏，视频解码  

给 CPU 加缓存，提高数据存取速度，更快喂给 CPU，用计算餐馆销售额举例  

脏位 -  Dirty bit  

流水线设计，用 1 个洗衣机和 1 个干燥机举例  

并行处理 -  parallelize  

乱序执行 -  out-of-order execution  

推测执行 -  speculative execution  

分支预测 -  branch prediction  

多个 ALU  

多核 (Core)  

多个独立 CPU  

超级计算机，中国的"神威 太湖之光"  


## 第 10 集：早期的编程方式  

本集重点：早期计算机如何编程  

打孔纸卡 → 插线板 → 面板拨开关  

开头说本集重点：程序如何进入计算机  

拿纺织业举例，给机器编程的需求远在计算机出现前就有了  

打孔纸卡 - Punched card  

插线板 - Plugboard  

冯诺依曼架构 - Von Neumann Architecture  

面板编程 - Panel programming  

第一款取得商业成功的家用计算机:  Altair 8800  

编程依然很困难，人们需要更友好更简单的方式编程  

下周主题：编程语言  


## 第 11 集：编程语言发展史  

编程：二进制 → 助记符（汇编器）→ A-0（编译器）→ FORTRAIN  

二进制写程序，先纸上写伪代码，手工转二进制，很快就烦了  

用 "助记符” 写代码（LOAD_A 14）为了把助记符转二进制，汇编器诞生 (Assembler)  

葛丽丝·霍普 (Grace Hopper)  - 哈佛1号计算机首批程序员, 海军军官  

Grace 设计了编程语言 A-0  

Grace 1952 年做了第一个编译器 (Compiler)，实现 A-0  

变量 (Variables)  

FORTRAN  

COBOL  

新语言  

1960 年代：ALGOL，LISP，BASIC  

1970 年代：Pascal，C，Smalltalk  

1980 年代：C++，Objective-C，Perl  

1990 年代：Python，Ruby，Java  


## 第 12 集：编程基础 - 语句和函数  

变量, 赋值语句  

Grace Hopper 拍虫子游戏  

if 判断  

while 循环  

for 循环  

函数  

下集介绍算法  


## 第 13 集：算法入门  

选择排序 - Selection sort  

大 O 表示法 - Big O notation  

归并排序 - Merge sort  

Dijkstra 算法  


## 第 14 集：数据结构  

数组     - Array  

字符串  - String  

矩阵     - Matrix  

结构体  - Struct  

指针     - Pointer  

节点     - Node  

链表     - Linked List  

队列     - Queue  

栈        - Stack  

树        - Tree  

二叉树 - Binary Tree  

图        - Graph  

没时间讲红黑树和堆, 不同数据结构适用不同场景  


## 第 15 集：阿兰·图灵  

介绍图灵  

可判定性问题  

阿隆佐·丘奇，Lambda 算子  

图灵机  

停机问题  

破解德军英格玛加密机  

图灵测试  

图灵的个人生活  

图灵奖  


## 第 16 集：软件工程  

对象  Object  

面向对象编程  Object Oriented Programming.  

API  Application Programming Interface  

public, private  

集成开发环境, IDE - Integrated Development Environments  

调试 debugging  

文档和注释 - readme, comment  

版本控制   Version control  

质量控制   Quality Assurance testing，QA  

Beta, Alpha  


## 第 17 集：集成电路与摩尔定律  

本集重点：晶圆的制作流程：光刻  (04:21~07:42)  

分立元件  Discrete components  

数字暴政  Tyranny of Numbers - 是 1960 年代工程师碰到的问题  

意思是如果想加强电脑性能，就要更多部件，这导致更多线路，更复杂。所以很难做  

光刻         Photolithography  

晶圆         Wafer  

光刻胶     Photoresist  

光掩膜     Photomask  

掺杂         Doping  

摩尔定律   Moore’s Law.  

英特尔      Intel  

晶体管数量大幅度增长, 1980年三万个，1990年一百万个，2000年三千万个，2010年十亿个  

进一步小型化会碰到 2 个问题  1. 光的波长不足以制作更精细的设计  2. 量子隧穿效应  


## 第 18 集：操作系统  

操作系统  Operating systems  

批处理     Batch processing  

计算机变便宜变多，有不同配置，写程序处理不同硬件细节很痛苦，因此操作系统负责抽象硬件  

外部设备         Peripherals  

设备驱动程序   Device drivers  

多任务处理      Multitasking  

虚拟内存         Virtual Memory  

动态内存分配  Dynamic memory allocation  

内存保护         Memory Protection  

1970年代，计算机足够便宜，大学买了让学生用，多个学生用多个 "终端" 连接到主机  

多用户分时操作系统，Multics  

Unix  

MS-DOS  

下集是内存&存储介质  



## 第 19 集：内存&储存介质  

本集重点：存储技术的发展  

纸卡                Paper punch cards  

延迟线存储器  Delay Line Memory  

磁芯               Magnetic Core Memory  

磁带               Magnetic Tape  

磁鼓               Magnetic Drum Memory  

硬盘               Hard Disk Drives  

内存层次结构  Memory Hierarchy  

软盘                Floppy Disk  

光盘                Compact Disk  

固态硬盘         Solid State Drives  


## 第 20 集：文件系统  

文件格式：可以随便存文件数据，但按格式存会更方便  

TXT   文本文件：ASCII  

WAV 音频文件：每秒上千次的音频采样数字  

BMP  图片文件：像素的红绿蓝 RGB 值  

文件系统：很早期时空间小，整个存储器就像一整个文件。后来随容量增长，多文件非常必要  

目录文件：用来解决多文件问题，存其他文件的信息，比如开头，结尾，创建时间等  

平面文件系统 - Flat File System：文件都在同一个层次，早期空间小，只有十几个文件，平面系统够用  

如果文件紧密的一个个前后排序会造成问题，所以文件系统会： 1. 把空间划分成一块块  2. 文件拆分存在多个块里  

文件的增删改查会不可避免的造成文件散落在各个块里，  

如果是磁带这样的存储介质就会造成问题，所以做碎片整理  

分层文件系统 - Hierarchical File System：有不同文件夹，文件夹可以层层嵌套  


## 第 21 集：压缩  

压缩的好处是能存更多文件，传输也更快  

游程编码   Run-Length Encoding  

无损压缩   Lossless compression  

霍夫曼树   Huffman Tree  

"消除冗余"和"用更紧凑的表示方法"，这两种方法通常会组合使用  

字典编码   Dictionary coders,  游程编码 和 字典编码 都是无损压缩  

感知编码   Perceptual coding  

有损压缩   jpeg 格式  

时间冗余   Temporal redundancy  

MPEG-4 视频编码  


## 第 22 集：命令行界面  

本集重点：计算机早期同时输入程序和数据（用纸卡/纸带）  

运行开始直到结束，中间没有人类进行操作，  

原因是计算机很贵，不能等人类慢慢输入，执行完结果打印到纸上 (02:34)  

到1950年代，计算机足够便宜+快，人类和计算机交互式操作变得可行  

为了让人类输入到计算机，改造之前就有的打字机，变成电传打字机 (02:44~05:38)  

到1970年代末，屏幕成本足够低，屏幕代替电传打字机，屏幕成为标配 (07:24)  

人机交互  Human-Computer Interaction  

早期输出数据是打印到纸上，而输入是用纸卡/纸带一次性把程序和数据都给进去  

QWERTY  打字机的发展，克里斯托弗·莱瑟姆·肖尔斯 发明于 1868 年  

电传打字机  Teletype machine  

命令行界面  Command line interface  

ls 命令  

早期文字游戏  Zork  (1977年)  

cd 命令  


## 第 23 集：屏幕与 2D 图形显示  

PDP-1 计算机。键盘和显示器分开，屏幕显示临时值  

阴极射线管  Cathode Ray Tube (CRT)  

CRT 有两种绘图方式：  

量扫描  Vector Scanning  

光栅扫描  Raster Scanning  

液晶显示器   Liquid Crystal Displays (LCD)，像素 (Pixel)  

字符生成器   Character generator  

屏幕缓冲区   Screen buffer  

矢量命令画图  

Sketchpad,  光笔 (Light pen)  

函数画线，矩形  


## 第 24 集：冷战和消费主义  

本集重点：冷战导致美国往计算机领域投入大量资源  (00:00~01:43)  

范内瓦·布什 预见了计算机的潜力，提出假想机器 Memex  

帮助建立 国家科学基金会，给科学研究提供资金  (01:43~03:43)  

1950 年代消费者开始买晶体管设备，收音机大卖  

日本取得晶体管授权后，索尼做了晶体管收音机，为日本半导体行业崛起埋下种子 (03:43~04:29）  

苏联 1961 年把宇航员加加林送上太空，导致美国提出登月  

NASA 预算大大增加，用集成电路来制作登月计算机 (04:29~06:27)  

集成电路的发展实际上是由军事应用大大推进的，阿波罗登月毕竟只有 17 次  

美国造超级计算机进一步推进集成电路 (04:29~07:11)  

美国半导体行业一开始靠政府高利润合同活着，忽略消费者市场，1970年代冷战渐消，行业开始衰败  

很多公司倒闭，英特尔转型处理器 (07:11~08:23)  

末尾总结：政府和消费者推动了计算机的发展  

早期靠政府资金，让技术发展到足够商用，然后消费者购买商用产品继续推动产品发展 (08:23~10:41)  


## 第 25 集：个人计算机革命  

本集：全是历史故事  

1970年代初成本下降，个人计算机变得可行  

Altair 8800  

比尔·盖茨 和 保罗·艾伦写 BASIC 解释器  

乔布斯提议卖组装好的计算机，Apple-I 诞生  

1977年出现3款开箱即用计算机：  

"Apple-II"，"TRS-80 Model I"，"Commodore PET 2001"  

IBM 意识到个人计算机市场  

IBM PC 发布，采用开放架构，兼容的机器都叫 IBM Compatible (IBM 兼容)  

生态系统产生雪球效应：  

因为用户多，软硬件开发人员更愿意花精力在这个平台  

因为软硬件多，用户也更乐意买 "IBM 兼容" 的计算机  

 苹果选封闭架构，一切都自己来，只有苹果在非  "IBM 兼容" 下保持了足够市场份额  


## 第 26 集：图形用户界面 (GUI)  

图形界面先驱：道格拉斯·恩格尔巴特（Douglas Engelbart）  

1970年成立 帕洛阿尔托研究中心（Palo Alto Research Center）  

1973年完成 Xerox Alto(施乐奥托) 计算机  

举例：写一个简单的 GUI 程序  

1981年的 Xerox Star system(施乐之星系统)  

史蒂夫·乔布斯去施乐参观  

所见即所得 WYSIWYG  

1983年推出 Apple Lisa  

1984年推出 Macintosh  

1985年推出 Windows 1.0，之后出到 3.1  

1995年推出 Windows 95 提供图形界面  

1995年微软做失败的 Microsoft Bob  


## 第 27 集：3D 图形  

线框渲染  Wireframe Rendering  

正交投影  Orthographic Projection  

透视投射  Perspective Projection  

网格  Mesh  

三角形更常用因为能定义唯一的平面  

扫描线渲染  Scanline Rendering  

遮挡            Occlusion  

画家算法     Painter's Algorithm  

深度缓冲      Z Buffering  

Z Fighting 错误  

背面剔除      Back Face Culling  

表面法线      Surface Normal  

平面着色      Flat Shading  

高洛德着色   Gouraud shading,  冯氏着色  Phong Shading  

纹理映射      Texture Mapping  

图形处理单元  GPU, Graphics Processing Unit  


## 第 28 集：计算机网络  

局域网   Local Area Networks - LAN  

媒体访问控制地址   Media Access Control address - MAC  

载波侦听多路访问   Carrier Sense Multiple Access - CSMA  

指数退避   Exponential Backoff  

冲突域       Collision Domain  

电路交换   Circuit Switching  

报文交换   Message Switching  

分组交换   Packet Switching  


## 第 29 集：互联网  

IP - 互联网协议 - Internet Protocol  

UDP - 用户数据报协议 - User Datagram Protocol  

校验和 - Checksum  

TCP - 传输控制协议 - Transmission Control Protocol  

DNS - 域名系统 - Domain Name System  

OSI - 开放式系统互联通信参考模型 - Open System Interconnection  



## 第 30 集：万维网  
超链接  Hyperlinks  

URL - 统一资源定位器 - Uniform Resource Locator  

HTTP - 超文本传输协议 -  HyperText Transfer Protocol  


HTML - 超文本标记语言  - HyperText Markup Language  

写一个简单网页，用到了 <h1> <a> <h2> <ol> <li> 标签  

第一个浏览器和服务器是 Tim Berners-Lee 花了 2 个月在 CERN 写的  

1991年正式发布，万维网就此诞生  

开始讲搜索引擎的故事  

Jerry 和 David 的万维网指南 后来改名成 Yahoo  

搜索引擎  JumpStation  

搜索引擎  Google  

网络中立性  


## 第 31 集：计算机安全  

Secrecy, Integrity, Availability  

保密性, 完整性, 可用性  

Threat Model 威胁模型  

身份验证 (Authentication) 的三种方式：  

What you know, 你知道什么  

What you have, 你有什么  

What you are, 你是什么  

访问控制   Access Control  

Bell LaPadula model  不能向上读取，不能向下写入  

隔离 Isolation, 沙盒 Sandbox  


## 第 32 集：黑客与攻击  

社会工程学   Social Engineering  

钓鱼             Phishing  

假托             Pretexting  

木马             Trojan Horses  

NAND镜像  NAND Mirroring  

漏洞利用      Exploit  

缓冲区溢出   Buffer Overflow  

边界检查      Bounds Checking  

代码注入      Code Injection  

零日漏洞      Zero Day Vulnerability  

计算机蠕虫   Worms  

僵尸网络      Botnet  

拒绝服务攻击   DDoS  



## 第 33 集：加密  

多层防御  Defence in depth  

加密 - Encryption，解密 - Decryption  

凯撒加密  Caesar cipher  

替换加密  Substitution cipher  

移位加密  Permutation cipher  

列移位加密  Columnar transposition cipher  

德国 Enigma 加密机  

1977年"数据加密标准" - Data Encryption Standard (DES)  

2001年"高级加密标准" - Advanced Encryption Standard (AES)  

密钥交换 - Key exchange  

用颜色来举例"单向函数"和"密钥加密"的原理  

迪菲-赫尔曼密钥交换 - Diffie-Hellman Key Exchange  

非对称加密 - Asymmetric encryption  

非对称加密算法  RSA  


## 第 34 集：机器学习与人工智能  

分类              Classification  

分类器           Classifier  

特征               Feature  

标记数据        Labeled data  

决策边界        Decision boundaries  

混淆矩阵        Confusion matrix  

未标签数据     Unlabeled data  

决策树            Decision tree  

支持向量机     Support Vector Machines  

人工神经网络   Artificial Neural Network  

深度学习         Deep learning  

弱AI, 窄AI      Weak AI, Narrow AI  

强AI               Strong AI  

强化学习         Reinforcement Learning  



## 第 35 集：计算机视觉  

检测垂直边缘的算法  

核/过滤器  kernel or filter  

卷积 convolution  

Prewitt 算子   Prewitt Operators  

维奥拉·琼斯 人脸检测   Viola-Jones Face Detection  

卷积神经网络   Convolutional Neural Networks  

识别出脸之后，可以进一步用其他算法定位面部标志，如眼睛和眉毛具体位置，从而判断心情等信息  

跟踪全身的标记点，如肩部，手臂等  


## 第 36 集：自然语言处理  

词性                   Parts of speech  

短语结构规则      Phrase structure rules  

分析树                Parse tree  

语音识别             Speech recognition  

谱图                    Spectrogram  

快速傅立叶变换   Fast Fourier Transform  

音素                   Phonemes  

语音合成           Speech Synthesis  



## 第 37 集：机器人  

法国吃饭鸭 - Digesting Duck, Canard Digerateur  

土耳其行棋傀儡, 下国际象棋  

第一台计算机控制的机器出现在1940年代晚期，叫数控机器, Computer Numerical Control(CNC)  

1960年 Unimate，第一个商业贩卖的 可编程工业机器人  

简单控制回路  simple control loop  

负反馈回路  negative feedback loop  

比例-积分-微分控制器   Proportional–Integral–Derivative controller   PID 控制器  

机器人三定律   Three Laws of Robotics  



## 第 38 集：计算机心理学  

我们需要了解人类心理学，做出更好的计算机  

易用度 - Usability  

颜色强度排序 和 颜色排序  

分组更好记，电话号码 317-555-3897 比 3175553897 好记  

直观功能 - Affordances  

认出 vs 回想 Recognition vs Recall  

让机器有一定情商以及 Facebook 的研究  

用软件修正注视位置。让视频通话时看起来像盯着对方，而不是盯着下方  

把机器人做的像人，恐怖谷理论  

有很多开放式的问题，心理学帮助我们明白不同选择可能带来的影响  



## 第 39 集：教育科技  

通过调速，暂停等技巧，加强学习效率  

大型开放式在线课程  - Massive Open Online Courses  (MOOC)  

智能辅导系统 - Intelligent Tutoring Systems  

判断规则 - Production rule  

域模型 - Domain Model  

贝叶斯知识追踪  Bayesian knowledge tracing  

1. 学生已经学会的概率  
2. 瞎猜的概率  
3. 失误的概率  
4. 做题过程中学会的概率  

教育数据挖掘  Educational Data Mining  


## 第 40 集：奇点，天网，计算机的未来  

普适计算  Ubiquitous Computing  

奇点         Singularity  

把工作分为4个象限，讨论自动化带来的影响  

机器人的存在时间可能长过人类，可以长时间探索宇宙  