# Notes
文脈自由言語のクラスは， 正規言語のクラスと同様に， 和集合， 連結演算， ス. ター演算について閉じている． 一方， 正規言語のクラスとは対照的に， 積集合と. 補集合については， 閉じていない．

# 「問題」の与え方
1.  入力として与えられる例題（インスタンス）の集合
2.  答えがYesになる条件（または出力の文字列が満たす性質）
	-   決定問題（答えがYes/No）
	-   計算問題（答えが数値または文字列）

# 非決定性計算モデル
-   非決定性計算モデルで、各枝分かれでの出力はORに相当する
-   これをANDに変えた場合のモデルを用いて多項式時間で解ける問題のクラスがco-NPに相当する

# NPクラスのの形式言語的な定義
A language L is in NP if and only if there exist polynomials p and q, and a deterministic Turing machine M, such that
-   For all x and y, the machine M runs in time p(|x|) on input (x,y)
-   For all x in L, there exists a string y of length q(|x|) such that M(x,y)=1
-   For all x not in L and all strings y of length q(|x|), M(x,y)=0

c.f. [https://en.wikipedia.org/wiki/NP_(complexity)](https://en.wikipedia.org/wiki/NP_(complexity))

# NP完全問題

## ハミルトン閉路問題
与えられたグラフで、全ての頂点を一度だけ通る閉路が存在するかどうかを調べる問題

## 独立集合問題
指定された大きさの、頂点集合 V'⊆V のうち V' 内の頂点間に枝が存在しないようなもの（独立集合）が存在するかを調べる問題

## 頂点被覆問題
全ての枝が、元となる頂点のうち少なくとも一つに接するような、頂点の部分集合を見つける問題
-   頂点集合が頂点被覆　＝　その補集合が独立集合

## クリーク問題
指定された大きさのクリーク（完全部分グラフの頂点集合）が存在するかを調べる問題
-   クリーク　＝　補グラフでの独立集合

## 充足可能性問題 (SAT, Satisfiability)
CNF (和積標準形、Conjunctive Normal Form）が与えられたとき、出力が1になるような入力値の組合せが存在するかどうかを判定する問題
-   最初に証明されたNP完全問題

## 有向ハミルトン閉路問題

## 無向ハミルトン閉路問題

# NP困難問題

## 最大独立集合問題

## 最小頂点被覆問題

## 最大クリーク問題

## 巡回セールスマン問題

  
**