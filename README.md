# s3-event-notification

- S3、SNSトピックを作成
- S3へファイルへのアップロードをSNSへ通知

## deploy

```sh
aws cloudformation create-stack \
    --stack-name s3-event-notification \
    --parameters ParameterKey=BucketName,ParameterValue=${BucketName} \
    --template-body file://template.yaml
```

*Paramters*

|Key|Description|Default|
|--|--|--|
|BucketName|S3バケット名|`s3-event-notification-s3bucket`|

## usage


- SnsTopicからサブスクリプションを登録
- S3へファイルをアップロードで、サブスクリプションへ通知
