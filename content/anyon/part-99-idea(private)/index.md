---
title: part-08-IDEAS(private)
description: エニオン理論に関する研究ノートとセミナーまとめ
tags:
  - anyon
  - topological-order
  - quantum-hall
  - fqhe
---

# 検討中のアイデア

.5ex plus .2ex minus .2exアイデア:システムをエニオンにする計算法
エニオンにおいて、$\mathbb{R}^2$というのは本質的である。
粒子の置換がブレイド群で記述されるからである。

さきほどのモデルでは、粒子が$\mathbb{R}^3$を運動しており、粒子の置換は対称群になるため、$\ket{ab}+e^{i\theta}\ket{ba}$という状態はあくまでstatistical
anyonに過ぎないと思われる。
そこで、光子が運動する自由度をひとつ減らす系から見ることで、その粒子を仮想的に$\mathbb{R}^2$と考えられないかという疑問がある。

静止系から見ると相変わらず$\mathbb{R}^3$であるから、考える意味がないかと思われるが、速度を持つ系から見ると、これがもし非可換エニオンに見えるのであれば、そのまま量子計算に持ち込めるため、応用の幅が広がるかもしれない。

.5ex plus .2ex minus .2exモデル改善案
光ファイバー内を進む2つの光子を考える。
光子どうしはエンタングルしているとする。
二つの点を通る平面$\mathbb{R}_p^2$上[^57]で運動を考える。

<figure data-latex-placement="htbp">
<div class="center">
<img src="limited.png" style="width:100mm" />
</div>
<figcaption>運動している光子が通る平面上を取るイメージ</figcaption>
</figure>

この平面は以下のようにして構成する。

各光ファイバー内の位置ベクトルを$\boldsymbol{r}_1,\boldsymbol{r}_2$とする。

2体波動関数$\psi(\boldsymbol{r}_1,\boldsymbol{r}_2)$を用いて、各時刻で粒子の位置の期待値の変化で張られる平面を考える。
$$\begin{equation}
\begin{split}
d\left<\boldsymbol{r}_i(t)\right> = \bra{\psi(\boldsymbol{r}_1,\boldsymbol{r}_2,t+dt)}\hat{\boldsymbol{r}_i}\ket{\psi(\boldsymbol{r}_1,\boldsymbol{r}_2,t+dt)}-\bra{\psi(\boldsymbol{r}_1,\boldsymbol{r}_2,t)}\hat{\boldsymbol{r}_i}\ket{\psi(\boldsymbol{r}_1,\boldsymbol{r}_2,t)},\,\,\,i=1,2\\
\end{split}
\end{equation}$$

これが準備されれば、光子の運動は $$\begin{equation}
\begin{split}
\mathbb{R}_p^2(t) = \{d\left<\boldsymbol{r}_1(t)\right>,d\left<\boldsymbol{r}_2(t)\right>\}
\end{split}
\end{equation}$$ で張られる空間上では、2次元だと考えられる。

この上でハミルトニアンを修正することを考えていく。
モデルが修正されれば、ブレーディングを実行する。

.5ex plus .2ex minus .2ex議論

- 期待値で張られる空間は、あくまで統計的に、次の瞬間に粒子がいる確率が高い場所を表しているだけで厳密にそこにいるわけではないので、2次元上で考えられないのではないか。

- 光ファイバー内の位置を記述する配位空間で同じ議論を簡潔に行えないか。これに関しては、光ファイバー内で光子は1次元中を動くと考えられないだろうと思われるため、却下。

.5ex plus .2ex minus .2ex過去の議論

::: itembox
**Prop.anyonの場の演算子の誤った定義**
$\Phi(x)$を、$x$にanyonを作る演算子とすると、 $$\begin{align}
\Phi(x) \Phi(y) \ket{0} \neq  \ket{xy} + e^{i\theta} \ket{yx}
\end{align}$$ である。
:::

::: proof
*Proof.* 後ほど計算を書くつもりだが、示せている。 ◻
:::

