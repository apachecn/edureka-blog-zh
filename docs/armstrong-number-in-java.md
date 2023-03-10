# 如何检验一个给定的数是不是阿姆斯特朗数？

> 原文：<https://www.edureka.co/blog/armstrong-number-in-java/>

在数论中，一个自恋的数，阿姆斯特朗数是以迈克尔·f·阿姆斯特朗的名字命名的，阿姆斯特朗是一个它自己的数字的和的数字，每个数字的幂。在这篇 [Java](https://www.edureka.co/blog/java-tutorial/) 中的阿姆斯特朗数文章中，让我们来学习如何检验一个给定的数是否是阿姆斯特朗数。

本文讨论的主题是:

*   什么是阿姆斯特朗号码？
*   [Java 程序检查阿姆斯特朗号](#JavaprogramtocheckanArmstrongnumber)
    *   [使用 For 循环](#forloop)
    *   [使用 While 循环](#whileloop)

让我们开始吧！

## 什么是阿姆斯特朗号码？

各个数字的幂之和等于数字本身。在 1 到 1000 之间，有五个阿姆斯特朗数。分别是:- 1，153，370，371，407。这是一般的方程式。

```
abcd... = an + bn + cn + dn + ...

```

让我们用一些例子来检验这个概念。 **例 1: 370**

3*3*3 + 7*7*7 + 0*0*0 = 27 + 343 + 0 = 370

**例 2:407**4 * 4 * 4+0 * 0 * 0+7 * 7 * 7 = 64+0+343 = 407

我希望你现在清楚这个概念了。接下来，让我们看看如何在 Java 中用检查一个给定的数是否是阿姆斯特朗数。

## **Java 程序检查阿姆斯特朗号**

在 Java 中有两种方法可以检查一个给定的数是否是阿姆斯特朗数:

1.  使用“while”循环
2.  Java“for”循环

### **使用*‘while’*循环**

在阿姆斯壮数为 3 位数的情况下，每个位数的立方之和等于该数本身。下面的示例程序检查一个给定的 3 位数是否是阿姆斯特朗数。

```
package MyPackage;

	public class ArmstrongNumber{
	    public static void main(String[] args) {
	        int num = 371, originalNum, remainder, result = 0;
	        originalNum = num;
	        while (originalNum != 0)
	        {
	            remainder = originalNum % 10;
	            result += Math.pow(remainder, 3);
	            originalNum /= 10;
	        }	
	        if(result == num)
	            System.out.println(num + " is an Armstrong number.");
	        else
	            System.out.println(num + " is not an Armstrong number.");
	    }
	}

```

**输出** : 371 是一个阿姆斯特朗数。

代码中列出的步骤有:

*   while 循环中的第一行从指定的数字中提取最后一位数字*(余数)*
*   第二行计算上一步得到的最后一位数字的立方，并将其添加到*结果*
*   然后，在除以 10 之后，最后一个数字从原始数字中删除

### **使用‘for*’*循环**

```
package MyPackage;

public class Armstrong {
    public static void main(String[] args) {
        int number = 9474, originalNumber, remainder, result = 0, n = 0;
        originalNumber = number;
        for (;originalNumber != 0; originalNumber /= 10)
        {
        	n++;
        }
        originalNumber = number;
        for (;originalNumber != 0; originalNumber /= 10)
        {
            remainder = originalNumber % 10;
            result += Math.pow(remainder, n);
        }
        if(result == number)
            System.out.println(number + " is an Armstrong number.");
        else
            System.out.println(number + " is not an Armstrong number.");
    }
}
```

**输出:**

```
9474 is an Armstrong number.

```

这里，我们有两个 for 循环。第一个计算给定数字的位数。第二个循环检查给定的数是否是阿姆斯特朗数。

至此，我们已经接近了本文的结尾。我希望上面解释的内容对您的 Java 知识有所帮助。继续阅读，继续探索！

*查看 Edureka 提供的  [**Java 认证课程**](https://www.edureka.co/java-j2ee-training-course) ，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。我们在这里帮助你的旅程中的每一步，为了成为一个除了这个 java 面试问题，我们提出了一个课程，这是为学生和专业人士谁想要成为一个 Java 开发人员设计的。*

有问题要问我们吗？请在“Java 中的阿姆斯特朗数”博客的评论部分提到它，我们会尽快回复您。