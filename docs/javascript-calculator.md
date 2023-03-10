# 如何搭建一个 JavaScript 计算器？

> 原文：<https://www.edureka.co/blog/javascript-calculator/>

任何开始学习一门新语言的人，在从事真正的行业特定项目之前，都不得不费力地学习各种模块。正如我们熟悉的从“hello world”节目开始的一般惯例一样，我们可以练习学习任何语言基础的节目很少。如果你曾经尝试过系统地学习，毫无疑问，你还没有遇到“建立一个计算器”阶段。所以，今天我们将使用 [JavaScript](https://www.edureka.co/javascript-jquery-training) 构建一个基本的计算器。这里涉及的各种主题有:

*   [构建 Javascript 计算器的要求](#requirements)
*   [JavaScript 函数构建计算器](#javascriptsection)
*   [可见部分](#visiblesection)
*   [添加 CSS 口味](#css)

为了简化这个过程，当我们在这里阅读整篇文章时，让我们的编译器准备好测试是非常重要的。让我们上车吧！

被称为网页“脚本语言”的 JavaScript 可以创造奇迹。众所周知，计算器将完成我们的基本运算，即。加法、减法、乘法和除法。首先，你应该熟悉 HTML 和 CSS。JavaScript 代码部分，我们会处理的。

## **使用 JavaScript 构建计算器的要求**

*   **集成开发环境**
*   **本地服务器/在线编译器**

如果你是网站开发的新手，你应该知道在部署之前需要一个本地服务器来测试代码。您可以使用 wamp、 [xampp](https://www.apachefriends.org/download.html) 或任何其他服务器。编写代码有很多选择:Sublime Text 3、NetBeans、括号等等。一旦你完成了平台的搭建，剩下的工作就是小菜一碟了。

要链接各种文件，可以使用以下命令:

### **嵌入 CSS**

*   **内联 CSS:** 当我们想给自己想要的元素添加 CSS 时，内联 CSS 就是我们的调用。如果你是开发新手，你可能更喜欢内联 CSS 而不是其他类型。这是一个良好的开端，但肯定不是搜索引擎优化友好。
*   **内部或嵌入 CSS:**CSS 属性和规则设置在同一个 HTML 文档中，由< head >部分的< style > < /style >标签指定。
*   **外部 CSS:** 一个单独的 CSS 文件，其样式属性与根目录下的主文件相链接。

在我们的 JavaScript 计算器中，我们将使用内部 CSS。首先，我们需要计算出我们需要多少个按钮。目前，我们坚持基本计算器的最小可行功能。所以，下面提到了元素列表:

1.  **显示屏:**这将用于用户输入和输出结果。即使我们开发了完整的计算器，没有实时显示屏也没有用。
2.  **按钮:**对于一个基本的计算器，我们至少需要 17 个按钮:

为了使计算器形象化，我们最好考虑形成一个表格。表格什么都不是，只有行和列。在 CSS 的帮助下，可见部分进入主体部分。不可见的部分是 JavaScript，它位于<风格的>部分。

## **JavaScript 部分**

该部分将包括显示、求解和清除功能。

```

<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-wp-preserve="%3Cscript%3E%0A%2F%2Ffunction%20for%20displaying%20values%0Afunction%20dis(val)%0A%7B%0Adocument.getElementById(%22edu%22).value%2B%3Dval%0A%26nbsp%3B%7D%0A%2F%2Ffunction%20for%20evaluation%0Afunction%20solve()%0A%7B%0Alet%20x%20%3D%20document.getElementById(%22edu%22).value%0Alet%20y%20%3D%20eval(x)%0Adocument.getElementById(%22edu%22).value%20%3D%20y%0A%7D%0A%2F%2Ffunction%20for%20clearing%20the%20display%0Afunction%20clr()%0A%7B%0Adocument.getElementById(%22edu%22).value%20%3D%20%22%22%0A%7D%0A%3C%2Fscript%3E" data-mce-resize="false" data-mce-placeholder="1" class="mce-object" width="20" height="20" alt="&lt;script&gt;" title="&lt;script&gt;" />

```

## **可见部分**

1.  **标题:**你可以在这里写任何东西，我们更喜欢称之为“Edureka JavaScript Calculator”。
2.  **创建表格:**每一行都必须有按钮和输入功能。对于显示屏，我们需要一个带有<栏的文本输入类型，因为我们需要更长的字符串。其他的仍然是按钮类型。
3.  这里显示的只是 onclick()函数，所以我们在这里使用 dis()函数。

```

<!-- create table -->
<body>
<div class = title >Edureka JavaScript Calculator</div>
<table border="1">
<tr>
<td><input type="button" value="c" onclick="clr()"/> </td>
<td colspan="3"><input type="text" id="edu"/></td>
<!-- clr() function will call clr to clear all value -->
</tr>
<tr>
<!-- creating buttons and assigning values-->
<td><input type="button" value="+" onclick="dis('+')"/> </td>
<td><input type="button" value="1" onclick="dis('1')"/> </td>
<td><input type="button" value="2" onclick="dis('2')"/> </td>
<td><input type="button" value="3" onclick="dis('3')"/> </td>
</tr>
<tr>
<td><input type="button" value="-" onclick="dis('-')"/> </td>
<td><input type="button" value="4" onclick="dis('4')"/> </td>
<td><input type="button" value="5" onclick="dis('5')"/> </td>
<td><input type="button" value="6" onclick="dis('6')"/> </td>
</tr>
<tr>
<td><input type="button" value="*" onclick="dis('*')"/> </td>
<td><input type="button" value="7" onclick="dis('7')"/> </td>
<td><input type="button" value="8" onclick="dis('8')"/> </td>
<td><input type="button" value="9" onclick="dis('9')"/> </td>
</tr>
<tr>
<td><input type="button" value="/" onclick="dis('/')"/> </td>
<td><input type="button" value="." onclick="dis('.')"/> </td>
<td><input type="button" value="0" onclick="dis('0')"/> </td>
<!-- Evaluating function call eval()-->
<td><input type="button" value="=" onclick="solve()"/> </td>
</tr>
</table>
</body>

```

## **添加 CSS 口味**

1.  标题元素是可选的，玩玩吧
2.  边框半径保持在 10px，以便为元素提供圆角。宽度应保持在 100%，以覆盖整个跨度。
3.  文本对齐由您决定，请随意。
4.  RGB 颜色代码:#ff4456

```

<!-- for styling -->
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-wp-preserve="%3Cstyle%3E%0A.title%7B%0Aborder-radius%3A%2010px%3B%0Amargin-bottom%3A%2010px%3B%0Atext-align%3Acenter%3B%0Awidth%3A%20210px%3B%0Acolor%3A%23ff4456%3B%0Aborder%3A%20solid%20black%201px%3B%0A%7D%0Ainput%5Btype%3D%22button%22%5D%0A%7B%0Aborder-radius%3A%2010px%3B%0Abackground-color%3A%23ff4456%3B%0Acolor%3A%20black%3B%0Aborder-color%3A%23ff4456%20%3B%0Awidth%3A100%25%3B%0A%7D%0Ainput%5Btype%3D%22text%22%5D%0A%7B%0Aborder-radius%3A%2010px%3B%0Atext-align%3A%20right%3B%0Abackground-color%3Awhite%3B%0Aborder-color%3A%20black%20%3B%0Awidth%3A100%25%0A%7D%0A%3C%2Fstyle%3E" data-mce-resize="false" data-mce-placeholder="1" class="mce-object" width="20" height="20" alt="&lt;style&gt;" title="&lt;style&gt;" />

```

现在我们已经有了完整的截面，让我们把它们放在一起看看结果:

**输出画面:**

![JavaScript Calculator](img/8c079da76c36e579e2bba24484df14a8.png)

说到这里，我们的文章就到此为止了。我希望您了解构建 JavaScript 计算器的最简单方法。如果你刚刚开始，那么看看这篇 JavaScript 教程，理解基本的 Java 概念。

**JavaScript 全教程| JavaScript 初学者教程| JavaScript 培训| Edureka**

[https://www.youtube.com/embed/o1IaduQICO0](https://www.youtube.com/embed/o1IaduQICO0)

*既然你已经知道了 JavaScript 数组方法，那就去看看 Edureka 的 [Web 开发者课程](https://www.edureka.co/masters-program/full-stack-developer-training)吧。* *Web 开发认证培训将帮助您学习如何使用 HTML5、CSS3、Twitter Bootstrap 3、jQuery 和 Google APIs 创建令人印象深刻的网站，并将其部署到亚马逊简单存储服务(S3)。*

*有问题吗？请在“构建 JavaScript 计算器的最简单方法”的评论部分提到它，我们会回复您。*