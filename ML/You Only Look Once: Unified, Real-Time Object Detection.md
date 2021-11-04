# You Only Look Once: Unified, Real-Time Object Detection

|tag|
|------|
|ML|
|Vision|
|Detection|
|YOLO|

## 9 May 2016

[paper](https://arxiv.org/pdf/1506.02640.pdf)


*****

기존은 복잡한 처리 과정을 거쳤지만, YOLO는 한번에 물체 감지를 수행한다.

장점: 
- 간단한 처리 과정
- class에 대한 맥락적 이해 높음, 이로인해 낮은 backgound error
- 물체에 대한 일반화된 특징 학습, 자연 이미지로 학습하고 미술품에 테스트했을 때 다른 detector보다 높은 성능
단점: 
- 낮은 정확도 (특히 작은 물체)

<br>
<br>

## Unified Detection
network design을 보며 입력과 출력이 어떻게 구성되었는지 본다.


### Network Design

paper에서는 488 \* 488 image가 여러 conv network를 거쳐 7 \* 7 \* 30 이미지로 변환된다.  

output인 7 \* 7 \* 30 tensor를 이용해 물체 인식을 할 수 있다.  
7X7은 49개의 Grid Cell을 의미하고  
Grid cell은 2개의 물체를 예측한다.  

1 \* 1 \* 30 의 Grid Cell의 0 ~ 5값은 첫번째 bounding box에 대한 값.  
6 ~ 10은 두번째 bounding box에 대한 값.  
10 ~ 30은 20개의 class에 대한 conditional class probability 값.  

bounding box의 confidence score와 각 conditional class probability를 곱하면 bounding box의 class specific confidence score가 나온다.  

이렇게 총 98개의 class specific confidence score 계산을 한다.

<br>

### Loss function

Grid cell의 여러 bounding box들 중, ground-truth box와의 IOU가 가장높은 bounding box를 predictor로 설정한다  

기호 3개가 등장한다.  
1. Object가 존재하는 grid cell i의 predictor bounding box j
2. Object가 존재하지 않는 grid cell i의 predictor bounding box 
3. Object가 존재하는 grid cell i
Ground-truth box의 중심점있는 grid cell은 object가 존재한다 여김.  

식 (1) 기호 **1**의 x와 y의 loss계산 * λcoord  
식 (2) 기호 **1**의 w와 h의 loss계산, IOU에 큰 box의 error 영향 적게 * λcoord  
식 (3) 기호 **1**의 confidence score의 loss 계산  
식 (4) 기호 **2**의 confidence score의 loss 계산 * λnoobj
식 (5) 기호 **3**의 conditional class probability의 loss 계산

- λcoord: coordinates(x,y,w,h)에 대한 loss와 다른 loss들과의 균형을 위한 balancing parameter. 
- λnoobj: obj가 있는 box와 없는 box간에 균형을 위한 balancing parameter. (일반적으로 image내에는 obj가 있는 cell보다는 obj가 없는 cell이 훨씬 많으므로)

<br>
<br>

## Limitation of YOLO
1. 각 grid cell이 하나의 클래스만 예측, 작은 object 여러개 붙어있으면 제대로 예측 못함
2. bounding box는 training data를 통해 학습, 새로운/독특한 형태의 bounding box는 정확히 예측 못함
3. 몇 단계의 layer를 거쳐서 나온 feature map으로 bounding box를 예측하므로 localization이 다소 부정확

<br>
<br>

## Experiments
Table1: 다른 real-time object detect system들에 비해 높은 mAP. Fast YOLO는 경우 가장 빠른 속도.

Figure4: Fast R-CNN과 비교했을 떄, 훨씬 적은 False-Positive. (low backgound error)

Table2: Fast R-CNN과 같이 동작시 Fast R-CNN을 보완. (yolo는 backgound error가 낮음으로)

Figure5: Natural image training -> Artwork detection 에서 매우 강한 모습.

*****

Figure5의 Recall Precision를 검색해보았다.  
- recall: 대상 물체들을 빠뜨리지 않고 얼마나 잘 잡아내는지
- precision: 검출된 결과가 얼마나 정확한지 즉, 검출 결과들 중 실제 물체가 얼마나 포함되어 있는지

검출율(recall)과 정확도(precision)는 서로 반비례 관계. 알고리즘의 파라미터를 조절해 검출율을 높이면 오검출(false alarms)이 증가하고 반대로 오검출을 줄이기 위해 조건을 강화하면 검출율(recall)이 떨어짐.

그래서 precision-recall 그래프를 그려 성능 변화 전체를 살펴본다.

*****

거의 처음 접한 paper 였다. 이때 번역기 없이 보겠다고 종이로 본 기억이 난다.

이 다음은 Fast RCNN을 살펴보려 한다.

precision-recall에 대해 알아 좋음
*****

## 참고
https://curt-park.github.io/2017-03-26/yolo/

https://darkpgmr.tistory.com/162