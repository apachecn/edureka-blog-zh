# 关于 Java Hashcode 你需要知道的一切

> 原文：<https://www.edureka.co/blog/java-hashcode/>

HashMaps 和 HashSets 用于操作数据，这是在散列的帮助下完成的。上述方法使用 hashCode()方法来检查和验证哈希值。在 Object 类中实现 hashCode()会为不同的对象产生不同的整数。有时我们可能需要在程序中实现 hashCode 方法。在本文中，我们将详细了解 Java hashcode，

本文主要关注以下几点:

*   [什么是 Java HashCode？](#WhatIsJavaHashCode?)
*   【Java Hashcode 的示例代码

让我们从 Java Hashcode 文章的第一个主题开始，

## **什么是 Java HashCode？**

它返回一个整数形式的 hashcode 值。Hashcode 值主要用在基于哈希的集合中，如 HashMap、HashSet、HashTable 等。这个方法必须在每个覆盖 equals()方法的类中被覆盖。

hashCode()方法的一般约定是:

*   hashCode()的多次调用应该返回相同的整数值，除非 equals()方法中使用的对象属性被修改。
*   一个对象散列码值可以在同一应用程序的多次执行中改变。
*   根据 equals()方法，如果两个对象相等，则它们的哈希代码必须相同。
*   根据 equals()方法，如果两个对象不相等，则不要求它们的哈希码不同。它们的散列码值可能相等也可能不相等。

让我们看一个样本代码来更好地理解这个概念，但是我建议从 [Java 安装](https://java.com/en/download/help/download_options.xml)开始，

## 【Java Hashcode 的示例代码

```
public int hashCode()
```

//该方法返回哈希码值

//对于调用此方法的对象 。

**例子**

```
public class Employee {
protected long employeeId;
protected String firstName;
protected String lastName;
public int hashCode(){
return(int)employeeId;
}
}

```

注意，如果两个 雇员 对象相等，它们也将具有相同的散列码。但是，正如在示例中特别容易看到的，两个 Employee 对象可以不相等，但仍然具有相同的哈希代码。这就对了，我们已经成功探索了这个概念。

关于“Java Hashcode”的这篇文章到此结束。如果你想了解更多，请查看 Edureka 值得信赖的在线学习公司提供的 [**Java 培训**](https://www.edureka.co/java-j2ee-soa-training) 。Edureka 的 Java J2EE 和 SOA 培训和认证课程旨在培训您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。

有问题要问我们吗？请在这篇文章的评论部分提到它，我们会尽快回复你。