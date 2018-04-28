# Terraform

## config.tfvars

access_key = "******************"
secret_key = "******************"
region     = "ap-northeast-1"
key_name   = "******************

以下のリンクでユーザーを生成する
https://console.aws.amazon.com/iam/home?region=ap-northeast-1#/users
作成したユーザーのAccessTokenとSecretTokenを使用する

key_nameの設定方法
以下のリンクでkeyを生成する
https://ap-northeast-1.console.aws.amazon.com/ec2/v2/home?region=ap-northeast-1#KeyPairs:sort=keyName

新しくkeyを取得した場合は、
```
$ chmod 400 *****.pem
$ ssh -i *****.pem ec2-user@IPADDRESS
```

## 実行方法
```
$ cd ./terraform
$ terraform init
$ terraform plan -var-file="config.tfvars"
$ terraform apply -var-file="config.tfvars"
$ terraform destroy -var-file="config.tfvars"
```
