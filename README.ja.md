# 自己紹介
1987/12/28 生まれ
元プロゲーマーで、2012年CS1.6のアジアチャンピオン

- qiita: http://qiita.com/sion_cojp
- github: https://github.com/sioncojp
- blog: https://sioncojp.hateblo.jp
- slideshare: https://www.slideshare.net/shoheikoyama77/presentations
- speakerdeck: https://speakerdeck.com/sioncojp

# 学歴
- 広島修道高等学校卒
- 日本電子専門学校コンピューターネットワーク科卒

# 職歴
## Timee
2020/1/5 ~ 現在まで

### 業務内容
#### 各SaaSのSSO化
- datadog
- sentry
- aws

#### datadogのterraform化 + dashbaord/アラート設計
- datadogを手動で追加してたのをterraform化。
- また適切なアラートやdashboard/アラートがなかったので追加
- その結果アラートがなったときだけ障害対応する状況にすることができた

#### rails cを叩けるようにした
- rails on fargateのつらみとして、ホストやコンテナにsshできないので、rails cが叩けない問題があった
- また、RDSは基本private subnetからのアクセスしか許可してないので、privateのインスタンスからアクセスさせるしかない。
- そこにどうセッションはるかという課題。
- Goでrails c用cliツールを作成し、下記を行なっている
    - saml2aws等でのsaml認証が必須。
    - ec2にセッションマネージャでセッションを貼る
    - ParameterStoreのデータをdecryptして環境変数にセット
    - ECRからprod/stgのタグに紐づいてるcommitHash値取得
    - 必要な引数をセット + commitHashイメージでdockerを立ち上げる

#### 全Fargateをfirelensに移行
- 今まではawslogsドライバーを使ってたので、fargate ->cloudwatch -> firehose -> lambda -> datadog, s3
- firelensに移行することで、fargate -> firehose -> datadog, s3とシンプルかつコスト削減化 

#### slack deploy導入
- slackからdeployできるようにした
- slack-deployは社内ツールで、Goで作ってます
- https://twitter.com/i/status/1217724217350733824

#### Railsのjemalloc対応
- メモリリークしてたので、メモリの断片化を防ぎながらメモリを確保していくjemalloc対応
- Dockerfileの修正のみ

#### Rails on EC2 -> Fargate
- Goでecs-deployという社内ツール作成
    - ecs task definition生成、登録
    - ecs serviceのupdate
    - fargate, cron(cloudwatch + fargate), runtaskを実行できる
- 暗号情報はSSM parameter storeに入れた
    - parameter storeを管理するGoツールを作成
    - https://github.com/sioncojp/pstore

#### fargate, cron(cloudwatch + fargate), runtaskを検証 + チュートリアル作成
- railsに適用できるか知見がなかったので検証。チュートリアルも作成

#### aws再設計作り直し
- awsアカウントのマルチアカウント構成（root, prod, stg, operation, sandbox....)
- GSuite SSO対応。それによるiam module作成
    - RBACで、各部署のロールベースにiam roleを作成
    - そのroleをrootアカウントでassume role
    - それぞれのアカウントで権限を絞ってる
- VPCから再作成
- makeでterraformが叩けるようにした


## FOLIO
2018/5 ~ 2019/1/4

### 業務内容
#### batch/cron実行基盤をFargateで実行できるように設計、導入
- batch: fargate runtask
- cron: fargete + cloudwatch logging
- logはdatadog logsへ
- [Fargate + cloudwatch eventでcronシステム構築](https://sioncojp.hateblo.jp/entry/2019/09/06/125617)
- [Fargate + cloudwatch eventでcronシステム ロギング設計編](https://sioncojp.hateblo.jp/entry/2019/09/10/183409)

#### ECS検証、設計、module化、本番導入
- logging周りはs3 + datadog logsに飛ばす設計
- 柔軟にコンテナがスケールするように意識
- serviceのコンテナ入れ替え検知 + slack通知をGoで実装
    - https://github.com/sioncojp/ecs-update-notify
- deployツールはGoで書いてる
    - （https://github.com/sioncojp/fargate-deploy/ を潤沢したものを社内private repositoryで管理

#### slack chatops deploy導入
- Go + supervisor で書き、社内private repositoryで管理

#### 社内用fmサーバ導入（社内ラジオ）
- hugo(Fargate) + s3（音声）

#### landing pageサイト構築
- s3 hosting + cloudfront + waf
- deployツールがtypescriptだったので、IAM認証系周りのPRを投げたり。

### 言語
Go/Python/TypeScript/Scala

### その他
terraform/aws/datadog/akamai/fluentd/jenkins

## fluct
2017/7 ~ 2018/3

### 業務内容
- impression計測基盤をPHP->Goに書き換えて、CentOS7化
- ログ収集基盤で使われてるbatch処理をDocker化し、オンプレ->ECSに移行

### 言語 
Go/PHP/Perl/Ruby/Python

### その他
terraform/aws/オンプレ/keepalived/puppet
ldap/cobbler/consul/apache/nginx/influxDB/grafana

## エウレカ
2016/4 ~ 2017/2

### 業務内容
- pairsのトラフィックを支えるaws運用構築

### 言語
Go/Ruby

## その他
terraform/aws/gcp
ansible/mackerel/Docker/nginx/bigquery/MySQL


## リブセンス
2012/7 ~ 2016/3

### 業務内容
- 転職サイトのモバイル用APIをRailsで開発
- リブセンスが持つ自社メディア全てを支えるインフラとネットワーク（オンプレ）
- 自社開発環境をopenstackで構築し提供

### 言語
Ruby/Rails

### その他
keepalived, nginx, openstack, cisco, vyos, drbd, ldap
nfs, kvm, mackerel, nagios, munin, chef, ansible, packer, vagrant

## ビットアイル
2008/4 ~ 2012/6

### 業務内容
- データセンターのレンタルサーバ、ネットワーク構築運用
- ハードウェアキッティング、テスト

### その他
Cisco, Juniper, サーバ, キッティング, ioDrive, Linux
