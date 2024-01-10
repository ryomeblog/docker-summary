# Debianイメージをベースとする
FROM debian:12.2-slim

# 必要なパッケージのインストール
RUN apt-get update && apt-get install -y \
    bash \
    curl \
    git \
    vim \
    zip \
    unzip \
    build-essential \
    && rm -rf /var/lib/apt/lists/*

# 作業ディレクトリの設定
WORKDIR /app

# コンテナ起動時に実行されるコマンド
CMD ["bash"]
