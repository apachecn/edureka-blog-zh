# 如何在 Selenium WebDriver 中截图

> 原文：<https://www.edureka.co/blog/how-to-take-a-screenshot-in-selenium-webdriver/>

Automation Testing has defined a new facet of modern day testing and it is here to stay. However, if the testing process fails, it would be highly inconvenient to re-test the entire script. This is where screenshots come in handy, as they help detect test failures instantly. Through the medium of this blog, we will learn how to take a screenshot in Selenium WebDriver. To learn more, check out the [Selenium Training](https://www.edureka.co/selenium-certification-training).

我将讨论以下主题:

*   [为什么自动化测试需要截图？](#Why_Screenshot_is_required_in_Automation_testing?)
*   [如何在 Selenium 中截图？](#How_to_capture_Screenshot_in_Selenium?)

*   [演示](#Demo)

所以，让我们开始吧，伙计们！

## **Selenium web driver 中的截图:为什么自动化测试中需要截图？**

截图对于 bug 分析是可取的。 *[硒](https://www.edureka.co/selenium-certification-training)* 可以在执行过程中自动截图。假设您编写了一个测试脚本来自动化一个 web 页面，您不会一直监视它是否每次都能正常工作。你会让剧本完成它的工作，而你会忙于其他的工作。

*   截图有助于我们理解应用程序的流程，并检查它是否相应地运行。
*   您需要类型转换 WebDriver 实例来拍摄屏幕快照。
*   当您执行[交叉浏览测试](https://www.edureka.co/blog/cross-browser-testing-using-selenium/)时，它会有所帮助，因为用户需要查看执行报告
*   如果你在一个无头浏览器上工作，跟踪执行会变得容易得多。
*   失败的测试的屏幕截图也可以很容易地捕捉到。

现在，让我们继续前进，学习如何在测试应用程序时获取屏幕截图。

**Selenium web driver 中的截图:如何在 Selenium 中截图？**

为了在 Selenium 中捕获屏幕截图，我们可以使用一个名为 **TakesScreenshot 的接口。**这个方法 i 指示驱动程序，它可以捕获屏幕截图并以不同的方式存储。

语法:

```
 File file = ((TakesScreenshot) driver).getScreenshotAs(OutputType.FILE);
String screenshotBase64 = ((TakesScreenshot) driver).getScreenshotAs(OutputType.BASE64); 
```

其中 *OutputType* 定义了截图的输出类型。

为了捕获截图并将其存储在特定的位置，有一种方法叫做“ **getScreenshotAs**

我们来详细了解一下这个

对于 WebDriver 扩展的 **TakesScreenshot** 方法，这将根据浏览器尽最大努力以更好的顺序返回以下内容:

*   整个页面
*   当前窗口
*   当前帧的可见部分
*   包含浏览器的整个显示屏的屏幕截图
*   HTML 元素的全部内容–HTML 元素的可见部分

语法:

```
  X getScreenshotAs(OutputType(X). target)  throws WebDriverException 
```

在哪里

*   X 是方法的返回类型
*   Target 保存目的地址
*   如果底层实现不支持截图，抛出[*web driver exception*](https://www.edureka.co/blog/exceptions-in-selenium/)。

### **测试用例失败**

[*Selenium web driver*](https://www.edureka.co/blog/what-is-selenium/)推出了一些很棒的新功能，让测试应用程序变得更加容易。这是因为 [*WebDriver 架构*](https://www.edureka.co/blog/selenium-webdriver-architecture/) 允许 Javascript 沙箱之外的交互。一个新的有用的功能是能够从网络驱动中截图。

您可以在测试的任何阶段截图，但大多数情况下，它是在测试**失败**时使用的，截图有助于分析，因此我们可以看到在测试失败期间出了什么问题。这可以通过使用 [*TestNG 注释来完成。*](https://www.edureka.co/blog/testng-annotations-in-selenium/)

为此，首先，我需要

*   创建一个类然后实现TestNG '*ITestListener**'*。
*   然后调用一个方法*【onTestFailure】*。
*   用这个方法添加代码截图。
*   

现在，问题是如何使用 TestNG 获得 TestListeners 类中的驱动程序对象？

我会帮助你理解做到这一点是多么容易。

To take a screenshot in Selenium, we need to to have a driver object. Get the driver from the ITestContext which has to be set in the base setup where it is easy to create our driver instance.Hope you guys are clear with this. Moving ahead, we’ll take a look at the demo where I will help you understand how simple it is to take a screenshot in Selenium.

我将在这里解释两个不同的程序，以便你对如何在 Selenium 中截屏有一个正确的概念。

第一个程序处理如何捕获测试用例成功运行的屏幕截图。第二个程序帮助你理解如何在测试失败时截图。

**Selenium web driver 中的截图:** **演示**

当您想要测试一个 web 应用程序时，首先要做的就是准备好 Selenium Jar 文件和 Java 库。您可以选择自己喜欢的 IDE。我更喜欢在 Eclipse IDE 上工作，因为它对用户友好。

*   我将浏览器驱动设置为 [*ChromeDriver* 。](https://www.edureka.co/blog/selenium-chromedriver-and-geckodriver/)
*   用 ChromeDriver 实例化驱动程序实例。
*   获取网页的 URL。
*   执行相应的操作。

在这种情况下，我将截图我们的官方网页[*Edureka.co。*](https://www.edureka.co/)

请参考以下代码:

```

import java.io.File;
import java.io.IOException;

import org.apache.commons.io.FileUtils;
import org.openqa.selenium.OutputType;
import org.openqa.selenium.TakesScreenshot;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;

public class Screen {

public static void main(String[] args) throws Exception {
System.setProperty("webdriver.chrome.driver", "C:UsersNeha_VaidyaDesktopchromedriver_win32chromedriver.exe");
WebDriver driver = new ChromeDriver();
driver.get("http://www.edureka.co/");
TakesScreenshot ts = (TakesScreenshot)driver;
File source = ts.getScreenshotAs(OutputType.FILE);
FileUtils.copyFile(source, new File("./Screenshots/Screen.png"));
System.out.println("the Screenshot is taken");
driver.quit();
}

}

```

上述代码的输出如下所示:

![ScreenOutput - How to take screenshot in Selenium - Edureka](img/26361eb4b974f7de9842df09a0700d73.png)

该文件夹包含图像

![Screenshot - How to take screenshot in Selenium - Edureka](img/9b5bab2044d3f22a5d86c53be74800bd.png)

现在，让我们来了解一下如何截图测试失败

*   首先， [*创建一个 Maven 项目。*](https://www.edureka.co/blog/create-selenium-maven-project/)
*   添加 TestNG XML 文件。
*   添加 maven 依赖项。
*   创建一个包含 WebDriver 实例的基类。
*   定义两个函数，即初始化()和失败()
*   在继承基类的另一个类 **demo** 中调用这两个函数。
*   这个演示类包含两个方法 setUp()调用 initialization()函数，tearDown()帮助关闭驱动程序，ScreenshotTest()断言实际和预期的输出。
*   在这种情况下，我将断言 true 和 false，这将导致测试用例失败。
*   创建另一个类 ListenersClass，帮助 WebDriver 监听特定事件。
*   将这段代码添加到主函数之前的演示类@ Listeners(Listeners class . class)中，以便监听测试用例。

你可以参考这个代码:

BaseClass

```

package com.edureka;
import java.io.File;
import java.io.IOException;
import org.apache.commons.io.FileUtils;
import org.openqa.selenium.OutputType;
import org.openqa.selenium.TakesScreenshot;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.testng.annotations.Listeners;

public class BaseClass {
public static WebDriver driver;

public static void initialization()
{
System.setProperty("webdriver.chrome.driver", "C:UsersNeha_VaidyaDesktopchromedriver_win32chromedriver.exe");
driver = new ChromeDriver();
driver.get("http://www.edureka.co/");

}
public void failed()
{
File srcFile = ((TakesScreenshot)driver).getScreenshotAs(OutputType.FILE);
try {
FileUtils.copyFile(srcFile, new File("/C:/Users/Neha_Vaidya/eclipse-workspace/Screens/"
+ "ScreenshotsTaken/tests.jpg"));
} catch (IOException e) {
e.printStackTrace();
}
}

}

```

民主阶级

```

package com.edureka;
import org.testng.Assert;
import org.testng.annotations.AfterMethod;
import org.testng.annotations.BeforeMethod;
import org.testng.annotations.Listeners;
import org.testng.annotations.Test;
@Listeners(ListenersClass.class)
public class demo extends BaseClass{
@BeforeMethod
public void setUp() {
initialization();

}

@AfterMethod
public void tearDown()
{
driver.quit();
}

@Test
public void takeScreenshotTest()
{
Assert.assertEquals(true, false);
}
}

```

听众班级

```

package com.edureka;
import org.testng.ITestContext;
import org.testng.ITestListener;
import org.testng.ITestResult;

public class ListenersClass extends BaseClass implements ITestListener{

public void onTestStart(ITestResult result) {
// TODO Auto-generated method stub

}

public void onTestSuccess(ITestResult result) {
// TODO Auto-generated method stub

}

public void onTestFailure(ITestResult result) {
System.out.println("Failed Test");
failed();

}

public void onTestSkipped(ITestResult result) {
// TODO Auto-generated method stub

}

public void onTestFailedButWithinSuccessPercentage(ITestResult result) {
// TODO Auto-generated method stub

}

public void onStart(ITestContext context) {
// TODO Auto-generated method stub

}

public void onFinish(ITestContext context) {
// TODO Auto-generated method stub

}

}

```

输出以这种方式描述:

![TestFailedScreenshot - How to take screenshot in Selenium - Edureka](img/d58da18bb3218a183bed11f9e48b367a.png)

![ScreenShot1- How to take screenshot in Selenium - Edureka](img/03d425d747f747f75bfc4385d08329eb.png)

*With this, we come to an end to this “How to take a screenshot in Selenium WebDriver” blog. I hope you guys enjoyed this article and understood how to run a test case. Got a question for us? Please mention it in the comments section of “How to take a screenshot in Selenium WebDriver” and we will get back to you.**If you wish to learn more about Selenium WebDriver and build a career in the same, then check out our [Selenium Certification Course](https://www.edureka.co/selenium-certification-training) which comes with instructor-led live training and real-life project experience. This training will help you understand Selenium Testing in depth and help you achieve mastery over the subject.*