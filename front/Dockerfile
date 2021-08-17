# latestバージョンのnodejsをDocker_hubからpullする。
FROM node:lts-alpine
# 作業ディレクトリを/appに指定し、/appディレクトリを作成する。
WORKDIR /app
# apk(Alpine Linux package management)をupdateしvue/cliをインストールする。
RUN apk update && npm install -g @vue/cli