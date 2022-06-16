## Version
- 

## ExecutionRole
ECSへのIAM role。ECRからimageをpullできるようにしたり、CloudWatchへログを書き込めるようにしたり。他のAWSサービスに対して、AWS API コールを実行するためのアクセス許可を付与する。

## TaskRole
ECS serviceのタスクで使用できるIAM role。コンテナからS3へのアクセスなどを制御する。

## Reference
- [AWS officail docs : ECSタスク実行IAMロール](https://docs.aws.amazon.com/ja_jp/AmazonECS/latest/developerguide/task_execution_IAM_role.html)
- [AWS officail docs : タスク用のIAMロール](https://docs.aws.amazon.com/ja_jp/AmazonECS/latest/developerguide/task-iam-roles.html)
- [stack overflow: difference between ExecutionRole and TaskRole](https://stackoverflow.com/questions/48999472/difference-between-aws-elastic-container-services-ecs-executionrole-and-taskr)
