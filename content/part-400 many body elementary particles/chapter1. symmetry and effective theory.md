---
title: chapter1. symmetry and effective theory
date: 2026-05-16
tags:
---
	### §1.1 場の理論の準備

時空の座標を以下のように定義する。

$$x^\mu = (x^0, x^1, \dots, x^d) = (t, \vec{x})$$

時空の次元は $d+1$ 次元である。

#### 1. 古典場の運動方程式

ここではもっとも単純なスカラー場 $\Phi(x)$ を考える。

- **ラグランジアン密度 (Lagrangian density):** $L = L(\Phi, \partial_\mu \Phi)$
    
    - ただし、$\partial_\mu \Phi := (\partial_t \Phi, \nabla \Phi)$
        
- **作用 (Action):**
    
    $$S[\Phi] = \int d^{d+1}x \, L(\Phi, \partial_\mu \Phi)$$
    

古典的な場の方程式（運動方程式：EoM）は作用原理（変分原理）によって決まる。

場の微小変化を $\Phi \rightarrow \Phi + \delta \Phi$ としたとき、作用の変化 $\delta S$ は以下のようになる。

$$\delta S = \int d^{d+1}x \left( \frac{\partial L}{\partial \Phi}\delta \Phi + \frac{\partial L}{\partial (\partial_\mu \Phi)}\delta(\partial_\mu \Phi) \right)$$

$$= \int d^{d+1}x \left[ \left( \frac{\partial L}{\partial \Phi} - \partial_\mu \left( \frac{\partial L}{\partial (\partial_\mu \Phi)} \right) \right)\delta \Phi + \partial_\mu \left( \frac{\partial L}{\partial (\partial_\mu \Phi)}\delta \Phi \right) \right]$$

**仮定:** 空間の無限遠（$x^\mu \rightarrow \infty$）で場がゼロ（$\Phi \rightarrow 0$）に収束すると仮定すると、全微分項である第2項（境界項）は0となる。

**作用原理 ($\delta S = 0$):**

これにより、オイラー・ラグランジュ方程式（運動方程式）が得られる。

$$\frac{\partial L}{\partial \Phi} - \partial_\mu \left( \frac{\partial L}{\partial (\partial_\mu \Phi)} \right) = 0$$

---

#### 2. 量子論の導入と生成汎関数

量子論における、過去（$t = -\infty$）の真空から未来（$t = \infty$）の真空への遷移振幅（真空期待値） $Z$ は、経路積分を用いて以下のように定義される。

$$Z := \langle 0 | 0 \rangle = \int D\Phi e^{i S[\Phi]}$$

※ $D\Phi$ は多様体（$d+1$ 次元多様体 $M_0$）上で定義された場の経路積分の測度。

時間順序積（Time-ordering）を考慮した2点相関関数は以下のように表される。

$$\langle \Phi(x)\Phi(y) \rangle = \frac{1}{Z} \int D\Phi \, \Phi(x)\Phi(y) e^{i S[\Phi]}$$

ここで、外部ソース $J(x)$ を導入した**生成汎関数** $Z[J]$ を定義する。

$$Z[J] = \int D\Phi \exp \left( i \left[ S[\Phi] + \int d^{d+1}x \, J(x)\Phi(x) \right] \right)$$

これを $J(x)$ で機能微分すると、以下の関係が得られる。

$$\frac{\delta Z[J]}{\delta J(x)} = i \int D\Phi \, \Phi(x) \exp \left( i \left[ S[\Phi] + \int d^{d+1}x \, J(x)\Phi(x) \right] \right)$$

これを用いることで、任意の $n$ 点相関関数を生成汎関数の微分によって求めることができる。例えば2点相関関数は次のように求まる。

$$\langle \Phi(x)\Phi(y) \rangle = \frac{(-i)^2}{Z[J]} \frac{\delta^2 Z[J]}{\delta J(x) \delta J(y)} \bigg|_{J=0}$$

---

### §1.2 対称性

「対称性がある」とは、ある変換に対して物理法則（または物理量、作用）が不変であることを意味する。

作用 $S$ に対し、場の変換を次のように導入する。

$$\Phi(x) \rightarrow \Phi'(x') = U \Phi(x)$$

このとき、ラグランジアン密度および作用が全微分項（境界項）の差を除いて不変であるとする。

$$L \rightarrow L' = L + \partial_\mu k^\mu$$

$$S \rightarrow S' = S + \int d^{d+1}x \, \partial_\mu k^\mu$$

この第2項（境界項）は、適当な境界条件（Boundary condition）のもとで消滅する。

- **量子論的な対称性:** 経路積分の測度も含めて変換で不変であるとき「量子論的に対称性がある」と言う。もし古典的に対称性があっても量子論的に破れている場合、それを**アノマリー (Anomaly)** と呼ぶ。
    

