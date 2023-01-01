# JavaScript 中有哪些不同的数据类型

> 原文：<https://www.edureka.co/blog/data-types-in-javascript/>

JavaScript 是一种网络脚本语言。像任何其他编程语言一样，它有自己的数据类型。语言中的数据类型定义了变量可以保存的数据类型。在本文中，我们将详细讨论 JavaScript 中的各种数据类型:

*   [JavaScript 中原始和非原始数据类型的区别](#difference-1)
*   [JavaScript 中的原始数据类型](#primitive)
*   [非原始数据类型](#non-primitive)
*   [未定义和空值之间的差异](#difference-2)
*   [JavaScript 中两种数据类型的差异](#disrepancies)

JavaScript 有七种类型。类型是 JavaScript 可以拥有的值。下面是 JavaScript 可以拥有的数据类型列表:

1.  号
2.  字符串
3.  布尔型
4.  未定义
5.  Null
6.  物体
7.  符号

“符号”数据类型在 JavaScript 中是新的。它已经包含在 ES6 版本中。我们可以通过使用“type of”JavaScript 操作符找到值或数据的类型。JavaScript 中的上述数据类型分为两大类，原语和非原语。

*   JavaScript 中的原始数据类型包括数字、字符串、布尔、未定义、空和符号。

*   非原始数据类型只有一个成员，即对象。

## **JavaScript 中原始和非原始数据类型的区别**

JavaScript 原始数据类型是指单个值的数据类型。

**如`var a =5;`**

这里，变量‘a’是一个整数数据类型，有一个整数值。变量“a”指的是内存中的单个值。如果我们想改变 a 的值，我们就必须给 a 赋一个新值。 *原始数据类型是不可变的。*

当我们创建一个变量时，它会在内存中为自己保留一个空间。变量“a”在内存中有空间来保存它的值。当我们试图通过指定另一个值来改变' a '的值时，比如 var a = 6，它不会改变原始 a 的值，它只是用新值 6 创建了一个新变量' a'。

我们可以将“a”的值赋给另一个变量，如下所示:

**T2`var a1=a;`**

这里，变量‘a1’被赋予‘a’的值，而不是‘a’在内存中的地址。

因此‘a1’现在拥有与‘a’相同的值。

我们可以比较两个变量‘a’和‘a1 ’,因为这两个变量现在指的是同一个值。

使用比较运算符将返回布尔值“真”。

**`a===a1 // equals to ‘true’ as ‘===’ `** 检查这两个变量的值和类型是否都为真。

JavaScript 非原语类型是对象。一个对象保存一个或多个键值对的引用/地址。每当我们引用一个对象时，我们引用的是内存中包含键值对的地址。如果我们将一个对象“object1”分配给另一个对象“object2”，我们实际上是将“object1”的地址分配给“object2”，而不是“object1”在内存中包含的键-值对。让我们看看下面”。

**T2`var object1= {a:5, a1:6};`**

**T2`var object2 = object1;`**

上面的语句将对象 2 的地址分配给对象 1，而不是值{a:5，a1:6}。因此，通过这种分配,“对象 1”和“对象 2”指的是内存中的同一个地址。

当我们比较这两个对象时，我们发现它们都指向内存中的同一个地址。

object 1 = = = object 2//将返回 true，因为两者指向同一个地址。如果我们像下面这样比较两个独立的对象:

`**var object1= {a:5, a1:6};**`

`**var object2 = {a:5, a1:6};**`

这个语句 object1===object2 //将返回一个 false，因为这两个对象都指向内存中两个不同的地址。当我们比较两个对象时，我们比较的是它们的地址，而不是它们的值。

我们在上面的原始数据类型中已经看到，当我们将变量“a”赋给变量“a1”时，“a”的值被复制到“a1”中，而不是复制到非原始数据类型中的地址中。

因此，原始数据类型指的是内存地址中的“单个值”，而非原始数据类型指的是内存中包含单个或多个键值对的“地址”。

## **原始数据类型**

原始数据类型有数字、字符串、布尔、空、无穷大和符号。非原始数据类型是对象。JavaScript 数组和函数也是对象。更多信息，请查看[网络开发者在线课程](https://www.edureka.co/masters-program/full-stack-developer-training)。

**数字:**

数字数据类型可以是整数、浮点值、指数值、NaN 或 Infinity。

```
var a=250;  // integer value
var b=25.5;  // a number containing a decimal 
var c = 10e4 //  an exponential value which evaluates to 10*10000;
```

*有特殊的数值，如 NaN 和 Infinity。*

如果一个数除以 0，结果是无穷大。

```
5/0;    // results in infinity
The type of infinity is a number
typeof(infinity);   // returns number
```

*当我们试图对一个带有非数值的数字执行运算时，结果为“南”*

```
‘hi’ * 5; // returns NaN
typeof(NaN);  // returns a number
```

*我们也可以使用 number()函数创建一个数字文字:*

```
var c = Number(5); 
console.log(c);  // This will return 5
```

*我们可以使用‘new’操作符和 number()构造函数创建一个数字对象:*

```
var num1= new Number(5);
console.log(num1); // This will return 5
typeof(num1); // This will return ‘number’
```

**字符串:**

JavaScript 中的字符串数据类型可以是由单引号、双引号或反引号括起来的任何一组字符。

```
var str1 = “This is a string1”;  // This is a string primitive type or string literal
var str2= ‘This is a string2’;
var str3 = `This is a string3`;
```

*或者，我们可以使用 String()函数创建一个新的字符串。*

```
var str4 = String(‘hi’);  // This creates a string literal with value ‘hi’
```

*String()函数也用于将非字符串值转换为字符串。*

```
String(4); // This statement will create a string ‘4’
```

*与“数字”和“布尔”数据类型一样，可以使用“新建”运算符创建“字符串”对象:*

```
var str5= new String(“hello”);  // This is a string object
console.log(str4); // This will return the string ‘hello’
```

**布尔:**

布尔数据类型只有两个值，true 和 false。它主要用于检查逻辑条件。因此，布尔是逻辑数据类型，可用于比较两个变量或检查条件。在某些情况下，当我们检查一个条件或变量或值的存在时，true 和 false 意味着“是”表示“真”,而“否”表示“假”。

当我们使用 type of 运算符检查数据类型“真”或“假”时，它返回一个布尔值。

```
typeof(true) // returns boolean
typeof(false) // returns boolean
```

让我们来看一个比较语句的例子:

```
var a =5;
var b=6;
a==b // returns false
```

布尔值也用于检查表达式中的条件:

```
If(a<b){
alert(a is a smaller number than b);
}
```

如果上述条件“a

我们可以使用 Boolean()函数创建一个新的布尔变量。

```
var check = Boolean(expression);  // If the expression evaluates to true, the value of &lsquo;check&rsquo; will be true or else it will be false.
var check = Boolean(a<b); // the expression evaluates to true, thus the value of check will be true.
```

Boolean()函数将非布尔值转换为布尔值。

```
var mystring = ‘hi there’;
Boolean(mystring); // This will result in true because the ‘mystring’ value exists.
```

可以使用 new 运算符创建布尔对象。

```
var booleanobj = new Boolean(true);
```

这里的'`boolleanobj`'是一个布尔对象。

虽然我们可以创建一个基本数据类型的对象，“数字”，“布尔”和“数字”，这是明智的或良好的做法，使用这些类型的原始版本。

**未定义:**

未定义的数据类型是指未定义的变量。变量已声明，但不包含任何值。

```
var a;
console.log(a); // This will return undefined.
```

变量“a”已经声明，但尚未赋值。我们可以给 a 赋值:

```
a=5;
console.log(a); // This will return 5
```

**Null:**

JavaScript 中的 null 是一种仅由一个值表示的数据类型，即“null”本身。空值意味着没有值。

大概是这样的:

```
var a = null;
console.log(a);   // This returns null
```

如果我们使用 type of 运算符检查 a 的数据类型，我们会得到:

```
typeof(a);         // This returns object
```

这意味着空值的类型是对象，而不是空值。

**符号:**

“符号”数据类型是 es6 中新增的。是 es6 的新特性之一。符号数据类型定义了对象的私有属性。它指的是对象的键-值对的“键”。

```
var object1 = {
   name: ‘Shalini’,
   age: 25,
   city: ‘Mumbai’
}
var occupation=Symbol(‘engineer’);
```

功能符号()用于创建一个新符号。这里，我们为上述对象“object1”创建了一个值为“engineer”的符号“occupation”。

每个符号都是独一无二的。两个符号即使具有相同的键值也不相同。

```
var occupation=Symbol(‘engineer’); 
var occupation=Symbol();
```

occupation===occupation //返回 false。因此，上述两个“职业”符号是不同的。每一个都是该对象的独特属性。

我们不能使用“new”运算符创建符号对象，因为符号()不能用作构造函数。

Symbol()函数中的字符串描述是可选的。检查“职业”符号的类型:

```
typeof(occupation);  // returns symbol
```

## **非原始数据类型**

“object”是 JavaScript 中的非原始数据类型。JavaScript 中的数组和函数属于“对象”数据类型。

**对象:**

让我们创建一个对象文字。JavaScript 中的对象在其地址中包含键值对。当我们引用 obj1 时，我们实际上是指内存中包含值{a: 5，b: 6}的地址，而不是直接引用值{a: 5，b: 6}。

```
var obj1 = { a: 5, b: 6 };
```

我们可以改变或突变 obj1 的值。

```
obj1[a] =7;
console.log(obj1) // will return the value {a: 7, b: 6}
```

因此，该值已成功更改。

当我们使用 typeof 操作符检查 obj1 的值时，它返回一个对象。

```
typeof (obj1) // will return the data type ‘object’.
```

**数组:**

JavaScript 中的数组是一种对象数据类型。数组包含多个具有数字索引的值，其中索引从 0 开始。因此，它将其值保存在一个键-值对中。

```
var arr1= [1, 2, 3];
```

我们不能突变或改变上面的数组 arr1。

假设我们试图改变它的值。

```
arr1[0] =4;
console.log(arr1) // This will return the array [4, 2, 3]
typeof (arr1) // will return the data type ‘object’.
```

数组“arr1”是指内存中包含值[4，2，3]的地址。

**功能:**

JavaScript 没有函数数据类型，但是当我们使用 type of 操作符找到函数的数据类型时，我们发现它返回一个函数。这是因为函数在 JavaScript 中是一个对象。理想情况下，函数的数据类型应该返回一个对象，但它却返回一个函数。这是 JavaScript 中的一个错误。

让我们定义一个名为 a 的函数:

```
function a(){ }
```

现在让我们通过使用 type of 运算符:找到 a 的数据类型

```
typeof(a); // This will return data type function 
```

## **未定义和空值之间的差异**

这是 JavaScript 的两种不同的数据类型。当一个变量被声明但尚未赋值时，该变量的数据类型是未定义的。

Null 是 JavaScript 中的一种数据类型，但它主要用作赋给变量的值。将空值赋给变量意味着变量不包含任何值，类似于“未定义”的含义，也意味着空值。

null 和 undefined 之间的两个区别:

*   ' **null** 可以作为一个值赋给一个变量，而 undefined 也可以作为一个值赋给一个变量，但这并不推荐，也不是一个好的做法。

没有值的变量仅仅意味着它是未定义的。

```
var a;
console.log(a); // returns undefined
```

‘a’不包含任何值，数据类型未定义。

```
var a=undefined; // possible but not recommended
console.log(a) // returns undefined
```

让我们看看另一个变量:

```
var b=null;
```

*   不包含值的变量的数据类型为‘未定义’，，但包含‘空’值的变量的数据类型为‘对象’而不是‘空’。这是 JavaScript 中的一个错误，我们将在下一节讨论。

## **JavaScript 中两种数据类型的差异**

我们知道 null 是 JavaScript 中的一种数据类型。如果我们找出 null 的数据类型，它应该返回 null，但实际上它返回的是 object 数据类型。

令人困惑的是不是,‘null’的数据类型是一个对象而不是 null。技术上它应该是空的，但是这是 JavaScript 中的一个差异，我们必须接受和遵守。

另一个话题是 JavaScript 中函数的数据类型。当我们找到 JavaScript 函数的数据类型时，它会返回一个函数。我们知道 JavaScript 没有函数数据类型，那为什么会显示函数数据类型。

点是函数数据类型实际上是一个对象。JavaScript 中的所有函数都有对象的属性。函数的数据类型返回函数，而不是对象，这只是 JavaScript 中的一个差异。这也是我们必须接受和记住的。

至此，我们结束了 JavaScript 文章中的数据类型。综上所述，JavaScript 有不同的数据类型，原语和非原语。有七种原始数据类型，数字，字符串，布尔，空，未定义和符号，以及一种非原始数据类型'对象'。

尽管 NULL 和 undefined 数据类型包含相同的值，但它们之间还是有区别的。像其他编程语言一样，JavaScript 也有一些内置的语言错误或差异，这可以在空数据类型和 JavaScript 函数的数据类型中找到。如果你刚刚开始，那么看看这篇 JavaScript 教程，理解基本的 Java 概念。

**JavaScript 全教程| JavaScript 初学者教程| JavaScript 培训| Edureka**

[https://www.youtube.com/embed/o1IaduQICO0](https://www.youtube.com/embed/o1IaduQICO0)

*查看 Edureka 的 **[Web 开发认证培训](https://www.edureka.co/complete-web-developer)** 。* *Web 开发认证培训将帮助您学习如何使用 HTML5、CSS3、Twitter Bootstrap 3、jQuery 和 Google APIs 创建令人印象深刻的网站，并将其部署到亚马逊简单存储服务(S3)。*

*有问题吗？请在“JavaScript 项目”的评论部分提到它，我们会给你回复。*