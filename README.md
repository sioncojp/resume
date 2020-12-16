[for Japanese](README.ja.md)

# Introduction
Birthday: 1987/12/28
Japanese
Ex-ProGammer, CS1.6 Asian champion 2012

http://qiita.com/sion_cojp
https://github.com/sioncojp
https://sioncojp.hateblo.jp
https://www.slideshare.net/shoheikoyama77/presentations
https://speakerdeck.com/sioncojp

I have philosophy on the following. 
- Work responsibly as a team instead of giving freedom
- Constructive and logical discussions
- Contribute to service growth and sales and get results.
- SRE but commit to ServerSide code if necessary

# Educational background
- Graduated Hiroshima Shudou High School
- Graduated Japan Electronics College: Computer Network department


# Career
## Timee
2020/1/5 ~ 

### Job description: Corporate Engineer
#### create terraform-provider for jamf
- https://github.com/sioncojp/go-jamf-api
- https://github.com/sioncojp/terraform-provider-jamf
- https://registry.terraform.io/publish/provider/github/sioncojp/terraform-provider-jamf

#### Checking flow for validity against invoices
- Sending each SaaS billing email to the slack and responding to it
- Also, as a criterion, it points to a slack pined for how much a pay-as-you-go or flat rate would be.

#### building an office network.
- Building a network of new offices
- Constructed in L3, L2 and AP (all meraki)
- All diagrams, operating procedures and information are managed on github.
- ref: https://tech.timee.co.jp/entry/2020/07/20/135854

#### MDM
- jamf proposal -> Introduction

#### security software installation and operation.
- Introducing crowdstrike.

### Job description: DRE
#### Lead of DRE work
- There are many additional posts and I can not write much code. But the team is requesting the lead business
- Mainly cross-sectional business, catching up on DRE related parts and proactively putting it into proposals and teams
- Participate in constructive discussions to help teams progress
- Review of code written by members + operation (fix bugs and etc...)

#### Manage gcp with terraform
- Install gcp to terraform
- GCP Project create by terraform
- Architecture around IAM, service account

#### Cue how to make an analysis base
- Figure out existing code in a repository
- DL-> ETL-> DW-> DM, architecture proposal using BigQuery and team building, kicked off

### Job description: SRE
#### verification of terraform 0.12 -> 0.13
https://sioncojp.hateblo.jp/entry/2020/10/13/195117

#### Design and build/operate infrastructure for a new business (Timey Delivery)
- Creating an aws account
- Create vpc
- Transfer route 53 operations to each account
- Creating RDS/ElastiCache
- added support for service, cron and runtask in ECS(Fargate)
- Creating a deploy mechanism (chatops via slack)
- ACM Creation
- Creating redash
- peering, etc.
- As for the front end, github actions can be used to deploy
- The part of the GCP that needed to be done with GCP was done with terraform.

#### Building each LP site.
- Built with s3 webhostring + cloudfront or went with vercel
- so this site https://timee.co.jp/jobs/

#### Team management
- https://sioncojp.hateblo.jp/entry/2020/04/06/153619
- 1on1 is weekly at first. Gradually shift to 2 per week
- Carry out 1on1 to work ways that are likely to get results and to expand the possibilities

#### Add Dockerfile to in-house next.js boilerplate
- because there was no Docker environment
- Enabled to start with make command
```shell
$ make help
docker/dev/build       docker build
docker/dev/run         docker起動
docker/ecs/build       docker build
docker/ecs/run         docker起動
```

#### Memory leak support when running rails in a container
- to be continued

#### SSO for each SaaS
- aws
- datadog
- sentry

#### datadog operation from terraform + architecture dashboard/alert
- Until now, manually set datadog, but now it with Terraform.
- Also added dashboard / alert settings
- As a result, it was possible to respond to a failure only when an alert was triggered

#### rails c command for Fargate architectrue
- As a task of rails on fargate, there was a problem that `rails c` could not be hit because the host or container could not be ssh.
- Also, since RDS only allows access from the basic private subnet, the only option is to allow access from a private instance.
- Launch a cli tool for rails c in Golang, doing the following
    - Saml authentication such as `saml2aws` is required.
    - Post a session on EC2 with session manager
    - Decrypt the parameter store data and set it to environment variables
    - Get commitHash value associated with prod / stg tag from ECR
    - Set required arguments + launch docker with commitHash image
