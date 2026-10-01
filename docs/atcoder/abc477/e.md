# [Wheel Distance](https://atcoder.jp/contests/abc477/tasks/abc477_e)

$s$ 到 $t$ 的最短路有且仅有两种：

- 经过 $n+1$，此时 $d_{s,t}=d_{s,n+1}+d_{n+1,t}$；
- 不经过 $n+1$，此时 $d_{s,t}=\min(\sum\limits_{i=s}^{t-1}a_i,\sum\limits_{i=1}^na_i-\sum\limits_{i=s}^{t-1}a_i)$

于是预处理 $a$ 的前缀和及 $n+1$ 的单源最短路即可做到 $O(1)$ 查询。