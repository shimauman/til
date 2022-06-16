## Version
-

## Premise
dockerを利用して本番環境を構成するとして。

## Health Check By ELB
HTTP通信を受け付けるコンテナに対して。AWSでは、ELBによるヘルスチェックの結果がunhealthyの場合にも、ECS配下にあるサービス(コンテナの集まり)を再起動してくれる。

## Health Check by ECS
HTTP通信を受け付けないコンテナに対して(イベントドリブンで動くコンテナなど)。例えばサインアップがトリガーとなり、ユーザー登録だけではなく、別のコンテナを使って他の処理を行うなど。


## Preparation In Application
1. ヘルスチェック用のAPIパスを作成。
```
{domain}/api/health-check みたいな。
```

2. そのAPIパスが叩かれると以下の処理を行うように設定。
```php
<?php
***
public function *** (Request $request)
{
    // User agentの取得
    $userAgentString = $request->userAgent();

    // User agentがELB-HealthChecker以外の場合は404を。
    if (strpos($userAgentString, "ELB-HealthChecker") === false) {
        abort(404);
    }

    try {
        // DBとの接続を確認する。
        DB::connection()->getDatabaseName();
    } catch (Exception $e) {
        return response()->json([
            'status'        => 'unhealthy',
            'db-connection' => 'failed',
            ***
        ], 500);
    }

    return response()->json([
        'status'        => 'healthy',
        'db-connection' => 'success',
        ***,
    ], 200);
}
```

## Setting In AWS Target Group (AWS CDK Stack)
1. ターゲットグループの作成。
2. 必要なリソーススタックをそのグループに所属させる。

```typescript
const targetGroup = new CfnTargetGroup(this, 'targetGroup', {
    healthCheckPath: '/api/health-check',
    ***
});
```

## Try ELB Health Check On Local With Docker
1. 本番環境用のコンテナをローカルで起動。
2. ブラウザのコンソール画面にて、User agentをELB-HealthCheckerに変更。
3. health checkのapiパスを叩いてみる。
 
TODO:
docker-compose.ymlファイルを使っているなら、それぞれのcontainerに対して本番環境用のimageに書き換えてもよい。これってローカルでbuildしたimageは設定できるのかな？無理かもな。

## Reference
- 
