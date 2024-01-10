# Javaの公式イメージをベースに使用
FROM openjdk:8

# JMeterのバージョンを指定
ENV JMETER_VERSION 5.4.1

# JMeterのダウンロードとインストール
RUN wget https://archive.apache.org/dist/jmeter/binaries/apache-jmeter-${JMETER_VERSION}.tgz \
    && tar -xzf apache-jmeter-${JMETER_VERSION}.tgz -C /opt \
    && rm apache-jmeter-${JMETER_VERSION}.tgz

# 環境変数の設定
ENV JMETER_HOME /opt/apache-jmeter-${JMETER_VERSION}
ENV PATH $JMETER_HOME/bin:$PATH

# 作業ディレクトリの設定
WORKDIR /jmeter

# ホストマシンとのフォルダ共有のためにボリュームを指定
VOLUME ["/jmeter"]

# Bashの起動
CMD ["bash"]
