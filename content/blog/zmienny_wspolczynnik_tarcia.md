---
title: "Zmienny współczynnik tarcia"
date: 2020-04-22T15:35:46+02:00
draft: false
categories: ["fizyka", "liceum"]
tags: ["fizyka", "liceum", "dynamika", "praca siły tarcia", "energia"]
---

Mamy klocek o masie $m$ i długości $h$, puszczamy go z prędkością $\mathbf{v_0}$ w prawą stronę. Podłoże po którym będzie sunąć ma współczynnik tarcia opisany funkcją

$$\mu(x) = \begin{cases}
\mu_1, & x \in [0,x_1]\cr
\mu_2, & x \in ]x_1, x_2]\cr
\mu_3, & x > x_2
\end{cases}.$$
Po przebyciu jakiej odległości $x_3 > x_2$ klocek się zatrzyma?

Powiedzmy, że klocek na początku znajduje się w punkcie $x = h/2$.
Jako, że klocek ma tam prędkość o wartości $v_0$, ma w tym układzie odniesienia energię kinetyczną $K_0 = m v_0^2 / 2$.
W momencie styku prawej granicy klocka z przejściem w obszar $x_1$, znajduje się on w punkcie $x = x_1 - h/2$.
Klocek w tym obszarze stracił prędkość na rzecz siły tarcia. Praca wykonana przez siłę tarcia to
$$dW_T = \mathbf{T}\cdot\mathbf{ds}.$$
Można zapisać zasadę zachowania energii
$$K_0 = K_1 + W_T.$$
Dla $x\in X_1 = [h/2, x_1 - h/2]$, $\mu = \mu_1$, więc
$$W_T[X_1] = \int\limits_{h/2}^{x_1-h/2} mg\mu_1 dx = mg\mu_1(x_1 - h).$$
Analogicznie dla $x\in X_2 = [x_1 + h/2, x_2 - h/2]$
$$W_T[X_2] = \int\limits_{x_1 + h/2}^{x_2 - h/2} mg\mu_2 dx = mg\mu_2(x_2 - x_1 - h)$$
oraz dla $x\in X_3 = [x_2 + h/2, x_3]$
$$W_T[X_3] = \int\limits_{x_2 + h/2}^{x_3} mg\mu_3 dx = mg\mu_3(x_3 - x_2 - h/2).$$
Pozostały obszary, gdzie klocek przechodzi między $\mu_i$ i $\mu_{i+1}$.
Wtedy dla $h_a$ - część po przejściu, $h_b$ - część przed przejściem mamy$$\mu(x) = \frac{\mu_i(h_b(x)) + \mu_{i+1}(h_a(x))}{h}.$$
Jako, że $h = h_a + h_b$, to można przepisać $\mu$ jako
$$\mu(h_a) = \frac{\mu_i(h-h_a) + \mu_{i+1} h_a}{h} = h_a\left(\frac{\mu_{i+1}}{h} - \frac{\mu_i}{h}\right) + \mu_i.$$
Teraz można policzyć dla $x \in X_i = [x_i - h/2, x_i + h/2]$
$$W_T[X_i] = \int\limits_0^h mg\mu(h_a)dh_a = \frac{1}{2}mgh(\mu_i+\mu_{i+1}),$$
ewentualnie jako pole trapezu opisanego przez $h_a\in [0,h]$, $\mu = h_a(\mu_{i+1}/h - \mu_i/h)+\mu_i$.

Cała początkowa energia kinetyczna pod koniec przechodzi na sumę wszystkich prac wykonanych przez tarcie:
$$\begin{align*}W = mg\mu_3(x_3 - x_2 - h/2) &= \frac{m}{2}v_0^2 - \frac{1}{2}mgh(\mu_1+\mu_2) - \frac{1}{2}mgh(\mu_2+\mu_3) - \cr
&- mg\mu_1(x_1-h) - mg\mu_2(x_2-x_1-h)\end{align*}$$

W związku z tym klocek zatrzyma się po przebyciu odległości
$$x_3 = \frac{1}{\mu_3}\left(\frac{v_0^2}{2g} - h(\mu_1+\mu_2) - h(\mu_2+\mu_3) - \mu_1(x_1-h) - \mu_2(x_2-x_2-h)\right) + x_2 + h/2$$
