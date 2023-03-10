# Android 项目:21 点游戏

> 原文：<https://www.edureka.co/blog/android-tutorial-on-blackjack/>

<center>[https://www.youtube.com/embed/PK0ABLwjTJc](https://www.youtube.com/embed/PK0ABLwjTJc)</center>

视频中展示了开发此类应用的设计水平概念。21 点游戏是由希沙布·穆尼尔设计的。

这个 21 点 android 游戏应用程序(21 游戏)非常酷，包括游戏的基本介绍。这款安卓游戏应用中也使用了音效。游戏的背景可以改变，音效也可以关闭。这里使用 Eclipse for Android development 来创建这个应用程序。所以让我们了解一下创建这样一个游戏的架构和步骤。

## **先决条件**

**技能**

以下是创建 Android 游戏所需的技巧:

*   Java 的基础知识
*   良好的 Android 编程知识
*   一个程序员的心思！

**1。游戏的基本前提:**

*   这是一个玩家和庄家之间的比较纸牌游戏

*   你想要比庄家的牌值更接近 21 的牌值。但是，记住，你不希望你的手牌值超过 21。

**2。卡的值:**

[![Android Project - Card values for Blackjack](img/e8d38cc69c7e44702c6ffad1a4b0aaf5.png "Android Project - Card values for Blackjack")](https://www.edureka.co/blog/android-tutorial-on-blackjack/)

3)a 点的值:

*   Ace 的值可以是“1”或“11”。
*   其默认值为 11。
*   如果:总*、【手牌值】*超过 21 *或*(如果你手里有两张 a*(当然，这种情况下手牌值也会超过 21)*，则计为 1。

示例:

**情况 1:** (A，7)的手牌值为 18

**案例二:** (A，7，8)手牌值 16。

I)在情况 1 中，Ace 的值为*‘11’*，而在情况 2 中，Ace 的值为*‘1’*。

ii)卡片‘2’到‘9’:卡片 2 到 9 按其面值标记。

iii) 10，杰克，皇后，国王都是以‘10’估值。

**4。手牌价值/一手牌的价值**

一手牌的价值仅仅是手中每张牌点数的总和。例如，包含(5、7 和 8)的手牌的值为 20。

**5。玩家移动(这些是点击按钮时的动作)**

*   **击**——表示你想抽另一张牌。
*   **停止**–表示您停止在当前总数。
*   **投降**–你将输掉手中赌注的一半。

很好，你已经很了解外行的部分了。不算太寒酸，嗯！

[dl URL = " # " class = ' eModal eModal-15 ' title = "下载代码" desc = " " type = " " align = " " for = " Download "]

快乐学习！

*![android](img/ec9a27372d875b471670c11da624b380.png)有问题吗？在评论区提到它们，我们会给你回复。*

**相关帖子:**

[Android SDK 安装](https://www.edureka.co/blog/android-sdk-installation/)

[开始你的安卓开发历程](https://www.edureka.co/android-development-certification-course)