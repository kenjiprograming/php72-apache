# PHP7.2-Apacheのdocker環境

## 想定する環境

- PHP7.2

  [php:7.2.0-apache](https://hub.docker.com/layers/library/php/7.2-apache/images/sha256-25417b6c9c2e1a52b551ba89087f4d07c216f58784773c9e7a1710a1f6e2b4a1?context=explore)

## 構成

- www/htmlが公開ディレクトリ

## 使い方

```bash
■ クローン
$ cd DocRoot/
$ git clone ${this repo}

■ ビルド
$ docker-compose build

■ 起動
$ docker-compose up -d

■ 終了
$ docker-compose down
```

## url

[http://localhost:80/](http://localhost:80/)

