# Java 中如何把 Double 转换成 Int？

> 原文：<https://www.edureka.co/blog/double-to-int-in-java/>

自从我们开始理解数字以来，我们每个人都好奇于将数字从一种形式转换成另一种形式。最流行的转换之一是将一个数字从 Double 转换成 Int。但是，在一个需要转换数百个数字的环境中，手动转换几乎是不可能的。因此，我们可以写一个简单的代码[来说明如何在](https://www.edureka.co/blog/hello-world-program-in-java/) [Java](https://www.edureka.co/java-j2ee-training-course) 中将 Double 转换成 Int。因此在这篇文章中，我将讨论同样的问题，按以下顺序:

*   [将 Double 转换为 Int 的方法](#waystoconvert)
*   [使用](#convert)将 Double 转换为 Int

在我讨论  [Java](https://www.edureka.co/blog/what-is-java/) 中双精度值转换为整数的编程方式之前，我们先讨论一下 Java 提供的不同方式。

## **Java 中把 Double 转换成 Int 的方法**

众所周知，双原语包含十进制数字。在将这些值转换为整数时，会根据您选择的方法将数字四舍五入为最接近的整数，从而截断小数位数。Java 提供了以下三种将双精度值转换为整数的方法:

请参考下表，了解上述方法的要点。

| **类型转换** | **Math.round()** | **Double.intValue()** |
| 简单易用。当你的目标是去掉小数点后的数字时，就使用它。 | 该方法用于将双精度值四舍五入为最接近的整数 | 当你有一个双宾语时，就用这个词。 |
| *Example:*int 值=(int)3.89；*输出:* 3 | *Example:*int value =(int)math . round(3.89)；*输出:* 4 | *Example:*双 d = 3.89int I = d . int value()；*输出:* 3 |

既然你已经理解了这三种方法的要点，那么让我们来理解如何为其编写代码。

## **使用类型转换将 Java 中的 Double 转换为 Int**

此方法用于将 Double 值向下转换为整数。

### **语法:**

```
double var = double value; //Assign double value to the variable var
int newvar = (int)var; //Assign the converted integer value to variable newvar 

```

### **举例:**

```
package edureka;
import java.util.Scanner;
public class DoubleToIntExample {

	public static void main(String[] args) {
		 Scanner Input = new Scanner (System.in);  

		System.out.print("Enter a Number with decimal digits greater than 5 - ");
		double Number = Input.nextDouble(); 
		int IntNumber = (int)Number;		
		System.out.println("The decimal number with decimal digits greater than 5 is convereted to integer - " +IntNumber); 

		System.out.print("Enter a Number with decimal digits less than 5 - ");
		double Number1 = Input.nextDouble(); 
		int IntNumber1 = (int)Number1;
		System.out.println("The decimal number with decimal digits less than 5 is convereted to integer - " +IntNumber1); 

		System.out.print("Enter a Number with decimal digits equal to 5 - ");
		double Number2 = Input.nextDouble(); 
		int IntNumber2 = (int)Number2;
		System.out.println("The decimal number with decimal digits equal to 5 is convereted to integer - " +IntNumber2); 
	}

}

```

**输出:**

## **![Output - Convert Double to Int - Edureka](img/18f60ca3e44af6589266d9b8f939a7c9.png)**

接下来，让我们看看如何使用 math.round()方法在 Java 中将 Double 转换为 Int。

## **在 Java 中使用 Math.round()** 将 Double 转换为 Int

此方法用于将 Double 值舍入到最接近的整数。

### **语法:**

```
double var = double value; //Assign double value to the variable var
int newvar = (int)Math.round(var); //Assign the converted integer value to variable newvar

```

### **举例:**

```
package edureka;
import java.util.Scanner;
public class DoubleToIntExample {

	public static void main(String[] args) {
		 Scanner Input = new Scanner (System.in);  

		System.out.print("Enter a Number with decimal digits greater than 5 - ");
		double Number = Input.nextDouble(); 
		int IntNumber = (int)Math.round(Number);
		System.out.println("The decimal number with decimal digits greater than 5 is convereted to integer - " +IntNumber); 

		System.out.print("Enter a Number with decimal digits less than 5 - ");
		double Number1 = Input.nextDouble(); 
		int IntNumber1 = (int)Math.round(Number1);
		System.out.println("The decimal number with decimal digits less than 5 is convereted to integer - " +IntNumber1); 

		System.out.print("Enter a Number with decimal digits equal to 5 - ");
		double Number2 = Input.nextDouble(); 
		int IntNumber2 = (int)Math.round(Number2);
		System.out.println("The decimal number with decimal digits equal to 5 is convereted to integer - " +IntNumber2); 
	}

}

```

**输出:**

## **![MathRound Output - Convert Double to Int - Edureka](img/fb3ab486778e70b33bfaa79f31533546.png)**

接下来，让我们看看如何使用 Double.intValue()方法在 Java 中将 double 转换为 Int。

## **在 Java 中使用** **Double.intValue()** 将 Double 转换为 Int

当你有一个双宾语时，使用这个方法。

### **语法:**

```
double var = double value; //Assign double value to the variable var
Double newvar = new Double(var); //Double object
int var1 = newvar.intValue; //Assign the converted integer value to variable var1 

```

### **举例:**

```
package edureka;
import java.util.Scanner;
public class DoubleToIntExample {

	public static void main(String[] args) {
		 Scanner Input = new Scanner (System.in);  

		System.out.print("Enter a Number with decimal digits greater than 5 - ");
		double Number = Input.nextDouble(); 
		Double DNumber = new Double(Number);
		int IntNumber = DNumber.intValue(); 
		System.out.println("The decimal number with decimal digits greater than 5 is convereted to integer - " +IntNumber); 

		System.out.print("Enter a Number with decimal digits less than 5 - ");
		double Number1 = Input.nextDouble(); 
		Double DNumber1 = new Double(Number1);
		int IntNumber1 = DNumber1.intValue(); 
		System.out.println("The decimal number with decimal digits less than 5 is convereted to integer - " +IntNumber1); 

		System.out.print("Enter a Number with decimal digits equal to 5 - ");
		double Number2 = Input.nextDouble(); 
		Double DNumber2 = new Double(Number2);
		int IntNumber2 = DNumber2.intValue(); 
		System.out.println("The decimal number with decimal digits equal to 5 is convereted to integer - " +IntNumber2); 
	}

}

```

**输出:**

*![Output - Convert Double to Int - Edureka](img/18f60ca3e44af6589266d9b8f939a7c9.png)*

*如果你发现这篇关于“如何在 Java 中将 Double 转换成 Int？”，查看 Edureka 提供的 **[Java 培训](https://www.edureka.co/java-j2ee-training-course)** ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你在你的旅程中迈出每一步，除了这个 java 面试问题，我们还为想要成为 Java 开发人员的学生和专业人士设计了一个课程。*

有问题要问我们吗？请在这篇“如何在 Java*中将 Double 转换为 Int”的评论部分提及，我们会尽快回复您。*