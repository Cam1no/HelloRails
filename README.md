# Terraform

## config.tfvars
```
access_key = "******************"
secret_key = "******************"
region     = "ap-northeast-1"
key_name   = "******************
```
### access_keyとsecret_keyの設定方法
以下のリンクでユーザーを生成する
https://console.aws.amazon.com/iam/home?region=ap-northeast-1#/users

作成したユーザーのAccessTokenとSecretTokenを使用する

### key_nameの設定方法
以下のリンクでkeyを生成する
https://ap-northeast-1.console.aws.amazon.com/ec2/v2/home?region=ap-northeast-1#KeyPairs:sort=keyName

新しくkeyを取得した場合は、
```
$ chmod 600 *****.pem
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


# 参考

## AWSでネットワーク構築
https://qiita.com/naoki_mochizuki/items/f795fe3e661a3349a7ce

## TerraformとAWSを同時入門する
https://qiita.com/litencatt/items/8da20374def6320a014b
