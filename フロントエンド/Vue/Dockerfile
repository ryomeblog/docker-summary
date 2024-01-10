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
# yarnを使用している場合
# COPY yarn.lock /app/

# 依存関係のインストール
RUN npm install
# yarnを使用している場合
# RUN yarn install

# アプリケーションのファイルをコピー
COPY . /app/

# Vueアプリケーションを起動するコマンド
CMD ["npm", "run", "serve"]
# yarnを使用している場合
# CMD ["yarn", "serve"]
