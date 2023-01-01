# Selenium 中的 setProperty 是什么，如何使用它？

> 原文：<https://www.edureka.co/blog/what-is-setproperty-in-selenium/>

网站测试的主要基础是实例化浏览器对象并设置浏览器驱动程序的系统属性。这是通过 *setProperty()* 方法实现的。在本文中，我将告诉您 [Selenium](https://www.edureka.co/blog/selenium-tutorial/) 中的 setProperty 是如何工作的。

本文涵盖以下主题:

*   硒的 setProperty 是什么？
*   [演示:演示 set 属性](#Demo:IllustratingsetProperty)

我们开始吧！

## 硒的 setProperty 是什么？

setProperty，顾名思义，有两个属性，分别是-`“System.setProperty(“propertyName”, “value”)”`。这意味着它将系统属性`‘propertyName'`设置为值`'value'.`

当[用 Selenium](https://www.edureka.co/blog/what-is-selenium/) 测试时，您将使用 setProperty 方法，因为浏览器没有内置的服务器来运行自动化代码。在这种情况下，您将需要一个 [Chrome/IE/Gecko 驱动程序](https://www.edureka.co/blog/selenium-chromedriver-and-geckodriver/)服务器来将您的 Selenium 代码传递给浏览器。

简而言之，要为各自的浏览器设置驱动程序的路径，你需要***system . set property .***

现在我们举一个小例子来理解它的工作原理。

## **演示:演示 Selenium 中的 set 属性**

看看下面的代码就知道它是如何工作的了。

```
import java.util.concurrent.TimeUnit;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
public class Demo {
public static void main(String[] args) {
// Here I am setting the system properties of chrome driver and specifying the path to it.
System.setProperty("webdriver.chrome.driver", "C:Selenium-java-edurekachromedriver_win32chromedriver.exe");
// Creating a object to instantiate the browser driver
WebDriver driver = new ChromeDriver();
//Navigating through a particular website
driver.get("https://www.ebay.com/");
//Locating elements using XPath locator for search box
driver.findElement(By.xpath("//input[@id='gh-ac']")).sendKeys("Guitar");
WebElement searchIcon = driver.findElement(By.xpath("//input[@id='gh-btn']"));//xpath for search button
searchIcon.click();
}
}
```

当您执行上述代码时，它将使用 Chrome 驱动程序在 Google Chrome 中启动 ebay 网站，其中驱动程序的初始化由 system.setproperty 方法处理。在初始化驱动程序的任何测试方法之前，这必须是 selenium 脚本中需要执行的第一行代码。事情就是这样的。如果你想使用火狐浏览器和 Gecko 驱动程序，你可以相应地使用它们。借助 Selenium 文章中的 [Gecko Driver 学习 Gecko Driver 的工作原理。](https://www.edureka.co/blog/selenium-chromedriver-and-geckodriver/#WhatisGeckoDriver?)

我希望这能让你清楚地了解[硒](https://www.seleniumhq.org/) 中的*设置属性是如何工作的。因此，它把我们带到了这篇文章的结尾。*

*如果您希望学习 Selenium 并在测试领域建立自己的事业，那么请查看我们的交互式在线直播 **[Selenium 认证](https://www.edureka.co/selenium-certification-training)** ，它提供 24*7 支持，在整个学习期间为您提供指导。*

*有问题吗？请在 Selenium 博客的 setProperty 的评论部分提到它，我们将会回复您。*