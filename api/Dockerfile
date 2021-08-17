# rubyのバージョンを指定して、Docker_hubからコンテキストをpullする。
FROM ruby:2.7.1
# apt-get updateかつinstallで必要なライブラリをinstallする。
RUN apt-get update && apt-get install -y \
    build-essential \
    libpq-dev \
    nodejs \
  # Dockerのimageファイルを軽量化するためrm -rf /var/lib/apt/lists/*でaptのキャッシュを削除する。
  && rm -rf /var/lib/apt/lists/*
# /appディレクトリを作成し作業ディレクトリを/appにする。
WORKDIR /app
# GemfileとGemfile.lockをコンテナにコピーする。
COPY ./Gemfile /app/Gemfile
COPY ./Gemfile.lock /app/Gemfile.lock
# コンテナ起動時にbundle installを実行する。
RUN bundle install