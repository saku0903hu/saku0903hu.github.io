---
title: "第2章：量子化EM場の位置空間表現"
---

# 2. 量子化EM場の位置空間表現 (The position space representation of the quantized EM field)

位置空間でEM場を量子化するために、光の波束の基本的な構成要素は高度に局所化された場の励起であると仮定する。簡単のため、一方向にのみ伝搬する光のみを考える。すなわち、$x$ 軸に沿った伝搬を考える。ハイゼンベルク描像を用いて、位置 $x$ 、時刻 $t$ における高度に局所化された場の励起の消滅演算子を $a_{s\lambda}(x, t)$ と記す。ここで $\lambda = H, V$ および $s = \pm 1$ はそれぞれ水平偏光と垂直偏光、および正と負の $x$ 方向に伝搬する励起に対応する。古典電磁気学と同様に、波束の期待値が光速 $c$ で伝搬することを要求する。本論文では、これは以下を仮定することによって考慮される：

$$\langle \psi_H | a_{s\lambda}(x, t) | \psi_H \rangle = \langle \psi_H | a_{s\lambda}(x - sct, 0) | \psi_H \rangle \tag{7}$$

ハイゼンベルク描像における量子化EM場の任意の状態 $|\psi_H\rangle$ に対して成り立つ。したがって

$$a_{s\lambda}(x, t) = a_{s\lambda}(x - sct, 0) \tag{8}$$

この式は、自由空間における量子化EM場の基本的な運動方程式を提供する。

次に、高度に局所化された場の励起が局所的な場の期待値の起源であることに注意する。以降、式 (8) を用いて、マクスウェル方程式と整合する局所的な場の観測量を導出する。誘電率 $\varepsilon$ と透磁率 $\mu$ の媒質中（$c = 1/\sqrt{\varepsilon\mu}$）で、電荷と電流がない場合、位置 $\mathbf{r}$、時刻 $t$ における電場 $\mathbf{E}(\mathbf{r}, t)$ と磁場 $\mathbf{B}(\mathbf{r}, t)$ に対するマクスウェル方程式は以下で与えられる [19]：

$$\nabla \cdot \mathbf{E}(\mathbf{r}, t) = 0, \quad \nabla \times \mathbf{E}(\mathbf{r}, t) = -\dot{\mathbf{B}}(\mathbf{r}, t)$$
$$\nabla \cdot \mathbf{B}(\mathbf{r}, t) = 0, \quad \nabla \times \mathbf{B}(\mathbf{r}, t) = \varepsilon\mu \dot{\mathbf{E}}(\mathbf{r}, t) \tag{9}$$

ハイゼンベルク描像における電場と磁場の観測量 $E(x, t)$ と $B(x, t)$ の期待値 $\langle E(x, t)\rangle$ と $\langle B(x, t)\rangle$ は、すべての時刻でこれらの方程式を満たす必要がある。後に示すように、以下を仮定すれば確かにそうなる：

$$E(x, t) = \sum_{s=\pm 1} \sqrt{\frac{\hbar c}{\varepsilon A}} \left[ \xi_{sH}(x, t) \hat{y} + \xi_{sV}(x, t) \hat{z} \right]$$

$$B(x, t) = \sum_{s=\pm 1} \frac{s}{c} \sqrt{\frac{\hbar c}{\varepsilon A}} \left[ -\xi_{sV}(x, t) \hat{y} + \xi_{sH}(x, t) \hat{z} \right] \tag{10}$$

ここで演算子 $\xi_{s\lambda}(x, t)$ は以下のように定義される：

$$\xi_{s\lambda}(x, t) = \frac{1}{\sqrt{2}} \left[ a_{s\lambda}(x, t) + a_{s\lambda}^\dagger(x, t) \right] \tag{11}$$

ここで $\hat{y}$ と $\hat{z}$ は正の $y$ 軸と $z$ 軸に沿った単位ベクトルであり、$A$ はEM場が占有する $x$ 軸周りの面積を表す。上式の規格化因子は便宜上選ばれたものである。$\xi_{s\lambda}(x, t)$ はエルミートなので、$\langle E(x, t)\rangle$ と $\langle B(x, t)\rangle$ は常に実数であることにも注意されたい。

微分の連鎖律を用いると、$a_{s\lambda}(x - sct, 0)$ の時間微分と位置微分が密接に関連していることを示せる：

