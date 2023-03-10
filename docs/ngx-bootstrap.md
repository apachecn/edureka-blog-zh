# ngx boostrap 是什么，怎么用？

> 原文：<https://www.edureka.co/blog/ngx-bootstrap/>

Anngx bootstrap是一个开源工具，是一个正在开发的独立项目。你可以排除你原来的 JavaScript 组件，只使用 Bootstrap 提供的标记和 [CSS 框架](https://www.edureka.co/blog/what-is-css/)。

在这篇博客中，你将了解到:

*   [安装 ngx 引导程序](#installation)
*   [手动设置引导程序](#setup)
*   [建造图书馆](#buildinglibrary)

我们开始吧。

## **安装 ngx 引导程序**

从基础开始，让我们学习如何安装 ngx bootstrap！

### **方法 1**

使用 npm 安装 ngx 引导

```
Npm install ngx-bootstrap --save
```

添加 NgModule 导入所需的必要包:

```
import { TooltipModule } from 'ngx-bootstrap/tooltip';

@NgModule({
...
imports: [TooltipModule.forRoot(),...]
...
})

```

将所需组件添加到页面:

```
<button type="button" class="btn btn-primary" tooltip="Vivamus sagittis lacus vel augue laoreet rutrum faucibus.">
  Simple demo
</button>

```

添加所需的引导样式:

*   **引导程序 3:**

```
<!--- index.html &rarr;
<link href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" rel="stylesheet">

```

*   **自举 4:**

```

<!--- index.html &rarr;
<link href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" rel="stylesheet">

```

### **方法二**

要更新您的角度项目，使用[角度命令](https://www.edureka.co/blog/angular-cli/) ng 添加命令

```
ng add ngx-bootstrap
```

或者你也可以使用 ng add 命令来添加需要的组件(或者例子-工具提示)

```
ng add ngx-bootstrap --component tooltip
```

添加您的页面所需的必要组件:

```
<button type="button" class="btn btn-primary" tooltip="Vivamus sagittis lacus vel augue laoreet rutrum faucibus.">
  Simple demo
</button>

```

## **手动设置 ngx 引导**

您的项目可能使用了一组不同的库，这可能会干扰引导框架，或者您可能已经定制了您的引导框架。当库不支持您的 bootstrap 版本时，用户界面可能会中断。为了避免这种情况，您可以使用 AddComponent 代码:手动设置引导版本

```
import { setTheme } from 'ngx-bootstrap/utils';
@Component({...})
export class AppComponent {
  constructor() {
    setTheme('bs3'); // or 'bs4'
    ...
  }
}

```

接下来，让我们学习如何构建用于开发的库。

## **建造图书馆**

当你第一次建造图书馆时，你可以，

*   克隆存储库
*   npm 安装
*   npm 运行构建

要更新您的 fork 并为本地使用做好准备，您可以使用以下代码:

*   git 拉动上游开发
*   rm -rf 节点模块
*   npm 安装
*   npm 运行构建

运行演示:

*   npm 运行 demo.serve *//为本地 demo 服务。这只是测试，没有观察员。*

对于本地开发运行，使用以下代码:

*   NPM run build . watch*//在第一终端*
*   ng 发球 *//第二次*

使用 Angular Universal 运行演示:

*   npm 运行 demo.serve-universal

希望这篇关于 ngx 自举 的博客有用。如有任何疑问，请在下面留下您的评论！

至此，本文结束。我希望你明白什么是引导分页，什么是不同类型的分页。

*查看 Edureka 的 **[Web 开发认证培训](https://www.edureka.co/complete-web-developer)** 。* *Web 开发认证培训将帮助您学习如何使用 HTML5、CSS3、Twitter Bootstrap 3、jQuery 和 Google APIs 创建令人印象深刻的网站，并将其部署到亚马逊简单存储服务(S3)。*

*有问题吗？请在这个博客的评论部分提到它，我们会给你回复。*