# [Concatenation of Prefixes](https://atcoder.jp/contests/abc480/tasks/abc480_d)

预处理整块和，单独求 $L$ 与 $R$ 所在的非整块和。

令 $A$ 的前缀和为 $S$，$S$ 的前缀和为 $T$，$P_i=\sum\limits_{j=1}^ij$。

在 $P$ 中二分，记 $L$ 在第 $L'$ 块，$R$ 在第 $R'$ 块，$l=L-P_{L'-1}$，$r=R-P_{R'-1}$，则答案为：

$$
\begin{cases}
S_r-S_{l-1} & L'=R' \\
T_{R'-1}-T_{L'}+S_{L'}-S_{l-1}+S_r & L'<R'
\end{cases}
$$