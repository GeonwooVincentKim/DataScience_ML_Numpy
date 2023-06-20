# AlexNet
## AlexNet 구조
    - 8개 Layer 로 구성
    - 5개 Convolution Layer + 3개 Full-connected Layer

## 1st Layer
    - 96개의 11 x 11 x 3 Size Kernel, 입력 영상을 Convolution 함
    - Convolution Stride 을 4로 설정, zero-padding 은 사용하지 않았음
    - zero-padding 은 Convolution 로 인해 특성 맵의 Size 가 축소되는 것을 방지, 또는 축소 정도 감소
      -> 가장자리 부분에 0 추가

    - ReLU 함수로 활성화, local response normalization 시행

## 2nd Layer
    - 256 개의 5 x 5 x 48 Kernel 사용, 전 단계의 특성맵을 Convolution 해줌
    - Stride 는 1, zero-padding 은 2로 설정
    - ReLU 함수 활성화, Stride 2 시행을 통해 13 x 13 x 256 특성맵 획득
    - local response normalization 시행, ReLU 함수 활성화

## 3rd Layer & 4th Layer
    - 384 = 3 x 3 x 256 Kernel, 전단계 Convolution
    - Stride 와 zero-padding 모두 1로 설정 -> 13 x 13 x 384 특성맵, ReLU 함수 활성화

## 5th Layer
    - 256 = 3 x 3 x 192 Kernel, 전단계 Convolution
    - Stride 와 zero-padding 모두 1로 설정 -> 13 x 13 x 384 특성맵, ReLU 함수 활성화
    - 3 x 3 overlapping max-pooling 을 stride 2 로 시행 -> 6 x 6 x 256 특성맵

## 6th Layer & 7th Layer
    - 6 x 6 x 256 특성맵 flattern, 6 x 6 x 256 = 9216 차원 Vector
    - 4096 개 뉴런과 fully connected, ReLU 함수 활성화

## 8th Layer
    - 1000 개의 뉴런, 전단계 4096 개 뉴런과 fully connected
    - 1000 개 뉴런 출력 값에 softmax 함수를 적용, 1000개 Class 에 각각에 속할 확률을 나타냄

## 출처
    - https://bskyvision.com/entry/CNN-%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98%EB%93%A4-AlexNet%EC%9D%98-%EA%B5%AC%EC%A1%B0
    - https://velog.io/@lighthouse97/AlexNet%EC%9D%98-%EC%9D%B4%ED%95%B4
