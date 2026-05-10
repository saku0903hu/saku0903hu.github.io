---
title: 01.回路
date: 2026-05-07
tags:
  - koderalab
---

## 回路メモ（整理版）

### Ohmic contact とは

金属配線と半導体を接続したとき、電流と電圧がオーム則に従う接触を **Ohmic contact** と呼ぶ。  
単に金属と半導体を接続すると、一般には **Schottky 障壁** が生じやすいため、障壁を抑えて線形な I-V 特性を得ることが重要。

---

### IQ demodulation

- I/Q で復調することで、搬送波そのものを保存せずに信号情報を扱える
- 実効的にデータ量を小さくできる
- Local oscillator（LO）を使ってミキシングする

---

### Attenuator（減衰器）

- 20 dB の減衰は、パワー比で $1/100$
- 室温から低温ステージへ入る熱雑音を抑えるため、段階的に減衰を入れる設計が一般的
- 各ステージで「必要信号レベル」と「熱雑音抑制」のバランスを取る

---

### Bias tee

- DC バイアスと RF 信号を同じ配線に重畳するために使う
- AC と DC を分離して扱える
- 寄生容量 $C_p$ は小さいほど望ましい場合が多い（実デバイス容量との兼ね合いが必要）

---

### その他メモ

- コイルの $Q$ factor の見積もり
- バラクタ（可変容量素子）の使いどころ
- Mixer は必要駆動パワーに合わせる
- デバイス入力は Attenuator で微調整
- VNA（Vector Network Analyzer）で S パラメータを測定

---

## パラメトリックアンプ

パラメトリックアンプは、非線形リアクタンス（主に可変容量）を利用して、微弱信号を低雑音で増幅する方式。

### 基本原理

- バラクタなどの非線形容量を利用
- ポンプ波（高周波）からエネルギーを供給し、信号波へ変換
- 抵抗性素子中心の増幅器に比べ、低雑音化が期待できる

### 量子計測での利用

- 代表例: JPA（Josephson Parametric Amplifier）
- 極低温環境で動作し、量子ビット読み出しの高感度化に有効
- 広帯域化の方向として JTWPA（進行波型）も重要

### 関連比較

- HEMT アンプ: 4 K 近傍で広く使われる低雑音アンプ
- パラメトリックアンプ: さらに低雑音が必要な場面で有利

参考:

- https://repository.dl.itc.u-tokyo.ac.jp/record/23490/files/sk011004001.pdf
- https://xtech.nikkei.com/atcl/nxt/column/18/02308/122800004/
- https://www.riken.jp/press/2025/20251030_1/index.html

---

## dBm

**dBm** は、1 mW を基準にした電力の対数表現。

- 1 nW = -60 dBm
- 1 μW = -30 dBm
- 1 mW = 0 dBm
- 1 W = 30 dBm
- 1 kW = 60 dBm

1 W 基準の dBW とは、

$$
\mathrm{dBW} = \mathrm{dBm} - 30
$$

の関係にある。

### 単位換算

電力 $P$（mW）と電力レベル $x$（dBm）の関係:

$$
x = 10\log_{10}\left(\frac{P}{1\,\mathrm{mW}}\right)
$$

電力を W で書くと:

$$
x = 30 + 10\log_{10}\left(\frac{P}{1\,\mathrm{W}}\right)
$$

逆変換:

$$
P(\mathrm{mW}) = 10^{x/10},\qquad
P(\mathrm{W}) = 10^{(x-30)/10}
$$

補足:

- +10 dB → 電力 10 倍
- +3 dB → 電力ほぼ 2 倍
- -3 dB → 電力ほぼ 1/2

詳細: https://ja.wikipedia.org/wiki/仕事率の比較

---

