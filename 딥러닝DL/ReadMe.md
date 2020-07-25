# DeepLearningSeries
For Beginners like me

## [펀딥] Activation Function Series
 Activation Function Series

### 0. Intro + step
### 1. sigmoid
### 2. tanh
### 3. ReLU 
### 4. ReLU family (Leaky ReLU, PReLU, ELU, Maxout) 
### 5. Softmax (출력층 함수) 

**Key Word**

- 퍼셉트론 perceptron: 단층 퍼셉트론을 의미; 계단 함수 사용
- 신경망 neural network: 다층 퍼셉트론 의미; 다양한 활성화 함수 사용 가능
- 선형 함수 linear algorithm
- 비선형 함수 non-linear algorithm
- 오차역전파 알고리즘 back-propagation
- 경사 하강법 gradient descent
- 기울기 소멸 문제 gradient vanishing

------------------------------------------------------------------

#### 1. Intro + step

+ 활성화 함수:

```
a = h(w1x1+w2x2+b)
h(a) = 0 if (x<=0)
     = 1 if (x>0)
```
이때,
w = 가중치
x = 입력값
b = 편향
h(x) = 활성화 함수

+ 선형 함수 사용하지 않는 이유
  - 선형 함수는 1개의 직선으로 표기가 가능하다
  - 은닉층을 사용하는 이유가 없다
+ 비선형 함수: 직선 1개로 그릴 수 없는 함수


```
def step(x):
  theta = 0
  return np.array(x>0, dtype=np.int)
```


#### 2. sigmoid 

```
def sigmoid(x):
  return 1/(1+np.exp(-x))
```

+ 시그모이드 함수와 계단 함수 비교

+ 시그모이드 함수롸 tanh 함수 비교


#### 3. tanh

```
def relu(x):
  return np.maximum(0, x)
```

#### 4. ReLU + ReLU family


#### 5. SoftMax (출력층)

앞에서 신경망은 총 3 종류의 층으로 이루어져 있다고 했다. 

**입력층 -> 은닉층 -> 출력층**
