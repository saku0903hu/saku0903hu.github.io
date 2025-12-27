# これからの研究計画: エニオン量子コンピュータについて

.5ex plus .2ex minus .2ex考えていることと研究の計画
私はanyonで面白いことがしたいと考えています。
また、手の中で作れるものであり、まだ実現していないものを作りたいと考えています。

それに当てはまるものとして、量子コンピュータがあります。
anyonを用いた量子コンピュータとして、トポロジカル量子コンピュータ($\in$誤り耐性fault
tolerant量子コンピュータ)が知られています。 fault
tolerant量子コンピュータ(FTQC)は、量子ビットのエラーを訂正しながら計算を行う量子コンピュータです。

FTQCに関する日本語の資料は藤井
啓祐さんの『量子計算超入門』<https://quantphys.org/keisukefujii/tokyotopological.pdf>があります。
自分は今これを読んでいます(10/18現在)。

.5ex plus .2ex minus .2ex現状の把握
エニオン量子コンピュータは、非可換エニオンの交換統計を利用し、トポロジカルな量子情報処理を実現することを目指すアーキテクチャです。
エニオンのトポロジカル性により、量子情報が局所的なノイズや誤りに対して本質的に耐性を持つため、フォールトトレラントな量子計算の有力候補とされています[@pachos2016short; @Lauda2024universal; @plugge2024spin]。
以下では文献を紹介します。
トピックを拾っているのみで、真面目に読めているものはほとんどないです。\
.5ex plus .2ex minus .2exエニオンとトポロジカル量子計算
エニオンは2次元系に現れる準粒子であり、特に非可換エニオンは粒子の交換（braiding）によって量子状態空間内で非自明なユニタリ操作を実現します。これにより、量子ビットや量子ゲートをトポロジカルに実装でき、局所的な誤りに対して耐性を持ちます[@pachos2016short; @plugge2024spin]。
anyonと量子計算についての理論論文はKitaevのFault-tolerant quantum
computation by
anyons<https://arxiv.org/abs/quant-ph/9707021>があります。 Kitaev
toric-codeのHamiltonianは、素励起がabelian anyonとして振る舞います。
任意の計算ができるユニバーサルゲートセットを作るにはnon abelian
anyonが必要です。 この拡張もしています。
また、これをゲージに対して一般化したのがKitaevのQuantum double
modelであり、同論文で定義されています[^51]。

レビュー論文としては、[@pachos2016short]があります。\
.5ex plus .2ex minus .2exユニバーサル量子計算性、スピン液体
[@Lauda2024universal]では、トポロジカル超伝導体やFQHE系における非可換エニオンは研究されてきたといい、磁気トンネル接合アレイに統合されたspin-liquid、半導体-spin
liquidを用いています。
spin-liquidとしては$\alpha$-RuCl$_3$を用いています。

.5ex plus .2ex minus .2ex実装プラットフォームと進展
量子Hall系の実験はGaAsやvan der Waalsヘテロ構造体で行われています[^52]。
GaAs系では、以下のように発展してきました。 MZI: Mach-Zehnder
Interferometer, FPI: Fabry-Pérot Interferometerです。

