# Larecs
ECSでLaravelをホストするための検証用プロジェクト

## 手順
### ECR上にprivateレポジトリを作成

### Github ActionsからECRへイメージをpushする用のIAMユーザーを作成
policyはAmazonEC2ContainerRegistryPowerUserを付与。

## Github Secrets
**AWS_ACCESS_KEY_ID**: ECRにpushする用のIAMユーザーのAccess key ID

**AWS_SECRET_ACCESS_KEY** ECRにpushする用のIAMユーザーのSecret access key
