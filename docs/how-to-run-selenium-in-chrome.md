# 如何在 Chrome 浏览器中运行 Selenium？

> 原文：<https://www.edureka.co/blog/how-to-run-selenium-in-chrome/>

测试系统是一项具有挑战性的任务，你需要一个工具来帮助你。Selenium 就是这样一个工具，主要处理网站测试。在本文中，我将告诉你如何在 Chrome 浏览器中运行 Selenium。进一步的细节，你可以通过[硒课程](https://www.edureka.co/selenium-certification-training)。

*   [硒是什么？](#WhatisSelenium?)
*   [什么是 Chrome 驱动？](#WhatisaChromeDriver?)
*   [Chrome 驱动安装](#InstallingChromeDriver)
*   [如何在 Chrome 浏览器中运行 Selenium？](#HowtorunSeleniuminChromeBrowser?)

我们开始吧！

## **硒是什么？**

[![Selenium - How to run selenium on chrome - Edureka](img/998814a657d3a68b858528b4cc627107.png) ](https://www.edureka.co/blog/selenium-tutorial)  Selenium 是一个开源的可移植框架，用于 web 应用程序的自动化测试。 在测试功能和回归测试用例时，它是高度灵活的。Selenium 测试脚本可以用不同的编程语言编写，如 [ Java ](https://www.edureka.co/blog/advanced-java-tutorial) 、 [ Python ](https://www.edureka.co/blog/python-tutorial/) 、C#等等。这些测试脚本可以在 Chrome、Safari、Firefox、Opera 等各种浏览器上运行，并且支持 Windows、Mac OS、Linux、Solaris 等各种平台。

Selenium 还支持交叉浏览，其中测试用例同时在不同的平台上运行。它还有助于创建健壮的、基于浏览器的回归 [自动化套件](https://www.edureka.co/blog/test-automation-frameworks/) 并执行测试。

接下来，让我们了解什么是 Chrome 驱动程序，以及如何在您的系统上配置它。

## **什么是 Chrome 驱动？**

[WebDriver](https://www.edureka.co/blog/selenium-webdriver-tutorial) 是一款开源工具，用于跨多种浏览器测试 web 应用。它提供了导航到网页、用户输入、 [JavaScript](https://www.edureka.co/blog/what-is-javascript/) 执行等功能。ChromeDriver 基本上是一个独立的服务器，为 Chromium 实现了 WebDriver 的有线协议。 为了实例化 ChromeDriver 的对象，可以借助下面的命令简单地创建对象。

`**Webdriver driver = New ChromeDriver();**`

Chrome driver 的主要座右铭是推出谷歌 Chrome。没有它，就不可能在 Google Chrome 浏览器中执行 Selenium 测试脚本。这是你需要 ChromeDriver 在谷歌 Chrome 浏览器上运行测试用例的主要原因。

现在你知道了什么是 chrome 驱动程序，让我们进一步看看如何在你的系统上配置 Chrome 驱动程序。

## **Chrome 驱动安装**

如果你想详细了解如何在你的系统上配置 Chrome 驱动程序，那么请查看这篇关于 **[Chrome 驱动程序](https://www.edureka.co/blog/selenium-chromedriver-and-geckodriver/)** 的文章。

现在让我们深入到本文的最后一节，了解如何在 Chrome 浏览器中运行 Selenium 脚本。

## **如何在 Chrome 浏览器中运行 Selenium？**

最重要的一步是配置 chrome 驱动程序。之后，您需要安装 Eclipse 并将所有 Selenium 依赖项添加到您的项目中。如果你想知道如何配置 [Selenium](https://www.edureka.co/blog/selenium-webdriver-architecture/) 并运行第一个测试用例，那么请查看这篇关于 **[Selenium 安装](https://www.edureka.co/blog/selenium-installation/)** 的文章。一旦完成，你就需要编写 [Selenium 脚本](https://www.edureka.co/blog/selenium-tutorial)并实例化 Chrome 驱动程序。

让我们看看如何做到这一点。

第一步:首先，您需要通过指定您正在使用的驱动程序的类型和保存该驱动程序的路径来设置属性。

接下来，你应该实例化 [Chrome 驱动](https://www.edureka.co/blog/selenium-chromedriver-and-geckodriver/#SettingUpChromeDriver)的对象，如下面的代码所示。这将帮助您启动 chrome 浏览器

**第三步:**使用`driver.get(),`，您将能够浏览特定网站的 URL。

**第四步:**之后，您可以使用定位器定位元素。如果你希望定位硒元素，那么请参考这篇关于[硒定位器](https://www.edureka.co/blog/locators-in-selenium/)的文章。

```
import java.util.concurrent.TimeUnit;
import org.openqa.selenium.By;
import org.openqa.selenium.chrome.ChromeDriver;
public class ChromeExample {
public static void main(String[] args) {
//Setting system properties of ChromeDriver
System.setProperty("webdriver.chrome.driver", "C://Selenium-java edureka//chromedriver_win32//chromedriver.exe");
//Creating an object of ChromeDriver
WebDriver driver = new ChromeDriver();
driver.manage().window().maximize();
//Deleting all the cookies
driver.manage().deleteAllCookies();
//Specifiying pageLoadTimeout and Implicit wait
driver.manage().timeouts().pageLoadTimeout(40, TimeUnit.SECONDS);
driver.manage().timeouts().implicitlyWait(30, TimeUnit.SECONDS);
//launching the specified URL
driver.get("https://www.google.com/");
//Locating&nbsp; the elements using name locator for the text box
driver.findElement(By.name("q")).sendKeys("YouTube");
//name locator for google search button
WebElement searchIcon = driver.findElement(By.name("btnK"));
searchIcon.click();
}
}
```

当您执行上述代码时，Chrome 驱动程序将启动*谷歌 Chrome* 浏览器，通过【google.com】导航，并给出 YouTube 的搜索结果。这就是它的工作原理。如果你想深入了解硒的基本原理，那么请查看这篇关于 **[硒教程](https://www.edureka.co/blog/selenium-tutorial)** 的文章。

至此，我们结束了这篇关于如何在 Chrome 中运行 [Selenium](https://www.edureka.co/blog/what-is-selenium/) 的文章。我希望你理解了这些概念，并且它增加了你知识的价值。

*如果您希望学习 Selenium 并在测试领域建立自己的事业，那么请在这里查看我们的交互式在线直播 **[Selenium 认证培训](https://www.edureka.co/selenium-certification-training)** ，它将为您提供全天候支持，在整个学习期间为您提供指导。*

*有问题吗？请在如何在 Chrome 中运行 Selenium 的文章的评论部分提到它，我们会给你回复。*