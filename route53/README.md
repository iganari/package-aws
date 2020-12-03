# Route 53

## アクセス情報を環境変数にいれる

```
export AWS_ACCESS_KEY_ID='hogehoge'
export AWS_SECRET_ACCESS_KEY='hugahuga'
```

## 全 zone の確認

+ 全 zone を json で出力

```
aws route53 list-hosted-zones --output json
```

+ 特定の zone の割り出す (`jq` が必要)

```
aws route53 list-hosted-zones --output json | jq .HostedZones[]
```

## 特定の zone の確認

+ `特定の zone` の Id が必要

```
export _hostedzone_id='fizzbuzz'
```
```
aws route53 list-resource-record-sets --hosted-zone-id ${_hostedzone_id} --output json
```

## 追加

+ json 作成
  + `add-a-record.json`

```
{
    "Comment": "CREATE a record",
    "Changes": [
    {
        "Action": "CREATE",
        "ResourceRecordSet":
        {
            "Name": "MY_FQDN",
            "Type": "A",
            "TTL": 30,
            "ResourceRecords": [
            {
                "Value": "MY_FQDN_VALUE"
            }
            ]
        }
    }
    ]
}
```
