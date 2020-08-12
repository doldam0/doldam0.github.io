---
layout: post
title:  "[내가 보려고 올리는 양자역학] 슈뢰딩거 방정식"
author: doldam
categories: [ quantum-physics ]
image: assets/images/math/limit/main.jpg
beforetoc: "슈뢰딩거 방정식은 양자 세계에서 일어나는 거의 대부분의 현상을 설명합니다."
toc: true
---

### 광양자설

아인슈타인(Albert Einstein)은 끝까지 양자역학을 거부한 사람 중 한명으로 잘 알려져 있습니다. 하지만 아이러니하게도, 양자역학의 포문을 연 것은 아인슈타인의 **광양자설**(light quantum theory)이었죠. 

아인슈타인의 광양자설은 쉽게 말해서, *빛이 입자일 수 있다는 것* 입니다. 빛이 입자이지 않으면, 즉 빛이 파동이라면 설명할 수 없는 현상을 아인슈타인이 발견했기 때문이죠.

아인슈타인은 금속판에 일정 주파수 이상의 빛을 쏘았을 때 금속판에 있던 전자가 튀어나오는 현상을 발견하게 되는데, 이를 **광전 효과**(photoelectric effect)라고 합니다. 그런데 튀어나온 전자의 에너지가 매우 특이했습니다. 기존의 과학자들은 빛이 파동이고, 빛의 세기가 전자의 에너지를 결정한다고 생각했었습니다. 하지만 튀어나온 전자가 가지는 에너지는 빛의 세기가 아닌 *빛 알갱이* 개수에 비례했습니다. 실험 결과가 보여준 것은 전자의 에너지가 빛 알갱이의 개수와 빛의 주파수에 비례한다는 것이었습니다.

$$ E \propto nf $$

그리고 이 식의 비례상수를 $$ h $$로 놓으면 다음과 같은 식이 됩니다.

$$ E = nhf $$

여기서 상수 $$ h $$는 플랑크 상수로, 그 값은 약 $$ \mathrm {6.626 × 10^{-34} m^2 kg / s} $$ 입니다. 따라서 빛 알갱이 하나에 해당하는 에너지는

$$ E = hf $$

입니다. 이로써 아인슈타인은 빛이 파동이 아니라 입자일 수 있다는 가설을 내놓게 됩니다. 또한 여기서 말한 빛 알갱이를 **광자**(photon)라고 부르기로 했습니다. 

### 물질파 이론

이후 드 브로이(de Broglie)라는 물리학자는 엑스선의 파동성(회절)과 입자성(광전 효과)을 모두 관찰하면서 **빛은 파동성과 입자성을 동시에 가진다**라고 결론짓습니다. 여기에 한술 더 떠, 드 브로이는 **모든 입자는 파동성과 입자성을 동시에 가진다**라고 말합니다. 그리고 입자의 파장을 다음과 같이 계산합니다.

아인슈타인의 특수상대성이론

$$ E^2 = (mc^2)^2 + (pc)^2 $$

에서 질량과 관련된 항 $$ (mc^2)^2 $$을 무시하면

$$ E^2 = (pc)^2 \quad \therefore E = pc $$

가 됩니다. 여기에 앞서 소개했던 광전 효과

$$ E = hf $$

를 대입하면

$$ hf = pc $$

입니다. 양변을 $$ fp $$로 나누면

$$ \frac{h}{p} = \frac{c}{f} $$

이고, 따라서

$$ \lambda = \frac{c}{f} = \frac{h}{p} $$

가 됩니다. 결론적으로 드 브로이 식은

$$ \lambda = \frac{h}{p} $$

가 됩니다. 이를 **물질파 이론**(matter wave theory)이라고 합니다.

이제 양자역학의 시작을 알린 두 식을 모두 알아보았습니다.

$$ E = hf $$

$$ \lambda = \frac{h}{p} $$

### 슈뢰딩거 방정식

이 두 식을 이용해 슈뢰딩거(Erwin Schrödinger)는 양자 세계의 현상을 너무나도 잘 설명하는 방정식인 **슈뢰딩거 방정식**(Schrödingers equation)을 만들게 됩니다.

먼저 위 두식을 

$$ \hbar = \frac{h}{2 \pi} $$

와

$$ f = \frac{\omega}{2 \pi} $$

$$ \lambda = \frac{2 \pi}{k} $$

를 이용해 정리하면 다음과 같이 쓸 수 있습니다.

$$ E = \frac{h \omega}{2 \pi} = \hbar \omega $$

$$ p = \frac{h}{\lambda} = \frac{hk}{2 \pi} = \hbar k $$

또한 에너지에 관한 고전역학적 식

$$ E = \frac{p^2}{2m} + V $$

에 이를 대입하면

$$ \hbar \omega = \frac{\hbar^2}{2m} k^2 + V $$

입니다.

파동성을 띄는 입자의 파동 함수를 다음과 같이 정의했을 때,

$$ \Psi = Ae^{i(kx - \omega t)} $$

양변을 $$ x $$에 대해 미분하면

$$ \frac{\partial \Psi}{\partial x} = ik Ae^{i(kx - \omega t)} = ik \Psi $$

가 되는 것을 알 수 있습니다. 여기서 한번 더 미분하면

$$ \frac{\partial^2 \Psi}{\partial x^2} = \frac{\partial}{\partial x} \left( \frac{\partial \Psi}{\partial x} \right) = \frac{\partial}{\partial x}ik \Psi = ik \frac{\partial \Psi}{\partial x} = ik(ik \Psi) = i^2 k^2 \Psi = -k^2 \Psi $$

입니다. 또한 양변에 $$ t $$를 미분한 결과는

$$ \frac{\partial \Psi}{\partial t} = -i \omega Ae^{i(kx - \omega t)} = -i \omega \Psi $$

입니다. 이를 에너지에 관한 고전역학적 식에 각각 대입하면

$$ k^2 = - \frac{1}{\Psi} \frac{\partial^2 \Psi}{\partial x^2} $$

$$ \omega = - \frac{1}{i} \frac{1}{\Psi} \frac{\partial \Psi}{\partial x} = i \frac{1}{\Psi} \frac{\partial \Psi}{\partial t} $$

$$ \therefore i \hbar \frac{1}{\Psi} \frac{\partial \Psi}{\partial t} = - \frac{\hbar^2}{2m} \frac{1}{\Psi} \frac{\partial^2 \Psi}{\partial x^2} + V $$

이제 양변에 $$ \Psi $$를 곱하면

$$ i \hbar \frac{\partial \Psi}{\partial t} = - \frac{\hbar^2}{2m} \frac{\partial^2 \Psi}{\partial x^2} + V \Psi $$

입니다. 이로써 슈뢰딩거 방정식이 완성되었습니다!
