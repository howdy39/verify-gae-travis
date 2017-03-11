# verify-gae-travis

## ローカルでの検証
http://qiita.com/kentarosasaki/items/2232113b44b016a56adc

```
curl https://sdk.cloud.google.com | bash
```

```
gcloud config set project gae-sample-160213
```

```
gcloud auth login
```

```
gcloud app deploy
```