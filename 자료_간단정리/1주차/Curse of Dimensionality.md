# Curse of Dimensionality

## 정의
    - 차원 (Dimension) 이 증가하면서 학습 Data 수가 차원 수보다 적어져서 성능이 저하되는 현상
    - 차원이 증가할수록 변수가 증가하고, 개별 차원 내에서 학습할 Data 수가 적어짐
    - 변수가 증가한다고 반드시 차원의 저주가 발생하는 것은 아니며, 관측치보다 변수 수가 많아지는 경우에 차원의 저주 문제가 발생
    
### 차원이 늘어난다의 정의
    - 차원 = 변수의 수 = 축의 개수
    - 차원이 늘어난다 = 변수의 수가 많아진다 = 축의 개수가 많아진다 = Data 의 공간이 커진다
    
## 해결 방법
    - 훈련 Sample 의 밀도가 충분히 높아질 때까지 Data 를 모아서 훈련 Set 의 크기 키우기
    - 그러나 일정 밀도에 도달하기 위해 필요한 훈련 Sample 수는 차원의 수가 커짐에 따라 기하급수적으로 증가
    - 특성 수를 크게 줄여 차원 축소를 하면 훈련 속도가 빨라지고 시각화 좋아짐
        = 일부 정도 유실로 인해 성능 저하 가능성 있음
        
    - 원본 Data 로 훈련해서 시간이 오래 걸리는지 확인하고 차원 축소 여부를 결정할 필요가 있음
    
# PCA & t-SNE 비교분석

## PCA 정의
    - 분포된 Data 들의 주성분 (Principal Component) 를 찾아주는 방법
    - 예시) 2차원 좌표평면에 n개의 점 Data (x1, y1), (x2, y2), (xn, yn) 들이 타원형 분포되어 있을 때

### 주성분 정의
    - 특정 방향으로 Data 들의 분산이 가장 큰 방향 Vector 들
    - PCA 는 Data 하나하나에 대한 성분을 분석하는 것이 아닌, 여러 Data 들이 하나의 분포를 이룰 때, 이 분포의 주 성분을 분석해 주는 방법
    
### PCA 활용
    - 2D 점들의 직선 근사 (1차 함수)
    - 3D 점들의 직선 또는 평면 근사
    - eigenface 와 영상인식 응용
    - PCA 를 이용한 얼굴검출과 얼굴 인식
    - PCA 를 이용한 안경제거
       
## t-SNE 정의
    - 고차원 Data 를 저차원 Data 로 변환하는 차원 축소 (Dimensionality Reduction) 기법, 좋은 성능 -> 비선형 차원 축소 기법 (Nonlinear Dimensionality Reduction)
    - 차원 축소 목적 -> 시각화, Clustering, 예측 Model 일반화 성능 향상
    - 고차원 공간상의 Data Point 들의 위치를 저차원 공간상에서의 극적으로 표현해줌, Data 존재할 수 있는 군집들을 시각화해서 표현해주는데 강점을 갖고, 시각화에 주로 사용됨

### 차원 축소 3가지 Category
    - feature selection
    - matrix factorization
    - neighbor graphs
    
## 츨처

### 차원의 저주 출처
    - https://oi.readthedocs.io/en/latest/ml/curse_of_dimensionality.html
    - https://for-my-wealthy-life.tistory.com/40
    
### PCA & t-SNE 출처
    - https://darkpgmr.tistory.com/110
    - https://angeloyeo.github.io/2019/07/27/PCA.html
    - https://3months.tistory.com/571
    - https://minye-lee19.gitbook.io/sw-engineer/business-analytics/class/1-7-t-sne
    - https://skyeong.net/284
