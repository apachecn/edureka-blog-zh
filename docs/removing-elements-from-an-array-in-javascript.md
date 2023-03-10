# 在 JavaScript 中从数组中移除元素

> 原文：<https://www.edureka.co/blog/removing-elements-from-an-array-in-javascript/>

通常情况下，不需要操纵一个凭空出现的数组。这种操作有多种方法，其中一种包括去除元素的方法。在本文中，我将带您了解在 [JavaScript](https://www.edureka.co/blog/what-is-javascript/) 中从数组中移除元素的各种方法。以下是本文将关注的要点，

*   [弹出方法](#PopMethod)
*   [换档方式](#ShiftMethod)
*   [拼接方法](#SpliceMethod)
*   [元素范围的拼接](#SpliceForRangeOfElements)
*   [按值删除元素](#RemoveElementsByValue)
*   [按值删除元素范围](#RemoveRangeOfElementsByValue)
*   [数组过滤方法](#ArrayFilterMethod)

让我们开始吧，

## **在 JavaScript 中从数组中移除元素**

## **弹出方法**

pop()方法从数组末尾移除元素，就像堆栈一样。另一方面，push()方法将元素添加到数组的末尾。 方法实现了后进先出(LIFO)的概念。

```

["Rock", "Metal", "Blues", "Jazz"]
list.pop()
["Rock", "Metal", "Blues"]

```

代码删除数组中的最后一个元素，即“Jazz”。push()方法将元素追加回数组。

## **Shift 方法:在 JavaScript 中从数组中移除元素**

方法的作用是:移除数组开头的元素。另一方面，unshift()方法将元素添加回数组的开头。

```

["Rock", "Metal", "Blues", "Jazz"]
list.shift()
["Metal", "Blues", "Jazz"]

```

代码从数组中删除第一个元素，即 Rock。 在使用 unshift()方法时，“岩石”将被添加回数组。

## **拼接方法**

splice()方法删除数组中特定的或有选择的部分。 它被证明是足智多谋的删除、替换或添加元素到数组的方法。

```

["Rock", "Metal", "Blues", "Jazz"]
list.splice(2, 1)
// Starting at index position 2, remove one element
["Rock", "Metal", "Jazz"]
list.splice(2,2)
// Starting at index position 2, remove two elements
["Rock", "Metal"]

```

在上面的例子中，slice 方法根据指定的索引删除元素。

“Blues”从第一个示例中删除，因为它位于索引 2 处。

在第二个例子中，移除了两个元素，即“布鲁斯”和“爵士乐”，因为索引指定必须从索引 2 开始移除 2 个元素。

必须注意，在 JavaScript 中数组是零索引的。

继续，这篇关于用 JavaScript 从数组中移除元素的文章，

## **元素范围的拼接**

使用 splice()方法移除连续元素似乎可行:

```

["Rock", "Metal", "Blues", "Jazz"]
list.splice(0, 2)
// Starting at index position 0, remove two elements
["Blues", "Jazz"]

```

该代码删除拼接方法中提到的值。

## **通过值移除元素:在 JavaScript 中从数组中移除元素，**

我们可以使用 splice()搜索一个元素，并连续删除它。 该方法可以与 indexOf()命令配合使用，该命令返回可以找到给定元素的第一个索引。如果没有找到该元素，它将返回-1 作为输出。

在下面的例子中，我们删除了元素“蓝调”:

```

["Rock", "Metal", "Blues", "Jazz"]
// Find the index position of "Blues," and remove one element from that position
list.splice( list.indexOf('Blues'), 1 );

```

代码在找出元素的索引位置后，删除元素“Blues”。

## **按值删除元素范围**

JavaScript 允许我们从数组中移除多个元素。

```

["Rock", "Metal", "Blues”, “Blues", "Jazz"]
for( var i = list.length-1; i--;){
if ( list[i] === 'Blues') list.splice(i, 1);
}
["Rock", "Metal", "Jazz"]

```

代码删除所有出现的元素“Blues”。

让我们从本文最后一点开始，用 JavaScript 从数组中移除元素，

## **数组过滤方法**

filter()创建了一个新数组，而不是改变调用它的数组。 它有一个单一的参数，称为回调方法。当 filter 方法迭代数组的元素时，回调方法被触发。查看这个[全栈开发课程](https://www.edureka.co/masters-program/full-stack-developer-training)，了解更多关于 Javascript 的知识。

它向回调函数传递三个值:

*   当前值
*   当前数组索引
*   全阵

它返回两个值:真或假。返回 true 的元素被添加到由过滤器()创建的新数组中。

```

var array = [1, 2, 3, 4, 5, 6, 7, 8, 9, 0];
var filtered = array.filter(function(value, index, arr){
return value > 4;
});
//filtered => [5,6, 7, 8, 9]

```

过滤后的数组由证明为真的元素组成。

从数组中移除元素本质上可能有点乏味，但事实上，这些方法是最高效和最灵活的。

至此，我们结束了这篇关于“用 JavaScript 从数组中移除元素”的博客。我希望你发现这是有益的，请继续关注更多类似主题的教程。您也可以查看我们的培训计划 t 以深入了解 jQuery 及其各种应用程序，您可以 [**在此**](https://www.edureka.co/masters-program/full-stack-developer-training) 注册在线实时培训，24/7 全天候支持，终身访问。

有问题要问我们吗？在这个博客的评论部分提到他们，我们会回复你。