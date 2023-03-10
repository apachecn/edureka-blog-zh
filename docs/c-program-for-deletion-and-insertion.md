# 如何写一个删除和插入的 C 程序？

> 原文：<https://www.edureka.co/blog/c-program-for-deletion-and-insertion/>

这篇关于 C [程序](https://www.edureka.co/blog/object-oriented-programming-in-cpp/)删除和插入的文章将向您介绍在 C 数组中删除和插入元素的基础知识。本文将涉及以下几点:

那么让我们开始吧

## **删除和插入的 C 程序**

数组是任何编程语言的基础。要掌握任何编程语言，你需要精通数组。在这个博客中，我们将学习如何使用 C 编程语言在数组中执行插入、删除和搜索等基本操作。

让我们首先了解如何在数组中搜索给定的元素。

## **查找数组中的元素**

要搜索数组中的元素，需要使用 loop 遍历数组并搜索给定的元素。

那么让我们继续用这个 C 程序来删除和插入文章，

## **C 函数搜索数组中的一个元素**

```
int findElement(int array[], int size, int keyToBeSearched) 
{ 
int i; 
// Finding & returning the position of the element 
for (i = 0; i < size; i++) 
if (array[i] == keyToBeSearched) 
return i; 
return - 1; 
}

```

那么让我们继续用这个 C 程序来删除和插入文章，

## **C 程序搜索数组中的一个元素**

```
#include<stdio.h> 
// Function to find the element for deletion
// where array[] is the array from which element needs to be deleted
// size is the size of the array
// keyToFind is the element to be deleted from the array
int findElement(int array[], int size, int keyToBeSearched) 
{ 
int i; 
// Finding & returning the position of the element 
for (i = 0; i < size; i++) 
if (array[i] == keyToBeSearched) 
return i; 
return - 1; 
}  
// Main Function 
int main() 
{ 
int array[] = { 31, 27, 3, 54, 67, 31 };
int size = sizeof(array) / sizeof(array[0]); 
int keyToBeSearched = 67; 
// Calling the function to delete an element from the array
int pos = findElement(array, size, keyToBeSearched); 
if(pos==-1){
printf("n Element %d not found", keyToBeSearched);
}
else{
printf("n Position of %d: %d", keyToBeSearched ,pos+1);
}
return 0; 
}

```

**输出**

![Output- C Program to delete or Insert an Element in an Array- Edureka.png](img/4aea09e2b2ba771b9474f33a2074006f.png)

那么让我们继续用这个 C 程序来删除和插入文章，

## **在数组中插入元素**

与排序数组相比，在未排序数组中插入元素速度更快。这是因为在未排序的数组中，您不必担心元素的新位置。新元素的位置是数组中的最后一个位置。

您需要检查数组的总长度。如果数组未满，可以在最后一个位置添加元素。

让我们看看在数组中插入元素的 C 函数。

## **C 函数在数组中插入一个元素**

```
//Function to insert an element in an array.
//arr[] = array, elements = number of elements present in the array
//keyToBeInserted = element to be inserted in the array
// size of the array
int insertElement(int arr[], int elements, int keyToBeInserted, int size) 
{ 
// Check if the capacity of the array is already full 
if (elements >= size) 
return elements; 
//If not then the element is inserted at the last index 
//and the new array size is returned
arr[elements] = keyToBeInserted; 
return (elements + 1); 
}

```

那么让我们继续用这个 C 程序来删除和插入文章，

## **C 程序在数组中插入一个元素**

**例子**

```
#include<stdio.h> 
//Function to insert an element in an array.
//arr[] = array, elements = number of elements present in the array
//keyToBeInserted = element to be inserted in the array
// size of the array
int insertElement(int arr[], int elements, int keyToBeInserted, int size) 
{ 
// Check if the capacity of the array is already full 
if (elements >= size) 
return elements; 
//If not then the element is inserted at the last index 
//and the new array size is returned
arr[elements] = keyToBeInserted;   
return (elements + 1); 
}  
// Main Function 
int main() 
{ 
int array[20] = { 31, 27, 3, 54, 67, 31 };
int size = sizeof(array) / sizeof(array[0]); 
int elements = 6; 
int i, keyToBeInserted = 32; 
printf("n Before Insertion: "); 
for (i = 0; i < elements; i++) 
printf("%d  ", array[i]); 
// Calling the function to insert the element in the array
elements = insertElement(array, elements, keyToBeInserted, size); 
printf("n After Insertion: "); 
for (i = 0; i < elements; i++) 
printf("%d  ",array[i]); 
return 0; 
}

```

**输出:**

![Output- C Program to delete or Insert an Element in an Array- Edureka.png](img/e13b95df320c642ef911fe524e8b506a.png)

接下来我们将了解如何从数组中删除一个元素。

## **从数组中删除元素**

要删除数组中的元素，我们需要首先搜索元素。然后我们需要删除该元素，并将其余的元素向左移动。

我们来看看 c 中的删除函数。

## 从数组中删除一个元素的函数

```
// Function to delete an element
// where array[] is the array from which element needs to be deleted
// size is the size of the array
// keyToBeDeleted is the element to be deleted from the array
int deleteElement(int array[], int size, int keyToBeDeleted) 
{ 
// Calling findElement function to get the position of the element which needs to be deleted
int pos = findElement(array, size, keyToBeDeleted); 
// If element is not found then it prints Element not found
if (pos == - 1) 
{ 
printf("Element not found"); 
return size; 
} 
// Otherwise it deletes the element & moves rest of the element by one position
int i; 
for (i = pos; i < size - 1; i++) 
array[i] = array[i + 1]; 
return size - 1; 
} 

```

那么让我们继续用这个 C 程序来删除和插入文章，

## C 程序从数组中删除一个元素

**例子**

```
#include<stdio.h> 
// Function to delete an element
// where array[] is the array from which element needs to be deleted
// size is the size of the array
// keyToBeDeleted is the element to be deleted from the array
int deleteElement(int array[], int size, int keyToBeDeleted) 
{ 
// Calling findElement function to get the position of the element which needs to be deleted
int pos = findElement(array, size, keyToBeDeleted); 
// If element is not found then it prints Element not found
if (pos == - 1) 
{ 
printf("Element not found"); 
return size; 
} 
// Otherwise it deletes the element & moves rest of the element by one position
int i; 
for (i = pos; i < size - 1; i++) 
array[i] = array[i + 1]; 
return size - 1; 
} 
// Function to find the element for deletion
int findElement(int array[], int size, int keyToBeDeleted) 
{ 
int i; 
// Finding & returning the position of the element 
for (i = 0; i < size; i++) 
if (array[i] == keyToBeDeleted) 
return i; 
return - 1; 
}   
// Main Function 
int main() 
{ 
int array[] = { 31, 27, 3, 54, 67, 31 };
int size = sizeof(array) / sizeof(array[0]); 
int i, keyToBeDeleted = 67; 
printf("n Before Deletion: "); 
for (i = 0; i < size; i++) 
printf("%d  ", array[i]); 
// Calling the function to delete an element from the array
size = deleteElement(array, size, keyToBeDeleted); 
printf("n After Deletion: "); 
for (i = 0; i < size; i++) 
printf("%d  ",array[i]); 
return 0; 
}

```

**输出:**

![Output- C Program to delete or Insert an Element in an Array- Edureka.png](img/3b6a84dadfe19453d2a256eb0bd9edf4.png)

现在，在浏览了上面的程序之后，你应该已经理解了如何在 C 语言中执行基本的数组操作。这就把我们带到了这篇关于删除和插入 C 程序的文章的结尾，

如果你想了解更多， 请查看 Edureka 值得信赖的在线学习公司提供的 [**Java 培训**](https://www.edureka.co/java-j2ee-soa-training) 。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这篇文章的评论部分提到它，我们会尽快回复你。