#### firelens on Fargate
- before: Fargate-> cloudwatch-> firehose-> lambda-> datadog, s3
- after: fargate-> firehose-> datadog, s3
- so simple and cost-saving

#### Launch slack-deploy
- Enabled to deploy from slack
- slack-deploy is an in-house Golang tool
- https://twitter.com/i/status/1217724217350733824

#### jemalloc with Rails
- Jemalloc support to secure memory while preventing memory fragmentation due to memory leak
- Dockerfile modification

#### Rails on EC2 -> Fargate: staging, production
- Launch ecs-deploy in-house Golang tool
    - ECS task definition generation and registration
    - ECS service update
    - Fargate, cron (cloudwatch + fargate), runtask can be executed
- Encrypted information is stored in SSM parameter store
    - Launch Golang tool to manage parameter store
    - Https: //github.com/sioncojp/pstore

#### Verification fargate, cron(cloudwatch + fargate), runtaskを検証 and create Each Tutorial
- Verification because there was no knowledge whether it is able to apply to rails. and create tutorial
 
#### AWS re-architecture
- AWS multi account Configuration (root, prod, stg, operation, sandbox ....)
- Compatible with GSuite SSO. And create IAN module
    - RBAC Base
    - Assume role with root account
    - Each account has limited permissions
- Recreate from VPC
- terraform execute `make` command

## FOLIO
2018/5 ~ 2020/1/4

### Job description 
#### Design and implement batch / cron execution platform to run on AWS Fargate
- batch: fargate runtask
- cron: fargete + cloudwatch logging
- logging: firehose, datadog logs, s3
- [Cron system architecture with Fargate + cloudwatch event](https://sioncojp.hateblo.jp/entry/2019/09/06/125617)
- [Cron system logging design with Fargate + cloudwatch event](https://sioncojp.hateblo.jp/entry/2019/09/10/183409)

#### Design and implement AWS ECS/Fargate platform
- logging: firehose, datadog logs, s3 / fluentd
- Consciously as containers scale flexibly.
- Implement container replacement detection + slack notification of service with Go
    - https://github.com/sioncojp/ecs-update-notify
- Implement deploy tool with Go
    - Manage a wealth of https://github.com/sioncojp/fargate-deploy/ in-house private

#### slack chatops deploy introduction
- Go + supervisor

#### Implement In-house fm server platform (in-house radio)
- hugo(Fargate) + s3（audito/video files）

#### Implement landing page site
- s3 hosting + cloudfront + waf
- Since deploy tool was typescript, I threw PR around IAM authentication system.

### Language
Go/Python/TypeScript/Scala

### Other
terraform/aws/datadog/akamai/fluentd/jenkins

## fluct
2017/7 ~ 2018/3

### Job description 
- Rewrite the impression measurement platform to PHP-> Go and Migrate to CentOS7
- Docker the batch processing used in the log collection infrastructure and migrate to on-pre-> ECS

### Language
Go/PHP/Perl/Ruby/Python

### Other
terraform/aws/on-premiss/keepalived/puppet
ldap/cobbler/consul/apache/nginx/influxDB/grafana


## Eureka
2016/4 ~ 2017/2

### Job description 
-aws operation construction to support the traffic of pairs

### Language
Go/Ruby

## Other
terraform/aws/gcp
ansible/mackerel/Docker/nginx/bigquery/MySQL

## Livesense
2012/7 ~ 2016/3

### Job description 
- Develop a mobile site API for career change site with Rails
- Infrastructure and network to support all of the company's media with Livesense
- Build and provide in-house development environment with openstack

### Language
Ruby/Rails

### Other
keepalived, nginx, openstack, cisco, vyos, drbd, ldap
nfs, kvm, mackerel, nagios, munin, chef, ansible, packer, vagrant

## Bit-Isle
2008/4 ~ 2012/6

### Job description 
- Rental server of data center, network construction operation
- Hardware kitting, testing

### Other
Cisco, Juniper, server, kitting, ioDrive, Linux
