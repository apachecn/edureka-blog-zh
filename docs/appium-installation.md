# 如何安装 Appium:一步一步完整教程

> 原文：<https://www.edureka.co/blog/appium-installation/>

关于 Appium 的安装有很多传言。它通常被认为是令人困惑和乏味的。在这篇博客中，我将教你如何在 Windows 和 MAC 上安装我们最喜欢的自动化测试工具 Appium。我会提供一步一步的指示以及必要的截图。以下是讨论的主题—

*   [什么是 Appium？](#what-is-appium)
*   [Appium 特性](#appium-features)
*   [在 Windows 上安装应用程序](#appium-installation-windows)
*   [在 Mac 上安装应用程序](#appium-installation-mac)

## **什么是 Appium？**

## ![appium logo - appium installation - edureka](img/b7820784e1b0e4298d013b6877d307dd.png)

Appium 是一款开源、跨平台的[移动应用测试](https://www.edureka.co/blog/mobile-application-testing)工具。它被测试人员广泛用于自动化他们的测试用例，因为它可以测试所有种类的应用程序。无论是本机应用程序、web 应用程序还是混合应用程序，也无论是 Android 还是 iOS 专用应用程序，Appium 都可以处理！Appium 只是一个 HTTP 服务器，处理对 UIAutomator 的请求，其中包含用于测试目的的 web 驱动命令。如果你有兴趣了解 Appium 的工作架构，你应该看看我的 [Appium 教程](https://www.edureka.co/blog/appium-tutorial/#appium-architecture)。

## **Appium 特性**

Appium 因其广泛的功能而被业界采用。让我们来讨论一下把 Appium 带到聚光灯下的那些。

1.  **支持 Webdriver 协议**–web driver 协议可以更好地控制 web UI。自动化，不中断页面上运行的 JS。Appium 仍然向后兼容 JSON Wire 协议。
2.  **强大的测试执行**–无论设备是在本地可用还是在远程服务器上，Appium 都可以轻松执行测试。测试也可以被实时监控。
3.  **多平台支持**–app ium 可以跨多个平台执行测试用例。截至目前，Appium 支持[安卓](https://www.edureka.co/blog/android-tutorial/)，iOS 和 Windows 应用。
4.  **无需重新构建应用程序**–app ium 不会一次又一次地将正在测试的应用程序重新安装到系统上。它也不需要访问应用程序的库或源代码。
5.  **并行执行**–app ium 支持用户在多个 Android 或 iOS 会话上执行测试自动化脚本。这可以使用 UIAutomator、UIAutomation 和 Xcode9 来实现。

## **在 Windows 上安装应用程序**

1.  将文件添加为库后，您应该会在 app 文件夹中看到一个  *build.gradle* 文件。双击它，然后重新构建您的项目。一旦项目重建成功，这意味着你已经在你的 Android studio 系统上安装了 Appium。

## **在 MAC 上安装应用程序**

1.  首先，我们将安装 java。要安装 java，请前往 [java 下载页面](https://www.oracle.com/technetwork/java/javase/downloads/jdk11-downloads-5066655.html)，在接受许可协议后下载“dmg”文件。按照屏幕安装完成 JAVA 安装后，在终端中输入以下代码，检查安装是否成功。该命令应该显示安装的 java 版本。

    ```
    java -version
    ```

2.  Now it’s time to set up the environment variable and path. Enter the following code into your terminal.

    ```
    vim ~/.bash_profile
    ```

    这将打开一个 vim 编辑器。按 I 进入插入模式，并输入以下代码。

    ```
    export JAVA_HOME = $(/usr/libexec/java_home)
    export PATH = $JAVA_HOME/bin=$PATH
    export PATH = /usr/local/bin:PATH
    ```

3.  输入上述代码后，按键盘上的 escape 键，输入“ **:wq** ”。这将使您返回到终端界面。现在输入下面的代码将路径作为参数传递。

    ```
    source ~/.bash_profile
    ```

4.  现在，是时候从 app store 安装 Xcode 了。只需在 app store 上搜索 Xcode，然后点击安装按钮。
5.  在你安装了 Xcode 之后，是时候在你的系统上安装 homebrew 了。复制下面的代码并粘贴到您的终端。

    ```
    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
    ```

6.  以上代码完全运行后，运行以下命令。

    ```
    brew update
    brew doctor
    xcode-select --install
    ```

7.  以上步骤完成了 Xcode 的安装。现在你只需要下载 Appium 服务器。前往[官方网站](http://appium.io/)，点击下载应用程序按钮。一旦下载完成，点击 DMG 文件。只需按照屏幕上的指示。安装 Appium 后，只需将其拖放到您的应用程序文件夹中。这就完成了 Appium 在 MAC 上的安装。

本《Appium 安装指南》到此结束。如果你想了解更多关于移动应用测试的知识，你可以阅读我的另一个博客。如果你有兴趣阅读其他一些关于各种趋势技术的博客，你可以看看我们的[博客目录](https://www.edureka.co/blog)。

如果你希望学习[软件测试](https://www.edureka.co/blog/what-is-software-testing/)并建立一个丰富多彩的职业生涯，那么请查看我们的 [***Selenium 认证课程***](https://www.edureka.co/testing-with-selenium-webdriver) ，该课程附带有讲师指导的现场培训和真实项目体验。该培训将帮助您深入理解软件测试和 selenium，并帮助您掌握该主题。

<article class="maincontentblog">Got a question for us? Please mention it in the comments section of “Appium Installation Guide” and we will get back to you as soon as possible.</article>