::: itembox
**Prop.superposition of boson field Operator equal anyon field
Operator?** 我々が示したいことは、boson場を用いて $$\begin{equation}
\begin{split}
\Phi_a(a,b)=\phi(a)\phi(b)+e^{i\theta}\phi(b)\phi(a)\\
\end{split}
\end{equation}$$ という場がanyonであるかどうかを示すことである。
:::

.5ex plus .2ex minus .2ex(2+1)dでの生成消滅演算子を用いた計算:要検証
J-W変換はbosonizationの一種であると思っている。 これを追ってみる[^58]。
anyon
likeな状態を交換関係に入れてみると、明らかに消滅どうしであれば打ち消して0になってしまう。
そのため、まずbosonizationの手続きを学ぶ必要があると感じた。

以上は以前までの結論である。\
$a^\dagger(x_c)$を、反時計回りに粒子を回すことを前提とした生成演算子とする。
このとき $$\begin{equation}
\begin{split}
a^\dagger(y_c)a^\dagger(x_c)\ket{0}=\ket{xy}+e^{i\theta}\ket{yx}
\end{split}
\end{equation}$$ である(要検証)。 この式の説明をする。
まず$x$に粒子を生成し、次に$y$に粒子を作る。
そして、$x,y$を反時計回りに入れ替えたときに局所位相$e^{i\theta}$を得るということを示している。
それであれば$\ket{yx}+e^{i\theta}\ket{xy}$でよくないか?という指摘があるかもしれない。
その場合は$a^\dagger(x_c)a^\dagger(y_c)\ket{0}$に対応する(要検証)。

(3.2)式を変形していくと、 $$\begin{equation}
\begin{split}
\ket{xy}+e^{i\theta}\ket{yx}=e^{i\theta}(\ket{yx}+e^{-i\theta}\ket{xy})\\
\end{split}
\end{equation}$$ となる。
この式の右辺の$e^\dagger$を除いた部分は、$y$に粒子をひとつ作った後に$x$に粒子をひとつ作るという状態をそれを反時計回りに用意するという前提で用意するという意味である。
すなわちこれは $$\begin{equation}
\begin{split}
  \ket{xy}+e^{i\theta}\ket{yx}&=e^{i\theta}(\ket{yx}+e^{-i\theta}\ket{xy})\\
  &=e^{i\theta}a^\dagger(x_{c^{-1}})a^\dagger(y_{c^{-1}})\ket{0}\\
\end{split}
\end{equation}$$ を意味する。
$c^{-1}$は時計回りの向きを正とした円である。

以上の議論より、 $$\begin{equation}
\begin{split}
a^\dagger(y_c)a^\dagger(x_c)=e^{i\theta}a^\dagger(x_{c^{-1}})a^\dagger(y_{c^{-1}})\\
\end{split}
\end{equation}$$ であると考えられる。(要検証)

これはanyonの生成演算子の交換関係ではない[^59]ため、$\ket{ab}+e^{i\theta}\ket{ba}$はanyonではないという結論である。

入射状態を$\ket{\psi_i}=\Phi_{\uparrow}^\dag(x)\Phi_{\downarrow}^\dag(x-vt)\ket{0}$とする。
場の演算子のみを時間発展させることを考えると、時間発展演算子は
$$\begin{align}
U=U_{L_a}U_P U_{L_b}
\end{align}$$ である。

これを用いて、それぞれの場の演算子を時間発展させていくことを考える。
まず、下向きスピンを持つ粒子は、 $$\begin{align}
\Phi_{\downarrow}(x-vt) &\to U_{L_b}^\dag \Phi_{\downarrow}(x-vt) U_{L_b} \\
&= e^{-i n_0 k_0 L_b} \Phi_{\downarrow}(x-vt)e^{i n_0 k_0 L_b} \\
&= \Phi_{\downarrow}(x -vt + n_0 L_b)
\end{align}$$ となる[^60]。

