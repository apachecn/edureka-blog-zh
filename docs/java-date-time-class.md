# 如何在 Java 中获取日期和时间？

> 原文：<https://www.edureka.co/blog/java-date-time-class/>

*[Java](https://www.edureka.co/blog/what-is-java/)* 提供了构成当前日期和时间的日期类。这个类可以在 **java.util 包**中找到。让我们更深入一点，理解 Java 中的日期和时间是如何设置的。

我们将关注的主题列举如下:

*   [日期类的构造函数和方法](#ConstructorandMethodsofDateclass)
*   [Java 日期](#JavaDates)
*   如何获取当前日期？
*   如何获取当前时间？
*   [如何获取当前日期和时间](#Howtogetcurrentdateandtime?)
*   [日期和时间格式](#DateandTimeformatting)

让我们开始吧！

## **日期类的构造函数和方法**

Date 类使用两个[构造函数](https://www.edureka.co/blog/constructor-in-java/):

### **构造函数:**

**Date( ):** 这个构造函数将用当前的日期和时间初始化对象。

**Date(long 毫秒):** 该构造函数接受一个参数，该参数等于自 1970 年 1 月 1 日午夜以来经过的毫秒数。

### **日期类的方法:**

Date 类中提供了几种方法。

**Object clone( ):** 该方法复制被调用的 Date 对象。

**boolean before(date Date):**如果被调用的' Date '对象包含的' Date '早于–Date 中的值所指定的日期，则返回 true，否则返回 false。

**(date Date)后布尔:** 如果被调用的' Date '对象包含的' Date '晚于 Date 指定的日期，则返回 true，否则返回 false。

**boolean equals(对象日期):** 如果被调用的日期对象包含与‘Date’指定的时间和日期相同的时间和日期，则返回 true，否则返回 false。

**long getTime( ):** 返回自 1970 年 1 月 1 日以来经过的毫秒数。

**int compare to(Object obj):**如果“obj”属于类 Date，则它的操作与 compareTo(Date)相同。否则，它抛出一个 ClassCastException。

**int hashCode( ):** 返回被调用对象的哈希码。

**void setTime(long Time):**设置由 time 指定的时间和日期，表示从 1970 年 1 月 1 日午夜开始经过的时间，单位为毫秒。

**String toString( ):** 将调用的 Date 对象转换为字符串并返回结果。

现在，让我们继续讨论 Java 日期。

## **Java 日期**

Java 没有为我们提供内置的日期类。我们必须从 **java.util 包中导入它。**这个包为我们提供了各种日期和时间类。以下是一份清单:

| **类** | **描述** |
| 当地日期 | 它表示一个日期(年、月、日(YYYY-MM-dd)) |
| 当地时间 | 它表示时间(小时、分钟、秒和毫秒(HH-mm-ss-zzz)) |
| 日期时间格式器 | 它是显示和解析日期时间对象的格式化程序 |
| 当地日期时间 | 它表示日期和时间(YYYY-MM-dd-HH-mm-ss.zzz) |

现在，继续，让我们看看如何获得当前的日期和时间？

## **如何获取当前日期？**

要显示当前日期，请导入 **java.time.LocalDate** 类。下面列出了一个例子。

```
import java.time.LocalDate;
public class Example {
public static void main(String[] args) {
LocalDate myObj = LocalDate.now();
System.out.println(myObj);
}

```

**产出:** 2019-08-09

同样，如果你想知道当前时间，这里有一个例子。

## 如何获取当前时间？

示例:

```
import java.time.LocalTime;
public class Example2 {
public static void main(String[] args) {
LocalTime myObj = LocalTime.now();
System.out.println(myObj);
}
}

```

**输出:** 15:38:17.483594

进一步，如果您希望一起获取当前日期和时间， *[Java](https://www.edureka.co/blog/java-tutorial/)* 为您提供了 LocalDateTime 方法。这里有一个例子:

## 如何获取当前日期和时间？

```
package Edureka;

import java.time.LocalDateTime;
public class Example {
public static void main(String[] args) {
LocalDateTime myObj = LocalDateTime.now();
System.out.println(myObj);
}
}

```

**输出:**

2019-08-08T18:13:34.269

现在，如果你想以不同的方式，或者以不同的格式显示日期和时间，我们有一个方法叫做: **ofPattern()** 方法。

## **日期和时间格式**

在这一部分中，您可以根据自己的要求自由显示日期和时间的格式。举例:

```
package Edureka;

import java.time.LocalDateTime; 
// Import the LocalDateTime class 
import java.time.format.DateTimeFormatter; 
// Import the DateTimeFormatter class 
public class Aggregation { public static void main(String[] args) 
{ 
LocalDateTime myDateObj = LocalDateTime.now(); 
System.out.println("Output with previous format: " + myDateObj); 
DateTimeFormatter myFormatObj = DateTimeFormatter.ofPattern("DD-MM-YYY HH:mm:ss"); 
String formattedDate = myDateObj.format(myFormatObj); 
System.out.println("Output After formatting: " + formattedDate); 
} 
}

```

**输出:**

原格式输出:2019-08-08T17:38:09.419 格式化后输出:08-08-2019 17:38:09

这就把我们带到了本文的结尾，我们已经通过各种例子学习了 Java 的日期和时间。希望你清楚本教程中与你分享的所有内容。

如果您发现这篇文章与“Java 中的日期和时间”相关，请查看一下  [*Edureka Java 认证培训*、](https://www.edureka.co/java-j2ee-soa-training) 这是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。

我们在这里为您的旅程中的每一步提供帮助，并为希望成为 Java 开发人员的学生和专业人士设计课程。该课程旨在让你在 Java 编程方面有一个良好的开端，并训练你掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

如果您遇到任何问题，请在“Java 中的日期和时间”的评论区提出您的所有问题，我们的团队将很乐意回答。