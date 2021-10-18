# BadNets: Identifying Vulnerabilities in the Machine Learning Model Supply Chain


|tag|
|------|
|ML|
|Vision|
|Attack|


## 11 Mar 2019

MNIST와 Traffic Sign Detection 공격

backdoor attack

[Universal Litmus Patterns: Revealing Backdoor Attacks in CNNs](https://github.com/SHSongs/fast-paper/blob/main/ML/Revealing%20Backdoor%20Attacks%20in%20CNNs.md)에서 백도어 어택 모델을 만들때 참조된 paper여서 읽는 중.

single target(하나의 라벨만 타겟), all-to-all(모든 라벨 i를 i+1로 인식하게) 등 다양한 공격 실험을 진행하였으며 성공률 또한 높아 치명적임을 알려줌.

아웃소싱과 전이학습 상황을 가정해서 실험을 진행함.

10%만 학습 데이터가 감염되도 공격이 성공한다. 

all-to-all attack 된 network의 첫번째 레이어를 시각화 했더니 공격에 이용되는 부분 발견. 
single target 은 시각화된 자료가 없는걸 보아 확연한 차이가 없는거 같음. 나중에 직접 실행해야겠다.  

*********

backdoor model을 직접 만들기 위해 보고있는 paper이다. 구현에 성공하면 RL에서도 backdoor를 만들어보고 싶다.