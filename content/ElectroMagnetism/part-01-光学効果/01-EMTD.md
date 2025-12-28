---
title: 電場中の誘電体の熱力学的関係式
description: 統計物理の周りの話をまとめます。
tags:
  - statistical mechanics
  - Electromagnetism
---

内部エネルギーの独立変数を
$$(S, N, \boldsymbol{D})$$
とし、化学ポテンシャルを $\mu$ とする。

このとき、内部エネルギー $U$ と Helmholtz 自由エネルギー $F$ の微分形は

$$
\begin{aligned}
dU &= TdS + \mu dN + \boldsymbol{E}\cdot d\boldsymbol{D} \\
dF &= -SdT + \mu dN + \boldsymbol{E}\cdot d\boldsymbol{D}
\end{aligned}
$$

となる。

> **注**
> Landau ではガウス単位系を用いている。
> ガウス単位系と SI 単位系の変換は
> $
> \boldsymbol{D}/4\pi \rightarrow \boldsymbol{D}
> $
> とすればよい。

これらの量の独立変数を $\boldsymbol{D}$ ではなく $\boldsymbol{E}$ に変えたものは、
Legendre 変換によって得られる。

$$
\begin{aligned}
\tilde{U}(S,N,\boldsymbol{E}) &= U - \boldsymbol{E}\cdot \boldsymbol{D} \\
\tilde{F}(T,N,\boldsymbol{E}) &= F - \boldsymbol{E}\cdot \boldsymbol{D}
\end{aligned}
$$

このとき微分形は

$$
\begin{aligned}
d\tilde{U} &= TdS + \mu dN - \boldsymbol{D}\cdot d\boldsymbol{E} \\
d\tilde{F} &= -SdT + \mu dN - \boldsymbol{D}\cdot d\boldsymbol{E}
\end{aligned}
$$

となり、したがって

$$
\boldsymbol{D}
= - \left(\frac{\partial \tilde{U}}{\partial \boldsymbol{E}}\right)_{S,N}\\
= - \left(\frac{\partial \tilde{F}}{\partial \boldsymbol{E}}\right)_{T,N}
$$

が成り立つことが分かる。

---

### 結晶の誘電的性質

この節は *Landau 電磁気学 §13* を参考にしている。

異方性媒質中では、電束密度と電場の関係は一般に

$$
D_i = P_i + \varepsilon_{ik} E_k
$$

と書ける。

ここで $\boldsymbol{P}$ は自発分極を表す定数ベクトルであるが、多くの場合、
結晶の対称性により許されない。
$\boldsymbol{P}$ が存在する結晶は **焦電的 (pyroelectric)** であるという。

$\varepsilon_{ik}$ は **誘電率テンソル**である。

---

> [!info] Prop. 誘電率テンソルの対称性
>誘電率テンソルは対称である： 
>$$
>\varepsilon_{ik} = \varepsilon_{ki}
>$$


**証明**

誘電率テンソルの熱力学的定義を用いる：

$$
\varepsilon_{ik}
= \frac{\partial D_i}{\partial E_k}
= \frac{\partial^2 \tilde{F}}{\partial E_k \partial E_i}
$$

相転移のない状況では微分順序を交換できるため、

$$
\varepsilon_{ik}
= \frac{\partial^2 \tilde{F}}{\partial E_i \partial E_k}
= \varepsilon_{ki}
$$

が成り立つ。∎

---

対称行列は対角化可能であるため、誘電率テンソルも対角化できる。
固有値を

$$
\varepsilon^{(1)},\ \varepsilon^{(2)},\ \varepsilon^{(3)}
$$

とすると、

* 三斜・単斜・斜方晶系：3つの固有値が異なる（**二軸性**）
* 正方晶・菱面体・立方晶系：2つが等しい（**一軸性**）
* 立方晶系：すべて等しい

と分類できる。



