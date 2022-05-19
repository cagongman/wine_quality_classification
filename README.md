# Project

대회 url: [https://dacon.io/competitions/official/235610/data](https://dacon.io/competitions/official/235610/data)

## 연구 목적

와인에 들어있는 각종 화학성분들의 데이터를 사용하여 와인의 품질을 분류하거나 예측하는 모델을 생성하는 것을 목표로 하고 있다.

## 탐색적 자료분석

### **Data 특징**

- **index 구분자 
(key)**

- **quality 품질 
(target)**

- fixed acidity 
산도

- volatile acidity 
휘발성산

- citric acid 
시트르산

- chlorides 
염화물

- free sulfur dioxide 
독립 이산화황

- total sulfur dioxide 
총 이산화황

- density 
밀도

- pH 
수소이온농도

- sulphates 
황산염

- alcohol 
도수

- type 
종류

- residual sugar 
잔당

데이터의 변수로는 총 13가지로
index 변수에는 unique한 id 값을 가지고 있다.

quality는 target 변수로 0~10 까지의 값을 가지고 있고 높을수록 좋은 quality를 의미한다.

type변수를 제외한 나머지 변수는 와인 안의 화학성분들로 모두 실수형의 값으로 저장되어 있다.

type 변수는 와인의 종류로 red wine, white wine 두가지 종류로 표시되어 있다.

### 데이터 수

train data는 5497개 (target: quality 값이 있음)

test data는 1000개 (target: quality 값이 없음)

quality별 데이터의 수를 봤을때 중간 정도(6)의 quality를 가지는 와인의 데이터 수가 가장 많은 것을 확인할 수 있다.

0부터 10까지의 quality로 나눠져 있다고 했지만 실제 데이터에는 3부터 8까지의 quality를 가지는 와인만이 존재했다.

![Untitled](Project%20be9a42c247674d1abffed537871603a8/Untitled.png)

### 결측치

train, test dataset 모두 결측치 없음

### Box plot

![Untitled](Project%20be9a42c247674d1abffed537871603a8/Untitled%201.png)

![Untitled](Project%20be9a42c247674d1abffed537871603a8/Untitled%202.png)

![Untitled](Project%20be9a42c247674d1abffed537871603a8/Untitled%203.png)

![Untitled](Project%20be9a42c247674d1abffed537871603a8/Untitled%204.png)

![Untitled](Project%20be9a42c247674d1abffed537871603a8/Untitled%205.png)

![Untitled](Project%20be9a42c247674d1abffed537871603a8/Untitled%206.png)

![Untitled](Project%20be9a42c247674d1abffed537871603a8/Untitled%207.png)

![Untitled](Project%20be9a42c247674d1abffed537871603a8/Untitled%208.png)

![Untitled](Project%20be9a42c247674d1abffed537871603a8/Untitled%209.png)

![Untitled](Project%20be9a42c247674d1abffed537871603a8/Untitled%2010.png)

![Untitled](Project%20be9a42c247674d1abffed537871603a8/Untitled%2011.png)

몇몇 변수에서 outlier 값이 존재하는 것을 확인할 수 있다.

### 상관관계

![Untitled](Project%20be9a42c247674d1abffed537871603a8/Untitled%2012.png)

## 프로젝트 진행 방법

**사용언어:** Python

**사용 툴:** jupyter notebook, pycharm, google Colab(이중에서 골라서 쓰면 될듯 함)

**사용 라이브러리:** Numpy, Pandas, Matplotlib, Seaborn, Scikit learn

### **Classification model**

0~10까지의 quality로 분류하는 분류 문제로 해당 문제를 해결한다.

**사용 예정 모델**

- SVM
- KNN
- Logistic regression

### **Regression model**

quality의 값을 예측하는 회귀 문제로 해당 문제를 해결한다.

**사용 예정 모델**

- Linear regression
- Polynomial regression

### Ensemble model

**사용 예정 모델**

- Random forest

### Boosting model

**사용 예정 모델**

- Gredient boosting
- Light GBM
- XG Boosting

### Deep learning model

단순한 신경망 구조를 설계하여 딥러닝 기법을 적용하여 학습을 진행하여 예측 또는 분류 문제를 해결한다.

- Multi Layer Perceptron (MLP)

### binary classification

red wine인지 white wine 인지를 판별하는 이진 분류 문제를 해결한다.
