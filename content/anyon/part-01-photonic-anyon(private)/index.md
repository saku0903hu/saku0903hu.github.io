# photonic anyonの理論と時間空間平面上のanyonについての研究(オリジナル)

.5ex plus .2ex minus .2ex本研究でやりたいことと進捗
やりたいこととその進捗具合をまとめる。

1.  時間差で光子に位相をつけることでanyonを作りたい。:これが一番のテーマ。背後には空間1次元時間1次元の2次元系でエニオンを作るというコンセプトや、次元を変えたときのダイナミクスを探ることがある。

    1.  第一量子化の言葉で議論してみたい。:Statistical
        anyonの論文にあった$\ket{ab}+e^{i\theta}\ket{ba}$(anyon
        likeな状態ベクトル)という状態にインスパイアされている。

        1.  進捗:bosonの場の演算子を用いた重ね合わせの状態の作成をもとに構成しようとしている。anyon-likeの場の消滅演算子同士から交換関係を出そうとすると、bosonの交換がなされてしまいうまくいかない。

    2.  具体的なモデルを立てる。:2つに分割した経路を持つ光ファイバーに時間差で光子を入れ、片方に電場をかけるという系を考える。:状態ベクトルはanyon
        likeであるが、これがanyonであるかは(a)の議論に依存する。

        1.  Hamiltonianを立てる。:光子のエネルギー、ビームスプリッターによる結合、電場による位相付与を考える。:できているはず。

        2.  2サイト模型に帰着させる。:光子の伝播方向に同じ速度で進む系から見る。これがJ-W変換でanyonの出る格子模型と一致させたい。:途中。ここでは第二量子化の言葉で行うので(a)と独立。並進演算子を用いた定式化を行ってみようとしている。

        3.  Jordan-Wigner変換を行い、anyonを出す。

    3.  IBMQなどのリモート量子コンピュータでシミュレーションする。:プログラムの言語を理解できておらず進んでいない。

2.  多粒子系を作りたい。

    1.  3粒子を作る。:$\ket{A}+e^{i\theta}\ket{B}+e^{i\phi}\ket{C}$という3体anyon
        likeな状態を作りたい。:Braid群の1次元表現を調べると、すべての粒子に対して、同じ方向での入れ替えは同じ位相をつけるので、非可換anyonへの道になると思われる。

    2.  N粒子をつくる。ネットワークをつくる。先行研究はKitaevのdouble
        modelがある。日本語の解説に関しては<https://osaka-kyoiku.repo.nii.ac.jp/record/2093321/files/kj1_70_023.pdf>。

.5ex plus .2ex minus .2exエニオンの第一量子化での定式化

(1+1)dで考える[^1]。 anyonの定義は $$\begin{align}
\braket{r}{\psi(r_1,r_2)}=e^{i\theta}\braket{r}{\psi(r_2,r_1)}\\
\end{align}$$ である。 これを第二量子化の言葉で書くと、
anyonの場の演算子$\Phi(x)$と、共役の$\Pi(x)$を用いて、
$$\begin{equation}
\begin{split}
\Phi(x)\Phi(y)=e^{i\theta \text{sgn}(x-y)}\Phi(y)\Phi(x)\\
\Pi(x)\Pi(y)=e^{-i\theta \text{sgn}(x-y)}\Pi(y)\Pi(x)\\
\Phi(x)\Pi(y)=e^{-i\theta \text{sgn}(x-y)}\Pi(y)\Phi(x)+\delta(x-y)\\
\end{split}
\end{equation}$$ と書けることがわかっている[^2]。\
また、anyonはboson場に、数演算子分の位相を付与するJordan-Wigner変換をすることで作れる(複合粒子描像)。この定式化は、boson場$\phi(x)$とその共役$\pi(x)$を用いて、
$$\begin{equation}
\begin{split}
\Phi(x) = \phi(x)\exp\left(i\theta\int_{-\infty}^x dx' n(x')\right)\\
\Pi(x) = \exp\left(-i\theta\int_{-\infty}^x dx' n(x')\right)\pi(x)\\
\end{split}
\end{equation}$$ となる。
ここまでが、すでにわかっているanyonの関係である。\
boson,fermionの生成消滅演算子の交換関係から場の交換関係を導出する流れとパラレルにやってみたい。

