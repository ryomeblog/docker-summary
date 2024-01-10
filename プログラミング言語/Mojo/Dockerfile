# Ubuntuイメージをベースにする
FROM ubuntu:23.04

# 必要なパッケージのインストール
RUN apt-get update && apt-get install -y \
    bash \
    git \
    vim \
    curl \
    && rm -rf /var/lib/apt/lists/*

# Mojo言語のインストール
RUN curl https://get.modular.com | sh - && \
    modular auth mut_～ && \
    modular install mojo
# mut～はhttps://developer.modular.com/downloadで確認します。

# 作業ディレクトリの設定
WORKDIR /app

# コンテナ起動時に実行されるコマンド
CMD ["bash"]
