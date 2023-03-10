# Java 中的集合:知道如何使用 Java 集合接口

> 原文：<https://www.edureka.co/blog/sets-in-java/>

Java 集合框架包含许多接口，其中之一是 Set 接口。本文将为您详细介绍 [Java](https://www.edureka.co/blog/java-tutorial/) 中的集合。以下是本文将涉及的要点:

*   [在 Java 中设置](#setsinjava)
*   [如何创建集合？](#creatingaset)
*   [Set Methods](#setmethods)
*   [集合上的基本运算](#setoperations)

## **在 Java 中设置**

集合被定义为无序元素的集合；其中不能存储重复值。它扩展了集合，因此集合接口中的所有方法都可以在集合接口中使用。它由 HashSet、LinkedHashSet 或 TreeSort 实现。

![Sets - Java Collections - Edureka](img/11dc7ea681102c525adc8d8c5634f739.png)

在对集合进行迭代时，这些实现中的每一个都有不同的行为，主要是关于元素的排序，以及插入和访问元素所花费的时间。

## **如何创建集合？**

以下代码定义了创建新集合的方法:

```
Set<Integer> num = new HashSet<>();
```

我们已经使用了[泛型](https://www.edureka.co/blog/generics-in-java/)来声明整数类型的集合。

## **在 Java 中设置方法:**

我们可以在集合上执行多个操作，如下所示:

### **添加方法**

add 方法向 [Java 集合](https://www.edureka.co/blog/java-collections)中插入一个元素。在下面的代码中，我们插入了一组名字。

```
Set<String> strName = new HashSet<>();  
strName.add("John");  
strName.add("Doe");  
System.out.println(strName);  

```

**输出:**

[约翰，多伊]

### **移除方法**

此方法从集合中移除指定的元素。

```
import java.util.*; 
public class Main{
    public static void main(String args[]) 
    { 
        // Creating an Empty Set 
        Set<String> set = new HashSet<String>(); 

        //Adding elements to the set
        set.add("John"); 
        set.add("Doe"); 

        // Display the set
        System.out.println("Set: " + set); 

        // Removing the element “Doe” using remove() method 
        set.remove("Doe"); 

        // Displaying the modified set
        System.out.println("Set : "
                           + set); 
    } 
}  

```

**输出:**

集合:[约翰，多伊]

集合:[约翰]

### **是空方法**

该方法检查确定[设置](https://www.edureka.co/blog/java-collections/#sets)是否为空。如果集合为空，则返回 true，否则返回 false。

```
import java.io.*; 
import java.util.*; 

public class Main { 
	public static void main(String args[]) 
	{ 
		Set<String> javaSet = new HashSet<String>(); 

		// Adding elements to the Set 
		javaSet.add("John"); 
		javaSet.add("Doe"); 

		// Display the set 
		System.out.println("Set: " + javaSet); 

		// Checking whether the set is empty
		System.out.println("Empty Set : " + javaSet.isEmpty()); 

		// Clearing the set using the clear() method 
		javaSet.clear(); 

		// Checking whether the set is empty 
		System.out.println("Empty Set : " + javaSet.isEmpty()); 
	} 
}

```

**输出:**

集合:[约翰，多伊]

空集:假

空集:真

### **尺寸方法**

size()方法返回集合的大小，即集合中元素的数量。

```
import java.util.*; 
public class Main { 
	public static void main(String args[]) 
	{ 
		// Creating a set 
		Set<String> set = new HashSet<String>(); 
		set.add("John"); 
		set.add("Doe");

		System.out.println("Set: " + set); 

		// Displaying the size of the sent
		System.out.println("Size of the set : " + set.size()); 
	} 
}

```

**输出:**

集:[约翰·多伊]

一套的大小:2

### **迭代一个集合**

我们可以通过以下方法迭代集合中的所有元素:

```
import java.util.*; 
import java.util.HashSet; 

public class Main { 
	public static void main(String args[]) 
	{ 
		// Creating a HashSet 
		HashSet<String> javaSet = new HashSet<String>(); 

		javaSet.add("John"); 
		javaSet.add("Doe"); 

		// Displaying the set
		System.out.println("HashSet: " + javaSet); 

		// Creating an iterator 
		Iterator itr = javaSet.iterator(); 

		// Displaying the values after iteration 
		System.out.println("Iterator values: "); 
		while (itr.hasNext()) { 
			System.out.println(itr.next()); 
		} 
	} 
}

```

**输出:**

哈塞特:[约翰，动手]

迭代器值:

约翰

母鹿

**在集合中搜索**

我们使用 contains()方法来确定集合是否包含指定的元素。如果找到该元素，则返回 true，否则返回 false。

```
import java.io.*; 
import java.util.HashSet; 

public class Main { 
	public static void main(String args[]) 
	{ 
		// Creating a HashSet 
		HashSet<String> javaSet = new HashSet<String>(); 
		javaSet.add("John"); 
		javaSet.add("Doe");

		// Displaying the HashSet 
		System.out.println("HashSet: " + javaSet); 

		// Checking for “John” in the set 
		System.out.println("John in set: " + javaSet.contains("John")); 

		// Checking for "Hazel" in set 
		System.out.println("Hazel in set: " + javaSet.contains("Hazel")); 
	} 
}

```

**输出:**

哈塞特:[约翰，动手]

场景中的约翰:没错

集合中的黑兹尔:假

## **Java 中对集合的基本操作**

*   **Union:** 要将一个集合添加到另一个集合，我们使用 Union 操作
*   **交集:**为了保留两个集合的公共值，我们使用交集操作。
*   **差:**要从另一个集合中删除一个集合的值，使用差运算。

**例子**

```
import java.util.*; 
public class Main
{ 
	public static void main(String args[]) 
	{ 
		Set<Integer> d = new HashSet<Integer>(); 
		d.addAll(Arrays.asList(new Integer[] {3, 2, 1, 9, 6, 4, 0})); 
		Set<Integer> e = new HashSet<Integer>(); 
		e.addAll(Arrays.asList(new Integer[] {3, 1, 9, 5, 2, 0, 7,})); 

		// Union Operation
		Set<Integer> union = new HashSet<Integer>(d); 
		union.addAll(e); 
		System.out.println("Union :" + union); 

		// Intersection Operation
		Set<Integer> intersection = new HashSet<Integer>(d); 
		intersection.retainAll(e); 
		System.out.println("Intersection :" + intersection);  

		// Difference Operation 
		Set<Integer> difference = new HashSet<Integer>(d); 
		difference.removeAll(e); 
		System.out.println("Difference :" + difference);  
	} 
}

```

**输出:**

联合:[0，1，2，3，4，5，6，7，9]

交集:[0，1，2，3，9]

差异:[4，6]

方法中提到的方法和操作使得集合接口本质上是基本的和有效的。

这样，我们就结束了这篇关于“Java 中的集合”的文章。如果你想了解更多，请查看由 Edureka(一家值得信赖的在线学习公司)提供的 [Java 培训](https://www.edureka.co/java-j2ee-soa-training) 。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在“java 中的集合”文章的评论部分提到它，我们会尽快回复您。