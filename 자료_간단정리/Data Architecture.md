# Data Architecture

## 정의
    - 수집부터 변환, 분배, 소비에 이르기까지의 Data 가 관리되는 방식
    - Data 와 Data Storage System 을 통해 Data 가 이동하는 방식에 관한 청사진 제공
    
## Architecture 종류

### EA (Enterprse Architect)
    단일 Project, 회사의 미래 Business 전략에 맞추어 향후 모든 Project 에 대한 Architecture 에 대한 책임을 짐
    
### BA (Business Architect)
    조직이 하는 일, Business 의 전반적인 이해를 바타으로 전체 Business Process 또는 IT 전략에 대한 설계 진행
    
### AA (Application Architect)
    Business 를 운영하기 위한 IT System 의 환경을 설계하는 역할
    
### SA (Solution Architect)
    Project 나 어떤 Business 요구사항에 따라, 개발 환경과 같은 Solution 에 대한 설계 담당
    
### DA (Data Architect)
    Business 나 Project 전체의 Data 와 관련된 Architecture 담당

### TA (Technical Architect)
    Mission Critical Application 을 지원하는데 필요한 기술 Infra (HW, SW, Networking)
    
## Data 관리 System 의 유형

### Data Warehouse
    Enterprise 전반의 다양한 RDS (관계형 Data Source) 의 Data 를 하나의 일관적인 중앙집중식 서비스

### Data Mart
    HR 부서와 같이 단일 Team, 조직 내 특정 사용자 Group 에 중요하고 필요한 일부 Data 를 포함
    
### Data Lake
    원시 Data 를 보통 PetaByte 규모로 저장하며, 정형 Data 와 비정형 Data 를 모두 저장할 수 있으므로 다른 Data Storage 와 차별화
    
## Data Architecture 유형

### Data Fabric
    Data 제공자와 Data 소비자 간 Data 가치 사슬에서 Data 통합, Data Engineering 및 거버넌스의 자동화에 중점을 둔 Architecture
    
### Data Mesh
    Business Domain 에 따라 Data 를 조직화하는 탈중앙집중식 Data Architecture
