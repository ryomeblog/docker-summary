# Node.jsバージョン20のイメージをベースにする
FROM node:20

# 必要なツールのインストール
RUN apt-get update && apt-get install -y \
    bash \
    git \
    vim \
    && rm -rf /var/lib/apt/lists/*

# 作業ディレクトリの設定
WORKDIR /app

# ホストマシンからのファイルコピー用ディレクトリ
VOLUME [ "/app" ]

# コンテナ起動時に実行されるコマンド
CMD ["bash"]
