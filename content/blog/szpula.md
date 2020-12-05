---
title: "Zadanie ze szpulą"
date: 2020-04-11T21:26:31+02:00
draft: false
tags: ["fizyka", "liceum", "szpula", "nić", "kinematyka"]
---

# Problem
Mamy nieruchomą szpulę (walec) o promieniu $r$, na którą nawinięto $k$ zwojów bardzo cienkiej nici. Końcówce nici nadano prędkość $\mathbf{v_0}$ skierowaną radialnie od środka szpuli.

Po jakim czasie nić zdąży się rozwinąć i spowrotem zawinąć na szpulę?

# Rozwiązanie

![Schemat wizualizujący zadanie](/img/szpula.png)

Rozważymy problem w czasie $T = t$ oraz $T = t + \Delta t$.

- $T = t:$\
Punkt styku przesunął się od początku o $r \varphi(t)$ i tyle też wynosi długość rozwiniętej nici.

- $T = t + \Delta t$:\
Punkt styku przesunął się od początku o $r \varphi(t+\Delta t)$, z punktem styku w czasie $T = t$ tworzy kąt $\varphi(t+\Delta t) - \varphi(t)$.

Droga $\xi$, którą przebył w czasie $\Delta t$ koniec nici wynosi
$$\xi(t) = r\frac{\varphi(t) + \varphi(t+\Delta t)}{2}\left(\varphi(t+\Delta t) - \varphi(t)\right).$$
Zamiast średniej można tu było wziąć w zasadzie równie dobrze $\varphi(t)$ lub $\varphi(t+\Delta t)$. Zauważmy jeszcze, że $\varphi(t+\Delta t) - \varphi(t) \equiv \Delta \varphi(t)$. Z drugiej strony, wartość prędkości końca nici jest stała, więc można zapisać
$$\xi(t) = |\mathbf{v}| \Delta t,$$ gdzie $|\mathbf{v}| = |\mathbf{v_0}|$.

Można zatem napisać
$$v_0 \Delta t = r\frac{\varphi(t) + \varphi(t+\Delta t)}{2}\Delta \varphi(t).$$
Przejdźmy z $\Delta t \to dt$ i scałkujmy obustronnie
$$v_0 \int\limits_0^{T_1} dt = r \int\limits_0^{2\pi k}\varphi d\varphi.$$
Górna granica prawej strony to łączny kąt o który musi się przesunąć punkt styku, aby nić się rozwinęła (i była styczna do punktu styku). Otrzymujemy
$$T_1 = \frac{2\pi^2 k^2r}{v_0}.$$
Czas potrzebny na obrócenie się nici w okół punktu styku (teraz punktu zawieszenia) wynosi
$$T_2 = \pi \frac{r}{v_0}.$$
Pozostaje zauważyć, że od tego momentu, $T_3 = T_1$. W związku z tym, łączny czas wynosi
$$T = T_1 + T_2 + T_3 = \frac{4\pi^2k^2r + \pi r}{v_0}.$$
