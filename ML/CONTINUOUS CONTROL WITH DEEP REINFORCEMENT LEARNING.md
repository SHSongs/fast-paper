# CONTINUOUS CONTROL WITH DEEP REINFORCEMENT LEARNING

|tag|
|------|
|ML|
|RL|

## 5 Jul 2019

[paper](https://arxiv.org/pdf/1509.02971.pdf)  

****

continuous action spaces에서 작동할수 있는 actor-critic, model-free algorithm를 기반으로한 deterministic policy gradient 제시한다.  

end-to-end 학습  

****

deep learning의 발전으로 가공 안된 data(image, sound ...)를 이용해 문제 해결 가능

deep neural network가 action-value 근사

dqn은 discrete and low-dimensional action spaces 풀기 가능

dqn이 continuous action spaces를 풀려면 많은 계산을 해야 함

****

제시된 방법을 이용하면 DQN보다 더 적은 스탭으로 solution을 찾을 수 있음  

하지만 몇가지 한계점이 있다. model-free 접근법과 마찬가지로 solution을 찾기 위해서는 매우 많은 training episodes가 필요하다.


## 느낌
- continuous action spaces를 ddpg는 왜 할 수 있는지  
- actor-critic은 구현만 해보았는데 paper도 봐야겠다.
- 강화학습은 paper의 식 보다 코드가 더 직관적인거 같다.

