---
title: "今更ながらFastAPIを用いて物体検出アプリを作ってみた"
emoji: "✨"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["python"]
published: true
published_at: 2026-02-12 08:00 # 未来の日時を指定する
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

# FastAPIの中身を書く

https://github.com/Ryo-Kawanami/object_detection_app_uv/tree/main/main.py

# 起動・ブラウザで開く

起動

```
uv run uvicorn main:app --reload
```

ブラウザで http://127.0.0.1:8000/ を開く。

# 実行する

![](/images/fast-api-app/showcase.png)

# 参考

- [FastAPI公式チュートリアル](https://fastapi.tiangolo.com/ja/tutorial/first-steps/#check-it)
- [FastAPIとuvで始めるPythonモダンAPI開発](https://qiita.com/y_inoue15/items/6ae20c20b4a4b2cad842)
