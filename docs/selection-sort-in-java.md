# 如何用 Java 实现选择排序？

> 原文：<https://www.edureka.co/blog/selection-sort-in-java/>

[选择排序](https://www.edureka.co/blog/selection-sort-in-c/)是学习&码最简单的算法之一。这篇文章将帮助你了解 Java 中选择排序的细节。本文将涉及以下几点:

*   [选择排序算法](#SelectionSortAlgorithm)
*   [选择排序示例](#SelectionSortExample)
*   [Java 中的选择排序方法](#SelectionSortMethodinJava)
*   [选择 Java 中的排序程序](#SelectionSortPrograminJava)

让我们从 Java 文章中的选择排序开始，

选择排序中最重要的部分是理解算法维护两个子数组:

*   一个子数组是排序数组
*   另一个子数组是未排序数组

![Image- Selection sort in Java- Edureka](img/401ca00c9118faaa23e81afd481d2c20.png)

排序后的子数组保存在原始数组的开头，而其余部分形成未排序的子数组。该算法将未排序数组中的最小元素移动到排序数组的末尾。准确的说，这不是移动，是用未排序数组的第一个元素交换未排序数组的最小元素，然后增加排序数组的索引。

让我们把它变得更简单。选择排序首先在未排序的数组(array[0..n]，它是第一次迭代中的完整数组)并将其与第一个元素交换。然后它在未排序的数组中找到第二小的元素(即 array[1..n])并将其与第二个元素交换，该算法一直这样做，直到整个数组排序完毕。

因此，排序数组随着每次迭代从 0 增长到 n，未排序数组随着每次迭代从 n 减少到 0。由于该算法不断选择最小的元素并将其交换到正确的位置，因此它被称为选择排序。由于时间复杂度是分析算法效率的最重要因素之一，让我们看看选择排序的时间复杂度。

*   最坏情况复杂度:O(n2)
*   最佳情况复杂度:O(n2)
*   平均案件复杂度:O(n2)

继续这篇关于 Java 中选择排序的文章

**选择排序算法**

第 1 步将 Min_Index 设置为 0 第 2 步搜索数组中的最小元素第 3 步与 Min_Index 处的元素交换值第 4 步递增 Min_Index 以指向下一个元素第 5 步重复该步骤，直到整个数组排序完毕

继续这篇关于 Java 中选择排序的文章

## **选择排序示例**

xarray[] = 15 10 99 53 36

找到数组[0…4]中最小的元素，并将其与开头的元素交换

找出 arr[1…4]中的最小元素。因为 15 是下一个最小的元素，所以移到下一个元素。10 15 99 53 36

找出 arr[2…4]中的最小元素，并将其与第三个元素 10 15 36 53 99 交换

找出 arr[1…4]中的最小元素。因为 53 是下一个最小的元素，所以移到下一个元素。10 15 36 53 99

默认情况下，最后一个元素位于正确的位置。10 15 36 53 99

现在我们已经了解了选择排序算法的工作原理，让我们来了解如何在 Java 中实现选择排序。

## Java 中的选择**排序方法**

```
void sort(int array[])
{
int n = array.length;
// Loop to increase the boundary of the sorted array
for (int i = 0; i < n-1; i++)
{
// Finding the smallest element in the unsorted array
int min_element = i;
for (int j = i+1; j < n; j++)
if (array[j] < array[min_element])
min_element = j;
/* Swap the smallest element from the unsorted array with the last element of the sorted array */
int temp = array[min_element];
array[min_element] = array[i];
array[i] = temp;
}
}

```

最后让我们看看执行选择排序的完整 Java 程序。

## **选择 Java 中的排序程序**

```
class SelectionSort
{
// Selection Sort Method
void sort(int array[])
{
int n = array.length;
for (int i = 0; i < n-1; i++)
{
int min_element = i;
for (int j = i+1; j < n; j++)
if (array[j] < array[min_element])
min_element = j;
int temp = array[min_element];
array[min_element] = array[i];
array[i] = temp;
}
}
// Method to print the elements of an array
void printarrayay(int array[])
{
int n = array.length;
for (int i=0; i<n; ++i)
System.out.print(array[i]+" ");
System.out.println();
}
// Main Method
public static void main(String args[])
{
SelectionSort ob = new SelectionSort();
int array[] = {15, 10, 99, 53, 36};
ob.sort(array);
System.out.println("Sorted arrayay");
ob.printarrayay(array);
}
}

```

**输出:**

![Output- Selection sort in Java- Edureka](img/7f60730bd49a32d0bbbb69b3fc80c231.png)

现在，在执行了上面的 Java 程序之后，您应该已经理解了选择排序是如何工作的&如何用 Java 实现它。我希望这篇博客能给你带来信息和附加值。这样，我们就结束了这篇关于“Java 中的选择排序”的文章。如果你想了解更多， 查看由 Edureka，一家值得信赖的在线学习公司提供的 [**Java 课程**](https://www.edureka.co/java-j2ee-training-course) 培训。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。