次に、上向きスピンを持つ粒子を考える。
数密度演算子を$\hat{n}(x)=\Phi_{\uparrow}^\dag(x)\Phi_{\uparrow}(x)$とすると、
$$\begin{align}
\Phi_{\uparrow}(x) &\to U_{L_a}^\dag U_P^\dag \Phi_{\uparrow}(x) U_P U_{L_a} \\
&= e^{in_0 k_0 L_a} e^{i\int_{x_0}^{x} \alpha E(l) \hat{n}_{\uparrow} \frac{dl}{v}} \Phi_{\uparrow}(x) e^{-i\int_{x_0}^{x} \alpha E(l) \hat{n}_{\uparrow} \frac{dl}{v}} e^{-in_0 k_0 L_a} \\
&= e^{i\int_{x_0}^{x} \alpha E(l) \hat{n}_{\uparrow} \frac{dl}{v}} \Phi_{\uparrow}(x + n_0 L_a) e^{-i\int_{x_0}^{x} \alpha E(l) \hat{n}_{\uparrow} \frac{dl}{v}}\\
& \equiv \Phi_{\uparrow A}(x)
\end{align}$$ 最後では、この場をエニオンの場として定義した(要検討)。

これを用いて、場の交換関係を考える。
物理的には、ブレイディングを考えていることになる。 $$\begin{align}
\Phi_{\uparrow A}(x) \Phi_{\downarrow}(x+vt+n_0 L_b) &= e^{i\alpha \int_{x_0}^{x} \hat{n}_{\uparrow}(l) \frac{dl}{v}} \Phi_{\uparrow A}(x)  e^{i\alpha \int_{x_0}^{x} \hat{n}_{\uparrow}(l) \frac{dl}{v}} \Phi_{\downarrow}(x+vt+n_0 L_b) \\
\end{align}$$ 前半にBCH公式を使うと、 $$\begin{align}
\Phi_{\uparrow A}(x) \Phi_{\downarrow}(x+vt+n_0 L_b) &= (\Phi_{\uparrow}(x)+\int_{x_0}^{x}dl \frac{i\alpha E}{v}[\hat{n}_{\uparrow}(l),\Phi_{\uparrow}(x)]+...) \Phi_{\downarrow}(x+vt+n_0 L_b) \\
\end{align}$$ となる。 電場一次に比例する交換子は、 $$\begin{align}
[\hat{n}_{\uparrow}(l),\Phi_{\uparrow}(x)] &= -\delta(l-x)\Phi_{\uparrow}(x)
\end{align}$$ であるから、積分の中に入れると、 $$\begin{align}
&=(\Phi_{\uparrow}(x) - \frac{i\alpha E}{v} \Phi_{\uparrow}(x) + ...) \Phi_{\downarrow}(x+vt+n_0 L_b) \\
&\simeq e^{-i\frac{\alpha E}{v}} \Phi_{\uparrow}(x) \Phi_{\downarrow}(x+vt+n_0 L_b) \\
&= e^{-i\frac{\alpha E}{v}} \Phi_{\downarrow}(x+vt+n_0 L_b) \Phi_{\uparrow}(x)
\end{align}$$
最後の式では、BCH公式を使った後、ボソンの場の演算子は交換するため、順番を入れ替えた。

[^1]: この下のA.Yamamotoによる仕事で、(1+1)dのanyonと(2+1)dのanyonのboson的描像はかなり異なるということが指摘されている。(2+1)dにおいてはanyonはboson+fluxで作れる。これはboson場にChern-Simonsゲージ場を入れることに対応するが、(1+1)dではWigner変換が平均場と解釈でき、平均場近似の結果だと思えば、元は多体効果だと解釈できる。これは(1+1)dのanyonはboson場にboson(あるいはfermion?)の多体相互作用が入ったものと等価である。何か自分たちのセットアップにも使えないだろうか?

[^2]: <https://arxiv.org/pdf/1709.06323>

[^3]: $\ket{ab}$と$\ket{ba}$で長さ同じでいいのか?

[^4]: Pockels効果を再考する必要あり

[^5]: 一般には$n$次感受率は$n+1$次テンソルだが、簡単のためスカラーとして扱う。

[^6]: 印加される電場を低周波の光と考えれば2次の非線形光学効果ともみなせるらしい。

