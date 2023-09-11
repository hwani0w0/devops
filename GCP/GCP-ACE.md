# GCP-ACE

## Cloud Computing
1. On-demand Self Service
2. Broad Network Access
3. Resource Pooling
4. Rapid Elasticity
5. Measured Service

## Cloud Deployment Modles
- Public
  - AWS, GCP, Azure
- Private
  - Anthos, AWS Outposts, Azure Stack
- Muti-Cloud : Public 2 or more 각 특징적인 서비스
- Hybrid : Public-Private

## Cloud Service Models
- ZaS(XaaS)

## GCP
- 13 Subsea cable ex.US-EU
- 25 regions 73 zones 144 netwokrd edge (2022)
- Zone < Region < Multi-Region

## Compute Service Option
### Compute Engine
- Instance
- public or private images 사용 가능
- Google Cloud Marketplace
- instance group > autoscaling
- disk or google cloud storage
- SSH

### GKE
- 컨테이너오케스트레이션
- 컨테이너 관
- 오픈소스 쿠버네티스 기반

### App Engine
- 완전관리형. 서버리스.
- 소프트웨어 보안 업데이트
- Go, Java, .Net, Node.js, PHP, Python, Ruby
- 다른 구글서비스와 연결 seamlessly
- 구글보안서비스(Web Security Scanner) 통합

### Cloud Functions
- single-purpose functions
- JavaScript, Pytho3, Go, Java
- UseCases:
  - Data processing, ETL operation (video transcoding)
  - Webhooks to respond to HTTP triggers
  - APIs that compose loosely coupled logic
  - Mobile backend functions
  - FaaS

### Cloud Run
- 완전관리 Knative 기반
- 컨테이너용 서버리


## Storage & Databases
### Storage Options
#### Cloud Storage
- 일관된 확장 기능
- 대용량
- object storage
- 무제한 스토리지
- Storage Classes
  - Standard
  - Nearline : 스탠다드보다 저렴. 저장만 함. 한달에 한번 접속
  - Coldline : 더 저렴. 분기에 한번 접속.
  - Archive : 가장 저렴. 1년에 한번 접속
- Availability : region/dual-region/multi-region
#### Filestore
- NFSv3
- Use VMs, Kuberneteste
#### Persistent Disks
- Durable Block storage
- data, photo, vidio
- option
  - standard
  - solid state(SSD) : 높은 iops
- 지역마다 옵션 다름

### Databases
#### SQL/Relational
- Cloud SQL
  - fully managed
  - MySQL, PostgreSQL, SQL Server
  - HA across zones
- Cloud Spanner
  - scalable
  - HA across regions
  - 일관적인 복제
#### NoSQL
- Bigtable
  - fully m
  - scalable
  - hight th
- Datastore
  - 











