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

# Flaskのインストール
RUN pip install flask

# ホストマシンからのファイルコピー用ディレクトリ
VOLUME [ "/app" ]

# コンテナ起動時に実行されるコマンド
# Flaskアプリケーションのエントリーポイントを指定
CMD ["flask", "run", "--host=0.0.0.0"]
