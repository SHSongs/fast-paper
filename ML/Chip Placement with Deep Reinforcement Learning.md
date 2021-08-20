# Chip Placement with Deep Reinforcement Learning

|tag|
|------|
|ML|
|RL|
|Chip|

[paper](https://arxiv.org/pdf/2004.10746.pdf)    

## 22 Apr 2020

chip 배치를 강화학습을 통해 배치한다.  
제시한 방법은 end-to-end 이며 6시간 안에 placements를 생성한다.  
반면 사람 전문가가 몇 주가 걸린다.  


***** 
Figure 1.  
RL agent(policy network)는 macro를 매 time마다 배치하고, 모든 macros가 배치되면 standard cells이 force-directed method를 이용해 배치된다.   
reward는 wire의 길이와 혼잡도(congestion)의 선형 조합이다.  

Figure 2.  
Policy와 value network 설계도.  
정보(netlist adjacency, node features, current macro)를 임베딩 후   
Policy network는 배치 가능한 위치 확률 분포
Value network는 현재 미치에 대한 예상 보상의 추정치  

Figure 3.  
Zero-Shot, Finetune, Scratch Trained 된 network의 Placement Cost 비교  

Figure 4.  
처음부터 학습한 network vs finetune된 network   

Figure 5.  
dataset 개수에 대한 RL Cost 비교, Small Medium Large, dataset이 커질수록 수렴이 잘 됨  

Figure 6.  
zero-shot placements from the pre-trained policy와 finetuned policy 배치 시각화  
zero-shot placements는 이전에 볼수 없던 배치  
pre-trained policy network  (with no fine-tuning) 는 최적에 가깝고 인간의 직관과 유사하게 배치(cell이 mecros에 둘러쌓이고 canvas의 중심)  

Figure 7.  
사람 전문과와 제시한 방법의 사진. 디자인이 독점적이기 떄문에 블러처리 되있음

****

상당히 표가 많았다.  
후에 paper를 자세히 읽어봐야겠다.  
Zero-Shot Learning이 뭔지 찾아봐야 겠다.  
google이 어떻게 chip placement dataset을 만들었는지.  
network의 자세한 구조.  
학습 방법 acter-critic을 사용한 것인가?  
