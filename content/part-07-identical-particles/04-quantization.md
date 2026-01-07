---
title: 04.量子化
date: 2025-12-27
tags:
  - anyon
---

# 同種粒子系の量子力学的扱い

同種粒子系のSchrodinger方程式を立てる際に、特異点で波動関数はどうあるべきか？という境界条件を考えるだけで、統計性は決まってしまうことを見る。

[[03-Identical-particles-in-QM|03.量子力学における同種粒子]]の内容を既知とする。

まず、スピンなどの内部自由度を無視し、空間的な波動関数のみで状態が決まっているとする。



## 1次元の場合
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

また、$\eta < 0$ の場合、上の解に加えて
$$
\begin{equation}
  \psi_\kappa^{(\eta)}(x,z) = \exp(i\kappa x)\frac{1}{2|\eta|} \exp(\eta z)
\end{equation}
$$
という解も存在する。
これは $z$ に対して指数関数的に減衰する解であり、2粒子が近づいたときに束縛状態を作る。
つまり、$\eta < 0$ のanyon系は粒子間にデルタ関数的な引力ポテンシャルがあるとみなせる。

## 2次元,3次元の場合:準備

1次元の時は境界(壁)での反射を見れば十分だった。
しかし、2次元,3次元の場合、特異点は点であり、壁ではない。
これをうまく定式化するため、波動関数を再定義する[^1]。

[^1]:これは1次元の状態と一致することを確認するべきだと思う。 

> [!info] (多分ラフな)定義: 局所Hilbert空間　$h_x$
>空間の各点$x$に対して、1次元複素ベクトル空間 $h_x$があるとする。(数学的にはファイバーバンドルと呼ばれる。)

> [!info] (多分ラフな)定義: 状態ベクトル $\Psi(x)$
>状態はこの空間上の場 $\Psi(x) \in h_x$であるとする。(数学的には切断(section)と呼ばれる。)

> [!info] (ラフな)定義: 波動関数
> 各点$x$において $h_x$ の基底 $\chi_x$ を取ると、状態ベクトルは
> $$
> \begin{equation}
>   \Psi(x) = \psi(x)\chi_x
> \end{equation}
> $$
> と書ける。
> このとき、$\psi(x)$を波動関数と呼ぶ。

状態は複素スカラーの波動関数のみで指定できるため、変わらずHilbert空間は1次元である。
規格化された基底(ゲージと呼ぶ)の選び方を変えると、波動関数の位相が変わる。
これを(第2種の?)ゲージ変換という。

空間が曲がっていたり、特異点がある時、ある点のベクトルを近くの点に比較することを考える。

点$x$のベクトルと点$x + dx$のベクトルは所属する空間が異なるため、直接比較できない。
そこで、点$x$のベクトルを点$x + dx$の空間に移動させる操作を考える。
この操作を**平行移動** (parallel transport) $P(x+dx,x)$と呼び、次の関係を満たす:
$$
\begin{equation}
  P(x+dx,x) \chi_x = (1+i \,dx^k \, b_k(x)) \chi_{x+dx}
\end{equation}
$$

> [!info] 定義: 並行移動演算子
> $$
>\begin{equation}
>  P(x',x) : h_x \to h_{x'}
>\end{equation}
>$$
>は線形であり、$h_x$のベクトルを、連続的に$x$から$x'$まで移動させる演算子である[^3]。

[^3]: 並行移動の仕方にはさまざまな移動の方法があるが、ここでは一意に存在すると仮定する。


ゲージの選び方の自由度があるため、ゲージ不変な微分があると嬉しい。

> [!info] 定義: 共変微分(Covariant derivative)
> ゲージ不変な微分として
> $$
>\begin{equation}
>  D_k = \frac{\partial}{\partial x_k} - i b_k(x)
>\end{equation}
>$$
> と定義する。

ここで、$b_k(x)$は**ゲージ場** ( 数学的には接続 connection )と呼ばれ、系のダイナミクスやゲージの選び方に依存する量である。

