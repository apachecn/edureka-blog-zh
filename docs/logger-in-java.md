# Java 中的 logger 是什么，为什么要用它？

> 原文：<https://www.edureka.co/blog/logger-in-java>

日志是一个重要的特性，开发人员需要考虑它来追溯错误。Java 是最流行的编程语言之一，它通过提供一个基本的日志 API 来提供一种可定制的日志方法。因此，在这篇关于 Java 日志记录器的文章中，我将讨论[的专业人士](https://www.edureka.co/java-j2ee-training-course)如何使用这个特性来实现 Java 中的可扩展日志记录。

本文将涵盖以下主题:

之前，我们深入探讨了 java 中的日志记录，让我们了解了日志记录的必要性。

## **需要记录日志**

在构建应用程序时，我们经常会遇到需要调试的错误。因此，在日志的帮助下，我们可以很容易地获得关于应用程序中发生了什么的信息，包括错误和异常情况的记录。现在，您可能会想到，为什么不在 [Java](https://www.edureka.co/blog/java-tutorial/) 中使用 System.out.print()语句。这些语句的问题是日志消息只会在控制台上显示。所以，一旦你自动关闭控制台，所有的日志都会丢失。因此，日志不会被永久存储，而是逐个显示，因为这是一个单线程环境。

为了避免这样的问题，在通过 `java.util.logging` 包和 `org.apache.log4j.*`包提供的 API 的帮助下，Java 的登录被简化了。

## **测井组件**

Java 日志组件帮助开发人员创建日志，将日志传递到各自的目的地，并保持正确的格式。以下是三个组件:

*   **Loggers**–负责捕获日志记录，并将它们传递给相应的 Appender。
*   **Appenders 或 Handlers**–他们负责将日志事件记录到目的地。在发送输出之前，Appenders 在布局的帮助下格式化事件。
*   **布局或格式器**–负责确定数据出现在日志条目中时的外观。

您可以参考下图了解所有三个组件的工作情况:

![Logging Components - Logger in Java - Edureka](img/e2eaf068de3480e54c7cad8faedac1e1.png)

当应用程序进行日志记录调用时，Logger 组件将事件记录在 LogRecord 中，并将其转发给适当的 Appender。然后，它根据所需的格式使用布局格式化记录。除此之外，您还可以使用多个过滤器来指定哪些 Appenders 应该用于事件。

现在，让我们深入了解一下什么是 Java 中的 logger。

## **Java 中的 Logger 是什么？**

Java 中的记录器是触发日志事件的对象，它们是在应用程序的代码中创建和调用的，在应用程序中，它们在将日志事件传递给下一个组件(即 Appender)之前生成日志事件。您可以在一个类中使用多个记录器来响应各种事件，或者在一个层次结构中使用记录器。它们通常使用分层的点分隔名称空间来命名。此外，所有记录器名称都必须基于所记录组件的类或包名。

除此之外，每个记录器在[记录器](https://docs.oracle.com/javase/7/docs/api/java/util/logging/Logger.html)名称空间中保持对最近的现有祖先的跟踪，并且还具有与之相关联的“级别”。我将在本文的后半部分讨论日志记录器，但在此之前，让我向您展示如何用 Java 创建日志记录器。

### **创建新的记录器**

用 Java 创建一个新的记录器的过程非常简单。你得用 `Logger.getLogger()`的方法。`getLogger()` [方法](https://www.edureka.co/blog/java-methods/)识别记录器的名称，并将字符串作为参数。因此，如果记录器预先存在，则返回该记录器，否则创建一个新的记录器。

#### **语法:**

```
static Logger logger = Logger.getLogger(SampleClass.class.getName());

```

这里，SampleClass 是我们正在获取 Logger 对象的类名。

**举例:**

```
public class Customer{
    private static final Logger LOGGER = Logger.getLogger(Customer.class);
    public void getCustomerDetails() {
    }
}

```

既然我已经告诉了您如何在 Java 中创建一个日志记录器，那么让我们来看看日志记录中可用的不同级别。

### **日志级别**

日志级别用于根据日志的严重性或对应用程序稳定性的影响对日志进行分类。 `org.apache.log4j.*`包和`java.util.logging `都提供了不同级别的日志记录。让我们一个一个来看看。

`org.apache.log4j.*`软件包按降序提供以下级别:

*   致命的
*   错误
*   警告
*   信息
*   调试

`java.util.logging`软件包按降序提供以下级别:

*   严重(最高级别)
*   警告
*   信息
*   配置
*   很好
*   好的
*   最精细(最低级别)

除此之外，上述包还提供了两个额外的级别`ALL`和`OFF`，分别用于记录所有消息和禁用记录。

#### **使用`org.apache.log4j.*`包登录 Java 的例子:**

```
import org.apache.log4j.Logger;
public class Customer {
    static Logger logger = Logger.getLogger(Customer.class);
    public static void main(String[] args) { 
	logger.error("ERROR");
        logger.warn("WARNING");	
	logger.fatal("FATAL");
        logger.debug("DEBUG");
        logger.info("INFO");
        System.out.println("Final Output");
    }
}

```

因此，如果您的输出是我们的 *log4j.properties* 文件中的 root logger 作为 WARN 级别，那么优先级高于 WARN 的所有错误消息都将打印如下:

您也可以使用`java.util.logging`包中的 setLevel()方法设置等级，如下所示:

```
logger.setLevel(Level.WARNING);

```

#### **使用`java.util.logging`包登录 Java 的例子:**

```
package edureka;
import java.io.IOException; 
import java.util.logging.Level; 
import java.util.logging.Logger; 
import java.util.logging.*; 

class EdurekaLogger { 
    private final static Logger LOGGER =  Logger.getLogger(Logger.GLOBAL_LOGGER_NAME);   
    public void sampleLog() 
    { 
        LOGGER.log(Level.WARNING, "Welcome to Edureka!"); 
    } 
}   
public class Customer { 
    public static void main(String[] args) 
    { 
        EdurekaLogger obj = new EdurekaLogger(); 
        obj.sampleLog(); 
        LogManager slg = LogManager.getLogManager();        
        Logger log = slg.getLogger(Logger.GLOBAL_LOGGER_NAME);   
        log.log(Level.WARNING, "Hi! Welcome from Edureka"); 
    } 
} 

```

要使用`org.apache.log4j.*`包或`java.util.logging`包在您的应用程序中启用日志记录，您必须配置属性文件。接下来，在这篇关于 Java Logger 的文章中，让我们讨论一下它们的属性文件。

### **Log4j 和 Java Util 包的属性文件**

#### **样本 Log4j 属性文件:**

```
# Enable Root logger option
log4j.rootLogger=INFO, file, stdout
# Attach appenders to print file
log4j.appender.file=org.apache.log4j.RollingFileAppender
log4j.appender.file.File=E:loglogging.log
log4j.appender.file.MaxFileSize=10MB
log4j.appender.file.MaxBackupIndex=5
log4j.appender.file.layout=org.apache.log4j.PatternLayout
log4j.appender.file.layout.ConversionPattern=%d{yyyy-MM-dd HH:mm:ss} %-5p %c{1}:%L - %m%n
# Attach appenders to print on console
log4j.appender.stdout=org.apache.log4j.ConsoleAppender
log4j.appender.stdout.Target=System.out
log4j.appender.stdout.layout=org.apache.log4j.PatternLayout
log4j.appender.stdout.layout.ConversionPattern=%d{yyyy-MM-dd HH:mm:ss} %-5p %c{1}:%L - %m%n

```

*   Log4j 属性文件创建在项目的 src 文件夹中。
*   log4j . appender . file = org . Apache . log4j . rolling file appender->打印文件中的所有日志
*   log4j . appender . stdout = org . Apache . log4j . console appender->打印控制台中的所有日志
*   log4j . appender . file . file = D:log logging . log->指定日志文件的位置
*   log4j . appender . file . max filesize = 10MB->日志文件的最大大小为 10MB
*   log4j . appender . file . maxbackupindex = 5->将备份文件的数量限制为 5 个
*   log4j . appender . file . layout = org . Apache . log4j . pattern layout-->指定日志打印到日志文件的模式。
*   log4j . appender . file . layout . conversion pattern = % d { yyyy-MM-DD HH:MM:ss } %-5p % c { 1 }:% L –% m % n-->设置默认转换模式。

#### **样例** **Java Util 包属性文件**

```

handlers= java.util.logging.ConsoleHandler

.level= WARNING

# Output will be stored in the default directory
java.util.logging.FileHandler.pattern = %h/java%u.log
java.util.logging.FileHandler.limit = 60000
java.util.logging.FileHandler.count = 1
java.util.logging.FileHandler.formatter = java.util.logging.XMLFormatter

# Level of logs will be limited to WARNING and above.
java.util.logging.ConsoleHandler.level = WARNING
java.util.logging.ConsoleHandler.formatter = java.util.logging.SimpleFormatter

```

这里，

*   Java . util . logging . file handler . pattern = % h/Java % u . Log->日志文件将被写入 C:TEMPjava1.log
*   Java . util . logging . file handler . limit = 50000->记录器写入任何一个文件的最大字节数。
*   Java . util . logging . file handler . count = 1->指定输出文件的数量
*   Java . util . logging . file handler . formatter = Java . util . logging . XML formatter->提到用于格式化的格式化程序。这里使用了 XML 格式化程序。
*   Java . util . logging . console handler . level = WARNING->将默认日志级别设置为 WARNING
*   Java . util . logging . console handler . Formatter = Java . util . logging . SimpleFormatter->指定所有控制台处理程序使用的格式化程序，这里使用的是 simple Formatter。

#### **记录事件**

要在 [Java](https://www.edureka.co/blog/what-is-java/) 中记录事件，您必须确保您分配了一个级别来轻松过滤事件。要指定级别并提及消息，您可以使用以下方法:

#### **方法一:**

```
logger.log(Level.INFO, “Display message”);

```

```
Here, level is INFO and the message to be printed is "Display Message".
```

#### **方法二:**

```
logger.info(“Display message”);

```

要确保 Java 中的 Logger 只记录 INFO 级别或以上的事件，可以使用上面讨论的 **setLevel()** 方法。

现在，我已经讨论了如何在 Java 中使用 Logger，让我们讨论 Log4j 架构的下一个组件，即 Appenders。

## **追加器或处理程序**

附加器或处理程序负责将日志事件记录到目标。每个记录器都可以访问多个处理程序，并从记录器接收日志消息。然后，附加器使用格式化程序或布局来格式化事件，并将它们发送到相应的目的地。

可以使用 setLevel(Level)关闭 Appender。OFF)方法。`java.util.logging`包中两个最标准的处理程序如下:

*   **FileHandler:** 将日志信息写入文件
*   **控制台处理器:**将日志消息写入控制台

为了让您更好地理解，我在属性部分解释了几个附加器。

## **布局或格式器**

格式化程序的布局用于格式化和转换日志事件中的数据。日志框架为 HTML、XML、Syslog、JSON、纯文本和其他日志提供了布局。

1.  **SimpleFormatter** :生成包含基本信息的短信。
2.  **XMLFormatter** :为日志生成 XML 消息

为了让您更好地理解，我在属性部分解释了一些布局。至此，我们结束了这篇关于“Java 日志记录器”的博客。我希望你们清楚这篇文章教给你们的东西。如果您刚刚开始，那么请阅读这篇 Java 教程，了解基本的 Java 概念。

[https://www.youtube.com/embed/iGGgxnJCNRM](https://www.youtube.com/embed/iGGgxnJCNRM)

*查看 Edureka 提供的 [**Java 在线课程**](https://www.edureka.co/java-j2ee-training-course)* *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

*有问题吗？请在这个“Java 日志记录器”博客的评论部分提到它，我们会尽快回复您。*