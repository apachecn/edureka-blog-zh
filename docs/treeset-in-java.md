# 如何用 Java 实现 Treeset？

> 原文：<https://www.edureka.co/blog/treeset-in-java/>

我们都知道集合在任何 java 应用程序中都扮演着重要的角色。它提供了各种类和接口，这些类和接口进一步提供了它们自己的子类和实现。Java 中的 Treeset 就是集合的一部分，它自然地以升序存储数据，不允许任何重复。让我们详细了解一下什么是 treeset，

本文将涉及以下几点:

*   [树集](#Treeset)
*   [树集类](#TreesetClass)
*   [树集方法](#TreesetMethods)
*   [树集函数示例程序](#ExampleprogramofTreesetfunctions)

继续关于 Treeset 的这篇文章

## **Java 中的 Treeset**

```
Set<String> syncTreeSet = Collections.synchronizedSet(syncTreeSet);
```

树集类也不允许任何空值。现在让我们看一个例子/

```
import java.util.*;  
class TreeSet1{  
public static void main(String args[]){  
TreeSet<String> treeSet=new TreeSet<String>();  
treeSet.add("Java");  
treeSet.add("Python");  
treeSet.add("Cobol");  
Iterator<String> itr=treeSet.iterator();  
while(itr.hasNext()){  
System.out.println(itr.next());  
} 
}  
}  

```

**输出:** Cobol

Java

Python

由于它是一个有序的类，输出如上所示。

继续关于 Treeset 的这篇文章

## **树集函数**

现在让我们看看 treeset 类提供的构造函数。它提供了四个构造函数。

| **构造者** | **描述** |
| TreeSet( ) | 创建一个默认排序的空树集。 |
| 树集(集合 c) | 用集合 c 的元素创建一个树集 |
| 树集(比较器组件) | 创建一个具有给定比较器顺序的空树集，用于存储元素时对其进行排序。 |
| 树集 | 用排序后的集合 s. 的元素创建一个树集 |

继续关于 Treeset 的这篇文章

## **树集方法**

除了这些构造函数，treeset 还提供了许多方法，如下所示。

| **法** | **描述** |
| void add(对象 o) | 添加一个元素到树集中，如果它还不存在的话 |
| 布尔加法(集合 c) | 将给定集合的所有元素添加到树集 |
| 对象克隆() | 返回该树集实例的浅层副本，即复制集 |
| 对象优先() | 返回存储在树集中的第一个(最低的)元素 |
| Object last() | 返回存储在树集中的最后一个(最高的)元素 |
| 布尔型 isEmpty() | 如果树集为空(其中没有元素)则返回 true |
| 布尔包含(对象 o) | 如果树集包含给定元素，则返回 true |
| void clear() | 这将删除所有元素 |
| 排序设置耳机(Object toElement) | 返回小于给定元素的所有 treeset 元素 |
| SortedSettailSet(Object from element) | 返回大于或等于给定元素的所有 treeset 元素 |
| sorted set subset(Object from element，ObjecttoElement) | 返回给定范围内的所有元素(包括 fromElement，不包括 toElement) |
| int size() | 返回树集的大小(存在的元素数) |
| 迭代器迭代器() | 返回一个迭代器来迭代集合中的元素 |
| 布尔删除(对象 o) | 删除指定的元素(如果存在的话) |
| SortedSet descendingSet() | 返回给定集合的逆序 |
| pollFirst() | 从集合中删除第一个(最低的)元素 |
| pollLast() | 从集合中删除最后一个(最大的)元素 |
| 降低(E e) | 返回集合中严格小于给定元素的最大元素，如果该元素不存在，则返回空值 |
| 更高(E e) | 返回集合中严格大于给定元素的最小元素，如果该元素不存在，则返回空值 |
| 比较器比较器() | 返回用于对集合中的元素进行排序的比较器，如果没有使用这样的比较器，则返回 null，并使用自然排序进行排序 |
| spliteratorspliterator() | 在元素上创建后期绑定和故障快速拆分器 |
| 楼层(E e) | 返回集合中指定元素的相等或最近的最小元素，或 null 没有这样的元素 |
| 天花板(E e) | 返回集合中指定元素的最大或最小元素，或 null 没有这样的元素 |
| 迭代器 descendingiterator() | 用于按降序迭代元素。 |

继续关于 Treeset 的这篇文章

## **Java 中的 Treeset 程序**

现在让我们看一个带有这些功能的示例程序。

```
importjava.util.Iterator;
importjava.util.TreeSet;
public class Sample {
publicstaticvoid main(String args[]){  
TreeSet<String>ol=newTreeSet<String>();  
ol.add("India");  
ol.add("Australia");  
ol.add("India");  
ol.add("Canada"); 
ol.add("Nepal");
ol.add("China");	
Iterator itr=ol.iterator();  
while(itr.hasNext()){  
System.out.println(itr.next());  
}  	
System.out.println("Size:"+ol.size());	
itr=ol.descendingIterator();
System.out.println("Elements in reverse order");
while(itr.hasNext()){  
System.out.println(itr.next());  
}	
System.out.println("Initial Set:"+ol);  
System.out.println("Reverse Set:"+ol.descendingSet());  
System.out.println("Head Set:"+ol.headSet("India"));  
System.out.println("SubSet:"+ol.subSet("China", "Nepal"));  
System.out.println("TailSet:"+ol.tailSet("Canada"));	
System.out.println("Highest Value:"+ol.pollFirst()); 
System.out.println("Lowest Value:"+ol.pollLast());
System.out.println("After poll operations:"+ol);
ol.remove("China");
System.out.println("After a removal:"+ol);
ol.add("Australia"); 
ol.add("Netherlands"); 
if(ol.contains("India")){
System.out.println("the given set contains India");
}	
ol.clear();
System.out.println("set after clear operation:"+ol);	
}
}

```

**输出:**

澳大利亚

加拿大

中国

印度

尼泊尔

尺寸:5

逆序元素

尼泊尔

印度

中国

加拿大

澳大利亚

初始设置:[澳大利亚、加拿大、中国、印度、尼泊尔]

反组:【尼泊尔、印度、中国、加拿大、澳大利亚】

耳机:[澳大利亚、加拿大、中国]

子集:[中国、印度]

tail set:[加拿大、中国、印度、尼泊尔]

最高值:澳大利亚

最低值:尼泊尔

投票操作后:[加拿大、中国、印度]

移除后:【加拿大、印度】

给定集合包含印度

清零操作后设置:【】

关于“Java 中的树集”的这篇文章到此结束。如果您想了解更多，请查看 Edureka 提供的 Java 培训，这是一家值得信赖的在线学习公司。Edureka 的 [Java J2EE 和 SOA 培训和认证](https://www.edureka.co/java-j2ee-soa-training/)课程旨在培训你掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。