$b_k(x)$を実に取った時、定義より、$P(x+dx,x)$はユニタリである。

ゲージ場$b_k(x)$を用いて、場の強さを定義する。

> [!info] 定義: 場の強さ
> 反対称テンソル
> $$
>\begin{equation}
>  f_{kl} = i[D_k, D_l] = \frac{\partial b_l}{\partial x_k} - \frac{\partial b_k}{\partial x_l}
>\end{equation}
>$$
> と定義する。(数学的には曲率 curvature と呼ばれる。)

電磁場中のハミルトニアンを思い出すと、接続はベクトルポテンシャルに対応しており、場の強さは磁場に対応していることがわかる。

ここでは、$f_{kl}$が定義されない原点以外では場の強さが0であるとする。

では、**特異点の周りを1周する経路**に沿って状態ベクトルを平行移動させたとき、状態ベクトルはどう変化するかを考える。

$P_x$を、点 $x$ から $x$ まで特異点の周りを1周する経路に沿って状態ベクトルを平行移動させる作用素とする。
$P_x$ は $h_x$ から $h_x$ への線形でユニタリな作用素である。

特異点の周りを1周する経路に沿って状態ベクトルを平行移動させることを$m$回繰り返すと、$P^m_x \Psi$ となる。



Hilbert空間が1次元なので、$P_x$は位相因子で表される:
$$
\begin{equation}
  P_x = e^{i\xi}
\end{equation}
$$
である。

