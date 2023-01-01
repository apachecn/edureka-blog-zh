# 关于 Java 中的流，你需要知道的一切

> 原文：<https://www.edureka.co/blog/stream-in-java/>

Java 8 中新增了一个名为 *java.util.stream 的包，为*用户提供高效的编程体验。流可以定义为一系列对象，支持多种方法。在本文中，我们将探索 [Java](https://www.edureka.co/blog/java-tutorial/) 中的流

本文将涉及以下几点:

*   [生成流](#GeneratingStreams)
*   [对流的操作](#OperationsonStreams)
*   [过滤](#Filtering)
*   [迭代](#Iterating)

在开始这篇关于 Java 流的文章之前，让我们先看看一些重要的特性，

#### **Java 中的流:特性**

*   流不是数据结构，不存储元素。集合、数组或 I/O 通道是它获取输入的地方。
*   在对流执行操作后，流的源保持不变。例如，过滤一个流只是产生一个没有被过滤元素的新流，而不是修改原始流。
*   stream 支持过滤、归约、匹配、查找等聚合操作。
*   懒惰可以被认为是流的一个特征，因为它只在需要的时候评估代码。
*   在流的生存期内，对流中存在的元素的访问只能进行一次。必须创建一个新的流来重新访问源中存在的相同元素。

继续这篇关于 Java 流的文章

## **生成流**

可以通过以下方法生成流:

*   stream()–返回一个顺序流。收藏视为出处。
*   parallel stream()–返回并行流。集合被视为来源。

```
List<String> strings = Arrays.asList("Hello", "", "Hi", "Hola", "Bonjour","", "Namaste");
List<String> filtered = strings.stream().filter(string -> !string.isEmpty()).collect(Collectors.toList());

```

继续这篇关于 Java 流的文章

## **流上的操作:**

#### **中级操作:**

**地图**

根据作为参数传递的谓词，集合中的元素可以映射到其他对象。以下示例通过使用 map 方法来显示数字的唯一正方形。

```
List<Integer> num = Arrays.asList(5,4,4,2,3,3);
List<Integer> squares = num.stream().map( y -> y*y).distinct().collect(Collectors.toList());

```

**过滤器**

通过使用此方法，可以根据标准移除元素。

```
List name = Arrays.asList("Saturday","Sunday","Thursday");
List res = name.stream().filter(s->s.startsWith("S")).collect(Collectors.toList());

```

**已排序**

可以使用此方法对流进行排序。

```
List name = Arrays.asList("Saturday","Sunday","Thursday");
List res = name.stream().sorted().collect(Collectors.toList());

```

#### ***Java 中的流:终端操作:***

**收藏**

可以使用 collect 操作将流元素的处理结果组合起来。

```
List num = Arrays.asList(4,3,2,5,6);
Set res = num.stream().map(y->y*y).collect(Collectors.toSet());

```

**forEach**

该方法用于遍历流中的每个元素。

```
List num = Arrays.asList(4,3,2,5);
num.stream().map(x->x*x).forEach(y->System.out.println(y));

```

**减少**

通过使用此方法，可以将流的元素简化为单个值。

```
List num = Arrays.asList(4,3,2,5);
int even = num.stream().filter(x->x%2==0).reduce(0,(res,i)-> res+i);

```

变量 res 最初赋值为 0，I 加到上面。

继续这篇关于 Java 流的文章

## **过滤**

可以使用流方法过滤代码。在下面的例子中，工具的价格被过滤掉。

```
import java.util.*;
import java.util.stream.Collectors;
class Instrument{
int num;
String name;
float price;
public Instrument(int num, String name, float price) {
this.num = num;
this.name = name;
this.price = price;
}
}
public class Test {
public static void main(String[] args) {
List<Instrument> instrumentsList = new ArrayList<Instrument>();
//Adding Products
instrumentsList.add(new Instrument(1,"Guitar",15000f));
instrumentsList.add(new Instrument(2,"Piano",18000f));
instrumentsList.add(new Instrument(3,"Flute",15000f));
instrumentsList.add(new Instrument(4,"Drums",48000f));
instrumentsList.add(new Instrument(5," Ukulele",32000f));
List<Float> InstrumentPriceList2 =instrumentsList.stream()
.filter(p -> p.price > 30000)// filtering data
.map(p->p.price)//fetching price
.collect(Collectors.toList()); // collecting as list
System.out.println(InstrumentPriceList2);
}
}

```

```
Output:
```

[48000.0, 32000.0]

继续这篇关于 Java 流的文章

## **迭代:**

在 java 中使用 stream 可以进行迭代。

```
import java.util.stream.*;
public class Test {
public static void main(String[] args){
Stream.iterate(1, element->element+1)
.filter(element->element%4==0)
.limit(6)
.forEach(System.out::println);
}
}

```

**输出:**

four

eight

Twelve

Sixteen

Twenty

Twenty-four

让我们来看另一个例子，以便更有效地理解 java 中流的概念。

**举例:**

```
import java.util.*;
import java.util.stream.*;
public class Test
{
public static void main(String args[])
{
//creating a list of integers
List<Integer> num = Arrays.asList(6,7,8,9);
//using map method
List<Integer> squares = num.stream().map(y -> y*y).
collect(Collectors.toList());
System.out.println(squares);
//creating a list of String
List<String> days =
Arrays.asList("Friday","Saturday","Sunday");
//filter method
List<String> res = days.stream().filter(s->s.startsWith("S")).
collect(Collectors.toList());
System.out.println(res);
//sorted method
List<String> display =
days.stream().sorted().collect(Collectors.toList());
System.out.println(display);
//creating a list of integers
List<Integer> number = Arrays.asList(6,9,5,7,1);
//collect method returns a set
Set<Integer> sqSet =
number.stream().map(y->y*y).collect(Collectors.toSet());
System.out.println(sqSet);
//forEach method
num.stream().map(y->y*y).forEach(x->System.out.println(x));
//reduce method
int even =
num.stream().filter(x->x%2==0).reduce(0,(result,i)-> result+i);
System.out.println(even);
}
}

```

**输出:**

[36, 49, 64, 81]

[周六、周日]

[周五、周六、周日]

[81, 49, 1, 36, 25]

Thirty-six

forty-nine

Sixty-four

Eighty-one

Fourteen

***流使用户能够有效地对元素进行操作。***

这样，我们就结束了这篇关于“Java 中的流”的文章。如果您想了解更多，请查看 Edureka 提供的 Java 培训，这是一家值得信赖的在线学习公司。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个博客的评论部分提到它，我们会尽快回复你。