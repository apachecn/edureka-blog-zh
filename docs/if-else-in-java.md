# 如何用 Java 实现 If Else？

> 原文：<https://www.edureka.co/blog/if-else-in-java/>

Java 中的条件可以通过使用 if 语句来测试。if 语句后面还可以跟一个 else 语句，当布尔表达式为 false 时执行该语句。本文将讨论 Java 中的 If Else 语句。

本文将涉及以下几点:

*   [if 语句](#ifstatement)
*   [if-else 语句](#if-elsestatement)
*   [使用三元运算符](#UsingTernaryOperators)
*   [if-else-if 阶梯](#if-else-ifladder)
*   [嵌套 if 语句](#Nestedifstatement)

从这篇关于 JAVA 中的 if else 的文章开始。

java 中有多种类型的 if 语句:

## **if 语句**

if 语句用于测试条件，后跟一组语句。只有当条件被证明为真时，语句才会执行。

**语法:**

```
if(condition){  
//code to be executed  
}  

```

**例子**

```
public class Test 
{  
public static void main(String[] args) 
{  
    //defining a 'price' variable  
    int price=1800;  
    //checking the price  
    if(price>1500){  
        System.out.print("Price is greater than 1500");  
    }  
}  
}

```

**输出:**

价格大于 1500

继续这篇关于 JAVA 中 if else 的文章。

## **if-else 语句**

java 中的 if-else 语句也用于测试条件。如果条件为真，则执行 if 块。如果条件为假，则执行 else 块。

**语法:**

```
if(condition)
{
//code if condition is true
}else{
//code if condition is false
}

```

**举例:**

```
public class Test 
{  
public static void main(String[] args) 
{  
    //defining a variable  
    int num=15;  
    //Checking if the number is divisible by 2 
    if(num%2==0){  
        System.out.println("Even number");  
}else
{  
        System.out.println("Odd number");  
 }  
}  
}  

```

**输出:**

奇数

让我们看另一个例子，程序检查输入的年份是否是闰年。

**举例:**

```
public class Test {    
public static void main(String[] args) {    
    int year=2028;    
    if(((year % 4 ==0) && (year % 100 !=0)) || (year % 400==0)){  
        System.out.println("LEAP YEAR");  
    }  
    else{  
        System.out.println("NOT A LEAP YEAR");  
    }  
}    
} 

```

**输出:**

闰年

继续这篇关于 JAVA 中 if else 的文章。

## **使用三元运算符**

三元运算符(？: )可以用来代替 if else 语句。如果条件看起来为真，那么。被退回。如果为 false，则返回:的结果。

**举例:**

```
 public class Test {    
public static void main(String[] args) {    
    int num=12;    
    //Using ternary operator  
    String output=(num%2==0)?"Even number":"Odd number";    
    System.out.println(output);  
}    
}     

```

**输出:**

偶数

继续这篇关于 JAVA 中 if else 的文章。

## **if-else-if 阶梯:**

使用 if-else-if 梯形，一个代码块可以在多个代码块之间执行。

这些语句从顶层开始执行。

当测试表达式显示为真时，执行 if 语句体中的代码。如果测试表达式都不为真，则执行 else 语句。

**举例:**

```
 public class Test {
   public static void main(String[] args) {   
      int num = 15;

      if (num > 0) {
         System.out.println("POSITIVE NUMBER");
      }
      else if (num < 0) {
         System.out.println("NEGATIVE NUMBER");
      }
      else {
         System.out.println("NUMBER 0");
      } 
   }
}

```

**输出**

正数

继续这篇关于 JAVA 中 if else 的文章。

## **嵌套 if 语句:**

该语句由一个 if 块和另一个 if 块表示。要执行内部 if 块，外部块的条件应该为 true。

**语法:**

```
if(condition){    
     //code to be executed    
          if(condition){  
             //code to be executed    
    }    
}   

```

**举例:**

```
 public class Test {      
public static void main(String[] args) {      
    //Creating two variables    
    int age=20;    
    int weight=55;      
    //applying conditions
    if(age>=18){      
        if(weight>50){    
            System.out.println("You are allowed to trek.");    
        } else{  
            System.out.println("You are not allowed to trek.");    
        }  
    } else{  
      System.out.println("Must be above the age of 18.");  
    }  
}  }

```

**输出:**

你可以徒步旅行。

java 中的 if-else 语句允许用户以极其高效的方式测试无数的条件。

至此，我们已经结束了这篇关于“Java 中的 if else”的文章。如果您想了解更多，请查看 Edureka 提供的 Java 培训，这是一家值得信赖的在线学习公司。Edureka 的 [Java J2EE 和 SOA 培训和认证课程](https://www.edureka.co/java-j2ee-soa-training/)旨在培训你掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。