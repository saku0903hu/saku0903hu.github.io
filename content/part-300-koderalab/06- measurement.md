---
title: 06.測定について
date: 2026-05-14
tags:
  - koderalab
---
## 
P2-B2特性でうまくCharge sensorが見えないときはLB1-LB2特性から見直す
ampのチェック
gain
directivity
5V

currentをcheckして合ってたらgainをcheck

はんだで着ける
石川大でテストしてもいい
VNAが石川台にある

data pointは図の1点にあるポイント数

QDAC sweepをするときとsingle shotをするときのdata pointの変化？

### QDAC sweepの例
decimation=5 
integration time=1e-06 s
sampling_freq=3,125,000.0 Hz
data_point=4 samples
Loading decimator FPGA image.
readout setting has finished

### single shotの例
decimation=12 
integration time=0.1 s
sampling_freq=24,414.0625 Hz
data_point=2,442 samples
Loading decimator FPGA image.
readout setting has finished

-1.315 -1.313

coulomb peakのqdac sweepからsingle shotをするときはvariable initializationをする

次はtime domain measurement

2 level fluctuator : parasidic QDかもしれない

#  single shot measurement

量子状態は直接観測すると、重ね合わせが壊れる。
そのため、量子TPや量子誤り検出などの量子プロトコルの実行の他mには量子状態を単一試行で読み出す必要がある。
この単発測定は緩和時間より短く行われる必要がある。
SNRの改善のために試行回数を増やしたり積算時間を増やしたりすることはこの事情により禁止される。

単一キャリアの電子スピンのスピン状態のエネルギー緩和時間は典型的に $T_1 \approx 100 ms$ なのでこれを十分早く行う必要がある。

・磁気モーメントを直接観測する方法について https://www.nature.com/articles/nnano.2013.169
これは要求される感度を達成するのが難しい。

そこで、スピン状態を量子ドットないの電子数変化の有無に対応させるspin -charge conversionである。

QND electron https://www.nature.com/articles/s41467-020-14818-8
QND in Si electron https://doi.org/10.1038/s41467-020-14818-8

電子数変化は量子コンダクタンスの量子化の変化中の領域を用いて行える。

QCのためには、測定時間が演算時間の制限になるから、位相緩和時間( $T_2^* \approx 100 \mu s$ )内の読み出しを可能とする1~10MHz以上の広帯域での測定が望ましいが、帯域を広げるとノイズを拾う領域も大きくなるので、読み出しにおけるSNRと測定帯域はトレードオフが存在する。

RF 反射測定は測定技法からトレードオフの限界に挑むアプローチである。

### SNR（信号対雑音比）とは

この論文 https://journals.aps.org/prapplied/abstract/10.1103/PhysRevApplied.6.054013 では、単一電子が量子ドットに出入りする「リアルタイムのトンネル現象」を観測することでSNRを評価しています 。

- **信号（Signal）：** センサーとなる量子ドットを流れる電流は、隣接する量子ドットに電子が「0個」か「1個」かによって2つのレベルにスイッチングします 。1秒間の電流データをヒストグラム（分布図）にすると、この2つの状態に対応する2つのガウス分布のピークが現れます 。この2つのピークの中心間の距離（電流の差）が、電子1個分の変化を示す「信号（ΔI）」となります 。
    
- **雑音（Noise）：** ヒストグラムに現れた各ガウス分布のピークの広がり（標準偏差）が、測定システムの「電流ノイズ（σI）」を表しています 。
    
- **SNRの計算：** SNRは、得られた信号をノイズで割った値です 。
    
    $$\text{SNR} = \frac{\Delta I}{\sigma_I}$$
    

2つの\sigmaが違うことがあるので、それぞれ片方を使ったものと平均したsigmaを使ったものの3種類を出力。

\Delta I = 0.005979
/sigma_0 = 

SNR vs int time
SNR vs sampling rate

intimeが増えると積分に時間がかかるから測定時間が伸びる

### 2. Charge Sensitivity（電荷感度）とは

電荷感度は、センサーが1ヘルツ（Hz）の帯域幅あたりに検出できる最小の電荷量を示す指標です。この値が小さいほど、より微小な電荷の変化を見分けることができる（＝感度が高い）ことを意味します。論文では、測定されたSNRと、アンプなどの測定機器が持つ実効的な測定帯域幅（バンド幅）を組み合わせて算出されています 。

帯域幅（f）に依存するノイズは、以下の積分式で定量化されています 。

$$\sigma_I^2(f) = \int_{1\text{ Hz}}^f i_n^2(f')df'$$

### 3. 論文における具体的な測定値と成果

論文の実験では、以下のような極めて優秀な数値が報告されています。

- **測定された信号とノイズ：** 電流の信号は ΔI = 0.772 nA、電流ノイズは σI = 0.112 nA と測定されました 。
    
- **達成したSNR：** 30 kHzの測定帯域幅において、SNR = 6.9 を達成しています 。
    
- **優れた電荷感度：** 算出された実効的な電荷感度は 8.2 × 10⁻⁴ e/√Hz でした 。
    
- **他技術との比較：** この感度は、rf QPC（約 10⁻³ e/√Hz）や、分散型ゲート読み出し（6.3 × 10⁻³ e/√Hz）といった他の主要な読み出し技術よりも高い（優れた）数値です 。
    
- **今後の課題と展望：** 現在の測定帯域幅（30 kHz）は室温の電流アンプによって制限されています 。低温プリアンプとより広帯域な室温アンプを組み合わせることで、SNRと測定帯域幅をさらに向上させることが可能だと述べられています 。
-

図の見方：

noise 
data = I 
data2 =Q

spin qubit 

mizokiuchiさんのabstruct読む「
JSAPだとどれくらいのnoveltyが必要か調べる
PSB DQDはnoveltyない
何をすればいいか？
fidelityのupdateは難しい

todo
abstruct, make DQD

## DQD 
B1= B2~-1.1V,
P1とP2をsweep

Charge sensorの場所を変えるならLB1,LB2を変える：ここがCSなので

P1,P2にだけAWGがつながっているのでP1,P2 sweepの時だけAWG。だけどQDACの方が広くsweepできるので、一旦QDACでsweepして、tuneをAWGで行う。


Radio-Frequency-Detected Fast Charge Sensing in Undoped Silicon Quantum Dots Akito Noiri,*,‡ Kenta Takeda,‡ Jun Yoneda, Takashi Nakajima, Tetsuo Kodera, and Seigo Tarucha*
https://pubs.acs.org/doi/full/10.1021/acs.nanolett.9b03847


Fidelity
https://www.nature.com/articles/s41534-024-00882-1

arakawa sanのSSDMの資料からacknowledgement
setup,PSB
