# 如何在 Java 中显示斐波那契数列？

> 原文：<https://www.edureka.co/blog/fibonacci-series-in-java/>

斐波那契数列是一个奇特的数列，以意大利数学家斐波那契命名。从 0 和 1 开始，斐波纳契数列中的每个新数字都是前面两个数字的和。例如，从 0 和 1 开始，序列中的前 5 个数字是 0、1、1、2、3 等等。在本文中，让我们学习如何用 [Java](https://www.edureka.co/blog/java-tutorial/) 编写斐波那契数列。

用 Java 写斐波那契数列主要有两种方法:

*   [不使用递归的斐波那契数列](#Fibonacci)
    *   [使用 For 循环](#FibonacciWithFor)
    *   [使用 While 循环](#FibonacciWithWhile)
*   [使用递归的斐波那契数列](#FibonacciWithRecursion)

我们开始吧！

## **不使用递归的斐波那契数列**

在不使用递归的情况下生成斐波纳契数列时，有两种方法:

1.  使用“for”循环
2.  使用“while”循环

## **方法 1:使用 for 循环编写斐波那契数列的 Java 程序**

下面的程序将帮助你如何编写一个 java 程序来使用 for 循环生成 Fibonacci 数列中的第一个‘n’数。这里使用的逻辑非常简单。首先，我已经初始化了数列的前两个数。然后是 for 循环，它将两个直接的前一个循环相加，并打印出值。这一直持续到程序打印出系列中的第一个“n”个数字。

```
package Edureka;
import java.util.Scanner;
public class Fibonacci {

	public static void main(String[] args) 
	{

		 int n, first = 0,next = 1;

		    System.out.println("Enter how may fibonnaci numbers to print");
	        Scanner scanner = new Scanner(System.in);
	        n = scanner.nextInt();
	        System.out.print("The first " + n + " Fibonacci numbers are: ");
	        System.out.print(first + " " + next);
	        for (int i = 1; i<=n-2; ++i)
	        {
	            int sum = first + next;
	            first = next;
	            next = sum;
	            System.out.print(" " + sum);
	        }

	}

}
```

**输出:**

```
Enter how may fibonnaci numbers to print
7
The first 7 Fibonacci numbers are: 0 1 1 2 3 5 8

```

***注**:for 循环中的条件为‘n-2’。那是因为程序在开始 for 循环之前已经打印了' 0 '和' 1 '。*

## **方法 2:使用 while 循环编写斐波那契数列的 Java 程序**

逻辑和前面的方法类似。您需要小心的只是 while 循环条件。看看下面的 [java](https://www.edureka.co/blog/what-is-java/) 代码，了解如何使用 while 循环生成斐波那契数列。

```
package Edureka;
import java.util.Scanner;
public class FibWhile {

	public static void main(String[] args) 
	{

		 int n, first = 0,next = 1;

		    System.out.println("Enter how may fibonnaci numbers to print");
	        Scanner scanner = new Scanner(System.in);
	        n = scanner.nextInt();
	        System.out.print("The first " + n + " Fibonacci numbers are: ");
	        System.out.print(first + " " + next);
	        int i = 1;
	        while (i<n-1)
	        {
	            int sum = first + next;
	            first = next;
	            next = sum;
	            System.out.print(" " + sum);
	            i++;
	        }

	}
}
```

**输出:**

```

Enter how may fibonnaci numbers to print 
7 
The first 7 Fibonacci numbers are: 0 1 1 2 3 5 8 

```

## **使用递归的斐波那契数列**

递归是基本的 java 编程技术，其中函数直接或间接调用自己。相应的函数称为递归函数。使用递归算法，某些问题可以很容易地解决。让我们看看如何使用递归在 Java 中打印 Fibonacci 数列的前 n 个数字。

下面的程序应该可以帮助你编写一个递归的 java 程序来生成斐波那契数列中的第一个“n”数。这里的逻辑很容易理解。首先，用户给出输入，然后使用for 循环，直到每次迭代调用函数 *`fibonaccinumber(int n)`* 返回位置 n 处的斐波那契数。斐波那契函数递归调用自身，将前两个斐波那契数相加。

```
package Edureka;
import java.util.Scanner;
public class FibRec {

	public static void main(String[] args) 
	{

		 int n;

		    System.out.println("Enter how may fibonnaci numbers to print");
	        Scanner scanner = new Scanner(System.in);
	        n = scanner.nextInt();

	        for (int i = 0; i<=n-1; ++i)
	        {
	           System.out.print(fibonaccinumber(i) + " ");
	        }
	}

	public static int fibonaccinumber(int n) {

		if(n==0)
			return 0;
		else if(n==1)
			return 1;
		else
			return fibonaccinumber(n-1) + fibonaccinumber(n-2);

	} 
}
```

**输出:**

```

Enter how may fibonnaci numbers to print 
7 
The first 7 Fibonacci numbers are: 0 1 1 2 3 5 8 

```

这就把我们带到了这篇“Java 中的斐波那契数列”文章的结尾。我们已经学习了如何使用循环语句或递归以编程方式打印第 n 个斐波那契数。

*如果你发现了这篇关于“Java 中的斐波那契数列”的文章，请查看 Edureka 的 [**Java 课程**](https://www.edureka.co/java-j2ee-training-course) 培训，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。*

*有问题吗？请在这个“Java 中的斐波那契数列*”*的评论部分提到它，我们会尽快回复你。*