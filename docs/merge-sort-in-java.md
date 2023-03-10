# 如何在 Java 中进行归并排序？

> 原文：<https://www.edureka.co/blog/merge-sort-in-java/>

听说过“分而治之”这个词吗？这篇文章正是基于这种方法。 ***合并排序*** 是一种“分而治之”的算法，我们首先将问题分成子问题，然后将它们合并在一起，以征服我们的解决方案。这里是 J [ava](https://www.edureka.co/blog/java-tutorial/) 中合并排序概念的完整概述。

*   [什么是 Java 中的归并排序？](#WhatismergesortinJava?)
*   [进行合并排序](#Workingofmergesort)
*   [示例:图表](#Example:Diagram)
*   [实施](#Implementation)
*   [复杂度](#Complexity)

让我们开始吧！

## **什么是 Java 中的归并排序？**

合并排序是可用的流行排序算法之一，它遵循分而治之的方法。一个问题分成子问题，组合在一起，得出最终的解决方案！

现在，合并排序的工作过程中到底发生了什么？让我们详细了解一下。

## **进行合并排序**

在该过程中，合并排序遵循两个步骤:

*   **Divide:** 在这一步中，输入数组被分成两半，轴心是数组的中点。对所有半数组递归地执行该步骤，直到不再有半数组要进一步划分。
*   **征服:**在这一步中，我们从下到上对分割后的数组进行排序和合并，并到达我们排序后的数组。

这种方法有助于你首先轻松地对问题的子部分进行分类，从而找到解决方案。

让我给你看一个合并排序的图示。

## **示例:图表**

![Merge Sort - Edureka](img/3de150a214e9b3a03f7f11d134a57520.png)

在这里，您看到了合并排序的样子。合并排序的主要概念是排序花费的时间更少。现在，继续我们的实现部分！

## **实现**

```
package MyPackage;
public class MergeSort
{
void merge(int arr[], int beg, int mid, int end)
{
int l = mid - beg + 1;
int r = end - mid;
int LeftArray[] = new int [l];
int RightArray[] = new int [r];
for (int i=0; i<l; ++i)
LeftArray[i] = arr[beg + i];
for (int j=0; j<r; ++j)
RightArray[j] = arr[mid + 1+ j];
int i = 0, j = 0;
int k = beg;
while (i<l&&j<r)
{
if (LeftArray[i] <= RightArray[j])
{
arr[k] = LeftArray[i];
i++;
}
else
{
arr[k] = RightArray[j];
j++;
}
k++;
}
while (i<l)
{
arr[k] = LeftArray[i];
i++;
k++;
}
while (j<r)
{
arr[k] = RightArray[j];
j++;
k++;
}
}
void sort(int arr[], int beg, int end)
{
if (beg<end)
{
int mid = (beg+end)/2;
sort(arr, beg, mid);
sort(arr , mid+1, end);
merge(arr, beg, mid, end);
}
}
public static void main(String args[])
{
int arr[] = {40,51,22,45,1,4,90,23,17,55};
MergeSort ob = new MergeSort();
ob.sort(arr, 0, arr.length-1);
System.out.println("nSorted array");
for(int i =0; i<arr.length;i++)
{
System.out.println(arr[i]+"");
}
}
}
```

**输出:** 排序数组 141722234045515590

这是描述合并排序的 Java 代码的样子。继续下一个环节。

## **复杂度**

复杂性分为两种类型:时间复杂性和空间复杂性。对于合并排序，数据如下所示:

| 复杂性 | 最好的情况 | 一般情况 | 最坏情况 |
| 时间复杂度 | O(n 对数 n) | O(n 对数 n) | O(n 对数 n) |
| 空间复杂性 | – | – | O(n) |

我将以此结束这篇文章。我希望上面解释的内容能够增加您的 Java 知识。我们将继续一起探索 Java 世界。敬请期待！

*查看 Edureka 提供的* [***Java 培训***](https://www.edureka.co/java-j2ee-soa-training)*，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 25 万名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

有问题要问我们吗？请在这个“ [*合并 Java 排序*](#_gjdgxs) *”博客的评论区提出来，我们会尽快回复你。*