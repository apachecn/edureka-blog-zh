# 用实例说明如何在 C 中实现插入排序

> 原文：<https://www.edureka.co/blog/insertion-sort-in-c/>

C 中的插入排序是一个简单而有效的排序算法，它一次创建一个最终排序的数组。它通常在用户拥有少量数据集时实现。我将讨论以下主题:

*   [什么是插入排序？](#what)
*   [简单工作和复杂性](#working)
*   [C 语言中插入排序的算法](#algo)
*   [在 C 中插入排序](#code)

## **什么是插入排序？**

插入排序是一种排序算法，通过一次获取一个元素来对数组进行排序。插入排序背后的原理是获取一个元素，遍历排序后的数组&找到它在排序后的数组中的正确位置。

![Deck-insertion-sort](img/59b62a172358828f5415e4bb363a7733.png)

插入排序的工作方式类似于我们排列一副卡片。

## **简单工作和复杂性**

在每次迭代中，它将当前元素与排序后的数组中的值进行比较。如果当前元素大于数组中的元素，则它离开该元素并迭代到下一个数组元素。否则，如果当前元素小于数组元素，那么它将数组中的其余元素移动一个位置，为排序后的数组中的当前元素腾出空间。

这就是插入排序如何一次获取一个输入元素，遍历排序后的子数组，每次迭代都在正确的位置插入一个元素。这就是该算法被称为插入排序的原因。

由于该算法的平均&最坏情况复杂度为 **O(n2)** ，其中 n 为元素个数，所以插入排序对于大数据集并不好。

## **插入排序算法**

*   **步骤 1**——如果元素是第一个，则它已经被排序。

*   **步骤 2**–移动到下一个元素

*   **步骤 3**—将当前元素与排序数组中的所有元素进行比较

*   **步骤 4**–如果排序后的数组中的元素小于当前元素，则迭代到下一个元素。否则，将数组中所有较大的元素向右移动一个位置

*   **步骤 5**—在正确的位置插入数值

*   **步骤 6**——重复进行，直到完整列表排序完毕

要了解插入排序的工作原理，请参考下图。

![insertion-sort-in-c](img/a2ad2f56504b0d255efb84eb07c0baf1.png)

让我们了解一下上图中插入排序是如何工作的。

*   **122** ，17，93，3，36

为 i = 1(2 个 第二个 元素)到 36(最后一个元素)

i = 1。因为 17 比 122 小，所以移动 122，在 122 前插入 17

*   **17，122** ，93，3，36

i = 2。由于 93 小于 122，所以移动 122，在 122 前插入 93

*   **17，93，122** ，3，36

i = 3。3 将移动到开头，从 17 到 122 的所有其他元素将比它们的当前位置向前移动一个位置。

*   **3，17，93，122，** 36

i = 4。36 将移动到 17 之后的位置，从 93 到 122 的元素将比它们当前的位置提前一个位置。

*   **3，17，36，93，122**

现在我们已经理解了插入排序是如何工作的，让我们快速看一下实现插入排序的 C 代码

**插入排序功能**

```
void insertionSort(int array[], int n) 
{ 
    int i, element, j; 
    for (i = 1; i < n; i++) { element = array[i]; j = i - 1; /* Move elements of arr[0..i-1], that are greater than key by one position */ while (j >= 0 && array[j] > element) { 
            array[j + 1] = array[j]; 
            j = j - 1; 
        } 
        array[j + 1] = element; 
    } 
}
```

## **在 C 代码中插入排序**

```
#include <math.h> 
#include <stdio.h> 

// Insertion Sort Function
void insertionSort(int array[], int n) 
{ 
    int i, element, j; 
    for (i = 1; i < n; i++) { element = array[i]; j = i - 1; while (j >= 0 && array[j] > element) { 
            array[j + 1] = array[j]; 
            j = j - 1; 
        } 
        array[j + 1] = element; 
    } 
} 

// Function to print the elements of an array
void printArray(int array[], int n) 
{ 
    int i; 
    for (i = 0; i < n; i++) 
        printf("%d ", array[i]); 
    printf("n"); 
}
```

现在，在执行了上面的 C 程序之后，你应该已经理解了插入排序是如何工作的&如何用 C 语言实现它。我希望这篇博客能给你带来信息和附加值。这样，我们就结束了 C #文章中的插入排序。

C *查看 Edureka 的  [**Java 培训**](https://www.edureka.co/java-j2ee-soa-training)* *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 25 万名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*