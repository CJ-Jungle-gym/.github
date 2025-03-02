# 🌿 CLOUD WAVE 5기 : CJ 올리브영 온라인 쇼핑몰 인프라 구축

![image](https://github.com/user-attachments/assets/604054a5-9329-4b3a-b073-3addc76dc995)

---

## 📌 프로젝트 개요

### **🔹 프로젝트의 시작**

K-뷰티의 대표 온라인 쇼핑 플랫폼인 **올리브영**에서는 **이벤트성 상품 출시 시 폭발적인 트래픽 증가**가 발생합니다.

이러한 **트래픽 폭증 상황에서 안정적인 구매 환경을 제공하는 것**이 중요한 과제가 되었습니다.

우리는 실제 시나리오를 바탕으로 **다음과 같은 세 가지 핵심 문제를 해결할 수 있는 아키텍처를 설계**하였습니다.

### **🔹 해결해야 할 핵심 과제**

- 1️⃣ **이벤트 트래픽 폭증을 효과적으로 처리하여, 사용자들이 원활하게 상품을 구매할 수 있도록 한다.**

- 2️⃣ **이벤트 트래픽이 기존 올리브영 서비스에 영향을 주지 않도록, 이벤트 시스템을 독립적으로 운영한다.**

- 3️⃣ **해외 사용자들도 빠르고 원활하게 이벤트에 참여할 수 있도록 글로벌 최적화된 서비스 환경을 구축한다.**

### **🔹 주요 트래픽 유형**

올리브영 서비스에서 발생하는 주요 트래픽 유형은 다음과 같습니다.

![image](https://github.com/user-attachments/assets/278a696f-194a-4bd1-ba4c-15f6b827389d)

- **이벤트 상품 구매 접속자** : 이벤트성 상품이 출시될 때 급증하는 트래픽을 분산 및 최적화
- **일반 상품 구매 접속자** : 올리브영 기본 서비스에서의 안정적인 트래픽 처리
- **해외 리전 상품 구매 접속자** : 글로벌 사용자들이 원활하게 서비스에 접근할 수 있도록 최적화

이러한 유형별 트래픽을 고려하여, **서비스의 가용성과 성능을 유지하는 것이 필수적**이었습니다.

### **🔹 프로젝트 목표**

이러한 문제를 해결하기 위해, 우리는 **운영계, 개발계, 이벤트계를 각각 분리하는 구조**를 설계하였습니다.

- **운영계** : 올리브영의 **일반 서비스 트래픽을 안정적으로 처리**하는 환경
- **개발계** : 새로운 기능을 개발 및 테스트하는 환경 (**CI/CD 자동화 적용**)
- **이벤트계** : 이벤트가 진행되는 동안 **자동으로 생성 및 제거되는 독립적인 환경**

이를 통해 **고객들에게는 원활한 쇼핑 경험을, 개발자들에게는 자동화된 운영 환경을 제공**할 수 있도록 구성하였습니다.

### **🔹 Jungle Gym 팀의 핵심 전략**

이 목표를 실현하기 위해, 우리는 다음과 같은 핵심 전략을 적용하였습니다.

- **트래픽 부하 분산** : **마이크로서비스 아키텍처(MSA) 기반**의 **이벤트 전용 인프라 구축**
- **자동화 및 운영 효율성** : **Terraform + AWS Lambda**를 활용하여 **이벤트 인프라를 자동 생성 및 제거**
- **비용 최적화** : **서버리스 아키텍처(ECS Fargate, CloudFront) 적용**으로 **필요할 때만 인프라 운영**
- **글로벌 최적화** : **AWS CloudFront**를 활용하여 **해외 사용자들에게도 빠른 응답 속도 제공**

### **🔹 프로젝트의 핵심 가치**

이러한 설계를 통해, 우리는 올리브영이 **더 많은 고객들에게 안정적이고 확장성 높은 서비스를 제공할 수 있도록 지원**하고자 합니다.

또한, **CI/CD 자동화, GitOps 배포, 보안 및 모니터링**까지 고려한 **완전한 클라우드 네이티브 환경**을 구현하였습니다. 🚀

---

## 👥 팀원 소개

| 마석재(PM) | 계현준 | 김찬수 | 연제민 | 이경민 | 장현아 |
| --- | --- | --- | --- | --- | --- |
| <img src="../images/마석제.jpg" width=150px> | <img src="../images/계현준.jpg" width=150px> | <img src="../images/김찬수.jpg" width=150px> | <img src="../images/연제민.jpg" width=150px> | <img src="../images/이경민.jpg" width=150px> | <img src="../images/장현아.jpg" width=150px> |
| <a href="https://github.com/MASEOKJAE">@MASEOKJAE</a> | <a href="https://github.com/kyebalza">@kyebalza</a> | <a href="https://github.com/ckqrhdl">@ckqrhdl</a> | <a href="https://github.com/jemsgusting">@jemsgusting</a> | <a href="https://github.com/rudalsss">@rudalsss</a> | <a href="https://github.com/hyeonahhh">@hyeonahhh</a> |

### **🔹 팀원별 담당 역할**

- **마석재** : 프론트엔드, DMS, 보안 및 인증 처리
- **계현준** : 백엔드 및 EKS 구축
- **김찬수** : EKS 구축, 클라우드 프론트, 키네시스
- **연제민** : DMS 구축, Terraform 관리
- **이경민** : CI/CD 구축, 모니터링 담당
- **장현아** : Lambda, DMS 및 ECS 구축

---

## **🛠️ 프로젝트 협업 도구 활용 방식**

| 협업 도구 | 로고 | 활용 목적 | 주요 활용 방식 |
| --- | --- | --- | --- |
| **JIRA** | <img src="https://cdn.worldvectorlogo.com/logos/jira-1.svg" width="100px"> | **일정 및 스크럼 관리** | - 주간 스프린트 계획 수립 - 태스크 상태 관리 (To Do, In Progress, Done) - 백로그 관리 및 우선순위 설정 - 주간 회고 (Retrospective) |
| **Notion** | <img src="https://upload.wikimedia.org/wikipedia/commons/4/45/Notion_app_logo.png" width="90px"> | **문서화 및 지식 공유** | - 아키텍처 설계 및 시스템 다이어그램 문서화 - 기술 연구 자료 정리 및 공유 - 회의록 기록 및 이슈 로그 관리 - 프로젝트 관련 주요 자료 정리 |
| **Slack** | <img src="https://upload.wikimedia.org/wikipedia/commons/d/d5/Slack_icon_2019.svg" width="90px"> | **실시간 협업 및 커뮤니케이션** | - 채널별 커뮤니케이션 (일반, 개발, 긴급 이슈 등) - 팀원 간 코드 리뷰 및 피드백 공유 - 긴급 이슈 발생 시 실시간 알림 및 대응 - JIRA, GitHub 등과 연동하여 자동화된 알림 수신 |

---

## 🌏 전체 아키텍처

<img src="../images/정글짐_아키텍처.png">

### 📌 아키텍처 개요

![image](https://github.com/user-attachments/assets/db828113-9f9f-414f-a0c3-d722d1ca43ea)

본 프로젝트의 아키텍처는 **개발계, 운영계, 이벤트계**의 3가지 환경으로 구성됩니다.

- **개발계** : 개발 및 QA 환경, 자동화된 CI/CD 적용
- **운영계** : 안정적인 운영을 위한 EKS 기반 인프라
- **이벤트계** : 이벤트 발생 시 자동 확장 및 비용 최적화된 아키텍처

### **🔹 개발계**

![image](https://github.com/user-attachments/assets/25a5489f-c0f3-4e9f-852e-383257615eac)

- **Jenkins Pipeline**을 사용하여 코드 테스트 → 보안 검사 → 컨테이너 이미지 배포 자동화
- **SonarQube + Dependency-Check** : 코드 품질 및 보안 점검
- **Trivy** : 컨테이너 이미지 보안 스캐닝
- **GitHub WebHook** : 코드 변경 감지 및 파이프라인 트리거

---

### **🔹 운영계**

**✅ ArgoCD**

ArgoCD를 이용하여 GitOps방식으로 EKS에서 GitOps방식으로 애플리케이션을 배포하고 관리

![image](https://github.com/user-attachments/assets/f2809af9-d567-41d3-a952-5cc5131eb59e)

**✅ EKS (Amazon Elastic Kubernetes Service)**

- **Multi-AZ 배포** : 가용성 보장
- **HPA (Horizontal Pod Autoscaler)** : CPU 부하 기반 Pod 자동 확장
- **Karpenter** : Node 자동 확장

---

### **🔹 이벤트계**

![image](https://github.com/user-attachments/assets/221ea1dd-3317-4e02-83cc-ad242e58c1f8)

이벤트 상황 발생 시 **대규모 트래픽 부하를 효과적으로 분산**하고,

**자동화된 인프라 배포 및 비용 절감**을 가능하게 하는 구조로 설계되었습니다.

### **✅ 아키텍처 개요**

이벤트 서비스는 **단기적인 고트래픽 환경**을 감안하여 **운영 서비스와 완전히 독립적으로 운영**됩니다.

![image](https://github.com/user-attachments/assets/ac395f29-da07-4d44-bdb1-065804ae44cf)

이를 위해 **운영계와 이벤트계를 완전히 분리**하는 전략을 적용하고, **서로 다른 컨테이너 이미지와 도메인**을 사용하여 환경을 완전히 격리하였습니다.

- **`prod` 도메인** : 운영계에서만 관리
- **`event` 도메인** : 이벤트 서비스에만 접근 가능

이러한 **분리된 구조를 통해 이벤트 서비스 장애 발생 시에도 운영 서비스에는 영향을 주지 않도록 설계**되었습니다.

또한, **이벤트 서비스에서 트래픽 부하가 발생하더라도 운영 서비스의 안정성을 유지할 수 있도록 고가용성을 확보**하였습니다.

### **✅ 이벤트 인프라 자동화**

이벤트 서비스는 **Terraform과 AWS Lambda를 활용하여 인프라 생성 및 제거를 자동화**하였습니다.

![image](https://github.com/user-attachments/assets/92c40043-9a64-44de-b732-da21bc2af493)

### **📌 이벤트 인프라 자동 생성 및 제거**

- **이벤트 시작 전일 (1일 오후 10시)** : `Terraform Apply` 실행 → 이벤트 전용 인프라 자동 생성
- **이벤트 종료 후 (4일 00시)** : 생성된 데이터를 운영계로 마이그레이션 후 `Terraform Destroy` 실행 → 불필요한 리소스 자동 정리

### **✅ Lambda를 활용한 Terraform 자동 실행**

Terraform의 **Apply와 Destroy를 자동화**하기 위해 **Lambda를 활용**하였으며, 실행 과정은 다음과 같습니다.

<p align="center">
  <img src="https://github.com/user-attachments/assets/88deb85b-c387-41a7-895a-1683b5f2f1fc" width="46%">
  <img src="https://github.com/user-attachments/assets/0a05e487-85f0-45a0-8fa6-756fd28d265b" width="46%">
</p>


1. **AWS Secrets Manager (ASM)에서 PEM 키 다운로드**
2. **EC2 인스턴스 생성 후 SSH 접속**
3. **GitHub에서 Terraform 디렉토리 및 `.tf` 파일 Clone**
4. **Terraform Init & Apply 실행 → 이벤트 서비스 인프라 자동 구성**
5. **Terraform Apply 과정에서 오류 발생 시 Slack 알림 전송 → 운영팀 즉시 대응 가능**

이를 통해 **이벤트 인프라의 배포 및 제거를 자동화**하고,

**문제 발생 시 신속한 트러블슈팅이 가능**하도록 설계하였습니다.

### **✅ DMS (AWS Data Migration Service)**

이벤트 종료 후, **이벤트 데이터는 운영계로 안전하게 마이그레이션**됩니다.

![image](https://github.com/user-attachments/assets/276d6016-1cb1-4521-947b-8761230e0776)

### **📌 DMS 데이터 마이그레이션 동작 방식**

1. **이벤트 종료 후, 이벤트계 DB 데이터를 운영계 DB로 전송**
2. **VPC 피어링을 활용하여 이벤트계 VPC와 운영계 VPC 간 안전한 네트워크 통신 구성**
3. **1시간마다 자동 동기화 수행**하여 **운영 데이터 최신 상태 유지**
4. **Terraform을 활용하여 DB 연결을 하루 단위로 생성 및 삭제**
    - **MITM (Man-In-The-Middle) 공격 예방**
    - **Lateral Movement 차단 (네트워크 보안 강화)**
    - **불필요한 리소스 사용 방지로 비용 최적화**

이러한 구조를 통해 **데이터 정합성을 유지하면서 보안성을 강화**하였습니다.

### **✅ 비용 최적화 전략**

이벤트계는 **한 달에 한 번만 운영되는 임시적인 환경**이므로,

**고정된 인프라 유지 비용을 줄이기 위해 AWS 서버리스 아키텍처를 적극 활용**하였습니다.

- **EKS 대신 ECS (Fargate) 사용** : 서버리스 환경에서 필요할 때만 실행
    
    ![image](https://github.com/user-attachments/assets/aa733cba-b233-4cff-b605-fca7a8821fec)

- **Lambda 활용하여 Terraform 자동 실행** → **운영 부담 감소**
    
- **VPC 및 리소스를 하루 단위로만 운영하여 연간 최대 96% 비용 절감**

---

### **✅ 성능 최적화 (CloudFront + ALB 연동)**
이벤트 계에서는 **전 세계 사용자가 몰릴 가능성이 높아**
**AWS CloudFront와 ALB를 연동하여 속도를 최적화**하였습니다.

![image](https://github.com/user-attachments/assets/afef1776-9d8a-47b1-9353-7a7026f8a65d)

이러한 구조를 통해 **글로벌 사용자의 서비스 응답 속도를 최적화**하였습니다.

---

### **🔹** 고가용성

서비스의 안정성을 보장하고, 장애 발생 시 신속한 복구가 가능하도록 **고가용성 인프라**를 구축하였습니다.

![image](https://github.com/user-attachments/assets/03643a44-81e9-4e71-87b6-7562516a62b3)

✅ **인프라 복구 자동화**

- **CloudFormation & Terraform 활용** : IaC(Infrastructure as Code) 방식으로 인프라를 자동 배포 및 복구 가능하도록 구성
- **재해 복구(Disaster Recovery) 대비** : 장애 발생 시 신속한 인프라 복구를 위한 IaC 적용

✅ **ECR 이미지 백업**

- **다중 리전 저장소 구성** : ECR 컨테이너 이미지를 **일본 리전(JP)과 한국 리전(KR)에 동기화**하여 서비스 중단 시 신속한 복구 가능

✅ **Multi-AZ (다중 가용 영역) 구성**

- **AZ-Replication 적용** : 모든 VPC가 **다중 AZ**로 구성되어 가용성을 극대화
- **이중화된 리소스 배포** : 애플리케이션, 데이터베이스(RDS, Redis) 및 컨테이너 서비스(ECS)가 **각 AZ에 분산** 배포되어 장애 발생 시에도 서비스 지속 가능

---

### **🔹 모니터링 및 로그 관리**

운영 및 이벤트 환경에서 발생하는 모든 데이터를 수집하고 분석할 수 있도록 구성하였습니다.

![image](https://github.com/user-attachments/assets/fc041be7-343b-432b-8ac8-54ed4914b24c)

- **Prometheus + Grafana** : EKS 메트릭 데이터 시각화
- **Alertmanager** : 에러 및 경고 Slack 실시간 알림
- **CloudWatch + Grafana** : ECS, Lambda, RDS 모니터링
- **Firehose + S3** : 이벤트 로그 저장 → **Athena 분석 예정**

---

## 🎯 트러블슈팅 사례

> 📌 문제 상황:


### ✅ **분석 과정**

### ✅ **해결 방법**

### ✔ **결과**

---
