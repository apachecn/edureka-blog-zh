# 如何在 Java 中创建日期格式

> 原文：<https://www.edureka.co/blog/date-format-in-java/>

不同的编程语言有不同的处理日期的方式。 [Java](https://www.edureka.co/blog/what-is-java/) 使用日期格式来做同样的事情。在本文中，我们将详细了解 Java 中的日期格式。以下是本文关注的要点，

*   [创建日期格式](#CreatingADateFormat)
*   [创建简单的日期格式](#CreatingASimpleDateFormat)
*   [日期到字符串](#DateToString)
*   [到目前为止的字符串](#StringToDate)

所以让我们从这篇文章开始，

## **Java 中的日期格式**

Java 中的 DateFormat 类用于格式化日期。可以将指定的日期格式化为数据/时间字符串。例如，日期可以格式化为:mm/dd/yyyy。日期格式类不同步。

让我们继续，看看 tom 是如何创建日期格式的

## **创建日期格式**

```
public final String format(Date date)
```

此方法以字符串格式返回日期或时间。

**举例:**

```

import java.text.*;
import java.util.Calendar;
public class Main {
public static void main(String[] args)
{
//Initializing the date formatter
DateFormat Date = DateFormat.getDateInstance();
//Initializing Calender Object
Calendar cals = Calendar.getInstance();
//Displaying the actual date
System.out.println("The original Date: " + cals.getTime());
//Using format() method for conversion
String currentDate = Date.format(cals.getTime());
System.out.println("Formatted Date: " + currentDate);
}
}

```

**输出:**

原始日期:世界协调时 2019 年 7 月 8 日 08 时 21 分 53 秒

格式化日期:2019 年 7 月 8 日

在这篇关于 Java 日期格式的文章的下一部分，我们将看到如何创建一个简单的日期格式，

## **创建简单的日期格式**

SimpleDateFormat 是一个具体的类，用于以区分区域设置的方式格式化和解析日期。

```
String pattern = "yyyy-MM-dd";
SimpleDateFormat simpleDateFormat = new SimpleDateFormat(pattern);

```

指定的参数“pattern”是用于格式化和解析日期的模式。

在本文的下一部分，我们将看到如何用日期到字符串的方法创建一个简单的日期格式，

## **日期到字符串**

也可以使用 SimpleDateFormat 在 java 中格式化日期:

```
import java.text.SimpleDateFormat;
import java.util.Date;
public class Main {
public static void main(String[] args) {
Date date = new Date();
SimpleDateFormat DateFor = new SimpleDateFormat("dd/MM/yyyy");
String stringDate= DateFor.format(date);
System.out.println(stringDate);
}
}

```

**输出:**

08/07/2019

在这篇关于 Java 中日期格式的文章的下一部分，我们将看到如何用字符串到日期的方法创建一个简单的日期格式，

## **到目前为止的字符串**

我们使用解析的方法将字符串转换为日期。

```
import java.text.ParseException;
import java.text.SimpleDateFormat;
import java.util.Date;
public class Main {
public static void main(String[] args) {
SimpleDateFormat DateFor = new SimpleDateFormat("dd/MM/yyyy");
try{
Date date = DateFor.parse("08/07/2019");
System.out.println("Date : "+date);
}catch (ParseException e) {e.printStackTrace();}
}
}

```

**输出:**

日期:2019 年 7 月 08 日 00:00:00 UTC

**举例:**

让我们来看看多种格式的完整示例:

```

import java.text.ParseException;
import java.text.SimpleDateFormat;
import java.util.Date;
import java.util.Locale;
public class Main {
public static void main(String[] args) {
Date date = new Date();
SimpleDateFormat DateFor = new SimpleDateFormat("MM/dd/yyyy");
String stringDate = DateFor.format(date);
System.out.println("Date Format with MM/dd/yyyy : "+stringDate);
DateFor = new SimpleDateFormat("dd-M-yyyy hh:mm:ss");
stringDate = DateFor.format(date);
System.out.println("Date Format with dd-M-yyyy hh:mm:ss : "+stringDate);
DateFor = new SimpleDateFormat("dd MMMM yyyy");
stringDate = DateFor.format(date);
System.out.println("Date Format with dd MMMM yyyy : "+stringDate);
DateFor = new SimpleDateFormat("dd MMMM yyyy zzzz");
stringDate = DateFor.format(date);
System.out.println("Date Format with dd MMMM yyyy zzzz : "+stringDate);
DateFor = new SimpleDateFormat("E, dd MMM yyyy HH:mm:ss z");
stringDate = DateFor.format(date);
System.out.println("Date Format with E, dd MMM yyyy HH:mm:ss z :"+stringDate);
}
}

```

**输出:**

日期格式为 MM/dd/yyyy : 07/08/2019

日期格式为年月日时:分:秒:秒:2019 年 7 月 8 日 08 时 51 分 58 秒

日期格式与 DD MMMM yyyy:2019 年 7 月 8 日

日期格式为 DD MMMM yyyy zzzz:2019 年 7 月 8 日协调世界时

日期格式为 E，DD MMM yyyy HH:mm:ss z:Mon 2019 年 07 月 08 日 08:51:

58 协调世界时

***这些方法在 java 的编程语言中用来格式化和解析日期。***

这样，我们就结束了这篇关于“Java 中的日期格式”的文章。如果您想了解更多，请查看由 Edureka(一家值得信赖的在线学习公司)提供的  [Java 认证](https://www.edureka.co/java-j2ee-training-course)培训。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。如果你刚刚开始，那么看看这篇 Java 教程，理解基本的 Java 概念。

[https://www.youtube.com/embed/aqHhpahguVY](https://www.youtube.com/embed/aqHhpahguVY)

有问题要问我们吗？请在本文的评论部分提到它，我们会尽快回复您，或者您也可以参加我们在多伦多举办的 [Java 培训。](https://www.edureka.co/java-j2ee-training-course-toronto)