# 什么是依赖注入？–知道如何实现依赖注入

> 原文：<https://www.edureka.co/blog/what-is-dependency-injection/>

在一个我们每天都在使用编程语言的世界里，我们所有人都倾向于寻找方法和技巧来使我们的生活变得简单。依赖注入就是这样一种技术，它旨在通过提供对另一个对象的依赖来帮助开发人员轻松编码。在这篇关于什么是依赖注入的文章中，我将帮助您详细理解这项技术。

本文将涵盖以下主题:

*   [依赖注入简介](#IntroductionToDependencyInjection)
*   [控制反转](#InversionofControl)
*   [依赖注入的类型](#TypesofDependencyInjection)
*   [依赖注入的好处](#BenefitsofDependencyInjection)
*   [使用 Spring Boot 实现依赖注入](#ImplementDIusingSpring%20Boot)

那么，就从这篇文章开始吧。

## **什么是依赖注入？**

依赖注入是一个对象提供另一个对象的依赖的能力。

现在，我很确定，你可能不理解上面的技术定义。所以，让我为你澄清困惑。

当你听到依赖这个词时，你会想到什么？

很明显，有些东西依赖于其他东西的支持，对吗？

嗯，这是相同的，在编程的情况下也是如此。

编程中的依赖是一种方法，其中一个类使用另一个类的特定功能。因此，举例来说，如果您考虑两个类 A 和 B，并且假设类 A 使用类 B 的功能，那么这意味着类 A 具有对类 B 的依赖性。现在，如果您正在用 Java 编写代码，那么您必须知道，您必须在类 A 使用对象之前创建类 B 的实例。

**![Types of Classes - What is Dependency Injection - Edureka](img/4a8c7966a8d5d10c516980289171f750.png)**

因此，如果我现在必须为您定义依赖注入，那么为其他某个类创建一个对象并让该类直接使用依赖的过程就称为依赖注入。它主要涉及三类:

*   **客户端类:**这是依赖类，依赖于服务类。

*   **服务类:**这个类为客户端类提供服务。

*   **注入器类:**这个类负责将服务类对象注入到客户端类中

现在，您已经理解了什么是依赖注入，接下来让我带您了解依赖注入所基于的原则。

## **控制反转**

正如我上面提到的，控制反转是依赖注入的一个原则。此外，顾名思义，控制反转基本上是用来反转一个类的不同种类的附加责任，而不是主要责任。

如果我必须用更简单的术语来解释你，那就考虑一个例子，你有烹饪的能力。根据国际奥委会的原则，你可以颠倒控制，所以你可以直接从外面订购，而不是烹饪食物，你可以在家门口收到食物。因此，食物送到你家门口的过程被称为控制倒置。

你不必自己做饭，相反，你可以点餐，让送餐员为你送餐。这样，你就不必顾及额外的责任，只需专注于主要工作。

现在，您已经知道了依赖注入背后的原理，让我带您了解一下依赖注入的类型。

## **依赖注入的类型**

依赖注入主要有三种类型:

*   **构造器注入:**在这种类型的注入中，注入器通过客户端类构造器提供依赖。

*   **Setter 注入/属性注入:**在这种类型的注入中，注入器方法将依赖注入到客户端公开的 Setter 方法中。

*   **接口注入:**在这种类型的注入中，注入器使用接口来提供对客户端类的依赖。客户端必须实现一个接口，该接口将公开一个接受依赖关系的设置器方法 。

到目前为止，我希望您已经理解了这样一个事实，即依赖注入负责创建对象，理解哪些类需要这些对象，并最终为这些类提供对象。因此，在这一点上，让我们接下来看看依赖注入的好处。

## **依赖注入的好处**

在我列出依赖注入的好处之前，让我向您解释一下在行业层面上进行这种注入的必要性，以帮助您更好地理解这些好处。

考虑一个场景，其中有一个电子邮件类，它的唯一职责是处理收到的电子邮件。现在，这个类将拥有诸如“收件人电子邮件地址”、“发件人电子邮件地址”、“电子邮件的主题和正文”等对象。

现在，如果公司想要保存文本和音频消息，您认为这个类可以保存消息吗？

嗯，答案是否定的？

这是因为，Email 类不能处理文本和音频消息的参数。在这种情况下，您必须重新创建该类。现在，重新创建类是一件相当麻烦的工作，尤其是如果您必须定期这么做的话。相反，如果您使用依赖注入，您可以在运行时更改对象。所以，用这种方法，你不需要重新创建类，这在很多方面对你有帮助。

所以，如果我必须总结依赖注入的好处，那么下面就是这些好处:

![Benefits of Dependency Injection - Dependency Injection - Edureka](img/51079810f48a6f7794f1b5fa815ced8b.png)

好了，现在你知道了依赖注入的好处，让我们向前看，看看如何使用 Spring Boot 实现依赖注入。

## 如何使用 Spring Boot 实现 DI？

**步骤 1:** 打开您的 **Eclipse IDE** ，通过右键单击并选择 **Spring Starter 项目**来创建一个 **Spring Boot 应用程序**。然后提及项目名称，点击**完成**。

![Spring Starter Project - What is Dependency Injection - Edureka](img/a90121efe3bec3e77433adde39c9e383.png)

要获得 Spring Starter 项目，您必须从 Eclipse Marketplace 安装 Spring Tool Suite。万一你没有安装 Spring Too Suite，可以参考我的文章[安装 Spring 工具套件](https://www.edureka.co/blog/spring-boot-setup-helloworld-microservices-example/#InstallSpringToolSuite(STS)inEclipse)。

您将自动看到一个应用程序文件创建如下。

**![Application File - What is Dependency Injection - Edureka](img/71c2ab370f4051183c2a0a67d2c55303.png)**

**第二步:**接下来，在同一个包中创建一个类。为此，右键单击 file - >选择**类**并提及**类名。**然后点击**完成**。这将创建一个**类**文件。在这里，我创建了一个客户类。参考下文。

**![Create New Class - What is Dependency Injection - Edureka](img/932e232d2c575ad56fd97646fac1c774.png)**

第三步:之后，让我们为这个类添加一些属性。因此，假设我们包括*客户 ID、客户名称*和*课程名称。*下面提一下代码。

```
package com.example.demo; //package name

public class Customers {
private int custid;
private String custname;
private String coursename;

}

```

**步骤 3.1:** 一旦你完成了，你必须**为这些属性生成 Getter 和 Setter 方法**。为此，选择这些属性并单击右键。然后选择**源**->-**生成 Getter 和 Setter 方法。**

![Generate Getter and Setter Methods - What is Dependency Injection - Edureka](img/238563c1c6e8afa28d3b60af89036dd5.png)

到目前为止，您的代码应该如下所示:

```
package com.example.demo;

public class Customers {
private int custid;
private String custname;
private String coursename;

public int getCustid() {
return custid;
}
public void setCustid(int custid) {
this.custid = custid;
}
public String getCustname() {
return custname;
}
public void setCustname(String custname) {
this.custname = custname;
}
public String getCoursename() {
return coursename;
}
public void setCoursename(String coursename) {
this.coursename = coursename;
}
}

```

### ***现在，考虑一个场景，您必须为客户创建一个对象，但您不想手动完成。在这种情况下，您将不得不使用依赖注入，以便在您需要时获取对象。***

那么，接下来让我们看看我们如何才能做到这一点。

**第四步:**首先，将**应用类文件**中的**运行行**修改如下:

```
ConfigurableApplicationContext context = SpringApplication.run(DemoApplication.class, args);

```

**注意:如果你得到一个错误，输入如下:**

```
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.context.ConfigurableApplicationContext;

```

上面这行代码将在执行时返回一个对象。现在将下面的代码添加到应用程序文件中。

```
customers c = context.getBean(customers.class);

```

上面一行告诉编译器返回 customer 类的一个对象。参考下文。

**![Create Spring Container - What is Dependency Injection - Edureka](img/760fe6a3b5291475ec001c90fc7d34b6.png)**

**步骤 4.1:** 现在，要检查它是否工作，您**可以返回到客户类**并添加一个方法，如下所示:

```
public void display()

{

System.out.println("Object Returned Successfully");

}

```

该方法将在成功执行时显示输出“对象成功返回”。

**第 4.2 步:**接下来，您必须回到申请文件并提及以下内容:

```
c.display();

```

这样，您就可以通过引用 display 方法来调用 Customers 类的对象。到目前为止，应用程序类的代码见下图:

![Application File Code - What is Dependency Injection - Edureka](img/c3c1a0de19b2ae7d32d824689b1ecf36.png)

现在，如果您执行这个项目，您将会看到一个**异常，没有类型为**的合格 bean。*这是因为您定义的客户类不是一个 Spring Bean，即不是一个 Spring 对象。*参考下文。

**![Type of Bean Exception - What is Dependency Injection - Edureka](img/9671716f72e4c0dd487900325de79222.png)**

**步骤 4.3:** 因此，为了告诉 Spring 容器，我们需要一个 customer 类的对象。为此，您需要在 Customer 类中提到**@组件注释**。Customers 类中的代码应该如下所示:

```
package com.example.demo;

import org.springframework.stereotype.Component;
@Component
public class Customers {
private int custid;
private String custname;
private String coursename;

public int getCustid() {
return custid;
}
public void setCustid(int custid) {
this.custid = custid;
}
public String getCustname() {
return custname;
}
public void setCustname(String custname) {
this.custname = custname;
}
public String getCoursename() {
return coursename;
}
public void setCoursename(String coursename) {
this.coursename = coursename;
}
public void display()

{
System.out.println("Object Returned Successfully");

}
}

```

然后，当你提到 customers**c = context . get bean(customers . class)；**编译器将检查容器中是否有可用的客户 bean。

如果 Bean 是可用的，那么 Spring 框架会在应用程序中注入 customer 对象。所以，基本上，这个对象是由 Spring 框架创建的，可以在应用程序中进一步使用。

因此，如果我现在执行这个项目，您将看到 Object 成功返回的输出。参考下文。

***![Output - What is Dependency Injection - Edureka](img/b2e0a5e019555960113825f3e9e337f8.png)***

这就是你实现依赖注入的基本方法。

**示例:使用自动连线注释的依赖注入**

我希望你已经理解了依赖注入在 Spring Boot 是如何工作的。现在，让我们扩展这个例子，进一步看看在 Spring Boot 中一个依赖于另一个类的类是如何使用那个类的功能的。

**步骤 1:** 创建一个新的**类文件**，通过再次**右击包**并通过选择**新建- >类。**现在，在下面提到类名并点击**完成。**

接下来，让我们为这个类添加一些属性。所以，让我们说，我们包括 *TechID，Techname。*下面提一下代码。

```
package com.example.demo;
public class Technologies {
private int techid;
private String techname;
}

```

**步骤 2.1:** 一旦你完成了这些，右键点击文件，为这些属性生成 **Getter 和 Setter 方法**，然后选择 **Source - > Generate Getter 和 Setter 方法。**

**步骤 3:** 现在，让我们说，我们必须创建一个打印“**成功**”的方法。为此，请提及代码:

```
public void tech()
{
System.out.println(" Successful");
}

```

到目前为止，您的代码应该如下所示:

```
package com.example.demo;

public class Technologies {
private int techid;
private String techname;
public int getTechid() {
return techid;
}
public void setTechid(int techid) {
this.techid = techid;
}
public String getTechname() {
return techname;
}
public void setTechname(String techname) {
this.techname = techname;
}
public void tech()

{

System.out.println(" Successful");

}
}

```

**步骤 4:** 现在，要调用**客户类**中的**技术()方法**，您必须创建一个技术类的对象。因此，在 customers 类中提到下面一行代码:

```
private Technologies techdetail;

```

**![Private Method - What is Dependency Injection - Edureka](img/ddf3b3c872058e3154bcce17cdac6e64.png)**

**步骤 4.1:** 一旦完成，通过**右击文件**，然后选择**源- >生成 Getter 和 Setter 方法，为这些属性生成 **Getter 和 Setter 方法**。**

**第五步:**接下来要使用 **tech()方法**，就不得不提一下**tech detail . tech()；**客户类别的**显示方式下。此外，为了确保 techdetail 对象被实例化，请提及**@组件注释**是**技术类。**参考下文。**

现在，当你执行这个项目时，你会看到一个**空指针异常**。这是因为现在 ***客户类依赖于技术类，但是它不知道技术类*** 的存在。

*![Exception - What is Dependency Injection - Edureka](img/253dfadcf80e3fb9c3fadc38598dcb2a.png)*

*因此，为了使客户能够识别技术类，您必须在客户类中插入**@自动连线注释**。客户类的最终代码应该如下:*

```

package com.example.demo;

import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Component;
@Component
public class Customers {
private int custid;
private String custname;
private String coursename;
@Autowired
private Technologies techdetail;

public Technologies getTechdetail() {
return techdetail;
}
public void setTechdetail(Technologies techdetail) {
this.techdetail = techdetail;
}
public int getCustid() {
return custid;
}
public void setCustid(int custid) {
this.custid = custid;
}
public String getCustname() {
return custname;
}
public void setCustname(String custname) {
this.custname = custname;
}
public String getCoursename() {
return coursename;
}
public void setCoursename(String coursename) {
this.coursename = coursename;
}
public void display()

{

System.out.println("Object Returned Successfully");
techdetail.tech();

}
}

```

一旦您执行了这些文件，您将看到 Object 成功返回的输出，这意味着我们已经完成了对类的依赖。参考下文。

**![Object Returned - What is Dependency Injection - Edureka](img/66cd795d4f91de836da6eb75f363f968.png)**

*既然你已经完成了这篇文章，那就来看看 Edureka 的 [**Spring 框架认证培训**](https://www.edureka.co/spring-framework) 吧，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。*

*有问题吗？请在这篇《什么是依赖注入？*“文章*我们会尽快给你回复。*