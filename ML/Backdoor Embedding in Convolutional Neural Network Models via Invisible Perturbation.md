# Backdoor Embedding in Convolutional Neural Network Models via Invisible Perturbation


|tag|
|------|
|ML|
|Vision|
|Attack|



## 30 Aug 2018

[paper](https://arxiv.org/pdf/1808.10307.pdf)  

Deep learning model은 전통적인 machine learning model보다 월등히 뛰어나다  
DL은 널리 퍼지고 있고 안전이 매우 우려된다  



이전 방법들은 눈으로 보기에 티났지만 저자가 제시한 방법은 거의 티가 안나게 data를 조작할 수 있다.  

이전 방법들의 paper가 공개된 년도가 2017, 2018년 이던데 지금까지 연구가 시작된지 별로 안된거 같고 이전 방법들을 살펴 봐야겠다. 쭉 보고 정리해서 한글 자료를 만들어야겠다.  

-> 이전 paper  
- [Targeted Backdoor Attacks on Deep Learning Systems Using Data Poisoning](https://arxiv.org/pdf/1712.05526.pdf)  
- [BadNets: Identifying Vulnerabilities in the Machine Learning Model Supply Chain](https://arxiv.org/pdf/1708.06733.pdf)  

data를 만드는 두가지 방법을 제시한다.  
1. Static Perturbation Mask
2. Adaptive Perturbation Mask

자세한 방법과 장단점은 더 살펴봐야 알겠지만 이전 paper를 본 후 다시 봐야겠다.  

복잡한 pipeline으로 이루어진 ML model과 End-to-End model 중 무엇이 더 공격당하기 쉬울까?  
End-to-End는 data가 더 많이 필요하니까 공격용 data를 못 골라낼 확률이 높을까?  