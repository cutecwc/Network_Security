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

AES算法使用了 **伽罗华域的计算**

![image-20211102204950984](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211102204950984.png)

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







# [密码学第一部分](https://www.w3cschool.cn/moderncryptography/moderncryptography-nrh338ui.html)

## 一、素数

无

## 二、模运算

### 取模和取余的区别

![image-20211029212006615](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211029212006615.png)

（解释：取模 模数为正 结果为正，即同号原则；而取余要求余数尽可能小*绝对值

## 三、费马定理

![image-20211029214446532](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211029214446532.png)

P是素数，a与P互素，有a^(p-1) mod p = 1;

​							other is: a^(p) = a mod p;

### 第一种证明方式（数学归纳法

![image-20211029221802518](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211029221802518.png)

参考资料：[证明](https://zhuanlan.zhihu.com/p/87611586)

### 另一种证明思路（剩余系法

```c
/*
开始费马小定理的证明：
P是质数

0,1,2,3,4…p-1是p的完全剩余系（都与P没有比1大公因子）

∵a,p互质

∴a, 2a, 3a, 4a …(p-1)a 也是mod p的完全剩余系{a, 2a, 3a, 4*a …(p-1)*a}mod p ≡ {0,1,2,3,4…p-1}

∴1 2 3…(p-1)≡1a 2a 3a…(p-1)*a (mod p)

∴ (p-1)! ≡ (p-1)! * a^(p-1) (mod p)

两边同时约去(p-1)!

a^(p-1)≡1(mod p)
*/
```

排版优化版（课本证明法（不全面

![image-20211030111438346](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211030111438346.png)

### 引理

若a，b，c为任意3个整数,m为正整数，且(m,c)=1，则当a·c≡b·c(mod m)时，有a≡b(mod m)。 证明：a·c≡b·c(mod m)可得ac–bc≡0(mod m)可得(a-b)·c≡0(mod m)。因为(m,c)=1即m,c互质，c可以约去，a– b≡0(mod m)可得a≡b(mod m)。

## 四、欧拉定理

### 欧拉函数φ(n)

定理：p和q不相等素数, n=p*q, φ(n)= φ(p) φ(q) = (p-1) (q-1)

```c
/*
考虑余数集合{0, 1, …, (pq-1)}中
不与n互素的余数集合是{p, 2p, …, (q-1)p}, 
				{q, 2q, …, (p-1)q}
				和0, 
所以φ(n) = pq-[(q-1)+(p-1)+1]
		=pq-(p+q)+1
		=(p-1)(q-1)
		=φ(p)φ(q)
		
整理得：
考虑模为n的数集Zn = {0, 1,2,....,pq -1}而不和n互质的集合由下面三个集合的并构成：
1) 能够被p整除的集合{p,2p,3p,....,(q-1)p} 共计q-1个
2) 能够被q整除的集合{q,2q,3q,....,(p-1)q} 共计p-1个
3) {0}
很显然，1、2集合中没有共同的元素，
因此φ(n)中元素个数 ＝ pq-1 -(p-1）-(q-1) = (p-1)(q-1) 
*/
```

**⬆这个不难证明，想法起点是构造与素数的互素集合**

### 欧拉定理

![image-20211029223810388](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211029223810388.png)

欧拉定理的证明：用到了一个等价排列的概念

![image-20211030113720610](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211030113720610.png)

## 五、中国剩余定理（CRT）

对中国剩余定理的描述：

![image-20211030120052218](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211030120052218.png)

```c
/*
对每一个i, i=1,…,t, gcd(di,n/di)=1, 存在yi, 使得
		(n/di)*yi mod di=1;
    进一步地, (n/di)*yi mod dj=0, j≠i, (因为dj是(n/di)的一个因数)
        令x=[(n/di)*yi*xi] mod n. 
	∵ x mod di = (n/di)*yi*xi mod di = xi, ((n/di)*yi mod di =1)
	∴ x是x mod di=xi (1≤i≤t)的公共解。
/*
```

在上述证明中 ，重点抓住 x mod di=xi 这个关键点；

**在求解剩余解时，实际是在求解乘法逆的过程。**

## 六、Discrete Logarithms

**离散对数**是包括**Diffie-Hellman密钥交换**和**数字签名(DSA)**在内的许多公钥算法的基础。

![image-20211030165345510](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211030165345510.png)

**记本原根a，由a^i生成的（mod p）循环结果为dlog的值。**

## 七、第一部分章节小结

![image-20211030165557828](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211030165557828.png)

# 密码学第二部分

## 八、RSA加密算法

### 对称密码的不足

```c
/*
加密能力与解密能力是捆绑在一起的
密钥分发困难：分发依赖于安全信道
密钥管理困难：对于每对用户都需要一个独特密钥，在一个1000人的局域网中，这个数量为（1000，2）
无数字签名
无法实现两个不认识的人的秘密通讯：无法第一时间给出公共密钥
*/
```

### 非对称密码

```c
/*
明文：算法的输入，可读信息或数据
加密算法：对明文进行各种转换
公钥和私钥：算法的输入，分别用于加密和解密(对于对称就多了一个公私钥的概念)
密文：算法的输出，依赖于明文和密钥
解密算法：根据密文和密钥，还原明文
*/
```

### 加密 签名

显然选择后者，解释略

### 单向陷阱函数

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211030171543026.png" alt="image-20211030171543026" style="zoom: 67%;" />



```c
/*
**仅满足(1)、(2)两条的称为单向函数；第(3)条称为陷门性，z 称为陷门信息

**当用陷门函数f作为加密函数时，可将f公开，这相当于公开加密密钥，此时加密密钥便称为公开钥，记为Pk
**f函数的设计者将z保密，用作解密密钥，此时z称为秘密钥匙，记为Sk。由于设计者拥有Sk，他自然可以解出x=f-1(y)
**单向陷门函数的第(2)条性质表明窃听者由截获的密文y=f(x)推测x是不可行的
*/
```

### 非对称密码 攻击

1、公钥穷举攻击

2、数学上未证明 单向陷门函数 是安全的

3、消息穷举攻击（公钥透明 可以把消息试出来，解决方法：可以在消息后附加随机数？？

### RSA流程

**用公钥加密，用私钥解密（对于签名反之，重点理解**

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211030172544942.png" alt="image-20211030172544942" style="zoom:50%;" />

```c
/*
1	select p q
2	n=pq
3	φ(n)=(p-1)(q-1)
4	select e
5	ed=1 mod φ(n)
------------------
C=P^e mod n加密
P=C^d mod n解密
*/
```

### RSA证明

#### 命题：![image-20211030173812538](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211030173812538.png)

命题关键：

***证明：M^k(p-1)(q-1)+1 mod p ?= M mod p ;分M-p互素与不互素两种情况***

![image-20211030190727764](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211030190727764.png)

![image-20211030190743881](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211030190743881.png)

### RSA攻击方法

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211030192919092.png" alt="image-20211030192919092" style="zoom:67%;" />

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211030193101090.png" alt="image-20211030193101090" style="zoom:67%;" />

### RSA 其他部分

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211030193027480.png" alt="image-20211030193027480" style="zoom:67%;" />

RSA 优缺点

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211030193139643.png" alt="image-20211030193139643" style="zoom:67%;" />

## 九、Diffie-Hellman

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211030193452162.png" alt="image-20211030193452162" style="zoom:67%;" />

**密钥交换协议**

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211030193545086.png" alt="image-20211030193545086" style="zoom:67%;" />

## 十、公钥分配问题

### 公钥的公开发布

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211030211441855.png" alt="image-20211030211441855" style="zoom:67%;" />

```c
//任何人都可以伪造A发布A的公钥
```

### **公开可访问的目录**

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211030211627564.png" alt="image-20211030211627564" style="zoom:67%;" />

```c
//一旦有人取得管理者私钥，可以对目录修改，窃取消息
```

### **公钥授权**

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211030211756701.png" alt="image-20211030211756701" style="zoom:67%;" />

```c
//复杂
//管理端负荷大且一旦下线 A与B就无法沟通
```

### **公钥证书**

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211030212014957.png" alt="image-20211030212014957" style="zoom:67%;" />

## 十一、密钥交换

### 两个不安全的版本

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211030212851956.png" alt="image-20211030212851956" style="zoom:50%;" />

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211030212915520.png" alt="image-20211030212915520" style="zoom: 50%;" />

第一个可以被 中间人攻击（过于简单

第二个可以被 重放攻击（解决方法是将3、4合并

### **Diffie-Hellman密钥交换**

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211030221716523.png" alt="image-20211030221716523" style="zoom:67%;" />

#### 举个栗子

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211030221825663.png" alt="image-20211030221825663" style="zoom:67%;" />

数字太大 别算了 看看就好

### **ElGamal密码体系**

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211030222756574.png" alt="image-20211030222756574" style="zoom:67%;" />

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211030222811534.png" alt="image-20211030222811534" style="zoom:67%;" />

文字描述：

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211030223323464.png" alt="image-20211030223323464" style="zoom:67%;" />

#### 举个栗子

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211030225613950.png" alt="image-20211030225613950" style="zoom:67%;" />

多练一练吧>>>>>>>>>>>>

# 密码学第三部分

## 十二、消息认证

消息认证是用来验证消息完整性的一种机制或服务。消息认证确保收到的数据确实和发送时的一样(即没有修改、插入、删除或重放)，且发送方声称的身份是真实有效的。

对称密码在那些相互共享密钥的用户间提供认证。用消息发送方的私钥加密消息也可提供一种形式的认证。

**关键：1、机密性，2、认证性，3、不可否认性，4、完整性**

## 十三、消息认证 问题

```c
/*

第二个问题，消息认证和数字签名的区别是什么？

消息认证码和数字签名都属于哈希函数应用（消息完整性）的范畴，数字签名其实也是一种消息认证技术，但是数字签名属于非对称密码体制，而消息认证码属于对称密码体制，所以消息认证码的处理速度也会比数字签名快很多，但是消息认证码无法实现不可否认性。

作者：知乎用户
链接：https://www.zhihu.com/question/363355112/answer/1187048666
来源：知乎
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。

*/
```

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031134902471.png" alt="image-20211031134902471" style="zoom:67%;" />

可以被分类为：

***A 传输过程中出现的三种问题：（发出时泄密消息，传输时消息被分析，接受到伪装消息***

***B 内容篡改的三个手段：（直接内容修改、调换消息顺序、消息重放***

***C 两个抵赖：（发送方抵赖、接收方抵赖***

## 十四、消息加密

**关键：1、机密性，2、认证性，3、不可否认性，4、完整性**

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031135448755.png" alt="image-20211031135448755" style="zoom: 80%;" />

```c
//	1	2（DES
//	1（用公钥加密
//	2	3（用私钥加密
//	1	2	3（签名了
```

## 十五、FCS帧校验序列

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031135730345.png" alt="image-20211031135730345" style="zoom:80%;" />

```c
/*
1	2（不可并行

1	2（可并行，但不是很安全
*/
```

## 十六、MAC 消息认证码

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031135914434.png" alt="image-20211031135914434" style="zoom: 67%;" />

```c
/*
2	

1	2	4

1	2	4
*/
```

## 十七、HASH 散列函数

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031140425366.png" alt="image-20211031140425366" style="zoom:67%;" />

```c
/*
1	2	4（DES

2	4（未加密M

2	3	4（A的私钥加密HASH值
*/
```

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031140442443.png" alt="image-20211031140442443" style="zoom:67%;" />

```c
/*
1	2	3	4（a的私钥与DES加密

4（S相当于密钥K

1	2	4（但是s可以被否认
*/
```

## 十八、 对比三种消息认证方法

HASH与FCS不需要密钥即可生成、故需要吧生成序列压入加密密文中，对比MAC，HASH具有更强的抗碰撞性

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031141600289.png" alt="image-20211031141600289" style="zoom:67%;" />

# 密码学第四部分

## 十九、数字签名

摘要：（全部签名、摘要签名（确定数字签名、概率数字签名

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031142212052.png" alt="image-20211031142212052" style="zoom: 67%;" />

**认证的目的与功能**

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031142601841.png" alt="image-20211031142601841" style="zoom:67%;" />

### 四种认证(协议)

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031155522242.png" alt="image-20211031155522242" style="zoom:67%;" />

### 双向认证

双向认证协议可以使通信双方达成一致并交换会话密钥

双向认证需要注意重放攻击：

​		解决方法：（序列号；时间戳；随机数（挑战应答

### 可信中继（对称加密方法

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031155943597.png" alt="image-20211031155943597" style="zoom:67%;" />

KDC对（用户生成的会话密钥）加密，完成第一次通讯后使用会话加密



![image-20211101215912142](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211101215912142.png)

### **ElGamal数字签名算法**

***使用EIGamal对明文m签名：***

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031162850469.png" alt="image-20211031162850469" style="zoom: 67%;" />

**关键就是一个式子：**（***m = Xa.r + k.s mod p-1求s***

反过来验证：即验证**a ^ m = ( Ya ^ r )* r ^ s mod p**是否相等

举个栗子：

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031163408704.png" alt="image-20211031163408704" style="zoom:67%;" />

## 二十、认证与Kerberos

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031171600305.png" alt="image-20211031171600305" style="zoom:50%;" />

### KDC

![image-20211031171808383](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031171808383.png)

![image-20211031171655544](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031171655544.png)

![image-20211031171743335](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031171743335.png)

### Kerberos

第三方认证服务--分布式环境下的认证服务

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031172601088.png" alt="image-20211031172601088" style="zoom:67%;" />

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031172620956.png" alt="image-20211031172620956" style="zoom:67%;" />

![image-20211031172943982](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031172943982.png)

![image-20211031172932183](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031172932183.png)

![image-20211031172919282](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031172919282.png)

![image-20211031172906706](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031172906706.png)

![image-20211031172851422](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031172851422.png)

### X.509

![image-20211031172109808](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031172109808.png)

![image-20211031172123855](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031172123855.png)

![image-20211031171916652](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031171916652.png)

#### 建立过程

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031172238031.png" alt="image-20211031172238031" style="zoom:67%;" />

<img src="C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031172304102.png" alt="image-20211031172304102"  />

##### 1

![image-20211031172347852](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031172347852.png)

##### 2

![image-20211031172400505](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031172400505.png)

##### 3

![image-20211031172414784](C:\Users\chens\AppData\Roaming\Typora\typora-user-images\image-20211031172414784.png)

### PKI(了解)









































