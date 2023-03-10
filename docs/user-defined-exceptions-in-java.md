# Java 中用户定义的异常是什么？

> 原文：<https://www.edureka.co/blog/user-defined-exceptions-in-java/>

异常是程序执行过程中出现的问题。Java，作为最流行的 **[面向对象语言之一，](https://www.edureka.co/blog/object-oriented-programming/)** 提供了处理这些异常的强大机制。在本文中，我将简要介绍 Java 中用户定义的 异常。

本文涵盖了以下主题:

*   什么是例外？
*   用户定义的异常

我们开始吧！

## 什么是例外？

异常是在程序运行时的程序执行过程中导致程序突然终止的突发意外事件。下面的快照显示了处理异常的执行流程。

![Exception flow - User Defined Exceptions in java - Edureka](img/a4744f1749ad46148fb4af2a7517d4bd.png)

我们总有一天会遇到这些异常，为了运行程序，我们必须解决这些异常。因此，我们需要首先了解这些类型的异常，以便在发生异常时，我们可以立即处理这些异常。

**使用 Try-Catch 块的异常:**

```
class MyException1 extends Exception{
   String str1;

   MyException1(String str2) {
	str1=str2;
   }
   public String toString(){ 
	return ("MyException Occurred: "+str1) ;
   }
}

class Example1{
   public static void main(String args[]){
	try{
		System.out.println("Starting of try block");
		throw new MyException1("This is error Message");
	}
	catch(MyException1 exp){
		System.out.println("Catch Block") ;
		System.out.println(exp) ;
	}
   }
}
```

在上面的代码片段中，我演示了 try-catch 块的用法，以及我们如何使用它来抛出异常。throw 关键字用于由用户引发异常。IO 异常用于这种异常处理。用户定义的异常必须包含自定义异常类。在代码中，我们使用了一个参数化的构造函数，它显示(这是错误消息)。

**输出:**

```
Starting of try block
Catch Block
MyException1 Occurred: This is error Message
```

**不使用试抓块**

```
class InvalidProductException extends Exception
{
    public InvalidProductException(String s)
    {
        // Call constructor of parent Exception
        super(s);
    }
}

public class Example1
{
   void Check(int weight) throws InvalidProductException{
	if(weight&lt;100){
		throw new InvalidProductException("Product Invalid");
	}
   }

    public static void main(String args[])
    {
    	Example1 obj = new Example1();
        try
        {
            obj.productCheck(60);
        }
        catch (InvalidProductException ex)
        {
            System.out.println("Caught the exception");
            System.out.println(ex.getMessage());
        }
    }
}
```

在这个例子中，我使用方法抛出异常。所以这里 throws 关键字被用在函数签名中，否则它会向我们显示一个错误。

**输出**

```
Caught the exception
Product Invalid
```

*基本上就是这么回事。这就把我们带到了关于 [Java](https://docs.oracle.com/javase/tutorial/) 中用户定义异常的博客的结尾。我希望你发现这个博客信息丰富，增加了你的知识价值。*

*查看 Edureka 的 [**Java 认证**](https://www.edureka.co/java-j2ee-training-course) 培训* *，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

*有问题吗？请在“Java 中的用户定义异常”博客的评论部分提到它，我们会尽快回复您。*T3