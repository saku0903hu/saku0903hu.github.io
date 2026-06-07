---
title: プラズマ工学7 excersise
description:
tags:
---
### (1) 磁束密度の $R$ 成分 $B_R$ と $Z$ 成分 $B_Z$ の導出
系の軸対称性より$\partial/\partial\phi = 0$。
問題文より、ポロイダル磁束は $\psi = RA_\phi$ で表されるため、$A_\phi = \frac{\psi}{R}$ である。
そのほかのベクトルポテンシャルの成分は0より、
$$B_R = -\frac{\partial}{\partial Z}\left(\frac{\psi}{R}\right) = -\frac{1}{R}\frac{\partial\psi}{\partial Z}$$

$$B_Z = \frac{1}{R}\frac{\partial\psi}{\partial R}$$
となる。

### (2) Grad-Shafranov 方程式の証明
定常状態で変位電流を無視したアンペールの法則は $\operatorname{rot} B = \mu_0 j$ である。 
$\operatorname{rot} B$ の $\phi$ 成分は、先ほどの $\operatorname{rot}$ の公式の第2成分に該当するため、以下が成立。

$$(\operatorname{rot} B)_\phi = \frac{\partial B_R}{\partial Z} - \frac{\partial B_Z}{\partial R}$$

これが電流密度の $\phi$ 成分 $\mu_0 j_\phi$ と等しいため、次式が成り立つ。

$$\frac{\partial B_R}{\partial Z} - \frac{\partial B_Z}{\partial R} = \mu_0 j_\phi$$

ここに(1) で求めた $B_R = -\frac{1}{R}\frac{\partial\psi}{\partial Z}$ と $B_Z = \frac{1}{R}\frac{\partial\psi}{\partial R}$ を代入する。

まず、第1項は

$$\frac{\partial B_R}{\partial Z} = \frac{\partial}{\partial Z}\left(-\frac{1}{R}\frac{\partial\psi}{\partial Z}\right) = -\frac{1}{R}\frac{\partial^2\psi}{\partial Z^2}$$

である。
次に、第2項は

$$\frac{\partial B_Z}{\partial R} = \frac{\partial}{\partial R}\left(\frac{1}{R}\frac{\partial\psi}{\partial R}\right) = -\frac{1}{R^2}\frac{\partial\psi}{\partial R} + \frac{1}{R}\frac{\partial^2\psi}{\partial R^2}$$

である。
これらをアンペールの法則の式に代入する。

$$\left( -\frac{1}{R}\frac{\partial^2\psi}{\partial Z^2} \right) - \left( -\frac{1}{R^2}\frac{\partial\psi}{\partial R} + \frac{1}{R}\frac{\partial^2\psi}{\partial R^2} \right) = \mu_0 j_\phi$$

整理すると

$$\frac{\partial^2\psi}{\partial R^2} - \frac{1}{R}\frac{\partial\psi}{\partial R} + \frac{\partial^2\psi}{\partial Z^2} = -\mu_0 R j_\phi$$

となる。
以上によりGrad-Shafranov方程式（式a）が成立することが証明された。