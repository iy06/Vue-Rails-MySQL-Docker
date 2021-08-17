# latestバージョンのnodejsをDocker_hubからpullする。
FROM node:lts-alpine
# 作業ディレクトリを/appに指定し、/appディレクトリを作成する。
WORKDIR /app
# apk(Alpine Linux package management)をupdateしvue/cliをインストールする。
RUN apk update && npm install -g @vue/cli
# vue create .実行後下記を追加する。
COPY package.json .
RUN npm install