# 基本イメージとしてOpenJDKを使用
FROM openjdk:11

# Kotlinのバージョンを指定
ENV KOTLIN_VERSION=1.6.10

# Kotlinコンパイラのダウンロードとインストール
RUN curl -sSL "https://github.com/JetBrains/kotlin/releases/download/v$KOTLIN_VERSION/kotlin-compiler-$KOTLIN_VERSION.zip" -o kotlin-compiler.zip \
    && unzip kotlin-compiler.zip -d /usr/share \
    && rm kotlin-compiler.zip

# 環境変数の設定
ENV PATH=$PATH:/usr/share/kotlinc/bin

# 作業ディレクトリの設定
WORKDIR /app

# ホストマシンとのフォルダ共有のためにボリュームを指定
VOLUME ["/app"]

# Bashの起動
CMD ["bash"]
