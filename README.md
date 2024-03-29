[for English](README_en.md)

# 自己紹介
1987/12/28 生まれ
元プロゲーマーで、2012年CS1.6のアジアチャンピオン

- qiita: http://qiita.com/sion_cojp
- github: https://github.com/sioncojp
- blog: https://sioncojp.hateblo.jp
- slideshare: https://www.slideshare.net/shoheikoyama77/presentations
- speakerdeck: https://speakerdeck.com/sioncojp
- note: https://note.com/sion_cojp

下記をベースに従事しております。
- 自由を与える代わりにチームとして責任もって働く
- 建設的でロジカルな議論をする
- サービスの成長と売上に貢献するために結果を出す

# 学歴
- 広島修道高等学校卒
- 日本電子専門学校コンピューターネットワーク科卒

# 職歴
## DXER
2022/10/1 ~ 現在
### 経営周り
- DXERや各事業がなぜ存在するかのIdea Docとそのフレームワーク作成
- MVPに向けての戦略
- MOAT模索
- 中長期ロードマップからのタスク分解、優先順位付け
- 採用

### PdM
- PRD/UserFlow作成
- 色々やってます

### Design
- Material Design 3 x TailwindベースのFigmaでUIデザイン

### バックエンド開発/設計
- 社内プロダクトのバックエンド設計/開発とレビュー
- Go x GraphQL

### フロントエンド開発
- Next.js + Tailwind + storybook

### 自社Chrome Extension開発/設計
- React
- 自社BPO用のツールとしてなにもないところから開発

## Chikaku
2021/3/1 ~ 2022/9/30

### 業務内容
#### flutterでアプリ開発検証
- now

#### 写真プリントサービスのモニタリングとSLI/SLOの策定とdatadogで設定
- 全てterraformで管理

#### 経営周りの手伝い
- 会社全体のMVVと戦略, プロダクトの戦略の策定

#### 写真プリントサービスのAPI/batch設計と実装と開発体制の改善
- Goで実装中
- API、テーブル設計、インフラまで全て実装
- メンバー3名
- ref: https://sioncojp.hateblo.jp/entry/2022/06/13/190923

#### 写真プリントサービスで使うGoのフレームワークサンプルを作成
- クリーンアーキテクチャベース
- docker-composeでDBにアクセスするtodoアプリ
- migrateの方法、testの書き方や実装の説明を社員に説明
- makeでコマンドを用意
```shell
$ make help
dist                    create .tar.gz linux & darwin to /bin
clean                   このMakefileで利用したファイルをクリアにする
build                   build
build/cross             create to build for linux & darwin to bin/
run                     go run
run/binary              run binary
go/get                  特定のパッケージをgo getする
go/mod_tidy             不要なgo packageを削除する
go/test                 go test
docker/build            docker build
docker_compose/up       compose起動
docker_compose/down     compose停止
docker_compose/down_all  compose停止 + 全てを初期化する
docker_compose/rebuild  appだけbuildし直す
migrate/up              migration. docker compose up後に実行できる
migrate/down            migrationのrollback. docker compose up後に実行できる
migrate/create          migrationファイル作成. migrations/ にup/downが作成される
```

#### テレビ電話サービス（API + Frontend）の構築、運用
- ２サービスをFargateで提供
- Frontendはvue + s3 + cloudfrontで、github actionsでCDを提供
- どちらもローカルで動くものを読解し、コード修正を施し、awsで稼働させた
- サービスがdjangoだったので、datadog logsにうまく流せるようlogger実装

#### datadogのterraform化
- awsのアカウント連携も全てterraformで管理するようにした

#### セキュリティ強化
- WAFを導入したり、クラッキングできないか検証して処置を施したりした

#### DBの統合
- 無駄なDBインスタンスがあったので、1つのRDSに統合した

#### RDSのAurora移行とRI購入
- https://sioncojp.hateblo.jp/entry/2021/06/18/153741

#### Fargate: cron移行
- 定期実行系をEC2 -> Fargateに移行
- 既存サービスのリバースエンジニアリング
- どんなロジックで処理をしているのかを資料にまとめて移行した

#### Fargate: runtask移行
- DB Migration系をruntaskで実行するようにした 

#### Fargate: service移行
- APIサーバをEC2 -> Fargateに移行
- 既存capistranoの処理を把握し、その上で移行

