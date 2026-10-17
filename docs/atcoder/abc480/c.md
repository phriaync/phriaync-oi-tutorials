# [Self-Stopping Shower](https://atcoder.jp/contests/abc480/tasks/abc480_c)

将 $A$ 从小到大排序。注意 $T$ 可能小于 $A_i$，可以令 $A_{n+1}=T$，设排序后 $T$ 第一次出现在 $A_x$。

令 $A_0=-k$，贪心地开开关，答案为：

$$
\sum_{i=1}^x\max(0,\lceil\frac{A_i-(A_{i-1}+k)}{k}\rceil)
$$