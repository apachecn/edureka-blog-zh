# Java 中的数组长度:关于 Java 中数组长度你需要知道的一切

> 原文：<https://www.edureka.co/blog/array-length-in-java/>

Java 中的数组可以包含多个元素，这取决于对象是如何创建的。 对于执行截然不同操作的用户来说，了解数组的长度是必不可少的。 这篇关于 [Java](https://www.edureka.co/blog/java-tutorial/) 中数组长度的文章旨在让我们熟悉获取数组长度的操作及其用法。

本文主要关注以下几点:

*   [数组长度属性:如何求数组的长度？](#ArrayLengthAttribute)
*   [在 Java 中使用数组长度搜索值](#SearchingavalueusingArrayLengthinJava)
*   [搜索数组](#SearchingforthelowestvalueinArray)中的最小值
*   [搜索数组](#SearchingforthehighestvalueinArray)中的最大值

那么让我们从这篇“Java 文章中的数组长度”开始吧，

## **数组长度属性:如何求数组的长度？**

为了获得 Java 数组长度，我们需要使用‘数组长度属性’，如下图**示例**:

```

/**
* An Example to get the Array Length is Java
*/
public class ArrayLengthJava {
public static void main(String[] args) {
String[] myArray = { "I", "Love", "Music" };
int arrayLength = myArray.length; //array length attribute
System.out.println("The length of the array is: " + arrayLength);
}
}

```

**输出**

数组的长度为:3

**必须注意的是，Java 数组对象****没有一个** ***方法*** **来获取其长度。**

很多时候，我们不知道数组对象是如何创建的。对于这样的程序，我们使用一个函数接收一个数组，并打印长度。

```

/**
* An Example to find the Java Array Length using a function
*/
public class ArrayLengthJava {
private static void printArrayLength(String[] myArray) {
if (myArray == null) //to check whether the array is empty or not
{
System.out.println("The length of the array can't be determined.");
} else {
int arrayLength = myArray.length;
System.out.println("The length of the array is: " + arrayLength);
}
}
public static void main(String[] args) {
String[] JavaArray1 = { "I", "Love", "Music" };
String[] JavaArray2 = { "R", "S" };
String[] JavaArray3 = { "1", "2", "3", "4" };
String[] JavaArray4 = { "Java" };
printArrayLength(null);
printArrayLength(JavaArray1);
printArrayLength(JavaArray2);
printArrayLength(JavaArray3);
printArrayLength(JavaArray4);
}
}

```

**输出:**

*   数组的长度无法确定。
*   数组的长度为:3
*   数组的长度为:2
*   数组的长度为:4
*   数组的长度为:1

必须注意，在访问一个空或 null 对象的长度字段时，会引发一个 NullPointerException。

## **在 Java 中使用数组长度搜索值**

数组长度有许多有用的属性，可以在编程时使用。 在下面的例子中，我们使用数组的长度来循环遍历所有的元素，并判断特定的值是否存在。

```

/**
* An Example that uses Java Array Length to check if the array contains a
* specific value.
*/
public class ArrayLengthJava {
private static boolean arrayContainsValue(String[] myArray,
String lookForValue) {
if (myArray != null) {
int arrayLength = myArray.length;
for (int i = 0; i <= arrayLength - 1; i++) {
String value = myArray[i];
if (value.equals(lookForValue)) {
return true;
}
}
}
return false;
}
public static void main(String[] args) {
String[] JavaArray = { "I", "Love", "Music" };
System.out.println(arrayContainsValue(JavaArray, "Love"));
System.out.println(arrayContainsValue(JavaArray, "Guitar"));
}
}

```

**输出:**

*   真
*   假

上面给出的程序输出的值为 true，因为数组中存在" **【爱】** ，而 **【吉他】** 是一个不存在的元素，因此输出为 false。

## **搜索数组**中的最小值

我们可以使用数组的长度来获取数组对象中的最小值。

```

public class ArrayLengthJava {
private static int minValue(int[] myArray) {
int minValue = myArray[0];
int arrayLength = myArray.length;
for (int i = 1; i <= arrayLength - 1; i++) {
int value = myArray[i];
if (value < minValue) {
minValue = value;
}
}
return minValue;
}
public static void main(String[] args) {
int[] JavaArray = { 28, 46, 69, 10 };
System.out.println("The min value in the array: "+minValue(JavaArray));
}
}

```

**输出:**

数组中的 最小值:10

## **搜索数组**中的最大值

此外，我们可以使用数组的长度来获取数组对象中的最高值。

```

public class ArrayLengthJava {
private static int maxValue(int[] myArray) {
int maxValue = myArray[0];
int arrayLength = myArray.length;
for (int i = 1; i <= arrayLength - 1; i++) {
int value = myArray[i];
if (value > maxValue) {
maxValue = value;
}
}
return maxValue;
}
public static void main(String[] args) {
int[] JavaArray = { 29, 46, 69, 10 };
System.out.println("The max value in the array: "+maxValue(JavaArray));
}
}

```

**输出:**

数组中的 最大值:69

鉴于此，我们可以得出结论，数组长度属性是一个非常通用的属性。

至此，我们已经结束了这篇关于“Java 中数组长度”的文章。如果你想了解更多，查看由 Edureka，一家值得信赖的在线学习公司提供的 **[Java 课程](https://www.edureka.co/java-j2ee-training-course)** 。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你，或者参加我们在剑桥的 [Java 培训。](https://www.edureka.co/java-j2ee-training-course-cambridge)