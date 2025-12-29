---

title: 05.Laughlinの波動関数
date: 2025-12-27
tags:
    - fqh
    - Laughlin
---

# Laughlin 波動関数

分数量子 Hall 状態を記述する代表的な波動関数のとしてLaughlin波動関数がある。

Laughlinによる試行関数の考え方を示す。

まず強磁場極限を考える。
強磁場極限においては、Landau準位間のエネルギーが十分大きく、準位間の遷移がないとみて、全ての電子が最低 Landau 準位に存在すると仮定する。

## 一電子状態
[[01-landau-levels|最低 Landau 準位]]における一電子波動関数は
$$
\begin{equation}
  \phi(\boldsymbol{r})=f(z)e^{-|z|^2/4}
\end{equation}
$$
と書けるとわかっている。
ここで
$$
\begin{equation}
z=\frac{x-iy}{l}
\end{equation}
$$
は複素座標であり、$f(z)$ は正則多項式である。

## 多電子波動関数

$N_e$ 電子系は、1電子波動関数から作られるSlater行列式の線形結合としてかけるので、一般に
$$
\begin{equation}
\Psi(z_1,\dots,z_{N_e})
=f(z_1,\dots,z_{N_e})e^{-\sum_i|z_i|^2/4}
\end{equation}
$$
となる。

ここで、$f(z_1,\dots,z_{N_e})$ は正則関数であるから $f(z_1,\dots,z_{N_e}) = a\prod_{i=1}^{N_e} $と書ける。

これは$i$番目の電子が角運動量$m_i \hbar$を持つ状態にいることを表している。

> [!proof] 証明
> $L_z$を$z,\bar{z}$を用いて書き換えると、 
> $$
>\begin{equation}
>  L_z = \frac{1}{l}\hbar(z \frac{\partial}{\partial z} - \bar{z} \frac{\partial}{\partial \bar{z}})
>\end{equation}
>$$
>となるから、$f(z)$が正則関数であることから、$L_z f(z) = \hbar z \frac{\partial}{\partial z} f(z)$となり、$f(z)=z^m$のとき、$m\hbar$が固有値となることがわかる。
> □

今、Coulomb 相互作用のみを考えているので、系の全角運動量$M=\sum_i m_i$は保存量であり、Hamiltonianの固有状態は$M$の固有状態に選べる。
よって、今考えている試行関数において、全ての項(全ての状態に対応する波動関数)が共通の全角運動量$M$を持つように選ぶ。
また、電子はフェルミ粒子であるので、波動関数は反対称でなければならない。

ここまでの議論は強磁場極限以外は一般的であり、励起状態を含む全ての固有状態が満たす性質であり、相互作用の様子にも依存しない。

次に、相互作用を入れる。
近距離で強い斥力相互作用であるという情報は、任意の2つの電子が近づく時に波動関数の値が小さくなることで反映できる。
この条件を満たす最も簡単な正則関数は
$$
\begin{equation}
f(z_1,\dots,z_{N_e})
=\prod_{i>j}(z_i-z_j)^q
\end{equation}
$$
であり、$q$ は奇数である。

この時、2体の相関のみを取り入れる波動関数は**Jastrow型波動関数**と呼ばれる。

以上より

$$
\begin{equation}
\Psi_q(z_1,\dots,z_{N_e})
=\prod_{i<j}(z_i-z_j)^q e^{-\sum_i|z_i|^2/4}
\end{equation}
$$
が得られる。
これをLaughlin波動関数と呼ぶ。

熱力学極限では占有率は

$$
\begin{equation}
\nu=\frac{1}{q}
\end{equation}
$$

となる。

---

## Laughlin波動関数の零点
Laughlin波動関数の特徴は零点にの分布に現れる。

$q=3,\nu=1/3$の場合を見ていく。

この時、波動関数の式
$$
\begin{equation}
  \Psi_q(z_1,\dots,z_{N_e})
=\prod_{i<j}(z_i-z_j)^3 e^{-\sum_i|z_i|^2/4}
\end{equation}
$$
がゼロになるのは、任意の2つの電子が同じ位置に来たときであり、その零点の次数は3である。
よって、その近傍では電子の距離の6条に比例して確率は小さくなる。

Laughlin波動関数は(ほとんど最大に)Coulomb相互作用を得するように設計されていることを見る。

これを理解するため、Laughlin状態ではないが占有率は同じ状態と比較してみる。

電子数$N_e$の系において、$\nu=1/3$の状態は角運動量が0から$M\hbar = 3(N_e-1)$までの状態に電子が入っていることになる。

このような一般の波動関数を
$$
\begin{equation}
  \Phi = f(z_1,\dots,z_{N_e})\exp \left( -\sum_i \frac{|z_i|^2}{4}\right)
\end{equation}
$$
と書くと、$f(z_1,\dots,z_{N_e})$は各$z_i$について最大で$M$次の多項式である($M$個の零点を持つ)ことがわかっている。

Pauliの排他原理より$f$は反対称性があるから、任意の2つの電子の座標が一致するとき波動関数は0になるため、任意の$i,j$について$\prod_{i>j} (z_i-z_j)$を因子に持つ。

よって、$f(z_1,\dots,z_{N_e})$を特定の$z_i$の関数として見ると
$N_e-1$個の零点は電子の位置が一致しているときに現れ、他の$2(N_e-1)$個の零点はどこにあってもよい。

一方、Laughlin波動関数の零点は、任意の2つの電子の位置が一致するときのみに存在していたから、より一般の波動関数の場合は電子同士が接近する確率が上がり、Coulomb相互作用を強く受ける。
また、零点と離れた位置に電子がある場合、零点付近の電子密度が低下し正の電荷密度が上がるため、Coulombエネルギーが上がる。

よって、一般の場合は2重でCoulombエネルギーが上がることになる。
Laughlin波動関数は、Coulomb相互作用を最もよく避けるように設計された波動関数であることがわかる。