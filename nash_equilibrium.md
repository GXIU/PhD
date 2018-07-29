## Results

### 几何空间选取

双曲空间：有最大的随机性，也就是满足了最大熵、幂律分布、强集聚效应的特性。如果是欧式空间，则仍然会有集聚效应，但是度分布就不是幂律分布了，而是Poisson分布（无厚尾）。

随机几何图的定义：均匀分布在某一个几何空间的结点的集合。一对点会被连起来，如果在某一度量下，两个点的距离小于固定阀值。

给定真实网络所在的空间是双曲的，我们先随机在双曲圆盘上撒点，（但是先不连边），给定撒的点的坐标，我们下一步要做的是确定连边的集合，来实现纳什均衡（Nash Network Graphs）。

然后分析均衡网络的结构性质，**惊奇地发现，**这种图有幂律分布和集聚效应。

<u>This result invites us to investigate whether these navigation-critical edges exist in real networks.</u>  

存在决定通行能力临界状态的边吗？

方法：将真实网络通过HyperMap映射到双曲空间，然后根据推断的坐标建立纳什均衡网络。**我们发现，真实网络基本都包括纳什均衡所必须的边。**



### 博弈定义

将$N$个结点随机撒在半径为$R$的双曲平面上。密度为密度函数
$$
\rho(r,\theta) = \frac{1}{2\pi} \frac{\alpha \sinh(\alpha r)}{\cosh(\alpha R)-1}
$$
其中，$\alpha \gt 1/2.$ $\alpha $是控制空间异质性的参数。如果$\alpha =1$那么点就是均匀分布的，因为$dA = \sinh(r)drd\phi.$ 

结点$u$的位置：
$$
\begin{cases}r_u=\frac{1}{\alpha}\text{acosh}\{1+[\cosh(\alpha R)-1]U\}\\
\phi_u = 2\pi U\end{cases}
\\U=\text{Uniform}[0,1]
$$
双曲空间中的距离定义为
$$
d(u,v)=\text{acosh}[\cosh r_u\cosh r_v-\sinh r_u\sinh r_v \cdot \cos(\phi_u-\phi_v)]
$$
**建立单向网络**如下：对于固定的结点$u$，如果$\exists u',u'\sim u,$ 且$d(u,v)\gt d(u',v),$ 那么称$v$与$u$互通. 

### Nash均衡

给定$u,$ 称$v$的**覆盖域**为：{相对于$u,$ 离$v$更近的结点}。当然$v$覆盖它自己，因为$d(v,v)=0<d(u,v).$ 所以如果$u$与所有其他结点相连，它就全覆盖他们。（？？？）.$u$最优策略是：连接最少量的结点，使得它连接的结点集合的覆盖域包含全部结点。这也就变成了一个最小覆盖问题。

这个问题的Nash equilibrium不一定唯一。但是，网络中总是存在一些frame edge。在任何的Nash equilibrium中都需被包含：Edge u-v is a frame edge if u is the closest player to v.  只要有一个这样的边没在均衡网络中，那么网络通行能力都不是$100$%. 

### 结构性质

用双曲三角学的性质，我们证明：如果结点的密度是均匀的，那么距离为$d$的两点在Nash equilibrium网络中相连接的概率在$e^{-8\delta e^{d/2}}$到$e^{-2\delta e^{d/2}}$之间。其中$\delta$是平面上人的平均密度。也就是$\frac{N}{A}.$ 

到圆心距离为$r_u$的点的期望度（是指数衰减的！同时密度$\rho(r)$是指数递增的）为
$$
\begin{align}
\bar{k}(r_u)&=N\iint p[d(u,v)]\rho(r_v,\theta_v)dr_vd\theta_v\\
&\in[\frac{1}{2}e^{(R-r_u)/2},2e^{(R-r_u)/2}]
.\end{align}
$$
于是所有的结点的期望度$\bar{k}:$ 
$$
\bar{k}=\int_0^R\bar{k}(r)\rho(r)dr\in[1,4]
$$

- 到圆心距离为$r_u$的点的期望度是指数衰减的，同时密度$\rho(r)$是指数递增的. 这两个指数是我们导出了网络的度分布是幂律的。
- 集聚系数
  - $\bar c(k)\sim 1/k$
  - $\bar c=\sum_k P(k)\bar c(k)\approx0.45$它与平均度无关，是一个正的常数。

这两个指数都与$\delta$无关。









## Discussion

## Method

