# React 路由器 v4 教程–为 React 应用创建路由

> 原文：<https://www.edureka.co/blog/react-router/>

在我开始这篇博客之前，我希望你已经在我的 ***[React 教程](https://www.edureka.co/blog/reactjs-tutorial)*** 博客中经历了**积木**React。如果没有，请先浏览一遍，以便更好地理解 React。在学习 React 的基础知识时，我相信您一定想知道如何在您的应用程序中添加导航。如果是这样，你就来对地方了。在这篇 **React 路由器**博客中，我将带你浏览 React 中的**路由**概念。

我们来看以下几个话题:

*   [常规路由](#conventionalRouting)
*   [我们为什么需要 React 路由器？](#whyRouter)
*   [反应中的路由](#RoutingReact)
*   [React 路由器 v4](#BenefitsRouter)的好处

## **常规路由**

一般来说，当用户在浏览器中键入一个 URL 时，一个 HTTP 请求被发送到服务器，然后服务器检索 HTML 页面。对于每个*新的 URL，*用户被重定向到一个**新的** HTML 页面。您可以参考下图来更好地理解路由是如何工作的。

## **![Basic-routing- React Router- Edureka](img/705143feb2d2da1f38b0dd0e0222b34e.png)**

那些打算在 web 开发领域大展宏图的人， ***React 认证培训*** 是适合你的选择。

## **我们为什么需要 React 路由器？**

单页面应用仅限于**单视图**并不能公平对待许多流行的社交媒体网站，如脸书、Instagram，它们使用 React today 呈现多视图。我们需要继续前进，学习如何在我们的单页应用程序中显示**多视图**。

例如，我们习惯于看到一个显示欢迎信息和相关内容的主页。该网站的背景细节可以在 “关于我们”页面上找到，用户列表和他们的详细信息列在 不同的页面上，可能有各种其他页面，包括几个不同的视图。要了解更多关于 React 的信息，请查看这个[网络开发者在线课程](https://www.edureka.co/masters-program/full-stack-developer-training)。

那么你认为这是如何实现的呢？在我们的应用程序中添加一个路由器库解决了这个需求。

## **路由在反应过来**

这就把我们带到了今天博客的主题:React 路由器 v4。2017 年 3 月 13 日，迈克尔·杰克逊&瑞安·弗洛伦斯发布了 React 路由器 v4 以及一份可靠的文档。

他们相信“学一次，路到天涯”的理念。

在 React Conf 2017 的演讲中，他们解释了这一点，展示了他们如何将他们的路由概念从 Web 无缝地投影到原生平台，以及将 **React 路由器**集成到 **VR** 中，并在 **React 原生**中创建动画。尽管他们谈话的吸引点是围绕着他们的路由器 API 是如何“T7”全部是关于组件的。

在反应过来的时候，那边只有一个**单** ' Html' 文件参与其中。 每当用户键入一个**新的** URL 请求时，路由器不是从服务器获取数据，而是为每个新的 URL 请求换入一个不同的**组件**。用户被骗在多个页面之间切换，但实际上，每个单独的**组件根据我们的需要重新呈现**实现多个视图。

a对此有何反应？

这就是**‘历史’**的概念出现的地方。 在 React 中，路由器查看每个**组件**的历史，当历史中有任何变化时，那个**组件**重新渲染。 直到路由器版本 4 我们不得不**手动**设置*历史*值。 然而，从路由器 v4 开始，<浏览器路由器>绕过了基本路径，为我们节省了大量工作。如果你还需要访问历史，HTML5 提供了一个内置的 API，允许我们通过 **pushState** 和 **replaceState** 方法修改 **History** 对象。

事实上，React Router 4 是对之前版本的完全重写。创建您自己的路线只是您已经非常熟悉的 React **组件**代码的自然扩展。尽管需要一些时间来理解，但是一旦你向前迈进，路由器 v4 将开始变得有意义。

好了，现在让我们深入了解一下第 4 版提供了什么。

## **React 路由器 v4 的好处**

我们本质上是想调用 React 的 render 方法里面的路由器组件。这是因为整个路由器 API 都是关于组件的。当然，每个组件的作用是呈现 UI，就像任何 React 应用程序一样。

**1。** **无需手动设置历史**

我们所做的就是将路由器应用组件包装在<浏览器>中。

```
ReactDOM.render((
<BrowserRouter>
<App/>
</BrowserRouter>
), document.getElementById(“root”));

```

现在，让我们借助一个例子来理解路由:

我们将创建三个页面。这是页面列表及其地址。

| **页面** | **地址** |
| 首页 | '/' |
| 关于 | ‘/关于’ |
| 话题 | '/topic' |

**2。**套餐拆分:

“react-router”库现在被分成三个独立的包。

*   **react-router-dom** :专为 web 应用设计。
*   **react-router-native** :专为移动应用设计。
*   **react-router-core:** 可以在任何地方用于核心应用。

我们需要安装依赖项:

```
$ npm install --save react-router-dom
```

(如果您没有安装最新的 npm (5.x)版本，请使用“保存”命令。) 我们从‘react-router-DOM’库中导入‘browser router’**组件**以及‘Link’和‘Route’。

我们可以将**浏览器路由器**视为呈现子路由的根组件。

```
import {
BrowserRouter,
Route,
Link
} from 'react-router-dom'

```

在继续介绍路由器 v4 的优势之前，让我们先了解一下**链路**和**路由**组件。

### **链接**

Link 用于在路由器应用程序中的**内部路由**中导航。它相当于锚标签:<a>T6/a>。

链接被传递一个字符串参数**到指定 URL 路径的**。

```
<ul>
<li><Link to="/">Home</Link></li>
<li><Link to="/about">About</Link></li>
<li><Link to="/topics">Topics</Link></li>
</ul>

```

### **路线**

我们现在来看一下 **<路线>、** ，它们可以被认为是单个的 **子** **组件** 负责根据用户的输入位置呈现UI。如果用户指定的位置与 **<路线>** 中定义的路径相匹配，那么 **<路线>** 可以通过两种方式定义 **视图**:

1.  创建一个**组件**中指定的 **<路线>**
2.  使用内嵌**渲染**功能

<**路由** >会在指定的 URL 与定义的路径不匹配的情况下返回 null。基本的 **<路径>** 有两个参数，一个用于**路径**，一个用于渲染 **UI。**

下面我来举例说明:

```
<BrowserRouter>
<div>
<Route exact path="/" render={ ( ) => (<h2> HomePage </h2>) } />
<Route path="/about" component={About}/>
<Route path="/topics" component={Topics}/>
</div>
</BrowserRouter> 
```

**3。IndexRoute 被替换为“精确的**”**:**

不需要使用 IndexRoute 来呈现主页，你会注意到前面代码片段中的**【精确】** 道具。这是 React 路由器 v4 的 **声明性** 性质的一个很好的例子。

v4 中的路线包含意味着可以同时渲染*多条路线*。我们使用**‘exact’**道具来解决多个匹配之间的竞争。

在前面的例子中没有使用‘exact’，URL **'/'** 将匹配路径为'/'、'/about '和'/topics '的路线。然而**，**我们希望 **'/'** 只匹配我们的渲染函数，因此使用‘exact’显式地实现了这一点。

**4。路由器只能有一个子元素:**

这就是为什么我们需要将我们的路线包在一个<分区>内。

如果我们没有这样做，您将会得到以下异常。

```
* Uncaught Error: A <Router> may have only one child element * 
```

**5。**开关:

虽然我们可以在单个< div >标签中封装几个路由。如果我们希望一次只呈现一个路由组件，我们使用一个<开关>标签来代替。它依次检查每条路线的匹配项，一旦找到第一个**匹配项**就停止。

```
<switch>
<route exact path=’/’   component={Home}/>
<route path=’/users/:id’ component={User }/>
<route path=’/users’   component={Roster}/>
<switch>

```

在我们的示例中，我们将路径为“users/:id”的路由放在了“users”的上方。这是因为“用户/:id”将与“用户”和“用户/:id”匹配。

现在您已经对 React 路由器有了基本的了解，下面是定义我们路由器应用组件的完整代码。

```
const App= () => (
<BrowserRouter>
<div>
<ul>
<li><Link to="/">Home</Link></li>
<li><Link to="/about">About</Link></li>
<li><Link to="/topics">Topics</Link></li>
</ul>
<Route exact path="/" render={ ( ) => (<h2> HomePage </h2>) } />
<Route path="/about" component={About}/>
<Route path="/topics" component={Topics}/>
</div>
</BrowserRouter>
)

```

这篇博客到此结束。希望这有助于您更好地了解 React 路由器的工作原理。要了解更多关于 React 路由器的信息，你也可以查看它的[文档](https://reacttraining.com/react-router/)。快乐学习！

*如果您在“**React Router”**上找到了这篇相关的博客，请查看 [React JS 培训](https://www.edureka.co/reactjs-redux-certification-training) 或 *[Web 开发认证](https://www.edureka.co/masters-program/web-developer-training)培训，该培训由* Edureka 提供，Edureka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。本 Edureka* *课程帮助学习者获得 React 基础和高级主题的专业知识，使您能够随时随地开发成熟的动态 web 应用程序。*

*有问题吗？请在评论区提到它，我们会给你回复。*