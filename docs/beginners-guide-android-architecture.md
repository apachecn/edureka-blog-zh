# Android 初学者指南:Android 架构

> 原文：<https://www.edureka.co/blog/beginners-guide-android-architecture/>

在我们之前的[Android 教程](https://www.edureka.co/blog/category/mobile-development/) 中，我们已经讨论了相当多的 Android 开发概念。然而，在浏览文章时，我发现我们还没有对 **Android 架构进行过适当的讨论。**

因为这是 Android 开发最基本的概念之一，所以我决定稍微倒退一下，快速浏览一下 Android 架构。

如果你希望强化你对 Android 的基本概念并拓展你在 Android 领域的职业机会，参加 ***[在线 Android 认证培训](https://www.edureka.co/android-development-certification-course)*** 是最好的方法之一。

## Android 架构:Android 堆栈中的层

谷歌的人称之为 **Android stack，它有许多层，每一层将几个程序组合在一起**。在本教程中，我将带你了解 Android stack 中的各个层以及它们所负责的功能。

以下是 Android 堆栈中的不同层:

*   Linux 内核层
*   原生层
*   应用框架层
*   应用层

## **内核层**

**[![Linux-Kernel ](img/4b39d1c34333fda5cfc6a1e61e39412c.png "Linux-Kernel")](https://cdn.edureka.co/blog/wp-content/uploads/2013/01/Linux-Kernel-1.png)** 

Android 堆栈的底层是 Linux 内核。它从来没有真正与用户和开发者互动过，但它是整个系统的核心。它的重要性源于它在 Android 系统中提供了以下功能:

*   硬件抽象
*   内存管理程序
*   安全设置
*   电源管理软件
*   其他硬件驱动程序(驱动程序是控制硬件设备的程序。)
*   支持共享库
*   网络堆栈

随着 Android 的发展，它所运行的 Linux 内核也在发展。

#### 这里有一个表格，突出显示了不同的内核版本。

[![Android evolution: Linux Kernel versions](img/fc5a3eca59a6c402aced6ff697124a95.png "Android evolution: Linux Kernel versions")](https://cdn.edureka.co/blog/wp-content/uploads/2013/01/Android-evolution-Linex-Kernel-versions-1.png)

Android 系统为其进程间通信(IPC)机制使用了绑定框架。binder 框架最初是作为 OpenBinder 开发的，用于 BeOS 中的 IPC。

## 原生库层

[![Native-Android-Libraries ](img/f3afd3664c9374feac559921e8f75e73.png "Native Android Libraries")](https://cdn.edureka.co/blog/wp-content/uploads/2013/01/Native-Android-Libraries-1.png)

Android 架构的下一层包括 Android 的本地库。库带有一组指令来指导设备处理不同类型的数据。例如，各种音频和视频格式的回放和记录由媒体框架库指导。

## 开源库:

*   曲面管理器:在屏幕上合成窗口

*   SGL: 2D 图形
*   打开 GL|ES: 3D 库
*   媒体框架:支持各种音频、视频和图片格式的回放和录制。
*   自由类型:字体渲染
*   WebKit:浏览器引擎
*   libc(系统 C 库)
*   SQLite
*   openssl

Android 运行时层位于库层的同一层，也包括一组核心 Java 库。Android 应用程序程序员使用 Java 编程语言构建他们的应用程序。它还包括 Dalvik 虚拟机。

[![Android-Runtime-layer ](img/72b0dc0b0773894adcd37349952c71a4.png "Android Runtime layer")](https://cdn.edureka.co/blog/wp-content/uploads/2013/01/Android-Runtime-layer-1.png)

## 什么是达尔维克 VM？

Dalvik 是开源软件。丹·博恩施泰因以他的一些祖先居住的冰岛 eyjafjr ur 的 Dalvík 渔村为它命名，他最初写道 Dalvic VM。它是负责在 Android 设备上运行应用程序的软件。

*   这是一个基于注册的虚拟机。
*   它针对低内存需求进行了优化。
*   它被设计成允许多个虚拟机实例同时运行。
*   依赖底层操作系统进行进程隔离、内存管理和线程支持。
*   对 DEX 文件进行操作。

## **应用框架层**

[![Application framework layer](img/b3def31ca8d1fbad6b1acdaa4ac9dc30.png "Application framework layer")](https://cdn.edureka.co/blog/wp-content/uploads/2013/01/Applications-framework-1.png)

我们的应用程序直接与 Android 架构的这些模块进行交互。这些程序管理电话的基本功能，如资源管理、语音呼叫管理等。

**应用框架的重要模块:**

*   **活动管理器:**管理应用的活动生命周期。要详细了解 Android 中的活动组件 [点击这里](https://www.edureka.co/blog/android-tutorials-for-beginners-activity-component/ "Activity Component in Android")。
*   **内容提供者:**管理应用之间的数据共享。我们关于 [内容提供商组件](https://www.edureka.co/blog/beginner-android-tutorials-content-provider/ "Content Providers in Android") 的帖子对此进行了更详细的描述
*   **电话管理器:**管理所有语音通话。如果我们想在应用程序中访问语音呼叫，我们使用电话管理器。
*   **位置管理器:**位置管理，使用 GPS 或手机信号塔
*   **资源管理器:**管理我们在应用程序中使用的各种资源

## **应用层**

[![Applications-layer-in-Android-stack ](img/186c1241b309d7f185e4d600306dbcb5.png "Application layer in Android stack ")](https://cdn.edureka.co/blog/wp-content/uploads/2013/01/Applications-layer-in-Android-stack-1.png)

应用程序位于 Android 堆栈的最顶层。Android 设备的普通用户将主要与这一层(用于**基本功能，如打电话、访问网络浏览器**等)进行交互。).**更下面的层主要由开发人员、程序员**之类的人访问。

每个设备都安装了几个标准应用程序，例如:

*   短信客户端应用
*   拨号器
*   网络浏览器
*   联系人管理

我们希望你现在已经清楚基本的 Android 架构了！如果没有，请随时到 [询问我们的专家！](# "Have a Doubt? Ask the experts!") 敬请期待更多安卓高级教程。

快乐学习！

(本 Android 教程使用了以下资源:[【developer.android.com】](http://developer.android.com/index.html "Android Tutorials Official")[](https://www.edureka.co/))

**相关帖子:**

[安卓项目:二十一点游戏](https://www.edureka.co/blog/android-tutorial-on-blackjack/ "Android Project : BlackJack Game")

[如何创建 Android Widgets:Android 中的 rating bar](https://www.edureka.co/blog/tag/how-to-create-android-widgets/ "How to create Android widgets: RatingBar in Android")

[大一新生 5 大安卓面试题](https://www.edureka.co/blog/interview-questions/top-5-android-interview-questions-for-freshers/ "Top 5 Android Interview Questions for freshers")

[安卓初学者教程:活动组件](https://www.edureka.co/blog/android-tutorials-for-beginners-activity-component/)

[应对软件公司第一次校园面试的 12 个技巧](https://www.edureka.co/blog/interview-questions/tips-to-handle-first-campus-interview-software-company/ "12 Tips to handle your first campus interview with a Software Company")