.5ex plus .2ex minus .2ex時間差を用いたphotonのanyonization

<figure data-latex-placement="htbp">
<div class="center">
<img src="setup_1.png" style="width:100mm" />
</div>
<figcaption>光子を時間差で入れ、片方に電場をかけるセットアップ</figcaption>
</figure>

二つの光子が時間差を持って光ファイバーに入射する。
50:50のビームスプリッターでパス$a,b$にわかれる。
パス$a$の方には、先に光子が入射した場合にのみ電場がかかるように、時間を制限した電場をかける。
(電場がかかる部分は複屈折結晶になっていると思えばよい。)
ふたつのパスはビームスプリッターで合流し、またわかれていく。
時間差できた光子が合流するように、ビームスプリッターの位置を調整する[^3]。
電場の影響はPockels効果として入れる。
(これは、Pockels効果を光子が得られるような複屈折結晶を用意するということである[^4]。)

Hamiltonianは次のように書ける。 $$\begin{equation}
\begin{split}
H(t) &= H_0 + H_{\text{int}} + H_P(t)\\
H_0 &= \hbar\omega_a a^\dagger a + \hbar\omega_b b^\dagger b\\
H_{\text{int}} &= i\hbar g (a^\dagger b - b^\dagger a)\\
H_P(t) &= \hbar\omega_P \Theta(t) E a^\dagger a \\
\end{split}
\end{equation}$$
ここで、$H_0,H_{\text{int}},H_P$はそれぞれ、光子のエネルギー、ビームスプリッターによる作用、電場による作用である。
$\Theta$はステップ関数で、うまく粒子がきたときのみ電場をあてる関数である。

(10/16追記)量子ドットからphotonを2個出す生成演算子を$A^\dagger$とし、BSの作用はユニタリであるはずだから、$U_{\text{BS}}$とすると、
$$\begin{align}
U_\text{BS} A^\dagger \ket{0} = \ket{aa} + \ket{ab} + \ket{ba} + \ket{bb}
\end{align}$$ と書けるはずである。 Post
Selectionを用いて、ある地点で2光子の間の位相を測り、位相が等しい状態を捨てることにすると、
$$\begin{align}
U_\text{BS} A^\dagger \ket{0} \to \ket{ab} + \ket{ba}
\end{align}$$ を考えればよいことになる。
エネルギー固有ブラを左から書けると、それぞれの状態の位置表示波動関数の複素共役になる。
$$\begin{align}
\bra{2} U_\text{BS} A^\dagger \ket{0} \to \bra{2}(\ket{ab} + \ket{ba}) = \bra{2}\ket{ab}(1+\frac{\braket{2}{ba}}{\braket{2}{ab}})
\end{align}$$ となる。 ここで、仮定として $$\begin{align}
\braket{2}{ab} \overset{?}{=} e^{i\theta}\braket{2}{ba}
\end{align}$$ であれば、 $$\begin{align}
\bra{2} U_\text{BS} A^\dagger \ket{0} \to \bra{2}\ket{ab}(1+e^{-i\theta})
\end{align}$$ であるはずである。
ただし、$\theta$については、Kerr効果が位相として入るとすると
$$\begin{align}
\theta = \frac{2\pi}{\lambda} \Delta n L = \frac{2\pi}{\lambda} n_2 I L
\end{align}$$
だが、時間成分のみを持つゲージ場による位相(AC効果)が入ると思うと
$$\begin{align}
\theta = \frac{e}{\hbar}\oint A^\mu dx_\mu = \frac{e}{\hbar}\int_0^L \phi dx
\end{align}$$ である。
磁場はないので、スカラーポテンシャルのみの積分を考えた。
複屈折結晶はKerr効果を持つとし、光の強度を$I$とした(Kerrでできるのか要検討)。
考えてみれば、AB効果が入る方が自然な気がする・・・。
1光子に$\lambda$があると思えない。

