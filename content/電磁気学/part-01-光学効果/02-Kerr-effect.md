---
title: 電場中の複屈折と Kerr 効果
description: 統計物理の周りの話をまとめます。
tags:
  - statistical mechanics
  - Electromagnetism
---

この議論は *Landau 電磁気学 §80* に基づく。

定電場 $\boldsymbol{E}$ 中の等方性物体を考える。
定電場によって、等方性物体は **光学的異方性**を示すようになる。

この効果は小さいため、誘電率テンソルを電場で展開する。

ゼロ次近似では

$$
\varepsilon_{ik} = \varepsilon^{(0)} \delta_{ik}
$$

である。

$\boldsymbol{E}$ の一次では対称な項を作れないため、次は二次項となる。
対称性を考慮すると、許される項は

* $\boldsymbol{E}^2 \delta_{ik}$
* $E_i E_k$

である。

前者は等方性を破らないため、$\varepsilon^{(0)}$ に吸収してよい。
よって二次までの展開は

$$
\varepsilon_{ik}
= \varepsilon^{(0)} \delta_{ik}

* \alpha E_i E_k
  $$

となる。

電場方向を主軸に取ると、固有値は

$$
\varepsilon_{\parallel}
= \varepsilon^{(0)} + \alpha E^2
$$

および

$$
\varepsilon_{\perp}
= \varepsilon^{(0)}
$$

となる。

したがって、定電場中の等方性物体は
**一軸性結晶として振る舞う**。

この現象を **Kerr 効果**と呼ぶ。
