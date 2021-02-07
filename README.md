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
$ java -jar GradleSpringBoot/app/build/libs/app.jar
# 別コンソールで実行
$ curl localhost:8080
Greetings from Spring Boot!
```

# UT実行

- 実行

```
$ cd GradleSpringBoot/
$ gradle test
Starting a Gradle Daemon (subsequent builds will be faster)

> Task :app:test
2021-02-25 14:25:16.406  INFO 273 --- [extShutdownHook] o.s.s.concurrent.ThreadPoolTaskExecutor  : Shutting down ExecutorService 'applicationTaskExecutor'
2021-02-25 14:25:16.550  INFO 273 --- [extShutdownHook] o.s.s.concurrent.ThreadPoolTaskExecutor  : Shutting down ExecutorService 'applicationTaskExecutor'

BUILD SUCCESSFUL in 1m 28s
3 actionable tasks: 3 executed
```
