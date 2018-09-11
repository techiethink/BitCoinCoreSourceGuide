# BitCoinCoreSourceGuide
这是一个Xmind文件，尝试去分析比特币源代码，从系统启动流程，p2p网络拓扑结构的维护，再到关键的业务流的分析。之所以先分析bitcoin network而不从ethereum开始，是因为在p2p网络层，以太坊使用了IPFS的libp2p，使得p2p网络层部分的功能和算法开不到。所以从学习和研究的目的看，选择了bitcoin network。

用到的工具目前有：xmind。请安装xmind来阅读启动流程部分，并注意每个分支中的注解，里头保护有代码的功能介绍。

另外，针对区块链行业瓶颈问题：分布式共识这部分，收集了一些传统分布式事务算法的论文，大家可以学习并比较一下区块链中的共识算法（PoW, PoS, DPoS, PoR, SideChain, Lightning network, network sharding etc...）。

分布式共识这部分的发展主线：分布式系统CAP模型已经被MIT从数学上面论证，在区块链共识这部分类似地也很难同时突破3个要素（安全性，性能，可扩展性）。从bitcoin network到ethereum再到EOS目前性能的提升看，每次的提升都伴随着安全上面的牺牲——越发趋于中心化。安全可以通过其他因素来约束。个人觉得联盟链落地高效的应用可能性更大，目前公链很难突破性能瓶颈，当然这部分的创新发展也很快，期待闪电网络的落地。

# 2PC-type consensus paper link
## PBFT
  http://pmg.csail.mit.edu/papers/osdi99.pdf    
  http://www.pmg.csail.mit.edu/papers/bft-tocs.pdf    
  [阅读时请自己提出批判性问题，去返推出作者观点。]    
  http://www.cs.utah.edu/~stutsman/cs6963/public/pbft.pdf    
## RAFT
  [实验室的分布式数据库也用的类似与RAFT的算法，只不过在实现时只满足了80%的RAFT算法]    
  https://raft.github.io/raft.pdf    
## Paxos
  http://www.scs.stanford.edu/~dm/home/papers/paxos.pdf    
  https://lamport.azurewebsites.net/pubs/lamport-paxos.pdf    
  https://lamport.azurewebsites.net/pubs/paxos-simple.pdf    
