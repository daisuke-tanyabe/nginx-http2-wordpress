FROM debian:jessie

# 必要なツールをインストールする
RUN apt-get update && apt-get -y install wget

# 最新版のWordPressをダウンロードしドキュメントルートに配置、所有者の変更を行う
RUN cd /tmp/ && wget https://ja.wordpress.org/latest-ja.tar.gz && tar -xzvf latest-ja.tar.gz \
&& cd wordpress && mkdir -p /usr/local/nginx/html/ && mv * /usr/local/nginx/html/. \
&& chown -R www-data:www-data /usr/local/nginx/html
