# 時間発展と位相獲得

時間発展演算子（S行列）$\hat{U}$ を計算する。 相互作用ハミルトニアンは
$$\begin{align}
\hat{H}_{int}^I(t) = \alpha(t) \, \hat{n}_\uparrow
\end{align}$$ という形をしている。 ここで、$\alpha(t)$
は電場分布などを含むc数（ただの数値関数）、$\hat{n}_\uparrow = \hat{\psi}_\uparrow^\dagger \hat{\psi}_\uparrow$
は光子数演算子である。
したがって、異なる時刻のハミルトニアン同士も可換である。 $$\begin{align}
[\hat{H}_{int}^I(t), \hat{H}_{int}^I(t')] \propto [\hat{n}_\uparrow, \hat{n}_\uparrow] = 0
\end{align}$$ 時間発展演算子 $\hat{U} = \exp(\hat{\Omega})$ の指数部
$\hat{\Omega}$ は以下のように展開される。 $$\begin{align}
\hat{\Omega} = \underbrace{ -\frac{i}{\hbar} \int dt H(t) }_{\text{第1項}} + \underbrace{ \frac{1}{2} \left(-\frac{i}{\hbar}\right)^2 \int dt \int dt' [H(t), H(t')] }_{\text{第2項}} + \dots
\end{align}$$
交換子がゼロであるため、第2項以降はすべて消失し、第1項のみが厳密解となる。
よって、単純な積分形になる。 $$\begin{align}
\hat{U} = \exp\left( -\frac{i}{\hbar} \int_{-\infty}^{\infty} dt \, \hat{H}_{int}^I(t) \right) = \exp( i \Phi(\Delta t) )
\end{align}$$

これを代入し位相を求める。 $$\begin{align}
\int dt \hat{H}_{int}^I(t) = \int dt \left( -\hbar \lambda k_\uparrow \int dx \, E_c(x,t) \, \hat{\psi}_\uparrow^\dagger(x-v_\uparrow t) \hat{\psi}_\uparrow(x-v_\uparrow t) \right)
\end{align}$$

この演算子 $\hat{U}$ を、光子1個の状態
$\ket{\Psi_\uparrow} = \hat{A}_\uparrow^\dagger \ket{0}$ に作用させる。
数演算子 $\hat{n}_\uparrow$ は固有値 $1$
を返すため、演算子を確率密度関数$|f_\uparrow|^2$ に置き換えて考える。
$$\hat{n}_\uparrow(x-v_\uparrow t) \rightarrow |f_\uparrow(x - x_1 - v_\uparrow t)|^2$$
これにより、獲得位相 $\Phi$ は以下の積分になる。 $$\begin{align}
\Phi = g(k) \int_{-\infty}^{\infty} dt \int_{0}^{L_p} dx \, E_c(x,t) \, |f_\uparrow(x - x_1 - v_\uparrow t)|^2
\end{align}$$ 電場、光子の分布がガウス分布とすると、 $$\begin{align}
E_c(x,t) = E_0 \exp\left[ - \frac{(x - x_c - v_c t)^2}{\sigma_c^2} \right], \quad |f_\uparrow(x,t)|^2 = \frac{1}{\sqrt{\pi}\sigma_\uparrow} \exp\left[ - \frac{(x - x_\uparrow - v_\uparrow t)^2}{\sigma_\uparrow^2} \right]
\end{align}$$ である。 ここで、$v_c=v_\uparrow = v$とする。

時刻 $t$ を固定して空間積分を行う。 $$\begin{align}
I_x(t) = \int_{-\infty}^{\infty} dx \exp\left[ - \frac{(x - (x_c + vt))^2}{\sigma_c^2} \right] \exp\left[ - \frac{(x - (x_\uparrow + vt))^2}{\sigma_\uparrow^2} \right]
\end{align}$$ ただし、結晶の長さ $L_p$
が波束幅より十分長いとして、積分範囲を $\pm\infty$ で近似した。

ガウス積分の公式
$\int e^{-A(x-a)^2} e^{-B(x-b)^2} dx = \sqrt{\frac{\pi}{A+B}} e^{-\frac{AB}{A+B}(a-b)^2}$
を利用する。 ここでは $a = x_c + vt, \ b = x_\uparrow + vt$ なので、差
$a-b = x_c - x_\uparrow$ は時間に依存しない。

$$\begin{align}
I_x = \sqrt{\frac{\pi \sigma_c^2 \sigma_\uparrow^2}{\sigma_c^2 + \sigma_\uparrow^2}} \exp\left[ - \frac{(x_c - x_\uparrow)^2}{\sigma_c^2 + \sigma_\uparrow^2} \right]
\end{align}$$ 空間積分は定数だから、時間積分は $$\begin{align}
\int_{-\infty}^{\infty} dt \rightarrow \int_{0}^{L_p/v} dt = \frac{L_p}{v}
\end{align}$$ となる。

まとめると、 $$\begin{align}
\Phi(\delta x) = g(k) E_0 \frac{1}{\sqrt{\pi}\sigma_\uparrow} \cdot \frac{L_p}{v} \cdot \sqrt{\frac{\pi \sigma_c^2 \sigma_\uparrow^2}{\sigma_c^2 + \sigma_\uparrow^2}} \exp\left[ - \frac{\delta x^2}{\sigma_c^2 + \sigma_\uparrow^2} \right]
\end{align}$$ である。 ただし、$\delta x = x_c - x_\uparrow$ である。

::: thebibliography
99 服部利明, 非線形光学入門, 裳華房, 2022 Imamoğlu, A. and Schmidt, H.
and Woods, G. and Deutsch, M., Strongly Interacting Photons in a
Nonlinear Cavity, Phys. Rev. Lett. 79, 1467 (1997)
:::
