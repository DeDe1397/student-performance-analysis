## 教育データ分析・目的
生徒情報と数学の成績の関係を分析し、学習支援に向けた改善施策の仮説を提示する。

## 実施内容
- EDA: 可視化（Plotly）
- 統計検定: t検定による有意差検証
- 機械学習: LightGBMによる予測モデル構築・特徴量重要度の算出
- モデル評価: MAE / RMSE による精度測定

## データ
- Kaggle: Students Performance in Exams  
  （公開データを使用）

## 実行環境
- Jupyter Lab

## 成果例
- テスト準備講座（test preparation course）の有無で統計的に有意な差を確認（p = 1.5e-08）  
- 読解力（reading）が数学に強い影響を与えていることを発見  
- LightGBM による予測：MAE = 4.60, RMSE = 6.1  
  → 平均点66点に対して ±6点程度の誤差

## 実務上の示唆
- SHAP値の高い writing score が低い生徒 → 補習や教材提供の優先対象とする  
- test preparation course 未受講の生徒 → 学校内での受講推奨施策や案内資料に活用可能

## 改善点
- 強相関する特徴量（reading, writing）の扱いを調整することで汎化性能の向上が期待できる  
- 今後は回帰モデルや因果推論を用いて test preparation course の効果を厳密に検証する
