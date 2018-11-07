---
layout: post
title: 로지스틱 리그레션
---
요즘 코세라에서 Deeplearning.ai 강좌를 듣고 있다.

Logistic Regression에서 우리가 관심이 있는 것은 추정 확률을 높히는 것이다.

a를 predict값이라고 볼 때, 확률은 이렇게 볼 수 있다.
<img src="https://latex.codecogs.com/gif.latex?P(y=1 | x)= a " />

<img src="https://latex.codecogs.com/gif.latex?\text { if y = 1 } t P(y | x)= a "/>
<img src="https://latex.codecogs.com/gif.latex?\text { if y = 0 } t P(y | x)= 1-a "/>

이것을 이렇게 축약 가능하다.

<img src="https://latex.codecogs.com/gif.latex?P(y | x)= a^y (1-a)^(1-y) "/>


P(y | x) = a^y * (1-a)^(1-y)

바로 위의 식에서 크로스 엔트로피 형식이 유도된다.
P(y | x)의 값을 최대화 하는 건 log(P(y | x))의 값을 최대화하는 것과 같다.

log(P(x | y)) = log(a^y * (1-a)^(1-y))
log(P(x | y)) = log(a^y) + log((1-a)^(1-y))
log(P(x | y)) = ylog(a) + (1-y)log(1-a) 

여기서 알 수 있는 건, ylog(a) + (1-y)log(1-a)는 Logistic Regression의 Loss fuction의 음수인 값
즉, -L(a, y)라는 것.

log(P(x | y)) = -L(a, y)인데, log(P(x | y))를 최대화 시키는 것이 목적인데, 이는 L(a, y)를 최소화 시키는 것과 같다.

하지만 이건 m개의 데이터 중 단 하나의 값만을 보는 것이다.

P(Overall...) = (Pi)(m, i=1)p(y^i | x^i)

log(P(overall...)) = log((Pi)(m, i=1)P(y^i | x^i))
log(P(overall...)) = log(P(y^1 | x^1) + log(P(y^2 | x^2) + ...
log(P(overall...)) = Sigma(m, i=1)-L(a, y)

J(w, b) = 1/m * Sigma(m, i=1)L(a,y)가 된다.

위의 cost function은 최대화가 아니라 최소화를 하는 게 목적이므로 -L(a, y)의 -를 없애준다. 그리고 편의성과, better scale을 위해서
1/m을 앞에 곱해준다.



