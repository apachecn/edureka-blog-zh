# 如何最好地利用 CSS 列表？

> 原文：<https://www.edureka.co/blog/css-lists/>

CSS 列表非常有助于找到一组编号或项目符号。这篇文章将向你展示如何使用 CSS 控制[网页](https://www.edureka.co/blog/category/front-end-web-development/)的类型、位置和风格。这里将涉及以下指针，

*   [CSS 属性](#CSSProperties)
*   [列表样式类型属性](#Thelist-style-typeProperty)
*   [CSS 列表:示例程序](#CSSLists:SampleProgram)
*   [列表样式位置属性中的标记值](#MarkerValuesForInlist-style-positionproperty)

那么让我们开始吧，

## **CSS 列表**

## **CSS 属性**

有五种不同的 CSS 属性可以用来控制列表:

*   List-style-type:它允许我们控制标记的形状或外观。
*   List-style-position:指定一个长点需要换行到第二行或者应该与第一行对齐或者从标记开始。
*   List-style-image:它指定应该为标记添加一个图像或使其比项目符号或编号点更吸引人。
*   列表样式:显示前面属性的简写。
*   标记-偏移:指定标记与列表中输入的文本之间的距离。

这里常用的列表有:列表-样式-类型和列表-样式-位置。下面将对其进行解释

继续这篇关于 CSS 列表的文章

## **列表样式类型属性**

在 list-style-type 属性中，它让你控制无序列表情况下的项目符号点或标记的形状和样式。在有序列表的情况下，它是编号字符。

下表表示无序列表:

| **值** | **描述** |
| ***无*** | 娜 |
| ***圆盘*** | 这是填在圆圈里的。(默认一个) |
| ***圆圈*** | 这是一个空圆圈。 |
| ***方形*** | 它被填在正方形里。 |

下表代表有序列表:

| **值** | **描述** | **例子** |
| ***Decimal*** | 是一个数字 | 1，4，3 |
| ***十进制前导零*** | 实际数前的 0 | 01，04，03 |
|  | 它是小写字母数字字符。 | a、b、c、d |
| ***上位-阿尔法*** | 是大写字母数字字符。 | A、B、C、D |
|  | 它是小写的罗马数字。 | 一、二、三、四、五 |
|  | 是大写的罗马数字。 | 一、二、三、四、五 |
| ***-希腊文*** | 标记是小写希腊语 | 阿尔法，伽马 |
| ***下拉丁语*** | 标记在低位拉丁文中 | a、b、c、d |
| ***上层拉丁文*** | 标记为拉丁文 | A、B、C、D |

继续这篇关于 CSS 列表的文章

## **CSS 列表:示例程序**

```

<ul style="list-style-type:circle;"><li>Java</li>
<li>Python</li>
<li>Angular</li>
</ul>
<ul style="list-style-type:square;">
<li>Java</li>
<li>Python</li>
<li>Angular</li>
</ul>
<ol style="list-style-type:decimal;">
<li>Java</li>
<li>Python</li>
<li>Angular</li>
</ol>
<ol style="list-style-type:lower-alpha;">
<li>Java</li>
<li>Python</li>
<li>Angular</li>
</ol>
<ol style="list-style-type:lower-roman;">
<li>Java</li>
<li>Python</li>
<li>Angular</li>
</ol>

```

**输出**

## **![Output - CSS Lists - Edureka](img/1a9a868a5bd3bd546732426f135bf166.png)**

继续这篇关于 CSS 列表的文章

## **列表样式位置属性**

## **列表样式位置属性的标记值**

在 list-style-position 属性中，它表示标记应该出现在包含项目符号点的框的内部或外部。这可以有两个值之一:

| **值** | **描述** |
| ***无*** | 娜 |
| *里面的* | 在这种情况下，如果文本在第二行，那么文本将在标记下换行。它还将显示如果列表在外面有一个值，文本将从哪里开始。 |
| *外* | 在这种情况下，如果文本进入第二行，文本将与第一行的开头对齐。 |

**举例:**

```

<ul style="list-style-type:circle; list-stlye-position:outside;"><li>Maths</li>
<li>Social Science</li>
<li>Physics</li>
</ul>
<ul style="list-style-type:square;list-style-position:inside;">
<li>Maths</li>
<li>Social Science</li>
<li>Physics</li>
</ul>
<ol style="list-style-type:decimal;list-stlye-position:outside;">
<li>Maths</li>
<li>Social Science</li>
<li>Physics</li>
</ol>
<ol style="list-style-type:lower-alpha;list-style-position:inside;">
<li>Maths</li>
<li>Social Science</li>
<li>Physics</li>
</ol>

```

**输出**

![Output - CSS Lists - Edureka](img/3c9d57216d6893c485f75f66bd27802a.png)

这就把我们带到了这篇关于 CSS 列表的文章的结尾。

*查看我们的  [全栈 Web 开发人员硕士课程](https://www.edureka.co/masters-program/full-stack-developer-training) ，该课程包含讲师指导的现场培训和真实项目体验。本培训使您精通使用后端和前端 web 技术的技能。它包括关于 Web 开发、jQuery、Angular、NodeJS、ExpressJS 和 MongoDB 的培训。*

有问题要问我们吗？请在文章的评论部分提到它，我们会给你回复。