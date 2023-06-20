# Semantic Segmentation 이란?

    - Digital Image 를 여러 개의 Pixel 집합으로 나누는 과정
    - 분할을 통해 Image 표현을 해석하기 쉬운 것으로 단순화하여 변환하는 것
    - Computer Vision 분야에서 많이 사용 중임

## Computer Vision 이란
	- AI 의 한 분야, Computer 와 System 을 통함
	- Digital Image, Video 및 기타 시각적 입력, 의미 있는 정보 추출 및 작업 실행, 추천
    - AI -> Computer 가 생각, Computer Vision -> Computer 가 보고, 관찰하고 이해 가능
  	- 예시) DL 의 CNN (Convolutional Neural Network)
  	- 참고 자료 : https://www.ibm.com/kr-ko/topics/computer-vision

## Semantic Segmentation 에서 다뤄지는 문제들

### Classification (분류)
    - Input 에 대해서 하나의 Label 을 예측하는 작업, AlexNet, ResNet, Xception 등의 Model

### Localization / Detection (발견)
    - 물체의 Label 을 예측하면서 그 물체가 어디에 있는지 정보 제공
    - 물체가 있는 곳에 네모를 그리는 Model 들인 YOLO, R-CNN

#### YOLO Model (You Only Look One)
    - Object Detection 분야에서 많이 알려진 Model
    - 이미지 전체를 한 번 본 후, 주변 정보까지 학습하여 이미지 전체를 처리하는 Object Detection Model

#### YOLO Model 참고자료
	- https://dotiromoook.tistory.com/24#:~:text=%E2%9C%85%20YOLO%20(you%20only%20look%20once)%20%ED%8A%B9%EC%A7%95&text=%EC%89%BD%EA%B2%8C%20%EB%A7%90%ED%95%B4%2C%20%EC%9D%B4%EC%A0%84%20%EC%9D%98%20R,%EB%A5%BC%20CNN%EC%97%90%20%ED%86%B5%EA%B3%BC%EC%8B%9C%ED%82%A8%EB%8B%A4.

	- https://byul91oh.tistory.com/321

### Segmentation (분할)
    - 모든 Pixel 의 Label 을 예측
    - FCN, SegNet, DeepLab 등의 Model

## Semantic Segmentation AI 학습방법

### Class 는 AI 이 인식하길 원하는 것들로 설정
    - 배경, 사람, 나무 등 다양한 종류의 Object

### 원본 Image 를 미리 정의해둔 Class 에 따라 구분
    - AI 에게 정답을 알려주는 과정
    - 사람이 직접 이미지에 정답을 표시해야 하므로, 이런 작업할 수 있는 도구의 도움이 필요함
 
### 구분된 정보를 통해 각 Pixel 의 RGB 값이 변경된 Image 를 생성할 수 있음
    - 도구에서 보이는 구분은 작업의 편의성을 위해 다양한 색깔 존재
    - AI 학습을 위한 Data 는 조금 더 단순하게 만들 수 있음

### Class 와 RGB 값의 Mapping 정보를 통해 가공 Image 의 RGB 값이 어떤 Class 를 나타내는지 정의
    - 단순화한 가공 Image 일 경우, 각 Class 에 숫자 ID 붙이고, RGB 값 변경하는 방법 사용
    - 예) 사람 -> RGB(1, 1, 1), 차 -> RGB(2, 2, 2)

### 학습 Data 준비 완료되면 인공지능은 원본 Image 를 입력으로 받아 분석하고
    - Pixel 단위로 의미적 분할
    - 결과를 가공 Image 의 정답과 비교하는 과정을 통해 학습 가능

### 학습 완료되면, 카메라를 통해 얻는 Image 의 Semantic Segmentation 하여 자율주행 분야에서 활용
### 참고 자료
    - https://blog.testworks.co.kr/semantic-segmentation-tech-and-learning-method-through-deep-learning/
    - https://medium.com/hyunjulie/1%ED%8E%B8-semantic-segmentation-%EC%B2%AB%EA%B1%B8%EC%9D%8C-4180367ec9cb
