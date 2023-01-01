# Java 中的 Object 是什么，如何使用？

> 原文：<https://www.edureka.co/blog/java-object/>

Java 是一种面向对象的语言。换句话说，Java 中的几乎所有东西都被视为对象。因此，在用 Java 编程时，应该知道用 Java 创建对象的所有可能的方法。但是在深入研究对象之前，您必须知道 [Java 类](https://www.edureka.co/blog/java-objects-and-classes/)的概念以及对象与它们的关系。

在这篇文章中，我们将介绍用 Java 创建对象的 5 种不同方法，并理解理解这些方法所需的所有基本概念。

1.  [使用‘新建’关键字创建对象](#newkeyword)
2.  [使用克隆( )方法创建对象](#clone()method)
3.  [使用](#newinstance()method) 类的 newInstance()方法创建对象
4.  [使用反序列化创建对象](#deserialization)
5.  [使用构造函数类](#newinstance()method) 的 newInstance()方法创建对象

让我们开始吧。

## **使用‘新建’关键字创建对象**

在用 Java 编程时，你可能肯定会遇到“新”这个关键词。它是一个关键字，用于创建一个动态分配内存的对象，即内存是在运行时分配给这些对象的。并且在创建对象时，大部分时间都需要这种动态分配。因此这种方法比其他方法更常用。

**语法**:class name object name = new class constructor()；

```
public class ObjectCreation {
   String FirstString = "Hello World";
   public static void main(String[] args)
   {
       ObjectCreation obj = new ObjectCreation();
       System.out.println(obj.FirstString);
   }
}
```

**输出-** 你好世界

如果一个类有不止一个[构造函数](https://www.edureka.co/blog/constructor-in-java/)，那么这种在 Java 中创建对象的方法可以和这个类的任何构造函数一起使用。

## **使用 clone()方法创建对象**

如果我们想要创建的对象是一个已经存在的[对象](https://www.edureka.co/blog/java-tutorial/#obj)的副本呢？在这种情况下，我们可以使用 clone()方法。clone()是 Object 类的一部分，但不能直接使用，因为它是一个受保护的方法。

clone()方法只有在实现了 Cloneable 接口并处理了CloneNotSupportedException 后才能使用。

```
class Message implements Cloneable
{
   String FirstString;

   Message() {
       this.FirstString = "Hello World";
   }
   public Object clone() throws
           CloneNotSupportedException
   {
       return super.clone();
   }

}

public class ObjectCreation {
   public static void main(String[] args) throws
           CloneNotSupportedException
   {
       Message FirstObj = new Message();
       System.out.println(FirstObj.FirstString);

       Message SecondObj = (Message)FirstObj.clone();
       System.out.println(SecondObj.FirstString);

       SecondObj.FirstString = "Welcome to the world of programming";

       System.out.println(SecondObj.FirstString);

       System.out.println(FirstObj.FirstString);

   }
}
```

**输出-**

你好世界

你好世界

欢迎来到编程的世界

你好世界

在上面的程序中，我们创建了一个已经存在的对象的副本。为了确保两个[变量](https://www.edureka.co/blog/java-tutorial/#variables)不指向同一个内存位置，有必要改变第二个对象的‘first string’的值，然后打印两个对象的值。

## **使用类 Class** 的 newInstance()方法创建对象

这种方法不常用于创建对象。如果我们知道类名，并且默认构造函数本质上是公共的，就使用这种创建对象的方法。为了使用这个方法创建对象，我们需要处理 3 个异常

**ClassNotFoundException-**如果 JVM 找不到作为参数传递的类，就会出现这种异常。

**instantiation exception-**如果给定的类不包含默认的构造函数，就会出现这个异常。

**IllegalAccessException-**如果我们没有访问指定的[类](https://www.edureka.co/blog/java-objects-and-classes/)的权限，就会发生这个异常。

一旦我们解决了这些异常，我们就万事大吉了。

```
class ObjectCreation{
   String FirstString = "Hello World";
   public static void main(String[] args)
   {
       try
       {
           Class Message = Class.forName("ObjectCreation");
           ObjectCreation obj =
                   (ObjectCreation) Message.newInstance();
           System.out.println(obj.FirstString);
       }
       catch (ClassNotFoundException e)
       {
           e.printStackTrace();
       }
       catch (InstantiationException e)
       {
           e.printStackTrace();
       }
       catch (IllegalAccessException e)
       {
           e.printStackTrace();
       }
   }

}
```

**输出-** 你好世界

## **使用反序列化创建对象**

在 Java 中，序列化用于将对象的当前状态转换成字节流。反序列化正好相反，因为我们使用字节流重新创建对象。对于序列化的过程，我们需要实现可序列化的接口。使用此方法创建对象时要进行异常处理。

```
ObjectInputStream objectInputStream = new ObjectInputStream(inputStream);
Classname object = (classname) objectInputStream.readObject();

```

## **使用构造函数类** 的 newInstance()方法创建对象

我们看到了用于创建对象的 class Class 的 newInstance 方法。类似地，类构造函数也由 newInstance()方法组成，该方法可用于创建对象。其他可以默认的构造函数借助这个方法我们也可以调用[参数化的构造函数](https://www.edureka.co/blog/parameterized-constructor-in-java/)。

```
import java.lang.reflect.*;

public class ObjectCreation
{
   private String FirstString = "Hello World";
   ObjectCreation()
   {
   }
   public void changeMessage(String message)
   {
       this.FirstString = message;
   }
   public static void main(String[] args)
   {
       try
       {
           Constructor<ObjectCreation> constructor = ObjectCreation.class.getDeclaredConstructor();
           ObjectCreation objectCreation = constructor.newInstance();
           objectCreation.changeMessage("Welcome to the world of programming");
           System.out.println(objectCreation.FirstString);
       }
       catch (Exception e)
       {
           e.printStackTrace();
       }
   }
}
```

**输出-**

欢迎来到编程的世界

在 Java 中有 5 种不同的创建对象的方法，其中一些比另一些更常用。每种方法都有自己的优缺点。最终，选择权在你。

Java 是一门有趣的语言，但是如果基础不清楚，它就会变得很棘手。首先，你要学习并掌握所有与 java 技术相关的技能，报名参加 [Java 认证项目](https://www.edureka.co/java-j2ee-training-course) ，释放你作为 Java 开发者的潜能。

有问题吗？请在这篇“Java 中的对象”文章的评论部分提到这一点，我们会尽快回复您。