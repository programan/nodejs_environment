FROM node:14.15.1-buster

RUN set -x \
  && apt update \
  && apt install -y \
  gosu \
  less \
  vim \
  nano \
  unzip \
  wget \
  sudo \
  locales \
  && sed -i -e 's/^# ja_JP\.UTF-8 UTF-8/ja_JP.UTF-8 UTF-8/g' /etc/locale.gen \
  && locale-gen \
  && apt clean \
  && rm -rf /var/lib/apt/lists/*

WORKDIR /tmp

# RUN set -x \
#   && curl https://getmic.ro | bash \
#   && mv micro /usr/local/bin


ENV LANG ja_JP.UTF-8
ENV LANGUAGE ja_JP:ja
ENV LC_ALL ja_JP.UTF-8

# 開発用ユーザー作成
# nodeイメージはidが1000でnodeユーザーが作られているのでそれを使う


# # EXPOSEは公開を宣言するだけで、マッピングはされない
EXPOSE 10080 10080

WORKDIR /apps

# `docker-compose exec --user hoge app bash`
# USER ${APACHE_RUN_USER}
# USER node
