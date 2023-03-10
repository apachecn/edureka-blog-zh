# Java 中的 Executor 框架是什么，如何使用？

> 原文：<https://www.edureka.co/blog/executor-framework/>

Java 一直对并发和 *[多线程](https://www.edureka.co/blog/java-thread/)* 编程有很强的支持。但是在开始的时候，直到 Java 5，这种支持是以在应用层调用本机结构的形式出现的。这是一个缺点，因为你不能更有效地处理原语调用。因此，这篇关于 Java Executor 框架的文章提出了这个问题的解决方案。

*   [什么是遗嘱执行人框架？为什么要用？](#What_is_the_Executor_Framework?_Why_use_it?)
*   [遗嘱执行人的类型](#Types_of_Executors)
    *   [单线程执行程序](#SingleThreadExecutor)
    *   [FixedThreadPool](#FixedThreadPool)
    *   [缓存线程池](#CachedThreadPool)
    *   [调度执行程序](#ScheduledExecutor)
*   [最佳实践](#Best_practices)

我们开始吧！

## **什么是遗嘱执行人框架？为什么要用？**

*Executor 框架*包含一堆用于有效管理多线程的组件。它是与 JDK 5 一起发布的，该版本用于运行可运行对象，而无需每次都创建新线程，并且大多数情况下还会重用已创建的线程。

这个执行器 API 在*执行器*的帮助下，将任务的执行与实际要执行的任务解耦。这是以为中心的 Executor 接口及其子接口***ExecutorService***和类***ThreadPoolExecutor。***

通过使用这个执行器，只有一个人必须实现可运行的对象，并将它们发送给执行器执行。

让我们看一个例子。

**举例:**

```
 public class Test implements Runnable
{
private String message;
public Test(String message)
{
this.message = message;
}
@Override public String run() throws Exception
{
return "Hello " + message + "!";
}
} 
```

在这个例子中，Test 类实现了 Runnable，并被参数化为 type [string](https://www.edureka.co/blog/java-string/) 。它也被声明为抛出异常。另外，请注意，t 他能够向执行程序抛出一个异常，然后执行程序将这个异常返回给运行程序，这一点非常重要，因为这有助于运行程序了解任务执行的状态。

让我们前进到本文的下一部分，看看 *[Java](https://www.edureka.co/blog/what-is-java/)* 中不同类型的执行器框架。

## **遗嘱执行人的类型**

主要有 4 种类型的遗嘱执行人可用。它们是:

*   单线线程执行程序
*   固定线程池
*   缓存线程池
*   预定的执行者

**单线程执行程序**

这个执行器只有一个线程，用于按顺序执行任务。如果任何线程在执行任务时由于异常而死亡，则会创建一个新线程来取代旧线程，并且后续任务会在新线程中执行。

**固定池执行人员**

这是一个固定数量的线程池。提交给执行器的任务由“n”个线程执行，假设有更多的任务要完成，它们被存储在一个 *LinkedBlockingQueue* 中。

**cache read executor**

这主要用于当生产线上有许多短期并行任务等待执行时。与固定线程池相比，这里，这个执行程序池的线程数量是不受限制的。如果所有的线程都忙于执行分配的任务，并且当有一个新任务时，它将创建并添加一个新线程到执行器。如果一个 thre ad 保持空闲接近 60 秒，它们将被终止并从缓存中删除。

**调度执行程序**

当您有一个需要定期运行的任务或者如果您希望延迟某个任务时，可以使用这个执行器。任务可以在 *ScheduledExecutor* 中使用两种方法 *scheduleAtFixedRate* 或 *scheduleWithFixedDelay* 进行调度。

谈到应该遵循的最佳实践，这里有一些。

## **最佳实践**

1.  总是对照静态分析工具运行 Java 代码，比如【PMD】和  FindBugs。
2.  务必注意交叉检查并计划更好的代码来检查顶部列表，以便在执行期间检测代码中可能出现的  *[死锁](https://www.edureka.co/blog/deadlock-in-java/)* 或活锁  。
3.  在多线程程序中，要养成随时随地捕捉错误的习惯，而不仅仅是异常。

至此，我们结束这篇关于“Java 中的 Executor 框架”的博客。我希望你们清楚这篇文章教给你们的东西。我们将继续一起挖掘 Java 世界。敬请期待！

*查看 Edureka 提供的 [**Java 培训**](https://www.edureka.co/java-j2ee-training-course)* *，edu reka 是一家值得信赖的在线学习公司，在全球拥有超过 25 万名满意的学习者。Edureka 的 Java J2EE 和 SOA 培训和认证课程是为想成为 Java 开发人员的学生和专业人士设计的。该课程旨在为您提供 Java 编程的良好开端，并训练您掌握核心和高级 Java 概念以及各种 Java 框架，如 Hibernate & Spring。*

*有问题吗？请在“Java 中的 Executor 框架”博客的评论部分提到它，我们会尽快回复您。*