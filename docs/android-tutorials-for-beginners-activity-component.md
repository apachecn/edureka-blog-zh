# Android 初学者教程第 1 部分:活动组件

> 原文：<https://www.edureka.co/blog/android-tutorials-for-beginners-activity-component/>

在我们之前的帖子中，我们已经解释了如何创建 Android 应用程序 和 [游戏](https://edureka.co/blog/how-to-create-android-games-blackjack/ "How to create Android games") 。然而，这些 Android 教程对于一个对该技术了解有限的初学者来说可能显得有些高深。我们的 Android 系列教程将帮助初学者熟悉 Android 的基本概念。这篇 Android 教程讨论了活动组件。

## **安卓新手教程:活动**

*   Activity 为用户提供了与应用程序交互的屏幕/界面。
*   一个应用程序通常有多个活动。应用程序的每个屏幕都是不同的活动。您可以使用下图来理解这一点:第一个活动(屏幕)有一个按钮，单击该按钮会将用户带到第二个屏幕，这是第二个活动。

[![Activity Component in Android Tutorial](img/f21ddf6c075abf755ba3b34c09d36303.png "Activity Component in Android Tutorial")](https://www.edureka.co/blog/android-tutorials-for-beginners-activity-component/)

让我们以您自己的脸书应用程序为例。登录屏幕是您启动脸书应用程序时看到的第一个活动。登录后，遇到的下一个活动是新闻提要屏幕。

[![News-feed screen in Android tutorial for beginners](img/8121f7351848c823d5ded7f668ec80bd.png "News-feed screen in Android tutorial for beginners")](https://www.edureka.co/blog/android-tutorials-for-beginners-activity-component/)

*   应用程序的所有活动都是松散连接的:一个活动是围绕用户在与另一个活动交互时采取的特定动作而设计的。此外，根据用户的动作，一个活动可以为几个不同的活动让路。
*   活动可以有全屏或浮动窗口。
*   主活动:一般一个应用的一个活动就是主活动。这是首次启动应用程序时呈现给用户的活动(屏幕)。

## **活动生命周期中的阶段**

为了开发一个成功的应用程序，开发人员根据用户的动作绘制出完整的活动流程是很重要的。这将确保应用程序完全按照预期运行。因此，理解活动的生命周期对开发人员来说非常重要。

以下是活动生命周期中的不同状态:

[![Activity Life-cycle in Android Tutorial for beginners](img/1d59257bd5e65d5ffddaab236c133613.png "Activity Life-cycle in Android Tutorial for beginners")](https://www.edureka.co/blog/android-tutorials-for-beginners-activity-component/)

**1)启动状态:**

当一个活动还不存在于内存中时，它就处于开始状态。

**2)恢复/运行状态:**

前台的活动处于运行状态。当前在屏幕上并与用户交互的任何活动都是在特定时间点正在运行的活动。它存在于活动堆栈的顶部。

**3)暂停状态:**

当活动不在焦点上(即，不与用户交互)，但在屏幕上仍然可见时，它处于暂停状态。

**4)停止状态:**

在屏幕上不可见但存在于存储器中的活动处于停止状态。

**5)销毁状态:**

销毁的活动是从内存中删除一个活动(不再需要)的结果。这种移除通常发生在当活动管理器决定这种活动不再有用时。

## **活动堆栈**

这些活动使用堆栈机制来完成它们的生命周期。“后进先出”系统在 Android 活动堆栈中运行。下面是活动后台堆栈工作方式的简要概述:

[![Activity stack in android tutorial for beginners](img/ccb64b52d133fd0859e9f45b8439dc95.png "Activity stack in android tutorial for beginners")](https://www.edureka.co/blog/android-tutorials-for-beginners-activity-component/)

*   运行活动(活动 1):在特定时间点与用户交互的活动位于堆栈的顶部。
*   Activity 2 starts:当一个新的 Activity 开始时，系统停止前一个 activity，并将其推到 back-stack 中的较低级别。新的活动现在是焦点，并且只要用户与之交互，它就会保持焦点。
*   Activity 1 在堆栈中的位置:原始 activity (Activity1)将位于(新的)当前运行的 activity (Activity 2)的正下方。
*   Activity 2 销毁:用户对当前 activity (Activity 2)的工作一结束，按下 back 按钮，原来的 activity (Activity 1)就来到前台(系统销毁正在运行的 Activity 之后)。

## **回调方法**

每当活动在其生命周期阶段经历任何变化时(例如:当正在运行的活动暂停时)，回调方法会通知它这一变化。无论活动正在被创建、销毁还是正在经历任何其他转换，都有一个回调方法来通知它。对于每个回调，都有一个预定义的行为。

为了确保不同活动之间的平稳过渡，开发人员必须事先实现回调。我们将在后续的 Android 教程中讨论更多关于回调的内容。呆在原地。

快乐学习！

有问题要问我们吗？请在评论区提到它，我们会给你回复。

**相关帖子:**

[安卓入门培训](https://www.edureka.co/android-development-certification-course)

[大一新生 5 大安卓面试题](https://www.edureka.co/blog/interview-questions/top-5-android-interview-questions-for-freshers/ "Top 5 Android Interview Questions for freshers")

[安卓初学者教程:活动组件](https://www.edureka.co/blog/android-tutorials-for-beginners-activity-component/ "Android Tutorials for Beginners Part-1: Activity component")

[安卓项目:二十一点游戏](https://www.edureka.co/blog/android-tutorial-on-blackjack/ "Android Project : BlackJack Game")

[【Android 初学者指南:Android 架构](https://www.edureka.co/blog/beginners-guide-android-architecture/ "The Beginner’s Guide to Android: Android Architecture")