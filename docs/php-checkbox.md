# 如何在 PHP 中创建复选框？

> 原文：<https://www.edureka.co/blog/php-checkbox/>

网络用户将复选框与“多项选择”联系在一起。它帮助你在两个互斥的选项中选择一个。这就像用“是”或“否”来回答一个问题。在本文中，我们将看到如何按以下顺序在 [PHP](https://www.edureka.co/blog/php-tutorial-for-beginners/) 中创建单个或多个复选框:

*   什么是复选框？
*   [PHP 中的单个复选框](#single)
*   [PHP 中的多个复选框](#multiple)

## 什么是复选框？

复选框帮助用户在两个互斥选项中选择一个。根据您选择的选项数量，有两种类型的复选框。

*   **复选框组**
*   **复选框**

点击复选框可以将它从开变为关，反之亦然。这些是多选选项的首选。在必须做出单一选择的用例中，单选按钮或选择选项会更好。如果在这种情况下出现“检查所有适用项”问题，可以使用复选框组。

现在你知道了什么是复选框，让我们继续，看看如何在 PHP 中创建一个复选框。

## **PHP 中的单个复选框**

每个响应应单独切换到开和关。单个复选框示例如下所示:

```
<?php
//Set “terms accepted” to false by default.
$termsAccepted=false;
//If the POST variable “terms_of_services” exists.
If ($_POST[‘terms_of_services’]) {
//Checkbox has been ticked.
$termsAccepted=true;
}
//Print it out for example purposes.
If($termsAccepted){
Echo ‘Terms of Service checkbox ticked!’;
}
?>
<form action=””method=”post”>
<lable>
I accept the terms of service.
<input type=”checkbox” name=”terms_of_services” value=”Y”>
<lable>
<input type=”submit” value=”Register”>
</form>
```

接下来，我们将看到如何在 PHP 中创建多个复选框。

## **PHP 中的多个复选框**

多个复选框比单个复选框稍微复杂一些。如果用户想要选择一个或多个选项，则使用。在这个例子中，我们允许用户选择他们最喜欢的蔬菜:

```
<?php
//Valid options . A whitelist of allowed options.
$vegetableOptions= array(
‘tomato’,
‘carrot’,
‘onion’,
‘Chilly’
);
//Empty array by default.
$vegetables = array();
//If the POST variable “vegetables” is a valid array.
If(!empty($_POST[‘vegetables’]) && is_array($_POST[‘vegetables’])){
//Loop through the array of checkbox values.
Foreach($_POST[‘vegetables’] as $vegetables){
//Make sure that this option is a valid one.
If(in_array($vegetable, $vegetableOptions)){
//Add the selected options to our $vegetables array.
$vegetables[]=$vegetable;
}
}
}
Var_dump($vegetables);
?>
<form action=””method=”post”>
<label>
Tomatoes
<input type=”checkbox” name=”vegetables[]” value=” Carrot”>
<label>
<label>
Onions
<input type=”checkbox” name=”vegetables[]” value=”Onions>
</label>
<label>
Chillies
<input type=”checkbox” name=”vegetables[]” value=”Chillies”>
</label>
<input type=”submit” value=”Register”>
</form>
```

说到这里，我们的文章就到此为止了。我希望你明白什么是复选框以及如何在 PHP 中创建它们。

*如果你发现这个博客相关，请查看 Edureka 的* *[**PHP 认证培训**](https://www.edureka.co/php-mysql-self-paced) ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。*

*有问题吗？请在 **PHP** 中的**复选框的评论区提出来，我会给你回复。***