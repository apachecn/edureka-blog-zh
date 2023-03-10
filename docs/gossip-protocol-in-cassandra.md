# 卡桑德拉的八卦协议

> 原文：<https://www.edureka.co/blog/gossip-protocol-in-cassandra/>

## Cassandra 中的八卦协议

在 Cassandra 中，节点之间的通信通常像点对点通信一样，每个节点都与另一个节点对话。如果是这样的话，那么所有的节点都会相互交流，并且会有大量的交流发生。八卦协议是解决这种通信混乱的一种方法。 在 Cassandra 中，当 一个节点与另一个节点通话时，期望响应的节点不仅提供关于其状态的信息，还提供关于其之前通信过的节点的信息。通过这个过程，减少了网络日志，保存了更多的信息，提高了信息收集的效率。该协议的主要特点是分别提供任意节点的最新信息。

## 故障检测

Gossip 协议的一个重要特征是故障检测。基本上，当两个节点相互通信时；例如，节点 A 向节点 B 发送消息“gossipdigestsynmessage”，这非常类似于 TCP 协议向节点 B 发送的消息。在这里，节点 B 一旦接收到消息，就发送确认消息“ack”，然后节点 A 用确认消息来响应节点 B 的“ack”消息。这就是所谓的三次握手。

如果在这种情况下，节点关闭，不发送 ack 消息，那么它将是一个标记关闭。即使当节点关闭时，其他节点也会定期 ping，这就是故障检测的发生方式。

有问题要问我们吗？在评论区提到它们，我们会回复你，或者从 Edureka 获得你的 [Cassandra 认证](https://www.edureka.co/cassandra)。

**![Cassandra Logo - Edureka](img/81ab8960b11ba7a9ab4beb7aa44956ec.png)**

**![edureka](img/981b79f2904efe6f9320df33611b9823.png)相关帖子:**

[学习卡珊德拉的 5 大理由](https://www.edureka.co/blog/top-5-reasons-to-learn-cassandra-decoded/)