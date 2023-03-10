# 如何在 PHP 中实现随机数生成器

> 原文：<https://www.edureka.co/blog/random-number-generator-in-php/>

在某些时候，当你用 PHP 编程时，你需要生成随机数。在这篇文章中，我们将看到如何生成一个随机数，也将看到如何用 PHP 中的随机数生成器指定一个下限和一个上限。本文涵盖了以下几点:

*   [兰德()方法](#rand())
*   [getrandmax()](#getrandmax())

继续这篇关于 PHP 中随机数生成器的文章。

## **rand()随机数生成方法**

当我们使用 rand()时，我们可以不提供任何参数，也可以提供两个参数。首先，我们将着眼于不提供参数。所以，如果我想回显 round()或者实际上创建一个名为 rand 的变量，我们可以在程序的后面使用它。PHP 中的随机数是自动生成的。因此，目前没有必要做任何事情，因为我们还没有提供我们的论据。这将生成一个介于最小和最大金额之间的随机数。最小金额为 0 或 1，最大金额为预先指定的金额。

```
<?php 
$rand=rand(); 
echo $rand; ?>

```

![random](img/904747b628cccfb83ea4ff253f13bfb7.png)

让我们再次重新加载浏览器

![reload](img/9d8ca57668a84a4b7db29df5ba1dc27f.png)

每次我们刷新浏览器的时候它都会产生一个随机数

还有一种方法可以找出上限值，让我们通过编码来理解它

```
<?php 
$rand=rand(); 
$max=getrandmax(); 
echo $rand. '/'.$max; ?>

```

![Image- Random number generator in php- Edureka](img/46f2f7a881217da1ca84a96a0f01a884.png) 继续这篇关于 PHP 中随机数生成器的文章。

因此， getrandmax() 将返回 rand()可能返回的最大随机值，本质上我们看到的是最大值中的随机数。所以 2147483647 是这种情况下可以生成的最大数，已经生成的数是 511779142。

刷新时，最大值将保持不变，但生成的随机数将会改变。

![Image- Random number generator in php- Edureka](img/8fd9a3f75a58201b31adc16255286235.png)

让我们看看你是否想创建一个用户必须随机掷骰子的骰子游戏。

```
<?php 
if(isset($_POST['roll'])) 
{ 
$rand=rand(1,6); 
echo 'Dice shows'." ".$rand; 
} 
?>
<form action="rand.php" method="POST">
<input type="submit" name="roll" value="roll dice">
</form>

```

![Image- Random number generator in php- Edureka](img/e42654d234901ea4543d06a5894e4a0b.png) 每次点击掷骰子，都会生成一个随机数。 到此，我们就结束这篇关于 PHP 中随机数生成器的文章。我希望你已经学会了如何在 PHP 中生成随机数，以及生成随机数的用例。

*查看 Edureka 提供的* *[**PHP 认证培训**](https://www.edureka.co/php-mysql-self-paced) ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。*

*有问题吗？请在“**PHP 中的随机数生成器**”的评论部分提到它，我会回复你。*