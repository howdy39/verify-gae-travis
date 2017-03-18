# verify-gae-travis
[Google App Engine Deployment | Travis](https://docs.travis-ci.com/user/deployment/google-app-engine/)

## Travis Cliのインストール
https://github.com/travis-ci/travis.rb#installation


## gcloudのインストール
http://qiita.com/kentarosasaki/items/2232113b44b016a56adc

```
curl https://sdk.cloud.google.com | bash
```

### gcloudの説明はこの辺に記載されている
https://cloud.google.com/sdk/docs/initializing


## プロジェクトの設定
```
gcloud config set project gae-sample-160213
```

## サービスアカウント認証
サービスアカウントの作成時は以下の２つの役割をいれること

- App Engineの管理者
- ストレージオブジェクトの管理者

ストレージオブジェクトも必要なのはgcloudを使う関係らしい？  
http://www.deadunicornz.org/blog/2017/01/31/travis-ci-and-deploying-golang-apps-to-gae/index.html

```
gcloud auth activate-service-account --key-file client-secret.json
```

## デプロイ
```
gcloud app deploy
```

## Travis用の設定

`travis encrypt-file client-secret.json --add`