#### 1. 内部対称性 (Internal Symmetry)

空間の座標を変えず、場の内部自由度を変換させる対称性。

$$\text{例: } \Phi(x) \rightarrow \Phi'(x) := e^{i\alpha}\Phi(x) \quad (\alpha \in \mathbb{R})$$

- **大域的（グローバル）対称性:** 変換パラメータ $\alpha$ が座標 $x$ に依存しない。
    
- **局所的（ローカル）対称性:** 変換パラメータ $\alpha(x)$ が座標 $x$ に依存する（＝ゲージ対称性）。
    

#### 2. $U(N)$ および $SU(N)$ 変換

複数の場を並べた多成分場に対するユニタリ変換を考える。

$$\Phi_i \rightarrow \Phi'_i = V_{ij}\Phi_j$$

無限小の $U(N)$ 変換は、エルミート行列 $X$（$X = X^\dagger$）を用いて次のように書ける。

$$V(N) = 1_N + i X$$

さらに $\det V = 1$ という条件（$SU(N)$ 変換）を課すと、トレースがゼロ（$\mathrm{Tr}(X) = 0$）となる。これらを満たす独立な生成子は $N^2 - 1$ 個存在する。

$SU(N)$ の生成子を $T_a$ とすると、変換は次のように表される。

$$V_\alpha = e^{i\alpha_a T_a}, \quad U_\beta = e^{i\beta_a T_a}$$

BCH公式（Baker-Campbell-Hausdorff formula）を用いると、これらの積の交換関係から群の演算が閉じることが分かり、生成子は以下の代数（**嘘代数 / リー代数**）を満たす。

$$[T_a, T_b] = i f_{abc} T_c \quad (\text{$f_{abc}$: $SU(N)$ の構造定数})$$

**例: $N=2$ の場合 ($SU(2)$)**

生成子 $T_a$ はパウリ行列 (Pauli matrices) $\sigma_i$ を用いて $T_a = \frac{1}{2}\sigma_a$ と定義される。

$$\sigma_1 = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}, \quad \sigma_2 = \begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix}, \quad \sigma_3 = \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}$$

規格化条件は $\mathrm{Tr}[T_a T_b] = \frac{1}{2}\delta_{ab}$ であり、交換関係は以下となる。

$$[T_a, T_b] = i \epsilon_{abc} T_c \quad (\text{$\epsilon_{abc}$ は完全反対称レヴィ=チヴィタ記号})$$

#### 3. その他の群

- **直交群 $O(N)$:** $O^T O = 1$ を満たす変換。
    
- **ユニタリシンプレクティック群 $USp(2N)$ (または $Sp(N)$):**
    
    $$v^T J v = v, \quad J = \begin{pmatrix} 0 & 1_N \\ -1_N & 0 \end{pmatrix}$$
    

---

### 3. 時空の対称性

#### a. 並進対称性 (Translation Symmetry)

座標の平行移動変換：

$$x^\mu \rightarrow x'^\mu = x^\mu + a^\mu$$

スカラー場は座標の移動によらず同じ値を与えるため、変換後の場は次の関係を満たす。

$$\Phi'(x') = \Phi(x) \quad \rightarrow \quad \Phi'(x) = \Phi(x-a)$$

#### b. ローレンツ対称性 (Lorentz Symmetry)

ミンコフスキー計量を $\eta_{\mu\nu} = \mathrm{diag}(+1, -1, -1, \dots, -1)$ とする。

座標変換 $x^\mu \rightarrow x'^\mu = \Lambda^\mu_{\nu} x^\nu$ において、不変間隔（世界間隔） $x^2 = \eta_{\mu\nu} x^\mu x^\nu = t^2 - \vec{x}^2$ を一定に保つ条件は次式で与えられる。

$$\eta_{\mu\nu} \Lambda^\mu_{\alpha} \Lambda^\nu_{\beta} = \eta_{\alpha\beta}$$

これを満たす変換群がローレンツ群 $O(1, d)$ であり、さらに $\det \Lambda = 1$ の自由度を $SO(1, d)$ と呼ぶ。このうち単位元と連続的につながっている部分（固有時空反転ローレンツ群）を $SO^+(1,d)$ と書く。

スカラー場はローレンツ変換に対して以下のように変換する。

$$\Phi(x) \rightarrow \Phi'(x) = \Phi(\Lambda^{-1}x)$$

#### c. ポアンカレ対称性 (Poincaré Symmetry)

ローレンツ変換と並進変換を合わせた変換。

$$x'^\mu = \Lambda^\mu_{\nu} x^\nu + a^\mu$$

相対論的な場の理論では、作用（Action）および経路積分はポアンカレ不変性（ローレンツ不変性）を保ったまま書き下される。

