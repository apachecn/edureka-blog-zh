# 什么是 Java 中的外部化，什么时候使用？

> 原文：<https://www.edureka.co/blog/externalization-in-java/>

*[Java 序列化](https://www.edureka.co/blog/serialization-in-java/)* 效率不是很高。如果你序列化有很多属性和特性的臃肿的对象，你不希望序列化。这就是 Java 中外部化的用武之地。这篇文章将帮助你理解外部化的工作原理。

*   [Java 中的外化是什么？](#What_is_Externalization?)
*   [什么时候使用外部化？](#When_to_use_this_Externalization?)
*   [什么是外化接口？](#What_is_the_Externalization_interface?)
*   [外部化和序列化的区别](#Difference_between_Externalization_and_Serialization)

我们开始吧！

## **Java 中的外化是什么？**

每当需要定制 *[序列化](https://www.edureka.co/blog/serialization-in-java/)* 机制时，就会用到 Java 中的外部化。如果一个类实现了一个外部化接口，那么对象的序列化将使用方法 *writeExternal()* 来完成。当一个可外部化的对象在接收者端被重建时，一个实例将被使用无参数构造函数创建，这个方法被称为 *readExternal()。*

这基本上服务于自定义序列化的目的，您可以决定在流中存储什么。

## 什么时候使用外部化？

如果你只想序列化一个[对象](https://www.edureka.co/blog/java-object/)、的一部分，那么外部化是最好的选择。您将必须只序列化对象的必需字段。

## **什么是外化接口？**

如果你想在序列化和反序列化过程中控制对象的读写过程，你需要让对象的类实现接口 *java.io.Externalizable* 。只有这样，您才能实现自己的代码来读写对象的状态。方法 *readExternal()* 和 *writeExternal()* 由*可外部化*接口*定义。*

下面我们来详细了解一下这些方法。

接口的对象实现了这个方法，通过调用原始类型的 数据输入 的方法来帮助恢复其内容。它还为对象、字符串和数组调用 readObject 。现在让我们讨论如何实现这个 readExternal 方法。

当这个 *readExternal()* 方法取一个 [对象输入](https://www.edureka.co/blog/java-object/) 时，就可以用它的方法从这些规则的底层流中读取对象的状态:

*   对于原语类型，可以使用  DataInput 接口的readXXX()方法。分别是，read boolean()，  readByte() ，  readInt() ，  readLong()。
*   如果你有对象类型，比如字符串，数组，或者任何你定制的[类](https://www.edureka.co/blog/java-objects-and-classes/)，你可以使用*read object()*方法。

**举例:**

```
public void readExternal(ObjectInput in) throws ClassNotFoundException, IOException {
this.code = in.readInt();
this.name = (String) in.readObject();
this.password = (String) in.readObject();
this.birthday = (Date) in.readObject();
}
```

正如您在这里看到的，我已经反序列化了以下属性:代码、姓名、密码和生日。

### **【write external(对象输出输出)**

接口的对象实现此方法，以便通过调用原始值的 DataOutput 方法或调用对象、字符串和数组的 ObjectOutput 的 *writeObject* 方法来保存内容。现在，我们来看看实现过程。

由于这个 *writeExternal()* 方法采用了一个 ObjectOutput ，你可以使用它的方法将对象的状态写入底层流，遵循这些规则:

*   对于原语类型，使用 write XXX()data output接口的方法，如write boolean()，  writeByte() ，  writeInt() ，  writeLong() 等。
*   对于像[字符串](https://www.edureka.co/blog/java-string/)、[数组](https://www.edureka.co/blog/java-array/)、您的自定义类这样的对象类型，您可以使用writeObject()方法。

**举例:**

```
public void writeExternal(ObjectOutput out) throws IOException {
out.writeInt(code);
out.writeObject(name);
// write empty password:
out.writeObject("");
out.writeObject(birthday);
}
```

但是，在这里，你可以看到我序列化了以下属性:代码、姓名、密码和生日。

现在，转到这篇 Java 外部化文章的下一个主题，让我们讨论 Java 外部化和序列化之间的主要区别。

## **外化 vs 序列化:** **外化和序列化的区别**

这是最常被问到的 *[Java 面试问题](https://www.edureka.co/blog/interview-questions/java-interview-questions/)* 。

| 因素 | 客观化 | 序列化 |
| 过程 | 使用自定义序列化过程 | 使用默认序列化过程 |
| 用户界面设计（User Interface Design 的缩写） | 不需要 UID | 需要 serialVersionUID |
| 储存；储备 | 你必须存储有对象的数据 | 您可以直接存储对象 |
| 接近 | 外部化接口为应用程序提供了对序列化过程的完全控制。 | 没有这样的通道 |

我希望你们清楚外部化和序列化的区别。至此，我们结束了这篇关于“Java 中的外部化”的文章。我希望你们清楚与你们分享的话题。

希望上述内容被证明有助于增强你的*[Java](https://www.edureka.co/blog/what-is-java/)*知识。继续阅读，继续探索！

*还可以查看由 Edureka 提供的 [Java 认证培训](https://www.edureka.co/java-j2ee-training-course)，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在让您在 Java 编程方面有一个良好的开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架[如 Hibernate&Spring](https://www.edureka.co/blog/java-frameworks/)。*