# Python 中的字符串介绍

> 原文：<https://www.edureka.co/blog/strings_in_python/>

[//www.youtube.com/embed/MDGwbJ3og2s](//www.youtube.com/embed/MDGwbJ3og2s)

在 Python 中，只需用引号将字符括起来就可以创建字符串。Python 不支持字符类型。这些被视为长度为一的字符串，也被视为子字符串。子字符串是不可变的，一旦创建就不能更改。

字符串是用单引号或双引号括起来的有序文本块。因此，任何用引号括起来的内容都被认为是字符串。虽然可以用单引号或双引号来写，但双引号允许用户将字符串扩展到多行而没有反斜线，这通常是表达式继续的信号，例如' abc '，' ABC '。

## **串联和重复**

*   **字符串用+号连接:**

> > > ' abc'+'def '

' abcdef '

*   **字符串以*符号重复:**

> > > ' abc'*3

‘abcabcabc’

## **分度和切片操作**

*   Python 从“0”开始索引
*   字符串 s 将具有从 0 到 len(s)-1(其中 len(s)是 s 的长度)的整数数量的索引。
*   S[i]获取 s 中的第 I 个元素。

## **内置字符串方法**

以下是可在 Python 中使用的内置字符串方法:

*   **大写()–**将字符串的第一个字母大写。
*   **count(str，beg= 0，end = len(string))–**在给定起始索引‘beg’和结束索引‘end’的情况下，统计 str 在字符串或字符串的子字符串中出现的次数。
*   **encode(encoding='UTF-8 '，errors = ' strict ')–**返回字符串的编码字符串版本；如果出现错误，默认值将引发 ValueError，除非错误带有“ignore”或“replace”。
*   **decode (encoding='UTF-8 '，errors = ' strict ')–**使用为编码注册的编解码器对字符串进行解码。编码默认为默认的字符串函数。
*   **index(str，beg=0，end=len(string))-** 与 find()相同，但如果找不到 str 则会引发异常。
*   **max(str)-** 从字符串 str 中返回最大的字母字符。
*   **min(str)-** 从字符串 str 中返回最小的字母字符。
*   **replace(old，new [，max])-** 将字符串中所有出现的“old”替换为“new”或最大值(如果给定了 max)。
*   **upper()-** 将字符串中的小写字母转换成大写字母。

有问题要问我们吗？在评论区提到它们，我们会给你回复。

**相关帖子:**

[Python 大数据分析入门](https://www.edureka.co/blog/free-webinar-on-python-for-big-data-analytics/ "Introduction to Python for Big Data Analytics")

[Python 进行大数据分析](https://www.edureka.co/blog/videos/python-for-big-data-analytics-2/ "Python for Big Data Analytics")

[学习 Python 进行大数据分析](https://www.edureka.co/python "Python for Big Data Anylytics")