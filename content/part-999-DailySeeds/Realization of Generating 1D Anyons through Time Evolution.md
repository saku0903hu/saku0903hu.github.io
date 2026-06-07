---
title: "Physical Realization of the Generalized Jordan-Wigner Transformation: Generating 1D Anyons through Time Evolution"
description:
tags:
---
## モチベーション

物理学において、次元は系の詳細を特徴づける重要なパラメータである。
特に、3次元より小さい1,2次元系は様々な点において、他の3以上の次元と比べ特異な振る舞いがある。
今回はその中でも1次元系に注目する。
1次元格子系では、boson-anyon-fermionマッピングができることが知られている。
その間の変換をgeneralized Jordan-Wigner変換といい、これを用いることでboson-anyon-fermionの等価性を示すことができる。
また、この変換は格子系だけでなく連続系、場の理論まで拡張することができることがわかっている。
本研究では、generalized Jordan-Wigner変換が非局所的なユニタリ変換である(Jordan-Wigner変換がユニタリであることに注目している先行研究はないと思われる)ことに注目して、この変換を場のユニタリ時間発展と同一視できるようなハミルトニアンが存在するかどうかを調べたい。
もしそのようなハミルトニアンが存在するならば、時間経過のみでfermion-anyon-bosonマッピングができることになる。一般的に、統計性が時空の各点で変わることは考えられていないだろうと思われるので、ダイナミクスによって粒子の統計性を変更できるならば時空と統計性の関係を再考するきっかけになるかもしれない。

## 本論文で実現したい流れ

本論文で主張したいことは、generalized Jordan-Wigner変換という統計性を変える変換がハミルトニアンによるユニタリ時間発展で実現できるかどうかを示すことである。
その流れは大きく分けて以下のようにすると良いのではないかと思われる。

1. generalized Jordan Wigner変換が非局所的なユニタリ変換であることを示す。
2. あるハミルトニアンと場を用意して、そのハミルトニアンによる時間発展がgeneralized Jordan-Wigner変換とみなせることを示す。あるいは、任意のハミルトニアンによる時間発展演算子によるユニタリ変換がgeneralized Jordan-Winger変換とみなせないことを示す。
3. 2つの時間において、それぞれ実際に場を変換して、交換関係が時間によって変化することを示す。

2がこの論文におけるもっとも重要な主張である。
そのため、論文として結果を残すためには、”generalized Jordan Wigner変換とみなせるようなユニタリ時間発展を実現するハミルトニアンが存在するか”のYes/Noを結論づけることが必要であると考える。

## 現時点で得ている結果

1の"generalized Jordan Wigner変換が非局所的なユニタリ変換であることを示す。"はできていると考えている。

![[Pasted image 20260519165618.png]]

### 流れ2の進捗

2成分モデルでは、それぞれの位相が打ち消しあってしまい、anyonの位相は出てこず、統計性は変化しないと思われる。

![[Pasted image 20260519165732.png]]

![[Pasted image 20260519165804.png]]

![[Pasted image 20260519165824.png]]
![[Pasted image 20260519165837.png]]

![[Pasted image 20260519165853.png]]

![[Pasted image 20260519165907.png]]

![[Pasted image 20260519165919.png]]

![[Pasted image 20260519165933.png]]

![[Pasted image 20260519165946.png]]

![[Pasted image 20260519165959.png]]

![[Pasted image 20260519170022.png]]

![[Pasted image 20260519170046.png]]

## 1成分モデル
計算の方法がわからず進んでいない。

![[Pasted image 20260520171609.png]]

![[Pasted image 20260520171655.png]]

## 結論

（自分の予想では、特殊なハミルトニアンによる時間発展でgeneralized Jordan WIgner変換を実現できると考えているため）ハミルトニアンによる時間発展のみで自然と統計性が変わりうることがわかった。