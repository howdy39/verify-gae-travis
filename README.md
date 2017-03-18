# verify-gae-travis
[Google App Engine Deployment | Travis](https://docs.travis-ci.com/user/deployment/google-app-engine/)

## Travis Cliのインストール
https://github.com/travis-ci/travis.rb#installation


## gcloudのインストール
http://qiita.com/kentarosasaki/items/2232113b44b016a56adc

```
curl https://sdk.cloud.google.com | bash
```


## gcloudの説明はこの辺に記載されている
https://cloud.google.com/sdk/docs/initializing

### プロジェクトの設定
```
gcloud config set project gae-sample-160213
```

### 認証・認可

#### サービスアカウント
```
gcloud auth activate-service-account --key-file client-secret.json
```

#### ブラウザログイン
```
gcloud auth login
```

### デプロイ
```
gcloud app deploy
```
