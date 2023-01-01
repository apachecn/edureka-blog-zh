# 什么是 Java 中的 Do while 循环，如何使用？

> 原文：<https://www.edureka.co/blog/java-do-while-loop/>

[Java](https://www.edureka.co/blog/what-is-java/) *do-while 循环*用于迭代一组语句，直到满足给定条件。如果迭代次数不固定，并且必须至少执行一次循环，则使用 do while 循环。在本教程中，您将学习 Java 中的 do while 循环以及如何使用它。

让我们深入这篇文章，探讨以下主题:

我们开始吧！

## **Java 中的 Do while 循环是什么？**

Do-while 循环与 [while 循环](https://www.edureka.co/blog/java-while-loop/)相似，但有一点不同:在 while 循环中，条件在循环体执行之前计算，而在 do-while 循环中，条件在循环体执行之后计算。

我会通过这个流程图让概念在视觉上变得清晰。

## **流程图:**

让我解释一下上面的图表:

现在，转到 Java 中 do while 循环的语法

### **语法:**

**做** {

//要执行的代码

} **而**(条件)；

如您所见，语法非常简单。接下来，让我通过一个示例向您展示 do while 循环的实现。

## **实例实现:**

```
 public class Example {

   public static void main(String args[]) {
      int x = 1;

      do {
         System.out.print("value of x : " + x );
         x++;
         System.out.print("n");
      }while( x < 11 );
   }
}

```

**输出:**

x 值:1x 值:2x 值:3x 值:4x 值:5x 值:6x 值:7x 值:8x 值:9x 值:10

在上面提到的代码中，您可以看到 do while 循环将执行条件一次，这是肯定的。

现在，让我们进入下一部分，Java 中的无限 do-while 循环。

## **Java 中的无限 do-while 循环**

Java 中的无限 do-while 循环类似于*无限 while 循环。*你可以参考我之前博客的一个部分——[Java 中的无限 while 循环](https://www.edureka.co/blog/java-while-loop/#Infinitewhileloop)。

如果在 do-while 循环中传递' true ',它将是不定式 do-while 循环。下面是语法:

### **语法:**

**做** {

//要执行的代码

} **而** ( **真**)；

下面是一个简单的例子，描述了 java 不定式 do while 循环的用法。

### **不定式 do while 循环示例:**

```
	public class DoWhileInfinite {  
	public static void main(String[] args) {  
	    do{  
	        System.out.println("infinitive do while loop");  
	        }while(true);  
	}  
	} 

```

**输出:**

不定式 do while 循环不定式 do while 循环不定式 do while 循环

为了退出循环，按下 ***ctrl+c*** 。

至此，我的博客已经接近尾声。我希望这些数据对您的 [Java](https://www.edureka.co/blog/java-tutorial/) 知识有所帮助。我们将继续挖掘 Java 世界的更多概念。敬请期待！

*查看 Edureka 的*[***Java 培训***](https://www.edureka.co/java-j2ee-soa-training)**，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 25 万名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。**

**有问题吗？请在这篇“Java 中的 Do while 循环”博客的评论部分提到它，我们会尽快回复您。**