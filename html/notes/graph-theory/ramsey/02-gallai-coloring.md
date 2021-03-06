# 【图论笔记】Gallai-Ramsey数（2）：Gallai染色

Gallai染色得名与匈牙利著名组合学家Gallai对可比图的研究工作．

---

## 目录

+ <a href="#1">1. 定义与基本性质</a>
+ <a href="#2">2. Gallai染色的颜色导出图</a>
+ <a href="#3">3. Gallai染色的结构定理</a>
+ <a href="#4">4. Gallai染色图中的单色支撑树</a>
+ <a href="/html/notes/graph-theory/graph-theory.html"> 返回【图论笔记】 </a>

---

## <a name="1"> 1. 定义与基本性质 </a>

1. 设图$G$具有边染色$c$．如果$G$的每个边的颜色都不同，则称$c$是$G$的==彩虹染色==；特别地，如果$G$是具有彩虹染色的三角形，则称$G$是==彩虹三角形==．
2. 设$n$阶完全图$G$具有边染色$c$且$c$至少使用了两种颜色．如果$K_n$没有彩虹三角形，则称$c$是$K_n$的一个==Gallai染色==．
3. 设$c$是$n$阶完全图$G$上的Gallai染色．我们称颜色为$i$的边子集为染色$c$的 ==$i$-色类==，记作$c^{-1}(i)$．设$G_i$是$G$的一个支撑子图，满足$V(G_i)=V(G)$，$E(G_i)=c^{-1}(i)$，则称$G_i$是==颜色$i$所导出的子图==．

> ==完全图的任意一种2-边染色肯定是Gallai染色==，我们需要研究颜色数大于等于3的Gallai染色．

>==引理 1.（基本性质）== 设$c$是$n$阶完全图$G$上的一个Gallai染色，$j$是$c$所用的一个颜色，颜色$j$在$G$上的导出子图记为$G_j$．如果$G_j$不连通，那么$G_j$的任意两个分支之间的所有边使用相同的颜色．

>==证明.== 设$C_1$和$C_2$是$G_j$的两个连通分支，$u_i,v_i\in C_i$（$i=1,2$）．$u_1u_2$所用的颜色为$k$．下证$v_1v_2$所用颜色也是$k$．因为$C_1$是连通分支，所以$G_j[C_1]$中存在一条$u_1$到$v_1$的路$P=w_0w_1w_2\dots w_t$，其中$w_0=u_1,w_t=v_1$．由于三角形$u_1w_1v_1$不是彩虹三角形，而$c(u_1w_1)=j,~c(u_1u_2)=k,~c(w_1u_2)\ne j$，所以$c(w_1u_2)=k$，以此类推对每一个$w_s(1\le s\le t)$，总有$c(w_su_2)=k$，所以$c(v_1u_2)=k$．同样地，在$G_j[C_2]$中存在一条从$u_2$到$v_2$的路，使用相似的论证可得，$c(v_1v_2)=c(v_1u_2)=k$．$\Box$

---

## <a name="2"> 2. Gallai染色的颜色导出图 </a>
 
>==引理 2.== 设$G$是$n$阶完全图（$n\ge4$）．那么$G$上每一个颜色数至少为$3$的Gallai染色中，==总有一种颜色导出不连通的子图==．

>==证明.== 设$c$是$G$上一个颜色数至少为$3$的Gallai染色．对$G$上任意一点$x$．若$x$的邻边没有用尽$c$的颜色，那么结论显然．不妨设$x$的邻边已经用尽了$c$的颜色．如果$c$在$G\setminus x$上只用了两种颜色，那么结论显然仍成立，所以不妨设$c$在$H$上仍然是一个颜色数至少为$3$的Gallai染色．

