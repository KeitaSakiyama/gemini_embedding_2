# gemini_embedding_2

COCO-Caption2017 データセットの画像群に対し、Gemini API を用いてマルチモーダル検索を行うためのリポジトリです。

## 概要

`lmms-lab/COCO-Caption2017` から抽出した **1,000枚の画像** を、Google の `gemini-embedding-2-preview` モデル（タスクタイプ: `RETRIEVAL_DOCUMENT`）でベクトル化し、保存しています。

本プロジェクトでは、これらの画像群に対して **「音声クエリ（`test.mp3`）」** を入力し、画像と音声のモーダルを跨いだ類似度検索（Audio-to-Image Retrieval）を行う検証などを可能にします。

## ディレクトリ構成

```text
gemini_embedding_2/
├── gemini_image_embeddings.npy  # 1,000枚分の画像埋め込みベクトル（NumPy形式）
├── gemini_image_metadata.json    # 各画像に対応するメタデータ（COCO IDやキャプション）
└── test.mp3                     # 検索クエリとして使用する音声ファイル（MP3形式）