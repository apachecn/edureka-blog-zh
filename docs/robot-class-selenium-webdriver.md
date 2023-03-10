# 关于 Selenium WebDriver 中的机器人类，您需要知道的全部内容

> 原文：<https://www.edureka.co/blog/robot-class-selenium-webdriver/>

机器人帮助管理所有活动，如在指定时间内执行任务、处理鼠标功能和键盘功能等等。这篇关于 Selenium 中的 ***机器人类的文章讨论了在使用 Selenium 测试应用程序时帮助控制鼠标和键盘的某些功能。有了[硒认证](https://www.edureka.co/selenium-certification-training)可以了解更多。***

*“Robots will play an important role in providing physical assistance and even companionship for the elderly” – BIll Gates*

**以下是我们将在本文中涉及的主题**

***   [什么是机器人类？](#What_is_a_Robot_class?)*   [机器人类的重要性](#Importance_of_Robot_class)*   [实现这个类的方法](#Methods_to_implement_the_robot_class)*   [如何在 Selenium 中实现机器人类？](#How_to_implement_the_Robot_class_in_Selenium?)*   [局限性](#Limitations)**

**那么，就从我们的第一个话题开始，*什么是机器人类？***

## ****什么是机器人类？****

**在测试应用程序时，时间扮演着重要的角色，我们需要确保在特定的时间内完成预期的任务。**

**[***Selenium***](https://www.edureka.co/blog/what-is-selenium/)中的*机器人类*用于为测试自动化、自运行演示和其他需要控制鼠标和键盘的应用程序生成本地系统输入事件。[***web driver***](https://www.edureka.co/blog/selenium-webdriver-architecture/)无法处理 OS 弹出窗口，所以在 Java 1.3 中，引入了 Robot 类。**

**这个机器人类的主要目的是方便 Java 平台实现的自动化测试[](https://www.edureka.co/blog/selenium-tutorial)。简单地说，我认为这个类提供了对鼠标和键盘设备的控制。**

**这很容易实现，因为它可以很容易地与当前自动化框架集成**

**现在，让我们了解一下这门课的重要性**

## ****机器人类的重要性****

***   当我们使用机器人类时，上传文件很容易*   可以模拟和处理鼠标和键盘功能*   它也可以处理弹出窗口**

**让我们进入下一个话题，了解实现机器人类的不同方法。**

## ****方法实现机器人类****

**为了实现 Robot 类，我们需要一些方法来帮助轻松执行测试脚本。我们有:**

***   键压()键压*   KeyRelease()*   MouseMove()*   MousePress()*   MouseRelease()**

**我们还使用了*键事件*，它是一个独立的类，负责击键**

**让我们详细了解一下他们每一个人**

***   **KeyPress()** :当你想按任意键时调用该方法**

**Ex: robot.keyPress(按键事件*)。VK _ UP*)；**

**这将按下键盘上的向上键**

***   **KeyRelease()** :该方法用于释放键盘上被按下的键**

**Ex:robot . key release(key event*)。VK _ 大写 _ 锁定*)；**

**这将释放键盘上按下的 capslock 键**

***   **MouseMove()** :当你想在 X 和 Y 坐标上移动鼠标指针时调用这个方法**

**Ex:robot . mousemove(coordinates . get . x()、coordinates . get . y())；**

**当你想在 X 和 Y 坐标上移动鼠标时，这个方法被调用**

***   **MousePress()** :用于按鼠标左键**

**Ex:robot . mouse press(input event。button 1 _ MASK)；**

**帮助按下鼠标键**

***   **MouseRelease()** :该方法帮助释放鼠标被按下的按钮**

**Ex:robot . mouse release(input event。BUTTON3_DOWN_MASK)**

**该方法用于释放鼠标右键**

**现在，让我们试着实现这个机器人类**

## ****如何在硒中实现机器人类****

**我们将尝试网页自动化*edureka.co*释放他们的互动方式**

****第一步:**将各自的浏览器驱动链接到[***chrome driver***](https://www.edureka.co/blog/selenium-chromedriver-and-geckodriver/)并指定路径**

****第二步:**获取对应网页的网址，导航时出现 O.S 弹出框。**

****第三步:**使用 [***元素定位器***](https://www.edureka.co/blog/locators-in-selenium/) 找到网页上的元素**

****第四步:**我们使用 Robot 类来处理弹出窗口，使用这个我们在代码中创建一个 Robot 类的实例，比如 **Robot robot = new Robot()** 。机器人类存在于 JDK 的 AWT 包中。**

***   为了按下键盘上的向下箭头键，我们使用( **robot.keyPress(KeyEvent。VK _ DOWN))；***   为了按下键盘的 TAB 键，我们使用( **robot.keyPress(KeyEvent。VK _ TAB))；***   为了按回车键，我们使用( **robot.keyPress(KeyEvent。VK _ ENTER))；****

**为了执行鼠标动作，我们使用了**

****第一步:** *MouseMove()* 方法以 X 和 Y 坐标为参数 *robot.mouseMove(640，360)* 其中 640 表示 X 轴，360 表示 Y 轴。所以，这个方法会将鼠标指针从当前位置移动到 X 和 Y 的交点。**

****第二步:**我们需要按下鼠标键。我们将使用 *mousePress* 方法。按钮 1 _ 向下 _ 遮罩)。**

****第三步:**按键按下后，需要松开鼠标键。我们将使用 *MouseRelease()* 来做这件事。robot.mouseRelease(InputEvent。这有助于释放鼠标左键。**

```
 **import java.awt.AWTException;
import java.awt.Robot;
import java.awt.event.KeyEvent;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;

public class DemoClass {

public static void main(String[] args) throws AWTException, InterruptedException {
System.setProperty("webdriver.chrome.driver", "C:UsersNeha_VaidyaDesktopchromedriver_win32chromedriver.exe");
WebDriver driver = new ChromeDriver();
driver.get("http://www.edureka.co");
driver.manage().window().maximize();
driver.findElement(By.linkText("Courses")).click();
Robot robot = new Robot();
Thread.sleep(4000);
robot.keyPress(KeyEvent.VK_DOWN);
Thread.sleep(4000);
robot.keyPress(KeyEvent.VK_TAB);
Thread.sleep(4000);
System.out.println("a");
robot.keyPress(KeyEvent.VK_TAB);
Thread.sleep(4000);
System.out.println("b");
robot.keyPress(KeyEvent.VK_TAB);
Thread.sleep(4000);
System.out.println("c");
robot.mouseMove(30,100);
Thread.sleep(4000);
System.out.println("d");
driver.quit();

}

}** 
```

```
**Now. let us have a look at the output of this program**
```

**它首先获取网页的 URL*edureka.co***

**![Output - Robot class in Selenium - Edureka](img/6f011e13f12e2351cafb5099710c077c.png)**

**接下来，它使用链接文本导航到下一页*edureka.co/all-courses***

**![Courses - Robot class in Selenium - Edureka](img/81fe2711278a09e0e8c9f66e3dfa6794.png)**

**按下键盘上的 TAB 键**

**![Tab function - Edureka](img/50a23a6c2cee0cb7ea88b5936c8e5ed1.png)**

**一旦完成，我们将执行鼠标上的动作**

**![MouseMove - Edureka](img/a4ff0a1893f937ec03d000f864515454.png)**

**此外，请查看机器人课堂上的视频，其中专家对其进行了详细的解释**

## ****Selenium web driver 中的机器人类| Selenium 中处理键盘事件****

****

**[//www.youtube.com/embed/iK1MMPQ7z8s?rel=0&showinfo=0](//www.youtube.com/embed/iK1MMPQ7z8s?rel=0&showinfo=0)**

**本视频将帮助您了解如何使用简单的方法实现键盘和鼠标功能的自动化。**

**现在，我们来看看这个机器人类有什么局限性**

## ****机器人类的局限性****

***   鼠标或键盘事件将只作用于当前窗口的实例*   很难在不同的框架或窗口之间切换*   像 MouseMove()这样的方法依赖于屏幕分辨率，所以代码有可能无法在其他机器上运行。*   在执行机器人事件时，如果代码执行被移动到另一个窗口，鼠标或键盘事件仍将保留在前一个窗口。**

**说到这里，我们就到了“*硒中机器人课堂”博客的尾声。我希望你们喜欢这篇文章，并且理解什么是 Selenium 中的机器人类。现在您已经了解了机器人类如何处理鼠标和键盘功能，请查看 Edureka 的 **[Selenium 认证课程](https://www.edureka.co/selenium-certification-training)** ，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 650，000 多名满意的学习者。本课程旨在向您介绍完整的 Selenium 特性及其在软件测试中的重要性。***

***有问题吗？请在“Selenium 中的机器人课程”的评论部分提到它，我们将会回复您，或者今天就加入我们在英国的的 [Selenium 培训。](https://www.edureka.co/selenium-certification-training-uk)***