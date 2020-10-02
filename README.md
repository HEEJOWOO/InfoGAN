# InfoGAN : https://arxiv.org/abs/1606.03657

#### <I studied while referring to various sites, but it is not enough. Thanks anytime for feedback.>
### <heejo5@naver.com>

Information Maximizing GAN
--------------------------

* 기존 GAN의 문제점
  * 생성 벡터 z의 공간 중에 생성 이미지의 특징이 표현
  * z의 각 차원의 특징을 해석하기 어려움
  * 해석 가능한 표현은 생성 이미지를 확인해서 찾을 수 밖에 없음
  * 지도학습으로는 일부의 특징 밖에 학습시킬 수 없음

* InfoGAN 목적
  * 생성시에 이용가치가 높은 특징량을 비지도학습으로 획득
  * 기존의 GAN계 모델에 비하여 간단하게 특징량을 획득
  * 생성용 벡터를 z와 Latent code c로 분할
  * Latent code c와 생성기 분포 G(z,c)의 상호정보량 I(c;G(z,c))를 극대화
  
* InfoGAN 아이디어
![image](https://user-images.githubusercontent.com/61686244/94900526-1b243b00-04d0-11eb-8f88-64982b4cdae0.png)


* 상호정보량, InfoGAN 목적함수
![image](https://user-images.githubusercontent.com/61686244/94900560-2b3c1a80-04d0-11eb-8610-ba156a66e284.png)

* InfoGAN 목적함수
![image](https://user-images.githubusercontent.com/61686244/94900614-4018ae00-04d0-11eb-8ec5-874e2646eee8.png)
![image](https://user-images.githubusercontent.com/61686244/94900643-4ad34300-04d0-11eb-9d1e-f7b6da4cef8c.png)
![image](https://user-images.githubusercontent.com/61686244/94900678-59215f00-04d0-11eb-813b-20c17420847c.png)

* InfoGAN Architecture
![image](https://user-images.githubusercontent.com/61686244/94900721-6c342f00-04d0-11eb-872b-ba80d8133761.png)

* 결과(MNIST)
![image](https://user-images.githubusercontent.com/61686244/94900761-853ce000-04d0-11eb-9a32-a2da8bdc555a.png)
![image](https://user-images.githubusercontent.com/61686244/94900777-8e2db180-04d0-11eb-917d-df0c7f89085a.png)

* Face dataset & 3D 의자 데이터
![image](https://user-images.githubusercontent.com/61686244/94900807-9e459100-04d0-11eb-9ed0-fc319946c935.png)
![image](https://user-images.githubusercontent.com/61686244/94900839-ad2c4380-04d0-11eb-96f6-bc9bb37e5e98.png)

* CelebA data
![image](https://user-images.githubusercontent.com/61686244/94900890-bfa67d00-04d0-11eb-8da9-1d4ba430599b.png)

Conclusions
-----------
* 생성 벡터 z와 Latent code c의 명시적 분할
* Latent code와 생성 분포의 상호정보량 I를 극대화 하여 종속성 보장
* 다양한 데이터세트에서 획득된 표현과 생성이미지 확인
* 완전히 비지도적이며, 어려운 데이터 세트에 대해서도 해석 가능
* InfoGAN은 GAN에 무시해도 될 수준의 계산 비용만을 더하여 트레이닝 하기 쉬움




  
 
