## 本リポジトリについて

chatモデルをvLLMでサーブし、埋め込みモデルをinfinityでサーブしたRAG開発サーバー構築を行ったリポジトリ

- chatモデル(vLLM): Qwen/Qwen3-4B-Thinking-2507

- 埋め込みモデル: sbintuitions/sarashina-embedding-v2-1b

## 環境

- CPU: Intel Core i9-14900KF

- メモリ: 64 GB

- GPU: NVIDIA GeForce RTX 4090


## 前提条件

- Dockerがインストールされていること

- `data/`配下に`input.pdf`が配置されていること(今回は、[テキスト生成 AI 利活用におけるリスクへの対策ガイ
ドブック](https://www.digital.go.jp/assets/contents/node/basic_page/field_ref_resources/c1959599-efad-472e-a640-97ae67617219/fe843dc6/20240610_resources_generalitve-ai-guidebook_01.pdf) を使用)

## 起動方法

1. `docker compose up`を実行

2. `localhost:8888`にアクセスし、jupyter labにアクセス

3. `notebooks/01_create_db.ipynb`を開く => ベクトルDBにデータを登録する

4. `notebooks/02_rag.ipynb`開く => ベクトルDBに登録した内容をテストする

## Tips

- vLLMで埋め込みモデルをサーブすると上手く動作しないケースがある。埋め込みモデル専用のライブラリを使用することが望ましい
