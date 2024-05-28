Shohei "Sion" Koyama

----

# 自己紹介
1987/12/28 生まれ
元プロゲーマーで、2012年CS1.6のアジアチャンピオン

- X: https://x.com/sion_cojp
- github: https://github.com/sioncojp
- blog: https://sioncojp.hateblo.jp
- note: https://note.com/sion_cojp
- qiita: http://qiita.com/sion_cojp
- slideshare: https://www.slideshare.net/shoheikoyama77/presentations
- speakerdeck: https://speakerdeck.com/sioncojp

# 学歴
- 広島修道高等学校卒
- 日本電子専門学校コンピューターネットワーク科卒

# 職歴
## DXER COO
2024/04/19 ~ 現在

- 経営周り
  - 資金調達に向けてピッチ資料作成
  - 各部署単位に中長期戦略の定義
- シスクル事業部
  - ピープルマネジメント研修・リーダーシップ研修の実施 + ピープルマネジメント・リーダーシップのマニュアル化
  - CTO時代の業務を引き続き

## DXER CTO
2022/10/1 ~ 2024/04/19

- 経営
  - シスクル事業の草案と実行
  - DXERや各事業がなぜ存在するかのService Idea Docとそのフレームワーク作成
  - 中長期ロードマップからのタスク分解、優先順位付け
  - 採用
- シスクル事業
  - 全部署の立ち上げと実務、業務プロセス確立、マニュアル作成、
    - CS...顧客のLTVを伸ばすために顧客と対話、提案、各部署連携
    - COS...シスクル事業をスムーズに使うためのオンボーディングスペシャリスト
    - Sales...セールス資料作成、料金定義、顧客と商談
    - Solution Architect...顧客の情シス業務の設計
    - SolutionEngineer...顧客の情シス業務の実装、マニュアル作成し、SystemAdministratorに落とし込み
    - SystemAdministrator...マニュアル作業、ヘルプデスク作業
    - Dev...SystemAdministrator向け開発、ドメインエキスパートとしてアドバイス、何をどの順に開発するか顧客の意見をdevに伝える
  - 全メンバー、全部署のマネジメント: [SpeakerDeck](https://speakerdeck.com/sioncojp/cheng-chang-wosahotosuruhihurumanesimentonoyarifang)
  - PdM
  - プロダクトデザイン + LP周りの一部作成/: Material Design 3 x TailwindベースでFigmaを利用
  - バックエンド開発/設計: Go x GraphQL
  - フロントエンド開発: Next.js + Tailwind + storybook
  - 自社Chrome Extension開発/設計（React）

## Chikaku
2021/3/1 ~ 2022/9/30

### 業務内容
- 経営周り: 会社全体のMVVと戦略, プロダクトの戦略の策定
- flutterでアプリ開発検証
- 写真プリントサービスのモニタリングとSLI/SLOの策定とdatadogで設定: 全てterraformで管理
- 写真プリントサービスのAPI/batch設計とリファクタとGoでのプロトタイプ開発: Django -> Go。API、テーブル設計、インフラまで全て実装
  - ref: https://sioncojp.hateblo.jp/entry/2022/06/13/190923
- 写真プリントサービスで使うGoのフレームワークサンプルを作成 : クリーンアーキテクチャベース。migrateの方法、testの書き方や実装を社員に説明
- テレビ電話サービス（API + Frontend）の構築、運用: Fargate, cloudfront, django
- awsのterraformで管理
- WAFの導入
- 無駄なDBインスタンスを1つのRDSに統合
- RDSのAurora移行とRI購入: https://sioncojp.hateblo.jp/entry/2021/06/18/153741
- 定期実行系をEC2 -> Fargateに移行: 既存サービスのリバースエンジニアリングを含む
- DB Migration系をFargete runtaskに移行 
- EC2 -> Fargateに移行
  - Fargate用module追加
  - Faraget Spotを使うようにした
  - Fargateのsandbox環境の構築、資料作成と説明
  - https://github.com/sioncojp/pstore 導入
  - https://github.com/sioncojp/ecs-update-notify 導入
  - Fargate用deployロジック追加
  - CI/CDの整備
  - datadog logs archiveの導入
  - firehose -> firelensにした
- AWSのコスト削減: 50%のコストカット

## Timee
2020/1/5 ~ 2021/3/1

### 業務内容
- VPoEっぽい動き
  - 基本的にCTOと密に思考/定義/浸透
  - エンジニア採用フローを整備（DMでやりとりしてたのを、出来る限りオープンなやりとりができるようにした）
  - 人事評価の定義
  - 全ポジションのJobDescription設定と、githubで管理
  - KGI -> NSM -> KPI -> OKRの落とし込み計画
  - 組織戦略と経営戦略
- コーポレートエンジニア
  - jamfのterraform-provider作成
    - https://github.com/sioncojp/go-jamf-api
    - https://github.com/sioncojp/terraform-provider-jamf
    - https://registry.terraform.io/publish/provider/github/sioncojp/terraform-provider-jamf
  - 請求書に対して妥当かどうかのチェックフロー: 各SaaSのbillingメールをslackに飛ばして、それにレスポンスする形
  - 各サービスのSSO設定
  - オフィスネットワーク構築: L3, L2, AP（全てmeraki）で構築し、構成図、運用手順、情報等は全てgithubで管理
    - ref: https://tech.timee.co.jp/entry/2020/07/20/135854
  - MDM Jamfの提案、導入
  - crowdstrikeの提案と導入
- DRE
  - 立ち上げとコードレビュー + 運用
  - gcpをterraformで管理
  - DL -> ETL -> DW -> DM の流れでBQを活用した設計提案とチーム作り
- SRE
  - [terraform0.12 -> 0.13の検証](https://sioncojp.hateblo.jp/entry/2020/10/13/195117)
  - 新規事業のインフラ設計と構築/運用: awsアカウントやVPC、peering作成...Fargateでdeploy出来るところまで
  - 各LPサイトの構築: s3 webhostring + cloudfrontで構築 or vercel
  - [チームマネジメント](https://sioncojp.hateblo.jp/entry/2020/04/06/153619)
  - railsをコンテナで動かした時のmemory leak対応
  - 各SaaSのSSO化
  - datadogのterraform化 + dashbaord/アラート設計
  - Goでrails c用cliツールを作成
  - Fargateをfirelensに移行: fargate -> firehose -> datadog, s3
  - slack deploy導入: Go
  - Railsのjemallocによるメモリリーク対応
  - Rails on EC2 -> Fargate
  - ecs-deployツール作成: Go 
  - aws再設計作り直し: awsアカウントのマルチアカウント構成（root, prod, stg, operation, sandbox....)

## FOLIO
2018/5 ~ 2020/1/4

### 業務内容
- batch/cron実行基盤をFargateで実行できるように設計、導入
  - [Fargate + cloudwatch eventでcronシステム構築](https://sioncojp.hateblo.jp/entry/2019/09/06/125617)
  - [Fargate + cloudwatch eventでcronシステム ロギング設計編](https://sioncojp.hateblo.jp/entry/2019/09/10/183409)
- ECS検証、設計、module化、本番導入
  - serviceのコンテナ入れ替え検知 + slack通知を[Goで実装](https://github.com/sioncojp/ecs-update-notify)
  - deployツールはGoで書いてる
- slack chatops deploy導入: Go + supervisor
- 社内用fmサーバ導入（社内ラジオ）: hugo(Fargate) + s3（音声）
- landing pageサイト構築: - s3 hosting + cloudfront + waf

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
