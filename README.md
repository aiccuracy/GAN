# GAN(Generative Adversarial Network)


* 모델이 dataset과 유사한 이미지를 만들도록 함
* Generator와 Discriminator 라는 두 모델이 적대적인 관계를 이루며 동시에 학습을 진행(minimax game)
* Generator : 실제 데이터 분포를 학습하여 fake 이미지를 생성  
  => fake image를 잘 생성해서 discriminator를 더 감쪽같이 속이는게 목표
* Discriminator : original 데이터인지 Generator로부터 형성된 데이터인지를 구별   
  => image를 제대로 구분하는 게 목표

## CGAN(Conditional Generative Adversarial Network)

* GAN과 거의 동일
* Generator와 Discriminator의 입력값으로 학습시킬 Condition(y)을 넣어주는 것

## DCCAN(Deep Convolutional Generative Adversarial Network)

* 기존의 GAN에 CNN 네트워크를 도입
* Fully-connected layer구조 -> Convolutional layer구조
* Generator와 Discriminator 모두에 batchnorm을 적용
* Generator : 출력을 제외한 layer에 ReLU activation function을 사용
* Discriminator : 모든 layer에 LeakyReLU 사용
