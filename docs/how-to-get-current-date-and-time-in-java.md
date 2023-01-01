# 如何在 Java 中获取当前日期和时间？

> 原文：<https://www.edureka.co/blog/how-to-get-current-date-and-time-in-java/>

想知道如何在 Java 中获取当前日期和时间吗？这篇文章会给你不同的方法来做同样的事情。本文将涉及以下几点:

*   [使用日期类](#UsingDateClass)
*   [使用日历类](#UsingCalendarClass)
*   [日期/时间 API](#Date/TimeAPI)

让我们从这篇关于如何在 Java 中获取当前日期和时间的文章开始吧。

## **如何在 Java 中获取当前日期和时间**

当需要在 java 编程语言中获取当前日期时，可以使用以下方法:

## **使用日期类**

用户所需的模式是在创建 SimpleDateFormat 实例时指定的。使用 DateFormat 类的 format()方法是为了将 date 对象作为参数传递给该方法。

```
DateFormat dform = new SimpleDateFormat("dd/MM/yy HH:mm:ss");
Date obj = new Date();
System.out.println(dform.format(obj)); 

```

该代码以上述格式显示日期和时间，即 25/07/2019 22:12:32。

继续这篇关于如何在 Java 中获取当前日期和时间的文章。

## **使用日历类:**

指定用户期望的模式。

Calendar 类的对象是使用 getInstance 方法()创建的。调用 format 方法，并将 Calendar.getTime()作为参数传递给该方法。

```
DateFormat dfor = new SimpleDateFormat("dd/MM/yy HH:mm:ss");
Calendar obj = Calendar.getInstance();
System.out.println(dfor.format(obj.getTime()));

```

**举例:**

```
import java.util.Date;
import java.text.DateFormat;
import java.text.SimpleDateFormat;
import java.util.Calendar;
public class Main {
public static void main(String[] args) {
//getting current date and time using Date class
DateFormat dfor = new SimpleDateFormat("dd/MM/yy HH:mm:ss");
Date obj = new Date();
System.out.println(dfor.format(obj));
/*getting current date time using calendar class 
*An Alternative of above*/
Calendar cobj = Calendar.getInstance();
System.out.println(dfor.format(cobj.getTime()));
}
} 

```

**输出:** 25/07/19 09:23:35

25/07/19 09:23:35

在 java 中，还有其他各种方法可以访问当前日期:

**时间。时钟**

时钟。SystemUTC.instant()方法输出当前日期和时间。

```
System.out.println(java.time.Clock.systemUTC().instant());
```

**sql。日期**

使用 java.sql.Date 类的实例可以显示Java中的当前日期。

```
long millis=System.currentTimeMillis();  
java.sql.Date dates=new java.sql.Date(millis);  
System.out.println(dates);

```

继续这篇关于如何在 Java 中获取当前日期和时间的文章。

## **日期/时间 API**

Java 8 中引入了一个新的 API。这样做的唯一原因是替换 java.util.Date 和 java.util.calendar。

**局部日期时间**

此方法返回 LocalDateTime 类的实例，并打印日期和时间。

```
System.out.println(java.time.LocalDateTime.now());
```

**局部日期**

这个方法只返回当前日期。

```
LocalDate date = LocalDate.now();
```

**当地时间**

这个方法只是返回当前时间，并且可以被格式化。

```
LocalTime time = LocalTime.now();
```

**ZonedDateTime**

此方法根据时区使用，可以通过以下方式实现:

```
ZonedDateTime dateTime = ZonedDateTime.now();
```

这也可以被格式化。

java 为用户提供了在 Java 中检索当前日期的非常有效的方法。

关于“如何在 Java 中获取当前日期和时间”的文章到此结束。如果您想了解更多，请查看 Edureka 提供的 Java 培训，这是一家值得信赖的在线学习公司。Edureka 的 [Java 课程](https://www.edureka.co/java-j2ee-training-course)旨在训练你掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。