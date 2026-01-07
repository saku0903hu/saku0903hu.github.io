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
  H = -\frac{\hbar^2}{2m}\left(\frac{\partial^2}{\partial x_1^2} + \frac{\partial^2}{\partial x_2^2}\right) = -\frac{\hbar^2}{4m}\frac{\partial^2}{\partial x^2} - \frac{\hbar^2}{m}\frac{\partial^2}{\partial z^2}
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

また、並進対称性から、$\eta$は$x$(重心座標)に依存しない。
いま、空間は一様であるから衝突の性質は位置によらないためである。

この$\eta$が系の固有の性質を決め、粒子の統計性を定める。

 - Boson系は $\eta = 0$ (微分が0)
 - Fermion系は $\eta = \infty$ (波動関数が0)

となるが、この中間の値の$\eta$も許され[^1]、この領域の粒子はbosonでもfermionでもない粒子に対応し、これを**anyon**と呼ぶ[^2]: 。
[^1]: 超選択則があるらしい。
[^2]: この論文ではanyonという用語は使われていない。

(1)の固有関数は
$$
\begin{equation}
  \psi_{k,\kappa} (x,z) = \exp(i\kappa x)\left( \cos(kz)+\frac{\eta}{k}\sin(kz)\right)
\end{equation}
$$
となる。
ただし、$k$は相対運動の波数、$\kappa$は重心運動の波数である。
三角関数の部分は
$$
\begin{equation}
  \sqrt{1+\left(\frac{\eta}{k}\right)^2} \cos(kz - \delta_k)
\end{equation}
$$
となり、$z=0$ で反射した波の位相が $\delta_k$ だけずれることがわかる。
把捉としてみると、反射にかかる時間の遅れ(time shift)
$$
\begin{equation}
  \tau = \frac{m\eta}{\hbar k (k^2 + \eta^2)}
\end{equation}
$$
があることがわかり、これはboson,fermionの場合は0である。

---
## 前後の記事

📚 目次：[[content/part-01-quantum-hall/index|量子 Hall 効果とエニオン]]  
次 →：[[01-quantum-hall|量子 Hall 効果]]
