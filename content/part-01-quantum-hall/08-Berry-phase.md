---
title: 08.Berry位相
tags:
  - fqh
  - quasiparticle
  - Laughlin
  - anyon
  - BerryPhase
---

Hamiltonianがパラメータ$\boldsymbol{R}$に依存している場合 $H(\boldsymbol{R})$ を考える。
パラメタはいくつあってもよく、その場合は全てのパラメタを並べたベクトルになる。

このHamiltonianが縮退していない固有状態 $\boldsymbol{\Psi}_\boldsymbol{R}$を持つとする。

この場合、瞬間的な定常状態のSchrödinger方程式は
$$
\begin{equation}
  H(\boldsymbol{R}) \boldsymbol{\Psi}_\boldsymbol{R} = E(\boldsymbol{R}) \boldsymbol{\Psi}_\boldsymbol{R}
\end{equation}
$$
となる。

ここで、パラメタ$\boldsymbol{R}$が時間に依存してゆっくり[^1] 変化し、パラメタ空間で閉曲線$C$を描くことを考える。

[^1]:ゆっくり変化するとは、エネルギー準位の大小の順序が変わらないに変化させるという意味である。この結果を**断熱定理**という。

 $C$ は閉曲線であるから、これに沿ってパラメタ $\boldsymbol{R}$ が変化したとき、時刻 $t_i$ に$\boldsymbol{R}(t_i)$ であったパラメタはゆっくりと連続的に変化し、時刻 $t_f$ に再び $\boldsymbol{R}(t_f) = \boldsymbol{R}(t_i)$ となる。

いま、状態に縮退がない時を考えているため、時刻$t_i$と$t_f$での状態は位相因子を除いて同じ状態である。

よって、
$$
\begin{equation}
  \boldsymbol{\Psi}_{\boldsymbol{R}(t_f)}(t_f) = \exp\left( -\frac{i}{\hbar}\int_{t_i}^{t_f} dt' E[\boldsymbol{R}(t')] + i\gamma(C) \right) \boldsymbol{\Psi}_{\boldsymbol{R}(t_i)}(t_i)
\end{equation}
$$
となる。

指数関数の第1項は固有エネルギーに依存する動的位相(dynamical phase)であり、第2項はパラメタ空間での閉曲線$C$に依存する幾何学的位相(Berry phase)と呼ばれる。