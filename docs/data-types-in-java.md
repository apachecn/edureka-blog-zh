# 了解 Java 中的各种数据类型

> 原文：<https://www.edureka.co/blog/data-types-in-java/>

**数据类型** 是变量的属性，它告诉编译器或解释器程序员打算如何使用[变量](https://www.edureka.co/blog/java-tutorial/#variables)。它 定义了可以对数据进行的操作以及可以存储什么类型的值。在本文中，我将简要介绍一下 **[Java](https://www.edureka.co/blog/java-tutorial/)** 中不同的数据类型。 根据所拥有的属性，数据类型分为两组:

1.  [**原始数据类型**](#PrimitiveDataTypes)
2.  [**非原始数据类型**](#Non-PrimitiveDataTypes)

**原始数据类型:**原始数据类型是由编程语言预先定义的。变量值的大小和类型是指定的，它没有额外的方法。

**非原语数据类型** **:** 这些数据类型实际上不是由编程语言定义的，而是由程序员创建的。它们也被称为“引用变量”或“对象引用”，因为它们引用存储数据的内存位置。

现在，让我们进一步深入原始数据类型的细节。

## **原始数据类型**

Java 中的数据类型分为四个方面，分别是 **int、float、character** 和 **boolean** 。但是，一般来说，有 8 种数据类型。它们如下:

*   [**布尔**数据类型](#booleandatatype)
*   [**字节**数据类型](#bytedatatype)
*   [**字符**数据类型](#chardatatype)
*   [**短**数据类型](#shortdatatype)
*   [**int** 数据类型](#intdatatype)
*   [**长型**数据类型](#longdatatype)
*   [**浮点**数据类型](#floatdatatype)
*   [**双精度**数据类型](#doubledatatype)

您可以参考下图，了解不同的数据类型与分配给它们的内存的关系。

现在，让我们深入了解每一种数据类型。首先我会告诉你什么是布尔数据类型。

## **布尔数据类型**

布尔数据类型由一位信息组成，只能存储**真**或**假**值。该数据类型用于跟踪**真/假** **条件**。现在我们来写一个小程序，了解一下它的工作原理。

```
class booleanDataType{
public static void main(String args[]){
// Setting the values for boolean data type

boolean Java = true;
boolean Python = false;
System.out.println(Java);   // Output will be true
System.out.println(Python);  // Output will be false
}
}
```

这就是关于布尔数据类型的全部内容。我希望你能理解。现在让我们进一步了解下一种数据类型，即字节数据类型。

## **字节数据类型**

这是一个原始数据类型的例子。它是一个 8 位有符号二进制补码整数。它存储介于-128 到 127 之间的整数。字节数据类型有助于节省大量内存。现在我们来写一个小程序，了解一下它的工作原理。

```
class ByteExample {
public static void main(String[] args) {
byte n, a;
n = 127;
a=177;
System.out.println(n); // prints 127
System.out.println(a); // throws an error because it cannot store more than 127 bits
}
}
```

这就是关于字节数据类型的全部内容。现在让我们进一步理解以下数据类型，即 char。

## **字符数据类型**

该数据类型用于存储一个  **单个** 字符。该字符必须用单引号括起来，如“E”或“E”。或者，您也可以使用 ASCII 值来显示某些字符。我们举个小例子，看看效果如何。

```
char  alpha = 'J';

char a = 65, b = 66, c = 67;
System.out.println(alpha); // prints J

System.out.println(a); // Displays 65
System.out.println(b); // Displays 66
System.out.println(c); // Displays 67
```

这就是关于 char 数据类型的全部内容。我希望你能理解。现在让我们进一步理解列表中的下一个数据类型，即短数据类型。

## **短数据类型**

短数据类型在大小上大于字节，小于整数。它存储范围从-32，768 到 32767 的值。该数据类型的默认大小:2 字节。我们举个例子，了解一下短数据类型。

```
class ShortExample {
public static void main(String[] args) {
short n= 3435,
System.out.println(n); // prints the value present in n i.e. 3435
}
}
```

接下来，让我们进一步看看下一种数据类型，即 int 数据类型

## **int 数据类型**

该数据类型可以存储从-2147483648 到 2147483647 的整数。通常，当你用数值创建[变量](https://www.edureka.co/blog/java-tutorial/#variables)时，int 是首选的数据类型。

**例如:**

```
int num = 5464564;
System.out.println(num); // prints 5464564

```

理解了这一点，现在让我们看看列表中的下一个数据类型是什么。

## **长数据类型**

该数据类型是 64 位二进制补码整数。默认情况下，long 数据类型的大小为 64 位，其值的范围为-2 <sup>63</sup> 到 2 <sup>63</sup> -1。

**例如:**

```
long num = 15000000000L;
System.out.println(num); // prints 15000000000

```

以上都是关于长数据类型的。现在我们来看看浮动数据类型。

## **浮点数据类型**

当你需要一个带小数的数字时，比如 8.88 或 3.14515，你应该使用浮点类型。

### **浮点数据类型**

此数据类型可以存储从 3.4e 038 到 3.4e+038 的分数。请注意，该值应以“f”结尾。让我们举一个小例子，详细了解一下这种数据类型。

```
float num =67;
System.out.println(num); // prints the floating number value 
```

这就是你使用浮点数据类型的方法。现在让我们看看另一种浮点数据类型，即 double。

### **双精度数据类型**

double 数据类型可以存储从 1.7e 308 到 1.7e+308 的分数。请注意，该值应以“d”结尾:

```
double num = 79.678d;
System.out.println(num); // prints double value 
```

这都是关于 Double 数据类型的，这就把我们带到了原始数据类型的结尾。现在让我们弄清楚原始数据类型和非原始数据类型之间的区别。

## **非原始数据类型**

非原始数据类型引用对象，因此它们被称为  **引用类型。**非原语类型的例子包括字符串、数组、类、接口等。下图描述了各种非原始数据类型。

![Non Primitive data types - Data types in Java - Edureka](img/81b203c5608da5f1f164bafbae9fa9bb.png)

现在让我们简单地理解一下这些非原始数据类型。

**字符串:**String是一个字符序列。但是在 Java 中，字符串是表示一系列字符的对象。 *java.lang.String* 类用于创建 String 对象。如果你想了解更多关于 Java 字符串的知识，可以参考这篇关于 Java 中[字符串的文章。](https://www.edureka.co/blog/java-string/)

**数组:**Java 中的数组是作为对象在 Java 中实现的同构数据结构。数组存储一个或多个特定数据类型的值，并提供索引访问来存储这些值。数组中的特定元素通过其索引来访问。如果你想详细了解数组，那么请查看这篇关于 [Java 数组](https://www.edureka.co/blog/java-array/)的文章。

**类:**Java 中的[类是一个包含你所有数据的蓝图。一个类包含描述对象行为的字段(变量)和方法。](https://www.edureka.co/blog/java-tutorial/#obj)

**接口:** 像一个类，一个 *接口* 可以有方法和变量，但是 [*接口*](https://www.edureka.co/blog/java-collections/#interface) 中声明的方法默认是抽象的(只有方法签名，没有体)。

这就是所有关于非原始数据类型的内容。现在让我们来理解原始数据类型和非原始数据类型的区别。

### **原始和非原始数据类型的区别**

**原语** 和  **非原语** 数据类型的区别如下:

*   原语类型是在 [Java](https://www.edureka.co/blog/what-is-java/) 中预定义的。非基本类型是由程序员创建的，不是由 Java 定义的。
*   非基元类型可以用来调用方法来执行某些操作，而基元类型则不能。
*   基本类型总是有一个值，而非基本类型可以为空。
*   基本类型以小写字母开头，而非基本类型以大写字母开头。
*   基本类型的大小取决于数据类型，而非基本类型的大小都相同。

这就把我们带到了关于 Java 中数据类型的文章的结尾。我希望你发现它信息丰富。

如果你刚刚开始，那么看看这篇 Java 教程，了解基本的 Java 概念。

[https://www.youtube.com/embed/iGGgxnJCNRM](https://www.youtube.com/embed/iGGgxnJCNRM)

*查看 Edureka 提供的 [**Java 认证**](https://www.edureka.co/java-j2ee-training-course) 培训，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。*

有问题要问我们吗？请在这篇“Java 中的数据类型”文章的评论部分提到它，我们会尽快回复您，或者您也可以参加在瓦拉纳西举办的 [Java 培训。](https://www.edureka.co/java-j2ee-training-course-varanasi)