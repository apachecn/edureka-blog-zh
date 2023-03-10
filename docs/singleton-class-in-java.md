# Java 中的单例类——如何使用单例类？

> 原文：<https://www.edureka.co/blog/singleton-class-in-java/>

在 Java 中，单例类是一个在给定时间只能有一个实例的类。它是 Java 中五种创造性设计模式之一，有助于轻松开发 [Java 程序](https://www.edureka.co/blog/java-programs/)。通过这篇文章，我将让您清楚地了解什么是 Java 中的 singleton 类，以及如何创建它。

下面是我将在本文中涉及的主题:

*   [什么是 Java 中的 Singleton 类？](#singletonclass)
*   [设计 Java 单例类的方法](#designingsingleton)
    1.  [急切的初始化方法](#eager)
    2.  [懒惰初始化方法](#lazy)
    3.  [线程安全单例方法](#threadsafe)
    4.  [用双锁方法进行懒惰初始化](#doublelock)
    5.  [懒载法](#lazyload)
    6.  [静态块初始化方法](#staticblock)

让我们开始吧。

## **什么是 Java 中的 Singleton 类？**

通俗地说，Java 中的单例类是指一次只允许通过一个实例访问它的类。这种设计模式用于限制不必要的类实例化，并确保每个 JVM 实例在任何时间点都只存在一个类的[对象。因此，在这种模式下，任何被定义为 Singleton 的类都只有一个实例 ，并且有一个全局访问点。与普通类不同，单例类不会在应用程序生命周期结束时被销毁。](https://www.edureka.co/blog/java-tutorial/#obj)

但是为什么我们首先需要一个单例类呢？

嗯，通过限制一个类的实例创建，它节省了内存空间，因为现在不会在每次发出新请求时都创建对象。相反，单个对象将被重复使用。这就是为什么 Java 中的单例模式主要用于多线程和数据库应用程序的原因。它基本上用于日志记录、缓存、线程池、配置设置和许多其他功能。

我希望你清楚 Java 中 Singleton 类的概念。所以，现在让我们继续阅读这篇 Java 文章中的 单例类，看看它们是如何创建的。

## **设计 Java 单例类的方法**

为了在 Java 中制作一个类单体，你需要以下三样东西:

1.  类的静态成员
2.  私有构造函数
3.  静态工厂方法

因为 Java 让开发人员探索他们的视野，所以有很多方法可以设计一个单例类。下面我列出了最受欢迎的。

1.  [急切的初始化方法](#eager)
2.  [懒惰初始化方法](#lazy)
3.  [线程安全单例方法](#threadsafe)
4.  [用双锁方法进行懒惰初始化](#doublelock)
5.  [懒载法](#lazyload)
6.  [静态块初始化方法](#staticblock)

现在，让我们逐一深入研究这些方法。

### **1。急切的初始化方法**

这是创建单例类的最简单的方法，其中实例是在类加载时创建的。要使用这种方法创建单例类，您需要遵循下面提到的步骤:

1.  将构造函数声明为私有的。
2.  下一步是为这个单体类创建一个私有类成员。
3.  现在，你需要定义一个工厂方法来返回你的类的对象，这个对象是我们创建的类成员的一个实例。
4.  如果你想直接访问这个静态实例，你甚至可以声明一个静态成员 public。

现在，让我们看看如何实现这些。

```
//Eager Initialization
public class EagerSingleton {
    private static final EagerSingleton INSTANCE = new EagerSingleton();
    private EagerSingleton() {}
  public static EagerSingleton getInstance() {
      return INSTANCE;
    }
}
```

如果你看到代码，你会发现每次我们实例化一个对象时，我们都在使用 getInstance() 方法，而不是调用类[构造函数](https://www.edureka.co/blog/constructor-in-java/)。 但它有自己的缺点。如果你使用这个方法使一个类成为单例类，那么不管应用程序是否使用它，实例都会被创建。

那么，让我们继续，看看用 Java 创建单例类的另一种方法。

### **2。惰性初始化方法**

这种方法被称为惰性初始化，因为它将类实例的创建推迟到第一次使用。我的意思是，用这种方法，一个对象只有在需要的时候才会被创建。它有助于避免不必要的创建[类实例](https://www.edureka.co/blog/java-tutorial/#obj)。要以这种方式设计一个单例类，您需要遵循下面列出的步骤:

1.  首先，将构造函数声明为私有。
2.  然后你需要为这个类创建一个私有的静态实例，但是还不需要实例化它。
3.  最后，创建一个工厂方法，首先检查实例成员是否为空。如果没有，那么它将为你创建一个 singleton 类的实例并返回它。

下面的代码显示了如何执行这个。

```
//Lazy Initialization
public class LazySingleton {
    private static LazySingleton INSTANCE = null;
    private LazySingleton() {}
    public static LazySingleton getInstance() {
        if (INSTANCE == null) {  
          synchronized(LazySingleton.class) {
        	  INSTANCE = new LazySingleton();
          }
        }
        return INSTANCE;
    }
}
```

### **3。线程安全单例** **方法**

但是上述方法在并发场景中会引起一些问题。由于单例模式主要用于多线程和 if 多线程同时进入 if 条件会引发问题。为了避免这种情况，我们试图通过同步全局访问方法来创建一个线程安全的单例类。这确保了在任何时间点都只有一个线程在执行该方法。参考下面的代码查看实现:

```
//Thread Safe Singleton
public class ThreadSafeSingleton {

    private static ThreadSafeSingleton INSTANCE;

    private ThreadSafeSingleton(){}

    public static synchronized ThreadSafeSingleton getInstance(){
        if(INSTANCE == null){
        	INSTANCE = new ThreadSafeSingleton();
        }
        return INSTANCE;
    }

}
```

但是有时这种方法也会变得非常麻烦，因为每次调用方法时，它都需要等待锁被释放，然后方法才能使用它。这导致进程变慢，并引导我们进入下一种方法，即带有双锁的 延迟初始化。

### **4。用双锁** **方法**进行惰性初始化

在这种方法中，我们不同步这些方法。相反，我们将对象创建代码封装在一个同步块中。 你可以说通过预先检查线程锁，它 减少了锁的获取次数。这种方法通常会提高应用程序的性能。查看下面的代码，看看它是如何完成的。

```
//Lazy Initialization with Double Lock
public class LazyDoubleLockSingleton {
    private static LazyDoubleLockSingleton INSTANCE = null;
    private LazyDoubleLockSingleton() {}
    public static LazyDoubleLockSingleton getInstance() {
        if (INSTANCE == null) {
            synchronized (LazyDoubleLockSingleton.class) {
                if (INSTANCE == null) {
                    INSTANCE = new LazyDoubleLockSingleton();
                }
            }
        }
        return INSTANCE;
    }
}
```

### **5。惰性加载方法**

这个方法基于 JSL(Java 语言规范),根据这个方法，JVM 将只在需要的时候加载静态数据成员。因此，当您的单例类加载到 JVM 中时，不会创建任何实例。此外，在程序执行期间，全局方法被按顺序调用。使用这种方法，您不必显式地同步静态 getInstance()来加载和初始化。静态类成员将以正确的顺序方式调用，全局方法的其余并发调用以相同的顺序返回，而不必执行同步开销。

下面是执行相同操作的代码。

```
//Lazy Load Method
public class LazyLoadSingleton {
    private LazyLoadSingleton() {}
    private static class SingletonClassHolder {
        static final Var INSTANCE = new LazyLoadSingleton();
    }
    public static LazyLoadSingleton getInstance() {
        return SingletonClassHolder.INSTANCE;
    }
}
```

### **6。静态块初始化方法**

这种在 Java 中创建单例类的方法是 类似于急切初始化法。唯一的区别是这个类的实例是在具有[异常处理](https://www.edureka.co/blog/java-exception-handling)功能的静态块中创建的。

```
//Static Block Initialization
public class StaticBlockSingleton {

    private static StaticBlockSingleton INSTANCE;

    private StaticBlockSingleton(){}

    //exception handling within static block
    static{
        try{
        	INSTANCE = new StaticBlockSingleton();
        } catch (Exception e) {
            throw new RuntimeException("Exception occured while creating a Singleton Class");
        }
    }

    public static StaticBlockSingleton getInstance(){
        return INSTANCE;
    }
}
```

这就把我们带到了这篇关于 Java 中单例类的文章的结尾。如果你想了解更多关于 Java 的知识，你可以参考我们的[其他 Java 博客](https://www.edureka.co/blog/what-is-java/)。

*既然您已经了解了什么是 Java 中的 Singleton 类，那么就来看看 Edureka 的* ***[Java 认证](https://www.edureka.co/java-j2ee-training-course)*** *培训* *吧，edu reka 是一家值得信赖的在线学习公司，拥有遍布全球的 250，000 多名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

*有问题吗？请在这篇“Java 中的 Singleton 类”文章的评论部分提到它，我们会尽快回复您。*