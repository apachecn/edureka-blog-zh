# Java HashMap——知道如何用 Java 实现 HashMap

> 原文：<https://www.edureka.co/blog/java-hashmap/>

**HashMap** 是 Java 中基于映射的集合类，用于在键&值对中存储数据。它还有助于在 Java 中实现 Map 接口。通过这篇文章的媒介，我将告诉你如何实现 [Java](https://www.edureka.co/blog/java-tutorial/) HashMap。

本文涵盖以下主题:

*   什么是 Java 散列表？
*   [Hashmap 的特性](#FeaturesofHashmap)
*   [Java HashMap 的性能](#PerformanceofJavaHashMap)
*   [Java 中 HashMap 的构造函数](#ConstructorsofHashMapinJava)
*   [HashMap 实现](#HashMapImplementation)

## 什么是 Java 散列表？

**HashMap** 从 Java 1.2 开始基本上就是 [Java 的集合](https://www.edureka.co/blog/java-collections/)的一部分。它提供了 Java 中 Map [接口的基本实现。它通常以(键，值)的形式成对存储数据。要访问 HashMap 中的值，必须知道它的键。](https://www.edureka.co/blog/java-interface/)

它之所以被命名为 HashMap，是因为它使用了一种叫做哈希的技术。哈希是通过保持[字符串](https://www.edureka.co/blog/java-string/)的值不变来将较大的字符串转换为较小的字符串的过程。产生的压缩值有助于索引和更快的搜索。

有了这些，现在让我们了解一下 Java 中 HashMap 的各种特性。

## **HashMap 的特性**

*   Hash Map 是 Java 中 util [包的一部分。](https://www.edureka.co/blog/packages-in-java/)

*   HashMap 扩展了一个[抽象类](https://www.edureka.co/blog/abstract-classes-in-java/) AbstractMap，它也提供了一个不完整的 Map 接口实现。

*   它还实现了 Cloneable 和 [Serializable](https://www.edureka.co/blog/serialization-in-java/) 上面定义中的 K 和 V 分别代表 Key 和值。

*   HashMap 不允许重复的键，但允许重复的值。这意味着一个键不能包含一个以上的值，但是一个以上的键可以包含一个值。

*   HashMap 只允许空键，但是可以使用多个空值。

*   这个类不保证地图的顺序；特别是，它不能保证顺序会随时间保持不变。它大致类似于哈希表，但是不同步。

现在您已经知道了什么是 Hashmap 及其各种特性，让我们进一步了解 Java Hashmap 的性能。

## **Java HashMap 的性能**

性能主要取决于两个参数:

1.  **初始容量**:容量就是桶的数量，而*初始容量*是 HashMap 实例创建时的容量。
2.  **负载系数:***负载系数* 是衡量何时应该进行重散列的指标。重新散列是一个增加容量的过程。在 HashMap 中，容量是 2 的倍数。Load Factor 也是一个度量标准，用来决定在重新散列之前允许填充散列表的哪一部分。当散列表中的条目数量增加时，当前容量和负载系数容量的乘积也会增加。这意味着重新散列已经完成。

***注意** : 如果初始容量保持较高，则永远不会进行再散列。但是保持较高的值会增加迭代的时间复杂度。所以应该非常巧妙的选择，增加性能。设置初始容量时，应考虑值的预期数量。最通常优选的负载因子值是 0.75，这在时间和空间成本之间提供了很好的交易。负载系数的值在 0 和 1 之间变化。*

## **HashMap 中的构造函数**

HashMap 提供了四个[构造函数](https://www.edureka.co/blog/constructor-in-java/)，每个构造函数的[访问修饰符](https://www.edureka.co/blog/access-modifiers-in-java/)都是公共的:

| **构造函数** | **描述** |
| **1\. HashMap()** | 它是创建 HashMap 实例的默认构造函数，初始容量为 16，负载系数为 0.75。 |
| **2。HashMap(int 初始容量)** | 这用于创建一个具有指定初始容量和负载系数 0.75 的 HashMap 实例 |
| **3。HashMap(int 初始容量，浮点加载因子)** | 它创建一个具有指定初始容量和指定负载系数的 HashMap 实例。 |
| **4\. HashMap(Map map)** | 它使用与指定映射相同的映射创建 HashMap 的实例。 |

有了这些，现在让我们看看如何在 [Java](https://docs.oracle.com/javase/tutorial/) 中实现 HashMap。

## **HashMap 实现**

下面的程序说明了如何用 Java 实现 HashMap。

```
package Edureka;

//Java program to illustrate
//Java.util.HashMap
import java.util.HashMap;
import java.util.Map;

public class Hashmap{
public static void main(String[] args){
HashMa<String, Integer> map = new HashMap<>();
print(map);
map.put("abc", 10);
map.put("mno", 30);
map.put("xyz", 20);

System.out.println("Size of map is" + map.size());

print(map);
if (map.containsKey("mno"))
{
Integer a = map.get("mno");
System.out.println("value for key \"mno\" is:- " + a);
}

map.clear();
print(map);
}

public static void print(Map<String, Integer> map){
if (map.isEmpty()){
System.out.println("map is empty");
}
else{
System.out.println(map);
}
}
}
```

在执行 HashMap 程序时，输出如下:

```
map is empty
Size of map is:- 3
{abc=10, xyz=20, mno=30}
value for key "abc" is:- 10
map is empty
```

这就把我们带到了 [Java](https://www.edureka.co/blog/advanced-java-tutorial) HashMap 文章的结尾。我希望你发现它信息丰富，并帮助你理解基本原理。

*查看 Edureka 提供的 **[Java 认证培训](https://www.edureka.co/java-j2ee-soa-training)** ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。该课程旨在为您提供 Java 编程的开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

*有问题吗？请在这篇“Java 散列表*”文章*的评论部分提到它，我们会尽快回复您。*