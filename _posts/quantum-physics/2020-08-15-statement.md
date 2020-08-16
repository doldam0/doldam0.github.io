---
layout: post
title:  "[내가 보려고 올리는 양자역학] 입자의 상태 - 기댓값과 표준편차"
author: doldam
categories: [ quantum-physics ]
image: assets/images/math/limit/main.jpg
beforetoc: "파동함수로 입자의 운동을 설명하기 위해서는 입자의 상태를 알아야 하는데, 기댓값을 구하면 입자의 상태를 알 수 있습니다."
toc: true
---

### 기댓값과 표준편차

확률적인 상황을 해석할 때 중요한 요소를 꼽으라고 하면 저는 **기댓값**과 **표준편차**를 꼽을 것입니다. 데이터의 특성을 잘 나타내주기 때문이죠.

먼저 기댓값이 무엇인지부터 알아보겠습니다. 기댓값은 다음과 같이 정의합니다.

$$ \langle x \rangle = \int_{-\infty}^{\infty} x \vert \Psi \vert^2 dx = \int_{-\infty}^{\infty} \Psi^* x \Psi dx $$

기댓값은 평균과 같습니다. 다만 어떤 확률적인 데이터를 추출했을 때 그 데이터가 '평균값이 나오길 기대'하기 때문에 기댓값으로 이름을 붙인 것 같습니다.

표준편차를 알아보기 전에, 먼저 **편차**와 **분산**에 대해 알아보겠습니다. 편차는 특정 데이터에서 기댓값을 뺀 값이고, 분산은 편차의 제곱의 평균입니다. 즉

<> 편차 $$ = \Delta x = x - \langle x \rangle $$

이고

<> 분산 $$ = \sigma^2 = \left\langle \left( \Delta x \right)^2 \right\rangle = \left\langle \left( x - \langle x \rangle \right)^2 \right\rangle $$

입니다.

여기서 분산식을 조금 변형하면

$$ \begin{aligned}
	\sigma^2
	&= \left\langle (x - \langle x \rangle)^2 \right\rangle \\
	&= \left\langle x^2 - 2x \langle x \rangle + \langle x \rangle^2 \right\rangle \\
	&= \left\langle x^2 \right\rangle - \left\langle 2x \langle x \rangle \right\rangle + \left\langle \langle x \rangle^2 \right\rangle \\
	&= \left\langle x^2 \right\rangle - 2 \langle x \rangle \langle x \rangle + \langle x \rangle^2 \\
	&= \left\langle x^2 \right\rangle - 2 \langle x \rangle^2 + \langle x \rangle^2 \\
	&= \left\langle x^2 \right\rangle - \langle x \rangle^2
\end{aligned} $$

이므로 최종적으로 아래 식을 쓸 수 있습니다.

$$ \sigma^2 = \left\langle x^2 \right\rangle - \langle x \rangle^2 $$

표준편차는 분산의 제곱근입니다.

<> 표준편차 $$ = \sigma = \sqrt{\sigma^2} $$

### 위치와 운동량

아제 기댓값과 표준편차를 이용해 입자의 상태를 나타낼 수 있습니다. 예를 들어 어떤 입자의 파동함수가 $$ \Psi $$라면 그 입자의 위치는

$$ \langle x \rangle = \int_{-\infty}^{\infty} \Psi^* x \Psi dx $$

입니다. 여기서 주의해야 할 점은 어떤 입자를 관측했을 때 정확히 그 입자의 위치가 $$ \langle x \rangle $$가 되는 것이 아닌, 이 위치에서 입자를 발견할 확률이 가장 높다는 것을 의미한다는 것입니다.

이제 이를 이용해 운동량을 구해봅시다. 슈뢰딩거 방정식을 구할 때[^1] 입자의 운동량을 이렇게 쓸 수 있다는 것을 알았습니다.

[^1]: 자세한 내용은 여기를 참고해주세요! [1차원 슈뢰딩거 방정식](/schrödinger-equation)

$$ p = \hbar k $$

또한 여기서 $$ k $$는

$$ \frac{\partial \Psi}{\partial x} = ik \Psi $$

$$ \therefore k = -i \frac{1}{\Psi} \frac{\partial \Psi}{\partial x} $$

이므로 따라서

$$ p = -i \hbar \frac{1}{\Psi} \frac{\partial \Psi}{\partial x} $$

입니다. 이제 양변에 $$ \Psi $$를 곱하면

$$ p \Psi = -i \hbar \frac{\partial \Psi}{\partial x} $$

이므로 운동량 $$ \langle p \rangle $$는

