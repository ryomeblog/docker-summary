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

# 依存関係ファイルのコピー（存在する場合）
COPY requirements.txt /app/

# Python依存関係のインストール
RUN pip install --no-cache-dir -r requirements.txt

# コンテナ起動時に実行されるコマンド
CMD ["bash"]
