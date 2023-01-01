# 如何从 Selenium WebDriver 的下拉列表中选择一个值

> 原文：<https://www.edureka.co/blog/selenium-select-class/>

执行任何动作，第一个 要做的任务是识别元素组。通常，在使用 Selenium 时，您可能需要从下拉列表中选择一些值，还需要执行其他活动并验证它们。因此，我将指导您理解什么是 Selenium WebDriver 中的选择类，以及如何**从 Selenium WebDriver 的下拉列表中选择**一个值。更多详情，您可以报名参加[硒培训](https://www.edureka.co/selenium-certification-training)。

我将按以下顺序讨论这个话题:

*   [在 Selenium WebDriver 中选择类](#Select_class_in_Selenium)
*   [不同的选择命令](#Different_Select_commands)
*   [多重选择命令是如何工作的？](#How_does_Multiple_SELECT_command_work?)
*   [取消选择方法](#DeSelect_Methods)
*   [如何从下拉菜单中选择一个选项？](#How_to_select_an_option_from_the_drop-down_menu?)

那么，让我们开始吧。

## **在 Selenium WebDriver 中选择类**

***选择*** 类是一个 [*Webdriver*](https://www.edureka.co/blog/selenium-webdriver-architecture/) 类，基本上提供了 HTML 选择标签的实现。Select 标记为 helper 方法提供了选择和取消选择选项。这个类可以在 **Selenium 的支持下找到。UI .选择**包。Select 实际上是一个普通的类，所以它的对象也是由关键字 *New* 创建的，也指定了 web 元素的位置。

**语法:**

```
Select oSelect = new Select();
```

它将抛出一个错误，要求向命令添加参数。所以使用 [*元素定位器*](https://www.edureka.co/blog/locators-in-selenium/) *指定 web 元素位置。*

它清楚地说明了 *Select* 正在为它的构造函数请求一个元素类型对象。

之后，一旦你得到了 *选择类* 的对象，你就可以通过键入***oSelect+dot***来访问驻留在 *选择* 类中的所有方法，这将提供选择类下的所有方法。根据您的测试用例选择任何方法。

所以，现在让我们继续学习这个 Select 类下的不同方法。

## **Selenium web driver 中的选择类:** **不同的选择命令**

下面是处理下拉列表最常用的方法。

1.**selectByVisibleText:***selectByVisibleText(String arg 0):void*

使用这种方法，在任何下拉框和多选框中选择一个选项都非常容易。它接受一个字符串参数，该参数是选择元素 的*值* *之一，它不返回任何值。*

**语法:****oselect . selectbyvisibletext(" text ")；**

**举例:**

```
Select oSelect =new Select(driver.findElement(By.id("search-box")));
oSelect.selectByVisibleText("Blog");
```

2 **。selectbyindex:*selectbyindex(int arg 0):参见***

这个方法几乎类似于“selectByVisibleText ”,但唯一的区别是用户必须提供选项的索引号，而不是选项文本。它接受整数参数，该参数是 *选择元素* 的索引值，它不返回任何值。

**synaptic tx:**oseselect by index(int)；

**举例:**

```
Select oSelect = new Select(driver.findElement(By.id("Seacrch-box")));
oSelect.selectByIndex(2);

```

3.**select by value:*selectbyvalue(字符串 arg0):参见***

这种方法与我之前讨论过的方法类似，唯一的区别是它要求期权的价值，而不是期权文本或指数。它接受一个字符串参数，该参数是选择元素的值之一，它不返回任何内容。

**语法:****oselect . selectby value(" text ")；**

**举例:**

```
Select oSelect = new Select(driver.findElement(By.id("Search-box")));

oSelect.selectByValue("Selenium Certification training");

```

4.**getOptions:*:getOptions():List<web element>***

这个方法有助于获取属于 Select 标签的所有选项。它不带参数，返回 *列表< WebElements >* 。

**语法:****oselect . get options()；**

**举例:**

```
Select oSelect = new Select(driver.findElement(By.id("Search-box")));
List <WebElement> elementCount = oSelect.getOptions();
System.out.println(elementCount.size());
```

那么，让我们进入下一个主题，了解多项选择方法

## **Selenium web driver 中的选择类:** **多重选择命令是如何工作的？**

多重选择属性是一个布尔表达式。当它存在时，它指定可以一次选择多个选项。这些选项因不同的操作系统和浏览器而异，即:

*   **对于 Windows:** 按住 control (ctrl)按钮选择多个选项。
*   **对于 Mac:** 按住命令按钮选择多个选项。

使用复选框而不是使用不同的执行操作的方式是用户友好的，因为您必须通知用户有多个选项可用。有一种方法实际上有助于指定您可以使用多个选择选项。

### **isMultiple**

***is multiple():boolean*–**该方法告知 SELECT 元素是否同时支持多个选择选项。该方法不接受任何内容，但返回一个布尔值(真/假)。

**语法:***oselect . is multiple()；*

**举例:**

```
Select oSelect = new Select(driver.findElement(By.id(Element_ID)));
oSelect.selectByIndex(index)
oSelect.selectByIndex(index)
// Or can be used as
oSelect.selectByVisibleText(text)
oSelect.selectByVisibleText(text)
// Or can be used as
oSelect.selectByValue(value)
oSelect.selectByValue(value)

```

## **选择 Selenium WebDriver 中的类:取消选择方法**

当您选择网页上的特定元素时，有几种方法可以帮助您取消选择该元素。但是这些方法中唯一的挑战是它们不能用于，只能用于  *多选* 元素。

如果您想要取消选择任何预先选择的选项，可以使用  来完成

*   取消全选()
*   取消选择索引
*   取消选择值
*   deselectByVisibletext

让我们详细了解一下方法。

*   **deselectAll():** 清除所有选中的条目。这仅在下拉元素支持多重选择时有效。

**举例:** oSelect。*deselectAll()*；

*   **deselectByIndex():** 它在给定的索引处取消选择选项。

**举例:** oSelect。*deselectByIndex②；*

*   **deselectByValue():** 该方法帮助取消选择其“*值*属性与特定参数匹配的选项。

**举例:** oSelect。*deselectByValue(" 13 ")；*

*   **deselectByVisibletext():**该方法帮助取消选择显示匹配参数的文本的选项。

**Selenium web driver 中选择类:如何从下拉菜单中选择一个选项？**

我将通过一个实时例子来帮助你们理解这个 *Select* 方法是如何工作的。

在这种情况下，我会考虑在著名的电子商务网站*facebook.com 工作。*

*   首先，将 Java 库添加到系统中。
*   您可以在其中编写代码的 IDE。我会考虑在 Eclipse IDE 上工作，因为它对用户友好。
*   在项目中添加 Selenium 库。
*   获取网页的 URL。
*   在下拉列表中执行所需的操作。

我已经用两个不同的程序解释了这一点。第一个程序将帮助您从下拉列表中选择一个值，第二个程序帮助您对下拉列表执行不同的操作。

*   首先设置 [*浏览器驱动*](https://www.edureka.co/blog/selenium-chromedriver-and-geckodriver/) 。
*   得到[](http://www.facebook.com/)的网址。
*   创建一个 [*WebElement*](https://www.edureka.co/blog/webelement-in-selenium/) 对象，使用元素定位器找到元素。
*   使用 Select 方法选择 WebElement 的对象。
*   退出驱动程序执行。

请参考以下代码:

```

package Edurekaa;

import org.junit.Test;
import org.openqa.selenium.By;
import org.openqa.selenium.JavascriptExecutor;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.Select;

public class SelectClass {
@Test
public static void main(String[] args) throws InterruptedException {
System.setProperty("webdriver.chrome.driver", "C:UsersVaishnaviDesktopchromedriver_win32 (2)chromedriver.exe");
WebDriver driver = new ChromeDriver();
driver.get("http://www.facebook.com");
driver.manage().window().maximize();
//js.executeScript("window.scrollBy(0,300)");
WebElement month_dropdown = driver.findElement(By.id("day"));
Select oSelect = new Select(month_dropdown);
oSelect.selectByIndex(3);
Thread.sleep(3000);
WebElement year_yy = driver.findElement(By.id("year"));
Select year_y = new Select(year_yy);
year_y.selectByValue("2000");
Thread.sleep(3000);
WebElement month_m = driver.findElement(By.id("month"));
Select month_d1 = new Select(month_m);
month_d1.selectByVisibleText("Jul");
driver.quit();

}

}

```

第二个程序处理在下拉列表上执行动作。在这种情况下，让我们打印月数和姓名。

*   创建一个 WebElements 列表并选择选项。
*   获取月份大小下拉列表。
*   打印月清单的大小。
*   创建 WebElement *ele* 的另一个对象，并获取月份名称。
*   使用 for 循环打印数字。
*   退出驱动程序执行。

```

package Edurekaa;

import java.util.List;

import org.junit.Test;
import org.openqa.selenium.By;
import org.openqa.selenium.JavascriptExecutor;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.Select;

public class SelectClass2 {
@Test
public static void main(String[] args) throws InterruptedException {
System.setProperty("webdriver.chrome.driver", "C:UsersVaishnaviDesktopchromedriver_win32 (2)chromedriver.exe");
WebDriver driver = new ChromeDriver();
JavascriptExecutor js = (JavascriptExecutor)driver;
driver.get("http://www.facebook.com");
driver.manage().window().maximize();
//js.executeScript("window.scrollBy(0,300)");
WebElement month_dropdown = driver.findElement(By.id("month"));
Select oSelect = new Select(month_dropdown);
List&amp;amp;lt;WebElement&amp;amp;gt; month_list = oSelect.getOptions();
int total_month = month_list.size();
System.out.println("Total count is "+total_month);
for(WebElement ele:month_list)
{
String month_name = ele.getText();
System.out.println("Months are"+month_name);
}

driver.quit();

}

}

```

至此，我们结束了这篇“如何在 Selenium WebDriver 中从下拉列表中进行选择”的博客。我希望你们喜欢这篇文章，并且理解 Selenium 中的 Select class 是如何工作的。

现在您已经了解了如何使用 Selenium 从下拉列表中选择一个值，请查看 Edureka 的Selenium 认证课程，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 650，000 名满意的学习者。本课程旨在向您介绍完整的 Selenium 特性及其在软件测试中的重要性。

有问题要问我们吗？请在“如何在 Selenium WebDriver 中从下拉列表中选择”的评论部分提到它，我们会回复您。