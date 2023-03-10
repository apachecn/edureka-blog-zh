# Android SDK 初学者教程

> 原文：<https://www.edureka.co/blog/android-sdk-tutorial/>

软件开发工具包(SDK)是一个可安装包中的软件开发工具集合。这个 SDK 也和 *[安卓](https://www.edureka.co/blog/android-tutorial/)* 一起使用，帮助下载工具，安卓的最新版本。所以，这篇 Android SDK 教程将帮助你了解 Android SDK。

*   [Android SDK 是什么？](#What_is_the_Android_SDK?)
*   [如何安装 Android SDK？](#How_to_install_Android_SDK?)
*   [Android SDK 特性](#Android_SDK_Features)
*   [SDK 工具](#SDK_Tools)
*   [Android SDK 管理器](#Android_SDK_manager)

我们开始吧！

## **Android SDK 是什么？**

谷歌每发布一个新版本，相应的 SDK 也随之发布。为了使用 Android，开发人员必须为特定设备下载并安装每个版本的 SDK。

![SDK Android-Android SDK Tutorial-Edureka](img/07c811ee080f27f610a114ca04b0b937.png)

Android SDK(软件开发工具包)是一套用于为 Android 平台开发应用程序的开发工具。

该 SDK 提供了构建 Android 应用程序所需的一系列工具，并确保该过程尽可能顺利进行。无论你是使用*[Java](https://www.edureka.co/blog/what-is-java/)**[Kotlin](https://www.edureka.co/blog/what-is-kotlin/)*还是 *[C#](https://www.edureka.co/blog/interview-questions/c-sharp-interview-questions/)* 创建应用，你都需要 SDK 来让它在任何 Android 设备上运行。您还可以使用模拟器来测试您构建的应用程序。

如今，Android SDK 也与 Android Studio 捆绑在一起，Android Studio 是一个集成开发环境，在这里可以完成工作，许多工具现在都可以得到最好的访问或管理。

***注:*** 可以独立下载 Android SDK。

现在，接下来的问题是如何在你的系统上安装 Android SDK。

## **如何安装 Android SDK？**

按照这些步骤安装 Android SDK。

**第一步:** [*在你的系统上安装 Android Studio*](https://www.edureka.co/blog/studio-install/) 。

**第二步:**当你看到 Android Studio 的欢迎页面时，点击**配置**并选择 SDK 管理器。

![SDK Installation-Android SDK Tutorial-Edureka](img/3514dd62bc5f9e792e5b909092c9482c.png)

**或**

如果你已经创建了一个新项目，只需进入**工具** - > **SDK 管理器** - > **SDK 工具**，安装所需的 SDK 文件即可。

![SDK- Android SDK Tutorial-Edureka](img/0d2fdd2291a6369c454205031499ad75.png)

**或**

你可以点击菜单栏上的下载图标。

![SDK-Android SDK Tutorial-Edureka](img/dde6007a3dcf9937a9a7cf90759fc0f9.png)

接下来，我们来看看 Android SDK 有哪些不同的特性。

## **Android SDK 特性**

Android SDK 有很多令人惊叹的功能。我试着记下了大部分。所以，看看吧！

*   **离线映射**

![SDK Features-Edureka](img/a6935e65c90de0471ee49f69beac915e.png) SDK 有助于以 60 多种语言动态下载 190 多个国家的地图。您可以离线查看这些内容。还处理地图样式和触摸手势。该 SDK 还能够渲染不同地图图层中交错的栅格切片和地图对象。

*   **动态标记**

在以前的版本中，如果没有回退或重新添加图标，您无法移动位置。但是在最新版本中，你可以动态更新图标的位置。

*   **简易 API 兼容性**

在最新版本中，从 Google Maps Android API 迁移要容易得多。这是在你的程序中使用 Android SDK 的另一个好处。

既然你们已经理解了这些特性，让我们继续前进，看看在 *[Android 开发中起主要作用的 SDK 工具。](https://www.edureka.co/blog/android-tutorial/)*

## **SDK 工具**

Android SDK 工具是 Android SDK 的一个组件。这包括一套完整的 Android 开发和调试工具。Android Studio 还包含 SDK 工具。

Android 不时推出修订版，最新版本是 SDK Tools，修订版 26 . 1 . 1*(2017 年 9 月)*

在这个版本中，他们做了一些改变。它们是:

*   在 *tools/bin/apkanalyzer 中添加了 APK 分析器的命令行版本。*它提供了与 *[Android Studio](https://www.edureka.co/blog/android-studio-tutorial/)* 中的 APK 分析器相同的功能，并且可以集成到 build/CI 服务器和脚本中，用于跟踪规模回归、生成报告等等。
*   在*工具/proguard* 下的 *ProGuard* 规则不再被 Gradle 的 Android 插件使用。

这些随着每次更新而改变。

![SDK Tools-Edureka](img/bab6d8cd13003affdfa102b353145f72.png)

SDK 工具通常是独立于平台的，无论你当前在哪个 Android 平台上工作，都需要它们。安装 Android Studio 时，会自动安装一组工具。我试着记下了其中的一些:

| 工具 | 描述 |
| 机器人 | 这个工具可以让你管理 AVD ( Android 虚拟设备)、项目和 SDK 的已安装组件。 |
| 仿真器 | 它让您可以在不使用物理设备的情况下测试应用程序。 |
| Proguard | 这个工具通过删除不使用的代码来帮助缩减、优化和模糊你的代码。 |
| ddms | 它可以让你调试你的 Android 应用程序 |
| Android 调试桥(Adb) | 这是一个多功能的命令行工具，可以帮助您与仿真器实例或连接的 Android 设备进行通信。 |

现在您已经了解了工具，让我们继续讨论本文的最后一个主题。

## **Android SDK 管理器**

为了从互联网上下载和安装最新的 android APIs 和开发工具，android 通过拥有 Android SDK 管理器来帮助我们。这将 API、工具和不同的平台分成不同的包，您可以下载。Android SDK 管理器附带 Android SDK 捆绑包。不能单独下载。

这就把我们带到了这篇“ *Android SDK 教程*”文章的结尾。我希望你们清楚讨论的主题，并且知道如何使用 Android SDK。

*现在您已经浏览了我们的 Android SDK 教程博客，您可以查看 Edureka 的  [Android App 开发认证培训](https://www.edureka.co/android-development-certification-course)* 来快速开始您的学习。

*有什么疑问吗？别忘了在这篇“Android SDK 教程”博客的评论中提到它们。我们会回复你的。*