# Java Enum 教程:什么是 Enum，如何实现？

> 原文：<https://www.edureka.co/blog/java-enum-tutorial/>

在 [Java](https://www.edureka.co/java-j2ee-training-course) 中的**枚举是一种使用关键字 **enum 定义类的方法，该类具有固定的和命名的常数以及它们各自的 [**数据类型**](https://www.edureka.co/blog/data-types-in-java/) 。**在这篇“ *Java 枚举教程*”文章中，我们将通过 示例来学习定义枚举，以便更好地理解。**

*   [什么是枚举？](#what)
*   [为什么我们需要枚举？](#why)
*   [枚举和类之间的差异](#diff)
*   [列举实例](#prac)
*   [Enum 的优点](#impt)
*   [枚举用例:石头，](#use) [剪刀布游戏](#use)

## **什么是枚举？**

**Java 枚举**是具有一组固定的常量或变量的类，这些常量或变量不会改变。Java 中的枚举是使用关键字 **enum 实现的。**Java**enum**常量是**静态**和 **final** 隐式。自 **JDK 版本 1.5 起，Enum 功能可用。**

## **为什么我们需要枚举？**

通过避免样板代码，枚举 提高了编译时检查的类型安全性，以避免运行时的错误。例如，如果您必须从最少的可用选项中选择一种可能性，比如说

**工作** **类型:**(合同 **/** 临时 **/** 永久)

![Java enum tutorial employee](img/4d87835cdda36303203074f9ba4e7aa5.png)

那么最好的选择是使用一个**枚举。**是因为**枚举** 可以方便地用在开关中。 **枚举** 可以遍历。 **枚举** 可以 **有** 字段、构造函数和方法。因此，它增加了编译时检查并避免了由于传入无效常数而导致的错误，因为您已经记录了哪些值是合法使用的。

## **枚举和类之间的差异**

虽然类和枚举在 Java 环境中有相似的功能，但它们在一些方面有所不同。让我们讨论一下不同之处

| **枚举** | **类** |
| 不能重写枚举常量 | 类常量可以被覆盖 |
| 枚举不支持创建对象 | 类支持对象的创建 |
| 枚举不能扩展其他类 | 一个类可以扩展其他类 |
| 枚举 c 一个实现接口 | 一个类可以实现接口 |

## **列举实例**

现在，为了更好地理解 enum，让我们基于下面的内容执行一些实际的例子。

*   [在 Java 中定义枚举](#define)
*   [开关情况下使用的枚举](#switch)
*   [继承使用枚举](#inherit)
*   [枚举自定义值](#custom)
*   [if-else-if 语句中的枚举](#ifelse)
*   [枚举使用的不同方法](#differ)
    1.  [值()](#value)
    2.  [valuesof()](#valuesof)
    3.  [依次](#ord) [()](#ord)

**在 Java 中定义枚举**

枚举可以在类内声明，也可以在类外声明。但是，它不能在任何方法中声明。让我们举一个小例子来理解它的语法、定义和声明。

**语法:**

```
enum name{constants;}
```

在这个例子中，我们在枚举中声明了 **main()** 方法

```
package definition;

public class Edureka {
     enum Level {
           BAJA, KTM, YAMAHA
     }
     public static void main(String[] args) {
           Level myVar = Level.KTM;
           System.out.println(myVar);
     }
}

```

**//输出**

`KTM`

在这个例子中， **main()** 方法在枚举的之外被声明为**。**

```
package definition;

enum Color{
      BAJAJ, KTM, YAMAHA;
}
public class Edureka{
      public static void main(String[] args){
              Bike b1 = Color.YAMAHA;
              System.out.println(b1);
      }
}

```

**//输出:**

`YAMAHA`

**开关情况下使用的枚举**

枚举也可以用在 switch 语句中。重要的是，所有 case 语句必须使用 switch 语句使用的相同枚举中的常量。让我们来看一个基于此的例子。

这里，我们将声明一个 enum，它的元素是星期几，我们将以字符串的形式传递数据，以打印匹配事例的数据。

```
package switched;

enum Day{
      SUNDAY, MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY;
}
public class Edureka{
      Day day;
      public Edureka(Day day){
            this.day = day;
      }
      public void dayIsLike(){
            switch (day){
                   case MONDAY: System.out.println("Hi, Today is Monday");
                                               break;
                   case TUESDAY: System.out.println("Hi, Today is Tuesday");
                                               break;
                   case WEDNESDAY: System.out.println("Hi, Today is Wednesday");
                                               break;
                   case THURSDAY: System.out.println("Hi, Today is Thursday");
                                               break;
                   case FRIDAY: System.out.println("Hello, Today is Friday.");
                                               break;
                   case SATURDAY: System.out.println("Hi, Today is your Weekend");
                                               break;
                   case SUNDAY: System.out.println("Hi, Today is a Holiday");
                                               break;
                   default: System.out.println("Please enter a valid day.");
                                               break;
             }
      }
      public static void main(String[] args){
            String str = "MONDAY";
            Edureka e1 = new Edureka(Day.valueOf(str));
            e1.dayIsLike();
      }
}

```

**//输出:**

`Hi, Today is Monday`

**使用枚举继承**

基本上，任何**枚举**都被表示为一个扩展抽象类 java.lang. **枚举**的类，并且有几个静态成员。因此，**枚举**不能扩展任何其他类，或者**枚举**没有多重**继承**。让我们执行一个例子来更好地理解它。

在这里，我们将继承基于手机制造商的操作系统。

```
package inheritance;

import java.util.ArrayList;
import java.util.List;

public class Edureka {
       public static void main(String[] args) {
              List<HTTPMethodConvertible> inherit = new ArrayList<>();
              inherit.add(LibraryEnum.FIRST);
              inherit.add(ClientEnum.google);
              for (HTTPMethodConvertible element : inherit) {
                     System.out.println(element.getHTTPMethodType());
              }
       }
       static interface HTTPMethodConvertible {
              public String getHTTPMethodType();
       }
       static enum LibraryEnum implements HTTPMethodConvertible {
              FIRST("Google Pixel"), SECOND("Huawei"), THIRD("Apple 11 Pro");
              String httpMethodType;
              LibraryEnum(String phone) {
                    httpMethodType = phone;
              }
              public String getHTTPMethodType() {
                    return httpMethodType;
              }
       }
       static enum ClientEnum implements HTTPMethodConvertible {
             huawei("HongMing OS"), apple("iOS"), google("Android One");
             String httpMethodType;
             ClientEnum(String s) {
                   httpMethodType = s;
             }
             public String getHTTPMethodType() {
                   return httpMethodType;
             }
       }
}

```

**//输出:**

`Google Pixel`

**具有自定义值的枚举**

默认情况下，枚举有自己的字符串值，我们也可以给枚举分配一些自定义值。让我们考虑下面的例子。

```
enum  Traffic
{
    RED(“STOP”), ORANGE(“WAIT”), GREEN(“GO”);
}
```

在上面的例子中，我们可以看到流量枚举有三个成员。即，

*红色、橙色*和*绿色*分别具有各自不同的自定义值*停止、等待*和*前进*。

现在，要在代码中使用相同类型的枚举，我们需要遵循以下几点:

*   我们需要为这个枚举类创建**参数化构造函数**。因为我们知道**枚举**类的对象不能显式创建，所以我们使用参数化构造函数来初始化。
*   **构造函数**不能是公共的或受保护的，它必须有**私有的**或**默认的**修饰符。如果我们创建 public 或 protected，它将允许初始化多个完全违反 **enum 功能的对象。**
*   我们必须创建一个 getter 方法来获取**枚举的值。**

让我们基于此执行一个程序。

```

package traffic;

enum TrafficSignal {
      RED("STOP"), GREEN("GO"), ORANGE("WAIT");
      private String action;
      public String getAction() {
             return this.action;
      }
      private TrafficSignal(String action) {
             this.action = action;
      }
}
public class Edureka {
      public static void main(String args[]) {
              TrafficSignal[] signals = TrafficSignal.values();
              for (TrafficSignal signal : signals) {
                      System.out.println("name : " + signal.name() + " action: " + signal.getAction());
              }
       }
}

```

**//输出:**

`name: RED action: STOP``name: GREEN action: GO`

**if-else-if 语句中的枚举**

现在，让我们执行一个基于 if-else-if 语句中的**枚举的程序。**这里，我们将通过传递 enum 中可用的方向值来找到遍历的方向。

```
package Directions;

enum Directions {
      EAST, WEST, NORTH, SOUTH
}
public class Edureka {
      public static void main(String args[]) {
            Directions dir = Directions.NORTH;
            if (dir == Directions.EAST) {
                   System.out.println("Direction: East");
            }
            else if (dir == Directions.WEST) {
                   System.out.println("Direction: West");
            } 
            else if (dir == Directions.NORTH) {
                   System.out.println("Direction: North");
            } 
            else {
                   System.out.println("Direction: South");
            }
      }
}

```

**//输出:**

`Direction: North`

**不同的方法与 enum** 一起使用

**Values():** 当你创建一个 enum 时，**[Java 编译器](https://www.edureka.co/blog/just-in-time-compiler/)** 内部增加了***Values()***方法。该方法返回一个 **[数组](https://www.edureka.co/blog/java-array/)** 包含 enum 的所有值。

**//语法:**

```
public static enum-type[ ] values()
```

我们将找出数组中特定元素的索引值。

```
package values;

enum Color {
      RED, GREEN, BLUE;
}

public class Edureka {
      public static void main(String[] args) {
           Color arr[] = Color.values();
           for (Color col : arr) {
                  System.out.println(col + " at index " + col.ordinal());
           }
           System.out.println(Color.valueOf("RED"));
      }
}

```

//输出:

`RED at index 0` `GREEN at index 1` `BLUE at index 2`

**ValueOf():** 此 方法用于返回枚举常数，其值等于调用此方法时作为参数传递的 **[字符串](https://www.edureka.co/blog/cheatsheets/java-string-cheat-sheet/)** 。

**//语法:**

```
public static enum-type valueOf (String str)
```

在这里，我们将根据传递给字符串的输入来查找特定手机的成本。

```
package valuesof;

enum Mobile {
       Samsung(1099), Apple(1250), Google(1325);
       int price;
       Mobile(int p) {
             price = p;
       }
       int showPrice() {
             return price;
       }
}
public class Edureka {
       public static void main(String args[]) {
             System.out.println("CellPhone List:");
             for (Mobile m : Mobile.values()) {
                   System.out.println(m + " costs " + m.showPrice() + " dollars");
             }
             Mobile ret;
             ret = Mobile.valueOf("Samsung");
             System.out.println("Selected : " + ret);
       }
}

```

**//输出:**

`Samsung costs 1099 dollars` `Apple costs 1250 dollars` `Google costs 1325 dollars`

**Ordinal():**Java 解释器在创建**枚举时，在内部添加了 **ordinal()** 方法。**ordinal()方法返回枚举值的**索引**。

**//语法:**

```
public final int ordinal()
```

这里，我们将找出数组中特定元素的索引值。还有樱桃果实的位置。

```
Package ordinal;

enum Fruits {
      Apple, Banana, Cherry, Date, Elderberry
}

enum Vegetables {
      Carrot, Beetroot, Beans, Tomato, Onion
}

public class Edureka {
      public static void main(String[] args) {
            Fruits[] fru = Fruits.values();
            for(Fruits fr : fru){
                    System.out.println(fr+" : "+fr.ordinal());
            }
            Fruits f1,f2,f3;
            f1  = Fruits.Apple;
            f2 = Fruits.Cherry;
            f3 = Fruits.Apple;
            if(f2.compareTo(f1) > 0){
                  System.out.println(f2+" comes after "+f1);
            }
            Vegetables v1 = Vegetables.Beetroot;
            if(f1.equals(v1)){
                  System.out.println("Incorrect");
            }
      }
}

```

//输出:

`Apple : 0``Banana : 1``Cherry : 2``Date : 3``Elderberry : 4`

## **Enum 的优点**

*   Java 中的枚举提高了**类型安全性**
*   Enum 设计为在**开关情况下**易于使用
*   枚举可以被**遍历**
*   枚举可以有**字段、方法、**和**构造函数**
*   Enum 可以实现**接口**
*   枚举不能扩展一个**类**，因为在内部，它扩展了**枚举**类

## **枚举用例:石头、剪子、布游戏**

![Java enum tutorial usecase2](img/3473507704b57b290e7a9ccc324a7809.png)

我们将使用 Java 中的 **enum** 来创建我们童年的游戏**石头剪刀布**。下面的代码解释了如何操作。

```
package Edureka;
import java.util.Random;
import java.util.Scanner;

enum HandSign {
       SCISSOR, PAPER, STONE
}

public class SPS {
      public static void main(String[] args) {
            Random random = new Random();
            boolean gameOver = false;
            HandSign playerMove = HandSign.SCISSOR;
            HandSign computerMove;
            int numTrials = 0;
            int numComputerWon = 0;
            int numPlayerWon = 0;
            int numTie = 0;
            Scanner in = new Scanner(System.in);
            System.out.println("nLet us begin...n");
            while (!gameOver) {
                   System.out.printf("%nScissor-Paper-Stonen");
                   boolean validInput;
                   do {
                        System.out.print("nYour turn (Please Enter s for a scissor, p for paper, t for stone, q to quit): n");
                        char inChar = in.next().toLowerCase().charAt(0);
                        validInput = true;
                        if (inChar == 'q') {
                               gameOver = true;
                        }
                        else if (inChar == 's') {
                               playerMove = HandSign.SCISSOR;
                        }
                        else if (inChar == 'p') {
                               playerMove = HandSign.PAPER;
                        }
                        else if (inChar == 't') {
                               playerMove = HandSign.STONE;
                        }
                        else{
                               System.out.println("nPlease check the input and try again!n");
                               validInput = false;
                        }
                   } while (!validInput);
                   if (!gameOver) {
                         int aRandomNumber = random.nextInt(3);
                         if (aRandomNumber == 0) {
                              computerMove = HandSign.SCISSOR;
                              System.out.println("nIt's My turn: SCISSORn");
                         } 
                         else if (aRandomNumber == 0) {
                              computerMove = HandSign.PAPER;
                              System.out.println("nIt's My turn: PAPERn");
                         } 
                         else {
                              computerMove = HandSign.STONE;
                              System.out.println("nIt's My turn: STONEn");
                          }
                         if (computerMove == playerMove) {
                              System.out.println("nIt's a Tie!n");
                              ++numTie;
                         } 
                         else if (computerMove == HandSign.SCISSOR &amp;&amp; playerMove == HandSign.PAPER) {
                              System.out.println("nScissor cuts paper, I won!n");
                              ++numComputerWon;
                         } 
                         else if (computerMove == HandSign.PAPER &amp;&amp; playerMove == HandSign.STONE) {
                              System.out.println("nPaper wraps stone, I won!n");
                              ++numComputerWon;
                         } 
                         else if (computerMove == HandSign.STONE &amp;&amp; playerMove == HandSign.SCISSOR) {
                               System.out.println("nStone breaks scissor, I won!n");
                              ++numComputerWon;
                         } 
                         else {
                              System.out.println("nCongratulations...! You won!n");
                              ++numPlayerWon;
                         }
                          ++numTrials;
                   }
            }
            System.out.printf("%nThe number of trials: " + numTrials);
            System.out.printf("I won %d(%.2f%%). You won %d(%.2f%%).%n", numComputerWon, 100.0 * numComputerWon / numTrials, numPlayerWon, 100.0 * numPlayerWon / numTrials);
            System.out.println("Bye!, Hope you enjoyed..!");
      }
}

```

**//输出:**

`Let us begin...``Scissor-Paper-Stone``Your turn (Please Enter s for a scissor, p for paper, t for stone, q to quit):``s``It's My turn: STONE``Stone breaks scissor, I won!``Scissor-Paper-Stone``Your turn (Please Enter s for a scissor, p for paper, t for stone, q to quit):``The number of trials: 1I won 1(100.00%). You won 0(0.00%).``Bye!, Hope you enjoyed..!`

至此，我们结束了 Java Enum 教程。希望你已经通过一些实时例子理解了 Java 中的 Enum 及其实现。

*现在您已经通过本“Java Enum 教程”了解了 **enum** 的基础知识，请查看 Edureka 的  [**Java 培训**](https://www.edureka.co/java-j2ee-training-course)* *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 250，000 名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在让您在 Java 编程方面有一个良好的开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate&[Spring](https://spring.io/projects/spring-framework)。*

有问题要问我们吗？在这个“Java Enum 教程”博客的评论部分提到它，我们会尽快回复您。