# Selenium 教程:关于 Selenium WebDriver 您需要知道的一切

> 原文：<https://www.edureka.co/blog/selenium-tutorial>

## **Selenium 教程——Selenium web driver**

在这篇 Selenium 教程文章中，我将向您介绍 Selenium Webdriver，它是当今市场上最流行的自动化测试框架。它是开源的，可以用于所有著名的编程语言，如 Java、Python、C#、Ruby、Perl 等。，用于自动化浏览器活动。通过这篇文章，我将告诉您开始使用 Selenium WebDriver 测试 web 应用程序所需要知道的一切。

以下是我将在这篇关于 Selenium 教程的文章中涉及的主题:

*   [什么是 Selenium WebDriver？](#WhatIsSeleniumWebDriver)
*   [硒好学吗？](#learnselenium)
*   [硒软件是做什么的？](#seleniumuses)
*   [硒的基础是什么？](#seleniumbasics)
*   [Selenium RC 的弊端和 WebDriver 的诞生](#DrawbacksOfSeleniumRC)
*   [什么是浏览器元素？【T2](#WhatAreBrowserElements)
*   [在网页上定位浏览器元素](#LocatingBrowserElements)
*   [对浏览器元素的操作](#OperationsOnBrowserElements)

这个硒教程博客会让你一窥 ***[硒训练](https://www.edureka.co/selenium-certification-training)*** 所需的所有重要概念。

## **什么是 Selenium WebDriver？**

Selenium WebDriver 是一个基于 web 的自动化测试框架，可以测试在各种 web 浏览器和各种操作系统上启动的网页。实际上，你也可以像 [Java](https://www.edureka.co/blog/java-tutorial/) ，Perl， [Python](https://www.edureka.co/blog/learn-python/) ， [Ruby](https://www.edureka.co/blog/ruby-on-rails-tutorial/) ，C#， [PHP](https://www.edureka.co/blog/php-frameworks/) ，以及 [JavaScript](https://www.edureka.co/blog/javascript-tutorial/) 等不同的编程语言自由编写测试脚本。请注意，Mozilla Firefox 是 Selenium WebDriver 的默认浏览器。

但是很多时候，初露头角的测试人员会有这种疑虑，

## **硒好学吗？**

用非常外行的话来回答这个问题，我会说:“是的，它是！”。Selenium 真的很容易学习和掌握，因为你需要对任何著名的编程语言有一个基本的了解，比如 Java、C#、Python、Perl、Ruby、PHP。拥有这些编程语言中任何一种的知识对于编写测试用例来说都是很方便的。但是如果你没有，那就不要担心。Selenium IDE 是基于 GUI 的工具，您可以有效地使用它。

## 【Selenium 软件是做什么的？

下面是 Selenium 软件的一些最有趣的用法:

1.  ***自动化测试:*** 自动化测试在大型项目中很方便，如果没有 Selenium，测试人员将不得不手工测试每一个创建的功能。有了 Selenium，所有的手工任务都自动化了，从而减轻了测试人员的负担和压力。
2.  ***跨浏览器兼容性:*** Selenium 支持 Chrome、Mozilla Firefox、Internet Explorer、Safari、Opera 等多种浏览器。
3.  ***增加测试覆盖率:*** 随着测试的自动化，总体测试时间减少，这使得测试人员有更多的时间在同一时间对不同的测试场景执行更多的测试。
4.  ***减少测试执行时间:*** 由于 Selenium 支持并行测试执行，所以对减少并行测试执行时间有很大帮助。
5.  ***多操作系统支持:*** Selenium WebDriver 提供跨 Windows、Linux、UNIX、Mac 等多种操作系统的支持。使用 Selenium WebDriver，您可以在 Windows 操作系统上创建一个测试用例，并在 Mac OS 上执行它。

### **硒的基础是什么？**

WebDriver 是作为 Selenium v2.0 的一部分引入的。Selenium v1 只包含 IDE、RC 和 Grid。但是 Selenium 项目的主要突破是在 Selenium v2 中开发和引入 WebDriver 作为替代品的时候。然而，随着 Selenium v3 的发布，RC 已经被弃用，并被转移到一个遗留包中。你仍然可以下载并使用 RC，但是不要期望它会得到任何支持。

简单来说，WebDriver 相对于 RC 的优势是:

*   支持更多编程语言、操作系统和网络浏览器
*   克服 Selenium 1 的局限性，如文件上传、下载、弹出窗口&对话框障碍
*   与 RC 相比，命令更简单，API 更好
*   支持批量测试、跨浏览器测试&数据驱动测试

但是与 RC 相比，它的缺点是无法生成测试报告。RC 生成详细的报告。

下图描述了 WebDriver 的工作方式:

![webdriver - selenium tutorial](img/18ef7dfe73efa4ab84a32b212c99fbfa.png)

但是你有没有想过为什么需要 Selenium Webdriver？在这篇 Selenium 教程文章的下一节中，我将讨论 Selenium RC 的限制，因为这是最终开发 WebDriver 的原因。

## **Selenium RC 的弊端和 WebDriver 的诞生**

当我说 Selenium RC 一经推出就一炮而红时，你可能会感到惊讶。这是因为它克服了**同源策略**问题，这是用 Selenium Core 测试 web 应用时的一个主要问题。但是你知道同源政策的问题是什么吗？

同源策略是实施 web 应用安全模型的规则。根据同源策略，当且仅当被测试的 JavaScript 和网页都来自同一个域时，网络浏览器才允许 JavaScript 代码访问网页上的元素。Selenium Core 是一个基于 JavaScript 的测试工具，由于同样的原因，它不能测试每个网页。

但是当 Selenium RC 出现时，它解决了测试人员的同源策略问题。但是，RC 是怎么做到的呢？RC 通过使用另一个名为 **Selenium RC 服务器**的组件来完成这项工作。所以，RC 是一个由两个组件组合而成的工具: **Selenium RC 服务器**和 **Selenium RC 客户端**。

Selenium RC server 是一个 HTTP 代理服务器，旨在“欺骗”浏览器，使其相信 Selenium Core 和正在测试的 web 应用程序来自同一个域。因此，无法阻止 JavaScript 代码访问和测试任何网站。

尽管 Selenium RC 大受欢迎，但它也有自己的问题。其中最主要的是执行测试所花费的时间。因为 Selenium RC 服务器是浏览器和 Selenium 命令之间通信的中间人，所以测试执行非常耗时。除了时间因素，RC 的架构也略显复杂。

该架构首先将 Selenium Core 注入网络浏览器。然后 Selenium Core 将从 RC 服务器接收指令，并将其转换为 JavaScript 命令。这段 JavaScript 代码负责访问和测试 web 元素。如果你看下面的图片，你会知道 RC 是如何工作的。

![rc architecture - selenium tutorial](img/e417303fc2cbcfc3245fbce868e455f1.png)

为了克服这些问题，开发了 Selenium WebDriver。WebDriver 速度更快，因为它直接与浏览器交互，不涉及外部代理服务器。架构也更简单，因为浏览器是从操作系统级别控制的。下图将帮助你理解 WebDriver 是如何工作的。

![webdriver architecture - selenium tutorial](img/c727690fddaf1fa7f0c86403afb0507d.png)

WebDriver 的另一个好处是它支持在 HTML 单元驱动上测试，这是一个无头驱动。我们说的无头驱动，是指浏览器没有 GUI。另一方面，RC 不支持 HTML 单元驱动程序。以上是 WebDriver 得分超过 RC 的一些原因。

在学习 Selenium 的概念之前，您应该对 Java 或任何其他 **对象** 面向编程语言有一个基本的了解。Selenium 支持的语言包括 C#、Java、Perl、PHP、Python 和 Ruby。目前，Selenium Webdriver 最受 Java 和 C#的欢迎。

现在让我们继续前进，在 Selenium 教程的下一部分学习“浏览器元素”,我将告诉你这些元素是什么，以及如何在这些 web 元素上进行测试。

## **什么是浏览器元素？**

元素是呈现在网页上的不同组成部分。我们在浏览时最常注意到的元素是:

*   文本框
*   CTA 按钮
*   图像
*   超链接
*   单选按钮/复选框
*   文本区/错误信息
*   下拉框/列表框/组合框
*   Web 表格/ HTML 表格
*   帧

测试这些元素本质上意味着我们必须检查它们是否工作正常，是否按照我们想要的方式做出响应。例如，如果我们测试文本框，你会测试它做什么？

1.  我们是否能够向文本框发送文本或数字
2.  我们能否检索已经传递到文本框的文本等。

如果我们正在测试一个图像，我们可能想要:

1.  下载图像
2.  上传图像
3.  点击图片链接
4.  检索图像标题等。

类似地，可以对前面提到的每个元素执行操作。但是只有在元素被定位到网页上之后，我们才能执行操作并开始测试它们，对吗？所以，我将在 Selenium 教程博客中讨论的下一个主题是元素定位器技术。

## **定位网页上出现的浏览器元素**

网页上的每个元素都有属性。元素可以有多个属性，并且这些属性中的大多数对于不同的元素都是唯一的。例如，假设一个页面有两个元素:一个图像和一个文本框。这两个元素都有一个“Name”属性和一个“ID”属性。对于每个元素，这些属性值需要是唯一的。换句话说，两个元素不能有相同的属性值。元素可以具有相同的“类名”值。

在所考虑的例子中，图像和文本框既不能有相同的“ID”值，也不能有相同的“Name”值。但是，页面上的一组元素有一些共同的属性。稍后我会告诉你这些属性是什么，但在此之前，让我列出 8 个属性，我们可以使用它们来定位元素。这些属性是 ID、名称、类名、标记名、链接文本、部分链接文本、CSS 和 XPath。

由于使用这些属性来定位元素，我们称它们为“定位器”。这些定位器是:

*   **By.id** 语法:driver . find element(by . id(" XXX "))；
*   **by . name**语法:driver . find element(by . name(" XXX "))；
*   **by . class name**语法:driver . find element(by . class name(" XXX "))；
*   **by . tagname**语法:driver . find element(by . tagname(" XXX "))；
*   **by . linktext**语法:driver . find element(by . linktext(" XXX "))；
*   **by . partiallinktext**语法:driver . find element(by . partiallinktext(" XXX "))；
*   **By.css** 语法:driver . find element(by . CSS(" XXX "))；
*   **by . XPath**语法:driver . find element(by . XPath(" XXX "))；

通过查看上面的语法，你可能已经意识到定位器是在方法内部调用的。因此，在进一步学习之前，您需要学习所有其他方法、浏览器命令和函数，这些都可以用来对元素执行操作。

## **对浏览器元素的操作**

从博客的这一部分开始，你将会有很多乐趣，因为理论会更少，代码会更多。所以请做好准备，并保持 Eclipse IDE 打开，安装所需的 Selenium 包。

要开始测试一个网页，我们需要首先打开一个浏览器，然后通过提供网址导航到该网页，对吗？看看下面这段代码，我复制了同样的代码。火狐浏览器将首先被启动，然后它将导航到脸书的登录页面。

```
package seleniumWebDriver;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.firefox.FirefoxDriver;

public class WebDriverClass 
{
public static void main(String[] args) 
{
System.setProperty("webdriver.gecko.driver", "files/geckodriver.exe");
WebDriver driver = new FirefoxDriver();
driver.get("https://www.facebook.com/");
driver.getTitle();
driver.quit();
}
}

```

**导入 org . open QA . selenium . web driver；**是一个库包，其中包含启动浏览器所需的类，该浏览器装有特定的驱动程序。

**导入 org . open QA . selenium . Firefox . Firefox driver；**是一个库包，包含了启动 FirefoxDriver 所需的 FirefoxDriver 类，作为 WebDriver 类发起的浏览器。

**system . set property(" web driver . gecko . driver "，" files/gecko driver . exe ")；–**这个命令通知运行时引擎 Gecko 驱动程序出现在指定的路径中。在 Firefox 35 之后，我们需要下载 Gecko 驱动程序来使用 WebDriver。如果你想在 chrome 上测试，那么你必须下载 ChromeDriver，这是一个. exe 文件，并在这行代码中指定它的路径。在其他浏览器的情况下，我们也必须这样做。

**web driver driver = new Firefox driver()；–**该命令用于启动一个新的 Firefox 驱动程序对象。

**driver . get(" https://www . edu reka . co/"；–**这个方法用于打开指定的 URL。

**driver . gettitle()；**–该命令获取浏览器中当前打开的标签的标题。

**driver . quit()；–**该命令关闭浏览器驱动程序。

但是，如果你想导航到一个不同的网址，然后进行测试呢？在这种情况下，您可以使用 navigate.to()命令，如下面的代码片段所示。如果您想返回上一页，可以使用 navigate.back()命令。类似地，为了刷新当前页面，可以使用 navigate.refresh()命令。

```
driver.navigate().to(“https://www.edureka.co/testing-with-selenium-webdriver”);
driver.navigate().refresh();
driver.navigate().back();

```

如果你想最大化浏览器窗口的大小，你可以使用下面的代码片段。

```
driver.manage().window().maximize(); 

```

如果您想为浏览器窗口设置自定义大小，那么您可以设置自己的尺寸，如下面的代码片段所示。

```
Dimension d = new Dimension(420,600);
driver.manage().window().setSize(d); 

```

现在你已经知道了大部分基础知识，让我们进入这篇 Selenium 教程博客的下一个主题。让我们尝试在 web 页面上找到一个元素，然后执行任何可能的操作。

我很确定，你们都有脸书的账户。所以，让我向你展示如何绕过代码本身的凭证登录到[脸书](https://www.facebook.com/)。

脸书登录页面有两个文本字段，一个用于**电子邮件/电话**，另一个用于**密码**。我们必须找到这两个元素，将凭证传递给这些元素，然后找到第三个元素:**需要单击的登录**按钮。

看下面的截图。是**脸书的**登录页面的截图。

![facebook screenshot - selenium tutorial](img/6ebce9bc9eb09bb55811eb09b9f46d00.png)

如果你检查(Ctlr + Shift + i)这个页面，你会在你的浏览器中看到同样的窗口。然后，在**元素**下，将显示页面上所有元素及其属性的列表。上面的截图中突出显示了三个部分。第一个突出显示的元素是电子邮件文本字段，第二个是密码文本字段，第三个是登录按钮。

如果您还记得，我之前提到过这些元素可以使用元素定位器技术来定位。让我们用它来定位这些元素并发送字段值。 这是查找元素的语法:**driver . find element(by . id(" XXX "))；** 对于发送它的值，我们可以使用方法**sendKeys(*credentials*)；** 对于点击按钮，我们必须使用**的方法 click()；**

因此，让我们开始寻找元素并对其执行操作。它的代码在下面的代码片段中。

```
driver.findElement(By.name("email")).sendKeys("xxx@gmail.com");
driver.findElement(By.name("pass")).sendKeys("xxxxxx");
driver.findElement(By.id("u_0_q")).click();

```

在第 1 行，我们通过唯一的“名称”属性来识别*电子邮件*元素，并向其发送 EmailID。 在第 2 行中，我们通过其唯一的“Name”属性来识别*密码*元素，并向其发送密码。 在第 3 行，我们通过唯一的 ID 定位*登录按钮*元素，并点击该按钮。

仅仅添加这几行代码可能还不够。这是因为页面的动态性，它可能不会立即响应，当页面加载时，WebDriver 将被终止并抛出超时异常错误。这个问题可能不会发生在脸书的网页上，因为它速度很快，但很可能会发生在任何其他电子商务网站和其他动态网站。

为了克服这个问题，我们需要使用一种先进的技术。我们需要请求我们的 WebDriver 在页面被访问后等待，在它完全加载后，我们需要定位元素，然后执行操作。

如果你想让你的 WebDriver 等到所有元素都加载到一个网页中，然后关闭浏览器，那么我们可以通过使用 **driver.wait()** 方法或者 **Threads.sleep()方法**来实现。但是，如果您正在编写更高级的代码，那么您应该使用**隐式等待**或**显式等待**。在 Selenium 教程系列的下一篇博客中，我将解释等待条件的概念。但是对于我们的情况，下面的命令就足够了。

```

driver.wait(5000);
// or use this:-
Thread.sleep(5000);

```

但是，在处理等待条件的同时，记得导入这个库: **导入 Java . util . concurrent . time unit；** 我们这样做是因为，等待类及其相关方法将出现在这个库中。

我解释的整个代码出现在下面的代码片段中。

```
package seleniumWebDriver;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.firefox.FirefoxDriver;
import java.util.concurrent.TimeUnit;

public class WebDriverClass 
{
public static void main(String[] args) 
{
System.setProperty("webdriver.gecko.driver", "files/geckodriver.exe");
WebDriver driver = new FirefoxDriver();
driver.get("https://www.facebook.com/");
driver.manage().window().maximize();
driver.getTitle();
driver.navigate().to(“https://www.edureka.co/testing-with-selenium-webdriver”);

driver.navigate().back();
driver.navigate().refresh();
driver.wait(5000);
// or use
// Thread.sleep(5000);

driver.findElement(By.name("email")).sendKeys("xxx@gmail.com");
driver.findElement(By.name("pass")).sendKeys("xxxxxx");
driver.findElement(By.id("u_0_q")).click();

driver.quit();
}
}

```

当您用您的实际电子邮件和密码替换凭证并执行此代码时，脸书将在一个新窗口中打开，输入您的凭证并登录到您的帐户。

**瞧吧**！您已成功登录，这意味着您的完整代码已完全执行。

我已经使用了 **ID** 和 **Name** 属性来定位元素。事实上，您可以使用任何其他定位器来查找元素。XPath 是定位器技术中最有用和最重要的。但是，只要您能够找到其中的一个属性并使用它们来定位元素，您就应该是优秀的。你可以看到下面由一位行业专家提供的视频，她亲自展示了 Selenium WebDriver 的所有上述特性。

## Selenium WebDriver 教程| Selenium 初学者教程| Selenium WebDriver 培训| Edureka



[https://www.youtube.com/embed/ph3NJm4Z7m4?rel=0&showinfo=0](https://www.youtube.com/embed/ph3NJm4Z7m4?rel=0&showinfo=0)This Selenium WebDriver tutorial talks about the drawbacks of Selenium RC and what was the need for Selenium WebDriver. It goes into the details of the advantages that WebDriver has over RC and how it replaced RC for automation testing.

在这个 Selenium 教程系列中，我的下一篇博客是关于如何将 TestNG 与 Selenium WebDriver 一起使用。我强烈建议您阅读它，因为它谈到了如何通过使用 TestNG 来克服 WebDriver(测试用例管理和报告生成)的局限性。

如果你在执行本博客中的代码时遇到任何问题，或者如果你有任何其他疑问，请在下面的评论区提出，我们会马上回复你。

*如果您希望学习 Selenium 并在测试领域建立自己的事业，请点击此处查看我们的互动在线直播 [Selenium 认证培训](https://www.edureka.co/selenium-certification-training)，它将为您提供全天候支持，在整个学习期间为您提供指导。*

有问题吗？请在“什么是硒”这篇文章的评论部分提到它，我们将会回复您，或者今天就参加我们在曼彻斯特的[硒培训。](https://www.edureka.co/selenium-certification-training-manchester)