### 1日の平均温度の予測モデルの作成と評価、特徴量追加による精度改善
### 
###### 本githubでは、横浜の1日の平均温度をKerasのLSTMを使用したモデルでの予測を試みています。
###### 本githubに含まれるbranchは、同一のモデルに対し異なる特徴量を使用しています。
- master: 特徴量に各都道府県の平均気圧を追加
- plane: 横浜の1日の平均温度データのみ
- yokohama: 横浜で観測された1日毎のデータを追加
###### 
###### 
###### 各条件での実行結果を以下に記載します。
| branch名 | 平均誤差[℃] | 不偏標準偏差 | 最大誤差[℃] | テストデータの精度 |
|:---      |:---         |:---         |:---         |:---              |
| master   | 0.004       | 1.61        |  7.5        | 1.666            |
| plane    | 1.038       | 1.988       |  9.9        | 2.054            |
| yokohama | 0.321       | 1.783       |  11.9       | 1.897            |
###### 
###### 
###### 以上の結果から、平均気圧を特徴量が予測の精度改善に有効であることが分かりました。
###### また、誤差の値を分析することで、各branchに共通して、3月、4月が特に誤差が多いことが分かりました。
