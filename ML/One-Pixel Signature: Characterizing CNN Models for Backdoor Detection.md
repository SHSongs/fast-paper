# One-Pixel Signature: Characterizing CNN Models for Backdoor Detection


[paper](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123720324.pdf)  

1픽셀 Signature: 백도어 감지를 위한 CNN model 특성화


backdoor detection을 위해 One-Pixel Signature 방법을 제안한다. 기존 detector보다 30% 정확도가 높다.  

black-box CNN모델에 내부 파라미터 접근 없이  효과적으로 계산 가능하다.  

Fig. 2  
학습 과정  
CNN model에서 만든 signature를 Trojan detector가 분석한다.  


Fig. 3  
CNN model이 학습 sample이 된다.  
- 왼쪽 그림: backdoored CNN detector를 훈련시키기 위한 CNN trojan을 만들기 위해 "vaccine" 랜덤 패턴을 생성한다.   
- 오른쪽 그림: backdoored CNN detector에 알려지지 않은 "virus" 패턴을 이용해 생성되는 모습  

CNN trojan에서 나온 SIGtrojan의 모습이 뭉처있는 점처럼 보이는데 신기하다.  

******

어떤 아이디어인지 잘 이해가 되지 않는다.  
signature?