#### Fargate環境のベース部分の構築
- Fargate用module追加
- Faraget Spotを使うようにした
- Fargateのsandbox環境の構築、資料作成と説明
- https://github.com/sioncojp/pstore 導入
- https://github.com/sioncojp/ecs-update-notify 導入
- Fargate用deployロジック追加
- CI/CDの整備
- datadog logs archiveの導入
- firehose -> firelensにした

#### AWSのコスト削減
- 指数関数的に増え続けていたawsのコストを分析し、チケット化
- 横断的に相談しやすいようにOKRに設定
- 結果、50%のコストカットをした


## Timee
2020/1/5 ~ 2021/3/1

### その他
- VPoEっぽい動きをしてました
    - 基本的にCTOと密に思考/定義/浸透
    - エンジニア採用フローを整備（DMでやりとりしてたのを、出来る限りオープンなやりとりができるようにした）
    - 人事評価の定義
    - 全ポジションのJobDescription設定と、githubで管理するようにした
    - エンジニアのルールをgithubで管理するようにし、検索性をあげた
    - mgrのmgrっぽい動き
    - KGI -> NorthStarMetric -> KPI -> OKRの落とし込み計画
    - 組織戦略と経営戦略（長期計画等々。NDAレベルが多いので詳しくかけないです）

### 業務内容: コーポレートエンジニア
#### jamfのterraform-provider作成
- https://github.com/sioncojp/go-jamf-api
- https://github.com/sioncojp/terraform-provider-jamf
- https://registry.terraform.io/publish/provider/github/sioncojp/terraform-provider-jamf

#### 請求書に対して妥当かどうかのチェックフロー
- 各SaaSのbillingメールをslackに飛ばして、それにレスポンスする形
- また判断基準として、従量課金or定額ならいくらか、をslackのpinedに指している

#### 各サービスのSSO設定
- 出来るところまでdone

#### オフィスネットワーク構築
- 新しいオフィスのネットワークを構築
- L3, L2, AP（全てmeraki）で構築
- 構成図、運用手順、情報等は全てgithubで管理
- ref: https://tech.timee.co.jp/entry/2020/07/20/135854

#### MDM
- jamfの提案 -> 導入

#### セキュリティソフト導入と運用
- crowdstrikeを導入

### 業務内容: DRE
#### DRE業務のリード
- 兼務が多くコードはあまり書けないが、リード業をチームから依頼されてやっております
- 主に横断的に事業をみて、DREに関わるところをキャッチアップして先回りして提案やチームに落とし込み
- チームがうまく進むための建設的議論の参加
- メンバーが書いたコードのレビュー + 運用（バグが発生したら修正するなど）

#### gcpをterraformで管理
- gcpをterraformから叩けるようにした
- project作成からterraformで管理するようにした
- IAM, service account周りの設計

#### 分析基盤をどう作っていくか頭出し
- 既存のコードが単一リポジトリに集約されてたので把握
- DL -> ETL -> DW -> DM の流れでBQを活用した設計提案とチーム作り、キックオフをした

### 業務内容: SRE
#### terraform 0.12 -> 0.13の検証
- https://sioncojp.hateblo.jp/entry/2020/10/13/195117

#### 新規事業（タイミーデリバリー）のインフラ設計と構築/運用
- awsアカウントの作成
- vpc作成
- route53操作を各アカウントに移管
- RDS/ElastiCache作成
- ECS(Fargate)でservice, cron, runtaskが実行できるようにした
- deploy機構作成（slack経由のchatops）
- ACM作成
- redash作成
- peering等
- フロントエンドに関してはgithub actionsでdeploy出来るようにした
- GCPで必要な部分はterraformで行った

#### 各LPサイトの構築
- s3 webhostring + cloudfrontで構築 or vercelで行ったりした
- https://timee.co.jp/jobs/

#### チームマネジメント
- https://sioncojp.hateblo.jp/entry/2020/04/06/153619
- 1on1は最初は週1。徐々に週2にずらしていく
- 成果が出やすい働き方と、可能性を広げるための1on1をおこなっていく

#### 社内next.js boilerplateにDockerfileを追加
- Docker環境がなかったので追加
- makeコマンドで立ち上げれるようにした
```shell
$ make help
docker/dev/build       docker build
docker/dev/run         docker起動
docker/ecs/build       docker build
docker/ecs/run         docker起動
```

#### railsをコンテナで動かした時のmemory leak対応
- to be continue

#### 各SaaSのSSO化
- datadog
- sentry
- aws

#### datadogのterraform化 + dashbaord/アラート設計
- datadogを手動で追加してたのをterraform化
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
2018/5 ~ 2020/1/4

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
