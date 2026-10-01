# [Count Cells in a Window](https://atcoder.jp/contests/abc477/tasks/abc477_f)

离线询问，对行做扫描线，维护前 $i$ 行每一列的黑块数量。于是一个询问可以拆成在 $A-1$ 行和 $B$ 行上的两个 $[C,D]$ 区间查询。$[L_i,R_i]$ 也是区间修改，那么线段树维护即可。