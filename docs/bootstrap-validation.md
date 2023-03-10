# Bootstrap 验证:如何使用 Bootsrap 验证表单？

> 原文：<https://www.edureka.co/blog/bootstrap-validation/>

Bootstrap Validation 用于确保表单上的重要块不为空。它确保用户以正确的格式准确地输入数据。以前， [JavaScript](https://www.edureka.co/blog/javascript-tutorial/) 插件被用来验证输入，但是现在大多数浏览器提供了一个内置的解决方案来处理表单的验证。

在这篇博客中，你将了解到:

*   [表单的布局](#layout)
*   [必填属性](#required)
*   [Maxlength 和 Minlength](#length)
*   [图案](#pattern)
*   [在 Bootstrap Studio 中进行表单验证](#form)

## **表单的布局**

一个[表单](https://www.edureka.co/blog/javascript-form-submission/)设计通常由几个输入框和按钮组成。这里，我们将使用三个输入字段——姓名、密码和电子邮件输入字段，以及一个“提交”按钮。

### **HTML 代码**

```
<div class = "registration-form">
<form>
<h3 class = "text-center"> Create your account </h3>
<div class = "form-group">
<input class = "form-control item" type = "text" name = "username" maxlength = "15" minlength = "4" pattern = "^[a-zA-Z0-9_.-]*$" id = "username" placeholder = "Username" required>
</div>
<div class = "form-group">
<input class = "form-control item" type = "password" name = "password" minlength = "6" id = "password" placeholder = "Password" required>
</div>
<div class = "form-group">
<input class = "form-control item" type = "email" name = "Enter E-mail ID" id = "email" placeholder = "Enter E-mail ID" required>
</div>
<div class = "form-group">
<button class = "btn btn-primary btn-block create-account" type = "submit">Create Account</button>
</div>
</form>
</div>
```

### **CSS 代码**

```
html {
background-color:#214c84;
background-blend-mode:overlay;
display:flex;
align-items:center;
justify-content:center;
background-image:url(../../assets/img/image4.jpg);
background-repeat:no-repeat;
background-size:cover;
height:100%;
}

body {
background-color:transparent;
}

.registration-form {
padding:50px 0;
}

.registration-form form {
max-width:800px;
padding:50px 70px;
border-radius:10px;
box-shadow:4px 4px 15px rgba(0, 0, 0, 0.2);
background-color:#fff;
}

.registration-form form h3 {
font-weight:bold;
margin-bottom:30px;
}

.registration-form .item {
border-radius:10px;
margin-bottom:25px;
padding:10px 20px;
}

.registration-form .create-account {
border-radius:30px;
padding:10px 20px;
font-size:18px;
font-weight:bold;
background-color:#3f93ff;
border:none;
color:white;
margin-top:20px;
}

@media (max-width: 576px) {
.registration-form form {
padding:50px 20px;
}
}
```

让我们看看上面代码中使用的引导验证类型。

在 HTML5 中，内联引导验证最简单的方法是使用输入属性。有大量的属性可用，但是这里我们将研究上面的 [HTML](https://www.edureka.co/blog/what-is-html/) 代码中使用的属性。

## **必需属性**

required 属性用于指示该字段不能为空。用户需要在提交表单之前填写所有必填字段。

```
<input class = "form-control item" type ="email" name = "Enter E-mail ID" id ="Enter E-mail ID" placeholder = " Enter your Email ID" required>
```

**输出:**

![output- bootstrap validation - edureka](img/7a9a0c68621c03b4522fb9bf12592f93.png)

## **最大长度和最小长度**

max length 和 minlength 属性指定输入字段可以容纳的字符或符号的最大或最小数量。当要求用户输入密码时，该属性很有用。

```
<input class = "form-control item" type = "password" name = "password" minlength = "6" id = "password" placeholder = "Password" required>
```

**输出:**

![output - bootstrap validation - edureka](img/41bed92cd7df36da13cb7bede6550fde.png)

## **图案**

此属性指定在输入数据时必须匹配特定的。可以在输入文本、搜索、电子邮件或密码时指定。

```
<input class = "form-control item" type = "text" name = "username" maxlength = "15" minlength = "4" pattern = "^[a-zA-Z0-9_.-]*$" id = "username" placeholder = "Username" required>
```

**输出:**

![](img/a2b5e011530b46a9c394e8827738ab99.png)

## **在 Bootstrap studio 中形成 Bootstrap 验证**

有了各种可用的方法，Bootstrap 提供了最快最简单的方法来验证表单，甚至不需要思考或编写任何代码。内置功能可帮助您即时设置表单，并根据您的要求进行设计。

就这样，我们来到了这篇文章的结尾。我希望你明白什么是引导验证。

*查看 Edureka 的 **[Web 开发认证培训](https://www.edureka.co/complete-web-developer)** 。* *Web 开发认证培训将帮助您学习如何使用 HTML5、CSS3、Twitter Bootstrap 3、jQuery 和 Google APIs 创建令人印象深刻的网站，并将其部署到亚马逊简单存储服务(S3)。*

*有问题吗？请在这个“自举验证”博客的评论部分提到它，我们会给你回复。*