# 環境構築

## 前提
- dockerがインストール&ログイン済みであること

## 初回作業

- dockerビルド

```
$ docker-compose build
```

## ローカル構築
- コンテナ起動

```
$ dokcer-compose up -d
```

# 実行

## jar作成 ~ 実行

- jar 作成

``` sh
$ cd /docker/src/GradleSpringBoot
$ ./gradlew build

BUILD SUCCESSFUL in 1s
7 actionable tasks: 7 up-to-date
```

- 実行

```
$ java -jar app/build/libs/app.jar
Hello World!
```
