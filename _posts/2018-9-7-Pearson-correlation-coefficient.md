---
layout: post
title: 머신 러닝과 공식
---
Pearson correlation coefficient

머신 러닝을 공부하다가 보니, 여러 Feature들 중 무엇을 Input으로 넣어야하나 그 기준에 대해 궁금해 본 적이 있었다.

배운 내용으로는 상관 계수가 높은 것을 취하는 것이 좋다고 하고 그 상관 계수를 구하는 방법 중 하나를 '피어슨의 상관계수'로 들었다.

![Alt text](https://IronSpirit.github.io/images/PccIMG_1.svg)

즉 인풋과 아웃풋을 공분산 한것을 각각의 표준 편차로 나눈 값이다. 

결과 중에서 음이든 양이든 계수가 높은 것을 채택하면 된다.


Likelihood와 Probability의 차이

Probability는 모델 파라미터가 주어지고, 관찰값을 참조할 수 없을 때, 임의의 결과의 그럴듯함을 계산한 값이고
Likelihood는 특정 관찰된 값이 있을 때, 모델 파라미터의 그럴듯함을 구하는 것이다. 