>下面对$n$作归纳．
>
>当$n=4$时，取$x\in V(G)$，那么$x$的三个邻边用尽了$1,2,3$三种颜色．容易验证$G\setminus x$上有两种颜色不能导出连通图．
>
>设$n\ge5$．假定图的阶数小于$n$时命题成立，现在考虑阶数为$n$的情况．设$H=G\setminus x$．由归纳假设知，$c$的某种颜色在$H$上导出的子图是不连通的，不妨颜色$1$在$H$上的导出子图（记作$H_1$）是不连通．设$H_1$的连通分支为$C_1,C_2,\dots,C_k$．由基本性质可知：对任何$C_i$和$C_j$（$i\ne j$），$C_i$和$C_j$之间的所有边的颜色只能是同一种异于$1$的颜色，否则会出现彩虹三角形（注意$G$是完全图）． 
>
>下面证明颜色$1$在$G$中的导出子图$G_1$是不连通的．由于$H_1$是不连通的，所以我们只需要证明存在某个$C_i$使得$x$与$C_i$之间没有颜色为1的边．假设不然，即任意$C_i$中总存在$y_i$使得边$xy_i$颜色为1．另一方面，由于$x$会用尽$c$的颜色，而$c$至少3种颜色，所以不妨设$u,v\in V(H)$，使得$xu$颜色为2，$xv$颜色为3．
>
> 1. $u,v$落入$H_1$的同一个分支中，不妨设$u,v\in C_1$．由于$C_1$与$C_2$之间的边颜色不是$1$，且$G$中没有彩虹三角形，所以$uy_2$颜色为$2$，$vy_2$颜色为$3$，这与基本性质矛盾．
>
> 2. $u,v$落入$H_1$的不同一个分支中，不妨设$u\in C_1$，$v\in C_2$．从三角形$xy_1v$来看，$vy_1$颜色为$3$；从三角形$xy_2u$来看，$uy_2$的颜色为$2$．这与基本性质矛盾．$\Box$

---

## <a name="3"> 3. Gallai染色的结构定理 </a>

>==定理 3.（Gallai染色的结构定理）== 设$c$是$n$阶完全图$G$（$n\ge3$）的任意一个Gallai染色．那么$V(G)$可以划分为$p$（$p>1$）个非空集$V_1,V_2,\dots,V_p$，满足：
>1. $E(G)\setminus \left[E(G[V_1])\cup E(G[V_2])\dots \cup E(G[V_p])\right]$至多只使用了两种颜色；
>2. $V_i$与$V_j$（$i,j=1,2,\dots,p$且$i\ne j$）之间的边只使用一种颜色．

