# golang-mongodb-network-connector

golang-mongodb-network-connector は Go ランタイムで MongoDB に対し、ネットワーク接続を行うためのライブラリです。

## 動作環境

動作には以下の環境であることを前提とします。

* OS: Linux OS
* CPU: ARM/AMD/Intel
* Golang Runtime

## 導入方法

go get でインストールしてください。

```sh
go get "github.com/latonaio/golang-mongodb-network-connector"
```

## 使用方法

### mongodb 接続のためのインスタンス作成

```go
db, err := database.NewMongodb(c.DB)
if err != nil {
  l.Error(err)
  return
}
```

### DB の切断処理

```go
defer db.Close()
```
