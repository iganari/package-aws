# Route 53

## アクセス情報を環境変数にいれる

```
export AWS_ACCESS_KEY_ID='hogehoge'
export AWS_SECRET_ACCESS_KEY='hugahuga'
```

## zone の確認

```
aws route53 list-hosted-zones --output json
aws route53 list-hosted-zones --output table
```