>==证明.== 对$c$所使用的的颜色数作归纳．如果$c$只用了两种颜色$1$和$2$，那么我们在$G$中删除颜色为1的边，将得到的子图的顶点集按连通分支划分，这个划分显然满足要求，结论成立．假定当$c$使用的颜色数小于$k~(k\ge3)$时结论成立，现在考虑$c$使用的颜色数为$k$的情况．因为$k\ge3$，所以$v(G)\ge4$．由引理 2可知，$c$所用的颜色中必有其一的导出子图不连通，不妨设颜色$1$的导出子图不连通．收缩掉颜色$1$的各个连通分支，设新图为$G'$，新的染色为$c'$．由基本性质可知：$c'$是$G'$上的Gallai染色．由于颜色$1$的导出图不连通，且颜色数至少为$3$，所以$v(G')\ge2$，又因为$c'$的颜色数小于$k$，所以由归纳假设知：$G'$有一个满足要求的划分，将这个划分还原为$G$的划分就是所要找的划分． $\Box$

>==推论 4.== $n$阶完全图的Gallai染色至多用掉$n-1$种颜色．

>==证明.== 使用定理 3的归纳法即可． $\Box$

带有Gallai染色的完全图叫做==Gallai染色图==．由定理 3 所给出的划分叫做Gallai染色图的==Gallai划分==．设$V_1,V_2,\dots,V_p$是Gallai染色图$G$的一个Gallai划分．将$V_1,V_2,\dots,V_p$分别收缩，我们会得到一个二色Gallai染色图$G/c$，我们称$G/c$是$G$的==基图==，每个$G[V_i]$也是一个Gallai染色图，称之为$G$的==分块==．

---

## <a name="4"> 4. Gallai染色图中的单色支撑树 </a>

>==Dirac定理.== $k$-连通图的任意$k$个顶点能被长度至少为$k+1$的圈所覆盖．

>注：Dirac定理是著名的 ==“扇子引理”== 的推论．

将一个路的一个端点粘在一个星的中心，得到的树叫做==扫帚（broom）==．

>==定理 5.== 完全图的每个Gallai染色都有一个单色支撑扫帚．

>==证明.== 设$G$是一个带Gallai染色的完全图．由定理 3 可知，$G$的基图是二色的，设两色为$1$和$2$，记这两色在$G$上的导出子图分别为为$G_1$和$G_2$．不妨设$G_1$的连通度不超过$G_2$的连通度．取$G_1$的一个最小点割集$A$．如果$A=\emptyset$，那么$G_1$不连通，所以$G$有一个颜色为$2$的支撑完全二部图，显然有一个颜色为$2$的支撑扫帚．不妨设$A\ne\emptyset$，那么$G_1$连通．而$G_2$的连通度不低于$G_1$，所以$G_2$也连通．那么$G\setminus A$有可以非平凡地划分为$X,Y$，使得$G\setminus A$在$X$和$Y$之间没有颜色为$1$的边．下面首先证明这个论断：
>
>+ ==**论断.** $X\cup Y$有一个颜色为2的支撑完全二部图$H$．==
>
>如果任何一对$x,y$不落在同一个分块中，那么论断显然成立．不妨设存在分块$B$使得$B\cap X\ne\emptyset$且$B\cap Y\ne\emptyset$．假设$X\cup Y\subseteq B$．如果某个包含于$A$的分块与$B$之间的边是颜色2，那么这个分块与$X\cup Y$之间的边的颜色就是2，那么$A$就不是$G_1$的最小点割集了．所以$B$与包含于$A$的分块之间的边的颜色都是1，因为$X\cup Y\cup A=V(G)$，所以除$B$之外，其他分块包含于$A$，所以$B$在颜色$2$的导出图$G_2$中不能与其他顶点相邻，这与$G_2$连通矛盾．因此$X\not\subseteq B$或$Y\not\subseteq B$．任取与$X$有交的另一个分块$B_1$．如果$B_1$与$B$之间的边的颜色为1，那么因为$B$与$Y$有交，所以$X$与$Y$之间存在颜色为1的边，矛盾．所以$B$与$X\setminus B$之间的边都是颜色2．同理，$B$与$Y\setminus B$之间的边都是颜色2．那么，$B\cap (X\cup Y)$与$(X\cup Y)\setminus B$之间的边的颜色都是2，所以论断成立．
>
>设$|A|=k$，那么$G_1$和$G_2$都是$k$-连通的．由Dirac定理可知，$G_2$上存在至少$k+1$个顶点的圈$C$覆盖$A$，因为$|C|>|A|$，所以$C$与$H$有交，因此$H\cup C$中显然有一个颜色为2的支撑扫帚． $\Box$

>==定理 6.== 完全图的每个Gallai染色都有一个高度至多$2$的单色支撑树．

>==证明.== 设$G$是一个Gallai染色的完全图．由定理3可知，$G$有一个两色的基图$H$．在$H$上以任意一个单色最大度顶点为根，很容易得到一个单色的高度至多2的支撑树$T$．下面将$T$还原为$G$的支撑树$T'$．首先将$T$的顶点还原为分块．下面选取分块之间的边加入$T'$．设$x\in V(T)$，$y$是$x$的父顶点，$z$是$x$的子顶点，$X,Y,Z$分别是$x,y,z$所对应的的分块．如果$x$不是树根，取定$Y$中的一个顶点$y_0$，将所有$y_0$与$X$之间的边加入$T'$；如果$x$是树根，设$x_0\in X$已经被$Z$中的顶点作为父顶点，再在$Z$中取一顶点$z_1$将$z_1$与$X\setminus x_0$全部加入$T'$．完成上述过程后所得到的$T'$显然是$G$的单色支撑树，且高度至多为2． $\Box$

>==定理 7.== 完全图的每个Gallai染色的单色最大度至少$\frac{2n}{5}$．

>==证明.== 设$G$是一个Gallai染色的完全图．由定理3可知：$G$有一个2色基图$H$．如果$v(H)\le4$，那么很容易由鸽笼原理验证，$1,2$两色中必有其一其最大度至少$n/2$．不妨设$v(H)\ge5$．那么存在一个分块，其顶点数至多$n/5$，所以这个分块至少有$4n/5$条边连出去，这些边的颜色为1或2，由鸽笼原理知结论成立．$\Box$

---

    参考文献
    A.Gyarfas, G. Simonyi, Edge Coloring of complete Graphs Without Tricolored Triangles, 2003.

---

<a href="/html/notes/graph-theory/graph-theory.html"> 返回【图论笔记】 </a>