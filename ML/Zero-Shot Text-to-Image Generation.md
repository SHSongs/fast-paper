# Zero-Shot Text-to-Image Generation

|tag|
|------|
|ML|
|Vision|
|Generation|

## 26 Feb 2021

[paper](https://arxiv.org/pdf/2102.12092.pdf)  

글을 이미지로  



지금까지의 text to image 는 dataset은 고정한 채 더 나은 모델을 찾는데 집중했다면, 제안한 방법은 데이터셋을 인터넷에서 가져오고 엄청난 파라미터 수로 학습시킨다.  

이미지와 글을 인코더에 넣는데 256\*256 이미지를 그대로 넣으면 메모리가 많이 필요하므로 32\*32 이미지로 줄인다.  
이미지와 글의 공통분포를 학습하는 autoregressive transformer 학습해서 이미지와 글을 concat한다.  

다른 생성 방법과 비교하는데 제안한 방법이 가장 validation과 가깝고 다른 방법(DF-GAN, DM-GAN, Attn-GAN)은 형태를 알아보기 힘들다.  


<br>

*****

이 paper를 작성하려면 비교대상인 generation기법들을 다 알고 사용하고 비교해야 하는데 ML paper를 작성하려면 상당한 배경 지식이 필요한 것 같다.  

Zero-Shot이 뭔지 찾아봐야겠다.  

사람은 생각해낼 수 있지만 엄청난 수련을 거쳐야 기록할 수 있다. (글쓰기, 그림 그리기)  
하지만 컴퓨터는 생각해낸 것을 바로 볼수 있는 게 좋은거 같다.  

컴퓨터 성능의 발전으로 수많은 시도를 할 수 있게 되어 ML이 발전할수 있는거 같다.  

[GPT-2 에서 개인정보를 빼내는 paper를 봤었는데](https://github.com/SHSongs/fast-paper/blob/main/ML/Extracting%20Training%20Data%20from%20Large%20Language%20Models.md) 이것도 학습시킬 때 특정 인물, 장소가 포함되어 있다면 image의 형태로 개인정보를 빼낼 수 있지 않을까 싶다.  