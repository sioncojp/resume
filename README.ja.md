# 自己紹介
1987/12/28 生まれ
元プロゲーマーで、2012年CS1.6のアジアチャンピオン

http://qiita.com/sion_cojp
https://github.com/sioncojp
https://sioncojp.hateblo.jp
https://www.slideshare.net/shoheikoyama77/presentations
https://speakerdeck.com/sioncojp

# 学歴
- 広島修道高等学校卒
- 日本電子専門学校コンピューターネットワーク科卒

# 職歴
## FOLIO
2018/5 ~ 現在まで

### 業務内容
#### batch/cron実行基盤をFargateで実行できるように設計、導入
- batch: fargate runtask
- cron: fargete + cloudwatch logging
- logはdatadog logsへ

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
