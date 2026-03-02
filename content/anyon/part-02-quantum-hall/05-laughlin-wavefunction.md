---

title: 05.Laughlinの波動関数
date: 2025-12-27
tags:

    - fqh

---

# Laughlin 波動関数

分数量子 Hall 状態を記述する代表的な波動関数が Laughlin 波動関数である。

## 一電子状態

最低 Landau 準位における一電子波動関数は

$$
\phi(\boldsymbol{r})=f(z)e^{-|z|^2/4}
$$

と書ける。
ここで

$$
z=\frac{x-iy}{l}
$$

は複素座標であり、$f(z)$ は正則多項式である。

## 多電子波動関数

$N_e$ 電子系では

$$
\Psi(z_1,\dots,z_{N_e})
=f(z_1,\dots,z_{N_e})e^{-\sum_i|z_i|^2/4}
$$

となる。
Coulomb 相互作用のみを考えると

$$
f(z_1,\dots,z_{N_e})
=\prod_{i<j}(z_i-z_j)^q
$$

であり、$q$ は奇数である。

## Laughlin 波動関数

以上より

$$
\Psi_q(z_1,\dots,z_{N_e})
=\prod_{i<j}(z_i-z_j)^q e^{-\sum_i|z_i|^2/4}
$$

を Laughlin 波動関数と呼ぶ。

熱力学極限では占有率は

$$
\nu=\frac{1}{q}
$$

となる。
