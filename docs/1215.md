# Java 中的阶乘程序:如何求一个数的阶乘？

> 原文：<https://www.edureka.co/blog/factorial-program-in-java/>

作为初学者，你会经常在 [Java 面试](https://www.edureka.co/blog/interview-questions/java-interview-questions/)中碰到阶乘程序。通俗地说，正整数的阶乘是所有降序整数的乘积。一个数的阶乘( *n)* 用 n 来表示！。还有，0 的阶乘是 1，没有为负整数定义。下面是计算一个数的阶乘的简单表示-

n！= n*(n-1)*(n-2)*。。。。。*1

Java 中求阶乘有多种方法，下面列出-

*   [Java 中使用 for 循环的阶乘程序](#factorialprogramusingforloop)
*   [Java 中的阶乘程序使用 while 循环](#factorialprogramusingwhileloop)
*   [Java 中使用递归的阶乘程序](#factorialprogramusingrecursion)

我们开始吧。

## **使用 For 循环的阶乘程序**

这是使用“For Loop”找到一个数的阶乘的最简单的程序之一。让我们深入一个例子，找出一个给定输入的阶乘。

```
public class FactorialProgram{  
 public static void main(String args[]){  
  int i,fact=1;    // defining fact=1 since least value is 1
  int number=5;    // given input to calculate factorial
  for(i=1;i<=number;i++){    
      fact=fact*i;    
  }    
  System.out.println("Factorial of "+number+" = "+fact);    
 }  
}  
```

**输出:**5 的阶乘= 120

**解释:** 将待求阶乘的数作为输入，存储在变量‘number’中。这里，我们已经初始化了 fact=1，因为最小值是 1。然后，我们使用 for 循环遍历 1 和输入数字(5)之间的所有数字，其中每个数字的乘积存储在变量“fact”中。

**注:** 阶乘程序的逻辑不变，只是执行方式不同。

既然你已经清楚了这个逻辑，让我们试着用另一种方式来实现[Java](https://uatcom.edureka.in/blog/what-is-java)中的阶乘程序，即使用 while 循环。

## **Java 中的阶乘程序使用 while 循环**

Java 中的 While 循环帮助您的代码根据条件重复执行。让我们访问代码并使用 while 循环在 Java 中实现阶乘程序。如果您遇到与该计划相关的任何错误或疑问，请务必告知我们。

```
public class FactorialProgram  
{

    public static void main(String[] args) {

        int number = 5; // user-defined input to find factorial
        long fact = 1; // defining fact=1 since least value is 1
        int i = 1;
        while(i<=number)
        {
            fact = fact * i;
            i++;
        }
        System.out.println("Factorial of "+number+" = "+fact);
    }
}
```

**输出:**5 的阶乘= 120

**解释-** 在上面的程序中，I 的值在循环体内递增。正如我上面已经提到的，java 中 factorial 的逻辑保持不变，只是执行方式不同。

接下来，让我们使用递归在 Java 中实现阶乘。

**Java 中使用递归的阶乘程序**

递归是一个不断调用自己的函数或方法。您可以使用调用自身的递归方法，从而使代码简短但理解起来有点复杂。让我们通过访问下面的代码来了解更多关于递归的知识。

```
public class FactorialProgram
{
	 static int factorial(int n){    
	  if (n == 0)    
	    return 1;    
	  else    
	    return(n * factorial(n-1));    
	 }    
	 public static void main(String args[]){  
	  int i,fact=1;  
	  int number=5; // user-defined input to find factorial    
	  fact = factorial(number);   
	  System.out.println("Factorial of "+number+" is = "+fact);    
	 }  
	}  
```

**输出-**5 的阶乘= 120

**解释:**在上面的代码中，我创建了一个递归方法 factorial，它调用自己，直到满足条件。

This brings us to the end of this article where we have learned how to implement factorial program in Java. Hope you are clear with all that has been shared with you in this tutorial. ***Make sure you practice as much as possible and revert your experience!***

如果你想学

如果您发现这篇文章与“Java 中的阶乘程序”相关，请查看一下 **Edureka 的 [Java 课程](https://www.edureka.co/java-j2ee-training-course)，** 这是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。 *我们在这里帮助你踏上成为 java 开发者的每一步，除了这个 Java 面试问题，我们还为想成为 Java 开发者的学生和专业人士设计了一个课程。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

如果您遇到任何问题，请在“Java 阶乘程序”的评论区提出您的所有问题，我们的团队将很乐意回答。