# hrv-based-stress-classification-using-the-wesad-.
WESAD データセットを用いて、心拍変動 (HRV) 指標からストレス状態を分類するベースライン実装。

# WESAD HRV ストレス分類（ベースライン）

このリポジトリは、[WESAD データセット](https://www.kaggle.com/datasets/) を用いて  
心拍変動（HRV: Heart Rate Variability）の特徴量からストレス状態を分類するベースライン実装です。  
Google Colab 上で動作するように構成しています。

## データセット
- **WESAD**: Wearable Stress and Affect Detection データセット  
- ライセンスの関係で、このリポジトリには **生データ（.pkl ファイル）は含まれていません**。  
- Kaggle から各自でダウンロードし、Colab 上の `/content/data/` に配置してください。

## 実行方法
1. Kaggle の API Key（`kaggle.json`）を用意し、Colab にアップロードする  
2. `baseline_notebook.ipynb` を開いてセルを上から順に実行する  
3. データセットが Kaggle から自動ダウンロード・解凍されます  
4. ECG 信号から HRV 特徴量（平均HR, SDNN, RMSSD など）を抽出  
5. ロジスティック回帰モデルで「ストレス vs 非ストレス」の分類を実施  

## 実行結果
被験者ごとに精度（accuracy）、Macro-F1、サンプル数を出力します。  

例:

| 被験者 | 精度 (accuracy) | Macro-F1 | サンプル数 |
|--------|-----------------|----------|------------|
| S3     | 1.000           | 1.000    | 107        |
| S8     | 1.000           | 1.000    | 90         |
| S6     | 0.966           | 0.919    | 116        |
| S5     | 0.962           | 0.917    | 103        |

## 必要なライブラリ
## 必要なライブラリ
neurokit2
pywavelets
seaborn
scikit-learn

## ライセンス
MIT License

