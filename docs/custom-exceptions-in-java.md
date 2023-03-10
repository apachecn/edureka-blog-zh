# Java 中如何处理自定义异常？

> 原文：<https://www.edureka.co/blog/custom-exceptions-in-java/>

Java 为用户提供了创建他们自己的异常的选项。这种异常称为自定义异常或用户定义的异常。在本文中，我们将探索 Java 中的自定义异常。

本文将涉及以下几点:

*   [自定义异常](#CustomException)
*   [自定义检查异常](#CustomCheckedExceptions)
*   [自定义未检查的异常](#CustomUncheckedExceptions)

这篇文章介绍了 Java 中的自定义异常。

## **Java 中的自定义异常**

可以按如下方式创建自定义异常:

[Java]//表示用户定义异常的类类 InvalidAgeException 扩展异常{InvalidAgeException(String s){super(s)； } } [/java]

```
//class that uses InvalidAgeException
class Test{  
static void validate(int age)throws InvalidAgeException{  
if(age<18)  
throw new InvalidAgeException("Invalid");  
else  
System.out.println("Eligible to Drive");  
}    
public static void main(String args[]){  
try{  
validate(15);  
}catch(Exception m){System.out.println("Exception: "+m);}  
System.out.println("Exit");  
}  
} 

```

**输出:**

异常:InvalidAgeException:无效

出口

继续这篇关于 Java 中自定义异常的文章。

## **需要定制例外**

通常，程序员发现需要指定他/她自己的异常。

引入这些例外的原因可能如下:

*   有一些只为业务逻辑和工作流定义的例外。这使用户能够确定问题的根源。
*   捕捉和处理现有的或先前定义的 java 异常。

Java 为用户提供了两个例外:

*   自定义检查异常
*   自定义未检查的异常

继续这篇关于 Java 中自定义异常的文章。

## **自定义检查异常**

自定义检查的异常是扩展 java.lang.Exception 的异常。它们本质上是可恢复的，并且是显式处理的。在下面的示例中，编写了一段代码来返回文件的第一行作为输出:

```
try (Scanner file = new Scanner(new File(fileName)))
{
if (file.hasNextLine()) return file.nextLine();
}
catch(FileNotFoundException e)
{
}

```

代码抛出异常 FileNotFound。用户不知道该异常的原因。我们不知道异常的来源，是由于文件不存在还是由于无效的文件名导致的。为了实现自定义异常，java.lang.Exception 类被扩展。

```
public class InvalidFileNameException extends Exception
{ 
public InvalidFileNameException(String errorMessage)
{
super(errorMessage);
}
}

```

创建一个名为 InvalidFileNameException 的自定义检查异常。

创建异常时必须提供构造函数。在我们的例子中，构造函数将 String 作为错误消息，并调用父类构造函数。

```

try (Scanner file = new Scanner(new File(fileName)))
{
if (file.hasNextLine())
return file.nextLine();
}catch (FileNotFoundException e)
{
if (!isCorrectFileName(fileName))
{
throw new InvalidFileNameException("Invalid filename : " + fileName );
}
}

```

尽管用户现在知道了确切的异常，但我们已经失去了异常的根本原因。这可以通过向构造函数添加 java.lang.Throwable 来解决。InvalidFileNameException 现在可以与异常的根本原因一起使用:

```
public InvalidFileNameException(String errorMessage, Throwable err) 
{
super(errorMessage, err);
}

```

继续这篇关于 Java 中自定义异常的文章

## **自定义未检查的异常**

自定义检查异常扩展了 java.lang.RuntimeException。它们本质上是不可恢复的。

```
public class InvalidFileExtensionException 
extends RuntimeException 
{
public InvalidFileExtensionException(String errorMessage, Throwable err) {
super(errorMessage, err);
}
}

```

该异常的用法如下:

```
try (Scanner file = new Scanner(new File(fileName)))
{
if (file.hasNextLine()) 
{
return file.nextLine();
} 
else 
{
throw new IllegalArgumentException("File is not readable.");
}
} 
catch (FileNotFoundException err) 
{
if (!isCorrectFileName(fileName)) {
throw new InvalidFileNameException("Invalid filename : " + fileName , err);
}
} 
catch(IllegalArgumentException err) 
{
if(!containsExtension(fileName)) 
{
throw new InvalidFileExtensionException("Filename does not have any extension : " + fileName, err);
}
}

```

用户定义的异常是必不可少的，因为它们使我们能够定义属于自己的异常。

我们就此结束了这篇文章。如果您想了解更多，请查看 Edureka 提供的 Java 培训，这是一家值得信赖的在线学习公司。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

*有问题吗？请在这个博客的评论部分提到它，我们会尽快回复你。*