# 6.3. Raft协议

raft 是一种分布式一致性算法，其能够保证在 2n+1 的系统，有 n+1 以上的节点存活时，向集群中写入的数据保证不会丢失。相比 paxos，其有更好的易读性和简洁性，所以从诞生起便受到很多人的赞许。该算法与 paxos 类似，被广泛应用于分布式调度的元信息存储，或在存储领域进行日志复制。

开源界使用最为广泛的实现是基于 raft 实现的 etcd、consul，不过 etcd 的 raft 和自身强绑定，我们如果只是想使用算法的话并不是很方便。hashicorp 为我们直接开源了 raft 的算法库 `https://github.com/hashicorp/raft`，本节中，我们将基于该库实现几个小工具。

## 实现分布式状态机

## 实现分布式日志复制
