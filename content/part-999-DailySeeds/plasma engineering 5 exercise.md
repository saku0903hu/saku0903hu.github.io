---
title: プラズマ工学5 excersise
description:
tags:
---
### 1) フーリエ係数 $A_n$ の積分形の導出

関数 $f(t)$ を以下のように余弦フーリエ級数展開する。

$$f(t) = \exp(\alpha \cos \omega t) = \frac{1}{2}A_0 + \sum_{m=1}^{\infty} A_m \cos(m\omega t)$$

この両辺に $\cos(n\omega t)$ を掛け、１周期にわたって $-\pi$ から $\pi$ まで $\omega t$ について積分する。
$$\int_{-\pi}^{\pi}d(\omega t) f(t) \cos(n\omega t)=\int_{-\pi}^{\pi}d(\omega t) [\frac{1}{2}A_0 \cos(n\omega t) + \sum_{m=1}^{\infty} A_m \cos(m\omega t)\cos(n\omega t)]$$
三角関数の直交性から、$\int_{-\pi}^{\pi} \cos(m\omega t) \cos(n\omega t) d(\omega t)$ は $m \neq n$ のとき $0$ となり、$m = n$ のとき $\pi$ となる。また、$A_0$の項は積分により0となる。

したがって、右辺の積分は $A_n \pi$ となる。
これを $A_n$ について解くことで、以下の式が得られる。

$$A_n = \frac{1}{\pi} \int_{-\pi}^{\pi} f(t) \cos(n\omega t) d(\omega t)$$

ここで、$\theta \equiv \omega t$ と定義し、$f(t) = \exp(\alpha \cos \theta)$ を代入することで、式(7)が導かれる。

$$A_n = \frac{1}{\pi} \int_{-\pi}^{\pi} \exp(\alpha \cos \theta) \cos(n\theta) d\theta$$

### 2) Eulerの公式を用いた被積分関数の変形

式(7)の被積分関数 $\exp(\alpha \cos \theta) \cos(n\theta)$ に対して、Eulerの公式を適用する。
cosは以下のように表される。

$$\cos \theta = \frac{\exp(i\theta) + \exp(-i\theta)}{2}$$

$$\cos(n\theta) = \frac{\exp(in\theta) + \exp(-in\theta)}{2}$$

ここで、 $z = \exp(i\theta)$ とおくと

$$\cos \theta = \frac{1}{2} \left( z + \frac{1}{z} \right)$$

$$\cos(n\theta) = \frac{1}{2} \left( z^n + \frac{1}{z^n} \right)$$

である。
これらを元の被積分関数に代入することで、式(8)が導出される。

$$\exp(\alpha \cos \theta) \cos(n\theta) = \frac{1}{2} \exp\left[ \frac{\alpha}{2} \left( z + \frac{1}{z} \right) \right] \cdot \left( z^n + \frac{1}{z^n} \right)$$

### 3) 複素平面上の周回積分への変換

設問1で求めた式(7)に、設問2で導出した式(8)を適用すると

$$A_n = \frac{1}{\pi} \int_{-\pi}^{\pi} \frac{1}{2} \exp\left[ \frac{\alpha}{2} \left( z + \frac{1}{z} \right) \right] \cdot \left( z^n + \frac{1}{z^n} \right) d\theta$$

となる。
次に、積分変数を $\theta$ から $z$ に変換する。
$z = \exp(i\theta)$ の両辺を $\theta$ で微分すると

$$dz = i \exp(i\theta) d\theta = i z d\theta$$

である。
これを $d\theta$ について解くと、$d\theta = \frac{dz}{iz}$ となり、また $\theta$ が $-\pi$ から $\pi$ まで変化するとき、複素数 $z$ は複素平面上で原点を中心とする半径1の単位円（この積分路を $C$ とする）を反時計回りに一周する。

これらを積分式に代入すると、

