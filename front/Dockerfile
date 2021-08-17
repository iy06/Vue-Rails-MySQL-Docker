# latestバージョンのnodejsをDocker_hubからpullする。
FROM node:lts-alpine
# 作業ディレクトリを/appに指定し、/appディレクトリを作成する。
WORKDIR /app
# package.jsonとpackage-lock.jsonをコンテナにコピーする。
COPY ./package.json /app/package.json
COPY ./package-lock.json /app/package-lock.json
# apk(Alpine Linux package management)をupdateしvue/cliをインストールする。
RUN apk update && npm install -g @vue/cli