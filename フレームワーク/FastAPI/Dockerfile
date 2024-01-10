# Pythonイメージをベースにする
FROM python:3.10

# 必要なツールのインストール
RUN apt-get update && apt-get install -y \
    bash \
    git \
    vim \
    && rm -rf /var/lib/apt/lists/*

# 作業ディレクトリの設定
WORKDIR /app

# FastAPIとUvicorn（ASGIサーバー）のインストール
RUN pip install fastapi uvicorn

# ホストマシンからのファイルコピー用ディレクトリ
VOLUME [ "/app" ]

# コンテナ起動時に実行されるコマンド
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--reload"]