$$A_n = \frac{1}{2\pi} \oint_C \exp\left[ \frac{\alpha}{2} \left( z + \frac{1}{z} \right) \right] \cdot \left( z^n + \frac{1}{z^n} \right) \frac{dz}{iz}= \frac{1}{2\pi i} \oint_C \left\{ \exp\left[ \frac{\alpha}{2} \left( z + \frac{1}{z} \right) \right] \cdot \left( z^n + \frac{1}{z^n} \right) \right\} \frac{dz}{z}$$

となる。

### 4) 第1種変形ベッセル関数の母関数を用いた式の変形

問題で与えられている第1種変形ベッセル関数の母関数の公式

$$\exp\left[\frac{\alpha}{2}\left(z+\frac{1}{z}\right)\right] = \sum_{k=-\infty}^{\infty} I_{k}(\alpha) z^{k}$$

を、設問3で導出した式(9)の被積分関数の一部である大括弧 `{ }` の中に適用する。

$$\exp\left[\frac{\alpha}{2}\left(z+\frac{1}{z}\right)\right] \cdot \left(z^{n}+\frac{1}{z^{n}}\right)= \left( \sum_{k=-\infty}^{\infty} I_{k}(\alpha) z^{k} \right) \cdot (z^{n} + z^{-n})$$
括弧を展開すると

$$ \sum_{k=-\infty}^{\infty} I_{k}(\alpha) z^{k} \cdot z^{n} + \sum_{k=-\infty}^{\infty} I_{k}(\alpha) z^{k} \cdot z^{-n}= \sum_{k=-\infty}^{\infty} I_{k}(\alpha) z^{k+n} + \sum_{k=-\infty}^{\infty} I_{k}(\alpha) z^{k-n}$$

により示された。

### 5) 留数定理を用いたフーリエ係数 $A_n$ の決定

設問4の結果を積分式に代入すると、式(12)が得られる。

$$A_{n} = \frac{1}{2\pi i} \oint_{C} \sum_{k=-\infty}^{\infty} I_{k}(\alpha) z^{k+n} \frac{dz}{z} + \frac{1}{2\pi i} \oint_{C} \sum_{k=-\infty}^{\infty} I_{k}(\alpha) z^{k-n} \frac{dz}{z}$$

整理すると

$$A_{n} = \frac{1}{2\pi i} \oint_{C} \sum_{k=-\infty}^{\infty} I_{k}(\alpha) z^{k+n-1} dz + \frac{1}{2\pi i} \oint_{C} \sum_{k=-\infty}^{\infty} I_{k}(\alpha) z^{k-n-1} dz$$

である。
そして複素積分における留数定理（コーシーの積分定理）を適用する。
原点を中心とする閉曲線 $C$ において、$\oint_C z^{m} dz$ は $m = -1$ のときのみ $2\pi i$ となり、それ以外の整数のときは $0$ になる。

**第1項の積分について：**

$z$ の指数が $-1$ になる条件は $k + n - 1 = -1$、すなわち $k = -n$ のときである。
このときのみ積分値が残り、結果は $I_{-n}(\alpha) \cdot 2\pi i$ となる。
これを $\frac{1}{2\pi i}$ で割るため、第1項から得られる値は $I_{-n}(\alpha)$ 。

**第2項の積分について：**

$z$ の指数が $-1$ になる条件は $k - n - 1 = -1$、すなわち $k = n$ のとき。
同様に積分すると、第2項から得られる値は $I_{n}(\alpha)$ 。

これらより、$A_n$ は以下のようになる。

$$A_{n} = I_{-n}(\alpha) + I_{n}(\alpha)$$

ここで、変形ベッセル関数の性質（式14：$I_{n}(z) = I_{-n}(z)$）を用いると

$$A_{n} = I_{n}(\alpha) + I_{n}(\alpha) = 2I_{n}(\alpha)$$

最後に、 $\alpha = \frac{eV_{RF}}{kT_e}$ を代入することで

$$A_{n} = 2I_{n}\left(\frac{eV_{RF}}{kT_{e}}\right)$$

となる。(問題文の(13)は$k\to n$の誤植と思われる。)