# Fully Convolutional Networks for Semantic Segmentation

## 8 Mar 2015

[paper](https://arxiv.org/abs/1411.4038)  


end to end, pixels to pixels 로 학습됨  

semantic segmentation에서 state of the art   
추론은 일반적인 이미지에서 1/5초 이내에 완료  

fcn network로 classification networks(AlexNet, VGG net, GoogleLeNet) 채택, fine tuning된 network를 segmentation task에 전이시킴.  

깊은 layer와 앝은 layer를 결합해 detail한 segmentations 작업 수행  

*****

classification networks를 segmentation 으로 확장, multi-resolution layer 결합으로 architecture 개선  

학습과 추론을 단순화하고 속도를 높임

