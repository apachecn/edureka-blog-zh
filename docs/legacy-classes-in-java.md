# Java 中的遗留类有哪些？

> 原文：<https://www.edureka.co/blog/legacy-classes-in-java/>

*[Java](https://www.edureka.co/blog/java-tutorial/)* 由几个类和接口组成，用来保存 Java 1.2 版本之前的对象。在这个版本之前，没有 *[收藏框架](https://www.edureka.co/blog/java-collections/)* 的存在。在这种情况下，遗留类和接口用于保存对象。这篇关于 Java 中遗留类的文章将让您深入理解这个概念

*   [Java 中有哪些遗留类？](#Legacyclass)
    *   [字典](#Dictionary)
    *   [属性](#Properties)
    *   [哈希表](#HashTable)
    *   [矢量](#Vector)
    *   [堆栈](#Stack)
*   [遗留接口](#LegacyInterface)
    *   [枚举](#Enumeration)

让我们研究一下遗产类。

## **Java 中有哪些遗留类？**

Java 的早期版本不包括集合框架。只有在 1.2 版中，您才可以真正使用这个遗留类。在这里，最初的类被重新设计以支持集合接口。这些类被称为遗留类。JDK 5 重新设计了所有遗留类和接口，以支持 *[泛型](https://www.edureka.co/blog/generics-in-java/)。*

### **字典**

*[字典](https://www.edureka.co/blog/dictionary-in-java/)* 是一个抽象类。主要工作是将数据保存为键或值对。它以 *[地图](https://www.edureka.co/blog/java-map-interface)* 集合的形式工作。

**属性**

属性类是线程安全的，即多个线程可以共享单个属性对象，而无需外部 *[同步](https://www.edureka.co/blog/synchronization-in-java/)* 。该类中的属性集将保存在键或值对中。属性类扩展了哈希表类。**举例:**

```
package lc;

import java.util.Properties;
import java.util.Set;

public class Test {
public static void main(String[] args) {
Properties pr = new Properties();
pr.put("Joey", "Friends");
pr.put("Rachel", " Friends ");
pr.put("Phoebe", " Friends ");
pr.put("Chandler", " Friends ");
Set<?> creator = pr.keySet();
for (Object ob : creator) {
System.out.println(ob + " stars in " + pr.getProperty((String) ob));
}
}
}

```

**输出:** 钱德勒主演《老友记》菲比主演《老友记》瑞秋主演《老友记》乔伊主演《老友记》

### **Java 中的遗留类:哈希表**

Hashtable 是 Java.util 包的一部分，它是一个扩展 dictionary 类的具体类。哈希表是同步的。从 Java 1.2 框架开始，哈希表类实现了 map 接口，它是集合框架的一部分。

**散列表的例子**

```
import java.util.*;
class HashTableDemo
{
public static void main(String args[])
{
Hashtable<String,Integer>ht = new Hashtable<String,Integer>();
ht.put("a",new Integer(10));
ht.put("b",new Integer(20));
ht.put("c",new Integer(30));
ht.put("d",new Integer(40));

Set st = ht.entrySet();
Iterator itr=st.iterator();
while(itr.hasNext())
{
Map.Entry m=(Map.Entry)itr.next();
System.out.println(itr.getKey()+" "+itr.getValue());
}
}
}

```

**输出:**10203040

### **Java 中的遗留类:Vector**

Vector 类类似于 *[ArrayList](https://www.edureka.co/blog/java-arraylist/)* 类但是有一定的区别。 *[向量](https://www.edureka.co/blog/vector-in-java/)* 一般是同步的。它用在程序员并不真正了解 *[数组](https://www.edureka.co/blog/java-array/)* 长度的地方。

让我们看看这个向量方法提供的一些方法。

| **方法** | **描述** |
| e 元素 At(int 索引) | 此方法返回指定索引处的元素 |
| e 第一元素() | 它有助于返回向量中的第一个元素 |
| 枚举元素() | 这有助于返回向量中柠檬的枚举 |
| e lastellemon_) | 返回向量中的最后一个元素 |
| void removeAllElements() | 它有助于移除矢量的所有元素 |

**举例:**

```
public class Test
{
public static void main(String[] args)
{
Vector ve = new Vector();
ve.add(1);
ve.add(2);
ve.add(3);
ve.add(4);
ve.add(5);
ve.add(6);
Enumeration en = ve.elements();
while(en.hasMoreElements())
{
System.out.println(en.nextElement());
}
}
}

```

**输出:**123456

### **堆栈**

*[栈](https://www.edureka.co/blog/stack-class-in-java/)* 代表后进先出。Stack 类扩展了上面提到的 Vector 类。

```
class Stack{
public static void main(String args[]) {
Stack st = new Stack();
st.push(1);
st.push(2);
st.push(3);
st.push(4);
st.push(5);
Enumeration e1 = st.elements();
while(e1.hasMoreElements())
System.out.print(e1.nextElement()+" ");
st.pop();
st.pop();
System.out.println("nAfter popping out one element&rdquo;);
Enumeration e2 = st.elements();
while(e2.hasMoreElements())
System.out.print(e2.nextElement()+" ");
}
}

```

**弹出一个元素后输出:**1 2 3 4 51 2 3 4

现在，让我们继续下一部分，即遗留接口。

## **遗留接口**

### **枚举:**

*[枚举](https://www.edureka.co/blog/enumeration-in-java/)* 接口用于枚举 Vector 的元素和 hashtable 的所有值以及 properties 类的属性。操作是由 *[迭代器](https://www.edureka.co/blog/iterator-in-java/)* 接口克隆的，还增加了几个操作，比如 remove 方法等等。

至此，我们结束了这篇关于“Java 中的遗留类”的文章。我希望你现在已经清楚这个概念了。继续阅读，继续探索！

既然您已经阅读了这篇 Java 文章中的传统课程，请查看 Edureka 的*Java 认证课程，*这是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。

*我们在这里帮助你踏上成为 java 开发者的每一步。除了这个 Java 面试问题，我们还为想成为 Java 开发者的学生和专业人士设计了一个课程。*

有问题要问我们吗？请在这篇“Java 中的遗留类”文章的评论部分提到它，我们会尽快回复您。