---
title: 04.量子化
date: 2025-12-27
tags:
  - anyon
---

## 同種粒子系の量子力学的扱い

同種粒子系のSchrodinger方程式を立てる際に、特異点で波動関数はどうあるべきか？という境界条件を考えるだけで、統計性は決まってしまうことを見る。

[[03-Identical-particles-in-QM|03.量子力学における同種粒子]]の内容を既知とする。

### 1次元の場合
- 状況設定
空間は半平面($x_1 \geq x_2$)である。
特異点は$z = |x_1 - x_2| = 0$である。
Hamiltonianは自由粒子とする:
$$
\begin{equation}
  H = -\frac{\hbar^2}{2m}(\frac{\partial^2}{\partial x_1^2} + \frac{\partial^2}{\partial x_2^2}) = -\frac{\hbar^2}{4m}\frac{\partial^2}{\partial x^2} - \frac{\hbar^2}{m}\frac{\partial^2}{\partial z^2}
\end{equation}
$$
ただし、$m$は粒子の質量であり、重心座標 $x=\frac{x_1+x_2}{2}$ と相対座標 $z= |x_1 - x_2|$ を用いた。

- 境界条件
通常、粒子が壁に閉じ込められている際は、壁で波動関数 $\psi(x,z)$ は0になるとするが、物理的に必要なのは、粒子が壁を通り抜けられないことである。
よって、確率流の法線成分が$z=0$で0になることが必要である:
$$
\begin{equation}
  \psi^*(x,0)\frac{\partial \psi}{\partial z}(x,0) - \psi(x,0)\frac{\partial \psi^*}{\partial z}(x,0) = 0
\end{equation}
$$
これが任意の$x$に対して成立すればよく、解くと、パラメータ$\eta \in \mathbb{R}$を用いて
$$
\begin{equation}
  \frac{\partial \psi}{\partial z}(x,0) = \eta \psi(x,0)
\end{equation}
$$
となる。

重ね合わせの原理から、$\eta$は波動関数と独立でなければならない。

> [!info] 補足: 
> 異なる波動関数$\psi_1,\psi_2$に対して異なる$\eta_1,\eta_2$を持つとすると、線形結合$\psi_1 + \psi_2$に対して
> $$
>\begin{equation}
>  \frac{\partial}{\partial z}(\psi_1 + \psi_2)(x,0) = \eta_1 \psi_1(x,0) + \eta_2 \psi_2(x,0)
>\end{equation}
>$$
>となるが、これも同じ境界条件を満たす必要がある。
> よって、$\eta_1 = \eta_2$でなければならない。

この$\eta$が統計性を定める。
- 統計性

---
## 前後の記事

📚 目次：[[content/part-01-quantum-hall/index|量子 Hall 効果とエニオン]]  
次 →：[[01-quantum-hall|量子 Hall 効果]]
