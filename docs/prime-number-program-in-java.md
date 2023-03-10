# 了解 Java 中的质数程序

> 原文：<https://www.edureka.co/blog/prime-number-program-in-java/>

质数是大于 1 的自然数，只能被 1 和它本身整除。例如，2、3、5、7、11…是质数，因为它们既不能被整除，也不是乘法的结果。关于质数的程序是大一新生最常被问到的 [*Java 面试*](https://www.edureka.co/blog/interview-questions/java-interview-questions/) 问题之一。在本帖中，我收集了一些 [*Java 中重要的素数程序。*](https://www.edureka.co/blog/java-tutorial/)

*   [程序检查给定的数是否是质数](#Program_to_check_whether_the_given_number_is_prime_or_not?)
*   [程序找出两个给定数字之间的所有质数](#Program_to_find_out_all_prime_numbers_between_two_given_numbers?)
*   [程序使用递归](#Program_to_check_whether_the_given_number_is_prime_or_not_using_recursion?) 检查给定的数是否是质数
*   [程序使用标志变量](#Program_to_check_if_the_number_is_prime_or_not_using_a_flag_variable)检查数字是否是质数
*   [打印 1 到 100 之间质数的程序](#Program_to_print_prime_numbers_between_1_to_100)

让我们从第一个节目开始。

## **程序检查给定的数是否是质数？**

在这个 java 程序中，我会取一个数字变量，检查这个数字是否是质数。

*   isPrime(int n)方法用于检查传递给它的参数是否是素数。如果传递的参数是质数，则返回 True，否则返回 False。
*   如果数字小于 1，if(inputNumber<= 1)将返回 false。
*   如果数字不小于或等于 1，则执行除法运算。
*   如果余数为零，则返回 false，这意味着它不是质数。
*   如果它是一个非零数字，则返回 true，从而得到一个质数。

```
package prime;

import java.util.Scanner;

public class PrimeNumberProgram 
{
static boolean checkForPrime(int inputNumber)
{
boolean isItPrime = true;

if(inputNumber <= 1) 
{
isItPrime = false;

return isItPrime;
}
else
{
for (int i = 2; i<= inputNumber/2; i++) 
{
if ((inputNumber % i) == 0)
{
isItPrime = false;

break;
}
}

return isItPrime;
}
}

public static void main(String[] args) 
{
Scanner sc = new Scanner(System.in);

System.out.println("Enter a number :");

int inputNumber = sc.nextInt();

boolean isItPrime = checkForPrime(inputNumber);

if (isItPrime)
{
System.out.println(inputNumber+" is a prime number.");
}
else
{
System.out.println(inputNumber+" is not a prime number.");
}

sc.close();
}
}

```

*注:0 和 1 不是质数。*

这个程序的输出是:

![Outpu1t- Prime number program - Edureka](img/ed349ca6c41b463aff3b8d15b443e7d3.png) ![Output2 - Prime number program - Edureka](img/ff00173130cee1d42499a4b6fe59fce9.png)

让我们进入下一个程序，在 [Java](https://uatcom.edureka.in/blog/what-is-java) 中检查质数程序。

## **程序找出两个给定数字之间的所有质数**

为了找出两个自然数之间的质数，

*   检查数字是否是自然数。
*   使用 IsPrime 方法检查数字是否是质数。
*   指定起始编号和结束编号。
*   For 循环打印质数。
*   您可以对一系列数字执行此操作，只需指定范围(开始和结束)。

```
import java.util.Scanner;

public class PrimeNumberProgram
{
static boolean checkForPrime(int inputNumber)
{
boolean isItPrime = true;

if(inputNumber<= 1)
{
isItPrime = false;
return isItPrime;
}
else
{
for (int i = 2; i= inputNumber/2; i++){
if ((inputNumber % i) == 0){
IsItPrime = false;
break;
}
}
return isItPrime;
}
}
public static void main(String[] args)
{
Scanner sc = new Scanner(System.in);
System.out.println("Enter the start value :");
int start = sc.nextInt();
System.out.println("Enter the end value :");
int end = sc.nextInt();
System.out.println("Prime numbers between "+start+" and "+end+" : ");
for (int i = start; i <= end; i++)
{
if(checkForPrime(i))
{
System.out.println(i);
}
}
sc.close();
}
}

```

输出:

![Prime Number between two numbers - Prime number program - Edureka](img/e4259304c6d335f7e322800e7b4e046a.png)

让我们进入下一个程序，在 Java 中检查质数程序。

## **使用递归检查数字是否为质数的程序**

*   在这种情况下，让我们使用递归来打印素数。
*   Scanner 类是存在于 java 中的一个类。util 包，允许用户读取各种[类型](https://www.edureka.co/blog/java-tutorial/#datatype)的值。
*   首先使用 if 条件检查数字是否是自然数，如果(n <= 1)，返回 false 并打印出该数字不是质数。
*   检查另一个条件，就是除法，检查余数是否为 0。如果余数是 0，那么它就不是素数。

```

package prime;

import java.util.Scanner;

import java.util.Scanner;

public class Recursion {

public static void main(String[] args) {
Scanner s = new Scanner(System.in);
System.out.print("Enter a number : ");
int n = s.nextInt();
if (isPrime(n)) {
System.out.println(n + " is a prime number");
} else {
System.out.println(n + " is not a prime number");
}
}

public static boolean isPrime(int n) {
if (n<= 1) {
return false;
}
for (int i = 2; i< n; i++) {
if (n % i == 0) {
return false;
}
}
return true;
}
}

```

输出:

让我们继续进行另一个关于质数的重要程序。

## **程序使用标志变量**检查数字是否是质数

*   这个程序使用一个标志变量帮助打印质数。
*   标志变量在编程中用作信号，让用户/程序知道某个条件已经满足。
*   创建一个静态方法 checkPrime(int n ),并添加验证该数字是否为素数的条件。
*   通过传递参数(整数)在主类中调用这个函数。
*   打印质数。

```

package prime;

public class Program{
static void checkPrime(int n){
int i,m=0,flag=0;
m=n/2;
if(n==0||n==1){
System.out.println(n+" is not prime number");
}else{
for(i=2;i<=m;i++){
if(n%i==0){
System.out.println(n+" is not prime number");
flag=1;
break;
}
}
if(flag==0) { System.out.println(n+" is prime number"); }
}//end of else
}
public static void main(String args[]){
checkPrime(1);
checkPrime(3);
checkPrime(17);
checkPrime(20);
}
}

```

让我们来看看 Java 中关于质数程序的最后一个问题。

## **程序显示从 1 到 100 的质数**

*   在这种情况下，使用*计数器*，它经常需要从数据库或文本文件中了解某个东西的频率。
*   声明一个空字符串，String primeNumbers =
*   使用 for 循环直接指定实际数字。for(num = I；数量> = 1；num –)并检查这个范围内的质数。
*   如果给定的数字能被输入的数字整除，它就增加计数器的值。|
*   如果计数器值为 2，则以[字符串](https://www.edureka.co/blog/java-string/)的形式追加质数。

```

package prime;

public class OneToN {
public static void main (String[] args)
{
int i =0;
int num =0;
//Empty String
String primeNumbers = "";

for (i = 1; i <= 100; i++) { int counter=0; for(num =i; num>=1; num--)
{
if(i%num==0)
{
counter = counter + 1;
}
}
if (counter ==2)
{
//Appended the Prime number to the String
primeNumbers = primeNumbers + i + " ";
}
}
System.out.println("Prime numbers from 1 to 100 are :");
System.out.println(primeNumbers);
}
}

```

输出:

![Prime numbers from 1 to 100 - prime number program in Java - Edureka](img/016767fc2dfe5b4330da320949625446.png)

`这就把我们带到了本文的结尾，在这里我们学习了 Java 中质数程序的常见问题[和](https://www.edureka.co/blog/interview-questions/java-interview-questions/)。希望你清楚本教程中与你分享的所有内容。`

`***确保你尽可能多的练习，恢复你的经验。***`

`如果您发现这篇文章与“Java 中的质数程序”相关，请查看一下 *Edureka 的 [**Java 在线课程**](https://www.edureka.co/java-j2ee-training-course)* [，](https://www.edureka.co/java-j2ee-training-course)这是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。 *我们在这里帮助你踏上成为 java 开发人员的每一步，除了这个 Java 面试问题，我们还为想成为 Java 开发人员的学生和专业人士设计了一个课程。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。如果您刚刚开始，那么请阅读这篇 Java 教程，了解基本的 Java 概念。*`

`[https://www.youtube.com/embed/iGGgxnJCNRM](https://www.youtube.com/embed/iGGgxnJCNRM)

*如果您遇到任何问题，请在“Java 质数程序”的评论区提出您的所有问题，我们的团队将很乐意回答，或者您也可以参加我们在多伦多举办的 [Java 培训。](https://www.edureka.co/java-j2ee-training-course-toronto)*`