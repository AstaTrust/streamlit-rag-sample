# Introduction 
Azure OpneAI + Azure AI Search を利用した RAG サンプルです。Web フレームワークとして Streamlit を使用しています。

# Getting Started
## ローカルでの実行
1.	ライブラリのインストール

```
pip install -r requirements.txt
```
2.	.env ファイルの記入  
```
SEARCH_ENDPOINT=<your-search-eandpoint>
SEARCH_API_KEY=<your-search-api-key>
SEARCH_INDEX_NAME=<your-index-name>
OPENAI_API_KEY=<your-openai-key>
OPENAI_API_VERSION=2024-05-01-preview
OPENAI_API_ENDPOINT=<your-openai-endpoint>
OPENAI_ENGINE=gpt-4o
OPENAI_EMBEDDING_MODEL=text-embedding-ada-002
```

3.	実行

```
streamlit run app.py
```

## Azure 上での動作確認
1. [Environment variables] -> [App settings] にて環境変数を追加する
2. [Configuration] -> [General sttings] -> [Startup Command] にてスタートアップコマンドを追加する

```
python -m streamlit run app.py --server.port 8000 --server.address 0.0.0.0
```

3. [Networking] -> [Inbound traffic configuration] にて適宜アクセス制限を追加する
4. デプロイを実施する