---

title: 2.非可換 anyon の例：FQH
date: 2025-12-27
tags:

    - anyon
    - FQH

---

2 次元 $xy$ 平面上の電子ガスを考える[^gas]。電場を $y$ 方向、磁場を $z$ 方向にかける。このとき $x$ 方向に電流 $J_y$ が流れるというのが量子 Hall 効果である。$J_y$ は

$$
\begin{aligned}
J_y = \sigma_{xy} E_x
\end{aligned}
$$

と書ける。ここで $\sigma_{xy}$ は Hall 伝導度であり、磁場の強さに応じて量子化される。FQH では、統計パラメータ $\nu=1/2, 2/3, 1/5,\dots$ に応じて分数量子化することが知られている。

この FQH のトポロジカル秩序相（Topological Ordered Phase）の特徴として、分数統計性をもつ anyon が存在する。anyon は大きく可換（Abelian）と非可換（Non-Abelian）に分けられる。

## 可換 anyon

可換 anyon とは、2 粒子の交換で一定の位相を得る粒子であり、場の演算子 $\Psi_1,\Psi_2$ が

$$
\begin{aligned}
\Psi_1 \Psi_2 = e^{i\theta}\Psi_2 \Psi_1
\end{aligned}
$$

を $\theta \neq 0,\pi$ で満たすようなものを指す。たとえば統計パラメータ $\nu=1/3$ の FQH 状態は $\theta=2\pi/3$ の anyon になる。

また、このような交換を説明するのに Fusion 則（Fusion rule）がある。たとえば

$$
\begin{aligned}
[e/3]\times [e/3] = [2e/3]
\end{aligned}
$$

のように書く（※ここは要整理）。

## 非可換 anyon

Fusion 則で右辺に 2 種類以上が出てくるとき非可換 anyon である（※なぜそう言えるかは後で補足する）。

例を二つ挙げる。

### 例 1：Ising anyon

Ising anyon は

$$
\begin{aligned}
\sigma \times \sigma = I + \psi
\end{aligned}
$$

を満たす。

1+1d の transverse field Ising 模型を使うと直観が得られる。Hamiltonian は

$$
\begin{aligned}
\hat{H} =
-J \sum_{\langle i,j \rangle} \hat{\sigma}_i^z \hat{\sigma}_j^z
-h \sum_i \hat{\sigma}_i^x .
\end{aligned}
$$

ここで $\sigma_i^\alpha$ は $i$ 番目のスピンの $\alpha$ 成分。

* $J>h$：SSB 相（up/down にそろう）
* $J<h$：スピンは $x$ 軸方向にそろう

空間を 3 つの領域に分け、右左が $J>h$、中央が $J<h$（領域を R,C,L）とする。C を縮めていく操作で Fusion を直観的に説明できる：

* $I$：R,L が up、C が横向き → C を縮めると全領域 up（恒等に対応）
* $\psi$：R が up、L が down、C が横向き → C を縮めると up/down 境界（kink 励起）→ $\psi$（Majorana fermion）に対応

実際の分数量子ホールでは、(2+1)d の Moore–Read 状態や $p+ip$ トポロジカル超伝導体の vortex がこの Fusion 則を満たすことが知られている。

### 例 2：Fibonacci anyon

Fibonacci anyon は

$$
\begin{aligned}
\tau \times \tau = I + \tau
\end{aligned}
$$

を満たす。Fibonacci anyon は $\pi/4$ 位相演算子を作れるため、任意のユニタリ演算が生成でき、量子計算への応用が期待されている。

実験的には、Weizmann などで $[e/3]$ 状態が shot noise により観測されている（要文献整理）。shot noise は電流の微小なゆらぎを観測し、有効電荷 $e^*$ と結びつく：

$$
\begin{aligned}
\left.
\frac{\int_{-\infty}^{\infty} dt, e^{-i\omega t},\langle I_i(t), I_j(t)\rangle}{2I}
\right|_{\omega\to 0}
= e^* .
\end{aligned}
$$

$\nu=1/3$ では $e^*=e/3$ が観測されている。なお shot noise は電荷を運ばない量（熱、conformal weight など）でも考えられる。

[^gas]: 「ガス」は気体という意味ではなく、結晶のような周期ポテンシャルをもたない自由な系を指す。

---

## 前後の記事

- ⬅️ 前：[[01-intro|1. はじめに]]
- ➡️ 次：[[03-CS-theory|3. Chern–Simons（CS）理論]]
