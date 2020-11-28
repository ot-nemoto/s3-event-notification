# s3-event-notification

- S3、SNSトピックを作成
- S3へファイルへのアップロードをSNSへ通知

## deploy

```sh
aws cloudformation create-stack \
    --stack-name s3-event-notification \
    --template-body file://template.yaml
```

## usage


- SnsTopicからサブスクリプションを登録
- S3へファイルをアップロードで、サブスクリプションへ通知
