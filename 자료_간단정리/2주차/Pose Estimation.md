# Pose Estimation 이란 (HPE - Human Post Estimation)

## Image 나 Video 에서 사람의 관절 (Key point) 이 어떻게 구성되어 있는지 위치 측정 및 추정 (Localization)
### Key point 란?
    - Head, Arm, Wrist, Knee, Ankle, torso
    - 자료 출처
        = https://ctkim.tistory.com/entry/Human-Pose-Estimation-%EA%B8%B0%EC%B4%88-%EC%9D%B4%EB%A1%A0-%EC%A0%95%EB%A6%AC
        = https://bkshin.tistory.com/entry/%EC%BB%B4%ED%93%A8%ED%84%B0-%EB%B9%84%EC%A0%84-12-%EC%9E%90%EC%84%B8-%EC%B6%94%EC%A0%95Pose-Estimation%EC%9D%B4%EB%9E%80

### Human Body Models

#### Skeleton-based Model
    - 사람 인식, 사람 위에 움직이는 관절부위를 탐지하여 미리 정해진 Skeleton 을 분할해서 투영해주는 것
    - 분할된 부분은 모두 skeleton 학습과 추출 가능
      -> 손과 같은 부분에도 이를 추출하여 제스쳐, 손동작 파악으로 사용 가능

    - 자료 출처
	  = https://wiserloner.tistory.com/1103
	  = https://reading-cv-paper.tistory.com/entry/CVPR-2019Skeleton-Based-Action-Recognition-with-Directed-Graph-Neural-Networks
	  = http://dmqm.korea.ac.kr/activity/seminar/351#:~:text=%EC%9D%B4%20%EC%A4%91%20skeleton%2Dbased%20HAR,%ED%98%95%ED%83%9C%EB%A1%9C%20%EC%9D%B4%ED%95%B4%ED%95%A0%20%EC%88%98%20%EC%9E%88%EB%8B%A4.

#### Contour-based Model (Active Contour Model)

##### 물체 내부와 외부의 energy minimization 을 통해 변형 가능한 Model 을 Image 에 일치시키는 기술
##### Object tracking, shape recognition, segmentation => Computer Vision 분야에서 널리 사용
##### Internal Energy
    - Curve 의 Shape 을 조절하는 식

##### External Energy 
    - Image Intensify 를 이용하여 Edge 를 찾도록 도와줌
    - Gradient 를 이용하여 정의할 수 있음
      = curve points 들이 너무 edge 에서 멀리 정의된 경우, 제대로 작동하지 않음
      = gradient vector flow (GVF) 를 이용

    - 의료영상 Segmentation 에서 빈번하게 이용되고 있음
    - 자료 출처
      = https://damio.tistory.com/m/74
      = https://nuguziii.github.io/survey/S-002/
      = https://www.edwith.org/medical-20200327/lecture/63155/

#### Volume-based Model

##### 3D 자세 추정에 사용하는 Model
##### Automated Construction of Complex Structural Models (복잡한 구조모델 자동화 구축)
###### Volume 이란
    - Application, DB 및 File System 이 Data 를 저장하는 Container
    - Host 가 Storage 의 Storage 를 Access 할 수 있도록 생성되는 논리적 구성 요소
    - Pull, Volume Group 에서 사용할 수 있는 용량에서 생성, 정의된 용량이 있음
    - 두 개 이상의 Drive 로 구성될 수 있지만, Volume 은 Host 에 하나의 논리적 구성 요소로 나타냄
    - 자료 출처: https://docs.netapp.com/ko-kr/e-series-santricity/sm-storage/what-is-a-volume.html

###### 지질학 및 지구물리학 Data
    - 구조적 Model (Structural Model)
    - 석유물리학 특성 (Petrophysical Properties)
    - Surface Model -> Volume Model 
      -> 수치적 처리 (Numerical Processing) -> App -> 운영 의사 결정 (Operational Decisions)

    - 자료 출처 : https://learninggeoscience.org/local/pages/?id=179

## Bottom Up
    - 전체 Image 에서 인체 주요 부위들을 먼저 찾은 뒤, 각 부위를 연결해 자세를 추정하는 방식
    - 특정한 Pose 또는 하나의 사람 객체의 Pose 로 Grouping 하는 방식 -> DeepCut Model

## Top Down
    - 먼저 사람 탐지 (Detect) 한 뒤, 탐지 결과를 바탕으로 인체 주요 부위를 찾아 자세 추정을 하는 방식
    - 사람 객체에서 관절을 추정

## Pose Estimation 중요성

### 사람의 Pose 를 잘 추적하여 사람의 행동에 대한 이해를 훨씬 세밀하게 잘 알 수 있게 됨
    - 자율주행에서 보행자 움직임 탐지 및 추적하여 종합적 판단하여 훨씬 안전하고 좋은 성능 만들어 낼 수 있음

## 자료 출처
	- https://bkshin.tistory.com/entry/%EC%BB%B4%ED%93%A8%ED%84%B0-%EB%B9%84%EC%A0%84-12-%EC%9E%90%EC%84%B8-%EC%B6%94%EC%A0%95Pose-Estimation%EC%9D%B4%EB%9E%80
 	- https://ivdevlog.tistory.com/1
  	- https://supermemi.tistory.com/entry/Human-Pose-Estimation-%EC%9D%B4%EB%9E%80-2022
  	- https://ctkim.tistory.com/entry/Human-Pose-Estimation-%EA%B8%B0%EC%B4%88-%EC%9D%B4%EB%A1%A0-%EC%A0%95%EB%A6%AC
  	- https://www.samsungsds.com/kr/insights/human_pose.html
  	- https://bkshin.tistory.com/entry/%EC%BB%B4%ED%93%A8%ED%84%B0-%EB%B9%84%EC%A0%84-12-%EC%9E%90%EC%84%B8-%EC%B6%94%EC%A0%95Pose-Estimation%EC%9D%B4%EB%9E%80
