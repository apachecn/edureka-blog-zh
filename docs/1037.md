# Tableau 中的函数以及如何使用它们

> 原文：<https://www.edureka.co/blog/tableau-functions/>

[***Tableau***](https://www.edureka.co/blog/what-is-tableau/)是一个工具，它不仅仅是为了漂亮的图形。Tableau 中的 ***函数对于最佳数据表示至关重要，因此，它是所有 [***Tableau 认证课程***](https://www.edureka.co/tableau-certification-training) 中的主要概念。***

幸运的是，这个工具有各种各样的内置功能，你可以直接应用到你上传的数据中。如果你用过 [***MS Excel***](https://www.edureka.co/blog/tutorial-on-advanced-excel-formulas/) 或者 [***SQL***](https://www.edureka.co/blog/sql-commands) ，这些你应该都很熟悉。

[https://www.youtube.com/embed/VdbBoZpELfg](https://www.youtube.com/embed/VdbBoZpELfg)

因此，下面是我们将在博客中讨论的各种功能。

*   [**数字功能**](#numberfunctions)
*   [**字符串函数**](#stringfunctions)
*   [**日期功能**](#datefunctions)
*   [**类型转换功能**](#typeconversionfunctions)
*   [**聚合函数**](#aggregatefunctions)
*   [**逻辑函数**](#logicalfunctions)

## **数字功能**

Tableau 中的这些内置函数允许您对字段中的数据值进行计算。数字函数只能用于包含数值的字段。以下是 Tableau 中的各种数字函数:

### **1。ABS**

函数 r 返回给定数字的绝对值。

**语法**

T2`ABS(number)`

T2`ABS(-4) = 4`

### **2。ACOS**

函数 r 返回给定弧度数的反余弦值。

**语法**

T2`ACOS(number)`

T2`ACOS(-1) = 3.14159265358979`

### **3。阿辛**

这个函数 r 返回给定弧度数的反正弦值。

**语法**

T2`ASIN(number)`

T2`ASIN(1) = 1.5707963267949`

### **4。ATAN**

这个函数 r 返回给定弧度数的反正切值。

**语法**

T2`ATAN(number)`

T2`ATAN(180) = 1.5652408283942`

### **5。天花板**

函数 r 返回一个给定的整数，四舍五入到最接近的整数。

**语法**

T2`CEILING(number)`

T2`CEILING(3.1415) = 4`

### **6。COS**

这个函数 r 返回给定角度的余弦值，用弧度表示。

**语法**

T2`COS(number)`

T2`COS(PI()/4) = 0.707106781186548`

### **7。吊床**

该函数 r 返回以弧度表示的给定角度的余切值。

**语法**

T2`COT(number)`

T2`CO1(PI()/4) = 1`

### **8。度**

这个函数 r 返回给定角度的值，以度为单位。

**语法**

T2`DEGREES(number)`

T2`DEGREES(PI()/4) = 45`

### **9。DIV**

给定被除数和除数，函数 r 返回商的整数值。

**语法**

T2`DIV(integer1, integer2)`

T2`DIV(11,2) = 5`

### **10。EXP**

这个函数 r 返回 e 的给定数字的幂。

**语法**

T2`EXP(number)`

T2`EXP(2) = 7.389 EXP(-[Growth Rate]*[Time])`

### **11。楼层**

这个函数 r 返回一个给定的数字，四舍五入到最接近的整数，等于或小于这个值。

**语法**

T2`FLOOR(number)`

T2`FLOOR(6.1415) = 6`

### **12。HEXBIN X，Y**

HEXBINX 和 HEXBINY 是六边形仓的宁滨和绘图函数。该函数将 x，y 坐标映射到最近的六边形面元的 x 坐标。箱的边长为 1，因此可能需要对输入进行适当的缩放。

**语法**

T2`HEXBINX(number, number)`

T2`HEXBINX([Longitude], [Latitude])`

### **13。LN**

函数 r 返回给定数字的自然对数。

**语法**

T2`LN(number)`

T2`LN(1) = 0`

### **14。**日志

该函数返回给定数字的以 10 为底的对数。

**语法**

T2`LOG(number, [base])`

T2`LOG(1) = 0`

### **15。MAX**

这个函数 r 返回所传递参数的最大值。

**语法**

T2`MAX(number, number)`

`MAX(4,7) = 7``MAX(Sales,Profit)`

### **16。敏**

这个函数 r 返回传递的参数的最小值。

**语法**

T2`MIN(number, number)`

`MIN(4,7) = 4``MIN(Sales,Profit)`

### **17。PI**

这个函数 r 返回圆周率的值。

**语法**

T2`PI() = 3.142`

### **18。力量**

这个函数 r 返回第一个参数的值乘以第二个参数的幂。

**语法**

T2`POWER(number, power)`

`POWER(2,10) = 1024`

### **19。弧度**

这个函数 r 返回给定角度的弧度值。

**语法**

T2`RADIANS(number)`

`RADIANS(45) = 0.785397`

### **20。一轮**

函数 r 返回给定的数字，四舍五入到指定的小数位数。

**语法**

T2`ROUND(number, [decimal place])`

`ROUND([Profit])`

### **21。**标志

这个函数返回一个给定数字的符号。

**语法**

T2`SIGN(number)`

`SIGN(AVG(Profit)) = -1`

### **22。**罪恶

该函数 r 返回以弧度表示的给定角度的正弦值。

**语法**

T2`SIN(number)`

T2`SIN(PI()/4) = 0.707106781186548`

### **23。SQRT**

这个函数 r 返回给定数字的平方根。

**语法**

T2`SQRT(number)`

T2`SQRT(25) = 5`

### **24。广场**

这个函数 r 返回给定数字的平方。

**语法**

T2`SQUARE(number)`

T2`SQUARE(5) = 25`

### **25。谭**

该函数 r 返回以弧度表示的给定角度的正切值。【T2

**语法**

T2`TAN(number)`

T2`TAN(PI()/4) = 1`

**字符串函数**

Tableau 中的这些内置函数允许你操作字符串数据。您可以使用这些函数做一些事情，比如将所有客户的所有姓氏提取到一个新字段中。以下是 Tableau 中的各种字符串函数；

### **1。ASCII 码**

函数 r 返回所述字符串第一个字符的 ASCII 码。

**语法**

T2`ASCII(string)`

T2`ASCII('A') = 65`

### **2。CHAR**

此函数 r 返回 ASCII 码所代表的字符。

**语法**

T2`CHAR(ASCII code)`

T2`CHAR(65) = 'A'`

### **3。**包含

如果字符串包含所述子串，则函数 r 返回 true。

**语法**

T2`CONTAINS(string, substring)`

T2`CONTAINS(“Edureka”, “reka”) = true`

### **4。ENDSWITH**

给定以所述子串结尾的字符串，函数 r 返回 true。

**语法**

T2`ENDSWITH(string, substring)`

T2`ENDSWITH(“Edureka”, “reka”) = true`

### **5。找到**

如果字符串包含所述子串，此函数 r 返回该子串在字符串中的索引位置，否则为 0。如果添加了可选参数 start，该函数将忽略出现在索引位置 start 之前的子字符串的任何实例。

**语法**

T2`FIND(string, substring, [start])`

T2`FIND(“Edureka”, “reka”) = 4`

### **6。find nth**

如果字符串包含所述子串，函数 r 返回该子串在字符串中第 n 次出现的索引位置。

**语法**

T2`FINDNTH(string, substring, occurrence)`

T2`FIND(“Edureka”, “e”, 2) = 5`

### **7。左**

函数 r 返回给定字符串中最左边的字符数。

**语法**

T2`LEFT(string, number)`

T2`LEFT(“Edureka”, 3) = "Edu" `

### **8。LEN**

这个函数返回给定字符串的长度。

**语法**

T2`LEN(string)`

T2`LEN(“Edureka”) = 7`

### **9。**下层

函数 r 返回小写字母的整个字符串。

**语法**

T2`LOWER(string)`

T2`LOWER(“Edureka”) = edureka`

### **10。LTRIM**

函数 r 返回给定的没有任何空格的字符串。

**语法**

T2`LTRIM(string)`

T2`LTRIM(“ Edureka ”) = "Edureka "`

**11。MAX**

这个函数 r 返回两个传递的字符串参数中的最大值。

**语法**

`MAX(a, b)`

T2`MAX ("Apple","Banana") = "Banana"`

T2

### **12。**中期

函数 r 从起始的索引位置返回给定的字符串。

**语法**

T2`MID(string, start, [length])`

T2`MID("Edureka", 3) = "reka" `

### **13。敏**

这个函数 r 返回两个传递的字符串参数中的最小值。

**语法**

`MIN(a, b)`

T2`MIN ("Apple","Banana") = "Apple"`

### **14。替换**T3

这个函数 s 在给定的字符串 中搜索子字符串 ，并用替换项进行替换。

**语法**

`REPLACE(string, substring, replacement)`

T2`REPLACE("Version8.5", "8.5", "9.0") = "Version9.0"`

### **15。右**

函数 r 返回给定字符串中最右边的字符数。

**语法**

T2`RIGHT(string, number)`

T2`RIGHT(“Edureka”, 3) = "eka" `

### **16。RTRIM**

这个函数返回给定的字符串，没有任何后续空格。

**语法**

T2`RTRIM(string)`

T2`RTRIM(“ Edureka ”) = " Edureka"`

### **17。空间**

函数 r 返回一个由指定数量的空格组成的字符串。

**语法**

T2`SPACE(number)`

T2`SPACE(1) = " "`

### **18。**分裂

这个函数 r 从一个字符串中返回一个子串，使用一个分隔符将字符串分成一系列的记号。

**语法**

T2`SPLIT(string, delimiter, token number)`

T2`SPLIT (‘a-b-c-d’, ‘-‘, 2) = ‘b’ SPLIT (‘a|b|c|d’, ‘|‘, -2) = ‘c’`

### **19。以**开始

给定以所述子串开始的字符串，该函数 r 返回 true。

**语法**

T2`STARTSWITH(string, substring)`

T2`STARTSWITH(“Edureka”, “Edu”) = true`

### **20。修剪**

这个函数返回给定的字符串，前后没有空格。

**语法**

T2`TRIM(string)`

T2`TRIM(“ Edureka ”) = "Edureka"`

### **21。上层**

这个函数以大写字母返回整个给定的字符串。【T2

**语法**

T2`UPPER(string)`

T2`UPPER(“Edureka”) = EDUREKA`

**日期功能**

Tableau 中的这些内置函数允许您操作数据源中的日期，如年、月、日、日和/或时间。以下是 Tableau 中的各种日期函数:

### **1。DATEADD**

此函数 r 返回指定日期，该日期的指定日期部分 加上指定的数字区间 。

**语法**

T2`DATEADD(date_part, interval, date)`

T2`DATEADD('month', 3, #2019-09-17#) = 2019-12-17 12:00:00 AM`

### **2。**DATEDIFF

函数 r 返回两个日期之间的差值，以日期部分的单位表示。一周的开始可以根据用户的需要进行调整。

**语法**

T2`DATEDIFF(date_part, date1, date2, [start_of_week])`

T2`DATEDATEDIFF('week', #2019-12-15#, #2019-12-17#, 'monday')= 1 `

### **3。** 日期名称

函数 r 以字符串形式返回日期的日期部分。

**语法**

T2`DATENAME(date_part, date, [start_of_week])`

T2`DATENAME('month', #2019-12-17#) = December`

### **4。日戳**

该函数以整数形式返回日期的日期部分。

**语法**

T2`DATEPART(date_part, date, [start_of_week])`

T2`DATEPART('month', #2019-12-17#) = 12`

### **5。**

此函数返回指定日期的截断形式，精度由日期部分指定。通过这个函数，您基本上可以返回一个新的日期。

**语法**

T2`DATETRUNC(date_part, date, [start_of_week])`

T2`DATETRUNC('quarter', #2019-12-17#) = 2019-07-01 12:00:00 AM  DATETRUNC('month', #2019-12-17#) = 2019-12-01 12:00:00 AM`

### **6。** 日

这个函数以整数的形式返回给定日期的第几天。

**语法**

T2`DAY(Date)`

T2`DAY(#2019-12-17#) = 17`

### **7。ISDATE**

给定一个字符串是有效日期，该函数返回 true。

**语法**

T2`ISDATE(String)`

T2`ISDATE(December 17, 2019) = true`

### **8。** 制造日期

该函数返回从指定的年、月、日构造的日期值。

**语法**

T2`MAKEDATE(year, month, day)`

T2`MAKEDATE(2019, 12, 17) = #December 17, 2019#`

### **9。make datetime**

该函数返回日期和时间值，该值由指定的年、月和日以及小时、分钟和秒构成。

**语法**

T2`MAKEDATETIME(date, time)`

`MAKEDATETIME("2019-12-17", #11:28:28PM#) = #12/17/2019 11:28:28 PM#` `MAKEDATETIME([Date], [Time]) = #12/17/2019 11:28:28 PM#`

### **10。MAKETIME**

该函数返回由指定的小时、分钟和秒构造的时间值。

**语法**

T2`MAKETIME(hour, minute, second)`

T2`MAKETIME(11, 28, 28) = #11:28:28#`

### **11。** 月

此函数以整数形式返回给定日期的月份。

**语法**

T2`MONTH(Date)`

T2`MONTH(#2019-12-17#) = 12`

### **12。现在**

这个函数返回当前的日期和时间。

**语法**

T2`NOW()`

T2`NOW() = 2019-12-17 11:28:28 PM`

### **13。今日**

这个函数返回当前日期。

**语法**

T2`TODAY()`

T2`TODAY() = 2019-12-17`

### **14。** 年份

此函数以整数形式返回给定日期的年份。

**语法**

T2`YEAR(Date)`

T2`YEAR(#2019-12-17#) = 2019`

## **类型转换功能**

Tableau 中的这些内置函数允许您将字段从一种数据类型转换为另一种数据类型，例如，您可以将数字转换为字符串，以防止或启用 Tableau 聚合。下面是 Tableau 中的各种类型转换函数；

### **1。日期**

给定一个数字、字符串或日期表达式，此函数返回一个日期。

**语法**

T2`DATE(expression)`

`DATE([Employee Start Date])``DATE("December 17, 2019") = #December 17, 2019#``DATE(#2019-12-17 14:52#) = #2019-12-17#`

### **2\. DATETIME**

给定一个数字、字符串或日期表达式，此函数返回一个日期时间。

**语法**

T2`DATETIME(expression)`

`DATETIME(“December 17, 2019 07:59:00”) = December 17, 2019 07:59:00`

### 3。给自己【

给定一个字符串，这个函数以指定的格式返回一个日期时间。

**语法**

`DATEPARSE(format, string)`

`DATEPARSE ("dd.MMMM.yyyy", "17.December.2019") = #December 17, 2019#`T2T4`DATEPARSE ("h'h' m'm' s's'", "11h 5m 3s") = #11:05:03#`

### **4。漂浮**

该函数用于将其参数转换为浮点数。

**语法**

`FLOAT(expression)`

`FLOAT(3)`=`3.000``FLOAT([Salary])`

### **5。INT**

该函数用于将其参数转换为整数。对于某些表达式，它还会将结果截断为最接近零的整数。

**语法**

`INT(expression)`

`INT(8.0/3.0) = 2``INT(4.0/1.5) = 2`

### **6。弦**

这个函数用来把它的参数转换成一个字符串。

**语法**

`STR(expression)`

`STR([Date])`

## **聚合函数**

Tableau 中的这些内置函数允许您汇总或更改数据的粒度。以下是 Tableau 中的各种聚合函数:

### **1。ATTR**

如果所有行只有一个值，该函数返回表达式的值，忽略空值，否则返回星号。

**语法**

`ATTR(expression)`

### **2。AVG**

该函数返回表达式中所有值的平均值，忽略空值。AVG 只能用于数值字段。

**语法**

`AVG(expression)`

### **3。收藏**

这是一个聚合计算，它组合了参数字段中的值，忽略了空值。

**语法**

`COLLECT(Spatial)`

### **4。CORR**

此计算返回两个表达式的皮尔逊相关系数。

***皮尔逊相关*** 衡量两个变量之间的线性关系。结果范围从-1 到+1(包括-1 和+1 ),其中 1 表示精确的正线性关系，因为一个变量的正变化意味着另一个变量相应幅度的正变化，0 表示方差之间没有线性关系，1 表示精确的负关系。

**语法**

`CORR(expr1, expr2)`

### **5。数一数**

这是一个函数，用于返回一个组中的项目数，忽略空值。也就是说，如果同一个项目有多个编号，该函数会将其计为单独的项目，而不是单个项目。

**语法**

`COUNT(expression)`

### **6。COUNTD**

这是一个函数，用于返回一个组中项目的不同计数，忽略空值。也就是说，如果同一个项目有多个编号，该函数会将其计为一个项目。

**语法**

`COUNTD(expression)`

### **7。科瓦尔**

这是一个返回两个表达式的**样本协方差**的函数。

两个变量一起变化的性质可以用**协方差**来量化。正协方差表示变量趋向于同向移动，当一个变量的值趋向于变大时，另一个变量的值也趋向于变大。S 当数据是用于估计较大总体协方差的随机样本时，充分协方差是合适的选择。

**语法**

`COVAR(expr1, EXPR2)`

### **8 个。covarT3 号机**

这是一个返回两个表达式的**人口协方差**的函数。

当存在整个群体(而不仅仅是一个样本)所有感兴趣项目的可用数据时，群体协方差是合适的选择。

**语法**

`COVARP(expr1, EXPR2)`

### **9。MAX**

该函数返回所有记录中表达式的最大值，忽略空值。

**语法**

`MAX(expression)`

### **10。中位数**

此函数返回所有记录的表达式的中值，忽略空值。

**语法**

`MEDIAN(expression)`

### **11。敏**

该函数返回所有记录中表达式的最小值，忽略空值。

**语法**

`MIN(expression)`

### **12。百分位数**

该函数返回给定表达式的百分比值。返回的数字必须介于 0 和 1 之间，例如 0.34，并且必须是数字常量。

**语法**

`PERCENTILE(expression, number)`

### **13。STDEV**

Tableau 中的这个函数根据总体样本返回给定表达式中所有值的统计**标准差**。

**语法**

`STDEV(expression)`

### **14\. STDEVP**

Tableau 中的这个函数根据有偏总体返回给定表达式中所有值的统计**标准差**。

**语法**

`STDEVP(expression)`

### **15。总和**

Tableau 中的这个函数返回表达式中所有值的和，忽略空值。SUM 只能用于数值字段。

**语法**

`SUM(expression)`

### **16 个。这里是 T2，T3**

给定基于总体样本的表达式，此函数返回所有值的统计方差。

**语法**

`VAR(expression)`

### **17 个。麻雀变凤凰**

给定基于总体的表达式，此函数返回所有值的统计方差。

**语法**

`VARP(expression)`

## **逻辑函数**

Tableau 中的这些内置函数可以让你确定某个条件是真还是假(布尔逻辑)。以下是 Tableau 中的各种逻辑函数:

### **1。还有**

此函数对两个表达式执行逻辑 AND(合取)。对于和，要返回 true，必须满足指定的两个条件。

**语法**

`IF <expr1> AND <expr2> THEN <then> END`

`IF (ATTR([Market]) = "Asia" AND SUM([Sales]) > [Emerging Threshold] )THEN "Well Performing"`

### **2。案例**

Tableau 中的这个函数执行逻辑测试并返回适当的值，类似于大多数常见编程语言中的 SWITCH CASE。

当一个值与给定表达式中指定的条件匹配时，CASE 返回相应的返回值。如果没有找到匹配项，则使用默认的返回表达式。如果没有默认返回，也没有匹配的值，则该函数返回 NULL。

CASE 通常比 IIF 或 IF THEN ELSE 更容易使用。

**语法**

`CASE <expression>` `WHEN <value1> THEN <return1>` `WHEN <value2> THEN <return2> ...` `ELSE <default return>`

`CASE [Region] WHEN 'West' THEN 1 WHEN 'East' THEN 2 ELSE 3 END`

### **3。ELSE &如果，那么**

Tableau 中的这个函数测试一系列输入，为满足 IF 条件的第一个表达式返回 THEN 值。

**语法**

`IF <expr> THEN <then> ELSE <else> END`

`IF [Profit] > 0 THEN 'Profit' ELSE 'Loss' END`

### **4。埃尔塞夫**

Tableau 中的这个函数测试一系列输入，为满足 ESLEIF 条件的第一个表达式返回 THEN 值。

**语法**

`IF <expr> THEN <then> [ELSEIF <expr2> THEN <then2>...] ELSE <else> END`

`IF [Profit] > 0 THEN 'Profit' ELSEIF [Profit] = 0 THEN 'No Profit No Loss' ELSE 'Loss' END`

### **5。结束**

这个函数结束一个表达式。

**语法**

`IF <expr> THEN <then> [ELSEIF <expr2> THEN <then2>...] ELSE <else> END`

`IF [Profit] > 0 THEN 'Profit' ELSEIF [Profit] = 0 THEN 'No Profit No Loss' ELSE 'Loss' END`

### **6 个。ifnull**的缩写形式

此 Tableau 函数返回 expr1 not NULL，否则返回 expr2。

**语法**

`IFNULL(expr1, expr2)`

`IFNULL ([Profit], 0)`

### **7。IIF**

这个 Tableau 函数 c 检查一个条件是否被满足，如果为真则返回一个值，如果为假则返回另一个值，如果未知则返回第三个值或 NULL。

**语法**

`IIF(test, then, else, [unknown])`

`IIF([Profit] > 0, 'Profit', 'Loss', 0)`

### **8。ISDATE**

这个函数 c 检查一个给定的字符串是否是一个有效的日期，如果是，返回 true。

**语法**

`ISDATE(String)`

`ISDATE("2004-04-15") = True`

### **9。is null**

此函数 c 检查给定的表达式是否包含有效数据，如果包含，则返回 true。

**语法**

`ISNULL(expression)`

`ISNULL ([Profit])`

### **10。不是**

该函数对给定的表达式执行逻辑非(非)运算。

**语法**

`IF NOT <expr> THEN <then> END`

`IF NOT [Profit] > 0 THEN "No Profit" END`

### **11。或者**

这个函数对两个表达式执行逻辑或运算。要使或返回 true，必须满足指定的两个条件中的任何一个。

**语法**

`IF <expr1> OR <expr2> THEN <then> END`

`IF [Profit] < 0 OR [Profit] = 0 THEN "Needs Improvement" END`

### **12。当**

该函数查找满足给定表达式中条件的第一个值，并返回相应的返回值。

**语法**

`CASE <expr> WHEN <Value1> THEN <return1> ... [ELSE <else>] END`

`CASE [RomanNumberals] WHEN 'I' THEN 1 WHEN 'II' THEN 2 ELSE 3 END`

### **13。ZN**

Tableau 中的这个函数如果不为空则返回给定的表达式，否则返回零。

**语法**

`ZN(expression)`

`ZN([Profit])`

*这些都是 Tableau 中必不可少的功能，要了解更多关于 Tableau 和与之相关的各种概念，你可以查看 [**这个播放列表**](https://www.edureka.co/blog/do-magic-with-tableau) 。*

*如果你希望掌握 Tableau，Edureka 有一个关于 **[Tableau 培训&认证](https://www.edureka.co/tableau-certification-training)** 的策划课程，该课程深入涵盖了数据可视化的各种概念，包括条件格式、脚本、链接图表、仪表板集成、Tableau 与 R 的集成等等。*