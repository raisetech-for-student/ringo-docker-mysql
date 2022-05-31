# ringo-docker-mysql
## 概要
このリポジトリはringoチームのDockerを用いたMySQL環境を構築します。

## 起動手順
`$ git clone https://github.com/raisetech-for-student/ringo-docker-mysql.git`

`$ cd ringo-docker-mysql`

`$ docker-compose up -d` コンテナを構築

## 動作確認方法
`$ docker ps` コンテナ名を確認する

`$ docker exec -it [コンテナ名] mysql -u root -p`

**Git Bashを使用される方は先頭に`winpty`を付けてください**

passwordの入力を要求されるため、`docker-compose.yml`ファイルの`MYSQL_ROOT_PASSWORD:`に記述したpasswordを入力する

`$ show databases;`

`$ use ringo;`

`$ show tables;` ringo_userテーブルが作成されていることを確認する

## 終了手順

`$ docker-compose down` コンテナを停止
