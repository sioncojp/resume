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

# Educational background
- Graduated Hiroshima Shudou High School
- Graduated Japan Electronics College: Computer Network department


# Career
## FOLIO
2018/5 ~ 

### Job description 
#### Design and implement batch / cron execution platform to run on AWS Fargate
- batch: fargate runtask
- cron: fargete + cloudwatch logging
- logging: firehose, datadog logs, s3

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
