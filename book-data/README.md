# python-r-stan-bayesian-model
"RとStanではじめるベイズ統計モデリングによるデータ分析入門" (馬場真哉) を Pythonで書籍の内容を記述しなおしたコードです。
最近はデータ分析にPythonをもちいることが多く、各種機械学習、深層学習やベイズ統計モデルなどの各種手法をスムースに分析できることが多いため、
全コードをPythonで再実装しました。

## 第１章
こちらは理論的な説明の章ですので割愛します。

## 第２章
データ分析に最低限必要なテクニックを学ぶ章です。また、Stanについても最適現の知識が解説されます。

- 2-1.py 四則演算、pandas DataFrame、Seriesの基本的な使い方、乱数生成の基礎
- 2-2.py データの読み込み、グラフ描画（ヒストグラム、カーネル密度推定、共分散、相関係数、コレログラム）
- 2-3.py グラフ描画、グラフ描画（ヒストグラム、カーネル密度推定、ボックスプロット、バイオリンプロット、ペアプロット、ラインプロット）
- 2-4.py 説明変数無しの正規分布のMCMC推定(2-4-1-calc-mean-variance.stan)
- 2-5.py 事後予測分布の推定
- 2-5-2.py 事後予測分布とサンプルの分布比較
- 2-6.py Stanの文法とコーディング
- 2-6-2.py 事後予測分布による平均値の差の比較

### 第３章
基本的な一般化線形モデル（GLM Generalized Linear Models）を学ぶ章です。本書ではライブラリbrmsで記述されているパートもすべてStanで記述しなおしています。
応答変数、説明変数、線形予測子の組み合わせでモデルを構築できるようになります。

- 3-2.py 単回帰モデル
- 3-3.py 単回帰モデルを用いた予測
- 3-5.py 回帰直線の図示
- 3-6.py ダミー変数と分散分析モデル(質的変数の正規分布モデル)
- 3-7.py 正規線形モデル（複数の説明変数、応答変数が正規分布モデル）
- 3-8.py ポアソン回帰モデル
- 3-9.py ロジスティック回帰モデル（2値データ用標準手法）
- 3-10.py 交互作用(カテゴリxカテゴリ)
- 3-10-2.py 交互作用（カテゴリx数量）
- 3-10-3.py 交互作用（数量x数量）

### 第４章
階層ベイズモデルと一般化線形混合モデルの基本を学ぶ章です。階層ベイズモデルは非常に適応範囲の広いモデルです。ここでは過分散（分散が多き過ぎる）モデルに対する改善としての階層ベイズを学びます。
- 4-1.py ランダム効果（変量効果）を利用した一般化線形混合モデルと比較するためのポアソン回帰モデル
- 4-1-2.py ランダム効果（変量効果）を利用した一般化線形混合モデルと比較するためのポアソン回帰モデルの事後予測分布
- 4-2-3.py ランダム効果（変量効果）を利用した一般化線形混合モデル
- 4-2.py ランダム切片モデル（変量効果をグループ化して切片に適応）
- 4-3.py 交互作用を用いたモデル
- 4-3-2.py ランダム係数モデル（変量効果を係数に適応）、縮約の観察

### 第５章
時系列データを扱う状態空間モデル（SSM State Space Model）を学ぶ章です。
- 5-2.py 正規ホワイトノイズとランダムウォーク
- 5-2-1.py ローカルレベルモデル
- 5-3.py ローカルレベルモデルを使った予測
- 5-3-2.py ローカルレベルモデルを使った補間
- 5-4.py 単回帰モデルの適応
- 5-4-2.py 時変係数モデル（説明変数の係数が時間に応じて変化するモデル）
- 5-5.py ローカルレベルモデルの適応
- 5-5-2.py 平滑化トレンドモデル
- 5-5-3.py ローカル線形トレンドモデル
- 5-6.py 基本構造時系列モデル（トレンド成分+周期成分+ホワイトノイズ）
- 5-7.py 自己回帰モデル
- 5-8.py 動的一般化線形モデル（一般化線形モデルが時間に応じて変化するモデル）二項分布
- 5-9.py 動的一般化線形モデル（一般化線形モデルが時間に応じて変化するモデル）ポアソン分布

---
Copyright (c) 2019 Masahiro Imai Released under the MIT license