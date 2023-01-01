# Java 中数组，ArrayList，String，List，Map，Set 如何排序？

> 原文：<https://www.edureka.co/blog/sort-arraylist-string-map-set-in-java/>

排序是任何编程语言的重要组成部分。毫无疑问，Java 是最好的编程语言之一。它有各种各样的功能，使它很容易！这篇文章将帮助你展开关于在 Java 中排序的一切，特别是在 Java 中排序数组、数组列表、字符串、列表、映射和集合。

这篇分类文章涵盖了以下主题:

*   [Java 中的排序数组](#sortarray)
*   [数组 vs 数组列表](#arrayvsarraylist)
*   [排序数组列表](#sortarraylist)
*   [排序字符串](#sortstring)
*   [排序列表](#sortlist)
*   [整理地图](#sortmap)
    *   [按键排序地图](#sortmapbykey)
    *   [按值排序地图](#sortmapbyvalue)
*   [在 Java 中对集合进行排序](#sortset)

让我们开始吧。:-)

## **Java 中的排序数组**

[Java 中的数组](https://www.edureka.co/blog/java-array/)存储一个或多个特定数据类型的值，并提供索引访问以将这些值存储在单个变量中。让我们看看下面的程序，用 Java 对数组进行升序排序。然而，确保你已经安装了[Java](https://java.com/en/download/help/download_options.xml)。

### **用 Java 对数组进行升序排序**

```

package Edureka;

import java.util.Arrays;

public class SortArray
{ 
public static void main(String[] args) 
{ 
int[] arr = {52,12,2,72,4}; // array of 5 elements
Arrays.sort(arr); 
System.out.printf("Sorted arr[] = %s", 
Arrays.toString(arr)); 
} 
}

```

**输出**–排序后的 arr[] = [2，4，12，52，72]

### **在 Java 中对数组进行排序——降序**

```

package Edureka;

import java.util.Arrays;
import java.util.Collections;

public class SortArray
{
public static void main(String[] args)
{
Integer[] arr = {52,12,2,72,4}; // used Integer[] instead of int as collections
Arrays.sort(arr, Collections.reverseOrder()); // reverseorder() for descending order
System.out.printf("Sorted arr[] = %s",
Arrays.toString(arr));
}
}

```

**输出:**排序后的 arr[] = [72，52，12，4，2]

**注意:**在上面的代码中，因为[集合](https://www.edureka.co/blog/java-collections/)，我已经用 Integer[]数组代替了 int。这是因为 reverseOrder()不支持基本类型。

很多人混淆了 Java 中数组和 ArrayList 的概念。下表可能会消除你所有的疑虑。

| **数组** | **阵列列表** |
| 它的长度是固定的 | 它的长度是可变的(大小是动态的) |
| 仅支持原始数据类型 | 可以将不同的对象和数据添加到列表中 |
| 不支持重复添加 | 允许添加重复元素 |
| 只能向前移动 | 可以向前和向后移动 |
| 大小不能动态修改 | 大小可以动态修改 |

我希望你清楚其中的区别，让我们继续，看看如何在 Java 中对[数组列表进行排序。](https://www.edureka.co/blog/java-arraylist/)

## **Java 中的 Sort ArrayList(String)**

通过使用一个简单的 **sort()方法**，可以很容易地对 Java 中的 ArrayList 进行排序。参考下面的代码在 Java 中对数组列表进行排序。

```

package Edureka;

import java.util.Arrays; 
import java.util.Collections;
import java.util.*;

public class sortingarraylist
{	  
    public static void main(String args[]) 
	    {  
	        ArrayList<String>
	            list = new ArrayList<String>(); 

	     // Populate the ArrayList
	     list.add("sorting");
	     list.add("java");
	     list.add("arraylist");
	     list.add("in"); 
	     System.out.println("Unsorted ArrayList: "
	                           + list); // printed unsorted arraylist
	     Collections.sort(list); // sort method for ascending order  

	     System.out.println("Sorted ArrayList "
	                           + "in Ascending order : "
	                           + list); // print sorted arraylist
	    } 
	} 

```

**输出—**

未排序的数组列表:[sorting，java，ArrayList，in] 按升序排序的数组列表:[arraylist，in，java，sorting]

继续 Java 文章中的排序，让我们看看如何对整数进行排序。让我们尝试使用不同的方法来实现排序，例如使用 Collections.sort()方法。

### **使用集合(整数)对 Java 中的数组列表进行排序**

可以使用 Collections.sort()方法对整数数组列表进行排序。

```
package Edureka;

import java.util.Arrays; 
import java.util.Collections;
import java.util.*;

public class SortingArrayList
{	
	public static void main(String args[]){
	   ArrayList<Integer> arraylist = new ArrayList<Integer>();
	   arraylist.add(48);
	   arraylist.add(2);
	   arraylist.add(19);
	   arraylist.add(22);
	   System.out.println("Before Sorting:"); // before sorting
	   for(int counter: arraylist){
			System.out.println(counter);
		}

	   Collections.sort(arraylist); // function to sort in ascending order 

	   System.out.println("After Sorting:"); // after sorting
	   for(int counter: arraylist){
			System.out.println(counter);
		}
	}
}

```

**输出-**排序前: 48 2 19 22 排序后: 2 19 22 48

## **Java 中的排序字符串**

Java 中的字符串是不可变的。Java 中没有对[字符串进行排序的直接方法。您可以使用 Arrays，它有一个 CharArray()方法，该方法将创建一个 char 输入字符串，使用另一个方法(Arrays.sort(char c[])我们可以轻松地进行排序。](https://www.edureka.co/blog/java-string)

```
package Edureka;

import java.util.Arrays; 
import java.util.Collections;
import java.util.*;

public class SortingString
{	
    public static String sortString(String inputString) 
    { 
        char Array1[] = inputString.toCharArray(); // converting input string to char array 

        Arrays.sort(Array1); 

        return new String(Array1); // return sorted string
    } 

    public static void main(String[] args) 
    { 
        String inputString = "Edureka"; 
        String outputString = sortString(inputString); 

        System.out.println("Input String : " + inputString); 
        System.out.println("Output String : " + outputString); 
    } 
}  
```

**输出-**输入字符串:爱德华卡输出字符串:艾德克鲁

## **用 Java 排序列表**

要在 [Java](https://www.edureka.co/blog/java-tutorial/) 中对列表进行排序，可以使用 Collections.sort()方法。请参考以下代码以获得更多理解:

```
package Edureka;

import java.util.Arrays; 
import java.util.Collections;
import java.util.*;

public class SortingList
{	
	public static void main(String[] args) 

	{
		Integer[] digits = new Integer[] {12,56,89,27,22,4,88,65,36};
    	List<Integer> digitsList = Arrays.asList(digits);

    	Collections.sort(digitsList); // sorted list

    	System.out.println("Sorted String :" +digitsList);
    } 
}    
```

**输出**:排序后的字符串:[4，12，22，27，36，56，65，88，89]

## **用 Java 排序地图**

Java 中的映射属于包含键值对的 [Java 集合](https://www.edureka.co/blog/java-collections/)。因此，可以用两种不同的方式对地图进行排序:

*   按关键字排序
*   按值排序

### 按关键字排序:

```
package Edureka;

import java.util.Arrays; 
import java.util.Collections;
import java.util.*;

public class SortingMap
{	
	public static void main(String[] args) 

	{
		HashMap<Integer, String> map = new HashMap<>();

		map.put(14, "Aayushi");
		map.put(2, "Rachit");
		map.put(30, "Amit");
		map.put(5, "Anamika");

		TreeMap<Integer, String> treeMap = new TreeMap<>(map);

		System.out.println(treeMap);
    } 
}    
```

**输出:** {2=Rachit，5=Anamika，14=Aayushi，30=Amit}

### **按值排序:**

```
package Edureka;

import java.util.Arrays; 
import java.util.Collections;
import java.util.*;

public class SortingMap  
{	
	public static void main(String[] args) 

	{
		HashMap<Integer, String> unSortedMap = new HashMap<>();

	unSortedMap.put(14, "Aayushi");
	unSortedMap.put(20, "Rachit");
	unSortedMap.put(60, "Amit");
	unSortedMap.put(70, "Anamika");

	LinkedHashMap<Integer, String> sortedMap = new LinkedHashMap<>();

	unSortedMap.entrySet()
	    .stream()
	    .sorted(Map.Entry.comparingByValue())
	    .forEachOrdered(x -> sortedMap.put(x.getKey(), x.getValue()));

	System.out.println(sortedMap);
	}
}    
```

**输出:** {14=Aayushi，60=Amit，70=Anamika，20=Rachit}

继续 Java 中的排序，让我们回到最后一个话题，即在 [Java](https://www.edureka.co/blog/what-is-java/) 中对集合进行排序。

## **Java 中的排序集**

Java 中的 Set 是一个扩展集合的接口。它是一个无序的对象集合，不存储重复的值。现在 Java 中没有直接的方法对集合进行排序。现在，要对集合进行排序，必须将集合转换为列表，然后使用 collections.sort() API，再次将列表转换回集合。请参考下面的代码以获得更多的理解:

```
package Edureka;

import java.util.Arrays; 
import java.util.Collections;
import java.util.*;

public class SortSet
{	
	public static void main(String[] args) 

	{
		//Unsorted list
		HashSet<Integer> numbersSet = new LinkedHashSet<>(
		        Arrays.asList(12,56,89,27,22,4,88,65,36) );

		List<Integer> numbersList = new ArrayList<Integer>(numbersSet);  //convert set to list

		//Sort the list
		Collections.sort(numbersList);

		numbersSet = new LinkedHashSet<>(numbersList);  //convert list to set

		//Print set to confirm
		System.out.println(numbersSet);
	}
}    
```

**输出**:【4，12，22，27，36，56，65，88，89】

我们关于 Java 排序的博客到此结束，你已经学会了如何在 Java 中对数组、数组列表、字符串、映射和集合进行排序。我希望你发现这个博客信息丰富，增加了你的知识价值。

***确保你尽可能多的练习，恢复你的经验。***

*查看 Edureka 的 [**Java 认证**](https://www.edureka.co/java-j2ee-training-course) 培训* *，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

*有问题吗？请在这篇“Java 中的排序:Java 中的数组、数组列表、字符串、映射和集合”的评论部分提到它，我们会尽快回复您。*