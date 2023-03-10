# 什么是反应？–使用 React 揭开交互式用户界面的神秘面纱

> 原文：<https://www.edureka.co/blog/what-is-react/>

## **什么是反应？**

你还记得几年前脸书的 UI 或者它的 messenger 是什么样子吗？在那段时间里，你不得不为新的更新或消息反复刷新或重新加载整个页面。但是现在已经不需要了。今天，每次有新的更新或消息时，都会弹出通知。点击它会自动刷新你的页面并显示最新的更新。 那么，这到底是怎么发生的呢？ 这就是 ReactJS 的神奇之处，在这篇博客中，我将讨论什么是 React 以及为什么你应该追求 React。但是在我们继续了解什么是 react 之前，让我们先来看看我将要讨论的主题:

*   [JavaScript 框架](#1)
*   [为什么会有反应？](#2)
*   [什么是反应？](#3)
*   [反应过来的特征](#4)

*Javascript* is a dynamic programming language which is widely used for developing web applications. It is very lightweight and is supported by most of the modern browsers. Moreover, JavaScript supports both object-oriented programming and procedural programming. Thus, it is used for creating web pages with a client-side script to interact with the user and make the web pages dynamic and robust.JavaScript has many frameworks among which we can choose depending on our need. Below diagram shows some popular JavaScript frameworks.

以下是 JavaScript 框架提供的主要优势:

1.  **效率:** 通过使用预建的模式和函数，应用程序的开发变得很容易。过去需要几个月开发的项目现在可以在很短的时间内完成。这提高了效率，也减少了时间和精力。
2.  **安全性:** 由于 JavaScript 是一个开源社区，其顶层框架都有很强的安全性安排。这些大型社区支持框架，其中的成员和用户也可以充当测试人员。这增加了检测框架中存在的任何后门或 bug 的机会。从而以更低的成本提供更好的安全性。
3.  **降低成本:** JavaScript 框架由于是开源的，所以可以免费公开使用。因此，当我们使用这些框架开发一个 web 应用程序时，应用程序的总成本要低得多。

由于所有这些优势，JavaScript 框架被大量用于开发网络应用。在过去的几年里，他们已经证明了自己的潜力。其中最受欢迎的是 React 和 Angular。” ***纵然反应过来是  的年轻，却是给了一个不分上下竞争地棱角分明的**。* 如果你打算在 web 开发领域大展宏图，那么 ***React 认证培训*** 是你的最佳选择。查看过去 7 年 React 和 Angular 的谷歌趋势结果。![react vs angular - What Is React - Edureka](img/60bfff71b17e5b5277eea7328283a63f.png)

因此，通过这个博客，我们将了解所有关于 ReactJS 的信息。 但是在了解什么是 React 之前，你首先需要明白我们为什么需要它。如欲了解更多信息，请立即查看此[全栈开发课程](https://www.edureka.co/masters-program/full-stack-developer-training)。

## **为什么会有反应？**

市场上有如此多的 JavaScript 框架，但 React 仍然占据了一席之地。让我们再深入一点，找出需要 ReactJS 的原因。

从下图可以看出，以前的框架使用的是传统的数据流。

![traditional data flow - What is React - Edureka](img/a1e4a3625017cf12fb96cfc16680e980.png)

这里，数据是从各种来源接收的，如初始数据、实时数据和传递给调度程序的用户输入数据。然后，调度程序将这些数据转发到商店，最终从商店到达视图。现在，视图是您或用户与应用程序交互的部分。所以，你在浏览器上看到的网页就是视图本身。

但是，您认为使用这种传统数据流的框架的后端会发生什么？

每次在后端添加新数据或更新任何数据时，浏览器都会重新加载网页并再次重复整个过程。只有在这个 之后，我们才能在视图上看到更新后的数据。 但是这种传统的数据流有一个主要缺点，它使用了 **DOM** (文档对象模型)。DOM 是浏览器每次加载网页时创建的对象，可以在后端动态添加或删除数据。但是每次修改后，都会为同一个页面创建一个新的 DOM。DOM 的重复创建导致了不必要的内存浪费和应用程序性能的下降。在印度和美国，React JS 是所有其他 [Web 开发人员培训](https://www.edureka.co/complete-web-developer)课程中需求量最大的。

此外，操纵 DOM 的 *非常昂贵* 。因此，人们寻求新的技术来拯救我们。这就是 ReactJS 来拯救我们的地方。使用 ReactJS，您可以将整个应用程序分成不同的独立组件。ReactJS 应用程序仍然使用相同的传统数据流，但是在后端发生了一些变化。下图显示了后端到底发生了什么。

![traditional data flow - What is React - Edureka](img/b9b24dc4161a06920bdcedf08314c780.png)现在，每次从后端添加或更新任何数据时，ReactJS 都会使用新的策略来处理。React 所做的不是重新加载整个页面，而是破坏旧的视图。之后，它用更新或新数据呈现视图组件，然后用新视图代替旧视图。作为对 DOM 造成的内存浪费的解决方案，React 引入了**虚拟 DOM。** 你可能会好奇这个虚拟 DOM 是什么，它是如何解决我们的问题的？别担心，我会在稍后的博客中详细解释，但是现在，让我们先了解一下什么是反应。

## **什么是反应？**

React 是一个基于组件的库，用于开发交互式 UI(*用户界面*)。它是目前最受欢迎的 JavaScript 前端库之一，拥有强大的基础和支持它的大型社区。

*注:ReactJS 只是一个前端库，并不是整个框架，它处理**MVC**(Model-**View**-Controller)的 **View** 组件。*

![lego - What Is React - Edureka](img/84591814fd200abb74be782398e80f72.png)

在 ReactJS 中，一切都是组件。将一个乐高房子视为一个完整的应用程序。然后将每个乐高积木与一个作为积木的组件进行比较。这些块/组件被集成在一起以构建一个更大的动态应用程序。

使用组件的最大好处是你可以在任何时间点改变任何组件，而不会影响应用程序的其他部分。当在数据频繁变化的大型实时应用程序中实现时，此功能最为有效。 每次添加或更新任何数据时，ReactJS 都会自动更新其状态已经*实际上*改变的特定组件。这将浏览器从重新加载整个应用程序以反映更改的任务中解救出来。

ReactJS 是由在脸书工作的软件工程师乔丹·沃克开发的。脸书于 2011 年在其*新闻订阅*部分实现了 ReactJS，但它于 2013 年 5 月向公众发布。ReactJS 实施后，脸书的用户界面得到了极大的改善。这导致了满意的用户和它的受欢迎程度的突然提高。

## **反应过来的特征**

既然你已经理解了什么是 React 以及为什么使用它，现在让我们揭开它的一些有趣的特性。

1.  JSX 代表 JavaScript XML。React 使用类似 XML/ HTML 的语法。它扩展了 ECMAScript，使 XML/ HTML 之类的文本可以与 JavaScript react 代码共存。 这个语法被像 *Babel* 这样的预处理程序用来将 JavaScript 文件中的 HTML 类文本转换成标准的 JavaScript 对象。使用 JSX，我们可以更进一步，再次将 HTML 代码嵌入到 JavaScript 中。这使得 HTML 代码易于理解，  提高了 JavaScript 的性能，同时使我们的应用程序更加健壮。**![jsx - What Is React - Edureka](img/08eaf94c10276e0043dae3b9786b3ff6.png)**让我们看看如何用 JSX 编写 Hello World 程序。script . jsx

    ```
    var MyComponent = React.createClass({
        render :function () {
                    return(    
                    <h2>Hello World</h2>
            );
        }
    });

    ReactDOM.render(
       <MyComponent/>, document.getElementById('content')
    );
    ```

2.  **Virtual DOM**: Like an actual DOM, *virtual DOM* is also a node tree that lists the elements and their attributes and content as Objects and their properties. React’s render function creates a node tree out of the React components. Then, it updates this tree in response to the mutations in data model caused by various actions done either by the user or by the system.

    这个*虚拟 DOM* 在**三个简单的步骤**中起作用。

    这使得我们的应用程序更快，并且没有内存浪费。

3.  **可测性** : React 视图可以作为状态的函数使用(状态是一个决定组件如何渲染和行为的对象)。因此，我们可以轻松地操作传递给 ReactJS 视图的组件状态，并查看输出和触发的动作、事件、函数等。这使得 React 应用程序非常容易测试和调试。
4.  **服务器端渲染(SSR):** 服务器端渲染只允许在服务器端预渲染 react 组件的初始状态。有了 SSR，服务器对浏览器的响应就变成了现在可以呈现的页面的 HTML。因此，浏览器现在可以开始呈现，而不必等待加载和执行所有 JavaScript。因此，网页加载速度更快。在这里，尽管 React 仍在下载 JavaScript、创建虚拟 DOM、链接事件等，用户仍能看到网页。在后端。【T8**![SSR - What Is React - Edureka](img/4fefbd694f2cbb4a4348e2f3b2557682.png)**
5.  **单向数据绑定:** 与其他框架不同，ReactJS 遵循单向数据流或单向数据绑定。单向数据绑定的主要优点是，在整个应用程序中，数据是单向流动的，这使您可以更好地控制它。因此，应用程序的状态包含在特定的存储中，因此，其余组件保持松散耦合。这使得我们的应用程序更加灵活，从而提高了效率。**![One way data binding - What Is React - Edureka](img/22a3223a340877fd7ddbb4522e3e367e.png)**
6.  **简单:**使用 JSX 文件使得应用程序真正简单容易 ![learning curve - What Is React - Edureka](img/10c55a0f0a25399e29d069b187b6c455.png)   编写  以及理解。尽管我们可以在这里使用普通的 JavaScript，但使用 JSX 更容易。React 基于组件的方法以及独特的生命周期方法也使其易于学习。
7.  **学习曲线:**与其他框架相比，React 的学习曲线相当低。任何一个有编程基础知识的人都可以很容易地学会 React。所以，如果你以前有 HTML 和 JavaScript 的知识，你可以很快掌握它。

这就把我们带到了关于*什么是反应的博客的结尾。*希望我能够清楚地解释什么是 React 以及为什么你应该使用它。你可以参考这个 [**ReactJS 教程**](https://www.edureka.co/blog/reactjs-tutorial) ，万一你想了解更多关于 ReactJS 的知识。

*如果你想接受 React 培训，并希望自己开发有趣的 UI，那就去看看 Edureka 提供的 **best React 课程**，我们的 **[React 课程大纲](https://www.edureka.co/reactjs-redux-certification-training)，**由行业专家策划，将帮助你掌握它的所有概念。*

*有问题吗？请在评论区提到它，我们会给你回复。*