$$\frac{d}{dt} a_{s\lambda}(x - sct, 0) = -sc \frac{d}{dx} a_{s\lambda}(x - sct, 0) \tag{12}$$

この関係を式 (8) と (10) と組み合わせると、以下が得られる：

$$\dot{E}(x, t) = -\sum_{s=\pm 1} sc \sqrt{\frac{\hbar c}{2\varepsilon A}} \frac{d}{dx} \left[ a_{sH}(x - sct, 0) \hat{y} + a_{sV}(x - sct, 0) \hat{z} \right] + \text{H.c.}$$

$$\dot{B}(x, t) = -\sum_{s=\pm 1} \sqrt{\frac{\hbar c}{2\varepsilon A}} \frac{d}{dx} \left[ -a_{sV}(x - sct, 0) \hat{y} + a_{sH}(x - sct, 0) \hat{z} \right] + \text{H.c.} \tag{13}$$

さらに、式 (10) から以下が得られる：

$$\nabla \times E(x, t) = \sum_{s=\pm 1} \sqrt{\frac{\hbar c}{2\varepsilon A}} \frac{d}{dx} \left[ -a_{sV}(x - sct, 0) \hat{y} + a_{sH}(x - sct, 0) \hat{z} \right] + \text{H.c.}$$

$$\nabla \times B(x, t) = -\sum_{s=\pm 1} \frac{s}{c} \sqrt{\frac{\hbar c}{2\varepsilon A}} \frac{d}{dx} \left[ a_{sH}(x - sct, 0) \hat{y} + a_{sV}(x - sct, 0) \hat{z} \right] + \text{H.c.} \tag{14}$$

これらの式を式 (9) と比較すると、$\langle E(x, t)\rangle$ と $\langle B(x, t)\rangle$ が確かにマクスウェル方程式の予測する通りに時間発展することが確認される。

古典電磁気学から、自由空間における時刻 $t$ での量子化EM場のエネルギーの観測量 $H_\text{eng}(t)$ は以下に等しいことが分かる：

$$H_\text{eng}(t) = \frac{A}{2} \int_{-\infty}^{\infty} dx \left[ \varepsilon E(x, t)^2 + \frac{1}{\mu} B(x, t)^2 \right] \tag{15}$$

式 (10) における $E(x, t)$ と $B(x, t)$ をこの式に代入すると、

$$H_\text{eng}(t) = \sum_{s, s'=\pm 1} \sum_{\lambda=H,V} \int_{-\infty}^{\infty} dx \, \frac{\hbar c}{2}(1 + ss') \, \xi_{s\lambda}(x, t) \xi_{s'\lambda}(x, t) \tag{16}$$

$s' = s$ の項のみが寄与するので、これは以下に簡約される：

$$H_\text{eng}(t) = \sum_{s=\pm 1} \sum_{\lambda=H,V} \int_{-\infty}^{\infty} dx \, \hbar c \, \xi_{s\lambda}^\dagger(x, t) \xi_{s\lambda}(x, t) \tag{17}$$

この式は、量子化EM場のエネルギーの期待値が常に正であることを示す。また、$\xi_{s\lambda}^\dagger(x, t) \xi_{s\lambda}(x, t)$ が位置 $x$ 、時刻 $t$ におけるエネルギー密度の観測量であることも示す。さらに、式 (17) は量子化EM場の並進対称性を尊重する。すべての内部自由度は $H_\text{eng}(t)$ に等しく寄与する。$\xi_{s\lambda}(x, t)$ はエルミートなので、$\xi^\dagger_{s\lambda}(x, t)$ の記法を用いる必要は厳密にはないが、ダガー記号は式の意味を明確にするのに役立つ。

以上の量子化EM場の記述は、すべての基本的な場の観測量——電場と磁場ベクトルおよび場のエネルギー——の式を提供するという意味で完全である。さらに、式 (8) は状態ベクトルと期待値の時間発展に使える運動方程式を提供する。位置空間では、光が単に一定速度で伝搬するため、波束のダイナミクスはほぼ自明である。序論で既に述べたように、高度に局所化された場の励起を個々の粒子と関連付けることはしない [29]。したがって、$a_{s\lambda}(x, t)$ 演算子の交換関係は不明である。後に述べるように、上記のいずれの式にも矛盾することなく、また自由空間における量子化EM場の基本的な対称性を保ちながら、局所的に作用する消滅演算子 $a_{s\lambda}(x, t)$ を導入する方法は複数存在する。
