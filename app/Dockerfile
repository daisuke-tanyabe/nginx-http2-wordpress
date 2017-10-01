FROM alpine:3.6

# 必要なツールをインストールする
RUN apk update && apk --update add wget

# 最新版のWordPressをダウンロードしドキュメントルートに配置、所有者の変更を行う
RUN cd /tmp/ && wget --no-check-certificate https://ja.wordpress.org/latest-ja.tar.gz && tar -xzvf latest-ja.tar.gz \
&& cd wordpress && mkdir -p /usr/local/nginx/html/ && mv * /usr/local/nginx/html/. \
&& chown -R root:root /usr/local/nginx/html