BSを50:50にするには、光子がBSにとどまっている時間:相互作用時間$\tau$を用いて
$$\begin{equation}
\begin{split}
g \tau = \frac{\pi}{4}
\end{split}
\end{equation}$$ になるようにすればよい(証明はあとで)。

光ファイバーのパスを並行にとり、その方向に光子が進む速度を$\boldsymbol{v}$とする。
これは、進んでいる場所の屈折率を$n$として、 $$\begin{equation}
\begin{split}
\boldsymbol{v} &= \frac{c}{n} \hat{\boldsymbol{e}}\\
\end{split}
\end{equation}$$
ここで、$\hat{\boldsymbol{e}}$は光ファイバーの進行方向を表す単位ベクトルである。

.5ex plus .2ex minus .2ex2サイト模型への帰着:保留中

これを光子の速度$u$で進む非慣性系から見ることで、2サイト光子模型になるはずである。
光の伝播方向と系の進む方向の間の$\theta$として、Doppler効果は
$$\begin{equation}
\begin{split}
\omega' = \omega \frac{\sqrt{1-(u/c)^2}}{1-(u/c)\cos\theta}
\end{split}
\end{equation}$$ となるから、これによるエネルギーシフトを考えればよい。

ビームスプリッターの結合定数もシフトする(途中)。

課題:
2サイト模型にすると、時間によってサイトの性質が変わる必要があるが、そのような模型にできるか?
すなわち、電場をかけている時刻とかけていない時刻でサイトの性質がかわる。
これはサイトの性質が時間依存する。
単なるhubberd模型ではなくなりそうである。\
これを解決するため、3サイト模型にして、そのうち2サイトを電場がかかるサイトにするのはどうか。
それらのサイトにはステップ関数で一時的なハードコア条件のようなものを課すことで実現できる気がする。

.5ex plus .2ex minus .2ex擬一次元系でのboson場の演算子の統計性
1次元光子はBose統計に従うのか?
厳密に1次元であれば電場、磁場は存在しない。
擬一次元系として考えると、厳密には3次元であるため、光子はBose統計に従う。

.5ex plus .2ex minus .2ex光学効果 .5ex plus .2ex minus .2ex線形光学
この章は[@hattori]の付録Bを参考にした。

まず線形光学についてまとめる。

電気感受率$\chi$と屈折率$\epsilon$、位相のかかわりを以下にまとめる。

実数の屈折率$n$は、 $$\begin{align}
n \coloneqq \sqrt{\frac{\epsilon_0}{\epsilon}}
\end{align}$$ で定義される。

電場があまり大きくない時、媒質内の分極$\boldsymbol{P}$は線形に電場$\boldsymbol{E}$に比例する。
この時、電気感受率$\chi$を $$\begin{align}
\boldsymbol{P} = \epsilon_0 \chi \boldsymbol{E}
\end{align}$$ によって定義する。

誘電率$\epsilon$は、電束密度と電場の比例関係の比例係数であるから、
$$\begin{align}
\boldsymbol{D} = \epsilon \boldsymbol{E} = \epsilon_0 \boldsymbol{E} + \boldsymbol{P} = \epsilon_0 (1+\chi) \boldsymbol{E}
\end{align}$$ となる。

これより、電気感受率と屈折率の関係は、 $$\begin{align}
n^2 = \epsilon_r = 1 + \chi
\end{align}$$ である。 位相は $$\begin{align}
\phi = kL = \frac{2\pi}{\lambda}nL
\end{align}$$ となる。

