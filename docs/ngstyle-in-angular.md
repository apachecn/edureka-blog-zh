# Angular 8 中关于 NgStyle 你需要知道的一切

> 原文：<https://www.edureka.co/blog/ngstyle-in-angular>

如果您已经在编码行业工作了一段时间，您可能已经知道在 web 应用程序中开发动态变化是一项艰巨的任务。根据你选择使用的编程平台，你的复杂程度往往会有所不同，但幸运的是，这个壮举可以在 Angular 8 和 Angular 的一些早期版本中轻松实现。在本文中，我们将讨论 agular 8 中的 ngstyle。

*   [Angular 8 中的模板属性语法](#template)
*   [ng class ng style in Angular 8](#style)
*   [nng 卡入角度 8](#click)

## **Angular 8 中的模板属性语法**

在我们深入探索 Angular 8 附带的所有功能和模块之前，让我们先看看 Angular 8 中的属性语法，以及我们如何在纯 Java 中更改

color 属性的颜色。

![ngstyle-in-angular](img/d39fbadd9d37fd5d4d69ab5bf0a446ef.png)

```
let myDiv = document.getElementById('my-div');
myDiv.style.color = 'orange'; // updating the div via its properties

```

让我们在 Angular 8 中通过使用内置库和其他模块来完成同样的任务。

```
<div [style.color]="'orange'">style using property syntax, this text is orange</div>

```

使用语法{property}，高效地实现任何代码，并几乎在瞬间对其进行更改。

在上面的例子中，我们所做的是直接访问 div 元素样式属性。与 DOM 对象和属性的属性相比，这是不同的。

使用内置的 Angular 8 特性，我们可以将 CSS 元素添加到我们选择的任何类中。请看下面的例子来更好地理解这一点。

```
<div [className]="'blue'">CSS class using property syntax, this text is blue</div>

```

## **角度 8 中的 NgClass 和 ng style**

它内置了 Angular 8 中的 ngSyntax 和 ngClass，可用于满足各种用途。在某种程度上，内置模块为实现比其他模块更复杂的字符串更改提供了方便。让我们看看 Angular 8 中 ngStyle 的语法。

```
<div [ngStyle]="{'color': 'blue', 'font-size': '24px', 'font-weight': 'bold'}">
style using ngStyle
</div>

```

在上面的例子中，我们使用了 Angular 中的 ngStyle 来改变类中多个元素的动态，同时将几个元素组合在一起，以便于用户根据自己的需要定制类。

上例的延续。

```

<div [ngStyle]="{'color': color, 'font-size': size, 'font-weight': 'bold'}">
style using ngStyle
</div>

<input [(ngModel)]="color" />
<button (click)="size = size + 1">+</button>
<button (click)="size = size - 1">-</button>

```

现在你已经了解了 ngStyle，让我们来看看 ngStyle 的一些元素。

```
<div [ngClass]="['bold-text', 'green']">array of classes</div>
<div [ngClass]="'italic-text blue'">string of classes</div>
<div [ngClass]="{'small-text': true, 'red': true}">object of classes</div>

```

angular 中的 ngClass 还允许我们以多种方式对代码进行修改，这样动态修改可以在瞬间实现，就像 ngStyle 一样。

看一下下面的例子，看看这两者是如何一起工作的。

```

import { Component } from '@angular/core';

@Component({
selector: 'my-app',
templateUrl: './app.component.html',
styleUrls: ['./app.component.css']
})
export class AppComponent {
color = 'pink';
size = 16;
displayText = 'show-class';
visible = true;
constructor() { }

toggle() {
this.visible = !this.visible;
this.displayText = this.visible ? 'show-class' : 'hide-class';
}
}

```

## **ng 点击角度 8**

现在您已经了解了 ngClass 和 ngStyle 的基本特性，以及在 Angular 8 平台中使用其中一个或两个可以实现什么，让我们来看看 ngClick 的用法。

**什么是 ngClick？**

如果在一个特定的事件中，你需要将一个程序的多个元素绑定在一起，这样一个单一的任务就可以完成，那么你就需要使用 ngClick。

```
<button ng-click="vm.toggleImage()">
<button ng-click="vm.toggleImage($event)">

```

以上是 ngClick 在 AngularJS 中使用的一个例子。当涉及 Angular8 时，不存在相同的模块，因此需要利用以下内容。

```
<button (click)="toggleImage()">
<button (click)="toggleImage($event)">

```

上述语法用于促进 Angular8 中的事件绑定，其中我们首先用括号定义目标事件的名称，然后通过包含引号和等号运算符来包含一个模板语句。一旦这些步骤完成，Angular8 就会为这个事件设置一个事件处理程序，一旦触发，这个事件就会被执行。

Angular8 不仅是最受欢迎的编程语言之一，由于其广泛的特性，它也是最具活力的语言之一。至此，我们结束了这篇关于 angular 中 NgStyle 的文章。我希望你了解这些是如何工作的。

*查看 Edureka 的 [**棱角训练**](https://www.edureka.co/angular-training) 。Angular 是一个 JavaScript 框架，用于创建可伸缩的、企业级的、高性能的客户端 web 应用程序。随着 Angular 框架的广泛采用，应用程序的性能管理是由社区驱动的，间接推动了更好的工作机会。Angular 认证培训旨在涵盖所有这些围绕企业应用程序开发的新概念。*