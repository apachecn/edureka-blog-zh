# C 语言中的阶乘程序:如何计算一个数的阶乘？

> 原文：<https://www.edureka.co/blog/factorial-program-in-c/>

正整数的阶乘是一个整数和它下面所有整数的乘积，即数字 n 的阶乘(用 n 表示！)将由给出

n！= 1*2*3*4* .。。。。*n

0 的阶乘定义为 1，不为负整数定义。有多种方法可以找到它，如下所列-

*   [C 中的阶乘程序 使用 For 循环](#factorialusingforloop)
*   [](#factorialusingforloop)[阶乘程序使用 函数](#factorialusingfunctions)
*   [阶乘程序 利用递归](#factorialusingrecursion)

让我们开始吧。

## **阶乘使用 For 循环**

求一个数的阶乘是最简单易行的方法。让我们先来看看代码—

```
#include <stdio.h>

 int main()

{

    int I , num , fact = 1; //defining factorial as 1 since least value is 1

   printf (“Enter a number to calculate its factorial”);

   scanf (“%d”, &num);

   if (num<0) //if the input is a negative integer

   {

   printf (“Factorial is not defined for negative numbers.”);

   }

   else

   {

   for(i=1;i<= num;i++) //for loop doesn’t gets executed for input 0 as 1>0,  therefore fact value remains 1

{

fact = fact * i;  // keeps on multiplying and storing in the value of factorial till the input integer is reached

              }

   printf(“Factorial of %d = %dn”, num, fact);

    }

    return 0; //since we have defined the main() method with a return value of integer type

}
```

****输出-****

5 的阶乘= 120

****解说**–**

要计算阶乘的数字作为输入，存储在一个变量中，并检查它是否为负。如果输入的整数是负数，则显示相应的消息。factorial 的值被预定义为 1，因为它的最小值是 1。对正整数执行 for 循环(除了 0，因为 0 的测试条件为假，所以事实保持为零)。在 for 循环中，阶乘的值与每个整数相乘并连续存储，直到达到输入数。例如，对于输入= 5，流程转到 For 循环，并执行以下步骤-

*事实=1，I =1—>事实= 1 * 1 = 1—>I =2 事实= 1，I = 2—>事实= 1 * 2 = 2—>I = 3 事实= 2，I = 3—>事实= 2 * 3 =6—>I = 4 事实= 6，I = 4—>事实= 6 * 4 =24—>I = 5 事实= 24*

现在 6 > 5，因此测试条件变为假，循环终止。将显示阶乘的值。

## **阶乘使用函数**

这种方法被称为模块化方法，编程时应遵循这种方法，因为它非常有效。它的一个优点是，当我们需要修改代码时，我们可以只修改相关的函数，而不是修改整个代码。使用这种方法寻找一个数的阶乘的代码如下所示

```
#include <stdio.h>

long factorial(int num)     //function for calculating factorial which takes an integer value as a parameter and returns an int type value
{
  int i;
  long fact = 1;

  for (i = 1; i <= num; i++)
	fact = fact * i;
 return fact;   	//returns to function call
}

int main()        	//execution begins from main() method
{
  int num;

  printf("Enter a number to calculate its factorialn");
  scanf("%d", &num);
  if(num<0) //if the input is a negative integer
  {
   printf("Factorial is not defined for negative numbers.");
   }
  printf("Factorial of %d = %dn", num, factorial(num));                             	//call to factorial function passing  the input as parameter
   return 0;
}

```

****输出【T2——****5 的阶乘= 120

****解说-****

除了使用不同的函数计算阶乘并将值返回到开始执行的 main 方法之外，程序的逻辑是相同的。

## **阶乘使用递归**

递归是函数调用自身，对应的函数称为递归函数的过程。它由两部分组成——一个基本条件和一个递归调用。提供基本条件的解，而较大值的解可以通过转换为较小值来求解，直到达到并使用基本解。

下面是使用递归寻找阶乘的代码:-

```
#include<stdio.h>
int fact(int);     //function prototype
int main()
{
    int num;
    printf("Enter the number whose factorial is to be find :");
    scanf("%d" ,&num);
    if(num<0)
    {
        printf("ERROR. Factorial is not defined for negative integers");
    }
    printf("Factorial of %d is %d", num, fact(num));  //first call is made
    return 0;
}
int fact(int num)
{
    if(num==0)    //base condition
    {
        return 1;
    }
    else{
        return(num*fact(num-1));   //recursive call
    }
}

```

**输出**–5 的阶乘= 120

**说明**—假设用户输入 5 作为输入，那么在 main()方法中，num 的值是 5。随着流程进入 printf 语句(第 12 行),调用 fact(5)函数。现在，事实(5) num 是 5，不等于 0，因此流程转到 else 语句，在该语句中，进行递归调用，并进行事实(4)。重复该过程，直到达到基本条件，即 num=0，并返回 1。现在流程转到事实(1)，从那里返回 1(至于事实(1) num=1)*1(从事实(0)返回的值)。重复该过程，直到获得所需值。

## **时间&空间复杂度——递归 V/S 迭代**

### **为递归-**

关于 **时间复杂度** ，我们知道阶乘 0 是唯一的比较。因此 T (0) =1。对于任何其他数字的阶乘，该过程包括一次比较、一次乘法、一次减法和一次函数调用。因此

T(n)= T(n-1)+3= T(n-2)+6= T(n-3)+9=… = T(n-k)+3k

因为我们知道 T (0) =1，对于 k=n，(n-k) =0

因此 T (n) =T (0) +3n = 1+3n

因此，该码的时间复杂度为 O (n)。

关于 **空间复杂度，** 为每个调用创建一个栈，该栈将被维护直到其值被计算并返回 。例如，对于 n=5，必须维护以下堆栈

*f(5)——>f(4)——>f(3)——>f(2)——>f(1)——>f(0)*

正如我们可以看到的，将必须维护 5 个堆栈，直到到达对 f(0)的调用，其值是已知的 并被返回。因此，对于 n 阶乘，必须维护 n 个堆栈。因此空间复杂度为 O(n)。从上面的图片中也可以明显看出，对于 n=5，必须维护 5 个堆栈。因此，对于 n 阶乘，必须维护 n 个堆栈。因此空间复杂度是 O(n)。

### **用于迭代-**

关于 **时间复杂度，** 循环内有 n 次迭代，因此时间复杂度为 O(n)。

关于 **空间复杂度，** 对于迭代求解，只需要维护一个栈，使用整数变量。所以空间复杂度为 O(1)。

本文到此为止。我希望你已经理解了 C 语言中阶乘程序的概念以及时间复杂性。

如果您遇到任何问题，请在“C 语言阶乘程序”的评论区提出您的所有问题，我们的团队将很乐意回答。