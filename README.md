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

## Cloud Formationに反映していない作業
public subnetにNAT Gatewayを置いてprivate subnetのルートテーブルの0.0.0.0/0に当該のNATを指定。。ECRなどのリージョンサービスにアクセスする必要があるから。

ターゲットグループ作成 -> ALB作成 -> ECSのサービスという作成順序っぽい。
ALBを作成する際は、subnetを2つ以上指定しろと怒られた。multi-AZ構成を前提としているみたい。
ということで別のregionにpublicサブネットを追加。

タスク実行ロールからパラメータストアを参照する必要があるので、executionRoleにSystem MangerとKMSのロールを付与。
