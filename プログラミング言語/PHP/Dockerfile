# PHPイメージをベースにする
FROM php:8.0-apache

# 必要なパッケージのインストール
RUN apt-get update && apt-get install -y \
    git \
    vim \
    && rm -rf /var/lib/apt/lists/*

# Composerのインストール
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

# 作業ディレクトリの設定
WORKDIR /var/www/html

# Apacheの設定
COPY .docker/apache.conf /etc/apache2/sites-available/000-default.conf

# コンテナ起動時に実行されるコマンド
CMD ["apache2-foreground"]
