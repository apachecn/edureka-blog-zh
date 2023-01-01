# 如何在 PHP 中将字符串转换成数组

> 原文：<https://www.edureka.co/blog/string-to-array-in-php/>

PHP 提供了从字符串转换成数组的函数。在本文中，我们将按照以下顺序了解如何在 [PHP](https://www.edureka.co/blog/php-tutorial-for-beginners/) 中将字符串转换为数组:

*   [PHP 中把字符串转换成数组的介绍](#intro)
*   [Str_split 方法](#str)
*   [PHP 中的字符串数组](#strings)

## **将字符串转换为数组的介绍**

preg_split 函数提供了控制结果数组的选项，并使用正则表达式来指定分隔符。explode 函数在找到指定分隔符的位置拆分字符串。在某种程度上，字符串也可以是字符数组。

**爆炸方式**

向 explode 函数传递一个分隔符和一个字符串，它将字符串拆分成数组元素，并在数组元素中找到分隔符。分隔符可以是单个字符，也可以是多个字符。

![String to Array in PHP](img/a7ceac7b81f8a0af2338c72c4ad6835c.png)

字符串包含由空格和逗号分隔的项目列表。Explode 函数用于通过传递由逗号和空格('，')组成的分隔符字符串作为第一个参数，将列表转换为数组。将要转换的字符串作为第二个参数传递:

```
// string to convert
$fruits = ‘apple, orange, pear, banana, raspberry, peach’;
$fruits_ar = explode(‘, ‘, $fruits);
Var_dump($fruits_ar);
{
[0]=>
String(5) “apple”
[1] =>
String(6) “orange”
[2] =>
String(4) “pear”
[3] =>
String(6) “banana”
[4] =>
String(9) “raspberry”
[5] =>
String(5) “peach”
}
*/

```

在下一个示例中，使用正斜杠(/)作为分隔符将路径名拆分为一个目录数组:

```
$dirs = explode(‘/’, $path);
Var_dump($dirs);
{
[0] =>
String(0) “”
[1] =>
String (4) “home”
[2] =>
String (8) “someuser”
[3] =>
String (9) “documents”
[4] =>
String(5) “notes”
[5] =>
String(4) “misc”
[6] =>
String(0) “”
}
*/

```

结果显示数组中的第一个元素和最后一个元素包含空字符串，因为最后一个正斜杠或第一个正斜杠前面没有任何内容。原始字符串在创建数组元素的点处被拆分。

如果在字符串中找不到分隔符字符串，将返回一个包含一个元素的数组，元素将包含整个字符串。分解功能提供了一个可选的限制参数。

preg_split 函数也使用正则表达式来指定分隔符。Preg_split 还提供了对返回的数组进行更多控制的选项。

## **Str_split 方法**

它将字符串参数转换为元素长度相等的数组。我们可以传递一个长度作为第二个参数，否则它将默认为 1。在下面的例子中，我们传递 3 来创建一个数组，它的元素各有三个字符:

```
$str = ‘abcdefghijklmnopqrstuvwxyz’;
$split = str_split($str, 3);
Print_r($split);
{
[0] => abc
{1} => def
[2] => ghi
[3] => jkl
[4] => mno
[5] => pqr
[6] => stu
[7] => vwx
[8] => yz
}
*/

```

在数组中，最后一项包含剩余的字符，即使少于 length 参数指定的字符。

**Str_word_count**

str_word_count 函数在传递第二个参数时将字符串转换为单词数组。

## **字符串作为字符数组**

字符串不是真正的数组，但可以使用数组语法访问字符串中的字符，如下所示:

```
$str = ‘top dog’;
Echo $str[2];

$str[2] = ‘y’;
Echo $str;

```

使用 echo 显示结果，并将其设置为一个新值。

我们可以使用 for 循环来访问字符串中的单个字符。我们通过使用 for 循环来演示，以查看字母“a”在示例字符串中出现了多少次:

```
$str = ‘An example string’;
$count = 0;
For ($i=0, $len=strlen($str); $i<$len; $i++ ) {
If ( strops(‘Aa’, $str[$i]) !== false ) {
$count++;
}
}
Echo $count; //2

```

在 for 循环中，我们依次检查每个字符，使用 strops 函数检查它是否是' aA '。我们递增$count 变量。在 for 循环的外部显示一次 echo。

在某种程度上，字符串可以被视为字符数组。

至此，我们结束了 PHP 文章中的字符串到数组。我希望您知道如何将字符串转换为数组。

*查看 Edureka 提供的* *[**PHP 认证培训**](https://www.edureka.co/php-mysql-self-paced) ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。*

*有问题吗？请在“PHP 中字符串到数组”的评论部分提到它，我会回复您。*