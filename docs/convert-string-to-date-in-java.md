# 如何在 Java 中将字符串转换为日期？

> 原文：<https://www.edureka.co/blog/convert-string-to-date-in-java/>

本文将向您介绍如何在 Java 中把字符串转换成日期，并给出一个完整的实践演示。本文将涉及以下几点:

*   [如何在 Java 中将字符串转换成日期？](#HowtoconvertStringtoDateinJava?)
*   [将日期作为文本>](#TakingthedateasaText)
*   [获取格式为“12/12/1988”](#TogettheDateformattedintheform%E2%80%9C12/12/1988%E2%80%9D)的日期
*   [更改时区](#TochangetheTimeZone)

让我们开始吧，

**如何在 Java 中将字符串转换成日期？**

在这里，我们将学习“如何使用简单的代码更改和技巧将字符串对象转换为日期对象”。最好的转换方式是 **字符串到日期**

```
SimpleDateFormat.parse(String);
```

**日期串**

```
SimpleDateFormat.format(Date);
```

解析工作方式多种多样:

继续这篇关于在 Java 中将字符串转换为日期的文章，

## **将日期作为文本**

如果你需要三个字母的月份文本，我们需要定义 3 'M '作为月份值。然后，月份值被解释为文本，如 Oct、Dec、Jun 等。

得到结果:1998 年 12 月 12 日

下面是用日期格式表示字符串值的代码。

```
Package com.test.test
import java.text.ParseException;
import java.text.SimpleDateFormat;
import java.util.Date;
public class TestDateExample1 {
public static void main(String[] argv) {
SimpleDateFormat formatter = new SimpleDateFormat("dd-MMM-yyyy");
String dateInString = "12-Dec-1998";
try {
Date date = formatter.parse(dateInString);
System.out.println(date);
System.out.println(formatter.format(date));
}catch (ParseException e) {
e.printStackTrace();
}
}
}
```

***输出:****Fri 12 月 00:00:00 MYT 1998*

继续这篇关于在 Java 中将字符串转换为日期的文章，

## **获取格式为“12/12/1988”**的日期

```
package com.test.date;
import java.text.ParseException;
import java.text.SimpleDateFormat;
import java.util.Date;
public class TestDateExample2
{
public static void main(String[] argv)
{
SimpleDateFormat formatter = new SimpleDateFormat("dd/MM/yyyy");
String dateInString = "12/12/1988";
try
{
Date date = formatter.parse(dateInString);
System.out.println(date);
System.out.println(formatter.format(date));
}catch (ParseException e) {
e.printStackTrace();
}
}
}
```

Java 8 使用提供 parse()方法的日期时间 API 将字符串值转换成日期时间值。对于基本的解析规则，已经定义了标准来以 *ISO_LOCAL_TIME 或 ISO_LOCAL_DATE* 格式表示日期和时间的字符串值。我们将格式化程序代码放在“try”和“catch”块中，每当不满足定义的规则时，它都会在运行时抛出一个异常。 简单解析的例子是:

```
LocalDateTime dateTime = LocalDateTime.parse("2018-05-05T11:50:55");
```

继续这篇关于在 Java 中将字符串转换为日期的文章，

## **改变时区**

为此，我们需要定义时区解析方法“ZonedDateTime ”,以直接将字符串值转换为日期-时间格式。你所需要做的就是定义你想要的日期时间所在的时区。例如，这里我们需要欧洲地区的日期和时间。因此，我们使用“ZonedDateTime”方法将 tiemzone 定义为 Europe/Paris::

```
ZonedDateTime zonedDateTime = ZonedDateTime.parse("2015-05-05T10:15:30+01:00[Europe/Paris]");
```

现在，我们来看看简单的 **日期时间 API** ，它使用 SimpleDateFormat: 将字符串值转换为日期值

1.  Java 引入了新的 *日期时间* API 调用以其版本 8 来表示日期时间的参数称为“java.time”。旧的称呼在所有以前的版本中用来表示日期的是*Java . util . date .*

让我们看看如何将一个字符串实际转换为本地日期和时间数据类型:

***解析 API 调用:***

如果我们需要转换为 *日期时间* 类型的字符串值是 ISO-801 格式，那么我们可以简单地使用 parse()方法调用 DateFormat 和 SimpleDateFormat 类。【T7

同样的一个例子:

```
import java.text.SimpleDateFormat;
import java.util.Date;
public class StringToDateExample1
{
public static void main(String[] args)throws Exception
{
String sDate1="31/12/1998";
Date date1=new SimpleDateFormat("dd/MM/yyyy").parse(sDate1);
System.out.println(sDate1+"t"+date1);
}
} 
```

**输出:**1998 年 12 月 31 日 周四 12 月 31 日 00:00:00 IST 1998 年

```
import java.text.SimpleDateFormat;
import java.util.Date;
public class StringToDateExample2 {
public static void main(String[] args)throws Exception {
String sDate1="12/10/1988";
String sDate2 = "12-Oct-1988";
String sDate3 = "12 10, 1988";
String sDate4 = "Wed, Oct 12 1988";
String sDate5 = "Wed, Oct 12 1988 23:37:50";
String sDate6 = "31-Dec-1998 23:37:50";
SimpleDateFormat formatter1=new SimpleDateFormat("dd/MM/yyyy");
SimpleDateFormat formatter2=new SimpleDateFormat("dd-MMM-yyyy");
SimpleDateFormat formatter3=new SimpleDateFormat("MM dd, yyyy");
SimpleDateFormat formatter4=new SimpleDateFormat("E, MMM dd yyyy");
SimpleDateFormat formatter5=new SimpleDateFormat("E, MMM dd yyyy HH:mm:ss");
SimpleDateFormat formatter6=new SimpleDateFormat("dd-MMM-yyyy HH:mm:ss");
Date date1=formatter1.parse(sDate1);
Date date2=formatter2.parse(sDate2);
Date date3=formatter3.parse(sDate3);
Date date4=formatter4.parse(sDate4);
Date date5=formatter5.parse(sDate5);
Date date6=formatter6.parse(sDate6);
System.out.println(sDate1+"t"+date1);
System.out.println(sDate2+"t"+date2);
System.out.println(sDate3+"t"+date3);
System.out.println(sDate4+"t"+date4);
System.out.println(sDate5+"t"+date5);
System.out.println(sDate6+"t"+date6);
}
}
```

通过使用上面的代码，你实际上可以得到所有提到的格式的结果。因此，我们在一个字符串值中定义了各种日期格式，然后通过定义 SimpleDateFormat 类来解析它们。完成后，输出以所有提到的日期时间格式生成。*1998 年 12 月 31 日* *周四 12 月 31 日 00:00:00:*

*1998 年 12 月 31 日**1998 年 12 月 31 日星期四 00:00:00:*

*1998 年 12 月 31 日**1998 年 12 月 31 日 00:00:00*

*1998 年 12 月 31 日星期四**1998 年 12 月 31 日星期四 00:00:00:*

*1998 年 1 2 月 31 日星期四 23 时 37 分 50 秒**1998 年 12 月 31 日星期四 23 时 37 分 50 秒*

*1998 年 1 2 月 31 日 23 时 37 分 50 秒**1998 年 12 月 31 日 23 时 37 分 50 秒*

要了解更多关于日期格式的信息，请阅读文档[【javadoc】](http://docs.oracle.com/javase/8/docs/api/java/text/SimpleDateFormat.html)。这里提到了一些有效的字符串到日期格式: y = year (yy 或 yyyy)

M =月(毫米)

d =一个月中的第几天(dd)

h =小时(0-12) (hh)

H =小时(0-23) (HH)

m =小时中的分钟(mm)

s =秒(ss)

S =毫秒(SSS)

z =时区文本(如太平洋标准时间…)

Z =时区，时间偏移(如-0800)

**注意:** 定义' Java.util.date '为 Date Date = new Date()；已被否决。所以，总是使用 **SimpleDateFormat** 和需要转换的匹配输入字符串。

“如何在 Java 中将字符串转换成日期？”这篇文章到此结束。如果您希望了解更多， 请查看值得信赖的在线学习公司 Edureka 的 [**Java 认证课程**](https://www.edureka.co/java-j2ee-training-course) 。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

如果您刚刚开始，那么请阅读这篇 Java 教程，了解基本的 Java 概念。

[https://www.youtube.com/embed/iGGgxnJCNRM](https://www.youtube.com/embed/iGGgxnJCNRM)

有问题要问我们吗？请在这篇文章的评论部分提到它，我们会尽快回复你。