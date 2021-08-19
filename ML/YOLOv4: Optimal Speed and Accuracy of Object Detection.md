
# YOLOv4: Optimal Speed and Accuracy of Object Detection

|tag|
|------|
|ML|
|Vision|
|Detection|

## 23 Apr 2020

[paper](https://arxiv.org/pdf/2004.10934.pdf)  


빠르고 정확한 detecter, YOLO v4 는 Conv Net을 향상시키는 수많은 방법들을 검증해본다. 

WRC, CSP, CmBN, SAT, Mish activation, Mosaic data augmentation, CmBN, DropBlck regularization, and CIoU loss 과 같은 기능들을 조합해 coco dataset에서 43.5% AP 달성

또한 3개의 다른 아키텍쳐 GPU에서도 test해보았음 (Maxwell/Pascal/Volta)  

이러한 실험들은 향후 연구와 개발에 많은 도움이 될 수 있음  

*****

AP가 뭔지 조사해야겠다.  
앞선 버전의 YOLO paper를 읽어보고 darknet을 사용해봐야겠다.  