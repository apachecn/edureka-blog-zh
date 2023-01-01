# 2023 年你必须准备的顶级 iOS 面试问题

> 原文：<https://www.edureka.co/blog/interview-questions/ios-interview-questions/>

据 The Verge 报道，世界上有数十亿台苹果设备在使用。随着全球 iOS 用户数量的稳步增长，iOS 应用开发者的未来看起来一片光明。苹果和 iOS 设备继续拥有忠实的客户群，这在一定程度上得益于苹果电视和苹果手表等创新型新设备。也就是说，一个 ***[iOS app 开发认证](https://www.edureka.co/ios-development)*** 大概是最简单的磨练和证明自己技能的方法了。成为 iOS 开发者的最佳时机。如果你正准备进入 iOS 应用程序开发领域，不要再犹豫了！我们创建了一个常见的 iOS 面试问题列表，将帮助您在 iOS 工作面试中胜出。

但是，如果您已经接受了 iOS 采访，或者有更多问题，我们鼓励您在下面的评论选项卡中添加它们。我们的专家会为您解答。

## iOS 面试问题

## 1。可可和可可触是什么？

 <caption>#### **可可 vs 可可触**</caption> 
| **可可** | **可可触摸** |
| 1。OS X 的应用开发环境 | 1。iOS 应用开发环境 |
| 2。包括基础和 AppKit 框架 | 2。包括基础和 UIKit 框架 |
| 3。用于引用任何基于 Objective-C 运行时&继承自根类的类/对象 | 3。用于引用使用任何编程接口的应用程序开发 |

更多关于 [这里](https://developer.apple.com/library/ios/documentation/General/Conceptual/DevPedia-CocoaCore/Cocoa.html) 。

## 2。iOS 支持哪个 JSON 框架？

*   iOS 支持 SBJson 框架。
*   SBJson 是 Objective-C 的 Json 解析器和生成器。
*   它提供了灵活的 API 和额外的控制，使得 JSON 处理更加容易。

## 3。原子和非原子的性质有什么区别？哪个是合成属性的默认值？

指定为原子的属性总是返回完全初始化的对象。这也是合成属性的默认状态。但是，如果您有一个属性，并且您知道检索未初始化的值没有风险(例如，如果对该属性的所有访问都已经通过其他方式进行了同步)，那么将它设置为非原子会比原子提供更好的性能。

## 4。区分“应用 ID”和“捆绑 ID”。解释为什么使用它们。

一个 [应用 ID](https://developer.apple.com/library/mac/documentation/General/Conceptual/DevPedia-CocoaCore/AppID.html) 是一个由两部分组成的字符串，用于标识一个开发团队中的一个或多个应用。该字符串由一个团队 ID 和一个捆绑包 ID 搜索字符串组成，带有一个句点(。)将两部分分开。团队 ID 由 Apple 提供，对于特定的开发团队是唯一的，而捆绑 ID 搜索字符串由开发人员提供，用于匹配单个应用程序的捆绑 ID 或一组应用程序的一组捆绑 ID。

捆绑包 ID 定义了每个应用程序，并在 Xcode 中指定。一个 Xcode 项目可以有多个目标，因此可以输出多个应用程序。一个常见的用例是同时拥有 lite/free 和 pro/full 版本或多种品牌的应用程序。

## 5。iOS 中实现并发的方式有哪些？

在 iOS 中实现并发的三种方式是:

*   线
*   调度队列
*   操作队列

## 6。解释不同类型的 iOS 应用程序状态。

不同的 iOS 应用程序状态包括:

*   **未运行**状态:app 尚未启动或正在运行，但被系统终止。
*   **Inactive** 状态:当 app 在前台运行，但当前没有接收事件时。当应用程序转换到另一种状态时，它会暂时停留在这种状态。它保持不活动的唯一时间是当用户锁定屏幕或系统提示用户响应一些事件，如电话或短信。
*   **Active** 状态:当 app 在前台运行，正在接收事件时。这是前台应用程序的正常模式。
*   **后台**状态:app 在后台执行代码时。大多数应用程序在被挂起的过程中都会短暂地进入这种状态。但是，请求额外执行时间的应用程序可以保持这种状态一段时间。此外，直接在后台启动的应用程序会进入这种状态，而不是非活动状态。
*   **挂起**状态:挂起的 app 留在内存中，但不执行任何代码。当出现内存不足的情况时，系统可能会在没有通知的情况下清除暂停的应用程序，以便为前台应用程序腾出更多空间。

## 7。哪个是用于构建 iOS 应用程序用户界面的框架？

UIKit 框架用于为 iOS 开发应用程序的用户界面。它提供了专门为触摸屏界面设计的事件处理、绘图模型、窗口、视图和控件。

## 8。哪个是应该使用 UIKit 类的应用程序线程？

UIKit 类应该只在应用程序的主线程中使用。

## 9。您会使用哪个 API 来编写测试脚本，以测试应用程序的 UI 元素？

UI 自动化 API 用于自动化测试过程。写入 UI 自动化 API 的 JavaScript 测试脚本模拟用户与应用程序的交互，并将日志信息返回给主机。

## 10。什么时候你会说一个 app 没有处于运行状态？

An app is said to be in ‘not running’ state in the following cases: – When it is not launched. – When it gets terminated by the system during running.

## 11。一个 app 什么时候被说成是处于活跃状态？

An app is said to be in active state when it is running in the foreground and is receiving events.

## 12。app 启动时的状态转换有哪些？

一个应用程序在启动前被称为处于未运行状态。

经过短暂的非活动状态转换后，它会在启动时进入活动或后台状态。

## 13。应用程序在被挂起的过程中会短暂地达到哪种状态？

一个应用程序在被挂起的过程中会短暂进入后台状态。

## 14。什么是 Swift，什么是 Objective-C？

Objective-C 是用于为 OS X 和 iOS 编写软件的主要编程语言。它是 C 编程语言的超集，提供面向对象的功能和动态运行时。Objective-C 继承了 C 的语法、基本类型和流控制语句，并增加了定义类和方法的语法。它还增加了对对象图管理和对象文字的语言级支持，同时提供动态类型和绑定，将许多责任推迟到运行时。

Swift 是一种新的面向 iOS、OS X、watchOS 和 tvOS 应用程序的编程语言，它建立在 C 和 Objective-C 的基础上，没有 C 兼容性的限制。Swift 采用了安全的编程模式，并增加了现代功能，使编程更容易、更灵活、更有趣。Swift 对 Objective-C 开发人员来说感觉很熟悉，对新程序员也很友好。

来源:苹果开发者图书馆

## 15。什么是 SpriteKit，什么是 SceneKit？

SpriteKit 是一个框架，用于轻松开发动画 2D 对象。

SceneKit 是一个继承自 OS X 的框架，用于辅助 3D 图形渲染。

预计 SpriteKit、SceneKit 和 Metal 将驱动新一代移动游戏，这些游戏将重新定义 iOS 设备强大的 GPU 所能提供的功能。

## 16。什么是 iBeacons？

iBeacon.com 将 iBeacon 定义为苹果的技术标准，它允许移动应用程序侦听来自物理世界的信号并做出相应的反应。iBeacon 技术允许移动应用程序在微观本地范围内了解自己的位置，并根据位置向用户提供超上下文内容。底层通信技术是蓝牙低能耗。

## 17。什么是自动释放池？

Every time – autorelease is sent to an object, it is added to the inner-most autorelease pool. When the pool is drained, it simply sends – releases to all the objects in the pool.Autorelease pools are a convenience that allows you to defer sending -release until “later”. That “later” can happen in several places, but the most common in Cocoa GUI apps is at the end of the current run loop cycle.

## 18。区分“分配”和“保留”关键字。

Retain -specifies that retain should be invoked on the object upon assignment. It takes ownership of an object.Assign – specifies that the setter uses simple assignment. It is used on attributes of scalar type like float, int.

## 19。什么是图层对象？

Layer objects are data objects which represent visual content and are used by views to render their content. Custom layer objects can also be added to the interface to implement complex animations and other types of sophisticated visual effects.

## 20。概述 UIButton 的类层次结构，直到 NSObject。

UIButton 从 UIControl 继承，UIControl 从 UIView 继承，UIView 从 UIResponder 继承，UIResponder 从根类 NSObject 继承。

有问题要问我们吗？在评论区提到它们，我们会回复你。

**相关帖子:**

[使用 Swift 2.0 开始 iOS 应用开发](https://www.edureka.co/ios-development)

关于 iOS 开发职业你需要知道的一切

[为什么 iOS 和 OS X 开发者都选择 Swift](https://www.edureka.co/blog/why-ios-iox-developers-are-choosing-swift)