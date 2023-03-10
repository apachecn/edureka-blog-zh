# 知道如何在 TestNG–TestNG 参数化中使用 DataProvider

> 原文：<https://www.edureka.co/blog/dataprovider-in-testng/>

[硒](https://www.edureka.co/blog/selenium-tutorial)是用来让事情变得更简单快捷的。但是如果测试用例必须手工提供，那么 **[自动化测试](https://www.edureka.co/testing-with-selenium-webdriver)** 又有什么意义呢？为了加速测试过程，测试用例必须自动化。这就是 DataProviders 适合的地方。 [TestNG](https://www.edureka.co/blog/selenium-webdriver-tutorial) 中的 DataProvider 用于自动化提供测试用例的过程，这也是我将在本文中讨论的内容。

我将在本文中讨论以下主题:

*   [什么是数据驱动框架？](#WhatisDataDrivenFramework?)
*   [测试中的参数化类型](#TypesofParameterizationinTestNG)
*   [TestNG 中的 DataProvider 是什么？](#WhatisDataProviderinTestNG?)
*   [使用 DataProvider 进行参数化](#ParameterizationusingDataProvider)
*   [数据提供者示例](#DataProviderExamples)

## **什么是数据驱动框架？**

数据驱动是一个[测试自动化框架](https://www.edureka.co/blog/test-automation-frameworks/)，它以表格或电子表格的形式存储测试数据。它允许自动化工程师用一个单一的测试脚本来执行表中出现的所有测试数据。在这个框架中，输入值从数据文件中读取，并存储在测试脚本的变量中。数据驱动测试能够在一个测试中构建正面和负面的测试用例。

在数据驱动的测试自动化框架中，输入数据可以存储在单个或多个数据源中，比如 XLS、XML、CSV 和数据库。

## **测试中的参数化类型**

为了更好的理解参数化，我们先来了解一下 [TestNG](https://www.edureka.co/blog/testng-annotations-in-selenium/) 中的参数化选项。在 TestNG 中有两种**方式**可以实现参数化，分别是:

*   借助**参数** **标注**和 **TestNG XML** 文件

@Parameters({"name "，" searchKey"})

*   在 DataProvider 注释的帮助下

@ data provider(name = " search provider ")

现在让我们深入了解一下 TestNG 中的 DataProvider 是什么。

**TestNG 中的 DataProvider 是什么？**

如果你必须提供测试数据，那么你需要声明一个方法，以二维对象数组 ***Object[][]的形式返回数据集。**T3 第一个数组代表一个**数据集**，而第二个数组包含**参数值**。 ***DataProvider 方法*** 可以在同一个测试类或者它的一个超类中。也可以在另一个类中提供 DataProvider，但该方法必须是静态的。*

一旦你添加了这个方法，你需要用 ***@DataProvider*** 对其进行注释，让 [TestNG](https://www.edureka.co/blog/testng-annotations-in-selenium/) 知道这是一个 DataProvider 方法。您还可以使用 DataProvider 注释的 name 属性提供一个名称。如果没有提供名称，默认情况下将使用方法的名称作为参考。

现在你已经知道了什么是 TestNG 中的 DataProvider，让我们进一步了解它是如何通过参数化工作的。

## **使用 DataProvider 进行参数化**

要使用测试框架填充成千上万的 web 表单，您需要一种不同的方法，它将在单个执行流程中为您提供一个非常大的数据集。这个数据驱动的概念是通过 TestNG 中的 **@DataProvider** 注释来实现的。它只有一个**属性【名称】**。如果不指定 name 属性，那么 DataProvider 的名称将与相应的方法名称相同。这就是 DataProvider 如何简化测试多组数据的任务。现在让我们借助例子深入到 TestNG 中 DataProvider 的实际实现。

## **数据提供者示例**

**示例一:**在这个示例中，我将把 getData()方法中的数据传递给 DataProvider。我也将发送数据到 3 行和 2 列即。我将传递三个不同的用户名和密码。让我们看看下面的代码。

```
package co.edureka.pages;
import org.testng.annotations.DataProvider;
import org.testng.annotations.Test;

public class DataProviderExample{

//This test method declares that its data should be supplied by the DataProvider
// "getdata" is the function name which is passing the data
// Number of columns should match the number of input parameters
@Test(dataProvider="getData")
public void setData(String username, String password)
{
System.out.println("your username is::"+username);
System.out.println("your password is::"+password);
}

@DataProvider
public Object[][] getData()
{
//Rows - Number of times your test has to be repeated.
//Columns - Number of parameters in test data.
Object[][] data = new Object[3][2];

// 1st row
data[0][0] ="user1";
data[0][1] = "abcdef";

// 2nd row
data[1][0] ="user2";
data[1][1] = "xyz";

// 3rd row
data[2][0] ="user3";
data[2][1] = "123456";

return data;
}
}
```

当您执行上面的代码时，您传递的每个数据集都将被视为一个测试方法。由于我已经向 DataProvider 传递了三组数据，它将显示如下所示的结果:

```
![Output of DataProvider Example1 - DataProvider in TestNG - Edureka](img/620ca7cc7322faf5d219524fbf02b866.png)
```

现在，让我们再看一个例子，我将使用 DataProvider 向脸书网站提供数据。

**Example II:** In this example, I want to type username and password and login into facebook.com. This test case should run 2 times with a different set of data(data we have provided in the 2D array)

让我们实现同样的方法，并检查它是如何工作的

```
package co.edureka.pages;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.testng.annotations.DataProvider;
import org.testng.annotations.Test;

public class TestDDT {
// this will take data from dataprovider which we created
@Test(dataProvider="testdata")
public void TestFireFox(String uname,String password){
System.setProperty("webdriver.gecko.driver", "C:geckodriver-v0.23.0-win64geckodriver.exe");
WebDriver driver = new FirefoxDriver();
// Maximize browser
driver.manage().window().maximize();
// Load application
driver.get("http://www.facebook.com");
// clear email field
driver.findElement(By.id("email")).clear();
// Enter usename
driver.findElement(By.id("email")).sendKeys(uname);
// Clear password field
driver.findElement(By.id("pass")).clear();
// Enter password
driver.findElement(By.id("pass")).sendKeys(password);
}

@DataProvider(name="testdata")
public Object[][] TestDataFeed(){

// Create object array with 2 rows and 2 column- first parameter is row and second is //column
Object [][] facebookdata=new Object[2][2];

// Enter data to row 0 column 0
facebookdata[0][0]="username1@gmail.com";
// Enter data to row 0 column 1
facebookdata[0][1]="Password1";
// Enter data to row 1 column 0
facebookdata[1][0]="username2@gmail.com";
// Enter data to row 1 column 0
facebookdata[1][1]="Password2";
// return arrayobject to testscript
return facebookdata;
}
}
```

当您执行上述代码时， [Chrome 驱动程序](https://www.edureka.co/blog/selenium-chromedriver-and-geckodriver/)将启动 Google Chrome，通过导航并输入两组数据，即登录凭证。基本上，这将检查 DataProvider 是否能够成功地将数据提供给 facebook.com。如果您有 100 个和数千个数据集，那么您可以使用 excel 表来存储数据，然后在您的代码中提供 Excel 文件的路径。这将帮助您处理 excel 文件中的所有记录。

这标志着这篇关于 TestNG 中 DataProvider 的文章到此结束。我希望你们喜欢这篇文章，并且理解如何输入数据和运行测试用例。现在，如果你想对 Selenium 有更深入的了解，可以查看关于 [Selenium 教程](https://www.edureka.co/blog/selenium-tutorial)的文章。

*如果您发现“测试中的数据提供者”**相关，请查看 Edureka 提供的 ***[Selenium 认证培训](https://www.edureka.co/testing-with-selenium-webdriver)**** *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。*

有问题要问我们吗？请在 TestNG 文章中的 DataProvider 的评论部分提到它，我们会回复您。