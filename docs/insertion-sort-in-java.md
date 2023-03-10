# 如何在 Java 中实现插入排序？

> 原文：<https://www.edureka.co/blog/insertion-sort-in-java/>

java 中的插入排序是一种简单而有效的排序算法，它一次一个元素地创建最终排序的数组。通常在用户数据集比较小的时候实现。我将讨论以下主题:

*   [什么是插入排序？](#what)
*   [插入排序算法](#algo)
*   [Java 中用于插入排序的代码](#code)
*   [复杂性和边界情况](#complexity)

## **什么是插入排序？**

java 中的插入排序是一种高效的排序算法，它一次一个元素地创建最终排序的数组。每次迭代后，输入数据中的一个元素将被删除。将它与数组中的最大值进行比较，然后将其移动到正确的位置。为了理解这种工作方式，让我们看一下这个例子。

![Inserion-sort-in-java](img/e0f03640275260d3518fac400f714a24.png)

## **插入排序算法**

假设我们有一个未排序的数组**【6，5，15，3，9】**

*   ***第 1 次索引迭代:*** 第 1 次索引时的值为 5，小于 6。数组变成**【6，6，15，2，8】**。

到达元素集合的开始时，我们将值放在第 0 个索引处。数组现在变成:**【5，6，15，3，9】**

*   ***第二次索引迭代*** :第二次索引处的值为 15，大于 6。数组中没有任何更改。

*   ***第三次索引迭代*** :第三次索引处的值为 3。该值小于 15，因此数组变为**【5，6，15，15，9】**

值 3 也小于 6，因此数组现在变为**【5，6，6，15，9】**

3 也比 5 小。数组再次修改为**【5，5，6，15，9】**

当到达数组的开头时，3 被放置在第 0 个索引处。该数组现在被定义为**【3，5，6，15，9】**

*   ***第 4 个索引迭代:***第 4 个索引处的值为 9。按照类似的算法，最终排序后的数组是:**【3，5，6，9，15】**

## **Java 中用于插入排序的代码**

```
// Java program to implement Insertion Sort
public class InsertionEx { 
	/*Function to sort array using insertion sort*/
	void sort(int a[]) 
	{ 
		int n = a.length; 
		for (int i = 1; i < n; ++i) { int key = a[i]; int j = i - 1; /* Move elements of a[0..i-1], that are greater than key, to one position ahead of their current position */ while (j >= 0 && a[j] > key) { 
				a[j + 1] = a[j]; 
				j = j - 1; 
			} 
			a[j + 1] = key; 
		} 
	} 

	/* A function to print array of size n*/
	static void displayArray(int a[]) 
	{ 
		int n = a.length; 
		for (int i = 0; i < n; ++i) 
			System.out.print(a[i] + " "); 

		System.out.println(); 
	} 

	// Driver code 
	public static void main(String args[]) 
	{ 
		int a[] = { 25, 28, 18, 10, 5 }; 

		InsertionEx ob = new InsertionEx(); 
		ob.sort(a); 
		displayArray(a); 
	} 
}
```

## **复杂性和边界情况**

*   ***时间复杂度*** :插入排序的时间复杂度为 O(n*2)。

*   ***边界情况*** :插入排序所花费的最大时间是元素逆序排序时。如果元素已经排序，花费的时间最少

当要排序的元素数量较少时，用户执行插入排序。当指定的数组几乎被排序时，也可以使用它，即只有少数数字被放错了位置，并且不在适当的位置。

至此，我们结束了 Java 文章中的插入排序。C *查看 Edureka 提供的  [**Java 培训**](https://www.edureka.co/java-j2ee-soa-training)* *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 25 万名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

有问题要问我们吗？请在这篇“Java 中的插入排序”博客的评论部分提到它，我们会尽快回复您。