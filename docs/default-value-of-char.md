# Java 中 Char 的默认值是多少？

> 原文：<https://www.edureka.co/blog/default-value-of-char/>

Java 是使用最广泛的编程语言之一。 学习 Java 可以帮助你理解编程的基础知识以及 [面向对象编程](https://www.edureka.co/blog/object-oriented-programming/) 概念。在 Java 中，char 的**默认值是“u 0000”**。我们来详细了解一下这个概念 。

本文涵盖以下主题:

*   [为什么知道数据类型的默认值很重要？](#Whyknowingthedefaultvalueofdatatypesisimportant?)T3T5
*   [Char 的默认值](#TheDefaultvalueofChar)
*   [验证结论](#VerifyingtheConclusion)
*   [理解 Unicode](#UnderstandingUnicode)

让我们开始吧。

## **为什么知道数据类型的默认值很重要？**

一些编程语言要求在使用变量之前在程序中声明变量。因此，如果您决定使用一种这样的语言，您应该熟悉不同数据类型的默认值，因为您可能不总是在程序中使用它们之前初始化变量。 当我们谈到 2019 年时，存在着大量的编程语言，从原始语言到最先进的语言。这些语言可以进一步分为以下两类:

*   静态类型语言
*   动态类型语言

现在让我们进入这些语言的细节。

## **静态类型语言**

简单地说，这些语言认真考虑了数据类型，因此被声明为严格语言。在使用静态类型语言时，需要记住的一件重要事情是，程序中使用的所有变量的数据类型都是在编译时确定的。换句话说， ***类型检查*** 发生在编译的时候。因此，程序员每次在程序中声明一个[变量](https://www.edureka.co/blog/java-tutorial/#obj)时，都需要指定[数据类型](https://www.edureka.co/blog/data-types-in-java/)。这就需要知道常用数据类型的默认值，因为我们可能不总是在声明时给变量指定自定义值。

**例子**–Java、C、C++

**静态打字示例**–

```
char  FirstVariable;
```

## **动态类型语言**

在动态类型语言中，变量的数据类型在*运行时*被检查。因此，在声明时不需要提及变量的数据类型。由于这种灵活性，存储在变量中的数据类型可以随时间而改变。在处理动态类型语言时，知道默认值并不重要。

**例子**——Python

**动态打字示例—**

```
FirstVariable = 'Hello, this is a String type variable'
print(type(FirstVariable))
a = 10
b = 20
FirstVariable = a + b
print(type(FirstVariable)
```

**输出:**

```
<class 'str'>  #Output of first print statement
<class 'int'>  #Output of second print statement
```

**注**:从上面的输出可以得出，最初，变量*的类型第一个变量*是字符串。一旦我们将一个整数值赋给同一个变量，它的类型就从字符串变成了整数。

现在，我们借助一个例子来看看 Java 中 char 的默认值是什么。

## **‘Char’的默认值**

由于 Java 是一种静态类型语言，变量应该在程序中使用之前声明。当我们声明一个变量而没有指定任何自定义初始值时，它会有一个默认值。不同数据类型的默认值是不同的。要了解更多关于各种数据类型及其默认值的信息，您可以参考此[](https://www.edureka.co/blog/data-types-in-java/)。

在知道特定数据类型的默认值之前，我们需要知道它是原语还是用户定义的数据类型。拥有这些信息有助于我们知道在哪里可以找到关于数据类型的更多信息。 由于*原始数据类型*已经由编程语言定义，我们可以在我们正在使用的编程语言提供的文档中找到更多关于它的信息。

同样，由于我们关心的是 Java 中的 **char** 的默认值，并且由于 **Char** 是一种原始数据类型，我们可以参考 Java [文档](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/datatypes.html) 。有关用户定义数据类型的更多信息，可以参考该类的开发人员提供的文档。

***Char** 字符的简称是单个 **Unicode** 字符的大小为 16 位，其中可以容纳单个值括在“”中。*

**语法:**

```
DataType Variablename = 'value';
```

**例子** :

```
char HelloWorld = 'a';
```

## **验证结论**

【char 能容纳的最小值是' **u0000** '，它是一个 Unicode 值，表示' **null** '或十进制的 0。它能容纳的最大值是'**ufff**'或**65535(含** )。最小值‘u 0000’也是 char 的默认值。你可能想知道“u0000”到底是什么意思？为什么默认值不是' a '或' b '或任何其他字符为什么只有' u000 '不要担心，我们会在这篇文章的下半部分解答你所有的疑问。首先，让我们尝试打印一个 char 类型的变量，并把这个场景分成两种情况:

第一种情况，首先声明一个 char 类型变量，并打印其值。

```
public class JavaDefaultValues {
char DeclaredVariable;  //Declaring variable 'DeclaredVariable'
public static void main(String[] args) {
JavaDefaultValues DefaultValues = new JavaDefaultValues();  //Creating object of class JavaDefaultValues
System.out.println("Value of DeclaredVariable = " + DefaultValues.DeclaredVariable);   //Printing value of DeclaredVariable
}
}

```

**输出:**

```
Value of DeclaredVariable =
```

在输出中，我们可以看到' = '后面有一个空格，表示空字符。

在第二种情况下，我们将声明一个 Char 类型的变量，并用默认值初始化它并打印它的值。

```
public static void main(String[] args) {
JavaDefaultValues DefaultValues = new JavaDefaultValues();   //Creating object of class JavaDefaultValues
char InitialisedVariable = 'u0000';    //Initialising variable 'InitialisedVariable'
System.out.println("Value of DeclaredVariable = " + DefaultValues.DeclaredVariable);   //Printing value of DeclaredVariable
System.out.println("Value of InitialisedVariable = " + InitialisedVariable);     //Printing value ppf InitialisedVariable
 }

```

**输出:**

```
Value of DeclaredVariable =
Value of InitialisedVariable =
```

从上面的输出中，我们可以看到我们收到了类似的输出。

```
System.out.println(DefaultValues.DeclaredVariable == InitialisedVariable);
```

在添加了下面一行比较两个变量的值的代码后，我们在输出屏幕上看到“ **true** ，这验证了我们的结论。

我们可以在输出屏幕上看到“ **true** ”，这是我们比较两个变量的值的语句的结果。你可以自己试试这个。下面给出了示例代码。

```
public static void main(String[] args) {
JavaDefaultValues DefaultValues = new JavaDefaultValues();     //Creating object of class JavaDefaultValues
char InitialisedVariable ='u0000';      //Initialising variable 'InitialisedVariable'
System.out.println("Value of DeclaredVariable = " + DefaultValues.DeclaredVariable);   //Printing value of DeclaredVariable
System.out.println("Value of InitialisedVariable = " + InitialisedVariable);          //Printing value ppf InitialisedVariable
System.out.println(DefaultValues.DeclaredVariable == InitialisedVariable);           //Checking if values are equal
}
}
```

至此，让我们更深入地阅读本文，理解 unicode 的概念。

## **理解 Unicode**

Unicode 是一种国际编码标准 ，用于不同的语言。在 Unicode 的帮助下，每个数字、字母或符号都被指定了一个唯一的数值，适用于不同的平台和程序。首先，我们来谈谈什么是字符编码？为什么我们需要通用编码系统？Unicode 是唯一可用的编码标准吗？ASCII 和 Unicode 有什么区别？

当在程序中使用字符、字母、文字符号时，它们不能按原样存储在数字设备中。首先，使用字符编码将其转换为数字或十六进制值。如果我的笔记本电脑使用一种编码系统，而我的另一台台式机使用不同的编码系统，那么在我的笔记本电脑上显示的文本在我的台式机上可能会有所不同。

因此，拥有一个通用的编码系统非常重要。最初， **A** 美国**S**standard**C**ode for**I**information**I**interchange**ASCII**被用作标准编码方案，但它只能覆盖 128 个字符(0–127)，其中包括英语、标点符号你可以看一下 ASCII 表 [这里](https://www.cs.cmu.edu/~pattis/15-1XX/common/handouts/ascii.html) 。这种方案不足以编码所有语言的字符。此时，Unicode 开始发挥作用。Unicode 可以包含 128，000 个字符。它为不同的字符指定十六进制值。*例如，*我们看到 char 的默认值是' **u0000** '这是一个十六进制值，当我们把这个值转换成十进制时我们得到' 0 '。类似地，char 的最大值是'**ufff**'，如果我们将这个十六进制值转换为十进制值，我们会得到 65，535，就像我们之前看到的那样。由于 char 能容纳的最大值是'**ufff**'，所以不能代表所有的 Unicode 字符。Unicode 方案涵盖了 ASCII 表中具有相同名称的所有 128 个字符。

至此，我们结束了这篇关于 Java 中 Char 的缺省值的文章。我希望这篇文章对你有所帮助。

*查看 Edureka 的 **[Java 培训](https://www.edureka.co/java-j2ee-soa-training)** ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。*

有问题要问我们吗？请在这篇“Java 中 Char 的默认值”文章的评论部分提到它，我们会尽快回复您。