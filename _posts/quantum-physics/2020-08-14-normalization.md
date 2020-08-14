---
layout: post
title:  "[내가 보려고 올리는 양자역학] 파동함수의 규격화"
author: doldam
categories: [ quantum-physics ]
image: assets/images/math/limit/main.jpg
beforetoc: "'슈뢰딩거 방정식의 해는 입자의 발견 확률이다' 라는 해석은 획기적인 발상이었습니다."
toc: true
---

### 파동방정식의 확률적 해석

일반적으로 슈뢰딩거 방정식을 풀면 그 해는 복소함수가 나옵니다. 따라서 이 해를 실세계에 적용하기가 굉장히 힘들었죠.

그래서 슈뢰딩거는 이 해를 실수값으로 만들기 위해 켤레복소수를 곱한 값을 생각합니다. 즉

$$ \Psi^* \Psi = \vert \Psi \vert^2 $$

를 생각한 것이죠. 이는 실수값이므로 실세계에 쉽게 적용할 수 있습니다.

처음 슈뢰딩거는 이 값을 **전하밀도**로 생각했습니다. 이 값이 큰 공간에서는 전하의 밀도가 크고, 이 값이 작은 공간에서는 전하의 밀도가 작은 것이죠.

그런데 막스 보른(Max Born)은 이 값을 **확률밀도**로 해석합니다. 정확히는 입자의 발견 확률 밀도입니다. 이 값이 큰 공간에서는 입자를 발견할 확률이 높고, 이 값이 작은 공간에서는 입자를 발견할 확률이 낮다는 것입니다.

<> $$ \vert \Psi \vert^2 = $$ 입자의 발견 확률밀도

이 주장을 들은 슈뢰딩거와 아인슈타인은 격하게 반대합니다. 심지어 아인슈타인은 이러한 말을 남겼죠.

<> *"신은 주사위놀음을 하지 않는다"*

하지만 오늘날에는 이러한 주장이 거의 정설로 받아들여 쓰이고 있습니다.

### 파동함수의 규격화

우리는 앞서 파동함수에 켤레복소수를 곱한, 즉 절댓값의 제곱값이 확률밀도라는 것을 알았습니다. 그러나 이 함수가 완벽한 확률밀도가 되려면 조건이 있습니다. 확률밀도 함수를 $$ \rho (x) $$라고 했을 때, 확률은 모두 더하면 $$ 1 $$이 되므로 다음과 같은 조건이 성립해야 합니다.

$$ \int_{-\infty}^{\infty} \rho(x) dx = 1 $$

따라서 다음 역시 성립해야 합니다.

$$ \int_{-\infty}^{\infty} \vert \Psi \vert^2 dx = \int_{-\infty}^{\infty} \Psi^*\Psi dx = 1 $$

이를 만족하도록 파동함수를 설정하는 것을 파동함수의 **규격화**(normalization)라고 합니다.

### 파동함수의 규격화에 관한 성질

파동함수는 아래와 같이

$$ \Psi = Ae^{i(kx - \omega t)} $$

$$ x $$와 $$ t $$의 함수이기 때문에 모든 $$ t $$에 대해 파동함수를 규격화해야 합니다. 하지만 사실, 그럴 필요가 없습니다!

만약 이 파동함수가 $$ t = t_0 $$에서 규격화되어 있다고 가정했을 때,

$$ \int_{-\infty}^{\infty} \vert \Psi(x,\ t_0) \vert^2 dx = 1 $$

이 값의 $$ t $$에 대한 변화량을 구해봅시다.

먼저 $$ \partial \Psi / \partial t $$와 $$ \partial \Psi^* / \partial t $$를 구해봅시다.

$$ i\hbar \frac{\partial \Psi}{\partial t} = -\frac{\hbar^2}{2m}\frac{\partial^2 \Psi}{\partial x^2} + V\Psi $$

$$ \therefore \frac{\partial \Psi}{\partial t} = \frac{i \hbar}{2m}\frac{\partial^2 \Psi}{\partial x^2} - \frac{i}{\hbar} V\Psi $$

양변에 켤레를 취하면

$$ \frac{\partial \Psi^*}{\partial t} = -\frac{i \hbar}{2m}\frac{\partial^2 \Psi^*}{\partial x^2} + \frac{i}{\hbar} V\Psi^* $$

따라서