- **空間回転の例 ($D=3+1$ 次元における $x$ 軸まわりの回転):**
    
    $$\begin{cases} y' = y \cos\theta - z \sin\theta \\ z' = y \sin\theta + z \cos\theta \end{cases}$$
    
- **ローレンツ・ブーストの例 ($x$ 方向へのブースト $\beta$):**
    
    $$\begin{cases} t' = t \cosh\beta + x \sinh\beta \\ x' = t \sinh\beta + x \cosh\beta \end{cases}$$
    

無限小変換において、回転の生成子を $J_i$、ブーストの生成子を $K_i$ とすると、これらは以下の**ローレンツ代数 ($SO(1,3)$)** を構成する。

$$[J_i, J_j] = i \epsilon_{ijk} J_k$$

$$[J_i, K_j] = i \epsilon_{ijk} K_k$$

$$[K_i, K_j] = -i \epsilon_{ijk} J_k$$

---

### §1.3 ネーターの定理 (Nöether's Theorem)

作用の連続的な対称性に対して、古典論のレベルで対応する保存電流（保存則）が存在する。

いま、連続群の無限小変換の下で作用が不変であるとする。ここで、大域的な対称性のパラメータ $\alpha$ をあえて座標に依存する局所的なもの（$\alpha(x)$）へと引き上げる。このとき、作用の微小変化 $\delta S$ はパラメータの微分項を用いて次のように書ける。

$$\delta S = \int d^{d+1}x \, j^\mu(x) \partial_\mu \alpha(x)$$

もし $\alpha = \mathrm{const}$（大域的変換）であれば、対称性の仮定より $\delta S = 0$ となる。

局所的な変化に対して部分積分を施すと、

$$\delta S = - \int d^{d+1}x \, (\partial_\mu j^\mu) \alpha(x)$$

運動方程式（EoM）が満たされている（$\delta S = 0$）とき、任意の $\alpha(x)$ に対してこれが成立するため、次の保存則が得られる。

$$\partial_\mu j^\mu = 0 \quad (\text{$j^\mu$ はネーター電流: Noether current})$$

#### 具体的な電流の導出

実際に作用の変分を計算すると、

$$\delta S = \int d^{d+1}x \left[ \left( \frac{\partial L}{\partial \Phi} - \partial_\mu \left( \frac{\partial L}{\partial (\partial_\mu \Phi)} \right) \right)\delta \Phi + \partial_\mu \left( \frac{\partial L}{\partial (\partial_\mu \Phi)}\delta \Phi \right) \right]$$

第1項は運動方程式（Euler-Lagrange eq.）によって消えるため、変化は全微分項のみとなる。

一般に、変換によってラグランジアン密度が全微分 $\delta L = \partial_\mu K^\mu$ と変化する場合、ネーター電流は以下のように定義される。

$$j^\mu = \frac{\partial L}{\partial (\partial_\mu \Phi)} \delta \Phi - K^\mu$$

この電流から、時間成分を空間積分することで**保存電荷 (Noether charge)** $Q$ が定義される。

$$Q := \int d^d x \, j^0(x)$$

電荷の時間変化は次のようにゼロになる（空間無限遠で電流が $0$ になる境界条件を適用）。

$$\frac{dQ}{dt} = \int d^d x \, \partial_0 j^0 = \int d^d x (\partial_\mu j^\mu - \nabla \cdot \vec{j}) = -\int \vec{j} \cdot d\vec{S} = 0$$

---

### エネルギー・運動量テンソル

作用が時空の並進対称性を持つ場合を考える。

場の微小変化およびラグランジアン密度の変化はそれぞれ以下のようになる。

$$\delta \Phi = -a^\nu \partial^\nu \Phi$$

$$\delta L = -a^\mu \partial_\mu L = \partial_\mu (-a^\mu L)$$

これに対応するネーター電流を求めると、パラメータ $a^\nu$ を除いて次のテンソルが導かれる。

$$T^{\mu\nu} = \frac{\partial L}{\partial (\partial_\mu \Phi)} \partial^\nu \Phi - \eta^{\mu\nu} L$$

これを**正準エネルギー・運動量テンソル**と呼び、以下の保存則を満たす。

$$\partial_\mu T^{\mu\nu} = 0$$

一般に、正準エネルギー・運動量テンソル $T^{\mu\nu}$ は対称テンソルになるとは限らない。しかし、理論がローレンツ不変性を持つ場合、適当な反対称テンソルを用いて、

$$\Theta^{\mu\nu} = T^{\mu\nu} + \partial_\lambda \Sigma^{\mu\nu\lambda} \quad (\text{Belinfante テンソル})$$

を導入することで、対称（$\Theta^{\mu\nu} = \Theta^{\nu\mu}$）かつ保存則（$\partial_\mu \Theta^{\mu\nu} = 0$）を満たすエネルギー・運動量テンソルを構成することができる。