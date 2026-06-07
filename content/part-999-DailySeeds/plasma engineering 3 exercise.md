---
title: プラズマ工学3 excersise
description:
tags:
---
### (1) 通常の水素プラズマにおける電子のプラズマ角周波数 $\omega_{pe}$

電子の集団が距離 $x$ だけ一斉にズレたとする。
このとき生じる電荷の偏り（面電荷密度 $\sigma$）は、電子密度 $n_e$ と電気素量 $e$ を用いて $\sigma=en_e x$ と書ける。
この電荷の偏りによって生じる電場 $E$ は、電磁気学のガウスの法則から以下のようになる。

$$E=\frac{\sigma}{\epsilon_0}=\frac{en_e x}{\epsilon_0}$$

運動方程式は以下のようにたてられる。

$$m_e\frac{d^2x}{dt^2}=-\frac{n_e e^2}{\epsilon_0}x$$

両辺を $m_e$ で割って整理する。

$$\frac{d^2x}{dt^2}=-\left(\frac{n_e e^2}{m_e\epsilon_0}\right)x$$

よって、電子のプラズマ角周波数 $\omega_{pe}$ は以下の式で表される。
$$\omega_{pe} = \sqrt{\frac{n_e e^2}{m_e \epsilon_0}}$$

---

### (2) 電子・陽電子プラズマのプラズマ角周波数 $\omega_p$ と $\omega_{pe}$ の関係

複数種類の荷電粒子が存在するプラズマ全体のプラズマ角周波数の2乗は、各粒子のプラズマ角周波数の2乗の和として表される。

$$\omega_p^2 = \omega_{pe}^2 + \omega_{pp}^2$$

（ここで、$\omega_{pp}$ は陽電子のプラズマ角周波数）

陽電子は電子と質量が同じ ($m_p = m_e$) で、電荷の絶対値も同じ ($|q| = e$) である。
また、問題の条件から陽電子密度は電子密度と等しい ($n_p = n_e$) ため、陽電子のプラズマ角周波数 $\omega_{pp}$ は電子のプラズマ角周波数 $\omega_{pe}$ と等しくなる。

$$\omega_{pp} = \sqrt{\frac{n_p e^2}{m_p \epsilon_0}} = \sqrt{\frac{n_e e^2}{m_e \epsilon_0}} = \omega_{pe}$$

したがって、全体のプラズマ角周波数 $\omega_p$は以下である。

$$\omega_p^2 = \omega_{pe}^2 + \omega_{pe}^2 = 2\omega_{pe}^2$$

$$\omega_p = \sqrt{2}\omega_{pe}$$

---

### (3) 無磁場の電子・陽電子プラズマの電磁波のカットオフ周波数

無磁場プラズマ中を伝播する電磁波の屈折率 $N$ は、プラズマ角周波数 $\omega_p$ と電磁波の角周波数 $\omega$ を用いて次のように表される。

$$N = \sqrt{1 - \frac{\omega_p^2}{\omega^2}}$$

問題文にある通り、カットオフ現象は屈折率 $N = 0$ のときに起こるから、

$$\sqrt{1 - \frac{\omega_p^2}{\omega^2}} = 0$$

$$1 - \frac{\omega_p^2}{\omega^2} = 0$$

$$\omega^2 = \omega_p^2$$

$$\omega = \omega_p$$

(2) で求めた関係式を用いると、カットオフ角周波数 $\omega$ は以下のようになる。

$$\omega = \sqrt{2}\omega_{pe} = \sqrt{\frac{2 n_e e^2}{m_e \epsilon_0}}$$

周波数に直すと

$$f = \frac{\omega}{2\pi} = \frac{\sqrt{2}\omega_{pe}}{2\pi}$$
となる。