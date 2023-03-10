# 使用 Python 的 Selenium 您需要知道的一切

> 原文：<https://www.edureka.co/blog/selenium-using-python/>

如果你问一个懒惰的程序员，他最喜欢的编程语言是哪一种，很大概率你会得到“***【Python***”作为答案。Python 被认为是最流行和最受欢迎的编程语言之一。众所周知， [Selenium](https://www.edureka.co/blog/selenium-tutorial) 是 web 应用程序自动化测试的完美工具。因此，与其他编程语言相比，Python 帮助我们以更简单的方式编写 Selenium 脚本。因此，我提出了这篇关于使用 Python 开发 Selenium 的文章，其中我将涉及以下主题:

*   [硒简介](#IntroductiontoSelenium)
*   [Python 简介](#IntroductiontoPython)
*   [硒与蟒蛇结合](#SeleniumandPythonBinding)
*   [使用 Python 定位 web 元素](#LocatingwebelementsusingPython)

*如果你想通过认证硒专家掌握硒的概念，请参考[硒培训](https://www.edureka.co/selenium-certification-training)或查看下面的视频，其中涵盖了更广泛的主题。*

## **使用 Python 测试自动化| Selenium Webdriver 教程使用 Python**



[//www.youtube.com/embed/CwLrdjgsJjU?rel=0&showinfo=0](//www.youtube.com/embed/CwLrdjgsJjU?rel=0&showinfo=0)

本视频将向您全面介绍 Python 的 Selenium 基础知识。

## **硒简介**

[Selenium](https://www.edureka.co/blog/what-is-selenium/) 是一款开源工具，用于自动化在 web 浏览器上执行的测试用例，或使用任何 web 浏览器进行测试的 web 应用程序。 等等，在你忘乎所以之前，让我重申一下，只有测试 web 应用程序才可能使用 Selenium。我们既不能测试任何桌面软件应用程序，也不能使用 Selenium 测试任何移动应用程序。所以它是一个开源工具，支持交叉浏览和自动化网络应用！

![What is Selenium - Selenium Using Python - Edureka](img/f6baa64c7a8b155889ddb5859b34843d.png)现在继续，让我们看看*为什么我们需要 Selenium IDE 进行自动化测试*？

正如我已经提到的——[Selenium](https://www.edureka.co/blog/selenium-webdriver-tutorial)是开源的，并且不涉及许可成本，这是相对于其他测试工具的一个主要优势。Selenium 日益流行背后的其他主要原因包括它们的测试用例、操作系统平台和浏览器支持。

与其他自动化工具相比， 这些是  保持领先的原因。现在让我们更深入地研究这篇文章，了解什么是 Python？

## **Python 简介**

[Python](https://www.edureka.co/blog/python-tutorial) 非常简单易学。它是最强大的语言之一，非常像英语！ 那么，是什么促成了它的简洁呢？Python 是

*   免费&开源
*   高层
*   解读
*   有幸拥有一个庞大的社区

Python 也有很多内置的测试框架，涵盖了调试&最快的工作流程。有很多工具和模块可以让事情变得更简单，如 *【硒】* 和 *Splinter 和 [Python](https://www.edureka.co/blog/python-programming-language) 也* 支持跨平台测试的&跨浏览器框架，如*PyTest*和 *机器人* 框架。

理解了这一点，现在让我们来理解 Selenium 和 Python 之间的绑定。

## **硒与蟒蛇结合**

![Selenium Python Binding - Selenium Using Python - Edureka](img/a5dcc1a164ba24403554c9f531b6ad03.png)第一步是使用 [Selenium](https://www.edureka.co/blog/selenium-tutorial) web 驱动编写您的功能测试，之后，您需要向 Selenium 服务器发送请求，然后在各种浏览器上执行测试用例。可以是谷歌 Chrome、Internet Explorer 或者 Mozilla Firefox。

现在，为了用 Selenium 实现 Python，我们首先需要导入 Selenium web 驱动程序！

首先，让我告诉你什么是 Selenium web driver。

Selenium 中的 [WebDriver 是一个基于 web 的](https://www.edureka.co/blog/selenium-tutorial)[自动化测试框架](https://www.edureka.co/blog/test-automation-frameworks/)，可以测试在各种 web 浏览器和各种操作系统上发起的网页。为了导入和配置依赖项以添加库和功能，您需要在以下命令的帮助下导入 Selenium Webdriver。

```
from selenium import webdriver
from selenium.webdriver.common.keys import keys
from selenium.import.*

```

这是关于 [Python](https://www.edureka.co/blog/python-tutorial/) 和 Selenium 之间的绑定。现在让我们进一步了解如何使用 Python 在 Selenium 中定位元素。

## **使用 Python 定位 Web 元素**

[Python 编程语言](https://www.edureka.co/blog/python-tutorial/)提供了各种框架，如 [Django](https://www.edureka.co/blog/django-tutorial) 、flask 等。你可以自定义它的主题和插件&它也可以让你提高生产力，而 **编码** 通过提供一些功能，如建议，本地 VCS 等。您可以使用任何工具，如 Jupyter Notebook、Anaconda 和 PyCharm，用 Python 编写 Selenium 脚本。N 现在我们来看看Selenium 中的[定位符是什么？](https://www.edureka.co/blog/locators-in-selenium/)

定位符是作为在网页内唯一标识网页元素的地址。定位器是 web 元素的 HTML 属性，它告诉 [Selenium](https://www.edureka.co/blog/selenium-framework-data-keyword-hybrid-frameworks) 它需要对哪个元素执行操作。 Selenium 使用定位器与网页上的 web 元素进行交互。

现在，有各种各样的 web 元素，如文本框、id、单选按钮等，识别这些元素一直是一个非常棘手的问题。因此，这需要一种准确有效的方法。因此，我们可以说定位器越有效，自动化脚本就越稳定。每个 Selenium 命令都需要定位器来查找 web 元素。因此，为了准确无误地识别这些 web 元素，我们有不同类型的定位器，即:

*   ID
*   名称
*   链接文本
*   CSS 选择器
*   部分链接文本和
*   XPath

如果你想详细了解这些定位器，你可以在 Selenium 阅读这篇关于[定位器的文章。](https://www.edureka.co/blog/locators-in-selenium/)

现在让我们看一个小例子来理解 Selenium 中使用 Python 的定位器的工作原理。

我将启动谷歌浏览器，导航到 hotstar.com 的。在这里，我将尝试使用 [**ID 定位器**](https://www.edureka.co/blog/locators-in-selenium/#Idlocator) 定位*搜索框*。

![C:UsersNeha_VaidyaDesktopHotstar Id example - Selenium Using Python - Edureka.png](img/6c571baf291d222949958f3feedcfb41.png)

检查上面的 web 元素，您可以看到它有一个输入标签和属性，如 class 和 id。现在，我将使用 Id 定位器的值，即**搜索字段**来定位搜索框。

![Inspect ID box - Selenium Using Python - Edureka](img/de784b97837bf95ede1717992aab229f.png)

让我们看看如何自动化搜索框，并使用 Id locator 向它发送值。

```
from selenium import webdriver
driver = webdriver.Chrome("C:UsersNeha_Vaidyaeclipse-workspaceSeleniumchromedriver_win32chromedriver.exe")
driver.get("https://www.hotstar.com")
driver.find_element_by_id("searchField").send_keys("Movies")

```

当你运行上面的代码， ***chrome 驱动*** 将启动谷歌 chrome，重定向到 Hotstar，在搜索框中输入值为‘Movies’。

我希望这能让你清楚地了解 [Selenium](https://www.edureka.co/blog/10-reasons-to-learn-selenium/) 中的 Id 定位器是如何工作的。现在让我们进一步了解如何使用[名称定位器](https://www.edureka.co/blog/locators-in-selenium/#Namelocator)。

现在假设你希望谷歌自动搜索一个元素，让我们看看如何在名称定位器的帮助下做到这一点。最初，我将检查谷歌搜索框，并检索名称属性的值，即' q '。下一步是将值发送到搜索框。一旦您将这些值发送给 search，它就会自动搜索 Selenium。你可以看看下面的 Python 代码。

```
from selenium import webdriver
driver = webdriver.Chrome("C:UsersNeha_Vaidyaeclipse-workspaceSeleniumchromedriver_win32chromedriver.exe") 
driver.get("https://www.google.com")
driver.find_element_by_name("q").send_keys("Selenium")
driver.find_element_by_name("btnK").click()

```

基本上，这就是它的工作方式。现在让我们看看使用 [XPath](https://www.edureka.co/blog/xpath-in-selenium/) 定位元素的通用代码。

```
from selenium import webdriver
driver = webdriver.Chrome("C:UsersNeha_Vaidyaeclipse-workspaceSeleniumchromedriver_win32chromedriver.exe")
driver.get("https://www.hotstar.com")
driver.find_element_by_xpath("//div[@class='signIn displayElement']").click()&nbsp; &nbsp;# Click on login icon
driver.find_element_by_xpath("//input[@name='email']").send_keys("xyz@edureka.co") # Entering email address
driver.find_element_by_name("password").send_keys("edureka123")&nbsp; &nbsp; #Entering the given password
driver.find_element_by_xpath("//button[@type='submit']").click()&nbsp; &nbsp; &nbsp; #Clicking submit button to login

```

上面的代码描述了 hotstar.com 的登录。首先，我将使用 [XPath](https://www.edureka.co/blog/new-features-of-chropath/) 点击登录图标，然后输入电子邮件地址和密码。之后，再次使用 XPath，我将点击提交按钮，通过 hotstar.com 登录。所以登录过程的每一步都是在 XPath 定位器的帮助下进行的。这就是它的工作原理。如果您希望深入学习 XPath 及其基础知识，可以阅读这篇关于 Selenium 中的 [**XPath 的文章。**](https://www.edureka.co/blog/xpath-in-selenium/)

至此，我们结束了这篇关于使用 [Python](https://www.edureka.co/blog/10-reasons-why-you-should-learn-python) 开发 Selenium 的文章。希望对你有帮助，让你的知识增值。

*如果您希望学习 Selenium 并在测试领域建立自己的事业，那么请在此处查看我们的交互式在线直播 **[Selenium 认证培训](https://www.edureka.co/selenium-certification-training)** ，它提供 24*7 支持，在整个学习期间为您提供指导。*

*有问题吗？请在 Selenium 使用 Python 文章的评论部分提到它，我们会尽快回复您。*