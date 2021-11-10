# ~~DES加密算法

（参考链接：[1](https://www.cxyxiaowu.com/1478.html)	[2](https://www.cnblogs.com/idreamo/p/9333753.html) ）

## Feistel结构

许多分组密码都采用Feistel结构，这样的结构由许多相同的轮函数组成。每一轮里，对输入数据的一半进行代换，接着用一个置换来交换数据的两个部分，扩展初始的密钥使得每一轮使用不同的子密钥。

## 混淆与扩散的概念

confusion and diffusion

![image-20211028211114338](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211028211114338.png)



![image-20211028192750757](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211028192750757.png)



![image-20211028205522151](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211028205522151.png)

## 密钥的生成（16轮），了解即可

![image-20211028195220169](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211028195220169.png)

## 加密部分（重点掌握）

![image-20211028200954907](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211028200954907.png)



![image-20211028205154324](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211028205154324.png)

## 最后还有一个逆置换的过程（逆置换是对初始换位的逆过程）

初始（左） 逆置换（右）

![image-20211028205709630](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211028205709630.png)![image-20211028205724695](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211028205724695.png)



# ~~流密码（分组密码学）

![image-20211028210128769](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211028210128769.png)

![image-20211028210237536](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211028210237536.png)



# ~~攻击类型（5

### ① 惟密文攻击（只有密文文本，爱看不看

（Ciphtext-only attack）

在惟密文攻击中，[密码分析](https://baike.sogou.com/lemma/ShowInnerLink.htm?lemmaId=109141&ss_c=ssc.citiao.link)者知道密码算法，但仅能根据截获的密文进行分析，以得出明文或密钥。由于密码分析者所能利用的数据资源仅为密文，这是对密码分析者最不利的情况。

### ②已知明文攻击（攻击者无法询问，给什么用什么

（Plaintext-known attack）

已知明文攻击是指密码分析者除了有截获的密文外，还有一些已知的“明文—密文对”来[破译密码](https://baike.sogou.com/lemma/ShowInnerLink.htm?lemmaId=59615543&ss_c=ssc.citiao.link)。密码分析者的任务目标是推出用来加密的密钥或某种 算法，这种算法可以对用该密钥加密的任何新的消息进行解密。

### ③ 选择明文攻击（有明文 问密文

（Chosen-plaintext attack）

[选择明文攻击](https://baike.sogou.com/lemma/ShowInnerLink.htm?lemmaId=109552&ss_c=ssc.citiao.link)是指密码分析者不仅可得到一些“明文—密文对”，还可以选择被加密的明文，并获得相应的密文。这时密码分析者能够选择特定的明文[数据块](https://baike.sogou.com/lemma/ShowInnerLink.htm?lemmaId=8783783&ss_c=ssc.citiao.link)去加密，并比较明文和对应的密文，已分析和发现更多的与密钥相关的信息。

密码分析者的任务目标也是推出用来加密的密钥或某种算法，该算法可以对用该密钥加密的任何新的消息进行解密。

### ④ 选择密文攻击（有密文 问明文

(Chosen—ciphenext attack)

[选择密文攻击](https://baike.sogou.com/lemma/ShowInnerLink.htm?lemmaId=68330277&ss_c=ssc.citiao.link)是指[密码分析](https://baike.sogou.com/lemma/ShowInnerLink.htm?lemmaId=109141&ss_c=ssc.citiao.link)者可以选择一些密文，并得到相应的明文。密码分析者的任务目标是推出密钥。这种 密码分析多用于攻击 [公钥密码体制](https://baike.sogou.com/lemma/ShowInnerLink.htm?lemmaId=8442176&ss_c=ssc.citiao.link)。



# ~~有限群 无限群

单纯指群元素个数 个数即为阶

（参考资料： [1](https://zhidao.baidu.com/question/237393210)群环域   [2](https://www.cnblogs.com/chester-cs/p/11657977.html)有限域 ）

![image-20211028214622849](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211028214622849.png)

## 环：<R,+,*>

（R，+）为可交换群：（满足，封闭、交换、结合、单位元、逆元

（R，*）为含幺半群：（满足，结合、单位元

（* 对 +）满足分配律

## 交换环

在上面的基础上满足（乘法交换律

## 整环

在上面的基础上满足（无零因子

无零因子：环乘法对任意两个元素的运算结果不为零（否则a为零**或**b为零

## 域：<R,+,*>

在整环的基础上，对乘法满足乘法逆元（除0以外，任意元素都有乘法逆元

## 有限域GF(p)

•有限域的阶(元素个数)必须是一个素数的幂p^n, n 为正整数。元素个数是p^n的有限域一般记为GF(p^n)，即Galois fields, 模p^n.

•关注两种特殊情形，n=1时的有限域和p为2时的有限域，即GF(p)和GF(2^n)

•最简单的有限域是GF(2)，它的代数运算简述如下：

```C++
/*
+ 0 1       x 0 1         w  -w  w-1

0 0 1       0 0 0         0  0  

1 1 0       1 0 1         1  1   1

   加          乘            求逆
   **加等于异或操作，乘等价于逻辑与**
   */
```

其中有限域GF（P）是关于素数P的（mod P）剩余类

![image-20211028215952800](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211028215952800.png)

![image-20211028220025915](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211028220025915.png)

此处⬆   （满足规律  **加等于异或操作，乘等价于逻辑与**

实际做运算时：加法视为GF（2） 加法后做（mod 2）处理 **对此：更清晰的解释为：**

![image-20211028221551746](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211028221551746.png)

![image-20211028220042132](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211028220042132.png)

多项式的最大公因子（略）es：与数字的求法一样 gcd（a‘，b’）

### 不可约多项式

​       定义：不能写成两个次数较低的多项式乘积形式的多项式（即只有1和其本身两个约数，又称不可约多项式

​		**即约多项式即相当于素数**

###  本原多项式（了解

​        定义：若n次不可约多项式的阶为时，称作本原多项式

​		其中：①  n次的意思就是多项式最高项次数为n②  不可约多项式的阶就是指多项式的周期

### 伽罗华域的运算补充

![image-20211029110349181](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211029110349181.png)

### 关于即约多项式的mod 运算

（算法原初 &未优化版本

![image-20211028225108800](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211028225108800.png)

上图中⬆

f(x)*g(x) =1000  0011 * 101  0111 

​			    = 10  1011  2111  1221  (each mod 2) 

​				= 10  1011  0111  1001

通俗易懂版本：

![image-20211029112616424](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211029112616424.png)

![image-20211029112558942](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211029112558942.png)

#### **做了一些题目后的发现：**

（使用乘法直接算其实也快  优化的计算方法一言难尽 不过确实快了许多（：节省稿纸

### 有限域GF(P)的生成元

![image-20211029131927840](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211029131927840.png)

关于生成元的计算了解即可（阶 to 乘数因子

![image-20211029132113521](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211029132113521.png)

![image-20211029172200281](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211029172200281.png)



# ~~~DES加密算法（3DES）

补充：des密钥原本64位，但只有56位是需要认为装填的，剩余8位是奇偶校验位。故对1DES的最坏密钥穷举攻击需要2^56

次的测试，中途相遇攻击其实和hash攻击中的生日攻击很类似。

## 双重des加密

（按顺序的两次加密 同时对应的有两把钥匙--》

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211029172652556.png" alt="image-20211029172652556" style="zoom: 80%;" />

但是遇到 中途相遇攻击时 ，密钥长度相当于只有56位；

![image-20211029174712552](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211029174712552.png)



## 三重DES加密

![image-20211029175059649](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211029175059649.png)

密钥总长度168位，

```
加密过程：C=E1  (  D2  (  E3  (  m  )  )  )

解密过程：P=D1  (  E2  (  D3  (  m  )  )  )
```

# ~~~AES加密算法

征集标准：128位分组长度，密钥长度为128 /192 /256比特。

![image-20211029175755935](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211029175755935.png)

## **Rijndael密碼系統的數學背景**

同DES算法使用了 **伽罗华域的计算**

<img src="https://pic4.zhimg.com/80/v2-b22e3bdd7da5ddf5ea6ff71909dac4b7_720w.jpg" alt="img" style="zoom: 80%;" />

参考资料：反正[不考](https://zhuanlan.zhihu.com/p/78913397)，爱谁谁（AES加密

## 安全性

![image-20211029183450709](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211029183450709.png)

# ~~~分组加密的工作模式

参考资料：1 很 [重要的部分](https://zhuanlan.zhihu.com/p/128582757)

## ECB（电码本模式）：

### 1、介绍

​		ECB可以说是分组密码的四种工作模式中最好理解的一种啦，也是最简单的一种运行模式，它一次对一个64bit的明文分组利用相同的密钥进行加密，当密钥取定时，对明文的每一个分组，都有一个惟一的密文与之对应。因此形象地说，可以认为有一个非常大的电码本，对任意一个可能的明文分组，电码本中都有一项对应于它的密文。

​		如果消息长于64比特,则将其分为长为64比特的分组，最后一个分组如果不够64bit，则需要对这个分组进行填充。解密过程也是一次对一个分组解密，而且每次解密都使用同一密钥。 我们来具体看一下他的加密流程：

![img](https://pic4.zhimg.com/80/v2-89293bc0bae4a05660dede34502bf18f_720w.jpg)

```c++
//将明文P分为大小为64位的N组；
//对每一个分组，使用同一个密钥K对其加密
//对每一个分组，密码本中都至少有一个可以与其对应
```

在图中可以看到，p1、p2、......、pN分别是64bit的明文分组序列，而其在经过分组密码加密以后的密文分别为：c1、c2、......、cN。

### 2、缺陷

ECB既然如此简单，那它就不可避免的存在很多问题。

1.  同样的平文块会被加密成相同的密文块；因此，它不能很好的隐藏数据模式
2.  不是很适合对流数据进行加密
3.  消息必须被填充到块大小的整数倍

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211029195319948.png" alt="image-20211029195319948" style="zoom: 67%;" />

```c
//在传输短消息（如DES密钥）时，很实用
//ECB加密后的密文仍可通过结构分析破解
//ECB的混淆与扩散做的不好
```

## CBC（密码分组链接模式）

### 1、介绍

​		由于ECB在安全性上存在一些缺陷，为了处理好这个问题，可以让重复的明文分组产生不同的密文分组，又设计出一种CBC模式，它可满足这一要求。

​		它一次使用同一密钥对一个明文分组加密，加密算法的输入是当前明文分组和前一次密文分组的异或，因此加密算法的输入不会显示出与这次的明文分组之间的固定关系，所以重复的明文分组不会在密文中暴露出这种重复关系，而在解密时，每一个密文分组被解密后，再与前一个密文分组异或，由此来产生明文分组。

<img src="https://pic4.zhimg.com/80/v2-d0457c9f36261b362669345efafb7973_720w.jpg" alt="img"  />

两种计算IV的方法：

1.用加密函数加密一个时变值，所用密钥和明文加密所用密钥相同。这个时变值对每次加密运算来说必须唯一。例如：时变值可以是一个计数器，一个时间戳或者消息数目。

2.第二种方法是用随机数发生器产生一个随机数分组。

```c
/*加密过程*/
//step 0:明文
//step 1:明文（异或）上一次密文
//step 2:DES加密
//step 3:密文

/*解密过程*/
//step 0:密文
//step 1:DES解密
//step 2:密文（异或）上一次密文
//step 3:明文
```

### 2、缺陷

1.  CBC模式相比ECB有更高的保密性
2.  解密可以并行进行



1.  对每个数据块的加密依赖与前一个数据块的加密所以加密无法并行
2.  不是很适合对流数据进行加密
3.  消息必须被填充到块大小的整数倍

![image-20211029201752490](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211029201752490.png)

```C
//解密可以并行（话说ECB也可以

//加密无法并行
//引入了初始向量IV，需要使用ECB提前告知
//数据不规整是需要填充
//攻击者改变P1或者IV中的某些位，那么后面的所有数据都会改变
```

## CFB（密码反馈模式）

### 1、介绍

（**将DES分组转换为DES流**

​		我们都知道DES是分组长为64bit的分组密码，但利用CFB模式或OFB模式**可将DES转换为流密码**。因为流密码不需要对消息填充，而且运行是实时的。因此如果传送字母流，可使用流密码对每个字母直接加密并传送。

​		流密码的明文和密文长度是相同的，因此，如果需要发送的每个字符长为16bit，就应使用16bit的密钥来加密每个字符。如果密钥长超过16bit，就会造成密钥的浪费。

​		下图是CFB模式示意图，设传送的每个单元(如一个字符)是j bit（一般情况下取j=8），与CBC模式一样，明文单元被链接在一起，使得密文是前面所有明文的函数。

![image-20211029203831794](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211029203831794.png)

![img](https://pic4.zhimg.com/80/v2-fa676d6fd3ece888aeb3f096daa0362f_720w.jpg)

#### **看不懂？比较CBC与CFB**

![img](https://img-blog.csdn.net/20180903220102338?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2NoZW5ncWl1bWluZw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

![image-20211029204702524](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211029204702524.png)

```c
//其他明文异或后直接参与加密，CFB明文不参与加密只参与异或
//加密流程
/*
step 1:上一次的密文加入移位寄存器
step 2:DES加密
step 3:移位寄存器丢弃j位

step 4:明文
step 5:异或（移位寄存器
step 6:密文
*/
//解密流程
/*
step 1:上一个密文加入以为寄存器
step 1:DES加密
step 1:移位寄存器对其j位

step 1:密文
step 1:异或（以为寄存器
step 1:明文
*/
```

### 2、缺陷

l、当数据以位或字节形式到达时使用都是适当的 

2、最通用的是流密码形式 

-   明文的改变会影响接下来所有的密文，因此加密过程不能并行化，但是解密过程是可以并行化的
-   在解密时，密文中一位数据的改变仅会影响两个明文块：对应平文块中的一位数据与下一块中全部的数据，而之后的数据将恢复正常
-   CFB拥有一些CBC所不具备的特性，这些特性与OFB和CTR的流模式相似：只需要使用块密码进行加密操作，且消息无需进行填充
    CBC模式除了能够获得保密性以外，还能用于认证。

## OFB（输出反馈模式）

OFB模式与CFB模式都有异曲同工之妙，但是不同点在于，OFB是将加密算法的输出反馈到移位寄存器，而CFB是将密文直接反馈到移位寄存器。

![img](https://pic2.zhimg.com/80/v2-942f1bd34096a8278766cabc74fd4765_720w.jpg)

### 共同讨论OFB与CFB的不同

结构上类似CFB，但是OFB中加密函数输出被反馈回移位寄存器，CFB中是密文单元被反馈回移位寄存器。优点是传输中的比特差错不会传播，缺点是比CFB更容易受报文流篡改攻击。

![image-20211029210442413](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211029210442413.png)

## CRT（计数器模式）

![image-20211029210911201](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211029210911201.png)

![image-20211029210930198](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211029210930198.png)

![image-20211029210945860](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211029210945860.png)



# 这一部分的整理完成了 命名为abc_1.pdf



































