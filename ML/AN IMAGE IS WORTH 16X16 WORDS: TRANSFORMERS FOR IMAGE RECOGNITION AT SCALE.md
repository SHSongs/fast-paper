# AN IMAGE IS WORTH 16X16 WORDS: TRANSFORMERS FOR IMAGE RECOGNITION AT SCALE

## 3 Jun 2021

[paper](https://arxiv.org/pdf/2010.11929.pdf)


transformer는 nlp에서는 거의 표준으로 사용하고 있지만 vision에서는 convolutional networks와 결합하거나 convolutional networks의 특정 요소를 대체하는 등 전체적인 구조는 유지한채로 tranformer를 사용한다.  

이 paper에서는 conv net 없이 transformer만으로 이미지를 분류하고 state-of-the-art 성능을 낼 수 있는 방법을 제시한다.  

학습 흐름

이미지를 고정된 크기로 잘게 자른 후 선형 임베딩 한다. 그리고 위치 임베딩과 더한다.  
더한것을 transformer encoder에 넣는다.   
classification token 을 사용한다.  


****

vision, nlp, rl 등 여러분야에서 거의 표준으로 사용하는 기술을 다른 분야에 적용시켜 좋은 결과를 얻어내는 이야기를 많이 듣고 있다.  