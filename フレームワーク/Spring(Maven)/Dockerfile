# OpenJDKを含む基本的なJavaイメージをベースにする
FROM openjdk:11

# Mavenをインストール
RUN apt-get update && apt-get install -y \
    maven \
    bash \
    curl \
    git \
    vim \
    && rm -rf /var/lib/apt/lists/*

# 作業ディレクトリの設定
WORKDIR /app

# コンテナ起動時に実行されるコマンド
CMD ["bash"]