$P_x$はスカラーだから、並行移動の演算子と可換で
$$
\begin{equation}
  P_{x'} = P(x',x) P_x P(x,x')^{-1} = e^{i\xi}
\end{equation}
$$
より、位相因子は点$x$に依存しない、2粒子系を特徴付けるパラメータである。

## ゲージ変換
ゲージ場 $b_k(x)$ を通した物理の記述には自由度がある。

### 特異ゲージの方法
$D_k$ の定義より、$b_k(x)$ は $D_k$ を通じてダイナミクスに影響を与えることがわかる。
しかし、今の場合、物理的な力が0であるため、基底の選び方を変えることで、見かけ上のポテンシャル $b_k(x)$ を0に変えることができる。

では、その方法を与える。
ある任意の点$x_0$での基底ベクトル $\chi_x$ を与える。
他の全ての点での基底ベクトルを、点$x_0$からの並行移動で定義する。
これによって、特異点をのぞいて$b_k(x) = 0$となるゲージを選ぶことができる。
これを**特異ゲージ** (singular gauge) と呼ぶ[^4]。

[^4]: 特異ゲージの特異とは、波動関数が多価(特異)であることを指すようである。

しかし、$e^{i\xi} \neq 0$ の時、波動関数は一般に多価になる。
すなわち、特異点の周りを1周したとき、基底は
$$
\begin{equation}
  \chi_x \to \pm e^{i\xi} \chi_x
\end{equation}
$$
と変化する(同じ場所にあるが、向きが違う)。

### 正則ゲージの方法
もう1つの方法は、ゲージ場は有限値になるが、波動関数は1価になるようにする方法である。
この場合、ゲージ場の影響はHamiltonianに現れる。
これを**正則ゲージ** (regular gauge) と呼ぶ[^5]。

[^5]: 正則ゲージの正則とは、波動関数が1価(正則)であることを指すようである。しかし、もちろんHamiltonianは特異になる。


> [!abstract] 📝 この章のまとめ
> 場の強さが0であれば、ゲージ場の影響を見えなくすることができる。
> しかし、その影響は基底に現れる。
> 結局、ゲージ場をHamiltonianに押し付けて波動関数を1価にするか、ゲージ場を0にする基底をとって波動関数を多価にするかという2択になる。

## 2次元の場合:調和ポテンシャル中の2粒子系
以下では、波動関数を1価にする正則ゲージの方法を用いて、調和ポテンシャル中の2粒子系を考える。

極座標$(r,\varphi),\varphi\in[0,2\pi)$を用いて、2次元自由粒子のHamiltonianは
$$
\begin{equation}
  H = -\frac{\hbar^2}{m} \left( \frac{\partial^2}{\partial r^2} + \frac{1}{r}\frac{\partial}{\partial r} + \frac{4}{r^2}\frac{\partial^2}{\partial \varphi^2} \right)
\end{equation}
$$
である。
ただし、波動関数の条件として
$$
\begin{equation}
  \psi(r,\varphi+2\pi) =e^{i\xi} \psi(r,\varphi)
\end{equation}
$$
を満たす。
ここで、$\xi = 0$ の時はboson、$\xi = \pi$ の時はfermionに対応するが、この中間の値の$\xi$を取らない理由はなく、これが2次元におけるanyonが存在しうる理由である。

(19)とは異なる波動関数の条件として、
$$
\begin{equation}
  \psi(r,\varphi+2\pi) = e^{-i\frac{\xi}{2\pi}\varphi} \psi(r,\varphi)
\end{equation}
$$
としても1価性がある。

この時、Hamiltonianは
$$
\begin{align}
  H' &= e^{-i\frac{\xi}{2\pi}\varphi} H e^{i\frac{\xi}{2\pi}\varphi} \\ 
   &= -\frac{\hbar^2}{m} \left( \frac{\partial^2}{\partial r^2} + \frac{1}{r}\frac{\partial}{\partial r} + \frac{4}{r^2}\left(\frac{\partial}{\partial \varphi} + i\frac{\xi}{2\pi}\right)^2 \right)
\end{align}
$$
となる。
これは原点に強さ$-\frac{\xi}{2\pi}$の磁束がある場合のHamiltonianに対応しており、有効的に角運動量$l+\frac{\xi}{2\pi}$を持つ状態に対応している。
物理的には、**Aharonov-Bohm効果**と呼ばれる現象に対応している。

ここで、調和ポテンシャル $V(r) = \frac{1}{4} m \omega^2 r^2$ を加える。
$H'+V$で駆動する系の固有関数は
$$
\begin{equation}
  \Psi'(r,\varphi) = e^{il\varphi} R(r) \quad l \in \mathbb{Z}
\end{equation}
$$
となる。
ただし、有理関数$R(r)$は
$$
\begin{equation}
  \left(\frac{d^2}{dr^2}  + \frac{1}{r}\frac{d}{dr} - \frac{4}{r^2}(l + \frac{\xi}{2\pi})^2 - \frac{m^2 \omega^2}{4\hbar^2} r^2 + \frac{mE}{\hbar^2}\right) R(r) = 0
\end{equation}
$$
の解である。

エネルギー固有値は
$$
\begin{equation}
  E = 2\hbar \omega \left(n+|l+\frac{\xi}{2\pi}|+\frac{1}{2}\right) \quad n=0,1,2,\dots
\end{equation}
$$
となる。

このスペクトルは$\xi$に依存し、
- $\xi = 0$ の時はboson系のスペクトル
- $\xi = \pi$ の時はfermion系のスペクトル
となるが、この中間の値の$\xi$に対しては、この間を連続的に変化する。

## 3次元の場合
前回述べたように、3次元の場合、同種粒子系の配位空間は実射影平面 $\mathbb{RP}^2$ になる。
2次元の場合と同様に、状態ベクトルはを1周させるという操作は位相因子 $e^{i\xi}$ に対応する。
しかし、2周すると元に戻るため、$e^{i\xi}$ は $\pm 1$ のみを取りうる。
つまり、3次元の場合、同種粒子系はbosonかfermionに限られ、anyonは存在しない。

---
## 前後の記事

📚 目次：[[content/part-01-quantum-hall/index|量子 Hall 効果とエニオン]]  
次 →：[[01-quantum-hall|量子 Hall 効果]]
