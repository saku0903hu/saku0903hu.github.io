---

title: 01.Landau準位
date: 2025-12-27
tags:

    - 2dsystem
    - FQH
    - IQH

---

# 量子力学による電子の運動
磁場 $\boldsymbol{B}$ 中の自由電子のHamiltonianは

$$
H= \frac{1}{2m_e}(\boldsymbol{p}-e\boldsymbol{A})^2 -g \mu_B sB
$$

で与えられる。ここで $\boldsymbol{A}$ はベクトルポテンシャルであり、$\boldsymbol{B}=\nabla\times\boldsymbol{A}$ を満たす。
また、$\boldsymbol{p}$は正準運動量で交換関係

$$
[p_\alpha, r_\beta] = -i\hbar \delta_{\alpha,\beta} \quad \alpha,\beta = x,y,z
$$
を満たす。

$g$ は電子の$g$因子($g$-factor)、$\mu_B$ はBohr磁子、$s$ はスピン量子数である。

以下では電子の軌道運動に注目し、スピン項を無視する。

## 運動量演算子、角運動量演算子
磁場中では正準運動量演算子 $\boldsymbol{\pi}$ と速度演算子 $\boldsymbol{v}$ は異なる。

> [!info] 定義: 速度演算子
>$$
>\boldsymbol{v} \coloneqq \frac{i}{\hbar} [H, \boldsymbol{r}] = \frac{1}{m_e}(\boldsymbol{p}-e\boldsymbol{A})
>$$

これを用いて、動的運動量(dynamical momentum)演算子 $\boldsymbol{\pi}$ を定義できる。

> [!info] 定義: 動的運動量演算子
>$$
>\boldsymbol{\pi} \coloneqq m_e \boldsymbol{v} = \boldsymbol{p}-e\boldsymbol{A}
>$$ 
動的運動量演算子は交換関係
$$
[\pi_\alpha, \pi_\beta] = -i\hbar e \epsilon_{\alpha\beta\gamma} B_\gamma = -i \frac{\hbar^2}{l^2} \epsilon_{\alpha\beta\gamma} B_\gamma 
$$
を満たす。

ここで、$l = \sqrt{\frac{\hbar}{eB}}$ は磁気長(magnetic length)あるいはLarmor半径と呼ばれる。

## 並進演算子の生成演算子
ゼロ磁場の場合、運動量演算子は並進運動の生成演算子である。
一様な磁場中は並進対称性があるため、対応する生成演算子が存在し、それはHamiltonianと交換するものである。

> [!info] 定義: 磁場中の並進演算子の生成演算子:擬運動量(pseudomomentum)$\boldsymbol{K}$
> $$
>\boldsymbol{K} = \boldsymbol{\pi} + e \boldsymbol{B} \times \boldsymbol{r} 
>$$
> この演算子は Hamiltonian と交換する。

距離$\boldsymbol{\delta}$だけの並進演算子は
$$
t(\boldsymbol{\delta}) = e^{-\frac{i}{\hbar} \boldsymbol{\delta} \cdot \boldsymbol{K}}
$$
となる。

# Landau 準位

$z$方向に磁場をかける。
磁場は

$\boldsymbol{B}=(0,0,B)$

である。
磁場中の2次元平面内の自由電子の Hamiltonian は

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
次 →：[[01-quantum-hall|量子 Hall 効果]]
