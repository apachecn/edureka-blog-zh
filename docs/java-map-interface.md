# 如何用 Java 实现 Map 接口？

> 原文：<https://www.edureka.co/blog/java-map-interface>

Java 中最有趣的话题之一是 Map 接口，它代表了键和值之间的映射。在 Java 中经常被误解为[集合](https://www.edureka.co/blog/java-collections/#interface)接口的子类型。这篇关于 Java 地图接口的文章将帮助你理解和掌握地图在 [Java](https://www.edureka.co/blog/java-tutorial/) 中是如何工作的。

下面列出了本文涉及的主题:

*   [Java 地图接口](#map-inteface)
*   [地图界面特征](#map-features)
*   [Java 地图层级](#map-hierarchy)
*   [Java Map 接口中的方法](#map-methods)
*   [地图接口的实现](#map-implementation)
    *   [HashMap 类](#hashmap)
    *   [树形图类](#treemap)
    *   [LinkedHashMap 类](#linkedhashmap)

## **Java 地图接口**

***Java 中的 Map 是一个[对象](https://www.edureka.co/blog/java-object/)，它将键映射到值，并被设计用于更快的查找。数据存储在键-值对中，每个键都是唯一的。每个键映射到一个值，因此命名为 map。这些键值对被称为映射条目。***

![Maps in Java - Java Map Interface - Edureka](img/15e091b64bd7f3a9a2b3c4fe366ec918.png)

、 [java.util.Map](https://docs.oracle.com/javase/8/docs/api/java/util/Map.html) 中的 是一个[接口](https://www.edureka.co/blog/java-collections/#interface)，它包含了基于键的元素插入、移除和检索的方法签名。有了这样的方法，它就是一个用于键值关联映射的完美工具，比如字典。

## **地图界面特征**

*   地图接口不是集合接口的真正子类型，因此，它的特征和行为不同于其余的集合类型。
*   它提供了三个集合视图——一组键、一组键-值映射和值的集合。
*   一个 映射 不能包含重复的键，每个键最多只能映射到一个值。有些实现允许空键和空值 *(* *HashMap 和 linked HashMap**)*，但有些不允许 *(* *TreeMap)。*
*   Map 接口不保证映射的顺序，但是，它取决于实现。例如， *HashMap* 不能保证映射的顺序，但是 *TreeMap* 可以。
*   AbstractMap 类提供了 Java Map 接口的框架实现，大多数 Map concrete [类](https://www.edureka.co/blog/java-objects-and-classes/)扩展了 AbstractMap 类并实现了所需的方法。

现在您已经了解了 Java 中的 Map 接口是什么，让我们继续检查 Java Map 的层次结构。

## **Java 地图层级**

java 中实现 Map 的接口有两个:Map 和  SortedMap。而 Java 中流行的 Map 实现类有 *HashMap、TreeMap* 和  *LinkedHashMap。*Java 映射的层次结构如下所示:

![Map Interface - Java Map Interface - Edureka](img/ea3492cbd463448d8402ae9cf5cac56f.png)

在我们检查上面提到的 Java Map 接口的三个实现类之前，这里有一些你在使用 Map 时会遇到的常用方法。

## **Java Map 接口中的方法**

| **方法** | **描述** |
| public put(对象键，对象值) | 该方法在地图中插入一个条目 |
| 公共 void putAll(地图地图) | 该方法将指定的地图插入到该地图中 |
| 公共对象删除(对象键) | 用于删除指定键的条目 |
| public Set keySet() | 返回包含所有键的集合视图 |
| public Set entrySet() | 返回包含所有键和值的集合视图 |
| void clear() | 用于重置地图 |
| public void putIfAbsent(K key，V value) | 只有在尚未指定的情况下，才在映射中插入带有指定键的指定值 |
| 公共对象 get(对象键) | 返回指定键的值 |
| public boolean contains key | 用于从该地图中搜索指定的键 |

## **实施地图**

有几个实现 Java Map 的[类](https://www.edureka.co/blog/java-tutorial/#obj)，但是三个主要的通用实现是 HashMap、TreeMap 和 LinkedHashMap。让我们通过一个示例[程序来看看每个实现的特征和行为。](https://www.edureka.co/blog/java-programs/)

### **HashMap 类**

实现 Java Map 接口的最常见的类是 HashMap。它是基于散列表的 Map 接口实现。它实现了所有的映射操作 ，并允许空值和一个空键。此外，该类不维护其元素之间的任何顺序。下面是一个演示 HashMap 类的示例程序。

```
package MyPackage;

import java.util.*; 

class HashMapExample {

    public static void main(String[] args) {
	        Map< String, Integer> courses = new HashMap< String,Integer>();

	        // Add some courses.
	        courses.put("Java Courses", new Integer(6));
	        courses.put("Cloud Courses", new Integer(7));
	        courses.put("Programming Courses", new Integer(5));
	        courses.put("Data Science Courses", new Integer(2));

	        System.out.println("Total courses: " + courses.size());    

	        Set< Map.Entry< String,Integer> > st = courses.entrySet();    

	        for (Map.Entry< String,Integer> me :st) 
	        { 
	            System.out.print(me.getKey()+":"); 
	            System.out.println(me.getValue()); 
	        } 
	        System.out.println();

	        String searchKey = "Java Courses";
	        if (courses.containsKey(searchKey))
	            System.out.println("Found total " + courses.get(searchKey) + " " + searchKey);

	    }
	}

```

**输出**

```
Total courses: 4
Cloud Courses:7
Programming Courses:5
Data Science Courses:2
Java Courses:6

Found total 6 Java Courses

```

在上面的程序中，我使用了很多表中提到的方法。首先， *put()* 方法在 map 中插入 4 个条目，下一步中的 *size()* 方法显示 map 的大小(总的键-值对)。之后，在下一步中， *entrySet()* 方法返回所有的键值对。该程序还展示了如何利用 *get()* 方法来使用相关的键搜索一个值。

让我们转到实现 Java Map 接口的下一个类——TreeMap。

### **树形图类**

这个实现使用红黑树作为底层的数据结构。树形图根据其关键字的自然顺序进行排序，或者根据创建时提供的比较器进行排序。这个实现不允许空值，但是保持了元素的顺序。下面是一个演示 TreeMap 类的示例程序。

```
package MyPackage;

import java.util.*; 

class TreeMapEx{

    public static void main(String[] args) {
	        Map< String, Integer> courses = new TreeMap< String,Integer>();

	        // Add some courses.
	        courses.put("Java Courses", new Integer(3));
	        courses.put("AWS Courses", new Integer(7));
	        courses.put("Programming Courses", new Integer(8));
	        courses.put("Data Science Courses", new Integer(2));

	        System.out.println("Total courses: " + courses.size());    

	        Set< Map.Entry< String,Integer> > st = courses.entrySet(); 
	        for (Map.Entry< String,Integer> me :st) 
	        { 
	            System.out.print(me.getKey()+":"); 
	            System.out.println(me.getValue()); 
	        } 
	        System.out.println();
    }
}

```

**输出**

```
Total courses: 4
AWS Courses:7
Data Science Courses:2
Java Courses:3
Programming Courses:8
```

在输出中，map 的元素按照严格的词典顺序打印，这在前面的 HashMap 示例中没有出现。我们要讨论的下一个类是 *LinkedHashMap* 。

### **LinkedHashMap 类**

顾名思义，Java Map 接口的实现使用哈希表和链表作为底层数据结构。因此，LinkedHashMap 的顺序是可预测的，默认顺序是插入顺序。此外，还允许类似 HashMap 中的空值。下面是一个演示 TreeMap 类的示例程序。

```
package MyPackage;

import java.util.*; 

	public class LinkedHashMapExample 
	{ 
	    public static void main(String a[]) 
	    { 
	        LinkedHashMap<String, Integer> courses = 
	                       new LinkedHashMap<String, Integer>(); 
	        courses.put("Java Courses", new Integer(3));
	        courses.put("Cloud Courses", new Integer(7));
	        courses.put("Programming Courses", new Integer(8));
	        courses.put("Data Science Courses", new Integer(2));

	        // It prints the elements in same order  
	        // as they were inserted     
	        System.out.println(courses); 
	        System.out.println("Total courses: " + courses.size());  
	        System.out.println("Contains key 'Hadoop'? "+  courses.containsKey("Hadoop"));

	        System.out.println("Getting value for key 'Programming Courses': " + courses.get("Programming Courses"));
	        System.out.println("Is map empty? " + courses.isEmpty());

	        System.out.println("delete element 'Cloud Courses': " +  courses.remove("Cloud Courses")); 

	        System.out.println(courses); 
	    } 
	} 

```

**输出**

```
{Java Courses=3, Cloud Courses=7, Programming Courses=8, Data Science Courses=2}
Total courses: 4
Contains key 'Hadoop'? false
Getting value for key 'Programming Courses': 8
Is map empty? false
delete element 'Cloud Courses': 7
{Java Courses=3, Programming Courses=8, Data Science Courses=2}

```

这个示例程序非常容易理解。我已经用一些基本的方法演示了 Java 中 LinkeHashMap 的功能。就像我之前说的，除了这三个类，还有很多其他类实现了 Java Map 接口。

这篇“Java Map Interface”文章到此结束。我讲过 Java 的一个有趣的话题，就是 Java 中的 Map 接口。

***确保你尽可能多的练习，恢复你的经验。***

*查看 Edureka 提供的 [**Java 认证课程**](https://www.edureka.co/java-j2ee-training-course) ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。*

*有问题吗？请在这篇“Java Map interface”**文章的评论部分提到它，我们会尽快回复您。*