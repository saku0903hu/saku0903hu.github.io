---

title: 01.Landau準位
date: 2025-12-27
tags:

    - 2dsystem

---

# Landau 準位

磁場 $B\hat{z}$ 中の 2 次元平面内の自由電子の Hamiltonian は

$$
H=\frac{1}{2m}\boldsymbol{\pi}^2,
\qquad
\boldsymbol{\pi}=\boldsymbol{p}-e\boldsymbol{A}
$$

である。動的運動量は

$$
[\pi_x,\pi_y]=-\frac{i\hbar^2}{l^2},
\qquad
l=\sqrt{\frac{\hbar}{eB}}
$$

を満たす。$l$ は磁気長（magnetic length）である。

## 中心座標演算子

正準変換として中心座標演算子 $(X,Y)$ を

$$
\boldsymbol{r}=
\left(
X+\frac{l^2}{\hbar}\pi_y,;
Y-\frac{l^2}{\hbar}\pi_x
\right)
$$

で定義する。このとき

$$
[X,Y]=il^2
$$

が成り立つ。

## 昇降演算子

動的運動量に対して

$$
\begin{aligned}
a &= \frac{l}{\sqrt{2}\hbar}(\pi_x-i\pi_y), \
a^\dagger &= \frac{l}{\sqrt{2}\hbar}(\pi_x+i\pi_y)
\end{aligned}
$$

と定義すると Hamiltonian は

$$
H=\hbar\omega_c\left(a^\dagger a+\frac{1}{2}\right)
$$

となり、エネルギー準位が離散化する。これを Landau 準位と呼ぶ。

以下では対称ゲージ

$$
\boldsymbol{A}=(-By/2,;Bx/2,;0)
$$

を用いる。

## 中心座標の自由度

中心座標に対しても昇降演算子を

$$
\begin{aligned}
b &= \frac{1}{\sqrt{2}l}(X-iY), \
b^\dagger &= \frac{1}{\sqrt{2}l}(X+iY)
\end{aligned}
$$

と定義する。角運動量演算子は

$$
L_z=\hbar(a^\dagger a-b^\dagger b)
$$

となる。

---

## 前後の記事

📚 目次：[[index|量子 Hall 効果とエニオン]]  
次 →：[[02-quantum-hall|量子 Hall 効果]]