$$ \begin{aligned}
	\langle p \rangle 
	&= \int_{-\infty}^{\infty} \Psi^* p \Psi dx \\
	&= \int_{-\infty}^{\infty} \Psi^* \left( -i \hbar \frac{\partial \Psi}{\partial x} \right) dx \\
	&= -i \hbar \int_{-\infty}^{\infty} \Psi^* \frac{\partial \Psi}{\partial x} dx
\end{aligned} $$

가 됩니다.

마찬가지로 위치의 표준편차를 구해보면

$$ \left\langle x^2 \right\rangle = \int_{-\infty}^{\infty} \Psi^* x^2 \Psi dx $$

이고

$$ \sigma_x = \sqrt{\left\langle x^2 \right\rangle - \langle x \rangle^2} $$

입니다. 운동량의 표준편차는 이것을 이용하면 되는데

$$ k^2 = - \frac{1}{\Psi} \frac{\partial^2 \Psi}{\partial x^2} $$

$$ \therefore p^2 = \hbar^2 k^2 = -\hbar^2 \frac{1}{\Psi} \frac{\partial^2 \Psi}{\partial x^2} $$

$$ \therefore p^2 \Psi = -\hbar^2 \frac{\partial^2 \Psi}{\partial x^2} $$

따라서

$$ \left\langle p^2 \right\rangle = \int_{-\infty}^{\infty} \Psi^* p^2 \Psi dx = -\hbar^2 \int_{-\infty}^{\infty} \Psi^* \frac{\partial^2 \Psi}{\partial x^2} dx $$

이고 최종적으로

$$ \sigma_p = \sqrt{\left\langle p^2 \right\rangle - \langle p \rangle^2} $$

입니다.

### 상태 연산자

우리는 앞서

$$ p\Psi = -i\hbar \frac{\partial \Psi}{\partial x} $$

임을 알았습니다. 이를 이용하면 운동량이 포함된 상태들(각운동량이나 운동에너지 등)을 모두 구할 수 있습니다. 하지만 매번 운동량과 관련된 식을 구하기란 쉽지 않은 일입니다. 그래서 더욱 쉽게 상태를 구하기 위해 특별한 연산자를 고안해냅니다.

$$ \hat p = -i\hbar \frac{\partial}{\partial x} $$

이를 **운동량 연산자**라고 부릅니다. 이 운동량 연산자가 정말 유효한지 알아보기 위해 $$ p^2\Psi $$를 구해보겠습니다.

$$ p^2\Psi = {\hat p}^2 \Psi = \left( -i\hbar \frac{\partial}{\partial x} \right)^2 \Psi = i^2 \hbar^2 \frac{\partial^2}{\partial x^2} \Psi = - \hbar^2 \frac{\partial^2 \Psi}{\partial x^2} $$

따라서 운동량 연산자가 잘 작동하는 것을 볼 수가 있습니다.

마찬가지로 **위치 연산자**를 정의하면

$$ \hat x = x $$

입니다. 위치 연산자는 그대로 위치 변수 그 자체를 나타낸다는 것을 볼 수가 있습니다.

이제 이를 응용하면 여러 가지 상태를 구할 수 있습니다. 입자의 운동에너지 $$ \langle T \rangle $$는

$$ \begin{aligned}
	\langle T \rangle 
	&= \left\langle \frac{p^2}{2m} \right\rangle \\
	&= \int_{-\infty}^{\infty} \Psi^* \frac{\hat p^2}{2m} \Psi dx \\
	&= \frac{1}{2m} \int_{-\infty}^{\infty} \Psi^* \hat p^2 \Psi dx \\
	&= \frac{1}{2m} \int_{-\infty}^{\infty} \Psi^* \left( -i\hbar \frac{\partial}{\partial x} \right)^2 \Psi dx \\
	&= -\frac{\hbar^2}{2m} \int_{-\infty}^{\infty} \Psi^* \frac{\partial^2 \Psi}{\partial x^2} dx
\end{aligned} $$

입니다.

### 불확정성 원리

위치와 운동량의 표준편차를 구하는 이유는 많지만, 지금은 그 중 하나인 **불확정성 원리**에 대해 설명하려고 합니다. 불확정성 원리는 하이젠베르크(Heisenberg)가 주장한 원리로써, 다음의 관계가 성립한다는 것입니다.

$$ \sigma_x \sigma_p \ge \frac{\hbar}{2} $$

보통은 표준편차가 아닌 위치와 운동량의 변화($$ \Delta x $$, $$ \Delta p $$)에 관한 식으로 더 잘 알려져있지만, 이 식은 다음 기회에 살펴보는 것으로 하고 지금은 표준편차에 관한 식으로 기억해 주시길 바라겠습니다.
