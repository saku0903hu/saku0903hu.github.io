---

title: 02.量子Hall効果
date: 2025-12-27
tags:


---

# 量子 Hall 効果

磁場中の 2 次元電子系を考える。面内に $x,y$ 平面をとり、磁場は面に垂直にかかっているとする。

電流密度 $\boldsymbol{j}$ と電場 $\boldsymbol{E}$ の関係は Ohm の法則より

$$
\begin{aligned}
\begin{pmatrix}
j_x \ j_y
\end{pmatrix}
=============

\begin{pmatrix}
\sigma_{xx} & \sigma_{xy} \
\sigma_{yx} & \sigma_{yy}
\end{pmatrix}
\begin{pmatrix}
E_x \ E_y
\end{pmatrix}
\end{aligned}
$$

すなわち

$$
\boldsymbol{j}=\boldsymbol{\sigma}\boldsymbol{E}
$$

と書ける。ここで $\boldsymbol{\sigma}$ は伝導率テンソルである。

面の等方性より

$$
\sigma_{xx}=\sigma_{yy}, \qquad
\sigma_{xy}=-\sigma_{yx}
$$

が成り立つ。
$\sigma_{xx}$ を縦伝導率、$\sigma_{xy}$ を Hall 伝導率と呼ぶ。

## 抵抗率テンソル

伝導率テンソルの逆行列を抵抗率テンソル $\boldsymbol{\rho}$ とすると

$$
\begin{aligned}
\rho_{xx}&=\rho_{yy}=\frac{\sigma_{xx}}{\sigma_{xx}^2+\sigma_{xy}^2}, \
\rho_{xy}&=-\rho_{yx}=-\frac{\sigma_{xy}}{\sigma_{xx}^2+\sigma_{xy}^2}
\end{aligned}
$$

である。

これらは実験的に測定可能な量であり、$\rho_{xy}$ は Hall 抵抗と呼ばれる。

---

## 前後の章

← 前：[[01-landau-levels|Landau 準位]]  
📚 目次：[[index|量子 Hall 効果とエニオン]]  
次 →：[[03-integer-qhe|整数量子 Hall 効果（IQH）]]