[^7]: 光Kerr効果を用いたQND測定をしている文献。使えそうだが読めていない。<https://annex.jsap.or.jp/photonics/kogaku/public/19-11-kaisetsu6.pdf>

[^8]: 使えそうな文献は<https://arxiv.org/pdf/quant-ph/0009110>,

    <https://journals.aps.org/pra/abstract/10.1103/PhysRevA.74.053818>など

[^9]: この追加の項でanyonの統計パラメタを与えられるか?$\to$これはまだ解決していない疑問である。$\hat{n}^2$と場の演算子の交換関係を実際に計算する必要がある。

[^10]: 演算子が$\frac{\partial}{\partial z}$の形をしているとき、任意の関数$f$を持ってきて$\frac{\partial f}{\partial z}$と考えて証明すればよい。

[^11]: $a\ket{0,0}=b\ket{0,0}=0$を解くとよい。

[^12]: 一般的には外場が弱い場合は量子効果を無視できないが、エネルギー準位の幅が小さかったり、inpurityポテンシャルの変化が十分緩やかだとし、仮想的に半古典的だとしていると考えられる

[^13]: 2次元面では$n_e r_0^2 \sim 1$であるから。また、Landau準位の縮退度は$n_\phi=1/{2\pi l^2}$だから、$n_e=\nu n_\phi$である。縮退度は、$\ket{0,m}$の状態が半径$\sqrt{2m}l$上にあるサイクロトロン軌道の線形結合になることと、そこで有限面積を持つ系を考えればよい。

[^14]: 吉岡本による記述であるから現状はわからない。

[^15]: これはのちほど詳しく述べる。

[^16]: パラメタ$\alpha$を持つ波動関数(試行関数 trial
    functionと呼ぶ)$\Psi(\alpha)$を仮定しハミルトニアンの期待値を計算して、$\alpha$について最小化する理論。

[^17]: $L_z = \hbar \left( z \frac{\partial}{\partial z} - \bar{z} \frac{\partial}{\partial \bar{z}} \right)$の固有関数になっている。

[^18]: 多項式の次数が同じ項の和で表されているということ。

[^19]: 3体力以上の相互作用は無視している。このような波動関数をJastrow波動関数と呼ぶ。

[^20]: 疑問:実際にはexpの部分も考えなくてはいけない気がする。

[^21]: 磁場中の2次元電子系の一般的考察[\[sonzaikakuritu\]](#sonzaikakuritu){reference-type="ref"
    reference="sonzaikakuritu"}より。

[^22]: 実在しないが、粒子として考えられるものを準粒子と呼んでいる。

[^23]: 場の理論の言葉では、CSゲージ場を作用に追加することに対応する。詳しくは次のpartに書いている。

[^24]: 2次元以下ではスピンと統計の関係が破綻するから、内部自由度を考えるのは無駄だと思っている。今の場合、そもそも準粒子の内部自由度は存在しないが。

[^25]: 電子がとれる状態の数の和が$M$であるから、これを自由度と見ている。

[^26]: 波動関数の冪の部分が偶数でないと、入れ替えで負符号が出るから。

[^27]: 1998年現在。いまはどこまでできてるか調べたい

[^28]: あとで足す。

[^29]: Universal Topological Quantum Computation from a
    Superconductor-Abelian Quantum Hall Heterostructure
    <https://journals.aps.org/prx/abstract/10.1103/PhysRevX.4.011036>

[^30]: GL理論を修正したものもあらわれている。

[^31]: ガスというのは気体であるということではなく、結晶のような周期ポテンシャルをもたない自由な系であるということを指す。

[^32]: よくわかっていない

[^33]: なぜ?

[^34]: なぜ?

[^35]: 後で調べる

[^36]: 微分形式を勉強する必要あり。たぶん$A \wedge dA$を略記している。$dA$ってなに?

[^37]: これは無限平面で考えていることに注意?

[^38]: 要検討

[^39]: 確かめてない

[^40]: 粒子が何もない状況が最もエネルギーが低い基底状態である。

