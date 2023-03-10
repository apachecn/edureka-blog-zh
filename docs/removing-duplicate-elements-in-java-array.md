# 删除 Java 数组中的重复元素

> 原文：<https://www.edureka.co/blog/removing-duplicate-elements-in-java-array/>

不管你使用哪种编程语言。在使用数组时，您肯定会遇到数据，尤其是您想要消除的重复数据。这篇文章将帮助你移除 Java 数组中的数据。我们来看看在 java 数组中删除重复元素的三种不同方法。

*   [方法 1](#Method1)
*   [方法二](#Method2)
*   [方法三](#Method3)

那么让我们开始吧，

## **删除 Java 数组中的重复元素**

为了删除数组中的重复元素并获得唯一的数组，我们使用了多种方法和过程。最重要的如下:

## **方法 1**

在这个方法中，我们使用一个临时数组来删除重复的元素。

```

public class Main{
public static int removeDuplicates(int array[], int n){
if(n==0 || n==1){
return n;
}
int[] temp = new int[n];
int j = 0;
for(int i=0; i&lt;n-1; i++){
if(array[i] != array[i+1]){
temp[j++] = array[i];
}
}
temp[j++] = array[n-1];
//Changing the original array
for(int i=0; i&lt;j; i++){
array[i] = temp[i];
}
return j;
}
public static void main (String[] args) {
int array[] = {18,18,25,25,25,28,28,29};
int length = array.length;
length = removeDuplicates(array, length);
//Printing The array elements
for(int i=0; i&lt;length; i++)
System.out.print(array[i]+" ");

}

}

```

我们创建一个临时数组来存储唯一的元素。遍历初始数组，并将唯一元素复制到临时数组中。使用“j”跟踪唯一元素的计数。然后将 j 中的值从临时数组复制到初始数组，之后返回 j。

该程序将删除数组中所有重复的元素。

**输出:**

18,25,28,29

让我们继续这篇关于“删除 Java 数组中的重复元素”的文章

## **方法二:** **删除 Java 数组中的重复元素**

在这种方法中，使用单独的索引。

```

public class Main{
public static int removeDuplicates(int array[], int n){
if(n==0 || n==1){
return n;
}
int j = 0;//for next element
for (int i=0; i &lt; n-1; i++){
if (array[i] != array[i+1]){
array[j++] = array[i];
}
}
array[j++] = array[n-1];
return j;
}
public static void main (String[] args) {
int array[] = {18,18,25,25,25,28,28,29};
int length = array.length;
length = removeDuplicates(array, length);
//printing array elements
for(int i=0; i&lt;length; i++)
System.out.print(array[i]+" ");
}
}

```

18,25,28,29

让我们转到本文的最后一点，

## **方法三**

这里，我们删除了未排序数组中的重复元素。首先使用 Array.sort()方法对未排序的数组进行排序。

```

import java.util.Arrays;
public class Main{
public static int removeDuplicates(int array[], int n){
if(n==0 || n==1){
return n;
}
int[] temp = new int[n];
int j = 0;
for (int i=0; i&lt;n-1; i++){
if(array[i] != array[i+1]){
temp[j++] = array[i];
}
}
temp[j++] = array[n-1];
//Changing original array
for(int i=0; i&lt;j; i++){
array[i] = temp[i];
}
return j;
}
public static void main (String[] args) {
int array[] = {25,28,18,29,25,18,29,28,25,18};//unsorted array
Arrays.sort(array);//sorting array
int length = array.length;
length = removeDuplicates(array, length);
//printing array elements
for(int i=0; i&lt;length; i++)
System.out.print(array[i]+" ");
}
}

```

**输出:**

18,25,28,29

本文提到的方法可以防止 java 数组中元素的重复。

如果您刚刚开始，那么请阅读这篇 Java Array 教程，了解基本概念。

[https://www.youtube.com/embed/TmM9XAIKa-Y](https://www.youtube.com/embed/TmM9XAIKa-Y)

因此，我们已经结束了这篇关于“删除 Java 数组中的重复元素”的文章。如果您想了解更多，请查看 Edureka(一家值得信赖的在线学习公司)提供的 [Java 在线课程](https://www.edureka.co/java-j2ee-training-course)。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在本博客的评论部分提及此事，我们将尽快回复您