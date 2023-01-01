# 什么是 JavaScript 方法，如何使用？

> 原文：<https://www.edureka.co/blog/javascript-methods/>

JavaScript 对象是键或值对的集合。这些值由属性和方法组成。此外，它还包含其他 JavaScript 数据类型，如[字符串](https://www.edureka.co/blog/javascript-string-functions/)、数字和布尔值。在本文中，我们将按以下顺序讨论不同的 JavaScript 方法:

*   [什么是 JavaScript 方法？](#methods)
*   [如何访问对象方法？](#object)
*   [不同类型的 JavaScript 方法](#types)

## **什么是 JavaScript 方法？**

JavaScript 方法是可以在对象上执行的操作。JavaScript 方法是包含一个[函数](https://www.edureka.co/blog/javascript-functions/)定义的属性。例如:

| **属性** | **值** |
| **名字** | 雏菊 |
| **姓氏** | 格林（姓氏）；绿色的 |
| **年龄** | Twenty-five |
| **FullName** | function(){返回此。名字+ " " +这个。姓氏；} |

这些方法不过是存储为[对象](https://www.edureka.co/blog/javascript-object/)属性的函数。现在让我们看看如何在 JavaScript 中访问这些对象方法。

## **如何访问对象方法？**

您可以使用以下语法访问对象方法:

```
objectName.methodName()
```

这里，您必须将 **FullName()** 描述为 Person 对象的方法，并将 FullName 描述为属性。当使用()调用 fullName 属性时，它作为一个函数工作。下面是一个如何访问 person 对象的 **FullName()** 方法的例子:

```
Name = person.FullName();
```

这就是你访问对象方法的方式。现在有不同类型的方法。因此，我们将详细讨论这些方法。

## **不同类型的 JavaScript 方法**

全局对象构造函数中可用的不同类型的 [JavaScript](https://www.edureka.co/blog/javascript-tutorial/) 方法有:

*   **Object.create()**
*   **Object.keys()**
*   **Object.freeze()**
*   **Object.values()**

### **Object.create**

可以用 **Object.create()** 函数创建对象。这具有额外的灵活性，允许您选择新对象的原型。

```
let createObj = Object.create(obj);
console.log(createObj); //{}
createObj.name = "Danny";
console.log(createObj.speak());
```

在上面的例子中，obj 是创建 createdObj 的原型。此外，由于继承，它可以使用原型的属性。因此，您可以使用 **speak()** 方法，而无需在 createdObj 中声明该方法。

### **Object.keys**

object.keys 函数用于仅选取对象的键或属性标签，并返回一个[数组](https://www.edureka.co/blog/javascript-array/)。

```
let keys = Object.keys(person);
console.log(keys);
// [ 'name', 'age' ]
```

### **Object.freeze**

冻结功能用于冻结对象的键或值的任何变化。除非在严格模式下，否则它不会抛出任何错误。但是对你的对象不会有价值变化的影响。

```
let frozenObject = Object.freeze(person);
frozenObject.name = "Rachel";
console.log(frozenObject);
```

### **Object.values**

此函数仅用于选择对象的值，并以下列方式返回一个数组:

```
let values = Object.values(person);
console.log(values); 
```

这些是一些不同类型的方法。说到这里，我们的文章就到此为止了。我希望您了解不同类型的 JavaScript 方法以及它们是如何使用的。

*既然你已经了解了 JavaScript 中的方法，那就来看看 Edureka 的 **[Web 开发认证培训](https://www.edureka.co/complete-web-developer)** 。* *Web 开发认证培训将帮助您学习如何使用 HTML5、CSS3、Twitter Bootstrap 3、jQuery 和 Google APIs 创建令人印象深刻的网站，并将其部署到亚马逊简单存储服务(S3)。*

*有问题吗？请在“JavaScript 方法”的评论部分提到它，我们会回复您。*