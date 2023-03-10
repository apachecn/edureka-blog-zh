# JavaScript 中的事件是什么，它们是如何处理的？

> 原文：<https://www.edureka.co/blog/javascript-events/>

事件是系统中发生的动作或事件。在编程的世界里， [HTML](https://www.edureka.co/blog/what-is-html/) 事件是发生在 HTML 元素上的事情。但是当在 HTML 页面中使用 [JavaScript](https://www.edureka.co/blog/javascript-tutorial/) 时，它可以对这些事件做出反应。在本文中，我们将按以下顺序了解 JavaScript 中有哪些不同类型的事件以及它们是如何工作的:

*   [JavaScript 中有哪些事件？](#what)
*   [JavaScript 中的事件类型](#types)
    *   [Onclick 事件](#onclick)
    *   [Onkeyup 事件](#onkey)
    *   [Onmouseover 事件](#mouse)
    *   [上传事件](#load)
    *   [聚焦事件](#focus)

## **JavaScript 中有哪些事件？**

Javascript 具有为网页提供动态界面的事件。这些事件连接到[文档对象模型](https://www.edureka.co/blog/html-dom) (DOM)中的元素。

另外，这些事件默认使用冒泡传播，即在 DOM 中从子节点到父节点向上传播。我们可以以内联方式或在外部脚本中绑定事件。在 JavaScript 的帮助下，您可以检测特定事件何时发生，并使事件发生以响应这些事件。

## **JavaScript 中的事件类型**

在 [JavaScript](https://www.edureka.co/blog/what-is-javascript/) 中有不同类型的事件用于对事件做出反应。在这里，我们将讨论一些著名的或最常用的事件，如:

*   **Onclick**
*   **Onkeyup**
*   **Onmouseover**
*   **加载**
*   **聚焦**

因此，让我们继续，用例子来看看 JavaScript 中的这些事件。

### **Onclick 事件**

Onclick 事件是一个鼠标事件，如果用户单击它所绑定到的元素，就会触发任何定义的逻辑。让我们举个例子，看看它是如何工作的:

```
<!doctype html>
<html>
<head>
<script>
function edu() {
alert('Welcome to Edureka!');
}
</script>
</head>
<body>
<button type="button" onclick="edu()">Click Button</button>
</body>
</html>
```

**输出:**

![Output 1 - events in javascript - edureka](img/513d52ab1d273779f3793ddc3e10b601.png)

单击该按钮后，您会收到以下警告消息:

![Output 2 - events in javascript- edureka](img/5c9dad6949c7c953567a3b91fac71a47.png)

### **Onekeyup 事件**

该事件是一个键盘事件，用于在按下某个键后释放该键时执行指令。以下示例显示了事件的工作方式:

```
<!doctype html>
<html>
<head>
<script>
var a = 0;
var b = 0;
var c = 0;
function changeBackground() {
var x = document.getElementById('bg');
bg.style.backgroundColor = 'rgb('+a+', '+b+', '+c+')';
a += 1;
b += a + 1;
c += b + 1;
if (a > 255) a = a - b;
if (b > 255) b = a;
if (c > 255) c = b;
}
</script>
</head>
<body>
<input id="bg" onkeyup="changeBackground()"
placeholder="write something" style="color:rgb(10, 99, 151)">
</body>
</html>
```

**输出:**

![](img/13f1b80a54404557fb100b053ccde615.png)

在你写了一些东西之后，它看起来像这样:

![Output 4 - events in javascript - edureka](img/495a3847c796e5526e87289bcec13704.png)

### **Onmouseover 事件**

JavaScript 中的 onmouseover 事件对应于将鼠标指针悬停在元素及其绑定到的子元素上。示例如下所示:

```
<!doctype html>
<html>
<head>
<script>
function hov() {
var e = document.getElementById('hover');
e.style.display = 'none';
}
</script>
</head>
<body>
<div id="hover" onmouseover="hov()"
style="background-color:rgb(61, 240, 225);height:400px;width:400px;">
</div>
</body>
</html>
```

**输出:**

悬停鼠标前会出现彩色框。当你将鼠标悬停在框上时，它就会消失。

![](img/3aa601593cb756cd7e946156a1a2d88c.png)

### **加载事件**

当一个元素被完全加载时，onload 事件被调用。让我们举个例子，看看它是如何工作的:

```
<!doctype html>
<html>
<head></head>
<body>
<img onload="alert('Image is loaded')"
alt="edu-Logo"
src="C:UsersxyzDesktopedureka logo.png">
</body>
</html>
```

**输出:**

![edureka logo - events in javacsript - edureka](img/e3c63e76e94866cc08391db544698f95.png)

![](img/e267b86d3f4503532b3a1694c7fe48b6.png)

### **聚焦事件**

Onfocus 事件有一个元素列表，每当它获得焦点时就执行指令。以下示例显示了 onfocus 事件的工作原理:

```
<!doctype html>
<!doctype html>
<html>
<head>
<script>
function focused() {
var e = document.getElementById('input');
if (confirm('Focus Event')) {
e.blur();
}
}
</script>
</head>
<body>
<p >Focus in the Input Box:</p>
<input id="input" onfocus="focused()">
</body>
</html>
```

**输出:**

![Onfocus - events in javascript - edureka](img/f3c3b96d4340b783c0f31b8ac9c60a8c.png)

![](img/d4e564564a7386793f21c4b3b2843410.png)

这些是 JavaScript 中最常用的一些事件。就这样，我们结束了我们的文章。我希望你明白什么是事件以及如何使用它们。

*查看我们的  [全栈 Web 开发人员硕士课程](https://www.edureka.co/masters-program/full-stack-developer-training) ，该课程包含讲师指导的现场培训和真实项目体验。本培训使您精通使用后端和前端 web 技术的技能。它包括关于 Web 开发、jQuery、Angular、NodeJS、ExpressJS 和 MongoDB 的培训。*

有问题要问我们吗？请在这个博客的评论部分提到它，我们会给你回复。