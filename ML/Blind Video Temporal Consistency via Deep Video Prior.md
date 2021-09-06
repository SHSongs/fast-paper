# Blind Video Temporal Consistency via Deep Video Prior

|tag|
|------|
|ML|
|Vision|

[paper](https://arxiv.org/pdf/2010.11838.pdf)    

## 22 Otc 2020

image처리는 좋은 알고리즘이 많지만, video 처리 알고리즘은 성능이 뛰어나지 못하다. 그림을 보면 일관성이 부족하다.  

기존 방법은 large data set에서 학습한 후 추론하는데 여기서 제안한 방법은 각 video에서 학습하고 추론한다.  


한계점
- test time에 상대적으로 긴 처리시간 
- 각 video마다 개별적으로  학습을 시켜야 한다

시간적 일관성을 위해 optical flow를 사용한 이전 방법과는 달리 video prior는 암묵적으로 신경망 훈련을 통해 시간적 일관성을 달성할 수 있다.  


********

학습법

이전의 learning-based 방법
- input frame과 processed frame으로 구성된 large-scale data이 필요함

제안한 방법
- test video로부터 직접 학습
- g^는 image operater f를 따라함
- g^는 다른 task에서도 적용될 수 있게 network의 type이 적용되지 않음
- 각 반복마다, 한 frame을 학습에 사용


*******

의문  

이전 optical flow를 이용한 방법을 조사해봐야겠다.  
opencv를 이용해 optical flow의 대략적인 내부 구조와 사용법만을 알고 있었는데 더 자세히 알아보고 opencv optical flow 함수를 살펴봐야겠음    


paper를 다 읽으면 해결될 것  
- image operater f는 어떻게 구성되있는지
- g^는 어떤 architecture를 사용했는지
- 성능 계산법  

*****

사람이 어떻게 흑백사진을 복원할까 생각
1. 많은 data로부터 object 대한 색을 학습함
2. 흑백으로 된 object를 감지하고 추론
3. object를 자신이 지금까지 본 일반화된 object와 비슷하게 채색한다
