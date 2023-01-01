# Java 中的 System Class 是什么，如何实现？

> 原文：<https://www.edureka.co/blog/system-class-in-java/>

Java 为我们提供了一套全面的预建类和库，减少了编码开销。一个这样的类是 Java 中的系统类。在本文中，我将讨论构成这个类的各种概念，以及它们如何使它成为在 Java 开发人员中最广泛使用的一个类。

以下是我将在本文中讨论的主题:

*   [Java 中的系统类](#systemclass)
*   [java.lang.System 类声明](#declaration)
*   [类字段](#fields)
*   [系统类方法](#methods)
*   [实现系统类方法](#implementation)

让我们开始吧。

## **Java 中的系统类**

System 是 Java 中的核心[类之一，属于](https://www.edureka.co/blog/java-objects-and-classes/) **java.lang 包** 。系统类是最终类，不提供任何公共[构造函数](https://www.edureka.co/blog/constructor-in-java/)。因此，这个类中包含的所有成员和方法本质上都是静态的。因此，您不能继承该类来重写它的方法。由于 [Java](https://www.edureka.co/blog/java-tutorial/) 中的系统类有如此多的限制，因此有各种预构建的类字段和方法可用。下面我列出了这个类支持的一些重要特性:

*   标准输入和输出
*   错误输出流
*   访问外部定义的属性和环境变量
*   用于复制数组一部分的内置工具
*   提供加载文件和库的方法

既然你已经知道了 Java 中的系统类到底是什么，那么让我们继续前进，看看如何声明这个类。

## ****java.lang.System** 类声明**

下面我演示了声明为[**Java . lang . system**](https://docs.oracle.com/javase/7/docs/api/java/lang/System.html)的类:

```
public final class System extends Object
```

Java 中的 System 类带有各种内置的类字段和方法。现在，让我们在本文中更进一步，从类字段开始，逐个了解它们。

## **类字段**

**java.lang.System** 类带有三个字段:

1.  **public static final InputStream in:**这是 Java 编程中的标准输入流。该流已经打开，可用于提供输入数据。该输入流主要对应于键盘输入或由主机环境或用户指定的其他输入源。
2.  **public static final PrintStream out:**这是 [Java 编程](https://www.edureka.co/blog/java-programs/)中的标准输出流。该流已经打开，可用于接受输出数据。该输出流主要对应于显示由主机环境或用户指定的输出或另一输出目的地。
3.  **public static final PrintStream err:**这是 Java 编程中标准的错误输出流。该流已经打开，可用于接受输出数据。该输出流主要对应于显示由主机环境或用户指定的输出或另一输出目的地。从技术上讲，这个输出流用于显示错误消息或其他需要用户立即注意的信息。

既然您已经知道了 Java 中 System class 的类字段，现在让我们来看看这个类提供的各种方法。

## **系统类方法**

在 **java.lang.System** 类中总共声明了 28 个内置方法。下面我列出了他们每一个人以及他们的解释。

| **方法** | **描述** |
| *静态* *void arraycopy(Object src，int srcPos，Object dest，int destPos，int length)* | 此方法有助于从指定的源数组复制一个数组，从指定的位置开始，直到目标数组的指定位置。 |
| *静态字符串 clearProperty(字符串键)* | 此方法有助于移除由指定键指示的系统属性 |
| *静态控制台控制台()* | 该方法有助于返回与当前 JVM 相关联的任何可用的唯一控制台对象 |
| *静态长电流时间 Millis()* | 此方法有助于返回以毫秒为单位的当前时间 |
| *静态无效退出(int 状态)* | 这个方法有助于终止当前运行的 JVM |
| *静态 void gc()* | 这个方法有助于运行垃圾收集器 |
| *静态映射<字符串，字符串> getenv()* | 这个方法有助于返回当前系统环境的不可修改的字符串映射视图 |
| *静态字符串 getenv(字符串名称)* | 此方法有助于检索指定环境变量的值 |
| *静态属性 getProperties()* | 这种方法有助于确定当前的系统属性 |
| *静态字符串 getProperty(字符串键)* | 此方法有助于检索由指定键指示的系统属性 |
| *静态字符串 getProperty(String key，String def)* | 此方法有助于检索由指定键指示的系统属性 |
| *静态安全管理器 getSecurityManager()* | 此方法有助于检索系统安全界面 |
| *静态 int identityHashCode(对象 x)* | 此方法有助于为给定对象返回相同的哈希代码，其值将类似于默认方法 hash code()，而不考虑给定对象的类覆盖 hashCode() |
| *静态通道继承了 Channel()* | 这个方法有助于返回从创建 JVM 的实体继承的通道 |
| *静态字符串行分隔符()* | 此方法有助于返回依赖于系统的行分隔符字符串 |
| *静态无效负载(字符串文件名)* | 此方法有助于从本地文件系统加载具有指定文件名的代码文件作为动态库 |
| *静态 void loadLibrary(String libname)* | 此方法有助于加载由 libname 参数指定的系统库 |
| *静态字符串映射库名(字符串库名)* | 此方法有助于将库名映射到表示本机库的特定于平台的字符串 |
| *静态长纳米时间()* | 这个方法有助于在几纳秒内返回正在运行的 JVM 的高分辨率时间源的当前值 |
| *静态 void runFinalization()* | 此方法有助于执行任何挂起终结的对象的终结方法 |
| *静态 void setErr(PrintStream err)* | 此方法有助于重新分配“标准”错误输出流 |
| *静态 void setIn(InputStream in)* | 这种方法有助于重新分配“标准”输入流 |
| *静态无效抵消(打印流输出)* | 此方法有助于重新分配“标准”输出流 |
| *静态 void setProperties(属性 props)* | 此方法有助于将系统属性设置为属性参数 |
| *静态字符串 setProperty(字符串键，字符串值)* | 此方法有助于设置由指定键指示的系统属性 |
| *静态 void setSecurityManager(security manager s)* | 这种方法有助于设置系统安全性 |
| *静态 void runFi**nalizersOnExit(布尔值)* | **已弃用** |

现在，让我们在本文的下一节中尝试用 Java 实现 System 类的这些[方法](https://www.edureka.co/blog/java-methods/)。

## **用 Java 实现系统类**

在下面的例子中，我实现了上面讨论的一些方法。

```
package edureka;

import java.io.Console;
import java.lang.*;
import java.util.*;

public class SystemClassMethods {

	public static void main(String[] args) {
		String a[]= {"D","P","R","E","K","A"}; //source array  
        String b[]= {"E","D","U","V","O","I","D","L","E","A","R","N","I","N","G"};  //destination array  
        String src[],dest[];  

        int srcPos,destPos,length;
        src=a;
        srcPos=2;
        dest=b;
        destPos=3;
        length=4;

        System.out.print("Source array:"); 

        for(int i=0;i<src.length;i++) {System.out.print(a[i]);}  
        System.out.println(); 

        System.out.print("Destination array:");         
        for(int i=0;i<dest.length;i++) {System.out.print(b[i]);}  
        System.out.println();  
        System.out.println("Source Position:"+srcPos);  
        System.out.println("Destination Position:"+destPos);  
        System.out.println("Length:"+length);  
        System.arraycopy(src, srcPos, dest, destPos, length); //use of arraycopy() method 

        System.out.println("After Copying Destination Array: "); 
        for(int i=0;i<b.length;i++)  
        {
        	System.out.print(b[i]);  
        }  
        System.out.println();

        System.out.println("---------Implementing NanoTime Method----------");
        System.out.println("Current time in nanoseconds = "+System.nanoTime());  

        System.out.println();
        System.out.println("---------Implementing getProperties() Method----------");
        System.out.println("Your System property for user");  
        Properties p = System.getProperties();  
        System.out.println(p.getProperty("user.name")); //property to get User's account name  
        System.out.println(p.getProperty("user.home")); //property to get User's home directory  
        System.out.println(p.getProperty("user.dir")); //property to get User's current working directory 

        System.out.println();
        System.out.println("---------Implementing console() Method----------");
        Console console = System.console();

        if(console != null){
            Calendar c = new GregorianCalendar();
            console.printf("Welcome %1$s%n", "Edureka"); 
            console.printf("Current time is: %1$tm %1$te,%1$tY%n", c); 
            console.flush();
        } else{
        	//No console is attached when executed in Eclipse
        	System.out.println("No Console attached");
        }

        System.out.println();
        System.out.println("---------Implementing getSecurityManager() Method----------");
        SecurityManager secManager = System.getSecurityManager();
        if(secManager == null){
        	System.out.println("SecurityManager is not configured");
        }
        SecurityManager mySecManager = new SecurityManager();

        System.setSecurityManager(mySecManager);
        secManager = System.getSecurityManager();
        if(secManager != null){
        	System.out.println("SecurityManager is now configured");
        }        
   }

}

```

#### **输出**

```
Source array:DPREKA
Destination array:EDUVOIDLEARNING
Source Position:2
Destination Position:3
Length:4
After Copying Destination Array: 
EDUREKALEARNING

---------Implementing NanoTime Method----------
Current time in nanoseconds = 433367948321300

---------Implementing getProperties() Method----------
Your System property for user
Swatee_Chand
C:UsersSwatee_Chand
C:UsersSwatee_Chandeclipse-workspaceSystemClass

---------Implementing console() Method----------
No Console attached

---------Implementing getSecurityManager() Method----------
SecurityManager is not configured
SecurityManager is now configured
```

你可以尝试实现其余的方法，如果你遇到困难，你可以发表评论，我们会帮助你。

至此，我们结束了这篇关于 Java 中的系统类的文章。如果你想了解更多关于 Java 的知识，你可以参考我们的[其他 Java 博客](https://www.edureka.co/blog/what-is-java/)。

*既然您已经了解了 Java 中的系统类是什么，请查看 Edureka 提供的* [***Java 认证培训***](https://www.edureka.co/java-j2ee-training-course)*，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

*有问题吗？请在这篇“Java 中的系统类”文章的评论部分提到它，我们会尽快回复您。*