# 理解 Java 哈希表

> 原文：<https://www.edureka.co/blog/understanding-java-hashmaps/>

[//www.youtube.com/embed/_PRb8x_q578](//www.youtube.com/embed/_PRb8x_q578)

## **什么是 Java 散列表？**

Java HashMap 是一个类，用于执行诸如在地图中插入、删除和定位元素的操作。我们创建一个映射，在这里我们传递两种类型的值，即“键”和“值”。

使用 HashMap 时，值将被放入 HashMap 中，每当用户检索一个值时，将使用键来使用该值。

映射是将键映射到元素的接口。地图是无序的。它们允许一个空键和多个空值。这些值存储在键和值中。在整个 HashMap 中，一个键或多个值可能为 null。密钥可以是任何对象。

在 HashMap 中有几个可用的方法

*   对象放置(对象键，对象值)
*   枚举键()–它将获取键
*   Enumeration elements()–它将获取元素
*   Object get(Object keys)–传递键并获取与之相关的值
*   布尔包含键(对象键)–用于检查一个键是否存在于 HashMap 中
*   布尔包含值(对象键)–传递键
*   移除物体(物体钥匙)–传递钥匙并移除物体
*   Int size()–用于使用大小
*   String to String()–用于转换成字符串

每个键都有相应的值，哈希表中的值也可以为空。

**HashMap 的创建。**

HashMap HashMap = new HashMap()；

**太岁元素**

hashmap.put("Ankita "，9634.58)；

hashmap.put("Vishal "，1283.48)；

hashmap.put("Gurinder "，1478.10)；

hashmap.put("克里希纳"，199.11)；

在这里，我们传递键和值。

显示值–获取迭代器

迭代器 iterator = hashmap.entrySet()。迭代器()；

这里，值存在于集合中，所以我们使用 entrySet。

沿线:

While(iterator . has next()){

地图。Entry entry=(Map。entry)iterator . next()；

system . out . print(entry . getkey()+":")；

system . out . printin(entry . getvalue())；

}

有问题要问我们吗？在评论区提到它们，我们会给你回复。

**相关帖子:**

[JAVA/J2EE 简介&SOA](https://www.edureka.co/blog/videos/introduction-to-javaj2ee-soa/)

[JAVA/J2EE & SOA 课程](https://www.edureka.co/java-j2ee-soa-training)