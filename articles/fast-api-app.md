---
title: "今更ながらFastAPIを用いて物体検出アプリを作ってみた"
emoji: "✨"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["python"]
published: true
published_at: 2027-06-12 09:03 # 未来の日時を指定する
---

# 環境の準備

## 著者の環境

- MacBook Pro
- チップ: Apple M4 Max
- MacOS: 15.6（24G84）

## プロジェクトの作成

まずは`object_detection_app`というフォルダを作成してそのディレクトリへ移動しましょう

```
mkdir object_detection_app
cd object_detection_app
```

## uvのセットアップとライブラリのインストール

次にuvの初期化を行います。

以下に従いuvのインストール
https://docs.astral.sh/uv/getting-started/installation/

初期化とライブラリのインストール

```
# 初期化
uv init

# ライブラリのインストール
uv add "fastapi[standard]"
uv add --dev ruff pytest pytest-cov
```
