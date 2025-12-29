---
title: 06.Landau準位の占有率とLaughlinの波動関数のパラメタ
tags:
  - 2dsystem
  - FQH
  - landaulevels
  - Laughlin
---

Laughlin波動関数のパラメタ $q$ は分数量子Hall状態の**充填率(filling factor)** $\nu$ と関係している。

Laughlin波動関数において、任意の電子に注目する。
多項式部分において、電子の座標$z_i$は最大のべきとして$M=(N_e-1)q$となる[^1]。

[^1]:$i>j$で積を取るのでパラメタを除く最大のべきは$N_e-1$である。

最大の角運動量$M$を持つ状態の軌道が囲む面積は$S=2M\pi l^2$である。[[01-landau-levels|最低 Landau 準位]]

よって、Laughlin状態において、全ての電子はこの軌道の内側を運動しており、この軌道内で電子が一様な密度を占めているとすると、Landau準位の占有率は
$$
\begin{equation}
  \nu = \frac{2\pi l^2 N_e}{S} = \frac{N_e}{M} = \frac{N_e}{(N_e-1)q} \approx \frac{1}{q}
\end{equation}
$$
となり、奇数分の1の占有率と結びつく。
ただし、最後の近似は熱力学極限$N_e \to \infty$である。
