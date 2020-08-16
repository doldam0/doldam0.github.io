---
layout: post
title:  "[내가 보려고 올리는 양자역학] Griffith 양자역학 3판 Chapter 1 연습문제 풀이"
author: doldam
categories: [ quantum-physics ]
image: assets/images/math/limit/main.jpg
beforetoc: "David Griffith 저 양자역학 3판 Chapter 1 연습문제 풀이"
toc: true
---

지금부터 David Griffith 저 양자역학 3판 Chapter 1의 연습문제를 풀어보겠습니다. 다만 문제 1.1과 문제 1.2는 이산확률의 기댓값과 표준편차에 관한 것이어서 넘어가겠습니다.

###### 문제 1.3

Gauss 분포

$$ \rho (x) = Ae^{-\lambda (x - a)^2} $$

가 있다. 여기서 $$ A $$, $$ a $$, $$ \lambda $$는 양의 실수이다.

(a) 규격화를 통해 $$ A $$를 구하라.

(b) $$ \langle x \rangle $$, $$ \left\langle x^2 \right\rangle $$, $$ \sigma $$를 구하라.

+++

(a)

먼저 확률밀도함수 $$ \rho (x) $$를 규격화해 보겠습니다. 확률의 전체 합이 $$ 1 $$이라는 것을 이용해

$$ \int_{-\infty}^{\infty} \rho (x) dx = 1 $$

$$ A $$를 구하면

$$ \begin{aligned}
	\int_{-\infty}^{\infty} \rho (x) dx 
	&= \int_{-\infty}^{\infty} Ae^{-\lambda(x - a)^2} dx \\
	&= A \int_{-\infty}^{\infty} e^{-\lambda (x - a)^2} dx \\
	&= A \int_{-\infty}^{\infty} e^{-(\sqrt{\lambda}x - \sqrt{\lambda}a)^2} dx \\
	&= \frac{A}{\sqrt{\lambda}} \int_{-\infty}^{\infty} e^{-u^2} du \\
	&\qquad \left( u \equiv \sqrt{\lambda}x - \sqrt{\lambda}a \Rightarrow du = \sqrt{\lambda}dx \quad \therefore dx = \frac{du}{\sqrt{\lambda}} \right) \\
	&= \frac{A}{\sqrt{\lambda}} \sqrt{\pi} \quad \left( \because \int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi} \right) \\
	&= 1
\end{aligned} $$

$$ \therefore A = \frac{\sqrt{\lambda}}{\sqrt{\pi}} = \sqrt{\frac{\lambda}{\pi}} $$

$$ e^{-x^2} $$꼴 함수의 적분 과정은 이 문제에서 치환적분을 통해 보여드렸습니다. 앞으로는 치환적분 과정을 생략하겠습니다.

(b)

$$ \begin{aligned}
	\langle x \rangle 
	&= \int_{-\infty}^{\infty} x \rho (x) dx \\
	&= \int_{-\infty}^{\infty} xAe^{-\lambda(x - a)^2} dx \\
	&= A \int_{-\infty}^{\infty} xe^{-\lambda (x - a)^2} dx \\
	&= \underbrace{A \int_{-\infty}^{\infty} (x - a)e^{-\lambda (x - a)^2} dx}_{\text{odd function}} + A \int_{-\infty}^{\infty} ae^{-\lambda (x - a)^2} \\
	&= Aa \int_{-\infty}^{\infty} e^{-\lambda (x - a)^2} \\
	&= Aa\frac{1}{\sqrt{\lambda}} \sqrt{\pi} \\
	&= \sqrt{\frac{\lambda}{\pi}} a\frac{1}{\sqrt{\lambda}} \sqrt{\pi} \\
	&= a
\end{aligned} $$

$$ \therefore \langle x \rangle = a $$

$$ \begin{aligned}
	\left\langle x^2 \right\rangle
	&= \int_{-\infty}^{\infty} x^2 \rho (x) dx \\
	&= \int_{-\infty}^{\infty} x^2 Ae^{-\lambda(x - a)^2} dx \\
	&= A \int_{-\infty}^{\infty} (x - a)^2e^{-\lambda (x - a)^2} dx + \underbrace{2A \int_{-\infty}^{\infty} 2a(x - a)e^{-\lambda (x - a)^2} dx}_{\text{odd function}} + A \int_{-\infty}^{\infty} a^2e^{-\lambda (x - a)^2} dx \\
	&= \frac{A}{\lambda} \int_{-\infty}^{\infty} \lambda(x - a)^2e^{-\lambda (x - a)^2} dx - A \int_{-\infty}^{\infty} a^2e^{-\lambda (x - a)^2} dx \\
	&= \frac{A}{\lambda} \frac{1}{\sqrt{\lambda}} \frac{\sqrt{\pi}}{2} + Aa^2\frac{1}{\sqrt{\lambda}}\sqrt{\pi} \quad \left( \because \int_{-\infty}^{\infty} x^2e^{-x^2} dx = \frac{\sqrt{\pi}}{2} \right) \\
	&= \frac{1}{2 \lambda} + a^2
\end{aligned} $$

$$ \therefore \left\langle x^2 \right\rangle = \frac{1}{2 \lambda} + a^2 $$

$$ \therefore \sigma = \sqrt{\left\langle x^2 \right\rangle - \langle x \rangle^2} = \sqrt{\frac{1}{2 \lambda}} $$

+++
