# 如何在 Java 中将数组列表转换成数组

> 原文：<https://www.edureka.co/blog/array-list-to-array-in-java/>

数组列表是框架集合的子集，存在于**“Java . util”**包中。它说明了 Java 中的动态数组。虽然，它可能比标准数组慢，但是在需要对数组进行大量操作的程序中，它确实很有帮助

*   [数组列表特征](#features)
*   [Java 中的一些常用方法](#common)
*   [将数组列表转换为 Array()语法。](#syntax)
    *   [Array List to Array()–转换为对象数组](#example1)
    *   [数组列表到数组(T[]a)–转换到对象数组](#example2)

## **数组列表的特征**

*   数组列表继承了**抽象**列表类，实现了列表**接口。**
*   数组列表按大小初始化；但是，如果从集合中提取对象，则当集合增大或缩小时，它的大小会增加。
*   Java 数组列表为我们提供了对列表的随机访问。
*   数组列表不能用于旧类型，如 **int，char，**等。包装类用于这种情况。
*   Java 中的数组列表可以看做类似于 C++中的向量。

![Array list to array in java picture 1](img/c56597c72d53c2cf8b00edf3f11c5bcc.png)

Java 数组列表由构造函数和方法组成。下面提到的细节是一些构造函数和方法的列表，以及它们的用法和功能。

*   **ArrayList():** 该构造函数用于创建一个空数组列表
*   **ArrayList(集合** **c):** 该构造函数用于创建一个数组列表，用集合 c 中的元素初始化
*   **ArrayList(int capacity):**该构造函数用于创建一个数组列表，并指定一个初始容量。

让我们看一个简单的代码来创建一个数组列表。

**举例:**

```
import java.io.*;
import java.util.*;

class arrayli {
      public static void main(String[] args) throws IOException {
           int n = 5;
           ArrayList<Integer> arrli = new ArrayList<Integer>(n);
           for (int i = 1; i <= n; i++)
                 arrli.add(i);
           System.out.println(arrli);
           arrli.remove(3);
           System.out.println(arrli);
           for (int i = 0; i < arrli.size(); i++)
                 System.out.print(arrli.get(i) + " ");
      }
}

```

**//输出:**

`[1, 2, 3, 4, 5]``[1, 2, 3, 5]`

## **Java 中的一些常用方法**

*   **forEach(消费者活动):** 对重复性要素的每个要素执行特定的活动，直到所有要素都已处理完毕，或者某个活动引发异常。
*   **retainAll(集合 c):** 它只保留特定集合中包含的列表中的元素。
*   **removeIf(谓词过滤器):** 提取集合中满足给定谓词的所有元素。
*   **contains (Object o):** 如果列表中有指定的元素，则返回 true。
*   **remove (int index):** 删除列表中给定位置的元素。
*   **remove (Object o):** 从列表中删除指定元素的首次出现，如果它存在的话。
*   **get (int index):** 返回列表中特定位置的元素。
*   **subList (int fromIndex，int toIndex):** 返回指定的 fromIndex(包含)和 toIndex(不包含)之间的列表部分。
*   **spliterator():**It对这个列表中的元素创建一个后期绑定和快速失败的 Split 迭代器。

## **将数组列表转换为 Array()语法。**

有两种方法:

*   **第一个方法** 不接受任何参数，返回一个对象类型的数组。我们的职责是迭代 objects 数组，找到所需的元素并将其类型转换为我们想要的类类型。
*   **第二种方法** 中返回的数组运行时类型为指定数组。如果一个列表适合一个指定的数组，它将被返回。否则，一个新的数组立即被分配一个指定数组的运行时类型和这个列表的大小。

在我们填充完所有数组元素后，数组中还剩下更多的空间。然后在所有这些额外的位置填充“null”。

*   **Array List to Array()–转换为对象数组**

对应输出的代码放在该输出的下面。

**举例:**

```
import java.util.ArrayList;
import java.util.Arrays;

public class ArrayListExample {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>(2);
        list.add("A");
        list.add("B");
        list.add("C");
        list.add("D");
        Object[] array = list.toArray();
        System.out.println( Arrays.toString(array) );
        for(Object o : array) {
            String s = (String) o;
            System.out.println(s);
        }
    }
}

```

**//输出:**

`[A, B, C, D]`

`A` `B` `C`

*   **数组列表到数组(T[]a)–转换为字符串数组**

**举例:**

```
import java.util.ArrayList;
import java.util.Arrays;

public class ArrayListExample{
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>(2);
        list.add("A");
        list.add("B");
        list.add("C");
        list.add("D");
        String[] array = list.toArray(new String[list.size()]);
        System.out.println(Arrays.toString(array));
    }
}

```

**//输出:**

`[A, B, C, D]`

到此，我们来结束这篇文章。我希望你已经通过一些实时例子理解了 Java 中的数组列表到数组，它们的类型，重要性以及它们的实现。

*现在您已经了解了 Java 中数组列表到数组的基础知识，请查看 Edureka 提供的  [**Java 培训**](https://www.edureka.co/java-j2ee-soa-training)* *，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在让您在 Java 编程方面有一个良好的开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate&[Spring](https://spring.io/projects/spring-framework)。*

有问题要问我们吗？在这篇“Java 中数组列表”博客的评论部分提到它，我们会尽快回复你。