# 如何用 Java 实现冒泡排序？

> 原文：<https://www.edureka.co/blog/bubble-sort-in-java>

排序是根据某种标准将项目按顺序排列的过程。有几种算法用于排序，其中之一是冒泡排序。冒泡排序算法被称为最简单的排序算法。所以这篇关于 *[Java](https://www.edureka.co/blog/what-is-java/)* 中的冒泡排序的文章将帮助你详细理解这个概念。

我将讨论以下主题:

*   [什么是冒泡排序？](#What_is_Bubble_sort?)
*   [Java 程序实现冒泡排序](#Implementation_through_a_Java_program)

我们开始吧！

## **什么是冒泡排序？**

在冒泡排序算法中，遍历一个数组。它从第一个元素开始，遍历到最后一个元素。将当前元素与下一个元素进行比较，如果当前元素大于下一个元素，则交换当前元素。这个过程一直持续到整个数组被排序。 我用一个例子给你解释一下算法。

**第一遍:**(**2 5**1 7 6)–>(**2 5**1 7 6)这里算法比较前两个元素。从 5 > 2 开始，它不会交换，但会继续。

(2**5 1**7 6)–>(2**1 5**7 6)在这种情况下，交换将会发生，因为 5 > 1。

(2 1**5 7**6)–>(2 1**5 7**6)它不会互换，因为 5 < 7。

(2 1 5**7 6**)–>(2 1 5**6 7**)作为 7 > 6，它互换。

**第二遍:**

(**2 1**5 6 7)–>(**1****2**5 6 7)自 1 < 2，遂其互换。(1**2 5**6 7)—>(1**2 5**6 7)

已经排序(1 2**5 6**7)–>(1 2**5 6**7)

已经排序(1 2 5**6 7**)–>(1 2 5**6 7**)

现在，我们知道 *[数组](https://www.edureka.co/blog/sort-arraylist-string-map-set-in-java/)* 已经排序，但是我们的算法不知道这个过程是否完成。该算法将再次遍历整个数组并进行检查。

**第三遍:**

(**1 2**5 6 7)->(**1 2**5 6 7)(1**2 5**6 7)->(1**2 5**6 7)(1 2**5**

经过这一关，算法理解目标完成。

现在你已经非常熟悉冒泡排序算法的工作原理，让我们进入下一部分。在这里，我将通过一个简单的 *[Java 程序](https://www.edureka.co/blog/java-programs/)* 向大家展示算法的实现。开始了。

## **Java 中的冒泡排序:通过 Java 程序实现**

```
public class BubbleSortExample {  
    static void bubbleSort(int[] arr) {  
        int n = arr.length;  
        int temp = 0;  
         for(int i=0; i < n; i++){  
                 for(int j=1; j < (n-i); j++){ if(arr[j-1] > arr[j]){  
                                 //swap elements  
                                 temp = arr[j-1];  
                                 arr[j-1] = arr[j];  
                                 arr[j] = temp;  
                         }  

                 }  
         }  

    }  
    public static void main(String[] args) {  
                int arr[] ={5,76,65,23,42,15};  

                System.out.println("Array Before Bubble Sort");  
                for(int i=0; i < arr.length; i++){  
                        System.out.print(arr[i] + " ");  
                }  
                System.out.println();  

                bubbleSort(arr);//sorting array elements using bubble sort  

                System.out.println("Array After Bubble Sort");  
                for(int i=0; i < arr.length; i++){  
                        System.out.print(arr[i] + " ");  
                }  

        }  
}
```

**输出:**

数组前冒泡排序 5，76，65，23，42，15

冒泡排序后的数组 5，15，23，42，65，76

嗯，我希望现在关于冒泡排序的模糊之处已经清楚了。

至此，我们已经到了题为“Java 中的冒泡排序”的博客的结尾。我希望这些内容能为你的 *[Java](https://www.edureka.co/blog/java-tutorial/)* 知识增添价值。

如果您发现这篇文章与“Java 中的冒泡排序”相关，请查看一下 [*Edureka Java 认证培训*、](https://www.edureka.co/java-j2ee-soa-training) 这是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。

我们在这里帮助你踏上旅程的每一步，除此之外，我们还为想成为 Java 开发人员的学生和专业人士设计了一套课程。该课程旨在让你在 Java 编程方面有一个良好的开端，并训练你掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

如果您遇到任何问题，请在“Java 中的冒泡排序”的评论区提出您的所有问题，我们的团队将很乐意回答。