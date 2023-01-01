# 在 Java 中反转数组:关于反转数组你需要知道的一切

> 原文：<https://www.edureka.co/blog/reversing-an-array-in-java/>

对数据结构中的一些数据进行反转，偶尔会达到一些有意义的目的。我们可能会发现自己需要间歇性地在 java 中反转数组。 做这件事有各种各样的方法。在本文中，我将讨论在 Java 中反转数组的最相关和最值得注意的方法。

我们将学习三种方法来实现上述目标，

*   [方法 1](#Method1)
*   [方法二](#Method2)
*   [方法三](#Method1)

让我们从第一种方法开始，

## **在 Java 中反转数组**

## ****方法一****

```
/* Basic Java program that reverses an array*/
public class arrayReverse {   
/*function that reverses the array and stores it  
in another array*/
static void reverse(int a[], int n) 
{ 
int[] d = new int[n]; 
int j = n; 
for(int i = 0; i < n; i++) { 
d[j - 1] = a[i]; 
j = j - 1; 
}   
/*Printing the Reversed array*/
System.out.println("The Reversed array is: n"); 
for(int k = 0; k < n; k++) { 
System.out.println(d[k]); 
} 
} 
public static void main(String[] args) 
{ 
int [] array = {25, 28, 29, 18, 65}; 
reverse(array, array.length); 
} 
}

```

程序授予以下步骤:

*   **输入 :** 数组的大小和元素作为输入。

*   **反转功能 :** 程序利用了反转功能。该函数接受参数:数组(即 array)和数组的大小(即 n)

*   **方法论** **:** 在函数中，初始化一个新数组，大小为第一个数组。数组 array[]从头开始迭代。

数组中的所有元素以相反的顺序放入新数组中。必须注意，新数组是从最后一个元素开始迭代的。

**输出:**

反转数组为:

65

18

29

28

25

使用的方法是反转数组的最基本方法，因其简单性而被广泛使用。

## **方法二:在 Java 中反转数组**

在前面的例子中，我们已经创建了一个包含反转元素的新数组。这种方法，我们将通过交换元素来反转原始数组。

```
/*Java program that reverses an array using swaps*/
public class Main
{
public static void main(String[] args) {
int[] array = { 10, 9, 8, 7, 6, 5, 4, 3, 2, 1 };
System.out.println("Array Before Reversing:");
/*function that reverses the array using swap*/ 
for(int i = 0; i < array.length; i++) {
System.out.print(array[i] + " ");
} 
for (int i = 0; i < array.length / 2; i++) {
int temp = array[i];
array[i] = array[array.length - 1 - i];
array[array.length - 1 - i] = temp;
} 
/*Printing the Reversed array*/
System.out.println("nArray After Reversing:");
for (int i = 0; i < array.length; i++) {
System.out.print(array[i] + " ");
} 
}
}

```

在上面的例子中，第一个元素与最后一个元素交换。 同样，第二个元素与倒数第二个元素交换，依此类推。 例如，1 与 n 交换，2 与 n-1 交换等等。

**输出:**

反转前的阵列:

10 9 8 7 6 5 4 3 2 1

反转后的数组:

1 2 3 4 5 6 7 8 9 10

让我们转到本文的最后一点，

## **方法三**

该方法通过将数组转换为列表来反转数组，之后利用*collections . reverse()*方法。*collections . reverse()*方法获取列表并反转元素。在下面给出的例子中，我们创建了一个名为 array 的数组列表，并向其中添加了多个元素。*collections . reverse()*方法在线性时间内反转数组。

```
import java.util.ArrayList;
import java.util.Collections;
public class Main {
public static void main(String[] args) {
ArrayList array = new ArrayList();
array.add("My");
array.add("Name");
array.add("Is");
array.add("Jeremy");
array.add("Hanson");
System.out.println("Before Reverse Order: " + array);
Collections.reverse(array);
System.out.println("After Reverse Order: " + array);
}
}

```

**输出:**

倒序前:【我的，姓名，是，杰里米，汉森】

逆序后:【汉森，杰里米，是，名字，我的】

这些方法为 Java 编程语言中的数组反转提供了最全面的方法。

这样，我们就结束了这篇关于“在 Java 中反转数组”的文章。如果你想了解更多，请查看 Edureka 值得信赖的在线学习公司提供的 [**Java 培训**](https://www.edureka.co/java-j2ee-soa-training) 。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。