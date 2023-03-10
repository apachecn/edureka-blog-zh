# 如何最好地利用 PHP 中的 Trim 函数？

> 原文：<https://www.edureka.co/blog/trim-functions-in-php/>

[PHP](https://www.edureka.co/blog/php-tutorial-for-beginners/) 函数是可以多次循环使用的一部分代码。它可以把努力作为参数表和再现值。PHP 中有成千上万的内置函数。在这篇文章中，我们将探讨 PHP 中的 Trim 函数。本文将涉及以下内容，

*   [PHP 函数的特点](#FeaturesOfPHPFunctions)
*   [PHP 中的 Trim 函数](#TrimFunctionInPHP)
*   [PHP Ltrim 函数](#PHPLtrimFunction)
*   [PHP Rtrim 函数](#PHPRtrimFunction)

那么让我们开始吧，

## **PHP 函数的特点**

#### **代码可重用性**

与其他编程语言一样，PHP 函数只定义一次，可以多次调用。

#### **少码**

它保护了大量代码，因为你不需要多次编写逻辑。通过使用函数，您可以只编写一次逻辑，并根据需要反复使用。

#### **通俗易懂**

PHP 函数将编程逻辑离散化。所以理解提交的漂移是比较平静的，因为每一个逻辑都是以函数的形式划分的。

我们可以在函数中规定一个默认的参数值。在调用 PHP 函数时，如果你没有指定任何参数，它将采用默认参数。

继续这篇关于 PHP 中 Trim 函数的文章

## **PHP 中的 Trim 函数**

删除字符串两边的字符(“Head”和“d！”中的“He！”【在“夏尔”)

```
<?php $str = "Hello sherd!";echo $str."<br>";echo trim($str,"Hed!");?>
```

函数的作用是:删除字符串两边的空格和其他预定义的字符 。

#### **相关功能 h3**

**ltrim()**

消除字符串左侧的空白或其他预定义字符。rtrim()–消除字符串右侧的空白或其他预定义字符。

**语法**

修剪(弦乐，查理斯)

修剪是删除第一个和最后一个字符的最快方法

**样本代码**

```
<?php $s = '/catalog/lyustry/svet/dom-i-svet/';
$times = 100000;
print cycle("str_preg('$s');", $times);
print cycle("str_preg2('$s');", $times);
print cycle("str_sub_replace('$s');", $times);
print cycle("str_trim('$s');", $times);
print cycle("str_clear('$s');", $times);
//print_r(str_preg2($s));
function cycle($function, $times){
$count = 0; if($times < 1){
return false; } $start = microtime(true); while($times > $count){
eval($function); $count++; } $end = microtime(true) - $start; return "n $function exec time: $end"; }
function str_clear($s){ $s = explode('/', $s); $s = array_filter($s, function ($s){if(!empty($s)) return true;}); return $s; } function str_preg2($s){
$s = preg_replace('/((?<!.)/(?=.))?((?<=.)/(?!.))?/i', '', $s); $s = explode('/', $s); return $s; } function str_preg($s){
$s = preg_replace('/^(/?)(.*?)(/?)$/i', '$2', $s); $s = explode('/', $s); return $s; } function str_sub_replace($s){
$s = str_replace('/' , '' , mb_substr( $s , 0, 1)) . mb_substr( $s , 1, -1) . str_replace('/', '', mb_substr( $s , -1));
$s = explode('/', $s); return $s; } function str_trim($s){ $s = trim($s, '/'); $s = explode('/', $s); return $s; }
```

**参数**

该函数接受一个强制参数和一个可选的 参数，如以上语法所示，如下所述。

**$字符串**

此参数表示要删除左边和右边的空白和预定义字符的字符串。

【T0 美元江湖术士】t1

这是一个可选参数，指定要从字符串中删除的字符。如果没有提到这一点，那么以下所有字符都将被删除。

“”–空“t”——制表符“n”——新行“x0B”——竖排制表符“r”——回车“——普通空格

**返回值**

它通过删除空格以及字符串左右两边的预定义字符来返回修改后的字符串。

继续这篇关于 PHP 中 Trim 函数的文章

## **PHP Ltrim 函数**

ltrim()函数是 PHP 中的一个内置函数，它可以删除字符串左边的空格或其他字符。

```
ltrim($string,$charlist)
```

**参数**

函数 ltrim()接受两个参数，如上面的语法所示。在这两个参数中，一个是强制的，而另一个是可选的。下面详细讨论它们:

**$string**

该强制参数指定要检查的字符串。

【T0 美元江湖术士】t1

该可选参数指定从字符串中删除哪些字符。如果不提供此参数，将删除以下字符。

“”–空“t”–制表符“n”–新行“x0B”–垂直制表符

" r "-回车" "-普通空格

**返回值**

返回修改后的字符串。

**样本程序**

这个程序显示了 ltrim()函数的使用，没有任何指定的 字符列表被删除。

```
<?php
$string = "time for edureka";
echo "Subsidize ".ltrim($string);
?>
```

**输出**

补贴 edureka 的时间

**样本程序**

他的程序展示了 ltrim()函数的使用，并指定了要删除的字符列表。

```
<?php
$string = "!!! (( !!)) time for edureka"; echo ltrim($string, "! ()");
?>
```

**输出**

爱德华卡的时间

继续这篇关于 PHP 中 Trim 函数的文章

## **PHP Rtrim 函数**

rtrim()函数是 PHP 中的一个内置函数，它从字符串的右边移除空格或其他字符(如果指定的话)。

**语法**

```
rtrim( $string, $charlist )
```

**参数**

函数 rtrim()接受两个参数，如上面的语法所示。在这两个参数中，一个是强制的，而另一个是可选的。

**$字符串**

该强制参数指定要检查的字符串。

【T0 美元江湖术士】t1

该可选参数指定从字符串中删除哪些字符。如果不提供该参数，则删除以下字符:

“”–空“t”——制表符“n”——新行“x0B”——竖排制表符“r”——回车“——普通空格

**返回值**

返回修改后的字符串。

**样本程序**

这个程序展示了 rtrim()函数的使用，没有指定要删除的字符列表。

```
<?php
$string = &ldquo; Time for "; echo rtrim($string)." edureka";
?>
```

**输出**

爱德华卡的时间

**样本程序**

这个程序展示了 rtrim()函数的使用，它有一个指定的要删除的字符列表。

```
<?php
$string = "Time for !!! (( !!))";
echo rtrim($string, "! ()")." Edureka ";
?>
```

**输出**

爱德华卡的时间

**参数**

string 它用来指定要检查的字符串

charlist 它指定删除哪个字符

**删除字符串两边的空格:**

```
<?php$str="HelloWorld!";echo"Withouttrim:".$str;echo"<br>";echo"With trim:" . trim($str);?>
```

**输出**

T2！DOCTYPE html > < html > <正文>

无修饰:Hello World！< br > With trim: Hello World！</正文> < /html >

至此，我们已经结束了 PHP 文章中的 Trim 函数。我希望你们喜欢这篇文章并理解 PHP 的概念。因此，随着本 PHP 教程的结束，您不再是脚本语言的新手。

*如果您发现这个 PHP 教程博客相关，请查看 Edureka 的* *[**PHP 认证培训**](https://www.edureka.co/php-mysql-self-paced) ，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。*

有问题要问我们吗？请在“PHP 中的 **Trim 函数”的评论部分提及，我会回复你。**