[^41]: 要検証

[^42]: これはDehn手術と呼ばれている。

[^43]: $A\neq0$のときの運動方程式が$da = -1/k \,dA$だったことを思い出すとよい。

[^44]: (1+1)dのfermionをbosonに変える枠組みがbosonization。詳しくは後述する

[^45]: 2準位系で状態を作るのがqbit。$d>2$準位系で作るとqditになる。

[^46]: Oracleを知っていることは探索問題の答えを知っているに等しいという疑問があるが、これは逆で、Groverは答えをこれで定義しているブラックボックスのモデルである。

[^47]: 複合化の証明にはFermatの小定理を用いる: $$\begin{align}
      g^{(p-1)(q-1)} \equiv 1 \mod N
    \end{align}$$

[^48]: この$r$を位数(order)と呼び、位数を求める問題を離散対数問題という。

[^49]: レジスタはひとかたまりのqbitというふうに扱う。たぶん、今回は$\ket{\text{第1レジスタ}}\otimes\ket{\text{第2レジスタ}}$という基底を持つHilbert空間を考えるということだと思われる。

[^50]: 例題3.7の解説がよくわかってない

[^51]: 戎さんからは、product stateからquantum
    doubleを作ることを目標にするのはどうかと言われており、自分もこれをやってみたいと思っています。

[^52]: 以下の表はISSP workshopのYuval Ronen, \"Interference in the
    Even-Denominator Quantum Hall Regime\"より。

[^53]: Higher-form
    symmetryの文脈で、アクシオン場が有効的にChern-Simonsになるという意味ですが、具体的な手続きは忘れてしまいました。

[^54]: Kitaevハニカム模型

[^55]: Landauではガウス単位系を用いている。ガウス単位系とSI単位系の変換は$\boldsymbol{D} /4\pi \rightarrow \boldsymbol{D}$とすればよい。

[^56]: 本の中では第1項が$D_{0i}$となっているが、この記法では次元があってないように見える。たぶん$D_0$というベクトルの$i$成分という意味だと思われるので、本文のように表記を変えた

[^57]: 擬平面,pseudo planeで$\mathbb{R}_p^2$としている。

[^58]: 参考:<https://park.itc.u-tokyo.ac.jp/ashida-g/note_chuo.pdf>,<https://repository.kulib.kyoto-u.ac.jp/bitstream/2433/204774/1/bussei_el_044203.pdf>,<https://arxiv.org/pdf/cond-mat/9908262>

[^59]: (2+1)dのAnyonの交換関係は $$\begin{equation}
    \begin{split}
    a_i(\boldsymbol{x}_{\mathcal{C}})a_i(\boldsymbol{y}_{\mathcal{C}})+q^{-1} a_i(\boldsymbol{y}_{\mathcal{C}})a_i(\boldsymbol{x}_{\mathcal{C}})=0\\
    a_i^\dagger(\boldsymbol{x}_{\mathcal{C}})a_i^\dagger(\boldsymbol{y}_{\mathcal{C}})+q^{-1} a_i^\dagger(\boldsymbol{y}_{\mathcal{C}})a_i^\dagger(\boldsymbol{x}_{\mathcal{C}})=0\\
    a_i(\boldsymbol{x}_{\mathcal{C}})a_i^\dagger(\boldsymbol{y}_{\mathcal{C}})+q a_i^\dagger(\boldsymbol{y}_{\mathcal{C}})a_i(\boldsymbol{x}_{\mathcal{C}})=0\\
    a_i^\dagger(\boldsymbol{x}_{\mathcal{C}})a_i(\boldsymbol{y}_{\mathcal{C}})+q a_i(\boldsymbol{y}_{\mathcal{C}})a_i^\dagger(\boldsymbol{x}_{\mathcal{C}})=0\\
    \end{split}
    \end{equation}$$ である。$q= e^{i\pi \nu}$である。論文Anyons and
    Quantum Groupsより。

[^60]: 最後の変形は物理的な要請からしてしまっている。どうやって正当化しようかなと思っている

## Sections

