# 用于 XPath 和 CSS 选择器的 ChroPath 的新特性

> 原文：<https://www.edureka.co/blog/new-features-of-chropath/>

对于自动化测试人员来说，识别元素和执行动作是一项重要的任务。为了更简单，Selenium 中引入了名为 [Locators](https://www.edureka.co/blog/locators-in-selenium/) 的概念。但是由于网页的 DOM 结构的复杂性，手动定位元素是一项麻烦的任务。这就是 ChroPath 的用武之地，它简化了在 [Selenium](https://www.edureka.co/blog/selenium-tutorial) 中定位元素的任务。在这篇关于 ChroPath 特性的文章中，我将告诉您如何将 ChroPath 用于 XPath 和 CSS 选择器。

以下是本文将要涉及的主题:

*   [XPath 和 CSS 选择器简介](#IntroductiontoXPathandCSSSelectors)
*   [什么是 ChroPath？](#WhatisChropath?)
*   [chro path 的特性](#FeaturesofChroPath)
*   [chro path 的工作](#WorkingofChroPath)

*如果你想通过 **[认证硒专家](https://www.edureka.co/testing-with-selenium-webdriver)** 掌握硒的概念，你可以看看下面的视频，这些话题涵盖了更广泛的范围。*

## **针对 XPath 和 CSS 选择器的 Chropath 新特性| Selenium 认证培训| Edureka**



[https://www.youtube.com/embed/2tneXeIXfNo?rel=0&controls=0&showinfo=0](https://www.youtube.com/embed/2tneXeIXfNo?rel=0&controls=0&showinfo=0)*This Edureka video on “Features of ChroPath” will give you a brief insight into how to use chropath for xpath and css selectors with the help of examples.*

让我们开始并理解什么是 XPath 和 CSS 选择器。

## **XPath 和 CSS 选择器简介**

XPath 是一种用于查询 XML 文档的语言。它 是元素在硒中定位的重要策略。它还包含一个路径表达式和一些条件。在这里，您可以轻松地编写一个 [XPath](https://www.edureka.co/blog/xpath-in-selenium/) 脚本/查询来定位网页中的任何元素。

现在谈谈 CSS 选择器，它主要用于为网页提供样式规则，你可以用它来识别网页中的一个或多个元素。CSS 选择器始终是在页面中定位复杂元素的最佳方式。如果您希望获得更多关于 CSS 选择器的见解，您可以查看 Selenium 中关于 [Locators 的博客。](https://www.edureka.co/blog/locators-in-selenium/)

现在，让我们进一步了解什么是 ChroPath，它有哪些独特的功能。

## **什么是 ChroPath？**

**ChroPath** 被认为是编辑、检查和生成 XPath 和 CSS 选择器的开发工具。使用 ChroPath，我们可以轻松地在任何网页上编写、编辑、提取和评估 XPath 和 CSS 查询，并在自动化脚本编写中节省至少 40–50%的人工工作量。ChroPath 是评级最高的(4.6+) XPath 工具。 ChroPath 是谷歌 chrome 的扩展之一，有助于 UI 元素的调试。大多数 软件测试公司 利用谷歌的这个扩展来提出与层和 UI/UX 测试相关的问题。

## **chro path 的特性**

*   ChroPath 在 dev tools 面板中作为侧边栏选项卡打开。
*   获得元素或所选节点的绝对 XPath 和 CSS 选择器很有帮助。
*   ChroPath 为所选元素生成唯一的相对 XPath 和 CSS 选择器。
*   它还可以用来验证 XPath/CSS 选择器，并允许您查看顺序出现的匹配节点。
*   如果匹配元素不在网页的可见区域，当鼠标悬停在匹配节点上时，它会自动滚动到该区域。
*   验证 XPath 时，如果输入的 XPath 表达式模式不正确或不完整，它会以红色突出显示。

现在，您已经对 ChroPath 有了一些了解，让我们进一步了解 ChroPath 的工作原理和示例。

**chro path 的工作**

它主要涉及四点:

1.  为谷歌 Chrome/Mozilla Firefox 添加 ChroPath 扩展。
2.  检查元件并选择 ChroPath。
3.  从 ChroPath 菜单中复制所需的 XPath 和 CSS 选择器。
4.  执行程序。

下面简单讨论一下以上四点。

1.  第一步是安装或添加 ChroPath 扩展。这很简单，你只需要在谷歌中搜索 ChroPath，然后将这个插件添加到你的 chrome 中，如下图所示。![Chropath extension - New Features of Chropath - Edureka](img/292416954d9f1c89a805581227280674.png)
2.  一旦添加了 ChroPath 扩展，您只需刷新网页，单击任何元素，然后选择 Inspect。在选择“inspect”选项卡时，您会发现添加了 ChroPath 扩展，如图所示。![](img/e84a2a32f353f16c1bbe56f75b34f8f6.png)
3.  现在，您可以选择所选元素的指定 XPath 或 CSS 选择器。在下图中，我已经检查了 yahoo 登录页面，所以我将从 ChroPath 菜单中选择 XPath 和 CSS 选择器。![](img/f38145d13cecd1f0452e896411b0c89b.png)
4.  最后一步是简单地复制 XPath 和 CSS 选择器，并将其粘贴到您的 [Java](https://www.edureka.co/blog/java-tutorial/) 程序中，然后运行代码。您将获得期望的输出。

```
package Edureka;
import java.util.concurrent.TimeUnit;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
public class CustomXpath {
public static void main(String[] args) {
System.setProperty("webdriver.chrome.driver", "C:Selenium-java-edurekachromedriver_win32chromedriver.exe");
WebDriver driver = new ChromeDriver();
driver.manage().window().maximize();
driver.manage().deleteAllCookies();
driver.manage().timeouts().pageLoadTimeout(40, TimeUnit.SECONDS);
driver.manage().timeouts().implicitlyWait(30, TimeUnit.SECONDS);
driver.get("<a href="https://login.yahoo.com/">https://login.yahoo.com/</a>");
driver.findElement(By.xpath("//input[@id='login-username']")).sendKeys("edureka@yahoo.com"); //xpath for search box
driver.findElement(By.cssSelector("#login-username")).sendKeys("edureka@yahoo.com"); //CSS Selector for search box
}
}

```

执行上述代码时，给定的电子邮件地址将被输入到电子邮件文本框中。事情就是这样的。它非常简单，因为它减少了搜索 XPath 和 CSS 选择器的手工工作。

你也可以使用 ChroPath extension for Mozilla Firefox。ChroPath 的工作方式保持不变。这个 把我们带到了这篇关于 ChroPath for XPath 和 CSS 选择器的新特性的文章的结尾。希望对你有帮助，让你的知识增值。

*如果您希望学习 Selenium 并在测试领域建立自己的事业，那么请在这里查看我们的交互式在线直播 **[Selenium 认证培训](https://www.edureka.co/testing-with-selenium-webdriver)** ，它将为您提供全天候支持，在整个学习期间为您提供指导。*

*有问题吗？请在 Chropath for XPath 和 CSS 选择器文章的新特性的评论部分提到它，我们会尽快回复您。*