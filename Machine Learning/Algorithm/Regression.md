## Linear Regression  
1. 수치형 설명변수 X와 연속형 숫자로 이루어진 종속변수 Y 간의 관계를 선형으로 가정하고, 이를 가장 잘 표현할 수 있는 회귀계수를 데이터로부터 추정하는 모델. 
2. Activation Function: Y=Wx+b  
3. Cost Function : MSE(오차 제곱합)  
 ex) 33명의 성인 여성에 대한 나이와 혈압 데이터를 가지고, 회귀계수를 구할 수 있고, 이를 통해 나이를 한 살 더 먹으면 혈압이 약 얼만큼 증가하는지 알 수 있다.  
4. 혈압이라는 연속형 숫자 대신, 범주형 변수를 이용한다면?
 ex) 나이와 암 발생여부(1이면 발생, 0이면 정상) 데이터가 주어졌을 때, 위와 동일한 방식으로 회귀모델을 구축하고 그래프로 그리면 이상한 모양이 나온다.  
5. 따라서, Y가 범주형(Categorical) 변수일 때는, 선형회귀 모델을 그래도 적용할 수 없다. 그래서 Logistic Regression이 탄생했다.  

코드: <https://github.com/eunhwa99/NLP/blob/main/02-1.%20Linear%20Regression.ipynb>

## Logistic Regression  
1. 실제 값과 비교하여, 예측 값과 실제 값이 가깝도록 학습하고, 새로운 값이 입력되면 그것을 분류하여 클래스에 속할 확률을 출력하는 학습 모델로, 데이터를 두 개 혹은 그 이상의 그룹으로 분류하는 문제에서는 로지스틱 회귀분석이 가장 기본적인 방법이다.   
2. Activation Function: Sigmoid, Softmax  
2-1) Sigmoid: 치역이 0과 1사이, Binary Classification 
2-2) Softmax: 확률의 합이 1이다, Multiple Classification  
3. Cost Function: BCE, CE  
3-1) BCE: Binary Cross Entropy (이항 분류)  
3-2) CE: Cross Entropy (다중 분류)  

코드: <https://github.com/eunhwa99/NLP/blob/main/03.%20Logistic%20Regression.ipynb>

### Binary Classification
- 현재 딥러닝에서 분류에 대해 가장 흔히 사용되는 손실함수는 Cross Entropy Error (CEE) 이다.  

  ![image](https://user-images.githubusercontent.com/68810660/104878350-1c09ab80-599f-11eb-9bc5-fa6e96dd5f88.png)  
  t는 정답 값, y는 추론 값

- sigmoid: 이진분류에서 가장 많이 사용되는 활성화 함수
- softmax: 다중분류에서 가장 많이 사용되는 활성화 함수

- 이진분류를 CEE로 나타내면 L=-(tlog(y)+(1-t)log(1-y)), 참(1)/거짓(0)

