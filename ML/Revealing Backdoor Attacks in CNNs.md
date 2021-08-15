# Universal Litmus Patterns: Revealing Backdoor Attacks in CNNs

## 15 May 2020

[paper](https://arxiv.org/abs/1906.10842)   



model 공격 종류
1. collision attack
> 잘못된 class 라벨링 등 여러 방법으로 model 학습 방해

2. backdoor
> 은밀하다. 특정 trigger를 input에 넣으면 잘못된 결과를 도출해냄.
> 매우 치명적임, 자율주행시 traffic sign classification model을 감염시키면 `stop sign`을 `speed limit sign`으로 인식하게 할 수 있음.

이는 인터넷에서 pre-training된 모델이 많아지면서 하면서 더욱 문제가 커짐.  


## ULPs(Universal Litmus Patterns)로 감염된 networks 분석

GTSRB, MNIST, CIFAR10, Tiny-ImageNet.으로 학습된 수백개의 **깨끗**한, **감염**된 model 준비  

classification model은 non-trainable 
ULPs와 Poisoned or Claean 은 trainable


장점: model을 forward pass만 시키면 돼서 빠름

### ULPs가 잘 동작하는 이유?
CNNs은 물체의 두드러진 특징 패턴 조합을 학습함 그리고 위치 특징은 변하지 않음.  
network가 감염되었을 때, trigger가 물체의 주요 특징이라는 것을 배움

각 ULP는 다양한 triggers의 집합이 되도록 형성,
그래서 오염된 network에 ULP를 사용하면 오염된 network는 높은 확률로 양성 반응을 보임  

## 의문
### paper를 다 읽으면 해결될 것 같음
- ULPs 초기화 어떻게 시키는지
- network 구조
- 일반화될수 있는지

### paper를 다 읽어도 모를거 같음
- 감염된 classification model을 이용해 segmentation, detection model 만들면 어떻게 되나?  
- NLP model에서 backdoor attack 방법