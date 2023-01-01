# Java 中的字符串数组是什么，是如何工作的？

> 原文：<https://www.edureka.co/blog/string-array-in-java/>

一个 ***数组*** 是一种基础而关键的[数据结构](https://www.edureka.co/blog/data-structures-algorithms-in-java/) Java 编程语言。由于其高效和多产的本质，它被程序员高度使用。一个 ***Java 字符串数组*** 是一个保存固定数量的[字符串值](https://www.edureka.co/blog/java-string/)的对象。在本教程中，让我们更深入地了解 Java 中字符串数组的概念。

本文将涉及以下几点:

让我们开始吧。

## **什么是 Java 中的字符串数组**

你必须意识到 [Java 数组](https://www.edureka.co/blog/string-array-in-java/)，它是一个包含相似数据类型元素的对象。此外，它们存储在连续的内存位置。另一方面，字符串是一个字符序列。它被认为是不可变的对象，即值不能改变。java 字符串数组以同样的方式工作。字符串数组用于存储固定数量的[字符串](https://www.edureka.co/blog/java-string/)。

现在，我们来看看 Java 字符串数组的实现。

## **如何在 Java 中声明字符串数组**

为了实现，确保你已经安装了 Java。字符串数组由以下方法声明:

```

String[] stringArray1 //declaring without size
String[] stringArray2 = new String[2]; //declaring with size

```

字符串数组也可以被声明为 **String strArray[]** ，但是前面提到的方法是更受欢迎和推荐的。注意 strArray1 的值是 null，而 strArray2 的值是[null，null]。

现在让我们继续学习如何初始化一个字符串数组，

## 在 Java 中初始化字符串数组

可以使用以下方法初始化字符串数组:

```

//inline initialization
String[] stringArray1 = new String[] {"R","S","T"};
String[] stringArray2 = {"R","S","T"};
//initialization after declaration
String[] stringArray3 = new String[3];
stringArray3[0] = "R";
stringArray3[1] = "S";
stringArray3[2] = "T";

```

上面指定的所有三个数组都具有相同的值。

由于 stringArray3 中只有 3 个元素，索引从 0 开始，所以最后一个索引是 3。我们还可以使用公式 ***(数组长度–1)***来确定索引的值。访问大于 2 的索引时，将引发异常。

**举例:**

```

String[] stringArray3 = new String[3];
stringArray3[3] = "U";

```

这将引发 Java . lang . arrayindexoutofboundsexception。

字符串数组的初始化可以通过在语法中使用 new 运算符与声明一起完成:

```
<strong>String</strong>[] stringArray3 = new <strong>String</strong>[]{“R”,”S”,”T”};
```

让我们继续这篇文章的下一个主题，

## 字符串数组的大小

字符串数组的属性可以用来确定数组中元素的个数。

```
<strong>String</strong>[] stringArray3 = {“R”,”S”,”T”};
```

system . out . println(string array 3 . length)；

**输出:**

**3**

接下来在这篇 Java 中的字符串数组文章中，我们将如何在一个字符串数组中迭代

**在字符串数组中迭代**

通过使用 java for 循环或 java for each 循环来完成对字符串数组的迭代。

```

String[] strArray3 = {“R”,”S”,”T”};
//iterating all elements in the array
for (int i = 0; i < strArray3.length; i++) {
System.out.print(strArray3[i]);
}

```

代码从索引 0 开始，一直延续到长度–1，这是数组的最后一个元素。

**输出:**

稀有

S

T

我们还可以利用 Java 5 提供的增强的 for 循环:

```

//iteration by using the enhanced for loop provided by Java 5 or later
for (String str : strArray3) {
System.out.print(str);
}

```

让我们继续这篇关于 Java 中字符串数组的文章，

## 在字符串数组中搜索

如果用户想要在字符串数组中搜索特定的值，则使用 for 循环。

```

public class SearchStringArrayExample {
public static void main(String[] args) {
String[] strArray3 = { "R", "S", "T" };
boolean found = false;
int index = 0;
String s = "S";
for (int i = 0; i < strArray.length; i++) {
if(s.equals(strArray[i])) {
index = i; found = true; break;
}
}
if(found)
System.out.println(s +" found at the index "+index);
else
System.out.println(s +" not found in the array");
}
}

```

**输出:**

b 在索引 1 处找到

关键字 *break* 用于一找到元素就停止循环。

## 对字符串数组排序

为了对字符串数组中的元素进行排序，我们可以实现自己的排序算法，或者调用 Arrays 类排序方法。

```

String[] vowels = {"o","e","i","u","a"};
System.out.println("Initial array "+Arrays.toString(vowels));
Arrays.sort(vowels);
System.out.println("Array after the sort "+Arrays.toString(vowels));

```

**输出:**

初始数组:[o，e，I，u，a]

排序后的数组:[a，e，I，o，u]

必须注意的是，String 实现了 Comparable 接口，因此它适用于自然排序。

## 将字符串数组转换为字符串

出于显示目的，有时需要将字符串数组转换为字符串。我们可以使用 Arrays.toString()方法进行转换。

```

String[] strArray3 = { "R", "S", "T" };
String theString = Arrays.toString( strArray3 );
System.out.println( theString );

```

**输出:**

[R、S、T]

这些元素不仅用逗号分隔，还用方括号括起来。

用户还可以选择实现自定义行为。在以下示例中，我们将使用自定义分隔符:

```

String[] strArray3 = { "R", "S", "T" };
String delimiter = "-";
StringBuilder sb = new StringBuilder();
for ( String element : strArray3 ) {
if (sb.length() > 0) {
sb.append( delimiter );
}
sb.append( element );
}
String theString = sb.toString();
System.out.println( theString );

```

**输出:**

R-S T

上面的代码使用了不带方括号的分隔符破折号。

让我们继续 Java 文章中这个字符串数组的下一个主题，

## 将字符串数组转换为列表

字符串数组的主要缺点是它的大小是固定的。对于大小可以增长的数组，我们实现了 List。

```

String[] strArray3 = { "R", "S", "T" };
List<String> stringList = Arrays.asList( strArray3 );

```

必须注意，我们不能向 Arrays.asList 方法返回的列表中添加项目。它引发 Java . lang . unsupportedoperationexception，如下面的代码所示:

```

String[] strArray3= { "R", "S", "T" };
List<String> stringList = Arrays.asList(strArray3);
stringList.add( "U" );

```

通过将字符串数组转换为 ArrayList 可以避免引发的错误。

```

String[] strArray3 = { "R", "S", "T" };
List<String> fixedList = Arrays.asList(strArray3);
List<String> stringList = new ArrayList<String>( fixedList );
stringList.add( "U" );

```

这段代码基于 Arrays.asList 返回的值构造了一个新的 ArrayList，它不会引发异常。

## 将字符串数组转换为集合

虽然列表可以包含重复的元素，但是集合不能。为了创建本质上唯一的元素集合，Set 被证明是一种合适的数据结构。

```

String[] strArray3 = { "R", "S", "T", "T" };
List<String> stringList = Arrays.asList(strArray3);
Set<String> stringSet = new HashSet<String>( stringList );
System.out.println( "The size of the list is: " + stringList.size() );
System.out.println( "The size of the set is: " + stringSet.size() );

```

**输出:**

列表的大小是:4

集合的大小是:3

如前所述，集合只包含唯一的元素。

## **将列表转换为字符串数组**

将列表转换回字符串数组是可行的。

```

List<String> stringList = new ArrayList<String>();
stringList.add( "R" );
stringList.add( "S" );
stringList.add( "T" );
String[] stringArr = stringList.toArray( new String[] {} ); //passing the toArray method
for ( String element : stringArr ) {
System.out.println( element );
}

```

toArray 指定返回的数组的类型。

Java StringArray 包含了无数的方法，但是它被广泛使用，以获得高效的编程体验。

这样，我们就结束了这篇关于“Java 中的字符串数组”的文章。如果你想了解更多，查看由值得信赖的在线学习公司 Edureka 提供的 **[Java 认证](https://www.edureka.co/java-j2ee-training-course)** 培训。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论区提出来，我们会尽快回复你，或者你也可以参加在谢菲尔德的 [Java 培训。](https://www.edureka.co/java-j2ee-training-course-sheffield)