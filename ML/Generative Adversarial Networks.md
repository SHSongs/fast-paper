# Generative Adversarial Networks

|tag|
|------|
|ML|
|Vision|
|Generation|

## 10 Jun 2014

[paper](https://arxiv.org/pdf/1406.2661.pdf)  

생성모델 G (generative)과 판별모델 D (discriminative)가 동시에 학습된다.  
G는 데이터 분포를 캡처  
D는 G가 아닌 training data의 sameple일 확률 추정   
G는 D가 실수할 확률을 최대화  

이 framework는 minimax two player 에 해당한다.  

G가 생성한 가짜 데이터를 D는 1/2확률로 맞추는 고유한 솔루션 존재  

G와 D가 multilayer perceptrons 으로 정의되어 있으면 전체 시스템은 backpropagation으로 학습 가능.  
훈련중이나 sample을 생성할때는 Markov chains나 unrolled approximate inference networks는 필요하지 않다.  

Vlaue function V(G, D)에서 G와 D는 서로 다른 목적을 가진다.  
G는 V(G, D)를 최대한 작게  
D는 V(G, D)를 최대한 작게  
하는게 목표다.  

이런식으로 학습하면 처음에 G와 D는 둘다 성능이 좋지 못하다 D가 real data를 더 잘 분류하기 시작한다. 그러다 G의 성능도 올라가고 결국 D는 G가 생성한 sample을 1/2확률로 구분한다.  (D는 G가 생성한 sample인지 구분 불가) 


******

GAN 모델의 시작 paper를 살펴봤다. 그림과 abstract만 봐서 잘 이해가 되지 않는데 실제 코드로 구현해보면서 한번 깊게 이해해야 겠다.  

