---
title: TikZ学习笔记：1.使用TikZ宏包
layout: default.html
---

# {{ page.title }}

----------------------------------
画一条折线

```
\documentclass[tikz]{standalone}
\usepackage{tikz}
\begin{document}
    \begin{tikzpicture}
        \draw (0,0) -- (3,5) -- (6,2);
    \end{tikzpicture}
\end{document}
```

画图效果
![一条折线](https://SongNingSDUT.github.io/img/tikz-1-1.jpg)

{{ page.date|date_to_string }}