## Version
- 

## VPC Endpoint
インターネットゲートウェイやNATゲートウェイ、NATインスタンスなどを経由せずに、VPCと他のAWSサービスとをプライベートに接続できるAWSのサービス。

## To Use AWS Systems Manager
AWS Systems Managerを利用するためには、以下AWSサービスへのVPCエンドポイントが必要。
 - com.amazonaws.region.ssm
 - com.amazonaws.region.ec2messages
 - com.amazonaws.region.ec2
 - com.amazonaws.region.ssmmessages
 - com.amazonaws.region.s3
 - (com.amazonaws.region.kms)

## Reference
- [図: ec2messagesとssmmessagesについて](../infrastructure-visualizations/aws-ssmmessages-ec2messages.jpeg)
- [AWS official docs : Systems Manager の VPC エンドポイントの作成](https://docs.aws.amazon.com/ja_jp/systems-manager/latest/userguide/setup-create-vpc.html)
- [AWS official docs :  SSM エージェントの使用](https://docs.aws.amazon.com/ja_jp/systems-manager/latest/userguide/ssm-agent.html)
- [AWS official docs :  ec2messages、ssmmessages](https://docs.aws.amazon.com/ja_jp/systems-manager/latest/userguide/systems-manager-setting-up-messageAPIs.html)
- [NEC docs : VPCエンドポイント](https://jpn.nec.com/clusterpro/blog/20180115.html)
