# appendix

.5ex plus .2ex minus .2ex電場による光学効果

.5ex plus .2ex minus .2ex電場中の誘電体の熱力学的関係式
内部エネルギーの独立変数を$S,N,\boldsymbol{D}$とすると、化学ポテンシャルを$\mu$として、内部エネルギーとHelmholtz自由エネルギーの微分形は

$$\begin{equation}
\begin{split}
dU = TdS + \mu dN + \boldsymbol{E}\cdot d\boldsymbol{D}\\
dF = -SdT + \mu dN + \boldsymbol{E}\cdot d\boldsymbol{D}\\
\end{split}
\end{equation}$$

となる[^55]。
これらの量の独立変数を$\boldsymbol{D}$でなく$\boldsymbol{E}$に変えたものは、Legendre変換を施すことで得られる:

$$\begin{equation}
\begin{split}
  \tilde{U}(S,N,\boldsymbol{E}) = U - \boldsymbol{E}\cdot \boldsymbol{D}\\
  \tilde{F}(T,N,\boldsymbol{E}) = F - \boldsymbol{E}\cdot \boldsymbol{D}
\end{split}
\end{equation}$$

とすればよい。 微分形は

$$\begin{equation}
\begin{split}
  d\tilde{U} = TdS + \mu dN - \boldsymbol{D}\cdot d\boldsymbol{E}\\
  d\tilde{F} = -SdT + \mu dN - \boldsymbol{D}\cdot d\boldsymbol{E}
\end{split}
\end{equation}$$

である。これより、

$$\begin{equation}
\begin{split}
  \boldsymbol{D} = - \Bigl(\frac{\partial \tilde{U}}{\partial \boldsymbol{E}}\Bigr)_{S,N} = -\Bigl(\frac{\partial \tilde{F}}{\partial \boldsymbol{E}}\Bigr)_{T,N}
\end{split}
\end{equation}$$

であることがわかる。

.5ex plus .2ex minus .2ex結晶の誘電的性質
この節はLandau電磁気学$\S13$を参考にした。
異方性媒質の中の電束密度と電場の間の関係は一般に $$\begin{equation}
\begin{split}
  D_i = P_i +\varepsilon_{ik}E_k
\end{split}
\end{equation}$$ となる[^56]。
ここで、$\boldsymbol{P}$は自発分極を記述する定数ベクトルであるが、たいてい、結晶の対称性によって許されないらしい。
$\boldsymbol{P}$が存在するとき、その結晶は焦電的であるという。
2階のテンソル$\varepsilon_{ik}$は誘電率テンソルと呼ばれる。

さて、誘電率テンソルは以下の性質を満たす。

::: itembox
**Prop.誘電率テンソルの性質** 誘電率テンソルは対称である。
$$\begin{equation}
  \begin{split}
    \varepsilon_{ik} = \varepsilon_{ki}
  \end{split}
\end{equation}$$
:::

::: proof
*Proof.* 誘電率テンソルの熱力学的定義から証明できる。
相転移のない環境を考えているので、恐れずに微分の順序を入れ替える。
$$\begin{equation}
  \begin{split}
    \varepsilon_{ik} = \frac{\partial D_i}{\partial E_k} = \frac{\partial^2 \tilde{F}}{\partial E_k \partial E_i} = \frac{\partial^2 \tilde{F}}{\partial E_i \partial E_k} = \varepsilon_{ki}
  \end{split}
\end{equation}$$ よって示された。 ◻
:::

対称行列は対角化可能であるから、誘電率テンソルは対角化可能である。
対角化した表示の対角成分には固有値が入る。
固有値を$\varepsilon^{(1)},\varepsilon^{(2)},\varepsilon^{(3)}$とする。
三斜、単斜、斜方晶系においては3つの固有値が異なり、これらは2軸性という。
正方晶系、菱面体晶系、立方晶系においては2つの固有値が等しく、これらは1軸性という。
立方晶系においては固有値すべてが等しい(これには特に名前はなさそう)。

.5ex plus .2ex minus .2ex電場の中の複屈折とKerr効果
ここの議論はLandau電磁気学$S80$による。
定電場$\boldsymbol{E}$中の等方性物体を考える。
定電場中の等方性物体は光学的には異方性を持つことを示す。
この異方性は相対的には小さい。
よって、誘電率テンソルを定電場でベキ展開することを考える。
第ゼロ近似では$\varepsilon_{ik}=\varepsilon^{(0)}\delta_{ik}$である。
$\boldsymbol{E}$の1次の項で対称な項は作れないため、次の項は2次である。
また誘電率テンソルが対称テンソルであることに注意すると、入ることのできる項は$\boldsymbol{E}^2\delta_{ik},E_iE_k$である。
前者は第ゼロ近似に定数を追加したものであるから、等方性を破るものではないため、あまり興味はない。
そこで、ここまで含めて$\varepsilon^{(0)}$を定義しておけばよい。
よって、2次までの展開は

$$\begin{equation}
\begin{split}
  \varepsilon_{ik} = \varepsilon^{(0)}\delta_{ik} + \alpha E_iE_k
\end{split}
\end{equation}$$ となる。 ここで$\alpha$はスカラー定数である。
電場の方向に軸を取りなおすことで、固有値の一つは $$\begin{equation}
\begin{split}
  \varepsilon_{\| } = \varepsilon^{(0)} + \alpha E^2
\end{split}
\end{equation}$$ となり、残りの二つは $$\begin{equation}
\begin{split}
  \varepsilon_{\bot } = \varepsilon^{(0)} 
\end{split}
\end{equation}$$

となる。
よって、定電場中にある等方性物体は光学的には1軸性結晶としてふるまう。
このことをKerr効果という。

## Sections

