# 通过几何重正化对真实网络进行多尺度展开

- 多尺度 与 小世界 的矛盾
  - 欧式长度和对称性的缺陷
- 复杂网络的几何重正化群
  - 将真实网络插入到一个度量空间，会体现出geometric scaling特征 



复杂网络中，多尺度也是共存的，但是它们被一些其他的事限制住了，并不能直接讨论*自相似性*和*标度无关性*。原因是我们没有一种有效的手段来对网络的length scale进行变换。

- 以前的手段：
  - 拓扑/粗粒化/random walks
  - /box-covering/：证明了真实网络有着有限的分形维数，有自相似性
  - 拓扑scaling性质只体现在度分布、平均度、最大度上面
  - 尽管有很好的度量，最短路径的集合作为研究length-based scaling factor还是很不好的数据集。（原因是small-world的存在）
- In this work, we introduce a geometric renormalization
  group for complex networks (RGN). The method is based on a geometric embedding of the networks to construct renormalized versions of their structure by coase-graining neighbouring nodes into supernodes and defining a new map which progressively selects longer range connections by identifying relevant interactions at each scale. The RGN technique is inspired by the block spin renormal- ization group devised by L. P. Kadanoff [18].

## 真实网络中几何标度存在的证据

- 研究对象：复杂网络到hidden度量空间的映射：$\mathcal M(T,G)$
  - 定义一个几何重正化算子$\mathbb F_r$，得到一个新的拓扑$T'$和一个新的几何图$G'$，由此定义一个新的重正化映射$\mathcal M'$:$$\mathcal M(T,G)\rightarrow^{\mathbb F_r}\mathcal M'(T',G')$$
  - The transformation zooms out by changing the **minimum length scale** from that of the original network to a larger value. 
  - 这个过程可以迭代$O(\ln N)$次。
- 例子：
  - 最简单的度量空间：一维圆周：$\{\theta_i:i=1,2,3,\cdots,N\}$
    - 重正化步骤：
      1. 定义block：圆周上挨着的$r$个点。
      2. 粗粒化为超级结点（不管是否连接）每个超级结点都控制一个角区域。所以它们的序关系得以保留。
         - 原连接：
           - 超级结点内
           - 超级结点间：建立边
  - 用到的例子：
    - Internet
    - Airports
    - 新陈代谢
    - scripts……
- $\mathbb S_1$模型：将结点放在一个圆周上，以一定概率分布连接每两个点。两个点越远链接概率越低（similarity），度乘积越大连接概率越高（popularity）。
- 



应用：The RGN enables us to unfold scale-free complex net-
works in a self-similar multilayer shell which unveils the coexisting scales and their interplay. Beyond

- Mini-me network replicas.
  - networked communication systems
  - 可以保持微观结构的同时，不破坏介观结构
  - Mini-me replicas can also be used to perform finite size scaling of critical phenomena taking place on real networks
  - Typically, the renormalized average degree of real net- works increases in the flow, since they belong to the small-world phase (see inset in Fig. 3B), meaning that the network layer at the selected scale is more densely connected. 
