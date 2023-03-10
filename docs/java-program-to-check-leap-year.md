# 如何实现 Java 程序查闰年？

> 原文：<https://www.edureka.co/blog/java-program-to-check-leap-year/>

我敢肯定，你们每个人都一定听说过这个术语，闰年！闰年有 366 天，每四年一次。闰年的这一额外的一天被添加到二月。在这篇文章中，我将向你简要介绍如何用 [Java](https://www.edureka.co/blog/what-is-java/) 实现闰年程序。

这一概念的议程如下:

*   什么是闰年？
*   [用 Java 实现闰年程序](#javacode)
*   [Java 程序解释](#explanation)

让我们开始吧！

## 什么是闰年？

闰年有 366 天。现在检查一年是不是闰年是有一定条件的！让我们来看看它们:

*   年份应该能被 4 整除。
*   如果一年能被 100 整除，那它就不是闰年，除非它也能被 400 整除。比如说；以 2100 年为例:它能被 100 整除，因此根据条件它不应该是闰年，但是，第二部分说如果它也能被 400 整除，它就是闰年！因此，2100 是闰年，因为它可以被 100 整除，然后被 400 整除！

既然您已经很清楚这个概念，那么让我们通过 Java 代码来实现它。

## **用 Java 实现闰年程序**

下面是用 java 实现闰年程序的 java 代码:

### **代码:**

```
class Test 
{ 
    static boolean Year(int year) 
    { 

        if (year % 400 == 0) 
            return true; 

        if (year % 100 == 0) 
            return false; 

        if (year % 4 == 0) 
            return true; 
        return false; 
    } 

    public static void main(String[] args)  
    { 
        int year = 2018; 
        System.out.println( Year(2018)? "Leap Year" : 
                           "Not a Leap Year" ); 
    } 
} 

```

**输出:** 不是闰年

在这里，您见证了我们在 Java 中实现我们的[概念是多么容易。](https://www.edureka.co/blog/java-tutorial/)

## **Java 程序解释**

1.  输入你想让你的代码检查闰年的年份。
2.  然后，if 语句检查年份是 4 的倍数而不是 100，还是 400 的倍数。
3.  然后打印结果。

我希望你现在已经清楚 Java 中闰年的概念了。继续阅读，继续探索！

至此，我们结束了这篇关于“java 闰年程序”的博客。我希望它能增加你对 java 的[知识。](https://www.edureka.co/blog/java-tutorial/)

*既然您已经了解了 Java 代码，请查看 Edureka 提供的  [**Java 培训**](https://www.edureka.co/java-j2ee-soa-training)* *，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & [Spring](https://spring.io/) 。*

有问题要问我们吗？请在这个“java 闰年程序”博客的评论部分提到它，我们会尽快回复您。