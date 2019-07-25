# 【图论笔记】权转移法（1）：构型和不可回避集
---

## 目录

+ <a href="#1">1. 构型</a>
+ <a href="#2">2. 不可回避集</a>
+ <a href="/html/notes/graph-theory/graph-theory.html"> 返回【图论笔记】 </a>

---

## <a name="1"> 1. 构型 </a>

设$G$是一个图．如果$H$作为$G$的子图满足$G$上的局部性质$\mathcal{Q}$，那么我们就说 ==$(H,\mathcal{Q})$是$G$的一个构型==（configuration），也称==构型$(H,\mathcal{Q})$在$G$上出现了==．如果在上下文语境中，局部性质$\mathcal{Q}$是明确的，那么我们也可以直接说 ==$H$是$G$的一个构型==．

>例如，在<a href="/html/notes/graph-theory/discharge/00-basic.html">【权转移法(0)】</a>的例题中，我们可以把边看成子图$K_2$，那么，$(5,5)$-边和$(5,6)$-边就是两种构型．如果我们分别记这两种构型为$H_1$和$H_2$，那么该例中的命题就可以变成：

>最小度为$5$的平面三角剖分图含有构型$H_1$或构型$H_2$．

---

## <a name="2"> 2. 不可回避集</a>

我们继续来剖析这个命题．

任何命题都有前提和结论．而任何图论命题的前提都蕴含了一个图族．例如，如果我们设$\mathcal{G}$是所有最小度为$5$的平面三角剖分图所构成的图族，并且记$\mathcal{H}=\{H_1,H_2\}$，那么，在上述命题又可以进一步改写为

>$\mathcal{G}$中的每个成员总会含有$\mathcal{H}$中的某个构型．

一般地，我们设$\mathcal{G}$是一个图族，$\mathcal{H}$是一个由构型组成的集合．如果$\mathcal{G}$中每个成员都含有$\mathcal{H}$中至少一个构型，那么，我们就说==构型集$\mathcal{H}$是图族$\mathcal{G}$所无法回避的==，或者说$\mathcal{H}$是$\mathcal{G}$的==不可回避集==（unavoidable set）．

如果我们依然设$\mathcal{G}$所有最小度为$5$的平面三角剖分图所构成的图族，并且记$\mathcal{H}=\{H_1,H_2\}$，那么，在上述命题最终可以改写为

>$\mathcal{H}$是$\mathcal{G}$的一个不可回避集．

本质上说，==权转移法就是搜索某个图族的不可回避集的方法==．

而<a href="/html/notes/graph-theory/discharge/00-basic.html">【权转移法(0)】</a>中的那个例题其实就是Wernicke在1904年提出的第一个使用权转移法解决的图论问题。

那么，权转移法是如何搜索不可回避集的呢？我们需要两个主要工具：==初始电荷量==和==放电规则==．

---
+ <a href="/html/notes/graph-theory/graph-theory.html"> 返回【图论笔记】 </a>