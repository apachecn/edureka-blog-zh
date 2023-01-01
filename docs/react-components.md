# React 组件 React 中的道具和状态以及示例

> 原文：<https://www.edureka.co/blog/react-components/>

## *“在反应中，一切都是一个分量”*

如果你熟悉 React，那么你一定听过或看过这个短语很多次。但是你知道它到底是什么意思，怎么用的吗？如果你不知道，那么阅读这篇博客，了解 React 组件及其生命周期中的不同阶段。我确信当你读完  这篇博客时，你会对 React 组件及其相关概念有一个完整的理解。但是在继续之前，请快速浏览一下我将要讨论的主题:

*   [什么是 React 组件？](#1)
*   [React 组件的优点](#2)
*   [道具](#3)
*   [状态](#4)
*   [状态 vs 道具](#5)
*   [反应组件生命周期](#6)

## **什么是 React 组件？**

早先，开发人员不得不编写 1000 行代码来开发一个简单的单页应用程序。这些应用程序中的大多数都遵循传统的 DOM 结构，对它们进行更改对开发人员来说是非常具有挑战性和乏味的任务。 他们不得不手动搜索需要改变的元素并相应地更新它。即使是一个小错误也会导致应用程序失败。此外，更新 DOM 非常昂贵。因此，引入了基于组件的方法。在这种方法中，整个应用程序被分成称为组件的逻辑块。React 是选择这种方法的框架之一。如果你计划在网络开发领域发展你的职业生涯，早开始会给你带来很多机会。今天就来看看这个 [Web 开发人员课程](https://www.edureka.co/masters-program/full-stack-developer-training)，了解一下 React 组件。

现在让我们了解一下这些组件是什么。

React 组件被认为是用户界面的构建模块。这些组件中的每一个都存在于相同的空间中，但是彼此独立地执行。React 组件有自己的结构、方法和 API。它们是可重用的，可以根据需要注入到接口中。为了更好地理解，可以将整个 UI 看作一棵树。 在这里，起始组件成为根，每个独立的片段成为分支，分支又进一步分为子分支。

这使我们的 UI 保持有序，并允许数据和状态变化从根逻辑地流向分支，然后流向子分支。组件直接从客户端调用服务器，这允许 DOM 在不刷新页面的情况下动态更新。这是因为 react 组件是基于 AJAX 请求的概念构建的。每个组件都有自己的接口，可以调用服务器并更新它们。由于这些组件彼此独立，每个组件都可以刷新，而不会影响其他组件或整个 UI。

我们用**react . create class()**的方法创建一个组件。必须向该方法传递一个将定义 React 组件的对象参数。每个组件必须恰好包含一个 **render()** 方法。它是负责在 JavaScript，JSX 中解析 HTML 的组件的最重要的属性。这个 **render()** 将组件的 HTML 表示作为 DOM 节点返回。因此，所有的 HTML 标签必须包含在 **render()** 内的封闭标签中。

下面是创建组件的示例代码。

```
import React from 'react';
import ReactDOM from 'react-dom';

class MyComponent extends React.Component{
    render(){
        return(       
              <div>           
                <h1>Hello</h1>
                <h1>This is a Component</h1>
              </div>
        );
    }
}
ReactDOM.render(
    <MyComponent/>, document.getElementById('content')
);

```

**React 组件的优点**

1.  **代码可重用性**–基于组件的方法使您的应用开发更加简单快捷。如果你想在你的代码中使用一个预先存在的功能，你可以把它放在你的代码中，而不是从头开始构建。它还允许您的应用程序架构随着时间的推移保持最新，因为您可以更新需要升级的特定区域。
2.  **快速开发**——基于组件的 UI 方法导致了迭代和敏捷的应用程序开发。这些组件托管在一个库中，不同的软件开发团队可以在整个开发过程中访问、集成和修改它们。
3.  **一致性**——实现这些可重用的组件有助于保持设计的一致性，并能在整个应用程序中清晰地组织代码。
4.  **可维护性**–具有一组组织良好的组件的应用程序可以快速更新，并且您可以确信哪些区域会受到影响，哪些不会。
5.  **可伸缩性**–通过一个组织良好的现成组件库，开发变得更加容易。确保组件有正确的命名空间有助于避免样式和功能随着项目的扩大而泄漏或重叠到错误的位置。
6.  **轻松集成**——组件代码存储在像 GitHub 这样的库中，并对公众开放使用。应用程序开发团队精通使用源代码库，因此他们能够根据需要提取代码并将其注入到应用程序中。

现在你已经了解了什么是组件，它有什么优点，让我们看看如何向这些组件提供数据。

组件接收数据有两种方式:

1.  道具
2.  状态

## **道具**

道具代表属性。它们是只读组件，工作方式类似于 HTML 属性。Prop 是一种将数据从父组件传递到子组件的方法。我们用一个例子来理解这个。

正如我们已经知道的，react 组件以树的形式排列 UI，其中父组件成为根，子组件成为分支和子分支。现在假设父组件想要发送数据到它的一个嵌套很深的组件。假设您需要从组件 1 向组件 6 发送一个属性。你会怎么做？

![prop - React Components - Edureka](img/ea0e08f832362d314ff239995f7da569.png)

您不能将属性直接传递给目标组件。这是因为 React 遵循的规则是，属性必须从父组件向下流到直接的*子组件*。这意味着在发送属性时不能跳过子组件层，子组件也不能将属性发送回父组件。如果父组件没有传递属性，您可以使用默认属性，以便它们仍然被设置。这就是 React 具有单向数据绑定的原因。

![one way binding - React Components - Edureka](img/ff227abc41bddeb606e81034ecf85d60.png) 所以，在这种情况下，我们需要一层一层地发送数据，直到它到达目标子组件。该路径中的每个组件都必须从其父组件接收属性，然后将该属性重新发送给其子组件。这个过程重复进行，直到你的属性到达它的目标组件 。

![props - React Components - Edureka](img/ecf5a7b189bb242ef246b08504487104.png)

下面是一个传递道具的例子。

```
import React from 'react';
import ReactDOM from 'react-dom';

class MyComponent extends React.Component{
        render(){
        return(   
              <div>
               <h1>Hello</h1>
               <Header name="maxx" id="101"/>
           </div>
        );
    }
}

function Header(props) {
    return (              
           <div>
            <Footer name = {props.name} id = {props.id}/>
           </div>
    );
}
function Footer(props) {
    return (             
           <div>             
            <h1> Welcome : {props.name}</h1>             
            <h1> Id is : {props.id}</h1>
           </div>
  );
}
ReactDOM.render(
   <MyComponent/>, document.getElementById('content')
);

```

由于道具只能从父组件传递，所以不能更改。这使它们变得不可改变和愚蠢。这带来了巨大的挑战，因为现代的 应用程序并没有在页面加载时准备好所有的状态。Ajax 或事件可能在数据返回时发生，因此需要有人负责处理更新。这就是反应状态出现的原因。

## **州**

一般是组件取道具，渲染。这些被称为无状态组件。但是它们也可以提供用于存储关于组件的数据或信息的状态，这些数据或信息可以随时间而改变。这样的组件被称为有状态组件。 状态 的变化可以作为对用户事件或系统事件的响应而发生。换句话说， **状态** 是每个 react 组件的核心，它决定了组件的行为和呈现方式。他们还负责使组件具有动态性和交互性。因此，它们必须尽可能简单。

状态可以用 **本** 引用，如 **本. state** 。你可以使用花括号 **{}** 来访问和打印 JSX 中的变量。同样，可以在 **render()** 内渲染 **this.state** 。 必须为 组件设置默认状态，否则 将设置为空。

现在让我们看看一个 **状态** 是如何被分配给一个组件的。

```
import React from 'react';
import ReactDOM from 'react-dom';

class MyComponent extends React.Component {
    constructor() {
        super();
        this.state = {
            name: 'Maxx',
            id: '101'
        }
    }
    render()
        {
            setTimeout(()=>;{this.setState({name:'Jaeha', id:'222'})},2000)
            return (             
                   <div>                     
                     <h1>Hello {this.state.name}</h1>
                     <h2>Your Id is {this.state.id}</h2>
                   </div>
             );
        }
    }
ReactDOM.render(
    <MyComponent/>, document.getElementById('content')
);

```

## **状态 vs 道具**

## ![state vs props - React Components - Edureka](img/7f620c68ad2478c5a72f375d02fd2559.png)

## **反应元件生命周期**

React 提供了各种方法，在组件生命周期的某个阶段出现时发出通知。这些方法被称为生命周期方法。 这些生命周期方法并不十分复杂。您可以将这些方法视为在组件生命周期的不同时间点调用的专用事件处理程序。您甚至可以向这些方法添加自己的代码来执行各种任务。谈到组件的生命周期，生命周期分为 4 个阶段。它们是:

1.  初始阶段
2.  更新阶段
3.  道具变化阶段
4.  卸载阶段

每个阶段都包含一些特定的生命周期方法。现在让我们来看看每个阶段都发生了什么。

**a .初始阶段—**React 组件生命周期的第一个阶段是初始阶段或初始呈现阶段。在这个阶段， 组件即将开始它的旅程，向 DOM 前进。这个阶段由以下方法组成，这些方法按预定义的顺序调用。

1.  ***getDefaultProps():*****该方法用于指定******的默认值。它甚至在你的组件被创建或者父组件的任何属性被传递给它之前就被调用了。****
2.  **【getInitialState():**该方法用于在组件创建前 指定****的默认值。****
3.  ***componentWillMount():*****这是组件呈现到 DOM 之前可以调用的最后一个方法。但是如果你在这个方法里面调用******setState()**你的组件就不会重新呈现。**
4.  ***render():***Th**is 方法负责返回单个根 HTML 节点，必须在每一个组件中定义。你可以返回******null**或**false****以防你不想渲染任何东西 。
5.  ***componentidmount():***一旦组件被渲染并放置在 DOM 上，这个 方法就被调用。在这里，您可以执行任何 DOM 查询操作。

**b .更新阶段—**一旦组件被添加到 DOM 中，它们只有在发生状态变化时才能更新和重新渲染。每次状态改变时，组件再次调用其 **render()** 。任何依赖于该组件输出的组件也会再次调用其**【render()**。这样做是为了确保我们的组件显示自己的最新版本。因此，为了成功更新组件状态，按照给定的顺序调用以下方法:

1.  ***【shouldcomponentdupdate():***使用这个方法你可以控制你的组件更新自身的行为。如果从该方法返回 true， 组件将更新。否则，如果该方法返回一个假，组件将跳过更新。
2.  ***componentWillUpdate():***T他的方法是在你的组件即将更新之前调用just。在这个方法中，你不能通过调用**this . setstate**来改变你的组件状态。
3.  ***render():***如果您通过**shouldComponentUpdate()**返回 false，那么 **render()** 内部的代码将被再次调用，以确保您的组件能够正常显示。
4.  ***【componentDidUpdate():***一旦组件被更新和渲染，那么这个方法就被调用。您可以将任何代码放入该方法中，以便在组件更新后执行。

**c .道具变化阶段——****组件被渲染到 DOM 后，除了状态变化之外，组件唯一会更新的时间就是其道具值变化的时候。实际上，这一阶段的工作与前一阶段类似，但是它处理的不是状态，而是道具。因此，这个阶段只有一个来自更新阶段的附加方法。**

1.  ***componentWillReceiveProps():***该方法返回一个参数，该参数包含将要分配给组件的新属性值。其余的生命周期方法的行为与我们在上一阶段看到的方法相同。
2.  ***【shouldcomponentdupdate()***
3.  ***【组件更新()】***

5.  ***【componentDidUpdate()***

**d. 卸载阶段—这是组件生命周期的最后一个阶段，在这个阶段，组件被销毁并从 DOM 中完全删除。它只包含一种方法:**

1.  ***componentWillUnmount():***一旦这个方法被调用，你的组件就被从 DOM 中永久删除了。 在这个方法中，y ou 可以执行任何与清理相关的任务，如删除事件监听器、停止计时器等。

以下是整个生命周期图:

![lifecycle of components - React Component - Edureka](img/a03d1b67a050ef3787937bf826749c0d.png)  这就把我们带到了 React 组件博客的结尾。我希望在这篇博客中，我能够清楚地解释什么是 React 组件，它们是如何使用的。你可以参考我在 [** ReactJS 教程**](https://www.edureka.co/blog/reactjs-tutorial) 上的博客，如果你想了解更多关于 ReactJS 的知识。

*如果你想接受 React 的培训，并希望自己开发有趣的 UI，那么就去看看 Edureka 的 [**React 课程**](https://www.edureka.co/reactjs-redux-certification-training) **或 [Web 开发认证](https://www.edureka.co/masters-program/web-developer-training)** 培训，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。*

*有问题吗？请在评论区提到它，我们会给你回复。*