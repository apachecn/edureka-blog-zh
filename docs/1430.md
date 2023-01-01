# 如何在 Python 中获取和修改日期时间？

> 原文：<https://www.edureka.co/blog/date-time-in-python/>

时间无疑是生活方方面面最关键的因素。因此，记录和跟踪这个组件变得非常必要。在 [Python](https://www.edureka.co/blog/python-tutorial/) 中，可以通过其内置的[库](https://www.edureka.co/blog/python-libraries/)跟踪日期和时间。这篇关于 Python 中日期和时间的文章将帮助您理解如何使用*时间*和*日期时间*模块来查找和修改日期和时间。

*   [Python 中处理日期和时间的模块](#modules)
*   [时间模块](#time)
    *   [内置函数](#timefunctions)
    *   [格式代码](#formatcodes)
    *   [使用*时间*在 Python 中查找并修改日期和时间](#timeexamples)
*   [日期时间模块](#datetime)
    *   [内置函数](#datetimefunctions)
    *   [使用*datetime*在 Python 中查找并修改日期和时间](#datetimeexamples)

## **Python 中处理日期和时间的模块**

Python 提供了 ***时间*** 和 ***日期时间*** 模块，帮助您轻松获取和修改日期和时间。让我们来详细了解一下其中的每一项。

## **时间模块:**

该模块由所有与时间相关的[函数](https://www.edureka.co/blog/python-functions)组成，这些函数需要使用时间来执行各种操作。它还允许您访问各种用途所需的几种类型的时钟。

### **内置函数:**

请看下表，它描述了时间模块的一些重要的内置函数。

| 功能 | 描述 |
| 时间() | 返回自纪元以来经过的秒数 |
| ctime() | 以经过的秒数作为参数，返回当前日期和时间 |
| 睡眠() | 在给定的持续时间内停止执行线程 |
| time.struct_time 类 | 函数要么将该类作为参数，要么将其作为输出返回 |
| 本地时间() | 将自 epoch 以来经过的秒数作为参数，并以 time.struct_time 格式返回日期和时间 |
| gmtime() | 类似于 localtime()，以 UTC 格式返回 time.struct_time |
| mktime() | localtime()的倒数。获取包含 9 个参数的元组，并返回从 epoch pas 输出开始经过的秒数 |
| asctime() | 接受包含 9 个参数的元组，并返回表示相同参数的字符串 |
| strftime() | 接受一个包含 9 个参数的元组，并根据使用的格式代码返回表示相同参数的字符串 |
| strptime() | 分析字符串并以 time.struct_time 格式返回 |

## **格式代码:**

在继续举例解释每个函数之前，先看看所有合法的*格式代码*:

| 密码 | 描述 | 例子 |
| %a | 工作日(简短版) | 孟人 |
| %A | 工作日(完整版) | 星期一 |
| %b | 月份(简写版) | 八月 |
| %B | 月份(完整版) | 八月 |
| %c | 本地日期和时间版本 | 2019 年 8 月 23 日星期二 1:31:40 |
| %d | 描述一个月中的某一天(01-31) | 07 |
| %f | 微秒 | 000000-999999 |
| %H | 小时(00-23) | Fifteen |
| %I | 小时(00-11) | three |
| %j | 一年中的某一天 | Two hundred and thirty-five |
| %m | 月份号(01-12) | 07 |
| %M | 分钟(00-59) | Forty-five |
| %p | 上午/下午 | 调幅;振幅调制(amplitude modulation) |
| %S | 秒(00-59) | Fifty-seven |
| %U | 从星期日开始的一年中的第几周(00-53) | Thirty-four |
| %w | 一周中的星期几 | 星期一(1) |
| %W | 从星期一开始的一年中的第几周(00-53) | Thirty-four |
| %x | 当地日期 | 06/07/19 |
| %X | 当地时间 | 12:30:45 |
| %y | 年份(简写) | Nineteen |
| %Y | 年份(完整版) | Two thousand and nineteen |
| %z | 协调世界时偏移 | +0100 |
| %Z | 时区 | 中央标准时间 |
| %% | %字符 | % |

struct _ time 类具有以下属性:

| 属性 | 价值 |
| tm _ 年 | 0000, .., 2019, …, 9999 |
| tm_mon(消歧义) | 1-12 |
| tm_mday | 1-31 |
| tm _ 小时 | 0-23 |
| tm_min | 0-59 |
| tm _ 秒 | 0-61 |
| tm_wday | 0-6(星期一是 0) |
| 日 | 1-366 |
| tm_isdst | 0，1，-1(夏令时，未知时，-1) |

现在让我们举几个例子来实现 ***时间*** 模块。

## **使用*时间* :** 在 Python 中查找日期和时间

使用上表中描述的内置函数和格式代码，您可以轻松地在 Python 中获取日期和时间。请注意，就像所有模块一样， **time** 模块也需要在使用任何内置函数之前导入。

**举例:**

```
import time
#time
a=time.time()           #total seconds since epoch
print("Seconds since epoch :",a,end='n----------n')
#ctime
print("Current date and time:")
print(time.ctime(a),end='n----------n') 
#sleep
time.sleep(1)     #execution will be delayed by one second
#localtime
print("Local time :")
print(time.localtime(a),end='n----------n')
#gmtime
print("Local time in UTC format :")
print(time.gmtime(a),end='n-----------n')
#mktime
b=(2019,8,6,10,40,34,1,218,0)
print("Current Time in seconds :")
print( time.mktime(b),end='n----------n')
#asctime
print("Current Time in local format :")
print( time.asctime(b),end='n----------n')
#strftime
c = time.localtime() # get struct_time
d = time.strftime("%m/%d/%Y, %H:%M:%S", c)
print("String representing date and time:")
print(d,end='n----------n')
#strptime
print("time.strptime parses string and returns it in struct_time format :n")
e = "06 AUGUST, 2019"
f = time.strptime(e, "%d %B, %Y")
print(f)
```

**输出:**

自纪元以来的秒数:1565070251.7134922————当前日期时间:2019 年 8 月 6 日星期二 11:14:11————当地时间:time . struct _ time(TM _ year = 2019，tm_mon=8，tm_mday=6，tm_hour=11，tm_min=14，tm_sec=11，tm_wday TM _ isdst = 0)———当前时间秒:1565068234.0———当前时间本地格式:Tue Aug 6 10:40:34 2019———表示日期和时间的字符串: 08/06/2019，11:14:12

time.struct_time(tm_year=2019，tm_mon=8，tm_mday=6，tm_hour=0，tm_min=0，tm_sec=0，tm_wday=1，tm_yday=218，tm_isdst=-1)

## **日期时间模块:**

与时间模块类似，datetime 模块也包含所有处理日期和时间所必需的方法。

### **内置函数:**

下表描述了该模块中的一些重要功能:

| 功能 | 描述 |
| 日期时间() | 日期时间构造函数 |
| 日期时间.今天() | 返回当前的本地日期和时间 |
| datetime.now() | 返回当前的本地日期和时间 |
| 日期() | 以年、月、日为参数，创建相应的日期 |
| 时间() | 将小时、分钟、秒、微秒和 tzinfo 作为参数，并创建相应的日期 |
| date.fromtimestamp() | 转换秒以返回相应的日期和时间 |
| 时间间隔() | 它是不同日期或时间之间的差异(持续时间) |

## **使用*日期时间* :** 在 Python 中查找日期和时间

现在，让我们尝试使用 *datetime* 模块在 Python 中实现这些函数来查找日期和时间。

**举例:**

```
import datetime
#datetime constructor
print("Datetime constructor:n")
print(datetime.datetime(2019,5,3,8,45,30,234),end='n----------n')

#today
print("The current date and time using today :n")
print(datetime.datetime.today(),end='n----------n')

#now
print("The current date and time using today :n")
print(datetime.datetime.now(),end='n----------n')

#date
print("Setting date :n")
print(datetime.date(2019,11,7),end='n----------n')

#time
print("Setting time :n")
print(datetime.time(6,30,23),end='n----------n')

#date.fromtimestamp
print("Converting seconds to date and time:n")
print(datetime.date.fromtimestamp(23456789),end='n----------n')

#timedelta
b1=datetime.timedelta(days=30, seconds=0, microseconds=0, milliseconds=0, minutes=0, hours=4, weeks=8)
b2=datetime.timedelta(days=3, seconds=0, microseconds=0, milliseconds=0, minutes=0, hours=4, weeks=8)
b3=b2-b1
print(type(b3))
print("The resultant duration = ",b3,end='n----------n')

#attributes
a=datetime.datetime.now()   #1
print(a)
print("The year is :",a.year)

print("Hours :",a.hour)

```

**输出:**

日期时间构造函数:

2019-05-03 08:45:30.000234————当前日期和时间使用今天:

2019-08-06 13:09:56.651691————当前日期和时间使用今天:

2019-08-06 13:09:56.651691————设定日期:

2019-11-07————凝固时间:

06:30:23————将秒转换为日期和时间:

1970-09-29——-<类' datetime.timedelta' > 合成时长= -27 天 0:00:00——-2019-08-06 13:09:56.653694 年份为:2019 小时数:13

这就把我们带到了“Python 中的日期和时间”这篇文章的结尾。我希望你已经明白了一切。

***Make sure you practice as much as possible and revert your experience.*  **

*有问题吗？请在“Python 中的生成器”博客的评论部分提到它，我们会尽快回复您。*

*要深入了解 Python 及其各种应用，您可以注册参加现场 **[Python 认证培训](https://www.edureka.co/data-science-python-certification-course)** ，全天候支持，终身访问。*