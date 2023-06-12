# Pytorch

## 정의
    - 2017년 초에 공개된 DL Framework 로 개발자들과 연구자들이 쉽게 GPU 를 활용하여 인공 신경망 Model 을 만들고 학습시킬 수 있게 도와줌
    - Torch -> Pytorch 의 전신, Lua Programing 언어로 되어 있었으나, Python 으로 새로 작성된 Framework 인 Pytorch 의 탄생
    - Python 을 사용하면 맞춤형 Data 계층 및 Network Architecture 를 쉽게 생성 가능
    
## PyTorch Tensor
    Pytorch 는 Tensor 라고 하는 다차원 배열 Data 를 나타내며, NumPy 와 같이 인기 있는 다른 Python Framework 에서 Data 가 처리되는 방식과 비슷

```python
## Numpy Tensor

import numpy as np
np.array([[0.0, 1.3], [2.8, 3.3], [4.1, 5.2], [6.9, 7.0]])

array([[0. , 1.3],
[2.8, 3.3],
[4.1, 5.2],
[6.9, 7. ]])
```

```python
import torch

torch.tensor([[0.0, 1.3], [2.8, 3.3], [4.1, 5.2], [6.9, 7.0]])
tensor([[0.0000, 1.3000],
[2.8000, 3.3000],
[4.1000, 5.2000],
[6.9000, 7.0000]])
```
