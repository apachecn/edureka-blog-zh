# Android 初学者教程-2: Android 意图

> 原文：<https://www.edureka.co/blog/android-tutorials-intent-component/>

在我们的[上一期 Android 教程](https://edureka.co/blog/android-tutorials-for-beginners-activity-component/ "Android Tutorial: Activity component")中，我们讨论了 Android 应用的活动组件。这里的 Android 教程涵盖了下一个构建模块的基础，即 Android Intent。

*如果你想免费听一场关于 Android 开发基础的现场讲座，[在这里注册](https://www.edureka.co/android-development-certification-course "Android tutorials for beginners")！*

[https://www.youtube.com/embed/_MoYpyBfK7M?version=3&rel=1&fs=1&autohide=2&showsearch=0&showinfo=1&iv_load_policy=1&wmode=transparent](https://www.youtube.com/embed/_MoYpyBfK7M?version=3&rel=1&fs=1&autohide=2&showsearch=0&showinfo=1&iv_load_policy=1&wmode=transparent)

观看此视频，了解目的概述。

### **1。Android 初学者教程:意图**

在我们的 [Android 教程中，涵盖了更新鲜的面试问题](https://edureka.co/blog/android-interview-questions-answers-for-beginners/ "Interview Questions Answers for Android beginners")，我们用下面的例子解释了意图在脸书的用法:

*假设你在新闻提要屏幕上(这是一项活动)，想查看我们朋友发布的一张照片。当您点击照片时，与照片的点击事件相关联的意图被激发，其传达消息，并且照片页面打开(这是新的活动)。*

[![Android Tutorial: Intent Component](img/606413de089c5ce1e32158fe826f9cd6.png "Android Intent Example")](https://www.edureka.co/blog/android-tutorials-intent-component/) 所以，我们假设你了解一点关于 Android 的意图。这篇 Android 教程将讨论一些与该主题相关的更深层次的概念。

*   把意图想象成传达动作的**消息。它是对你想做的事情的描述，例如:观看视频、玩游戏等。**
*   它们是命令，当被调用时，将充当 Android 的三个核心组件(即活动、服务和广播接收器)之间的**通信器。**
*   当您正在与一个活动交互时，您可能想要切换到另一个活动；这是通过为行动定义一个适当的意图来实现的。这里，一个活动使用 Intent 请求启动另一个活动。因此，很明显**使用意图，一个 Android 组件可以请求 Android** 的其他组件的动作。

为了简化，让我们再一次以脸书应用程序为例。

*下面的示例假设您正在进行照片库活动，并且想要查看特定的照片(该照片将在它自己的活动中打开)。这就是如何激发与点击照片事件相关联的意图:*

[![Android Tutorials for beginners: Intent component of Android](img/3724bfafd5772d6c633a60a7caaeaedd.png "Facebook Intent Example")](https://www.edureka.co/blog/android-tutorials-intent-component/)

有时，**可以定义意图来通知 Android 系统关于事件**的发生。这正是在广播接收机*的情况下发生的事情(例如，**意图被定义为向用户**传达电池电量低通知)。*

再举一个达美乐披萨 app 的例子。让我们假设您正在查看应用程序的菜单屏幕(Activity ),并且想要选择一个比萨饼。当你选择墨西哥波比萨饼，并点击定制按钮，另一个屏幕(活动)弹出，在那里你可以进一步指定比萨饼的大小，你想要的外壳类型等。这里，菜单上的点击动作(选择比萨饼意图)传达了打开新弹出窗口(新活动)的消息。

[![Android Tutorials for beginners: Intent Example using Domino's Pizza app](img/8209ba9516bd8415a77396bc21d73129.png "Dominos Pizza Intent")](https://www.edureka.co/blog/android-tutorials-intent-component/)

简单；对！让我们在 Android 教程的下一部分深入了解一些细节:

#### **2。意图对象**

如果你想和你的朋友共进晚餐，并通过信使传递信息，你应该给信使详细的信息，如你朋友的名字和希望见面的细节(时间、地点等)。).没有把会议的细节告诉信使，你不能认为他们会想出该做什么。你可以把所有这些信息写在一张纸上，供送信人参考。

同样， ***作为意图是一条消息**，**它要传达的完整信息必须存储在某个地方**，对！意向对象照顾那个*。

#### **2.1 意向对象包含哪些信息？**

***意图对象*** 包含了‘意图’所要传达的全部信息:

1.  接收意图的组件所需的所有**信息(例如，接收意图时要采取的动作)。*(在上面的例子中，这是你的朋友想要知道的信息，比如会议的地点、时间等等。)***
2.  Android 系统所需的**信息(如意图所针对的组件类别的描述)包含在 ***意图对象*** 中。*(在上面的例子中，信息传递者本身所需要的信息也是其中的一部分，比如朋友的名字，他的地址等等。)***

#### **以下信息构成意图对象的一部分:**

*   **组件名称:**该信息是可选的。如果设置了组件名，**Android 系统直接将意图映射到目标组件**。在其他情况下，系统利用其他信息来定位合适的目标。*组件名由 **setComponent()、setClass()或 setClassName()设置，由 getComponent ()** 读取。*

*   **动作:**这条信息指定了 Android 组件在接收到意图时应该采取的**动作，或者已经发生的动作，并且正在通知系统。Android 系统定义了许多动作常量。我们在这个 Android 教程中列出了两个:**

[![Android Tutorials: Intent Object Action](img/6bb89d6ee543ef36ab3f658ab0c43e2e.png "Action-Intent Object")](https://www.edureka.co/blog/android-tutorials-intent-component/)

*   **数据:**包含数据的**统一资源标识符(URI)。不同的动作有不同类型的数据规范。例如，如果定义的动作是 ACTION_CALL，数据字段将包含一个要呼叫的号码(电话:URI)。为了正确地将意图匹配到合适的组件，定义数据类型(除了 URI 之外)会有所帮助。例如，应该调用显示图像的组件来仅显示图像，而不是播放音频文件。**

*   **类别:**这定义了将处理意图的组件的**类别。**

*   **Extras:** 这是需要传递给处理意图的组件的附加信息。

*   **标志:**许多标志可以是意图对象中包含的信息的一部分。例如，标志可以指示 Android 系统以特定的方式启动一个活动 ***(您可以指定在浏览器的新窗口中启动新活动。)***

#### **3。意图类型**

进一步研究，意图可以是明确的，也可以是隐含的。

#### **3.1 明确意图:**

一个明确的意图就是字面上的意思: ***一个“明确的意图”去执行一个动作*** 。简单地说，在这种情况下，我们显式定义需要调用的 Android 组件(活动、服务或广播接收器)。

**样本代码 1:明确意图样本代码** [![Android Tutorials: Explicit Intent sample code](img/155286e11964892a68768a8df140492f.png "Explicit Intent Sample code") ](https://www.edureka.co/blog/android-tutorials-intent-component/) [ ![Android Tutorials for beginners: Explicit Intent Example](img/cfe8317bcaeab185cad04ce2ec1e90ba.png "Explicit Intent Example")](https://www.edureka.co/blog/android-tutorials-intent-component/)

#### **3.2** **隐含意图**

这里我们不具体定义需要调用的组件。然而，意图包含了足够的信息来指导系统获取正确的信息。

**样本代码 2:隐含意图样本代码** [![Android tutorials for beginners: Implicit Intent sample code](img/383ba10e395f2c5e5791d3a5f92886c8.png "Implicit Intent sample code")](https://www.edureka.co/blog/android-tutorials-intent-component/)

*上面隐含的意图告诉 Android 系统查看 URI 中提供的网页。*

[![Implicit Intent Example: Basic Android tutorials ](img/66c3fd0ad4aee0536af83bb9dd85f7c2.png "Implicit Intent example")](https://www.edureka.co/blog/android-tutorials-intent-component/)

#### **4。意向解析**

由于隐含意图的任意性，系统使用称为 ***意图解析*** 的过程来正确映射它们。系统通过将意图描述与系统中的默认描述进行匹配来实现这一点。

前面定义的意图对象在这里起了作用。意图解析将意图对象的内容与意图过滤器进行比较。 ***(意图过滤器与不同的 Android 组件相关联，并且可以接收意图。意图过滤器是 Android 组件向 Android 系统声明其能力的一种方式。)***

过滤器在定义 Android 组件可以接收的意图类型中扮演着重要的角色。没有过滤器的组件只能接收显式意图，而有过滤器的组件能够接收显式和隐式意图。意图解析使用以下信息将意图映射到适当的 Android 组件:

*   行动
*   类型(数据类型和 URI)
*   类别

可以看到，额外的和旗帜在这里没有作用。

看完这篇 Android 教程，你现在可能对 Android 意图的概念有了更好的理解。

#### **[对本 Android 教程讨论的任何话题有疑问？问我们！](#)**

我们将在后面的教程中讨论更多关于意图过滤器的内容。敬请关注。目前，你可以加入 [Android 课程](https://www.edureka.co/android-development-certification-course "Android tutorials for beginners")。

快乐学习！

#### **你可能也会喜欢这些相关的帖子:**

*   [Android 初学者教程第一部分:活动组件](https://www.edureka.co/blog/android-tutorials-for-beginners-activity-component/ "Android Tutorials for Beginners Part-1: Activity component")
*   [Android 初学者教程第三部分:Android 服务](https://www.edureka.co/blog/android-tutorials-beginners-service-component/ "Android Tutorials for beginners Part-3: Android Services")
*   [如何创建 Android Widgets:自定义 Toast](https://www.edureka.co/blog/android-tutorial-custom-toast/ "How to create Android Widgets:Custom Toast")
*   应对软件公司第一次校园面试的 12 个技巧