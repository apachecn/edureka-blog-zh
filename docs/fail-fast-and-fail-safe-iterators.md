# Java 中的 Fail Fast 和 Fail Safe 迭代器:区别是什么？

> 原文：<https://www.edureka.co/blog/fail-fast-and-fail-safe-iterators/>

Java 集合支持两种类型的迭代器，第一种是快速失效，第二种是安全失效。当涉及到 Java 中的异常处理时，这些起着至关重要的作用。在这篇关于“快速失效和安全失效迭代器”的文章中，我们将分析这两种迭代器的工作原理以及它们之间的本质区别。

以下是本文将要讨论的要点:

*   [并发修改](#ConcurrentModifications)
*   [快速迭代器失败](#FailFastIterator)
*   [故障安全迭代器](#FailSafeIterator)
*   [故障快速与故障安全迭代器](#FailFastvsFailSafeIterator)

在详细解释之前，让我们先熟悉一下并发修改的概念。

## **并发修改**

当单个线程(或多个线程)遍历集合时，它可以通过添加或删除集合中的元素，或者通过更新特定位置的元素值来更改集合的结构。这个过程被称为并行修改。

让我们快速地看一下与上述主题有关的两个系统，然后再进入相同的细节，

### **故障快速系统:**

如果一个系统在错误发生后立即关闭，则该系统被标记为故障快速系统。操作会立即中止，并暴露故障或错误。

### **故障安全系统:**

如果一个系统在故障或错误发生后仍能继续运行，则该系统被称为故障安全系统。他们不会中止操作并隐藏错误，而不是暴露错误。

java 中的迭代器允许我们遍历集合对象。集合返回的迭代器本质上不是快速失效就是安全失效。

## **快速迭代器失败**

Java 中的失败快速迭代器不允许在对集合进行迭代时对其进行任何类型的结构修改。结构修改包括在迭代集合时添加、移除或更新集合中的任何元素。如果在迭代过程中对集合进行了结构修改，迭代器将抛出 ConcurrentModificationException。

但是，必须注意，如果使用迭代器自己的方法(即 remove()方法)移除一个项，则不会抛出异常。这是一个完全安全的过程。确保您的系统上安装了 Java

### **失败快速迭代器示例:**

```
import java.util.HashMap;
import java.util.Iterator;
import java.util.Map;

public class FailFastExample {

public static void main(String[] args) {
Map monthIndex = new HashMap();
monthIndex.put("1", "January");
monthIndex.put("2", "February");
monthIndex.put("3","March");

Iterator iterator = monthIndex.keySet().iterator();

while (iterator.hasNext()) {
System.out.println(monthIndex.get(iterator.next()));
//adding an element to Map
//exception will be thrown on next call
//of next() method.
monthIndex.put("4", "April");
}
}
}

```

**输出:**

线程“main”Java . util . concurrentmodificationexception 中出现异常

at Java . util . hashmap $ hashiterator . next entry(未知来源)

现在让我们继续看一看故障安全迭代器，

## **故障安全迭代器**

与失败快速迭代器不同，如果集合在迭代过程中被修改，失败安全迭代器不会抛出任何异常。这是因为它们迭代的是集合的克隆，而不是实际的集合。他们没有注意到对实际集合所做的结构修改。

然而，应该注意的是，不存在真正的故障安全迭代器。称之为弱一致是恰当的。这仅仅意味着 ***如果*** 一个集合在迭代的过程中被修改，迭代器看到的是弱保证的。不同的集合有不同的行为，在 Javadocs 中有记录。

### **故障安全迭代器示例:**

```

public class FailSafeExample {

	public static void main(String[] args) {
	    ConcurrentMap monthIndex = new ConcurrentHashMap();
	    monthIndex.put("1", "January");
	    monthIndex.put("2", "February");
	    monthIndex.put("3","March");

	    Iterator iterator = monthIndex.keySet().iterator();

	    while (iterator.hasNext()) {
	        System.out.println(monthIndex.get(iterator.next()));
	        monthIndex.put("4", "April");
	    }       
	}    
}

```

**输出:**

*   一月
*   二月
*   三月

最后，在本文中，我们将比较这些迭代器，

## **区别:快速失效和安全失效迭代器**

下面给出了两个迭代器之间的本质区别:

| **参数** | **快速迭代器失败** | **故障安全迭代器** |
| ***抛出并发修改异常*** | 是的，如果一个集合在迭代过程中被修改，它们会抛出 CocurrentModificationExcepti-on。 | 不，如果一个集合在迭代过程中被修改，它们不会抛出任何异常。 |
| ***克隆收藏*** | 不，它们使用原始集合来遍历元素。 | 是的，他们使用原始集合的副本来遍历。 |
| ***内存开销*** | 不，它们不需要额外的内存。 | 是的，它们需要额外的内存来克隆集合。 |
| ***例句*** | HashMap, Vector,ArrayList,HashSet | copy onwriterarraylist |

这些迭代器在通用的 java 语言中既独特又非常需要。尽管 fail safe 有一个令人欣慰的光环，但 fail fast 迭代器被证明是健壮的。

这就引出了本文的结尾。如果你想了解更多，请查看 Edureka 的 [**Java 培训**](https://www.edureka.co/java-j2ee-soa-training) 。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在为您提供 Java 编程的良好开端，并培训您核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这个“快速失败 vs 安全失败”博客的评论部分提到它，我们会尽快回复你。