$$ \begin{aligned}
	&\frac{d}{dt} \int_{-\infty}^{\infty} \vert \Psi \vert^2 dx \\
	&= \frac{d}{dt} \int_{-\infty}^{\infty} \Psi^* \Psi dx \\
	&= \int_{-\infty}^{\infty} \frac{\partial}{\partial t} \Psi^* \Psi dx \\
	&= \int_{-\infty}^{\infty} \left( \frac{\partial \Psi^*}{\partial t} \Psi + \Psi^* \frac{\partial \Psi}{\partial t} \right) dx \\
	&= \int_{-\infty}^{\infty} \left[ \left( -\frac{i \hbar}{2m}\frac{\partial^2 \Psi^*}{\partial x^2} + \frac{i}{\hbar} V\Psi^* \right) \Psi + \Psi^* \left( \frac{i \hbar}{2m}\frac{\partial^2 \Psi}{\partial x^2} - \frac{i}{\hbar} V\Psi \right) \right] dx \\
	&= \int_{-\infty}^{\infty} \left( -\frac{i \hbar}{2m}\frac{\partial^2 \Psi^*}{\partial x^2}\Psi + \frac{i}{\hbar} V\Psi^*\Psi + \frac{i \hbar}{2m}\Psi^*\frac{\partial^2 \Psi}{\partial x^2} - \frac{i}{\hbar} V\Psi^*\Psi \right) dx \\
	&= \int_{-\infty}^{\infty} \left( -\frac{i \hbar}{2m}\frac{\partial^2 \Psi^*}{\partial x^2}\Psi + \frac{i \hbar}{2m}\Psi^*\frac{\partial^2 \Psi}{\partial x^2} \right) dx \\
	&= \frac{i\hbar}{2m} \left( \int_{-\infty}^{\infty} \Psi^*\frac{\partial^2 \Psi}{\partial x^2} dx - \int_{-\infty}^{\infty} \frac{\partial^2 \Psi^*}{\partial x^2} \Psi dx \right)
\end{aligned} $$

여기서 부분적분법을 사용합니다.

$$ \int_a^b fg' dx = \left[ fg \right]_a^b - \int_a^b f'g dx $$

그러면

$$ \begin{aligned}
	&\frac{d}{dt} \int_{-\infty}^{\infty} \vert \Psi \vert^2 dx \\
	&= \frac{i\hbar}{2m} \left( \int_{-\infty}^{\infty} \Psi^*\frac{\partial^2 \Psi}{\partial x^2} dx - \int_{-\infty}^{\infty} \frac{\partial^2 \Psi^*}{\partial x^2} \Psi dx \right) \\
	&= \frac{i\hbar}{2m} \left( \left[ \Psi^*\frac{\partial \Psi}{\partial x} \right]_{-\infty}^{\infty} - \int_{-\infty}^{\infty} \frac{\partial \Psi^*}{\partial x} \frac{\partial \Psi}{\partial x} dx - \left[ \frac{\partial \Psi^*}{\partial x} \Psi \right]_{-\infty}^{\infty} + \int_{-\infty}^{\infty} \frac{\partial \Psi^*}{\partial x} \frac{\partial \Psi}{\partial x} dx \right) \\
	&= \frac{i\hbar}{2m} \left( \left[ \Psi^*\frac{\partial \Psi}{\partial x} \right]_{-\infty}^{\infty} - \left[ \frac{\partial \Psi^*}{\partial x} \Psi \right]_{-\infty}^{\infty} \right)
\end{aligned} $$

그런데

$$ \int_{-\infty}^{\infty} \vert \Psi \vert^2 dx $$

가 수렴하려면

$$ \left[ \frac{\partial \Psi}{\partial x} \right]_{x = \infty} \neq 0 $$

이고

$$ \left[ \frac{\partial \Psi}{\partial x} \right]_{x = -\infty} \neq 0 $$

이어야 합니다. 따라서

$$ \begin{aligned}
	&\frac{d}{dt} \int_{-\infty}^{\infty} \vert \Psi \vert^2 dx \\
	&= \frac{i\hbar}{2m} \left( \left[ \Psi^*\frac{\partial \Psi}{\partial x} \right]_{-\infty}^{\infty} - \left[ \frac{\partial \Psi^*}{\partial x} \Psi \right]_{-\infty}^{\infty} \right) \\
	&= 0
\end{aligned} $$

입니다. 결국 

$$ \frac{d}{dt} \int_{-\infty}^{\infty} \vert \Psi \vert^2 dx = 0 $$

이고

$$ \int_{-\infty}^{\infty} \vert \Psi(x,\ t_0) \vert^2 dx = 1 $$

이었으므로 모든 $$ t $$에 대해서

$$ \int_{-\infty}^{\infty} \vert \Psi \vert^2 dx = 1 $$

일 수밖에 없습니다.

결론을 말하자면, 특정 $$ t = t_0 $$에 대해 규격화를 시킨 파동함수는 언제나 규격화되어 있습니다.
