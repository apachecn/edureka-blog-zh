# 如何最好地利用 Java 中的断言？

> 原文：<https://www.edureka.co/blog/assertions-in-java/>

本文向您介绍了 Java 中的断言，这是一个简单而重要的概念，并通过编程演示进行了后续介绍。本文将涉及以下几点:

*   [为什么需要断言？](#WhyDoYouNeedAssertions?)
*   [启用和禁用 Java 断言](#EnablingandDisablingJavaAssertions)
*   [如何使用 Java 断言？](#HowtoUseJavaAssertions?)
*   [哪里不使用断言？](#WhereNottoUseAssertion?)
*   [使用断言进行操作](#UsingAssertionsforOperations)

所以让我们开始吧，

想在你的程序中测试一个假设是否正确？嗯，你可以用 Java 中的断言语句做到这一点。您可以使用 assert 关键字创建断言，以便在程序中测试您的假设。

让我们举一个例子。ABC 公司员工的年龄不能是负数。您可以使用断言来确保雇员的年龄不是负数。

让我们再举一个例子。如果你的方法计算一个质点的速度，那么你的假设是质点的速度小于光速。因此，为了测试这个假设，可以在 Java 中使用断言语句。

**语法**

断言语句有两种形式:

```
assertexpression1;
```

这里，

表达式 1 是布尔表达式。

断言表达式 1:表达式 2；

在这种形式下，表达式 1 是一个布尔表达式，表达式 2 有一个值将与表达式 1 进行比较。

现在，你可能会问——你为你的程序选择哪种形式？当您的程序具有可能有助于诊断程序中的错误或失败的附加信息时，您可以使用第二种形式。

在 java 1.4 之前，您可以使用关键字“assert”来命名变量、方法、函数等等。对于较新版本的 JVM，这可能会导致命名冲突——所以您需要注意这个事实。

继续这篇关于 Java 断言的文章

## **为什么需要断言？**

您可能认为 Java 中的断言语句是不必要的。你可能会发现对小程序来说没有必要。但是，当涉及到具有复杂逻辑的大型程序时，这些断言语句就派上了用场。

断言语句的主要用途是用于调试和测试。如果断言语句中有任何失败，那么 JVM 将抛出一个标记为 AssertionError 的错误。如您所见，这提供了一种有效的方法来检测和纠正程序中的错误。

除了调试和测试之外，断言语句使您的代码更具可读性。让我们举一个例子:

下面的代码将帮助我们验证某些可能阻止应用程序正常工作的情况。

```
Connection conn = getConnection();
if(conn == null) {
throw new RuntimeException("Connection is null");
}

```

通过一条断言语句，您基本上可以取消“if and throw”语句，如下所示:

```
Connection conn = getConnection();
assert conn != null;

```

继续这篇关于 Java 断言的文章

## **启用和禁用 Java 断言**

因为 Java 断言使用 assert 关键字，所以不需要导入包或库。如前所述，您可以对变量、方法和函数使用 assert 关键字。为了向后兼容，也为了避免潜在的命名冲突，JVM 默认禁用断言验证。必须显式启用断言。您可以使用命令行参数(-enableassertions)或其简写(-ea)来实现这一点。

让我们考虑几个例子:

Java-ea com . bael dung . assertion . assertion

以上实现了对类的断言。

Java-ea:com . bael dung . assertion…com . bael dung . assertion . assertion

您也可以为特定的包和类启用断言。这显示在上面的例子中，我们已经为 com.baeldung.assertion 包中的类启用了断言。

现在我们已经了解了如何启用断言，让我们看看如何禁用它们。与启用断言非常相似，对于特定的包和类，可以使用命令行参数(-disable assessions)或其简写(-da)来禁用断言。

继续这篇关于 Java 断言的文章

**如何使用 Java 断言？**

在程序中实现断言需要两件事情 assert 关键字和一个布尔条件。让我们以一个代码片段为例:

```
public void setup()
{
Connection conn = getConnection();
assert conn != null;
}

```

您还可以为上述断言使用一个字符串，如下所示:

```
public void setup() 
{
Connection conn = getConnection();
assert conn != null : "Connection is null";
}

```

在上面的代码片段中，如果有 AssertionError，将使用字符串来构造错误。

在上述两种情况下，代码检查到外部源的连接是否返回非空值。如果值为 null，那么 JVM 将自动抛出 AssertionError。

在第二个示例中，当出现 AssertionError 时，我们使用的字符串出现在堆栈跟踪中。当您尝试调试程序时，这些附加信息会很有用。这些详细的消息将帮助您修复可能导致断言失败的错误。因此，当您在启用断言的情况下运行该类时，结果将类似于下面的结果:

线程“main”Java . lang . assertion 错误:com . bael dung . assertion . assertion . setup 处的连接为空(assertion . Java:15)com . bael dung . assertion . assertion . main(assertion . Java:10)

让我们考虑一个简单的例子:

```
import java.util.Scanner;
class AssertionExample
{
public static void main( String args[] )
{
Scanner scanner = new Scanner( System.in );
System.out.print("Enter your age ");
int value = scanner.nextInt();
assert value>=18:"Not valid";
System.out.println("value is "+value);
}
}

```

现在您已经有了代码，是时候运行它了。因为断言在默认情况下是禁用的，所以您必须启用它们。

您可以用以下代码编译上面的代码:javac AssertionExample.java

然后，您可以使用以下代码运行它:java -ea AssertionExample

上述代码的**输出**为:

输入您的年龄 11

线程“main”Java . lang . assertion 中出现异常错误:无效

正如你所看到的，我们给了 11 作为年龄值。该程序不将其视为合法值。因此，您将看到一个 AssertionError。

继续这篇关于 Java 断言的文章

## **哪里不使用断言？**

虽然在包含内部不变量、控制流不变量、前置条件、后置条件和类不变量的情况下使用断言是好的，但是在某些情况下不应该使用断言。

让我们深入探讨这些问题:

**用于公共方法中的参数检查**

您应该理解，参数检查是方法的已发布规范或契约的一部分。无论是否启用断言，都必须遵循这些规则。

继续这篇关于 Java 断言的文章

**使用断言进行操作**

默认情况下，断言是禁用的。你的程序不应该假设断言语句中的布尔表达式总是被求值。

让我们举一个例子，看看这会如何影响你的程序。比方说，您想从一个姓名列表中删除所有的空元素，并且您知道您的列表包含空元素。

assert names . remove(null)；

如果启用了断言，上面的代码片段将会工作。但是，如果断言被禁用，它就会失败，因为代码不会删除任何空元素。要解决这个问题，您可以在程序中使用下面的代码片段:

boolean nulls removed = names . remove(null)；断言 nullsRemoved

上面的代码片段将删除空值，即使断言被禁用。

现在，在执行了上面的 Java 程序之后，你应该已经理解了“Java 中的断言”。  这篇关于 Java 快速排序’的文章到此结束。如果你想了解更多， 请查看 Edureka 值得信赖的在线学习公司提供的 [**Java 培训**](https://www.edureka.co/java-j2ee-soa-training) 。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。