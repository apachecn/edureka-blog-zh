# Java 中三元运算符是什么，怎么用？

> 原文：<https://www.edureka.co/blog/java-ternary-operator/>

在[编程](https://www.edureka.co/blog/python-programming-language)领域，条件语句扮演着重要的角色。不管程序是简单还是复杂，程序都很有可能包含[条件语句](https://www.edureka.co/blog/loops-in-python/)。有时候我们需要广泛地使用它们，但是一遍又一遍地输入同样的东西会变得很乏味。为了克服这个问题，我们使用一个三元运算符，它可以被认为是 if-else 语句的速记技术。在这篇 java 三元运算符的文章中，我们将了解与该运算符及其用法相关的所有基本概念。

*   [Java 中的三元运算符是什么？](#whatisternaryoperatorinjava)
*   [工作:如何使用 Java 三元运算符？](#working)
*   [Java 三元运算符示例](#examples)
*   [连锁操作](#chainedoperation)

让我们开始吧。:-)

## **Java 中的三元运算符是什么？**

三元运算符有助于将几行代码转换成一行代码，这在需要多次执行小型条件运算时是最佳选择。

**举例**–

```
if (BooleanValue) {
   Greetings = "Hello!";
}
else {
   Greetings = "Bye!";
}
```

上面的语句包含 6 行，一遍又一遍地写它们是一项单调乏味的任务。大量使用 if-else 语句可能会在代码中造成“{ 0 }”的混乱。为了避免这种情况，我们使用三元运算符来简化代码，并最小化混淆的可能性。

**例题-**

```
Greetings = (BooleanValue) ? "Hello!" : "Bye!";
```

上面的表达式涉及 1 行。因此，如果我们不得不一次又一次地写条件，为了简化，我们可以使用三元运算符。

在这篇文章的下一部分，我们将讨论 Java 中三元运算符的所有组成部分。

## **工作:如何使用 Java 三元运算符？**

如果你第一次使用三元运算符，它可能看起来让人不知所措。因此，让我们打破所有的组成部分，当我们使用一个三元运算符。

```
Greetings = (BooleanValue) ? "Hello!" : "Bye!";
```

从上面的陈述中，我们可以看到三元运算符共有 3 个组成部分，我们将逐一介绍。

**boolean value**–这是一个变量，它的值是一个布尔值，这意味着它要么是真，要么是假。它不一定是一个变量，它可以是一个表达式，其值在求值后应该为真或假。你可以认为它类似于我们在使用 if 语句时提到的条件。

“你好”——就在“？”，‘你好’被放置。它基本上意味着如果' BoleanValue '变量的值为' true '，' Hello！'如果' BoleanValue '变量的值为' false '，' bye！'，则将被赋给' Greetings '变量将被赋给“Greetings”变量。

**语法:**

```
Variablename = (Condition) ? the value assigned if 'true' is returned: the value assigned if 'true' is returned;
```

## **Java 三元运算符示例**

至此，我们知道了如何使用三元运算符。现在，让我们看一些例子，这些例子将为我们提供不同用例及其局限性的见解。

让我们从一个在理解[条件语句](https://www.edureka.co/blog/python-programming-language#FlowControl)的概念时最常用的经典例子开始。

```
public class Ternaryy {
   public static void main(String[] args) {
       int Raining = 1;
       String Whether;

       Whether = (Raining == 1) ? "don't forget your umbrella" : "it's a sunny day";
       System.out.println(" Today " + Whether);
   }
}
```

**输出-** 今天别忘了你的伞

现在，让我们再看一个例子:

```
public class Ternaryy {
   public static void main(String[] args) {
       String Toss = "Heads";
       String Result;

       Result = (Toss == "Heads") ? "You won the toss" : "Sorry, better luck nex time";
       System.out.println(Result);
   }
}
```

****输出-**** 掷硬币你赢了

**使用三元运算符时需要记住的要点是:**

*   在理解了三元运算符的工作原理之后，你可能会想到把它作为处理条件的首选，但是这里的问题是，随着条件开始变得复杂，代码变得不那么可读，这在[编程](https://www.edureka.co/blog/python-programming-language)时不是一个好习惯。当表达简短时，总是可以使用它。

*   三元运算符求值后返回的值应存储在与返回值类型相同的变量中。否则你将面临一个错误，这种错误很小，因此很难发现。

## **连锁操作**

链式操作也称为嵌套操作。它们类似于嵌套的 [if-else 语句](https://www.edureka.co/blog/if-else-in-python/)，但是代码行更少。

```
public class Ternaryy {
   public static void main(String[] args) {

       String coffeeOrder = "Piccolo Latte";
       if (coffeeOrder == "Espresso" ) {
           System.out.println("would you like whipped cream on the top");
       } else if (coffeeOrder == "Piccolo Latte") {
           System.out.println("25ml or 30ml");
       } else if (coffeeOrder == "Short Macchiato") {
           System.out.println("Short or long");
       } else {
           System.out.println("Hello, we were unable to process your order");

       }
   }
}
```

**输出-**

25 毫升或 30 毫升

上面的操作很简单，但是很费时间。让我们使用三元运算符来简化我们的工作。

```
public class Ternaryy {
   public static void main(String[] args) {

       String coffeeOrder = "Piccolo Latte";
        String FinalOrder = (coffeeOrder == "Espresso") ? " would you like whipped cream on the top" : (coffeeOrder == "Piccolo Latte") ? "25ml or 30ml" : (coffeeOrder == "Macchiato") ? "Short or long" : "Hello, we were unable to process your order";
       System.out.println(FinalOrder);
   }
}
```

差别非常明显。我们的第二个解决方案用更少的代码行实现了这个目的。这是你的选择，在 if-else 和三元运算符之间选择时，根据情况明智地选择。

这是 Java 文章中三元运算符的结尾。我希望你们清楚我上面讨论的每一个方面。

*既然您已经了解了 Java 的基础知识，请查看 Edureka 提供的  [**Java 培训**](https://www.edureka.co/java-j2ee-training-course)* *，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

有问题要问我们吗？请在这个“Java 中的三元运算符”博客的评论部分提到它，我们会尽快回复您。