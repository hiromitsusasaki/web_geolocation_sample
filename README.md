Web Geolocation Sample
====

## Description

Geolocation APIのサンプル実装

## Environment

以下の手順で開発環境を構築できる

### Requirement

以下がインストールされていることを前提とします

- nodejs
- npm
- firebase-cli (npm module)

## Project setup

```
$ git clone git@github.com:hiromitsusasaki/web_geolocation_sample.git

or

$ git clone https://github.com/hiromitsusasaki/web_geolocation_sample.git

$ cd web_geolocation_sample
$ npm intall
```

### Operation

####  開発時

SPAとしてローカルで起動（ホットリロード）

```
$ yarn serve
```

### ビルド＆デプロイ

#### ビルド

```
$ yarn build
```

#### デプロイ

デプロイするソースをあらかじめ`ビルド`して`dist/`ディレクトリにビルド後のファイル一式が生成されていることが前提です。

firebaseにログインする（ログイン済みの場合は不要）
```
$ firebase login
```

firebaseプロジェクトの作成（当該vue.jsプロジェクトのデプロイのためのfirebaseプロジェクトがすでにある場合は不要）

```
$ firebase projects:create {your-project-id}
```

`.firebaserc`の`{your-project-id}`の部分を上記で作成したfirebaseプロジェクトのIDに変更する

`.firebaserc`
```
{
  "projects": {
    "default": "{your-project-id}"
  }
}
```

firebaseにデプロイする
```
$ firebase deploy
```
