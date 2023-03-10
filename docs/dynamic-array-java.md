# 什么是 Java 中的动态数组？

> 原文：<https://www.edureka.co/blog/dynamic-array-java/>

Java 中的数组是在 Java 中作为对象实现的同构数据结构。数组存储一个或多个特定数据类型的值，并提供索引访问来存储这些值。数组中的特定元素通过其索引来访问。在本文中，我们将按以下顺序讨论 Java 中的动态数组:

*   [Java 动态数组简介](#dynamic)
*   [尺寸与容量](#size)
*   [加倍追加](#append)
*   [删除一个元素](#delete)
*   [在 Java 中调整动态数组的大小](#resize)

## **Java 动态数组简介**

动态数组就是这样一种在自动调整大小方面有巨大改进的数组。数组的唯一限制是它的大小是固定的。这意味着您只能提前指定数组可以容纳的元素数量。另一方面，动态数组可以随着我们实时添加更多元素而扩展。因此，编码器不需要提前确定数组的大小。它也有更多的优势:

*   **快速查找** 。和数组一样，当检索给定索引处的元素时，需要 O (1)时间。

*   可变大小。我们可以插入任意多的元素，一个动态数组会相应地扩展来容纳它们。

*   缓存友好。与数组类似，动态数组可以在内存中相邻放置项目，从而有效利用缓存。

在我们的代码中使用动态数组有一些缺点。尽管在大多数应用程序中，我们使用动态数组的次数比其他任何东西都多，但是在某些情况下，由于其局限性，它们并没有成为首选。

*   **慢速追加**。通常，当在动态数组的末尾添加新元素时，在一个实例中需要 O (1)。然而，如果动态数组对一个新的条目没有更多的索引，那么它将需要扩展，每次需要 O (n)。

*   **代价高昂的插入和删除。** 类似于数组，元素彼此相邻存储。因此，在数组中心添加或删除一个元素时，需要推送其他元素，一次需要 O (n)个元素。

下图显示了阵列如何实时工作，并描述了元素如何堆叠。它还显示了在数组函数的一般情况和最坏情况下，指令是如何变化的。

![array - dynamic array in java - edureka](img/7b632c60579759ee4b25f23ad9ea9825.png)

![](img/dadf651bfa5246e670d6c63ad4f569ec.png)

## **大小与容量**

当我们初始化一个动态数组时，动态数组实现创建一个可理解的固定大小的数组。初始大小与实现相对应。例如，让我们使我们的实现数组使用 10 个索引。现在我们向动态数组中添加四项。现在，我们的动态数组长度为 4。然而，我们的底层数组长度为 10。因此，我们可以说动态数组的大小是 4，容量是 10。动态数组存储特定的结束索引，以跟踪动态数组的结束点和额外容量开始的起始点。

![size - dynamic array in javascript - edureka](img/79f887c326d5c10627b659053e88050c.png)

![](img/82f6d4625f21ba3edf0df54b00532c8b.png)

## **加倍追加**

可能会有这样的情况，我们试图将一个项目添加到容量已经满了的数组中。因此，创建房间动态数组会自动创建新的、更大的底层数组。通常，它会变得两倍大，以处理任何新添加的内容，这是它之前没有预料到的。因此，复制每个项目不会耗费时间。每当向我们的动态数组追加一个项时，都会自动生成一个新的双倍大小的底层数组，这种追加不需要时间。

## **删除一个元素**

从数组中删除元素时，默认的“remove()”方法从末尾删除一个元素，并在最后一个索引处自动存储零。它还将通过调用 removeAt(i)方法删除特定索引处的元素，其中“I”是索引。removeAt(i)方法从给定的索引开始移动左侧的所有右侧元素。

![delete - dynamic array in java - edureka](img/611294969e9b0b8ff0fdf09c1bf8e571.png)

## **调整数组大小**

当数组的右边没有数据会占用不必要的内存时，srinkSize()方法会释放额外的内存。当所有的槽都被消耗并且添加了额外的元素时，底层的固定大小的数组必须增加大小。实际的大小调整是很昂贵的，因为我们必须分配一个更大的数组，并从一个数组中复制所有的元素，直到它能够追加一个新的元素。

![resize - dynamic array in java - edureka](img/1bfaa74919418918fd43e5bc9237203c.png)

下面是一个程序示例，其中数组变满，新元素被复制到一个新的双倍大小的数组中。该元素是一个名为“Mahavir”的字符串元素，是对已经满满的大小为 3 的数组的添加。

```
import java.util.ArrayList;
import java.util.Arrays;
import java.util.Scanner;
public class AddingItemsDynamically
{
public static void main(String args[])
{
Scanner sc = new Scanner(System.in);
System.out.println("Enter the size of the array :: ");
int size = sc.nextInt();
String myArray[] = new String[size];
System.out.println("Enter elements of the array (Strings) :: ");
for(int i=0; i<size; i++)
{
myArray[i] = sc.next();
}
System.out.println(Arrays.toString(myArray));
ArrayList<String> myList = new ArrayList<String>(Arrays.asList(myArray));
System.out.println("Enter the element that is to be added:");
String element = sc.next();
myList.add(element);
myArray = myList.toArray(myArray);
System.out.println(Arrays.toString(myArray));
}
}
```

**输出:**

![](img/46cfc74e7cac9cccc73f267738bdb9c1.png)

这样，我们就到了 Java 文章中动态数组的结尾。我希望您对如何使用动态数组有所了解。

*查看 Edureka 提供的  [**Java 在线课程**](https://www.edureka.co/java-j2ee-training-course)* *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

有问题要问我们吗？请在这篇“Java 动态数组”博客的评论部分提到它，我们会尽快回复您。