# 定义区块链技术

> 原文：<https://www.edureka.co/blog/blockchain-technology/>

对加密货币的兴起感到兴奋吗？想知道区块链技术是如何工作的？你来对地方了。这个博客会让你理清头绪，让你对区块链有更好的了解。

**以下将是本博客的学习:**

*   [定义区块链技术](#Defining%20Blockchain)
*   [简单的比特币交易](#Bitcoin%20transaction)
*   [区块链:一组技术](#Blockchain%20technology)
*   [区块链类型](#Blockchain%20types)
*   [区块链技术用例](#Blockchain%20uses)
*   [可能的区块链构造转变](#tectonic%20shift)

**在我开始之前先抬起头来！！**

曾经想象过一个如此安全&强大的系统，可以改变我们的经济、治理系统、商业运作的方式，并可能改变我们对贸易、所有权以及信任的概念。嗯，这样的技术已经存在，叫做**区块链**。

**似乎很吸引人？让我们一起揭开这个谜团……**

## **定义区块链技术**

区块链是一个反向链接、去中心化和分布式的加密记录数据库。

好吧，如果这些话看起来令人困惑，那么让我来给你解释一下:

*   这是一种数据结构，其中每个块都以**时间戳**时间顺序链接到另一个块
*   这是一个**只附加的事务数据库**，不是传统数据库的替代品
*   每个节点保留一份过去发生的所有交易的副本，这些交易由**加密保护**
*   所有信息一旦存储在分类帐中，都是可验证和可审计的，但**不可编辑**
*   高度**容错**因为有**无单点故障 ![Blockchain-Blockchain-Technology-Edureka](img/94c455bf87c6f5d05bef3872b6553bad.png)** 

由于区块链没有将 概念化为 本身就是一个单独的实体，它是比特币的主干技术，所以我们要试着用比特币的用例&来理解它是如何帮助安全地转移这个**数字黄金**。

## **区块链技术|区块链教程|爱德华卡**

[//www.youtube.com/embed/g5ExoEfnXNU?rel=0&showinfo=0](//www.youtube.com/embed/g5ExoEfnXNU?rel=0&showinfo=0)

## **简单的比特币交易**

考虑一笔比特币交易，其中，詹姆斯在网络中转账 **5** **BTC** 他的朋友凯文。![Blockchain Technology- Bitcoin transaction-edureka](img/e5a0036c0af11556334f248f101808a4.png)

现在，这个交易被广播到**比特币区块链网络**，被称为**矿工**的特殊节点从*未确认交易*的池中拿起这个交易，验证它并将其添加到他们的区块中。![Blockchain Technology-Miners-Edureka](img/8ac3424720ab49d1d0bf06fc7ff1a7a7.png)

这里，假设 Lisa 和 Robert 是矿工，他们验证网络中的交易，并将验证的交易分组到一个块中，并开始竞争解决一个名为 ***的复杂数学难题，工作证明*** 。

如果丽莎先解决了这个难题，她会向整个网络广播这个信息块。其他挖掘者验证该块，并且每个节点一致同意分类帐的当前状态，每个节点独立地更新记录。因此，James 和 Kevin 收到一条确认消息，表明交易已经完成。![Blockchain Technology-ledgers-edureka](img/efd2c22eaf5b7ec6a2e62c2f42011b42.png)

交易因此成为通用 ***分布式账本*** (或区块链)的一部分。而且，由于她的计算工作，Lisa 获得了新创造的比特币(因此有了术语 *挖掘* )。目前每块奖励 12.5 比特币。

*“因此，数字货币从一个人转移到另一个人，而不需要我们在传统系统中使用的第三方。是不是很神奇？!"*

**然而，区块链技术尽管有其优点，却并不是一项新技术。**

顺便说一下，这是以一种新的方式融合了多种有效的技术。

## **区块链:一组技术![Blockchain Technology- Group of technology-edureka](img/c94bb336f917d3fa2ec6c0de3c7a8c71.png)** 

### **密码算法:**

区块链采用强大的 最先进的加密机制进行保护。区块链上存储的一切都是加密的。

为了让你更好地了解区块链是如何使用的，让我们回到我们之前讨论的例子，凯文将 5 BTC 转移给詹姆斯。这种交易以加密信息的形式进入网络。该消息对于每笔交易都是唯一的。

现在，你可能会问是什么让这一信息独一无二？正是因为交易是由发送方唯一的密钥**、**签名，所以才有了**、*数字签名*。**这个机制看起来是这样的:![Blockchain Technology- Digital Signature-edureka](img/32c4d1901933e5ff496a6cb19edd4d0e.png)

**矿工验证该数字签名，以验证网络中的交易。**

爽。不是吗？让我告诉你一些更有趣的事情。以前见过这些号码:**09 bed8e 02e 49277378 f 256 c 9d 93 ba 4 e 408771088483 f 3955 c 6 b 1186 AC 8 c 7630 a**。看起来像胡言乱语，对吗？嗯，它叫做安全散列算法 **(SHA-256)** 。

这个功能非常强大，如果你把任何东西通过这个算法，它会给你一个这个输入的 ***数字指纹*** 。即使改变了一个空格，指纹也会完全改变。

**想知道在区块链上是怎么用的？**记得我告诉过你，在区块链中，区块是相互反向链接的。好吧，这就对了。如果你对一堆交易进行哈希运算，也就是说，给整个交易“块”一个唯一的指纹！就是这样。

现在，您的下一个事务块有了新的事务— *加上来自前一个块的*。![Blockchain Technology- cryptographic Security-edureka](img/10ed58fcafa2c1e7d470a756b55b3162.png)

这就是区块链系统如何被加密保护的。

### **分布式网络:**

区块链使用分布式网络，其中两个或多个节点以协调的方式相互合作，以实现共同的结果。x 区块链上的所有用户都是维护自己账本的节点(或对等体)。

| 

*   在分布式架构中，交易点对点传输
*   通过网络传输交易大约需要 1-2 秒

*更快的交易流程使验证流程对同行来说更快捷。这最终会加快数字资产的传输速度。* | ![Blockchain Technology- Distributed network-edureka.png](img/1211f1ef4899474307a896a31624ee3d.png) |

### **程序(区块链协议):**

区块链使用网络服务协议，实现系统的平稳安全运行。这些节点通过维护交易记录来服务于网络。可以为每个区块链定制验证流程。基本上，管理区块链网络的是**共识机制**。*比特币区块链工作证明示例。*

| Consensus does two things: 

*   它确保了区块链中的下一个块是真理的唯一版本
*   它防止强大的对手破坏系统

更快的交易过程使得同行的验证过程更快。这最终会加快数字资产的传输速度。 | ![Blockchain Technology-consensus mechanism-edureka](img/949ceb00a8e6fcd628546c1f7f642512.png) |

**我想现在你知道这些常规概念是如何在区块链技术中使用的了。让我向你展示这个系统如何运作的视觉图形![Blockchain Technology- Blockchain working-edureka](img/f456f02ecc8ba750daba4d98b5142cbc.png)** 

好吧，让我们继续讨论区块链的类型。

## **区块链类型:![Blockchain Technology- Blockchain types-edureka](img/5d7d540ee5ce81bb7600bd2d8316d277.png)** 

***公共:*** 公共区块链的分类帐对互联网上的每个人都是可见的，任何人都可以核实并向区块链添加大宗交易。

**举例——**比特币、以太坊、Dash、Factom

***私有:*** 所有权限都集中到一个组织。私有区块链仅允许组织中的特定人员验证和添加交易块，但通常允许互联网上的每个人查看。

**举例-** 多链、块堆栈

***财团:*** 由财团成员控制。只有预定义的节点集有权写入数据或数据块。

**举例-** 涟漪，R3 & Hyperledger1.0

## **区块链技术使用案例:![Blockchain Technology- Monetary aspects-edureka](img/e93f29e3013494759368bc8946fdf7ed.png)** 

*货币方面只是区块链技术的冰山一角。区块链是一项突破性的技术，金钱只是其中一种可能的应用。*

**以下是区块链的一些 现实应用:**

![Blockchain Technology-use cases-edureka](img/5bb44d4e40308165ee8ab287a517ac3f.png)

现在让我给大家展示一下区块 链技术是 走向 引领我们在 不远的将来。

## **可能的区块链构造转变:**

根据世界经济论坛的调查，区块链技术有望取得以下进步。

![Blockchain Technology-tectonic shift-edureka](img/decf469f3e3638bc20a4eaf2aedfa0b2.png)

我们的区块链技术博客到此结束。我希望你喜欢阅读这个博客，并发现它的信息量。要了解更多关于区块链的信息，请观看我们关于“区块链技术”的视频

[https://www.youtube.com/embed/_M7oDW6v8js?rel=0&showinfo=0](https://www.youtube.com/embed/_M7oDW6v8js?rel=0&showinfo=0)

## **区块链技术|区块链讲解|区块链教程|爱德华卡**

*有问题吗？请在评论区提到它，我们会尽快回复您。*

*如果你希望了解区块链技术，掌握密码学、区块链网络、智能合约、以太坊和超级账本的概念，请在这里查看我们的互动在线直播 [**区块链认证**](https://www.edureka.co/blockchain-training) ，它将提供 24*7 支持，在整个学习期间为你提供指导。*