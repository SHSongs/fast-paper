RandAugment: Practical automated data augmentation with a reduced search space

|tag|
|------|
|ML|
|Data|


[paper](https://arxiv.org/pdf/1909.13719.pdf)  


****




## Figure 1. ResNet-50, EfficientNet-B5 and EfficientNet-B7 에 해당하는 최적 외곡 강도 이미지.  
강도가 증가함에 하면, args의 강도가 증가한다.  



## Figure 2.  
```py
transforms = [
'Identity', 'AutoContrast', 'Equalize',
'Rotate', 'Solarize', 'Color', 'Posterize',
'Contrast', 'Brightness', 'Sharpness',
'ShearX', 'ShearY', 'TranslateX', 'TranslateY']

def randaugment(N, M):
"""Generate a set of distortions.
  Args:
    N: Number of augmentation transformations to
        apply sequentially.
    M: Magnitude for all the transformations.
"""
 sampled_ops = np.random.choice(transforms, N)
 return [(op, M) for op in sampled_ops]
```

N개 만큼의 transform을 랜덤으로 골라 M의 강도로 진행하는 코드이다.  



## Figure 3. 
최적 강도 조사 (model size와 training set)  


CIFAR-10
Wide-ResNet model architectures

그래프 A.  
200epoch와 45K training set로 학습시킨 여러 크기의 Wide-ResNet
model 크기가 크면 왜곡 magnitude 높여야 효과적임.   

그래프 C.  
training set sizes (1K, 4K, and 10K)로 학습시킨 model  
dataset이 크면 왜곡 magnitude 높여야 효과적.  

그래프 B.  
그래프 A의 변형  

그래프 D.   
그래프 C의 변형  



## Figure 4.

transformations의 개수에 따른 성능 조사  
RandAugment (N = 3, M = 4) 로 학습했다.  
transformations이 많을수록 더 높은 정확도 달성



******

다양하게 실험을 한 결과도 paper로 작성할 수 있다