# Clean-Label Backdoor Attacks on Video Recognition Models


## 16 Jun 2020

[paper](https://arxiv.org/pdf/2003.03030.pdf)  

video에서 효과적인 backdoor attack 방법인 universal adversaril trigger를 제시한다.

fixed static trigger와 비교했을떄 좋은 성늘을 보인다.

image backdoor attack은 video에서 효과적이지 않은 이유
1. 입력이 큼
2. 차원이 큼
3. class가 많고 class 당 example이 적음 (sparse dataset)
4. attacks with access to correct labels ? (무슨 소린지 잘 모르겠음)

attack pipeline을 보면 trigger도 생성하고  Adversarial Perturbation으로 조작되기 쉬운 video를 만든다.  

*****

전에도 backdoor attack paper를 읽었는데 한번 구현해봐야겠다.