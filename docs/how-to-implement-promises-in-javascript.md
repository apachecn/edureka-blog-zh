# 如何用 JavaScript 实现承诺？

> 原文：<https://www.edureka.co/blog/how-to-implement-promises-in-javascript/>

[JavaScript](https://www.edureka.co/blog/what-is-javascript/) 中的承诺基本都是用来处理操作异步操作的。承诺是一个可以在未来产生单一值的对象:或者是一个已解决的值，或者是一个错误。

本文将涉及以下几点:

*   [重要性](#Importance)
*   [状态类型](#Typesofstates)
*   [承诺的产生](#CreationofPromises)
*   [创建承诺的示例 1](#Example1forCreationofPromises)
*   [创建承诺的示例 2](#Example2CreationofPromises)
*   [创建承诺的示例 3](#Example3CreationofPromises)
*   [消费者在承诺中接着()](#ConsumersinPromisesinthen())
*   [承诺何时兑现的示例](#AnexampleofwhenPromiseisresolved)
*   [拒绝承诺的例子](#AnexampleofwhenPromiseisrejected)
*   [承诺的消费者 catch()](#ConsumersinPromisescatch())
*   [消费者承诺示例 1](#Example1ConsumersinPromises)
*   [消费者承诺示例 2](#Example2ConsumersinPromises)
*   [消费者承诺例 3](#Example3ConsumersinPromises)

让我们从这篇关于 JavaScript 承诺的文章开始吧

## **重要性:**

当有多个异步操作需要处理时，这些承诺就派上了用场。在 JavaScript 中引入承诺之前，已经有了用于处理异步操作的事件和回调函数。由于事件在异步操作中用处不大，所以它们不是首选。谈到回调，多次使用它们会造成混乱，任何人都很难理解代码。因此，承诺是每个程序员以最简单的方式处理异步操作的首选。它们具有高级功能，这使得它们处理操作比回调和事件更容易。

*   Promises 使代码可读，这意味着它可以在开发的后期由编码人员编辑。
*   与回调和事件相比，在整个异步操作中有更好的处理。
*   高级错误处理也被认为是一个重要的特性。
*   这里有一个更好的异步控制定义流。

继续这篇关于 JavaScript 承诺的文章

## **状态类型:**

**兑现:**与那些成功的承诺有关。 **被拒绝:**与那些被拒绝的承诺有关。 **待定:**与那些待定的承诺相关，即没有被拒绝也没有被接受。 **已解决:**与正在履行或拒绝的承诺有关。

继续这篇关于 JavaScript 承诺的文章

## **承诺的产生**

使用 promise 构造函数创建 promise。

**语法:**

```
var promise = new Promise(function(resolve, reject){
//do something here 
});

```

**参数:** Promise 构造函数取一个参数，回调函数。回调函数中有两个参数，resolve 或 reject。操作是在回调函数中执行的，如果一切顺利，那么调用解决，否则调用被拒绝。

继续这篇关于 JavaScript 承诺的文章

**例 1:**

```
var promise = new Promise(function(resolve, reject) { 
/*declaring and defining two variables of const data type with same content.*/
const a = "Hello there! My name is Yash and I am interested in computer Science."; 
const b = " Hello there! My name is Yash and I am interested in computer Science.";
//checking if both the content stored in variables are same or not
if(a === b) { 
//calling resolve 
resolve(); 
} else { 
//calling reject
reject(); } 
}); 
promise. 
then(function () { 
console.log('Promise Resolved!!'); 
}). 
catch(function () { 
console.log('Promise Rejected!!'); 
});

```

**输出:T2**

继续这篇关于 JavaScript 承诺的文章

**例 2:**

```
var promise = new Promise(function(resolve, reject) {
//initializing two variables with integer values
const x = 11+2;
const y = 26/2;
//checking if both variables are equal or not
if(x === y) {
//calling resolve
resolve();
} else {
//calling reject
reject(); }
});
promise.
then(function () {
console.log('Promise is Resolved!!');
}).
catch(function () {
console.log('Promise is Rejected!!');
});

```

**输出:![Output- Promises in JavaScript- Edureka](img/36caa939458f5da0c406cb8db6fafd1a.png)**

继续这篇关于 JavaScript 承诺的文章

**例 3:**

```
var promise = new Promise(function(resolve, reject) { 
const i = "Hello";
const a = "World"; 
//performing addition of two variables to store value in another variable
const j= i+a;
if((i+a) === j) { 
//calling resolve
resolve(); 
} else { 
//calling reject
reject(); } 
}); 
promise. 
then(function () { 
console.log('Promise is Resolved!!'); 
}). 
catch(function () { 
console.log('Promise is Rejected!!'); 
});

```

**输出:![Output- Promises in JavaScript- Edureka](img/c730dd02fcdf40a10a2b839d52792e9d.png)**

继续这篇关于 JavaScript 承诺的文章

## **消费者在承诺**

有两种注册功能:

**然后()**

当承诺被解决或拒绝时，就会调用()。

**参数:**

*   如果解决了承诺，则执行第一个函数并接收结果。
*   如果承诺被拒绝，则执行第二个功能，并在屏幕上显示错误。

**语法:**

```
.then(function(result){
//handling  success
}, function(error){
//handling the error
})

```

继续这篇关于 JavaScript 承诺的文章

**例子**

## **承诺完成时**

```
//resolving of promise
var promise = new Promise(function(resolve, reject) { 
resolve('Success message is written here!'); 
}) 
promise 
.then(function(successMessageishere) { 
//success handling function is invoked 
console.log(successMessageishere); 
}, function(errorMessageishere) { 
console.log(errorMessageishere); 
})

```

**输出:T2**

继续这篇关于 JavaScript 承诺的文章

## **当承诺被拒绝时**

```
//Rejection of promise
var promise = new Promise(function(resolve, reject) { 
reject('Rejection message is written here!') 
}) 
promise 
.then(function(successMessage) { 
console.log(successMessage); 
}, function(errorMessage) { 
//error handler function is invoked 
console.log(errorMessage); 
})

```

**输出:T2**

继续这篇关于 JavaScript 承诺的文章

**赶** ( **)**

每当在执行期间出现某种错误或承诺被拒绝时，就会调用 catch()。参数:

*   在 catch()方法中，只有一个函数作为参数传递。
*   该函数用于处理错误或承诺拒绝。

**语法:**

```
.catch(function(error){
//handling error
})

```

继续这篇关于 JavaScript 承诺的文章

**例 1:**

```
var promise = new Promise(function(resolve, reject) { 
reject('Promise is Rejected') 
}) 
promise 
.then(function(success) { 
console.log(success); 
}) 
.catch(function(error) { 
//error handler function is invoked 
console.log(error); 
});

```

**输出:![Output- Promises in JavaScript- Edureka](img/b3351e924fdefc70b04d81b45b71c6e0.png)**

继续这篇关于 JavaScript 承诺的文章

**例 2:**

```
var promise = new Promise(function(resolve, reject) { 
//error message
throw new Error('There is some error!') 
}) 
promise 
.then(function(success) { 
console.log(success); 
}) 
.catch(function(error) { 
//error handler function is invoked 
console.log(error); 
});

```

**输出:![Output- Promises in JavaScript- Edureka](img/3ee8716fd31698f6ccc547f55453b3c0.png)**

继续这篇关于 JavaScript 承诺的文章

**例 3:**

```
var promise = new Promise(function(resolve, reject) { 
//error message can be edited here
throw new Error('some error occured !') 
}) 
promise 
.then(function(Thissuccess) { 
console.log(Thissuccess); 
}) 
.catch(function(Thiserror) { 
//error handler function  invoked 
console.log(Thiserror); 
});

```

**输出:**

**应用:** 1 .处理异步事件。 2。处理异步 http 请求。

这样，我们就结束了这篇关于“JavaScript 中的承诺”的文章。如果你想了解更多，可以去看看 Edureka 值得信赖的在线学习公司提供的  [Java 培训](https://www.edureka.co/java-j2ee-soa-training) 。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。