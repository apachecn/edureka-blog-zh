# Java 中的树形图简介及实例

> 原文：<https://www.edureka.co/blog/treemap-in-java/>

用 Java 实现 Map 接口是一项非常重要的任务。为此，我们有了**树形图**和**散列表**。在本文中，我们将按照以下顺序关注 [Java](https://www.edureka.co/blog/java-tutorial/) 中的树形图:

*   [Java 中的树形图是什么？](#what)
*   [树形图的特征](#features)
*   [树形图中的构造函数](#constructors)
*   [树形图中的方法](#methods)
*   [Java 中的树形图示例](#example)

## **Java 中的树形图是什么？**

Java 中的树形图用于实现地图接口和导航地图以及抽象类。映射根据其键的自然顺序进行排序，或者根据使用的构造函数，通过在创建映射时提供的比较器进行排序。这被证明是排序和存储键值对的有效方式。

树映射维护的存储顺序必须与 equals 保持一致，就像任何其他排序的映射一样，与显式比较器无关。树形图的实现是不同步的，如果一个图被多个线程同时访问，并且至少有一个线程在结构上修改了这个图，那么它必须在外部同步。

## **树形图的特征**

*   这个类是 Java 集合框架的成员。

*   该类实现了地图接口，包括 NavigableMap、SortedMap 和 extends AbstractMap

*   Java 中的 TreeMap 不允许空键(如 Map ),因此会引发 NullPointerException。但是，多个空值可以与不同的键相关联。

*   所有地图。由该类中的方法及其视图返回的条目对表示映射在产生时的快照。

*   它们不支持 Entry.setValue 方法。

## **需要记住的要点**

1.  Java TreeMap 除了实现 Map 接口，还实现了 NavigableMap，间接实现了 SortedMap 接口。TreeMap 还扩展了 AbstractMap 类。

2.  树形图条目按其关键字的自然顺序排序。它还提供了一个构造函数来提供用于排序的比较器。因此，如果您使用任何类作为键，请确保它实现了自然排序的可比接口。查看 java 集合面试问题，了解这些方法的重要性。

3.  Java TreeMap 实现为 containsKey、get、put 和 remove 操作提供了有保证的 log(n)时间开销。

4.  TreeMap 不同步，因此不是线程安全的。对于多线程环境，可以使用 collections . synchronizedsortedmap 方法获得包装的 synchronized。

5.  获取键集和值的 TreeMap 方法返回迭代器，本质上是快速失败的，所以任何并发修改都会抛出 ConcurrentModificationException。

6.  java 中的 TreeMap 不允许空键，但是，你可以有多个空值与不同的键相关联。

## **树形图中的构造函数**

| **构造器** | **描述** |
| **树图()** | **构造一个空的树形图，将使用其键的自然顺序进行排序。** |
| **树形图(比较器比较)** | **构建一个空的基于树的映射，该映射将使用比较器 comp 进行排序。** |
| **树图(地图 m)** | **用 m 中的条目初始化一个树形图，这些条目将使用关键字的自然顺序进行排序。** |
| **树图(黑色文件夹 sm)** | **用来自 SortedMap sm 的条目初始化一个树形图，这些条目将按照与 sm 相同的顺序排序。** |

## **树形图中的方法**

| **方法** | **描述** |
| **void clear()** | 从该树图中删除所有映射。 |
| **对象克隆()** | 返回该树形图实例的浅层副本。 |
| **比较器比较器()** | 返回用于排序此映射的比较器，如果此映射使用其键的自然顺序，则返回 null。 |
| **布尔包含键(对象键)** | 如果此映射包含指定键的映射，则返回 true。 |
| **布尔包含值(对象值)** | 如果此映射将一个或多个键映射到指定值，则返回 true。 |
| **设置 entrySet()** | 返回此映射中包含的映射的集合视图。 |
| **对象 firstKey()** | 返回当前排序图中的第一个(最低的)键。 |
| **对象获取(对象键)** | 返回该映射将指定键映射到的值。 |
| **sorted map headMap(Object toKey)** | 返回该地图中键严格小于 toKey 的部分的视图。 |
| **设置密钥集()** | 返回包含在此映射中的键的集合视图。 |
| **Object lastKey()** | 返回当前排序后的地图中的最后一个(最高的)键。 |
| **对象放置(对象键，对象值)** | 将指定值与该映射中的指定键相关联。 |
| **void putAll(地图地图)** | 将指定映射中的所有映射复制到该映射。 |
| **物体移除(物体键)** | 如果存在，从该树形图中删除该键的映射。 |
| **int size()** | 返回此映射中键值映射的数量。 |
| **sorted map subMap(Object from key，Object toKey)** | 返回该地图部分的视图，其键的范围从包含键到不包含键。 |
| **sorted map tail map(Object from key)** | 返回此地图中键大于或等于 fromKey 的部分的视图。 |
| **集合值()** | 返回此映射中包含的值的集合视图。 |

## **Java 中的树形图示例**

```
import java.util.TreeMap;

public class TreeMapMain {

	public static void main(String args[])
	{
		// TreeMap with Country as key and capital as value
		// TreeMap stores elements in natural ordering of keys.
		TreeMap<String,String> countryCapitalMap=new TreeMap<String,String>();
		countryCapitalMap.put("India","Delhi");
		countryCapitalMap.put("Japan","Tokyo");
		countryCapitalMap.put("France","Paris");
		countryCapitalMap.put("Russia","Moscow");

		System.out.println("-----------------------------");
		// Iterating TreeMap Using keySet() and for each loop
		System.out.println("Iterating TreeMap Using keySet() and for each loop");
		for (String countryKey:countryCapitalMap.keySet()) {
			System.out.println("Country:"+ countryKey +" and  Capital:"+countryCapitalMap.get(countryKey));

		}
		System.out.println("-----------------------------");
	}

}
```

**输出:**

![Output-TreeMap](img/856353c33196b3b0026c45447e8dc895.png)

至此，我们结束了这篇 Java 文章中的树形图。C *查看 Edureka 提供的  [**Java 培训**](https://www.edureka.co/java-j2ee-soa-training)* *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 25 万名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

有问题要问我们吗？请在这个“Java 树形图”博客的评论部分提到它，我们会尽快回复您。