.5ex plus .2ex minus .2ex電磁場の量子化 量子化の手続きについてまとめる。
この章は[@Gerry_Knight_2004]を参考にした。
考えている空間の体積を$V$とし、偏光の方向を$s$とする。
単一モードであれば、$x$方向の電場演算子は $$\begin{align}
\hat{E}_x=\mathcal{E}_0 (\hat{a}e^{-i\omega t} + \hat{a}^\dagger e^{i\omega t})\sin(kz)
\end{align}$$ となる。 複数モードであれば、 $$\begin{align}
\hat{\boldsymbol{E}}(\boldsymbol{r},t) = i \sum_{\boldsymbol{k},s} \sqrt{\frac{\hbar \omega_k}{2\epsilon_0 V}} \boldsymbol{e}_{\boldsymbol{k},s} \left( \hat{a}_{\boldsymbol{k},s}  e^{i(\boldsymbol{k}\cdot\boldsymbol{r}-\omega_k t)} - \hat{a}^\dagger_{\boldsymbol{k},s}  e^{-i(\boldsymbol{k}\cdot\boldsymbol{r}-\omega_k t)} \right)
\end{align}$$ となる。 また、磁場は $$\begin{align}
\hat{\boldsymbol{B}}(\boldsymbol{r},t) = \frac{i}{c} \sum_{\boldsymbol{k},s} \sqrt{\frac{\hbar }{2\epsilon_0 V \omega_k}} (\boldsymbol{\hat{k}}\times \boldsymbol{e}_{\boldsymbol{k},s}) \left( \hat{a}_{\boldsymbol{k},s}  e^{i(\boldsymbol{k}\cdot\boldsymbol{r}-\omega_k t)} - \hat{a}^\dagger_{\boldsymbol{k},s}  e^{-i(\boldsymbol{k}\cdot\boldsymbol{r}-\omega_k t)} \right)
\end{align}$$ となる。 ここで、$\hat{\boldsymbol{k}}$は単位波数ベクトルである。
波数の間隔が十分小さければ、和は $$\begin{align}
\sum_{\boldsymbol{k}} \to \frac{V}{(2\pi)^3} \int d^3 \boldsymbol{k}
\end{align}$$ と書き換わる。

場の演算子で書く。

.5ex plus .2ex minus .2ex非線形光学

::: itembox
**Def. 非線形感受率**
非線形性があまり大きくないと仮定して、非線形感受率$\chi^{(n)}$を以下で定義する[@hattori]。
$$\begin{align}
\boldsymbol{P(t)}&= \epsilon_0 \left( \chi^{(1)}\boldsymbol{E(t)} + \chi^{(2)}\boldsymbol{E^2(t)} + \chi^{(3)}\boldsymbol{E^3(t)} + ... \right)\\
&=\boldsymbol{P}^L + \boldsymbol{P}^{NL}
\end{align}$$ ここで、 $$\begin{align}
\boldsymbol{P}^L &= \epsilon_0 \chi^{(1)}\boldsymbol{E(t)}\\
\boldsymbol{P}^{NL} &= \epsilon_0 \left( \chi^{(2)}\boldsymbol{E^2(t)} + \chi^{(3)}\boldsymbol{E^3(t)} + ... \right)
\end{align}$$ はそれぞれ線形感受率と非線形感受率と呼ばれている。

非線形分極のうち、電場の$n$乗に比例する項$\boldsymbol{P}^{(n)}=\epsilon_0 \chi^{(n)}\boldsymbol{E}^{\boldsymbol{n}}$を$n$次の非線形分極と呼び、$\chi^{(n)}$はn次非線形感受率と呼ばれる[^5]。
:::

屈折率が電場の1次に比例する効果をPockels効果と呼び[^6]、2次に比例する効果をKerr効果と呼ぶ[@hattori]。

## Sections

- [[01-pockels|Pockels効果]]
- [[02-kerr|光Kerr効果]]
- [[03-section|時間発展と位相獲得]]

← [[anyon/index|Anyon theory]]
