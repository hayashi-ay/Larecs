# Larecs
ECSでLaravelをホストするための検証用プロジェクト

## 手順
### Github Actionsで使用するIAMユーザーを作成
`AmazonEC2ContainerRegistryPowerUser`と以下のポリシーを付与。
- https://github.com/aws-actions/amazon-ecs-deploy-task-definition#permissions

### ECR上にprivateレポジトリを作成

### ECSクラスターとサービスを作成

## Github Secrets
**AWS_ACCESS_KEY_ID**: ECRにpushする用のIAMユーザーのAccess key ID

**AWS_SECRET_ACCESS_KEY** ECRにpushする用のIAMユーザーのSecret access key
