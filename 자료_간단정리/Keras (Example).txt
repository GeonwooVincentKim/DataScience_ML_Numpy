# Keras (Example)
## 정의
    - 거의 모든 종류의 DL Model 을 간편하게 만들고, 훈련시킬 수 있는 Python 을 위한 DL Framework
    - Tensorflow 에서 Release 하였으며, 신속하게 실험을 해야 하는 연구자들을 위해 개발됨
    
## 특징
    - 동일한 Code 로 CPU 와 GPU 에서 실행 가능
    - 사용하기 쉬운 API 소유, DL Model 의 Prototype 을 빠르게 만들 수 있음
    - 합성곱 신경망, 순환 신경망 지원하며, 자유롭게 조합하여 사용 가능
    - 다중 입출력 모델, 층의 공유, Model 공유 등 어떤 Network 구조도 만들 수 있음
    
## Keras 일반적인 사용법

### Model 정의 방법

#### Sequential Class (가장 자주 사용하는 구조)

```python
from keras import models
from keras import layers

model = models.Sequential()
model.add(layers.Dense(32, activation='relu', input_shape=(784,)))
model.add(layers.Dense(10, activation='softmax')
```

#### 함수형 API (완전히 임의의 구조를 만들 수 있는 비순환 유향 Graph 생성)

```python
from keras import models
from keras import layers

input_tensor = layers.Input(shape=(784,))
x = layers.Dense(32, activation='relu')(input_tensor)
output_tensor = layers.Dense(10, activation='softmax')(x)

model = models.Model(inputs=input_tensor, outputs=output_tensor)
```

    - 함수형 API 사용하면 Model 이 처리할 Data Tensor 를 만들고, 마치 함수처럼 이 Tensor 의 층을 적용
    - Model 구조 정의, 어떤 Model 방식을 사용했는지 상관없으며, 이후 단계는 동일함
    - Compile 단계에서 학습 과정이 설정됨, Model 이 사용할 Optimizer, 손실 함수, 훈련 Monitoring 위한 필요한 측정 지표 지정
    
```python
from keras import optimizers

model.compile(optimizer=optimizers.RMSprop(lr=0.001),
              loss='mse',
              metircs=['accuracy'])
```

    입력 Data 의 Numpy 배열을 모델의 fit() Method 에 전달함으로써 학습 과정이 이루어짐
    
```python
model.fit(input_tensor, target_tensor, batch_size=128, epochs=10)
```

## 출처
    - https://gggggeun.tistory.com/110
    - https://tensorflow.blog/%EC%BC%80%EB%9D%BC%EC%8A%A4-%EB%94%A5%EB%9F%AC%EB%8B%9D/3-2-%EC%BC%80%EB%9D%BC%EC%8A%A4-%EC%86%8C%EA%B0%9C/
    - https://www.tensorflow.org/guide/keras/save_and_serialize?hl=ko#:~:text=Keras%EB%8A%94%20%EA%B5%AC%EC%84%B1%EC%9D%84%20%EC%83%9D%EC%84%B1,%EB%90%9C%20%ED%98%95%EC%8B%9D%EC%9D%84%20%EC%83%9D%EC%84%B1%ED%95%A9%EB%8B%88%EB%8B%A4.