::: {#tab:GaAs_experiments}
   FQH odd   FQH even   IQH MZI   IQH FPI   FQH odd FPI   abelian braiding
  --------- ---------- --------- --------- ------------- ------------------
    1982       1987      2003      2009        2019             2020

  : GaAs系の実験的進展
:::

一方、van der Waals系(grapheneなど)では以下のように発展しています。

::: {#tab:vdW_experiments}
   FQH odd   FQH even   IQH MZI   IQH FPI   abelian braiding
  --------- ---------- --------- --------- ------------------
    2009       2014      2017      2020           2024

  : vdW系の実験的進展
:::

.5ex plus .2ex minus .2ex分数量子ホール効果系
エニオンがすでに観測されているものとして、**分数量子ホール効果
(Fractional Quantum Hall Effect, FQHE)** が観測される二次元電子ガス
(2DEG) があります。

- **GaAs/AlGaAsヘテロ構造**:
  高移動度の二次元電子ガスを形成する古典的な材料系であり、様々な分数量子ホール状態が実現されています。特に、$\nu = 5/2$
  状態は非可換エニオン（Isingエニオン）の物理的実現候補として広く研究されています[@nayak2007anyon].

.5ex plus .2ex minus .2exトポロジカル超伝導体
トポロジカル超伝導体中のマヨラナ零モードは、非可換エニオンの一例であり、ナノワイヤや磁性原子鎖などでの実装が進められています。マヨラナモードのbraidingによる量子ゲート操作の実証が目指されています[@pachos2016short; @plugge2024spin]。

.5ex plus .2ex minus .2ex超伝導回路
超伝導量子回路上でグラフ頂点の非可換braidingを実現する実験が報告されており、人工的なエニオン統計の制御が進展しています[@google2023nonabelian]。
トランズモン回路を作っている?

.5ex plus .2ex minus .2ex時空間領域干渉法によるエニオン統計の検出
「*Anyon statistics through conductance measurements of time-domain
interferometry*」という論文では、時空間領域干渉法を用いたコンダクタンス測定によってエニオン統計を検出する可能性を探っています[@goldstein2023anyon]。分数量子ホール効果（FQHE）系において、エッジ状態を利用した干渉実験は、アベリアンエニオンの統計性を検証する有力な手法とされており、この研究はエニオンの基本的な特性を実験的に探るものです。

.5ex plus .2ex minus
.2exポンププローブ分光によるエニオンブレイディングの検出 「*Detection of
anyon braiding through pump-probe
spectroscopy*」という論文では、ポンププローブ分光法を用いてエニオンのブレイディングを検出する新しい手法を提案しています[@sugimoto2025detection]。このアプローチは、エニオンのダイナミクスをリアルタイムで観測し、その非可換な特性を詳細に調べるための新たな道を開くものです。これは、量子情報処理におけるエニオンの制御技術の進展に貢献する可能性があります。

.5ex plus .2ex minus .2exエニオンコリジョンによる統計性の研究
「*Non-Abelian Anyon
Collider*」という論文は、エニオンコリジョン実験によってエニオンの統計性を研究するアプローチを提案しています[@stern2022nonabelian]。
量子ポイントコンタクトを用いた時間領域干渉計やエニオンコリジョン実験は、エニオンの交換統計やバンチング・アンチバンチング現象を観測するのに役立ちます。
これは、エニオンの特異な統計的性質を直接的に検証するための実験的な枠組みを提供します。

.5ex plus .2ex minus .2ex半導体との関わり・理論的な研究
半導体におけるエニオンの理論的研究は、主にトポロジカル物質科学や量子物性物理の発展と密接に関連しています。

.5ex plus .2ex minus .2exトポロジカル絶縁体におけるエニオン応答
トポロジカル絶縁体の磁気秩序化状態では、エニオン場が量子化され、磁電効果や層ホール効果などの現象が現れます。
例えば、のような材料では、層自由度に由来する**層ホール効果**や**非散逸的伝導**がエニオン場によって記述され、デバイス応用への可能性が示されています[@pan2023dissipationless; @wang2024high_pmc]。

.5ex plus .2ex minus .2exエニオン理論とトポロジカル磁性体・マグノン
磁性トポロジカル絶縁体やトポロジカルマグノン絶縁体では、エニオン場がスピン波（マグノン）のトポロジーや伝搬特性に影響を与えることが理論・実験の両面から示されています[@fang2021topological; @wang2023understanding; @pan2023dissipationless]。

.5ex plus .2ex minus .2ex半導体との関わり・実験的な研究

.5ex plus .2ex minus .2exトポロジカル超伝導体とマヨラナフェルミオン
非アーベル統計を持つ準粒子としてマヨラナフェルミオンがあります。
半導体-超伝導体ハイブリッド構造を用いた実験でその証拠が探されています[@nichele20174piperiodic]。

トポロジカル超伝導体は、その表面やエッジにマヨラナフェルミオンと呼ばれる非アーベル統計を持つ準粒子を宿すことが期待されており、これも非可換エニオンの一種と見なすことができます。

- **半導体ナノワイヤと超伝導体のハイブリッド構造**:
  InAsやInSbなどの半導体ナノワイヤをNbやAlなどの超伝導体と接合させることで、マヨラナフェルミオンを生成する実験が進行中です[@nichele20174piperiodic]。

- **トポロジカル絶縁体/超伝導体ヘテロ構造**:
  HgTe/CdTe量子井戸やBi$_2$Se$_3$などのトポロジカル絶縁体と超伝導体を組み合わせることで、界面にマヨラナフェルミオンを誘起する研究も行われています。

- **鉄系超伝導体、銅酸化物超伝導体**:
  これらの強相関電子系でも、特定の条件下でトポロジカル超伝導状態が実現される可能性が議論されています[@sato2016topological]。

.5ex plus .2ex minus .2exハイブリッド構造を用いたエニオンの探索
半導体ナノワイヤと超伝導体を組み合わせた構造や、特定の結晶構造を持つ二次元材料において、エニオン的な振る舞いを示す準粒子の創出や検出を目指す実験が行われています[@larsen2015]。

.5ex plus .2ex minus
.2exエニオン場（アクシオン場）の導入(これはここに入れるべきか?)
元々高エネルギー物理学でCP対称性の破れを説明するために導入されたアクシオン場は、固体物理学ではトポロジカル絶縁体や磁性体の電磁応答を記述する有効場[^53]として現れます。
半導体では、**トポロジカル絶縁体**や**磁性半導体**において、エニオン場が磁電効果や層ホール効果などの新奇な現象を特徴づける理論的枠組みとして用いられています[@wang2024high_arxiv; @wang2024high_pmc; @pan2023dissipationless; @wang2023understanding].
アクシオンに関しては、ダークマターの候補であることから、まずアクシオンを作ることが難しいと思います。

.5ex plus .2ex minus .2exトポロジカル絶縁体におけるアクシオン応答
のような磁性トポロジカル絶縁体では、アクシオン絶縁体相での特異な輸送現象、例えば量子化された磁気電気効果や異常ホール効果などが実験的に観測されており、これが理論的なエニオン（アクシオン）応答と関連付けられています[@pan2023dissipationless; @wang2023understanding; @wang2020evidence; @wang2021strongly]。これらの実験は、温度、磁場、ゲート電圧などの外部パラメータを変化させることで、エニオンに起因する現象を制御・検証しようと試みています。
また、**高スピンアクシオン絶縁体**では、スピン数に応じてエニオン場の値が変化し、層トポロジーや磁電効果の制御が可能となることが理論的に示されています[@wang2024high_arxiv; @wang2024high_pmc]。

アクシオン電磁気学は、以下のようなラグランジアン密度で記述されます。
$$\mathcal{L}_{\text{axion}} = \frac{1}{2} (\partial_{\mu} \phi)^2 - V(\phi) - \frac{1}{4} F_{\mu\nu} F^{\mu\nu} - \frac{\theta}{4\pi} \mathbf{E} \cdot \mathbf{B}$$
ここで、$\phi$ はアクシオン場、$\theta$
はアクシオン結合定数、$\mathbf{E}$ は電場、$\mathbf{B}$
は磁場を表します。固体物理学では、$\theta$
は系に依存した定数として扱われることが多いです。

.5ex plus .2ex minus .2exその他の候補材料

- **二次元遷移金属ダイカルコゲナイド (2D TMDs)**: MoS$_2$, WS$_2$,
  WS$_2$などの2D
  TMDsは、強い層間結合と高いキャリア移動度、ならびにエキシトンやトリオン（荷電エキシトン）生成の容易さから、量子光学や励起子物理のプラットフォームとして注目されています[@wang2023alloptical; @wang2022drift; @wang2023quantum_pmc; @wang2023quantum_science]。これらの系で、局所的なポテンシャル操作による準粒子の空間制御や、将来的なエニオン探索への応用が期待されます。

- **量子スピン液体**:
  量子スピン液体は、分数量子励起を伴うトポロジカルオーダーを持つ物質であり、非可換エニオンの候補としても研究されています[@vaezi2024spin][^54]。カゴメ格子などの幾何学的フラストレーションを持つ磁性体でその実現が期待されています。

.5ex plus .2ex minus .2exエニオンの実験のための手法 .5ex plus .2ex minus
.2ex\*電気的輸送測定

- **ホール抵抗測定**:
  量子ホール効果において、分数量子ホール状態のホール抵抗のプラトーを観測することで、エニオンの分数量子統計を示す証拠が得られます。

- **ショットノイズ**:
  電流の微小な揺らぎ（ショットノイズ）を測定することで、エニオンの有効電荷や統計性を評価できます。特に、分数量子ホール状態でのショットノイズ測定は、エニオンの存在を示す重要な手法です[@Lee_2019]。

.5ex plus .2ex minus .2ex\*量子情報科学からのアプローチ

- **エンタングルメントエントロピーの測定**:
  基底状態のエンタングルメントエントロピーを測定することで、トポロジカルエンタングルメントエントロピー
  (TEE)
  を抽出し、トポロジカル秩序の存在やエニオンの量子次元を診断することができます[@zhang2023anyon_arxiv; @zhang2023anyon_pmc]。

- **エニオンのブレイディング操作**:
  量子ゲート操作としてエニオンを物理的に移動させて交換する「ブレイディング」や、測定のみによってブレイディング変換を生成する「測定のみのトポロジカル量子計算」も理論的に提案されています[@bonderson2008measurement]。これらの操作は、将来的なトポロジカル量子コンピュータの実現に向けた核心技術となります。

::: thebibliography
99

J. K. Pachos, A Short Introduction to Topological Quantum Computation,
<https://scipost.org/10.21468/SciPostPhys.3.3.021/pdf> Aaron D.Lauda,
Universal quantum computation using Ising anyons from a non-semisimple
Topological Quantum Field Theory, <http://arxiv.org/pdf/2410.14860.pdf>
R. Ainsworth and J. K. Slingerland , Topological Qubit Design and
Leakage, <https://arxiv.org/pdf/1102.5029.pdf> Kai Klocke et al.,
Spin-liquid-based topological qubits,
<https://arxiv.org/pdf/2411.08093.pdf> Google Quantum AI et al.,
Non-Abelian braiding of graph vertices in a superconducting processor,
<https://pmc.ncbi.nlm.nih.gov/articles/PMC10247379/>

N. Schiller et al., Anyon statistics through conductance measurements of
time-domain interferometry, <https://arxiv.org/abs/2301.00021>

X.Yang et al., Detection of anyon braiding through pump-probe
spectroscopy, <https://arxiv.org/abs/2503.22792>

M.Lee et al., Non-Abelian Anyon Collider,
<https://arxiv.org/pdf/2202.03649.pdf>

Shuai Li, et al. (2024). *High spin axion insulator*. arXiv preprint
arXiv:2404.12345. <https://arxiv.org/pdf/2404.12345.pdf> Shuai Li, et
al. (2024). High spin axion insulator. *PMC*.
<https://pmc.ncbi.nlm.nih.gov/articles/PMC11102527/> Shuai Li, et al.
(2023). Dissipationless layertronics in axion insulator MnBi2Te4.
*National Science Review*.
<https://academic.oup.com/nsr/advance-article-pdf/doi/10.1093/nsr/nwad262/51994113/nwad262.pdf>
Jian-Rui Soh, et al. (2023). Understanding unconventional magnetic order
in a candidate axion insulator by resonant elastic x-ray scattering.
*PMC*. <https://pmc.ncbi.nlm.nih.gov/articles/PMC10256702/> Wenqin Chen,
et al. (2024). Gauge theory of giant phonon magnetic moment in doped
Dirac semimetals. *arXiv preprint arXiv:2405.10318*.
<http://arxiv.org/pdf/2405.10318.pdf> Joan Bernabeu, et al. (2025).
Axionic Acoustic Phonons. *arXiv preprint arXiv:2502.01471*.
<https://arxiv.org/pdf/2502.01471.pdf> Yanyu Jia, et al. (2020).
Evidence for a Monolayer Excitonic Insulator. *arXiv preprint
arXiv:2010.05390v1*. <http://arxiv.org/pdf/2010.05390v1.pdf> Youn Jue
Bae, et al. (2021). Strongly correlated excitonic insulator in atomic
double layers. *arXiv preprint arXiv:2104.05066*.
<https://arxiv.org/pdf/2104.05066.pdf> Fengfeng Zhu, et al. (2022).
Exciton-Coupled Coherent Magnons in a 2D Semiconductor. *arXiv preprint
arXiv:2201.13197*.
<https://arxiv.org/ftp/arxiv/papers/2201/2201.13197.pdf> Yao-Wen Fang,
et al. (2021). Topological magnon insulators in two-dimensional van der
Waals ferromagnets CrSiTe3 and CrGeTe3. *PMC*.
<https://pmc.ncbi.nlm.nih.gov/articles/PMC8442887/> Mauricio Bejarano,
et al. (2024). Parametric magnon transduction to spin qubits. *PMC*.
<https://pmc.ncbi.nlm.nih.gov/articles/PMC10954226/> E Rongione , et al.
(2023). Emission of coherent THz magnons in an antiferromagnetic
insulator triggered by ultrafast spin--phonon interactions. *PMC*.
<https://pmc.ncbi.nlm.nih.gov/articles/PMC10066367/> Moyu Chen, et al.
(2024). Selective and Quasi-continuous Switching of Ferroelectric Chern
Insulator Device for Neuromorphic Computing. *arXiv preprint
arXiv:2407.17010*. <https://arxiv.org/pdf/2407.17010.pdf> Qing Yan, et
al. (2024). Rules for dissipationless topotronics. *PMC*.
<https://pmc.ncbi.nlm.nih.gov/articles/PMC11152134/> Matthew J Gilbert,
et al. (2024). Chern networks: reconciling fundamental physics and
device engineering. *PMC*.
<https://pmc.ncbi.nlm.nih.gov/articles/PMC12032342/> Chaoyu Chen, et al.
(2023). Fabrication of a novel magnetic topological heterostructure and
temperature evolution of its massive Dirac cone. *PMC*.
<https://pmc.ncbi.nlm.nih.gov/articles/PMC7515900/>

J Wiedenmann, et al. (2017). 4$\pi$-periodic Josephson supercurrent in
HgTe-based topological Josephson junctions. *Nature Materials*, 16(2),
273-278. <https://pmc.ncbi.nlm.nih.gov/articles/PMC4735757/> Y. P. Wang,
et al. (2019). High-frequency rectifiers based on type-II Dirac
fermions. *Nature Photonics*, 13(12), 856-860.
<https://pmc.ncbi.nlm.nih.gov/articles/PMC7952558/> Libo Zhang, et al.
(2013). Tunable Dirac Fermion Dynamics in Topological Insulators. *Nano
Letters*, 13(7), 3020-3025.
<https://pmc.ncbi.nlm.nih.gov/articles/PMC3740283/> T.W. Larsen, et al.
(2015). Semiconductor-Nanowire-Based Superconducting Qubit.
<https://arxiv.org/abs/1503.08339>

C. Nayak, et al. (2007). Why should anyone care about computing with
anyons? *arXiv preprint arXiv:0704.2241*.
<https://arxiv.org/pdf/0704.2241.pdf>

F. S. Nichele, et al. (2017). 4$\pi$-periodic Josephson supercurrent in
HgTe-based topological Josephson junctions. *Nature Materials*, 16(2),
273-278. <https://pmc.ncbi.nlm.nih.gov/articles/PMC4735757/> M. Sato, et
al. (2016). Topological superconductors: a review. *arXiv preprint
arXiv:1608.03395*. <http://arxiv.org/pdf/1608.03395.pdf>

Yadong Pan, et al. (2023). Dissipationless layertronics in axion
insulator MnBi2Te4. *National Science Review*.
<https://academic.oup.com/nsr/advance-article-pdf/doi/10.1093/nsr/nwad262/51994113/nwad262.pdf>
Yujie Wang, et al. (2023). Understanding unconventional magnetic order
in a candidate axion insulator by resonant elastic x-ray scattering.
*PMC*. <https://pmc.ncbi.nlm.nih.gov/articles/PMC10256702/>

Y. Wang, et al. (2023). All-optical control of high-purity trions in
nanoscale waveguide. *PMC*.
<https://pmc.ncbi.nlm.nih.gov/articles/PMC10097695/> Y. Wang, et al.
(2022). Drift-dominant exciton funneling and trion conversion in 2D
semiconductors on the nanogap. *PMC*.
<https://pmc.ncbi.nlm.nih.gov/articles/PMC8816338/> Y. Wang, et al.
(2023). Quantum control of exciton wave functions in 2D semiconductors.
*PMC*. <https://pmc.ncbi.nlm.nih.gov/articles/PMC10954220/> Y. Wang, et
al. (2023). Quantum control of exciton wave functions in 2D
semiconductors. *Science Advances*.
<https://www.science.org/doi/pdf/10.1126/sciadv.adk6369?download=true>

A. Vaezi, et al. (2024). Spin-liquid-based topological qubits. *arXiv
preprint arXiv:2411.08093*. <https://arxiv.org/pdf/2411.08093.pdf>

S. Mukherjee, et al. (2022). Ultrafast imaging of polariton propagation
and interactions. *arXiv preprint arXiv:2205.01176*.
<https://arxiv.org/ftp/arxiv/papers/2205/2205.01176.pdf> Y. Wang, et al.
(2022). Ultrafast Thermionic Electron Injection Effects on Exciton
Formation Dynamics at a van der Waals Semiconductor/Metal Interface.
*ACS Photonics*.
<https://pubs.acs.org/doi/pdf/10.1021/acsphotonics.2c00394>

X. Zhang, et al. (2023). Anyon Quantum Dimensions from an Arbitrary
Ground State Wave Function. *arXiv preprint arXiv:2304.13235v2*.
<https://arxiv.org/html/2304.13235v2> X. Zhang, et al. (2023). Anyon
quantum dimensions from an arbitrary ground state wave function. *PMC*.
<https://pmc.ncbi.nlm.nih.gov/articles/PMC11180095/> A. Bonderson, et
al. (2008). Measurement-Only Topological Quantum Computation via Anyonic
Interferometry. *arXiv preprint arXiv:0808.1933*.
<https://arxiv.org/pdf/0808.1933.pdf> B.Lee et al., (2019). Negative
Excess Shot Noise by Anyon Braiding <https://arxiv.org/abs/1907.00532>
:::

## Sections

