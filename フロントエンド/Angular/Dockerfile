# Node.jsイメージをベースにする
FROM node:20

# 必要なツールのインストール
RUN apt-get update && apt-get install -y \
    bash \
    git \
    vim \
    && rm -rf /var/lib/apt/lists/*

# 作業ディレクトリの設定
WORKDIR /app

# パッケージ依存関係のコピー
COPY package.json /app/
COPY package-lock.json /app/

# 依存関係のインストール
RUN npm install

# アプリケーションのファイルをコピー
COPY . /app/

# Angularアプリケーションを起動するコマンド
CMD ["npm", "start"]
