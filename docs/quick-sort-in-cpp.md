# 关于 C++中的快速排序，你需要知道的是

> 原文：<https://www.edureka.co/blog/quick-sort-in-cpp>

有太多的排序算法。为您的应用找到合适的解决方案是一项任务，需要对性能、时间复杂度、代码长度等因素有一个简单的了解。一个特定的算法。在这篇文章中，我们将按照以下顺序来看看在 C++中实现快速排序所需的所有基本概念:

*   [了解快速排序算法](#understand)
*   [伪代码为快速排序](#pseudocode)
*   [c++中的快速排序程序](#program)
*   [时间复杂度快速排序](#complexity)

## **了解快速排序算法**

就像[合并排序](https://www.edureka.co/blog/merge-sort-in-cpp)，快速排序遵循分而治之的策略。通过使用分治策略，我们将问题分成许多子问题，并递归地解决它们。首先，我们将一步一步地理解整个过程，然后，在一个例子的帮助下，我们将对整个过程有一个深刻的理解。

1.  首先，我们将向用户询问未排序的数组。

2.  一旦我们有了未排序的数组，我们需要从数组中选择一个枢纽值。我们可以选择任何值。

3.  一旦我们选择了中枢点，我们需要以这样的方式排列数组的其他元素，所有小于中枢值的元素都应该放在中枢值的右边，所有大于中枢值的元素都应该放在中枢值的右边。

4.  我们执行第 3 步，直到得到排序后的数组。

现在，让我们考虑一个例子，实现这个算法，看看它是如何工作的。

你好[5，4，1，11，9，6，2，3]在这个例子中，我们将始终把轴心视为列表中最右边的元素。

![Quicksort in C++](img/97b740f6187fb1959b7b754637f3f29e.png)

让我们来看一下每一步，并理解我们用来解决问题的逻辑。

*   首先，我们选择“3”作为我们的枢纽，并在右侧排列所有小于“3”的元素，在右侧排列所有大于“3”的元素。

*   在这一点上，我们有两个子问题。让我们先解决右边的子问题。我们选择一个作为我们的枢纽，并把 2 放在右边。

*   为了解决第二个子问题，我们选择“6”作为支点，并按照我们之前讨论的方式放置元素。

*   我们还有两个子问题。第一个问题通过选择 4 作为主元来解决，第二个问题通过选择 9 作为主元来解决。最后，我们有一个排序后的数组，元素放在下划线索引处。

**注意-** 这里需要理解的重要一点是，所有的操作都发生在同一个数组中。不会创建新数组。

## **c++中快速排序的伪代码**

```
QuickSort(array[], start_index, end_index)
{
    if (start_index < end_index)
    {
        partition_index = partition(array, start_index, end_index);

        QuickSort(array, start_index, partition_index - 1);         QuickSort(array, partition_index + 1, end_index);
    }
}
```

## **c++中的快速排序程序**

我们理解了算法，并对算法的工作有了深刻的理解。让我们用 C++实现 Quicksort，写一个对数组排序的程序。

```
#include <iostream>

using namespace std;

void swap_elements(int* a, int* b) 
{ 
    int temp = *a; 
    *a = *b; 
    *b = temp; 
} 

int partition (int array[], int start_index, int end_index) 
{ 
    int pivot = array[end_index];    
    int i = (start_index - 1);  

    for (int j = start_index; j <= end_index- 1; j++) 
    { 

        if (array[j] <= pivot) 
        { 
            i++;     
            swap_elements(&array[i], &array[j]); 
        } 
    } 
    swap_elements(&array[i + 1], &array[end_index]); 
    return (i + 1); 
} 

void quickSort(int array[], int start_index, int end_index) 
{ 
    if (start_index < end_index) 
    { 

        int partition_index = partition(array, start_index, end_index); 

        quickSort(array, start_index, partition_index - 1); 
        quickSort(array, partition_index + 1, end_index); 
    } 
} 

void printArray(int array[], int number) 
{ 
    int i;
    cout<<"Sorted Array: ";

    for (i = 0; i < number; i++)  
        cout << array[i] << " ";  
    cout << endl;
}

int main() 
{ 
     int Hello[30]; 
    int i;
    int NumberofElements;
    cout<<"Enter the number of elements to be sorted:"; cin>>NumberofElements;
    cout<<"Enter the elements one by one: ";

    for(i=0;i<NumberofElements;i++) { cin>>Hello[i];
    }

    quickSort(Hello, 0, NumberofElements-1); 

    printArray(Hello, NumberofElements); 
    return 0; 
}
```

**输出:**

![Output-1](img/177225f700bd9c315e432481ad21b3f4.png)

## **时间复杂度**

让我们来谈谈任何排序算法最重要的方面，即时间复杂度。它告诉我们算法在各种情况下的性能。这些值可以帮助我们决定是否可以在我们的应用程序中使用该算法。

*   **最佳情况-** O(n)
*   **平均情况-**【nlogn】
*   **最坏情况-**O(n2)

至此，我们结束了这篇 C++快速排序文章。如果你想了解更多，请查看由 Edureka(一家值得信赖的在线学习公司)提供的  [Java 培训](https://www.edureka.co/java-j2ee-soa-training)。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。