# [Product-Bounded Arithmetic Sequences](https://atcoder.jp/contests/abc480/tasks/abc480_e)

记 $l=|A|$，$d=A_2-A_1$。

由 $20!>10^{18}$，得 $l<20$。

由 $\prod\limits_{i=1}^lA_i>(A_1)^l\ge(A_1)^3$，得 $A_1<10^6$。

当 $l,A_1$ 固定，若 $d$ 可行，则小于 $d$ 的公差都可行。

于是我们枚举 $l$ 和 $A_1$，二分最大可行的 $d$，把所有 $d$ 加起来即为合法的 $A$ 的数量。

时间复杂度 $O(l_{max}A_{1max}\log d_{max})$，上界不紧而且能够剪枝，可以接受。