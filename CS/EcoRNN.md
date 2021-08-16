# EcoRNN: Efficient Computing of LSTM RNN on GPUs

## Published in MICRO 2018 

|tag|
|------|
|CS|
|ML|
|NLP|

[paper](https://www.microarch.org/micro51/SRC/posters/20_zheng.pdf)  

-------

Tensorflow와 MXNet에 구현된 LSTM은 많고 작은 gpu 커널 호출

NIVIDIA's deep learning library인 cuDNN은 2배의 성능 향상할 수 있으나 비공개 소스이고 유연하지 않음. 이는 PyTorch같은 frameworks의 성능 개선과 연구 방해  


제시한 EcoRNN을 이용하면 최대 3배 성능 향상.  

EcoRNN 을 MXNet Python Library에 open-source로 통합  

-----
ML compiler가 있어 쉽게 frontend interface에서 동적 코드 최적화 수행 가능  

ML programmers는 사용하고 싶은 것을 hyperparameters를 명시해 사용 가능 

microbenchmark는 다르게 구현된 backends(Default, cuDNN, EcoRNN)의 runtime을 milliseconds안에 비교한다. 그리고 가장 좋은 것을 선택해 몇 시간 동안 학습시킨다.  


## 의문
### paper를 다 읽으면 해결될 것 같음
- microbenchmark 구현
- 표에서는 Y = X\*WT 를 YT = W\* XT 로 하면 Runtime은 짧아지고 자원 활용은 늘어나는데 왜 이렇게 동작하는지

### paper를 다 읽어도 모를 거 같음
- ML compiler의 동작 원리
- cuDNN의 구조
- 지금까지 ML Library는 왜 EcoRNN 방식으로 안 했는지
