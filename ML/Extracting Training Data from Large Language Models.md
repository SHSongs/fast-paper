# Extracting Training Data from Large Language Models


|tag|
|------|
|ML|
|NLP|
|Attack|

## 15 Jun 2021

[paper](https://arxiv.org/pdf/2012.07805.pdf)  

GPT-2 같은 LM(large model)에서 개인정보를 추출하는 방법을 연구한 paper이다.  

단 한번만 train data에 포함되 있어도 개인정보를 추출할 수 있다.  
Raddit URL을 훈련시키고 얼마나 URL이 기억되는지 실험했는데  
큰 모델일수록 처음 10000개에 생성된 문장에서 훈련시킨 URL이 나올 확률이 높다.  
중간 사이즈의 모델도 URL의 처음 6자를 제공하면 훈련시킨 URL이 거의 나왔다. 


하지만 attack을 하기 위해서는 사람이 직접 민감한 정보인지 가려내야 한다.  

ML을 적극적으로 시대가 될수록 개인정보를 추출하려는 사람 또한 늘어날 것이다. paper에서는 개인정보 유출 완화를 위한 방법들이 나와있다.  

*****

큰 모델이 memorization이 잘되는게 신기하며 어떤 원리로 memorization이 되는지 더 읽어봐야겠다.  

이전에 vision model의 backdoor attack관련 paper를 보았는데 다양한 공격 기법이 나올수록 pretrain된 model을 활용하는 것보단 처음부터 학습하는 기업이 늘어날 것 같고 점점 폐쇄적으로 될 것 같다.   

자동으로 개인정보를 추출하는 연구가 있는지 조사해야겠다.  