# 如何在 C 中实现堆排序？

> 原文：<https://www.edureka.co/blog/heap-sort-in-c/>

电脑真的很擅长整理东西。他们可以立即完成复杂的分类任务。留给我们的唯一事情是告诉他们给定排序任务要使用的方法。这篇文章将告诉你的计算机系统如何在 [C](https://www.edureka.co/blog/c-data-structures) 中使用堆排序来排序你的数据。

本文将关注以下几点:

*   [二元堆的基本原理](#FundamentalsofBinaryHeap)
*   [结合实例理解算法](#UnderstandingtheAlgorithmwithexample)
*   [用 C 写一个堆排序的程序](#WriteaprogramforHeapsortinC)
*   [时间复杂度](#TimeComplexity)

让我们从 C #文章中的堆排序开始，

目前，有 100 多种著名的排序算法，如果你对它们不满意，你可以用足够的数据结构、算法和排序知识来准备你自己的算法。在这篇文章中，我们将学习堆排序，这是一种广泛使用的基于二进制堆数据结构的方法。

## **二进制堆的基本原理**

除了排序应用，二进制堆还有其他应用，如优先级队列、图形算法等。二进制堆是由父节点和子节点组成的树状结构。根据父节点和子节点之间的关系，可以进一步分类为

1.  最小堆
2.  最大堆

#### **C:Min 堆中的堆排序**

Min Heap 是一棵树，其中父节点的值是 的子节点。例如，让我们考虑一个数组- [5，6，11，4，14，12，2]。 上图是给定数组的 min 堆表示。

#### **![Sample - Heap Sort In C++ - Edurekaac](img/f80654c56cb2a312de99b63fcedce9c7.png)**

#### **C 中堆排序:** **最大堆**

就父节点和子节点的关系而言，最大堆与最小堆相反。这里，父节点的值为子节点。让我们考虑同一个数组[5，6，11，4，14，12，2]

![Sample ac- Heap Sort In C++ - Edurekaac](img/1b1579a8eec973824f3ee66d0ca79321.png)

上图是给定数组的最大堆表示。现在，我们基本上知道了什么是二进制堆以及它们的类型。这些概念将极大地帮助我们理解堆排序算法。

让我们继续这篇关于 C 中堆排序的文章，

## **通过示例理解算法**

在编写程序之前，我们应该理解我们将用来对给定数组进行排序的方法。首先，我们将讨论算法，然后我们将通过一个例子来理解它。我们将使用 max heap 作为我们的用例。

1.  最初，我们会要求用户输入要排序的内容。
2.  一旦接收到数组，我们需要创建一个从数组中接收到的数字堆，以升序对它们进行排序。
3.  现在，我们需要从那个堆中创建一个最大堆。创建最大堆必须遵循一个规则，即父节点的值应该是其子节点的值 。
4.  树创建后，我们需要检查上述条件。如果子节点的值大于父节点的值，我们需要交换它们的值并再次检查，直到满足步骤 3 中提到的条件。
5.  一旦条件得到满足，并且所有元素都相应地进行了排列。我们需要将根节点与最后一个节点交换。
6.  交换后，从堆中移除最后一个节点。我们正在删除它，因为它已经排序。
7.  重复步骤 4、5 和 6，直到堆中只剩下一个元素。

通过一个例子来理解上面的算法，会让你对整个过程有深入的了解。我们将使用与上面相同的数组来使事情更有关联。

**例子**数组=【5，6，11，4，14，12，2】

![Sample ac- Heap Sort In C++ - Edurekaac](img/eecb9cfbbec36377a4fa8a3f638992de.png)

是的，我们考虑的例子是一个大例子，但是让我们理解当用 C 或其他语言实现堆排序时会发生什么，

1.  在第一步中，我们开始创建一个堆，因为 11 大于 5，我们交换它们来创建一个最大堆
2.  然后我们引入了数组的其他成员，用 14 交换 6 来创建一个最大堆
3.  在第 4 步和第 5 步中，我们分别用 11 和 5 交换了 15 和 12。
4.  在步骤 5 中，我们的最大堆被创建。
5.  我们在步骤 6 中用 2 替换了 14，因为我们在上一节中已经讨论过，一旦创建了最大堆，我们需要用最后一个节点替换第一个节点并删除最后一个节点，因此我们删除了 14
6.  为了再次创建最大堆，我们用 2 替换了 5
7.  在创建最大堆之后，我们用 12 替换了 2，并删除了 12
8.  再次创建最大堆，我们用 2 交换了 11，用 2 交换了 6，之后，我们在创建和移除最大堆时交换了 11 和 2 11
9.  在步骤 12 和 13 中，我们分别用 2 交换 6 和 4
10.  因为我们有一个最大堆，所以我们用 2 交换 6 并移除 6

此时，您会注意到数字按升序被删除，并从右到左放置在数组中

1.  在步骤 15 中，我们将 5 与 2 交换以创建一个最大堆，再次将 2 与 5 交换并移除 5
2.  一旦我们将 2 与 4 交换以创建最大堆，并再次将 4 与 2 交换以移除 4，我们就差不多完成了。
3.  最后，我们的堆中只剩下 1 个元素，即 2。
4.  将该元素放入数组的第 0 个 第 位置，算法完成。

现在让我们继续编程部分，

## 用 C 语言写一个堆排序的程序

现在，我们对将要使用的排序算法有了很好的理解。那么，我们开始吧。

```
#include<stdio.h>
#include <conio.h>
void Adjust(int Heap_of_Numbers[],int i)&nbsp; /*Function to arrange the elements in the heap*/
{
int j;
int copy;
int Number;
int Reference = 1;
Number=Heap_of_Numbers[0];
while(2*i<=Number && Reference==1)
{
j=2*i;&nbsp; &nbsp;
if(j+1<=Number && Heap_of_Numbers[j+1] > Heap_of_Numbers[j])
j=j+1;
if( Heap_of_Numbers[j] < Heap_of_Numbers[i])
Reference=0;
else
{
copy=Heap_of_Numbers[i];
Heap_of_Numbers[i]=Heap_of_Numbers[j];
Heap_of_Numbers[j]=copy;
i=j;
}
}
}
void Make_Heap(int heap[])
{
int i;
int Number_of_Elements;
Number_of_Elements=heap[0];
for(i=Number_of_Elements/2;i>=1;i--)
Adjust(heap,i);
}
int main()
{
int heap[30];
int NumberofElements;
int i;
int LastElement;
int CopyVariable;
printf("Enter the number of elements present in the unsorted Array:");
scanf("%d",&NumberofElements);
printf("nEnter the members of the array one by one:"); /* Asking for the elements of the unsorted array*/
for(i=1;i<=NumberofElements;i++)
scanf("%d",&heap[i]);
heap[0]=NumberofElements;
Make_Heap(heap);
while(heap[0] > 1) /*Loop for the Sorting process*/
{
LastElement=heap[0];
CopyVariable=heap[1];
heap[1]=heap[LastElement];
heap[LastElement]=CopyVariable;
heap[0]--;
Adjust(heap,1);
}
printf("nSorted Array:n");/*Printing the sorted Array*/
for(i=1;i<=NumberofElements;i++)
printf("%d ",heap[i]);
return 0;
}

```

我使用了相同的数组来验证我们的结果，正如您在输出窗口中看到的，我们收到了相同的结果。手动操作涉及许多步骤，有可能出错，因此这个程序可以帮助我们解决这些问题，节省我们的时间。**输出**

这就把我们带到了 C 文章中堆排序的最后一点，

#### **C 中的堆排序:** **时间复杂度**

现在，我们已经理解了所有的关键概念，我们需要检查任何算法最重要的方面，即它的时间复杂度。 对于不知道这个术语的人，这里有一个简单的解释。时间复杂度是算法计算输出所需时间的度量。

堆排序的时间复杂度为 O(nLogn)。

至此，我们结束了这篇关于“C 中的堆排序”的文章。我希望你发现这是有益的，请继续关注更多类似主题的教程。您也可以查看我们的培训计划 t 以深入了解 jQuery 及其各种应用程序，您可以 [**在此**](https://www.edureka.co/c-programming-datastructure-course-self-paced) 注册在线实时培训，24/7 全天候支持，终身访问。

有问题要问我们吗？在这篇文章的评论部分提到它们，我们会给你回复。