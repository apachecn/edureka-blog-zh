# C 程序设计中的先来先服务调度

> 原文：<https://www.edureka.co/blog/first-come-first-serve-scheduling/>

先来先服务是 CPU 用来调度作业的调度算法。这是一种非抢占式算法。优先级是根据处理器对它们的请求而给出的。让我们按照以下顺序来理解这个概念:

*   [先来先服务计划中的条款](#terms)
*   [示例代码](#code)
*   [FCFS 调度说明](#explanation)

![First Come First Serve Scheduling](img/a93399754d59b6b108c05a69158b5275.png) 先请求 CPU 服务的进程，先得到 CPU。这是先来先服务算法使用的哲学。

## **先到先得的条款**

*   完成时间:执行完成的时间。
*   周转时间:突发时间和等待时间之和就是周转时间
*   等待时间:进程需要等待它获得 CPU 并开始执行的时间称为等待时间。

#### **要点**

*   它是不可抢占的
*   平均等待时间不是最佳的
*   无法并行利用资源

## **示例代码**

```
#include<stdio.h>

 int main()

{
    int n,bt[20],wt[20],tat[20],avwt=0,avtat=0,i,j;
    printf("Enter total number of processes(maximum 20):");
    scanf("%d",&n);

    printf("nEnter Process Burst Timen");
    for(i=0;i<n;i++)
    {
        printf("P[%d]:",i+1);
        scanf("%d",&bt[i]);
    }

    wt[0]=0;   

    for(i=1;i<n;i++)
    {
        wt[i]=0;
        for(j=0;j<i;j++)
            wt[i]+=bt[j];
    }

    printf("nProcessttBurst TimetWaiting TimetTurnaround Time");

    for(i=0;i<n;i++)
    {
        tat[i]=bt[i]+wt[i];
        avwt+=wt[i];
        avtat+=tat[i];
        printf("nP[%d]tt%dtt%dtt%d",i+1,bt[i],wt[i],tat[i]);
    }

    avwt/=i;
    avtat/=i;
    printf("nnAverage Waiting Time:%d",avwt);
    printf("nAverage Turnaround Time:%d",avtat);

    return 0;
}

```

###### O**输出:**

#### **![](img/589b5b0e83b459933bac802559c7f37a.png)**

#### **解释**

在上面的代码中，展示了先来先服务调度算法。要求用户输入进程的数量。在输入进程数量时，我们必须输入每个进程的突发时间。

首先计算等待时间。首先，第一个流程的等待时间为零。

```
for(i=1;i<n;i++)
  {
      wt[i]=0;
      for(j=0;j<i;j++)
          wt[i]+=bt[j];
  }
```

等待时间的计算是通过加上前一过程的突发时间来完成的。假设前一个进程的突发时间为 10，那么秒的等待时间将为 10。类似地，对于第三个进程，等待时间将是第一个和第二个进程的突发时间之和。

```
for(i=0;i<n;i++)
    {
        tat[i]=bt[i]+wt[i];
        avwt+=wt[i];
        avtat+=tat[i];
        printf("nP[%d]tt%dtt%dtt%d",i+1,bt[i],wt[i],tat[i]);
    }
```

下一部分我们计算周转时间。每个流程的周转时间通过将突发时间和等待时间相加来计算。

最后，计算平均周转时间和平均等待时间。

```
avwt/=i;
avtat/=i;
```

I 给出了进程的总数。我们将所有等待时间的总和除以周转时间，得到平均值。这就是先来先服务算法的工作原理。

至此，我们结束了 C 编程中的先来先服务调度。

我希望这能给你带来信息和帮助，请继续关注更多类似主题的教程。您也可以查看我们的培训项目 t 以获得关于 jQuery 及其各种应用程序的深入知识，您可以 [**在此**](https://www.edureka.co/masters-program/full-stack-developer-training) 注册参加实时在线培训，享受全天候支持和终身访问。 用不同的字符串和修改实现上面的代码。现在，我们已经很好地理解了与指针相关的所有关键概念。

有问题要问我们吗？在这个博客的评论部分提到他们，我们会回复你。