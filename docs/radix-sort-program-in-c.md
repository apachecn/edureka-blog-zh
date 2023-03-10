# 如何在 C 中最好地实现基数排序程序？

> 原文：<https://www.edureka.co/blog/radix-sort-program-in-c/>

本文将向您介绍基数排序，并告诉您如何用 c 语言实现基数排序程序。本文将涉及以下指针:

*   [基数排序算法](#RadixSortAlgorithm%20)
*   [基数排序功能](#RadixSortfunction%20)
*   [计数排序功能](#CountSortFunction%20)

那么让我们开始吧，

简单来说，排序就是把给定的元素按照系统的顺序排列起来。大多数算法都进行了排序，因为排序使搜索更容易，最终使算法更有效。在这篇博客中，我们将了解一种常用的排序算法，即基数排序。

基数排序是一种非比较整数排序算法。它从最低有效位(即右边的位)到最高有效位(即左边的位)逐位排序。基数排序使用计数排序作为子例程进行排序。基于比较的排序算法(如堆排序、快速排序、归并排序)的下界是ω(nLogn)，&它们不可能提高到 nLogn 以上。如果我们谈论计数排序，它是一个线性时间排序算法，时间复杂度为 O(n+k)，其中范围位于 1 到 k 之间。现在，计数排序的问题是，当元素范围从 1 到 n2 时，它需要 O(n2)。

所以，为了对一个数组进行线性排序，我们需要基数排序。基数排序从最低有效位到最高有效位逐位对数组进行排序。基数排序使用计数排序作为子例程进行排序。

继续这篇关于 C 语言中基数排序程序的文章，

## **基数排序算法**

对所有数字执行以下步骤，从右边的最低有效数字开始，向左边的最高有效数字移动。

根据当前数字使用计数排序对元素进行排序。 **例如:**

原数组: 140，65，85，110，612，54，12，86

排序最低有效数字，即在一个人的位置，给出

140, 110, 612, 12, 54, 65, 85, 86

注意:由于 612 出现在 12 之前，并且只对一位数字进行排序，因此在这次迭代之后，612 出现在 12 之前。

按下一个数字排序，即在第 10 位，得出:

110, 612, 12, 140, 54, 65, 85, 86

按最高有效位排序，即出现在 100 位，得出:

012, 054, 065, 085, 086, 110, 140, 612

继续这篇关于 C 语言中基数排序程序的文章，

## **C 语言中的基数排序程序**

首先看基数排序函数

## **基数排序函数:**

```
void radixsort(int array[], int n) {
//Get the largest number to know the maximum number of digits
int m = getMax(array, n);
int dig;
//Counting sort is performed for every digit
for (dig = 1; m / dig > 0; dig *= 10)
countSort(array, n, dig);
}

```

继续这篇关于 C 语言中基数排序程序的文章，

## **计数排序功能:**

```
void countSort(int array[], int n, int dig) {
int output[n]; 
int i, count[10] = { 0 };
// Store count of occurrences in count[]
for (i = 0; i < n; i++)
count[(array[i] / dig) % 10]++;
// Change count[i] so that count[i] now contains actual 
//  position of this digit in output[] 
for (i = 1; i < 10; i++) count[i] += count[i - 1]; // Build the output array for (i = n - 1; i >= 0; i--) {
output[count[(array[i] / dig) % 10] - 1] = array[i];
count[(array[i] / dig) % 10]--;
}
// Copy the output array to arr[], so that arr[] now 
// contains sorted numbers according to current digit
for (i = 0; i < n; i++)
array[i] = output[i];
}

```

向前推进，让我们写一个 C 程序来实现基数排序。

**举例:**

```
#include<stdio.h>
//Function to find the Largest Number
int getMax(int array[], int n) {
int max = array[0];
int i;
for (i = 1; i < n; i++) if (array[i] > max)
max = array[i];
return max;
} 
//Function for Count sort
void countSort(int array[], int n, int dig) {
int output[n]; 
int i, count[10] = { 0 };
// Store count of occurrences in count[]
for (i = 0; i < n; i++)
count[(array[i] / dig) % 10]++; 
// Change count[i] so that count[i] now contains actual 
//  position of this digit in output[] 
for (i = 1; i < 10; i++) count[i] += count[i - 1]; // Build the output array for (i = n - 1; i >= 0; i--) {
output[count[(array[i] / dig) % 10] - 1] = array[i];
count[(array[i] / dig) % 10]--;
} 
// Copy the output array to arr[], so that arr[] now 
// contains sorted numbers according to current digit
for (i = 0; i < n; i++) array[i] = output[i]; } // The main function to that sorts arr[] of size n using Radix Sort void radixsort(int array[], int n) { //Get the largest number to know the maximum number of digits int m = getMax(array, n); int dig; //Counting sort is performed for every digit for (dig = 1; m / dig > 0; dig *= 10)
countSort(array, n, dig);
}
//Function to Print Array
void print(int arr[], int n) {
int i;
for (i = 0; i < n; i++)
printf("%d ", arr[i]);
} 
int main() {
int arr[] = { 140, 65, 85, 110, 612, 54, 12, 86 };
int n = sizeof(arr) / sizeof(arr[0]);
radixsort(arr, n);
print(arr, n);
return 0;
}

```

**输出**

![Output- Radix Sort Program in C- Edureka](img/7fabbd66bec867ad86f57bffcfea3ddd.png)

现在，在执行了上面的程序之后，你应该已经理解了 c 语言中的基数排序程序。这样，我们就结束了这篇关于“Java 中的快速排序”的文章。如果你想了解更多，请查看 Edureka 提供的 [Java 培训，这是一家值得信赖的在线学习公司。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。](https://www.edureka.co/java-j2ee-soa-training)

有问题吗？请在这个博客的评论部分提到它，我们会尽快回复你。