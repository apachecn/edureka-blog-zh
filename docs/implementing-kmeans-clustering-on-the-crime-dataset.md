# 在犯罪数据集上实现 K-means 聚类

> 原文：<https://www.edureka.co/blog/implementing-kmeans-clustering-on-the-crime-dataset/>

在这篇博客中，您将了解什么是 K-means 聚类，以及它如何在美国各州收集的犯罪数据上实现。这些数据包含了 1973 年美国 50 个州每 10 万居民中的袭击、谋杀和强奸犯罪。除了分析数据，您还将了解:

*   了解 k-means 算法的机理。

让我们从分析开始。数据看起来像:

[![dataset](img/d825784d1dc6fb65971c33645d7ede03.png "data")](https://edureka.wistia.com/medias/eea6j441fs/download?media_file_id=76016491)

Click on the image to download this dataset



***需要这个数据集？点击上面的图片下载。***

首先让我们为分析准备数据。为此，我们应该删除数据中可能存在的任何 NA 值，并将数据转换为矩阵。

```
> crime0 <- na.omit(USArrests)
> crime <- data.matrix (crime0)
> str(crime)
 num [1:50, 1:4] 13.2 10 8.1 8.8 9 7.9 3.3 5.9 15.4 17.4 ...
 - attr(*, "dimnames")=List of 2
 ..$ : chr [1:50] "Alabama" "Alaska" "Arizona" "Arkansas" ...
 ..$ : chr [1:4] "Murder" "Assault" "UrbanPop" "Rape"
```

让我们假设集群的数量为 5。Kmeans()函数接受输入数据和数据将被聚类的聚类数。语法是:kmeans( data，k)其中 k 是聚类中心的数量。

```
> cl <- kmeans(crime, 5)
> class(cl)
[1] "kmeans"
```

分析聚类:

```
> str(cl)
List of 9
 $ cluster : Named int [1:50] 5 3 3 5 3 5 4 5 3 5 ...
 ..- attr(*, "names")= chr [1:50] "Alabama" "Alaska" "Arizona" "Arkansas" ...
 $ centers : num [1:5, 1:4] 2.95 6.11 12.14 5.59 11.3 ...
 ..- attr(*, "dimnames")=List of 2
 .. ..$ : chr [1:5] "1" "2" "3" "4" ...
 .. ..$ : chr [1:4] "Murder" "Assault" "UrbanPop" "Rape"
 $ totss : num 355808
 $ withinss : num [1:5] 4548 2286 16272 1480 3653
 $ tot.withinss: num 28240
 $ betweenss : num 327568
 $ size : int [1:5] 10 9 14 10 7
 $ iter : int 3
 $ ifault : int 0
 - attr(*, "class")= chr "kmeans"
```

str()函数给出了 kmeans 的结构，其中包括各种参数，如 withinss、betweenss 等，分析这些参数可以了解 kmeans 的性能。

两两之间:平方和之间，即聚类内相似性

内:平方和内，即聚类间相似性

totwithinss:所有聚类的所有 withinss 之和，即总的类内相似性

一个好的聚类将具有较低的 withinss 值和较高的 betweenss 值，这取决于最初选择的聚类数“k”。让我们看看怎样才能找到“k”的最佳值。

## 寻找‘k’的最佳值

“k”的最佳值是给我们一组具有最小失真的收敛聚类的值。变形越大，形成的簇就越差。

**失真:**

可以根据每个聚类的“内差”来计算失真。特定聚类的“withinss”值越小，它的分布越密集，因此失真最小。

```
kmeans.wss.k <- function(crime, k){
 km = kmeans(crime, k)
 return (km$tot.withinss)
 }
```

该函数获取数据和 k 的值，并为其返回“km$totwithinss”。“km $ totwithinss”是总的组内平方和，因此包括所有 5 个创建的组的组内，即`sum(withinss)`。“km$totwithinss”的值越高，失真越大。

对于 k=5，withinss 是 24417.02

```
> kmeans.wss.k(crime,5)
 [1] 24417.02
```

让我们将 k 的值从 5 增加到 10，并观察差异。

```
> kmeans.wss.k(crime,10)
 [1] 11083.04
```

可以看出，随着 K 值的增加，失真减小。

我们可以取出“km $ totwithinss”的不同值，并将它们绘制在图表中，以找到失真与 k 值之间的关系。下面的函数为我们完成了这项工作:

```
> kmeans.dis <- function(crime, maxk){
+ dis=(nrow(crime)-1)*sum(apply(crime,2,var))
+ dis[2:maxk]=sapply (2:maxk, kmeans.wss.k, crime=crime)
+ return(dis)
+ }
> maxk = 10
> dis = kmeans.dis(crime, maxk);
> plot(1:maxk, dis, type='b', xlab="Number of Clusters",
 + ylab="Distortion",
 + col="blue")
```

[![Capture1 (1)](img/39daf48f0aa1002fbe2346fffabd0974.png "plot")](https://cdn.edureka.co/blog/wp-content/uploads/2015/01/Capture1-1.png)

哒哒！！！因此，我们有著名的肘曲线。

**肘部曲线:**

这是每个 k 值的“k”、聚类数和“totwithinss”(或失真)之间的关系图。您可以看到，当聚类数较少时，失真会逐渐降低，但随着 k 值的不断增加，失真值的降低率会保持不变。

这个 k 值是最佳值，超过这个值，失真率变为常数。这里 k=4。

让我们应用一些动画来理解 R 是如何给出聚类结果的。

```
> library(animation)
> cl<- kmeans.ani(crime, 4)
```

**k 均值聚类算法:**

让我们理解 k-means 聚类工作的算法:

第一步。如果 k=4，我们选择 4 个随机点，并假设它们是要创建的聚类的聚类中心。

第二步。我们从空间中选取一个随机数据点，并找出它与所有 4 个聚类中心的距离。如果数据点最接近绿色聚类中心，则它被着色为绿色，并且类似地，所有点都被分类到 4 个聚类中。

[![Capture10](img/8b64a3a76b9cc7bb2a0dcf92113e7696.png "plot1")](https://cdn.edureka.co/blog/wp-content/uploads/2015/01/Capture101.png)

第三步。现在，我们计算所有绿色点的质心，并将该点指定为该聚类的聚类中心。

类似地，我们计算所有 4 个彩色(聚类)点的质心，并将新的质心指定为聚类中心。

[![Capture9](img/5c473cccf1184ae2ebea2c580df7e99e.png "plot2")](https://cdn.edureka.co/blog/wp-content/uploads/2015/01/Capture91.png)

第四步。步骤 2 和步骤 3 迭代运行，除非聚类中心收敛于一点并且不再移动。

[![Capture8](img/e423e4dc7da022fc0ed5401e1de00b54.png "plot3")](https://cdn.edureka.co/blog/wp-content/uploads/2015/01/Capture81.png)

[![Capture7](img/9cc9b78e930b6f13aec780da8ab6da08.png "plot4")](https://cdn.edureka.co/blog/wp-content/uploads/2015/01/Capture71.png)

[![Capture6](img/415e06b389982484c3242a2d81f69050.png "plot5")](https://cdn.edureka.co/blog/wp-content/uploads/2015/01/Capture61.png)

[![Capture5](img/eef22c8675c130980022e286230b39be.png "plot6")](https://cdn.edureka.co/blog/wp-content/uploads/2015/01/Capture51.png)[](https://cdn.edureka.co/blog/wp-content/uploads/2015/01/Capture6.png)[![Capture4](img/dbd64bc855544390614a34da9a189699.png "plot7")](https://cdn.edureka.co/blog/wp-content/uploads/2015/01/Capture42.png)

[![Capture3](img/5b489d969999e8d4133ff6381e834e89.png "plot8")](https://cdn.edureka.co/blog/wp-content/uploads/2015/01/Capture34.png)

因此，我们到达了聚合的集群中心。

可以看出，数据分为 4 个簇。集群中心包括:

```
> cl$centers
 Murder Assault UrbanPop Rape
Texas 4.740741 104.8519 62.96296 16.10
Louisiana 10.907143 219.9286 71.71429 25.95
South Carolina 13.375000 284.5000 46.25000 25.05
New Mexico 11.040000 298.0000 77.60000 32.68
```

以“新墨西哥”为聚类中心的聚类-4 具有巨大的犯罪率和最高的人口。

群组 3 和群组 2 采取后续行动。

每个州都被分配了一个聚类，根据这个聚类我们现在可以预测它的犯罪排名。输出如下所示:

[![cluster-output](img/5b940fbc6f26561cc430d3f67fd7796f.png "clustered output")](https://cdn.edureka.co/blog/wp-content/uploads/2015/01/cluster-output1.png)

有问题要问我们吗？请在评论区提到它，我们会给你回复。

**相关帖子:**

[R](https://www.edureka.co/r-for-analytics)商业分析入门

[数据科学入门](https://www.edureka.co/data-science)