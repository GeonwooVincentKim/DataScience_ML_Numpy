# NumPy

## 정의
    - 행렬이나 일반적으로 대규모 다차원 배열을 쉽게 처리할 수 있도록 지원하는 Python 의 Library
    - Data Structure 외 수치 계산을 위해 효율적으로 구현된 기능을 제공

## 장점
    Powerful N-Dimensional Array
    - NumPy 에서 배열 및 Vector 를 표현하는 핵심 구조인 ndarray 를 사용하여 빠르고 Memory 를 효율적으로 사용 가능 
    
    Numerical Computing Tools
    - 반복문을 작성할 필요 없이 전체 Data 배열에 대해 빠른 연산을 제공하는 다양한 표준 수학함수를 제공
    
    Performant
    - 잘 최적화, Compile 된 C/C++ Code 를 사용하여 빠른 연산을 가능하게 함
    
## Numpy Programming 기초
```python
import numpy as np
```
    - 행렬 및 Vector 연산을 위해선 다차원 Array 사용 필요
    - 다차원 Array 형태인 핵심적인 객체를 ndarray 라고 부름
    
```python
ndarray.ndim
ndarray.shape
ndarray.size
ndarray.dtype
ndarray.itemsize
ndarray.data
```

### 배열 생성
    - 기본적인 NumPy 배열 생성은 np.array() 함수를 통해 Python list 를 인자로 받아 아래와 같이 생성 가능

```python
a = np.array([0, 1, 2])
b = np.array([(1.5, 2, 3)NumPy, (4, 5, 6)])
print(a)
print(b)

# 실행결과
# array([0, 1, 2])
# array([[1.5, 2. , 3. ],
#        [4. , 5. , 6. ]])

### 아래와 같은 방법으로도 NumPy Array 생성 가능
np.zeros()
np.ones()
np.empty()
np.arrange()

# 실행결과
# array([0., 0.]) 
# array([1., 1.]) 
# array([0, 1, 2, 3])
```


