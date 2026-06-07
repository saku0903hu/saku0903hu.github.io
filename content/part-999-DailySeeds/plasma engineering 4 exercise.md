---
title: プラズマ工学4 excersise
description:
tags:
---
### (1) $B$ と $j$ が互いに平行となることの証明

プラズマが平衡状態でマクロに静止している（$Dv/Dt=0$）とき、MHD方程式は

$$\nabla p=j\times B$$
となる。
さらに、問題の条件としてプラズマ中の圧力 $p$ も場所によらず一定の定数であるから圧力勾配 $\nabla p$ は $0$ となるので、これを上の式に代入すると、以下のようになる。

$$j\times B=0$$

電流密度 $j$ と磁束密度 $B$ の外積が $0$ ベクトルになるということは、$j$ と $B$ が互いに平行であるということである。

### (2) $B_z$ がゼロ次のベッセル微分方程式を満たすことの証明

問題(1)の結果から $B$ と $j$ は互いに平行であるため、$j=\lambda B$ （$\lambda$ は定数）と記述する。

定常状態において、変位電流を無視したアンペールの法則 $\operatorname{rot} B=\mu_0 j$ に $j=\lambda B$ を代入すると

$$\operatorname{rot} B=\mu_0\lambda B$$

となる。

無限に長い円筒容器内の軸対称プラズマを想定しているため、$z$ 方向および $\theta$ 方向への物理量の変化はなく、$\partial/\partial z=0$、$\partial/\partial\theta=0$ である。
この条件を与えられた軸対称系の $\operatorname{rot}$ の公式 に適用すると

$$\operatorname{rot} B = \left(-\frac{\partial B_\theta}{\partial z}\right)e_r + \left(-\frac{\partial B_z}{\partial r}\right)e_\theta + \frac{1}{r}\left[\frac{\partial}{\partial r}(rB_\theta)\right]e_z$$

$$\operatorname{rot} B = -\frac{\partial B_z}{\partial r}e_\theta + \frac{1}{r}\frac{\partial}{\partial r}(rB_\theta)e_z$$

となる。
これを $\mu_0\lambda B = \mu_0\lambda (B_r e_r + B_\theta e_\theta + B_z e_z)$ と成分ごとに比較すると

- **$r$ 成分:** $0 = \mu_0\lambda B_r \implies B_r = 0$
    
- **$\theta$ 成分:** $-\frac{\partial B_z}{\partial r} = \mu_0\lambda B_\theta$
    
- **$z$ 成分:** $\frac{1}{r}\frac{\partial}{\partial r}(rB_\theta) = \mu_0\lambda B_z$
    

となる。
次に、$\theta$ 成分の式を変形して $B_\theta$ を求める。

$$B_\theta = -\frac{1}{\mu_0\lambda}\frac{\partial B_z}{\partial r}$$

これを $z$ 成分の式に代入する。

$$\frac{1}{r}\frac{\partial}{\partial r}\left(r\left(-\frac{1}{\mu_0\lambda}\frac{\partial B_z}{\partial r}\right)\right) = \mu_0\lambda B_z$$

両辺に $-\mu_0\lambda$ を掛けて整理する。

$$\frac{1}{r}\frac{\partial}{\partial r}\left(r\frac{\partial B_z}{\partial r}\right) + (\mu_0\lambda)^2 B_z = 0$$

左辺の微分を実行すると、以下の微分方程式が得られる。

$$\frac{\partial^2 B_z}{\partial r^2} + \frac{1}{r}\frac{\partial B_z}{\partial r} + (\mu_0\lambda)^2 B_z = 0$$

この方程式は、変数 $r$ に対するゼロ次のベッセル微分方程式の標準形である。