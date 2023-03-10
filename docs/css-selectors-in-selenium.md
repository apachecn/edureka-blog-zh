# 如何在 Selenium 中使用 CSS 选择器定位 Web 元素？

> 原文：<https://www.edureka.co/blog/css-selectors-in-selenium/>

在 Selenium WebDriver 中，为了与 web 元素交互，比如点击，或者输入一些东西，我们需要首先定位这些元素。测试自动化工程师最重要的任务之一是能够识别网页上的不同元素。有几个 [***元素定位器***](https://www.edureka.co/blog/locators-in-selenium/) 但是，使用 CSS 选择器定位元素是首选方式，因为它比 XPath 更快。

我希望你们一定已经理解了如何使用 [***XPath***](https://www.edureka.co/blog/xpath-in-selenium/) 和帮助定位 XPath、[***ChroPath***](https://www.edureka.co/blog/new-features-of-chropath/)的插件在网页上定位元素，这些是 Selenium 中广泛使用的元素定位器。因此，在这篇文章中，我们将看到 CSS 如何在寻找一个元素的前线。更多细节可以参考[硒训练](https://www.edureka.co/selenium-certification-training)。

以下是我们将在博客中涉及的话题:

*   [什么是定位器？为什么用？](#What_are_locators?_Why_is_it_used?)
*   [不同类型的定位器](#Different_types_of_locators)
*   [CSS 定位器是什么？【T2](#What_are_CSS_locators)
*   [命令](#Commands)
*   [演示](#Demo)

让我们开始讨论，了解硒中的元素定位器是什么，为什么它如此重要。

## **CSS 选择器:什么是元素定位器？为什么用？**

定位元素的确是一场噩梦，因为在网页中找到一个 web 元素及其复杂性。为了简化这个任务，我们在 [***【硒】***](https://www.edureka.co/blog/what-is-selenium/) 中使用了被称为定位器的东西。

定位符被定义为在网页内唯一标识网络元素的地址。它基本上是一个命令，告诉***IDE***喜欢哪些 GUI 元素——文本框、按钮、复选框等。它需要动手术。

![Selenium Locators - Locators in Selenium - Edureka](img/a9d2a761888dc59fa7ef37144989f147.png)

找到正确的 GUI 元素被认为是创建自动化脚本的先决条件，但是，准确识别 GUI 元素比听起来要困难得多。有时，您甚至可能最终使用不正确的 GUI 元素或者根本没有元素！因此，使用正确的定位器可确保测试更快、更可靠或维护更少。

这有助于我们理解硒的实际功能。现在您已经理解了什么是元素定位器，让我们更深入地了解 Selenium 中的各种类型的定位器。从[自动化测试认证](https://www.edureka.co/masters-program/automation-testing-engineer-training)中了解更多自动化测试及其应用。

## **CSS 选择器:不同类型的硒定位器**

web 元素有不同的范围，如文本框、复选框、下拉菜单、单选按钮等。它需要一种有效和准确的方法来识别这些元素。因此，你可以提出，随着 locator 有效性的增加，自动化脚本的稳定性也会增加。

![Types of Locators- CSS Selectors -Edureka](img/3ef4d338d6dde5b5f8774c67b3bac473.png)

为了准确无误地识别 web 元素，Selenium 使用了不同类型的定位器。它们如下:

*   Id 定位器
*   名称定位器
*   链接文本&部分链接文本
*   CSS 选择器
*   XPath

下面我们来详细了解一下他们每一个人。

1.  **ID 定位器:**识别 web 元素最流行的方法是使用 ID。ID 被认为是最安全和最快的定位器选项，应该始终是多个定位器中的第一优先选项。
2.  **名称定位器:**这也是定位具有名称属性的元素的有效方法。使用这种策略，将返回具有 name 属性值的第一个元素。如果没有元素具有匹配的名称属性，那么将引发一个 **NoSuchElementException** 。
3.  **LinkText&ParialLinkText:**你可以用这个 *linkText* 来识别网页上的超链接。可以借助*锚定标签* ( < a >)来确定。为了在网页上创建超链接，可以在链接文本后使用锚标记。在某些情况下，您可能需要通过 *linkText* 元素中的部分文本来查找链接。在这种情况下，您可以使用*部分链接文本*来定位元素。
4.  **CSS 选择器:** CSS 主要用于为网页提供样式规则，你可以用它来标识网页中的一个或多个元素。CSS 选择器始终是在页面中定位复杂元素的最佳方式。我们将在下一个主题中更多地讨论 CSS 选择器。
5.  **XPath:** XPath 是一种查询 XML 文档的语言。 ***[XPath](https://www.edureka.co/blog/xpath-in-selenium/)*** 是定位硒中元素的重要策略。它还包含一个路径表达式和一些条件。在这里，您可以轻松地编写 XPath 脚本/查询来定位网页中的任何元素。

另外，看看这个关于 Selenium 中不同类型的元素定位器的视频。

## **Selenium web driver 中的定位器| Selenium 中的元素定位器| Selenium Training**



[https://www.youtube.com/embed/jK_4nnEJVHQ?rel=0&controls=0&showinfo=0](https://www.youtube.com/embed/jK_4nnEJVHQ?rel=0&controls=0&showinfo=0)This Edureka video on Locators in Selenium talks about different types of selenium locators and steps involved to locate a web element using locators along with examples.Having understood this, let’s understand the main concept of this article, What are CSS Selectors in Selenium Webdriver.

## **CSS 选择器:CSS 选择器是什么？**

众所周知，每一个现代网页都是由 CSS 构建的，它们定义了外观行为(如大小、字体、倾斜度等)。)和/或页面中的对象。CSS 规则根据对象的类名进行分组，以定义这些对象的组合外观行为。类似地，我们可以使用 Object 的 id 属性来定义单个对象的外观。我们也可以使用 CSS 属性来识别对象。

这个 CSS 选择器是一个元素和一个选择器值的组合，用来识别网页中的 web 元素。元素和选择器值的组合被称为*选择器模式*。这个选择器模式是使用 HTML 标签、属性及其值构建的。

使用 CSS 选择器定位元素有一些好处:

*   更快
*   更具可读性
*   和使用更频繁的

现在让我们看看几个有助于定位元素的基本命令。

## **CSS 选择器:基本命令**

首先，我们来看看语法。

**CSS 选择器的语法**

![Syntax - CSS Selector - Edureka](img/be5cf79378b55ed64e224845e5e7551d.png)

*   **HTML 标签**:用来表示 web 元素的标签。
*   **#:** 哈希符号用来象征 ID 属性。如果正在使用 ID 属性，则必须使用散列符号。
*   **ID 属性的值**–是正在被访问的 ID 属性的值。ID 的值前面总是有一个散列符号。

举例:

`driver.findElement(By.cssSelector("#gh-btn")).click();`

如果我们指定了类属性，

![Commands- CSS Selector- Edureka](img/d022fccdfb363683dd779ba5faff2f0d.png)

该命令有助于找到指定了 class 属性的元素。

*   T1。–点号用来象征阶级属性。如果正在使用类属性，则必须使用点号。
*   Class 的值前面总是有一个点号。

举例:

driver . find element(by . CSS selector(class。type ahead _ _ button’)。单击()；

*   **< HTML 标签>【定位器* = '值'】**

![Syntax - CSS Selector - Edureka](img/ffd3ec6614a1fe2757c9582537452692.png)

*   该命令用来借助匹配子串来对应字符串。
*   *****–使用子串匹配字符串的符号表示法。
*   **子串**–执行匹配操作所基于的字符串。期望可能的字符串具有指定的字符串模式

举例:

CSS = input # Passwd[name $ = ' wd ']

**< HTML 标签>【定位器^ = '值'】**

**![Syntax 2 - CSS Selector - Edureka](img/d8867657940dd127a1a137f4166eac42.png)**

*   **^**–使用前缀匹配字符串的符号表示法。
*   **前缀**–执行匹配操作所基于的字符串。可能的字符串应该以指定的字符串开始。

例子

css=input#passwd[name^='pass'】

**< HTML 标签>【定位器$ = '值'】**

*   **$**–使用后缀匹配字符串的符号表示法。
*   **后缀**–它是执行匹配操作所基于的字符串。可能的字符串应该以指定的字符串结尾。

例子

CSS = input # Passwd[name $ = ' wd ']

*   **< HTML 标签> < : > <包含> <(文本)>**

*   **:**–圆点符号用来象征包含一个方法
*   包含–它是被访问的类属性的值。
*   Text——显示在网页上任何位置的文本，与它的位置无关。
*   由于其简化的语法，这是定位 web 元素最常用的策略之一。

例子

CSS = input # Passwd[name:' Pass ']

理解了这一点，我们将继续看一个演示，从中我们将了解 Selenium Webdriver 中 CSS 选择器是如何工作的。

## **Selenium web driver 中的 CSS 选择器| Selenium 教程| Selenium 认证培训**



[https://www.youtube.com/embed/6fFL-KdEPfQ?rel=0&controls=0&showinfo=0](https://www.youtube.com/embed/6fFL-KdEPfQ?rel=0&controls=0&showinfo=0)This ‘CSS Selector in Selenium’ video by Edureka helps you understand how this locator aids to identify elements on a web page.

## **CSS 选择器:演示**

我们将在一个最著名的电子商务网站上进行自动化测试，即本演示中的*Ebay.com*。让我们看看如何做到这一点。我们将看到如何注册 chrome 的驱动程序，以及如何在页面上搜索元素。我们将考虑在 Eclipse IDE 上工作，因为它很容易执行 Java 程序。

对于谷歌 chrome，你需要在你的系统中安装一个 ***[chrome 驱动](http://chromedriver.chromium.org/downloads)*** 。现在让我们仔细看看代码。如你所见，

*   我已经用 *System.setproperty()* 设置了 chrome 驱动的路径。
*   然后我使用 *driver.get()* 导航到**ebay.com**。
*   最大化网页
*   初始化 JavascriptExecutor，它在使用 Selenium 时充当接口
*   使用 CSS 选择器找到搜索框，在指定 ID 之前添加一个 **#** ，然后向搜索框发送关键字。
*   使用 CSS 选择器搜索网页上的搜索图标并点击它。
*   然后我们将使用 JavascriptExecutor 向下滚动网页，并指定我们想要滚动的轴。

```

package co.edureka;

import org.openqa.selenium.By;
import org.openqa.selenium.JavascriptExecutor;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;

public class DemoClass {

public static void main(String[] args) {
System.setProperty("webdriver.chrome.driver", "C:UsersVaishnaviDesktopChromechromedriver.exe");
WebDriver driver = new ChromeDriver();
driver.get("http://ebay.com");
driver.manage().window().maximize();
JavascriptExecutor js = (JavascriptExecutor) driver;
driver.findElement(By.cssSelector("#gh-ac")).sendKeys("OnePlus6T");
driver.findElement(By.cssSelector("#gh-btn")).click();
js.executeScript("window.scrollBy(0,300)");
}

}

```

这产生了输出

*![Output - CSS Selector - Edureka](img/d3c287833a31391235aa32d875da1abb.png)*

首先，这将打开*ebay.com*，然后我们将搜索 OnePlus6T 并点击搜索图标。

*![Output 2 - CSS Selector - Edureka](img/b84876353bf6209c9c7465ebf8449ac5.png)*

在这之后，我们将向下滚动页面。

*![Output 3 - CSS Selector - Edureka](img/00ece9eea226f43790d2acdb277e4364.png)*

*至此，我们结束了这篇“Selenium 中的 CSS 选择器”的博客。我希望你们喜欢这篇文章，并且理解 CSS 在 Selenium 中扮演的角色。现在，您已经了解了如何使用 CSS 选择器定位元素，请查看 Edureka 的 **[Selenium 认证课程](https://www.edureka.co/selenium-certification-training)** ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 650，000 名满意的学习者。本课程旨在向您介绍完整的 Selenium 特性及其在软件测试中的重要性。有问题吗？请在“Selenium 中的 CSS 选择器”的评论部分提到它，我们会回复您。*