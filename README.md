# EEG Classification (Deep Learning 基礎講座 最終課題)

被験者が画像を見ているときの脳波データ（EEG）から、その画像がどのカテゴリ（animal, food, clothing, tool, vehicle）に属するかを分類するプロジェクトです。

## プロジェクトの目的
- ニューラルネットワーク(MLP)モデルを追加し、既存のGBDT系モデルとアンサンブルしてスコア向上を目指す。
- ベースラインの 38.8% を超え、目標精度 55% 以上を目指す。

## 現在の進捗・課題
- ベースラインの CNN モデルにて学習を実施。
- 学習が進むにつれて過学習が発生（Epoch 50時点で Train Acc 49.9% に対し Val Acc 31.0%）。
- 解決策として、モデルの Head 部分を多層 MLP に刷新し、正則化（Dropout等）を強化予定。

## ディレクトリ構成
- `DLBasics2025_competition_EEG_baseline.ipynb`: メインの学習ノートブック
- `data/`: 脳波データ（eeg.npy, labels.npy 等）※非公開
- `categorization.tsv`: 画像カテゴリ対応表
- `image_metadata.npy`: 画像メタデータ