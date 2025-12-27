---

title: 3.Chern–Simons（CS）理論
date: 2025-12-27
tags:

  - Chern-Simons
  - FQH

---

## Chern–Simons 理論の作用と Particle–Vortex duality

FQH は根本的に多体問題であるのにも関わらず、Laughlin 波動関数のようなきれいな波動関数が知られている。そこで低エネルギー有効理論として、トポロジカルな性質を取り出す Chern–Simons 理論が用いられる。

以下、(2+1)d とし、外場（ベクトルポテンシャル）を $A_\mu;(\mu=t,x,y)$ とする。Chern–Simons 作用は

$$
\begin{aligned}
S = \frac{1}{4\pi}\int d^3x, \epsilon^{\mu\nu\rho} A_\mu \partial_\nu A_\rho .
\end{aligned}
$$

カレントを $J^\mu=\delta S/\delta A_\mu$ と定義すると

$$
\begin{aligned}
J^\mu
= \frac{1}{2\pi}\epsilon^{\mu\nu\rho}\partial_\nu A_\rho
\end{aligned}
$$

（※添字の整合は要チェック。元文の $A_\nu\partial_\rho A_\sigma$ はたぶん誤記）となり、Hall 応答が再現される。

次に $A_\mu$ と電流源 $J_\mu$ の結合を入れて

$$
\begin{aligned}
S
=

\frac{1}{4\pi}\int d^3x, \epsilon^{\mu\nu\rho} A_\mu \partial_\nu A_\rho

* \int d^3x, J_\mu A^\mu
  \end{aligned}
  $$

を考える。ここで $J_\mu$ は本来保存電流 $\partial_\mu J^\mu=0$ を満たすべきなので、Particle–Vortex duality を導入する。

> [!info] Def. Particle–Vortex duality
> $$
> \begin{aligned}
> J^\mu = \frac{1}{2\pi}\epsilon^{\mu\nu\rho}\partial_\nu a_\rho
> \end{aligned}
> $$
> ここで $a_\mu$ は “emergent” な $U(1)$ ゲージ場（Chern–Simons ゲージ場）。

このとき密度 $\rho$ と vortex（磁束密度）$b=\nabla\times \mathbf{a}$ の関係は

$$
\begin{aligned}
\rho = \frac{b}{2\pi}
\end{aligned}
$$

となる。

さらに内部自由度の CS 項 $\frac{k}{4\pi}\int a,da$ を追加し、微分形式の略記（$A\wedge dA$ を $AdA$ と書く等）を使うと

$$
\begin{aligned}
S
=

\int\left(
\frac{1}{4\pi}AdA

* \frac{1}{2\pi}Ada
* \frac{k}{4\pi}ada
  \right)
  \end{aligned}
  $$

となる。$k$ をレベルと呼ぶ。

## CS ゲージ場の運動方程式

変分から

$$
\begin{aligned}
da = -\frac{1}{k}dA
\end{aligned}
$$

が得られ、P–V duality を用いて応答電流は

$$
\begin{aligned}
J^\mu
=====

-\frac{1}{2\pi k}\epsilon^{\mu\nu\rho}\partial_\nu A_\rho
\end{aligned}
$$

と書ける。よって有効的に $\nu=1/k$ の FQH を記述している。

## CS ゲージ場の量子化

$A=0$ とすると

$$
\begin{aligned}
S = \frac{k}{4\pi}\int a,da
= \int d^3x,\frac{k}{4\pi}\epsilon^{\mu\nu\rho}a_\mu\partial_\nu a_\rho .
\end{aligned}
$$

この作用には $a_x\partial_t a_y$ 型の項が含まれ、正準交換関係を導入できると考えられる：

$$
\begin{aligned}
[a_x(\mathbf{x}),a_y(\mathbf{x}')]
==================================

\frac{2\pi i}{k}\delta(\mathbf{x}-\mathbf{x}').
\end{aligned}
$$

## トーラス上のゲージ不変量：Wilson loop

> [!info] Def. Wilson loop
> 穴を囲むループを $C_1$、チューブ断面を囲むループを $C_2$ とすると、
> $$
> \begin{aligned}
> W_1=e^{i\oint_{C_1}a},\qquad
> W_2=e^{i\oint_{C_2}a}
> \end{aligned}
> $$
> を Wilson loop と呼ぶ。

$C_1(C_2)$ を $x(y)$ 方向とみると、交差により

$$
\begin{aligned}
W_1W_2 = e^{2\pi i/k}W_2W_1
\end{aligned}
$$

となり、分数統計が現れる。

基底状態の縮退（GSD）を見るために、$W_1$ の固有基底 ${|n\rangle}$ を

$$
\begin{aligned}
W_1|n\rangle = e^{2\pi i n/k}|n\rangle
\end{aligned}
$$

とおくと、$W_2$ は

$$
\begin{aligned}
W_2|n\rangle = |n+1\rangle
\end{aligned}
$$

を満たす（導出は元の議論のまま）。したがって $n=0,\dots,k-1$ が必要で、GSD は $k$。

## 複数階層 CS 理論と K 行列

階層を 1 段増やすと

$$
\begin{aligned}
S
=

\int\left(
\frac{1}{4\pi}AdA

* \frac{1}{2\pi}Ada
* \frac{k}{4\pi}ada
* \frac{1}{2\pi}adb
* \frac{k'}{4\pi}bdb
  \right)
  \end{aligned}
  $$

となり、応答は

$$
\begin{aligned}
J^\mu
=====

-\frac{1}{2\pi}\frac{1}{k-\frac{1}{k'}}
\epsilon^{\mu\nu\rho}\partial_\nu A_\rho .
\end{aligned}
$$

$A=0$ では

$$
\begin{aligned}
a_I=
\begin{pmatrix}
a\ b
\end{pmatrix},\qquad
K_{IJ}=
\begin{pmatrix}
k & 1\
1 & k'
\end{pmatrix}
\end{aligned}
$$

として

$$
\begin{aligned}
S=\frac{1}{4\pi}\int K_{IJ}a_I,da_J
\end{aligned}
$$

とまとめられる。

> [!info] Def. Smith Normal Form（SNF）
> 行・列の基本変形（行列式 1 の変換）で整数行列を対角化していく標準形。

例：$k=1,k'=-2$ のとき $\nu=2/3$ を記述する、など。

さらに外場の probe として $t_I$ を入れると

$$
\begin{aligned}
\nu = t^{\mathsf{T}}K^{-1}t
\end{aligned}
$$

で一般に占有率が書ける。

---

## 前後の記事

- ⬅️ 前：[[02-nonabelian-fqh|2. 非可換 anyon の例：FQH]]
- ➡️ 次：[[04-boundary-CS|4. 境界あり Chern–Simons 理論]]
