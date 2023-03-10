# Java 中的回文:如何检查一个数是回文？

> 原文：<https://www.edureka.co/blog/palindrome-in-java>

当人们[参加 Java](https://www.edureka.co/blog/interview-questions/java-interview-questions/) 的面试时，通常会测试他们的逻辑和编程技能。最常见的问题之一是 Java 中的回文程序。回文只是一个数字或者一个字符串，当它被反转时不会改变。比如: ***12321*** 或者 ***MAAM*** 。很明显，字母在反转时形成镜像。

I have covered the following aspects which demonstrate multiple ways to check Palindrome in Java:

*   [回文程序使用 While 循环](#PalindromeUsingWhileLoop)
*   [回文程序使用 For 循环](#PalindromeUsingForLoop)
*   [回文程序(字符串)使用库方法](#PalindromeUsingLibraryMethod)

## **回文程序使用 While 循环**

这是一个最简单的程序来找到回文程序使用'循环'。让我们深入一个例子来检查给定的输入是否是回文。

```
public class PalindromeProgram {

    public static void main(String[] args) {

        int rem, rev= 0, temp;
	int n=121; // user defined number to be checked for palindrome 

        temp = n;

        // reversed integer is stored in variable 
        while( n != 0 )
        {
            rem= n % 10;
            rev= rev * 10 + rem;
            n=n/10;
        }

        // palindrome if orignalInteger(temp) and reversedInteger(rev) are equal
        if (temp == rev)
            System.out.println(temp + " is a palindrome.");
        else
            System.out.println(temp + " is not a palindrome.");
    }
}
```

**输出:** 121 是一个回文数

**说明**:输入你要检查的数字，存储在一个临时(temp)变量中。现在反转数字，比较临时数字是否与反转的数字相同。如果两个数相同，将打印回文数，否则不是回文数。

**注:**回文程序的逻辑不变，只是执行不同。

现在你已经清楚了逻辑，让我们试着用另一种方式在 Java 中实现回文程序，即使用 while 循环。

## **回文程序使用 For 循环**

```
public class PalindromeProgram {

    public static void main(String[] args) {

        int n=1234521, rev=0, rem, temp;

        temp = n;

        for( ;n != 0; n /= 10 )
        {
            rem = n % 10;
            rev= rev* 10 + rem;
        }

        // palindrome if temp and sum are equal
        if temp== rev)
            System.out.println(temp + " is a palindrome.");
        else
            System.out.println(temp + " is not a palindrome.");
    }
}

```

**输出:** 1234521 不是回文

**Explanation:** In the above program, the number is not a palindrome. The logic remains the same, just ‘for’ loop is used instead of a while loop. On each iteration, num /= 10 is executed and condition num!=0 is checked.

## **Java 中的回文程序(字符串)使用库方法**

在本节中，我们将找到一个 [Java 字符串](https://www.edureka.co/blog/java-string/)的回文。它的工作原理和整数一样，比如“madam”是回文，但“madame”不是回文。让我们用 Java 实现这个回文程序，使用字符串反转函数。

```
class PalindromeProgram
{
public static void checkPalindrome(String s)
{
// reverse the given String
String reverse = new StringBuffer(s).reverse().toString();

// checks whether the string is palindrome or not
if (s.equals(reverse))
System.out.println("Yes, it is a palindrome");

else
System.out.println("No, it is not a palindrome");
}

public static void main (String[] args)
throws java.lang.Exception
{
checkPalindrome("madam");
}
}
```

**输出:**对，是回文

**Explanation:** In the above code, we have used [string](https://www.edureka.co/blog/java-string/) reverse function to calculate the reverse of a number and then compare the same with the original number. If both the numbers are same, it will print palindrome number, else not a palindrome number.This brings us to the end of this article where we have learned how to find palindrome in Java. Hope you are clear with all that has been shared with you in this tutorial.***Make sure you practice as much as possible and revert your experience.*  **

如果您发现这篇文章与“Java 中的回文”相关，请查看一下 **Edureka 的 [Java 认证](https://www.edureka.co/java-j2ee-training-course)培训、** 一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。 *我们在这里帮助你踏上成为 java 开发者的每一步，除了这个 Java 面试问题，我们还为想成为 Java 开发者的学生和专业人士设计了一个课程。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

如果您遇到任何问题，请在“Java 回文”的评论区提出您的所有问题，我们的团队将很乐意回答。