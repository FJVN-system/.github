# FJVN system

기간 : 기간 : 2022.12 ~ 진행중

## 프로젝트 개요 
- 기존에 만들었던 B2B 음반 거래 웹(admin, shop)의 고객사가 늘어남
- 고객사 별로 각각 개발, 배포를 하다보니 유지 보수가 어려움(ex. 기능추가시 두개 이상의 레포에 수정 및 배포 필요 등)
- CI/CD가 구현이 안되어 있어서 배포도 각각 진행했어야 함(Firebase로 배포중이라 각 회사별로 ID를 공유받아 각 ID로 배포 해야함)

## 개발 정의
- Admin은 하나의 앱으로 개발해서 일원화 -> 기능 개발 및 배포시의 관리포인트 최소화
- Shop은 각 회사별로 최초 1회 UI 수정 제공
- 기존 DB는 최초에 빠른 개발을 위해 Collection-Document 방식의 NoSQL인 Firebase의 Firestore로 개발되어있는 상태
- 현재 전체적인 테이블의 구조가 잡힌 상태이기 때문에 SQL로 구현
- API 서버는 Spring과 JPA를 이용해서 구현
- 회원기능은 AWS Cognito를 이용 -> Front에서 회원가입, 로그인, 인증 구현
- ECR을 이용한 컨테이너 환경으로 배포 및 Github Actions를 이용한 CI/CD 자동화


## 전체 아키텍쳐
![FJVN아키텍쳐](https://user-images.githubusercontent.com/104489626/221384282-87b8be46-7325-4124-8117-5a41f00ef756.jpg)

## FREE-STORE
### DNS 주소 [링크](http://fjvn-free-store.s3-website.ap-northeast-2.amazonaws.com)
 - http://fjvn-free-store.s3-website.ap-northeast-2.amazonaws.com

## DEMO-ADMIN 
### DNS 주소 [링크](http://fjvn-demo-admin.s3-website.ap-northeast-2.amazonaws.com)
 - http://fjvn-demo-admin.s3-website.ap-northeast-2.amazonaws.com

## API-SERVER
### DNS 주소 [링크](http://fjvn-api-server-prod-1286120377.ap-northeast-2.elb.amazonaws.com/healthcheck)
 - http://fjvn-api-server-prod-1286120377.ap-northeast-2.elb.amazonaws.com
 - http://fjvn-api-server-prod-1286120377.ap-northeast-2.elb.amazonaws.com/healthcheck
 
 
 





 
