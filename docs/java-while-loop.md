# Java 中什么是 While 循环，如何使用？

> 原文：<https://www.edureka.co/blog/java-while-loop/>

Java 语言提供了几个循环。[循环](https://www.edureka.co/blog/java-tutorial/#control)基本上是用来重复执行一组语句，直到满足特定条件。在这里，我将告诉你 Java 中的‘while’循环。本文包含的主题如下:

*   [Java 中的 while 循环是什么？](#WhileloopinJava)
    *   [while 循环的语法](#Syntaxofwhileloop)
    *   [实际演示](#Example)
*   [什么是无限 while 循环？](#Infinitewhileloop)
    *   [无限 while 循环的语法](#Syntaxofinfinitewhileloop)
    *   [实际演示](#Example)

我们开始吧！

## **Java 中的 while 循环是什么？**

Java while 循环用于反复迭代程序的一部分。如果迭代次数不固定，那么可以使用 while 循环。

while 循环如何工作的图示:

![While Loop in Java - Edureka](img/37267bce82ac68b90b8a6261a59d4b6a.png)在上图中，当执行开始且条件返回 false 时，则[控制](https://www.edureka.co/blog/java-tutorial/#control)跳转到 while 循环后的下一条语句。另一方面，如果条件返回 true，则执行 while 循环中的语句。

继续这篇关于 [Java](https://www.edureka.co/blog/java-tutorial/) 中 While 循环的文章，让我们来看看语法:

### **语法:**

```
while (condition) {

  // code block to be executed

}
```

现在我已经向您展示了语法，下面是一个示例:

### **实际实施:**

```
class Example {
    public static void main(String args[]){
         int i=10;
         while(i>1){
              System.out.println(i);
              i--;
         }
    }
}

```

## **输出**:

1098765432

接下来，我们来看另一个例子:

### **Java 中 While 循环的另一个例子:**

```
// Java While Loop example

package Loops;

import java.util.Scanner;

public class WhileLoop {
	private static Scanner sc;

	public static void main(String[] args) {
		int number, sum = 0;
		sc = new Scanner(System.in);	

		System.out.println("n Please Enter any integer Value below 10: ");
		number = sc.nextInt();

		while (number <= 10)  {
			sum = sum + number;
			number++;
		}
		System.out.format(" Sum of the Numbers From the While  Loop is: %d ", sum);
	}
}

```

**输出**:

请输入 10: 7 以下的任意整数值。While 循环中的数字之和为:34

与前面的例子相比，上面的例子有点复杂。让我一步一步来解释。

在这个 Java while 循环示例中，机器会要求用户输入任何小于 10 的整数值。接下来，While 循环和 While 循环中的条件将确保给定的数字小于或等于 10。

现在，用户输入值= 7，我已经初始化了 sum = 0

这就是迭代的工作方式:(关注代码中编写的 while 循环)

**第一次迭代:**

sum = sum+numbersum = 0+7 = =>7 现在，数字将递增 1 (number ++)

**第二次迭代**

现在，在第一次迭代中，Number 和 sum 的值都改变为:Number = 8 和 sum = 7sum = sum+Numbersum = 7+8 = =>15 同样，Number 将增加 1 (number ++)

**第三次迭代**

现在，在第二次迭代中，Number 和 sum 的值都已更改为:Number = 9 和 sum = 15sum = sum+Numbersum = 15+9 = =>24 遵循相同的模式，Number 将再次递增 1 (number ++)。

**第四次迭代**

在 Java while 循环的第三次迭代中，Number 和 sum 的值都更改为:Number = 10 和 sum = 24sum = sum+Numbersum = 24+10 = =>34

最后，数字将最后一次递增 1 (number ++)。

这里，数字= 11。因此，while 循环中的条件失败。

最后 System.out.format 语句会打印出上面看到的输出！

再往前走，

您需要记住的一点是，您应该在 while 循环中使用 increment 或 decrement 语句，以便循环变量在每次迭代中都发生变化，从而在某个时刻，条件返回 false。这样就可以结束 while 循环的执行。否则，循环将无限期执行。在这种情况下，循环无限执行，您将在 [Java](https://www.edureka.co/blog/what-is-java/) 中遇到无限 while 循环的概念，这是我们下一个讨论的主题！

## **Java 中的无限 while 循环**

当您在 while 循环中传递' true '时，将启动无限 while 循环。

**语法**:

```
while (true){
    statement(s);
}

```

## **实际演示**

让我给你看一个 Java 中无限 While 循环的例子:

```
class Example {
    public static void main(String args[]){
         int i=10;
         while(i>1)
         {
             System.out.println(i);
              i++;
         }
    }
}

```

这是一个无限的 while 循环，因此不会结束。这是因为代码中的条件表示 i>1，这将始终为真，因为我们在 while 循环中增加了 I 的值。

至此，我已经接近了这篇博客的结尾。我真的希望上面分享的内容能对你的 Java 知识有所帮助。让我们一起继续探索 Java 世界。敬请期待！

*查看 Edureka 提供的* [***Java 在线培训***](https://www.edureka.co/java-j2ee-training-course) *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

有问题要问我们吗？请在这篇“Java 中的 While 循环”博客的评论部分提到它，我们会尽快回复您。