---

title: 4.境界あり Chern–Simons 理論
date: 2025-12-27
tags:

    - Chern-Simons
    - anyon

---

境界のある CS 理論では chiral boson が現れることを確かめる。

外場を切り $A_\mu=0$、また $\nu=1/k$ とする。作用は

$$
S
=

\frac{k}{4\pi}\int a,da

\frac{k}{4\pi}\int d^3x,\epsilon^{\mu\nu\rho}a_\mu\partial_\nu a_\rho .
$$

運動方程式は

$$
\begin{aligned}
da=0 .
\end{aligned}
$$

一見つまらないが、トーラス上の anyon の trajectory などを考えると non-trivial なトポロジカル数が現れる。

セットアップ：$xy$ 平面で $y>0$ が真空、$y<0$ が FQH 状態。$a$ に関する変分を取ると boundary 項が出る：

$$
\begin{aligned}
\delta S
=

\frac{k}{2\pi}\int d^3x,
\Bigl[
2\epsilon^{\mu\nu\rho},\delta a_\mu,\partial_\nu a_\rho
+
\epsilon^{\mu\nu\rho}\partial_\mu(a_\nu,\delta a_\rho)
\Bigr].
\end{aligned}
$$

boundary の取り扱いにより、例えば

$$
\begin{aligned}
a_t|*{y=0}=0
\quad\text{or}\quad
a_x|*{y=0}=0
\end{aligned}
$$

などの条件が必要になる。あるいは

$$
\begin{aligned}
(a_t - v a_x)|_{y=0}=0
\end{aligned}
$$

としてもよい（$v$ は後で chiral boson の速度として解釈される）。

この理論に bosonization を施すと、境界自由度が chiral boson の理論に等しいことを示せる（詳細は後述）。

まず $x$ 方向に速度 $v$ で動く系 $(t',x',y')$ に移る：

$$
\begin{aligned}
t' = t,\qquad x' = x + vt,\qquad y' = y .
\end{aligned}
$$

1-form の変換として

$$
\begin{aligned}
\omega'*\mu = \frac{\partial x^\nu}{\partial x'^\mu},\omega*\nu
\end{aligned}
$$

を用いると

$$
\begin{aligned}
a'_t = a_t - v a_x,\qquad
a'_x = a_x,\qquad
a'_y = a_y .
\end{aligned}
$$

境界で $a'_t=0$ が運動方程式になり、さらに

$$
\begin{aligned}
da' = f_{x'y'} = 0
\end{aligned}
$$

より、解は boson 場 $\phi$ を用いて

$$
\begin{aligned}
a'_i = \partial'_i \phi,\qquad i=x',y'
\end{aligned}
$$

と書ける。

---

## 前後の記事

- ⬅️ 前：[[03-CS-theory|3. Chern–Simons 理論]]
- ➡️ 次：[[05-nonabelian-anyon|5. 非可換 anyon]]
