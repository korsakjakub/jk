---
title: "Równanie Ciołkowskiego"
date: 2020-05-08T10:48:05+02:00
draft: false
categories: ["fizyka", "studia"]
tags: ["fizyka", "studia", "rakieta", "równanie Ciołkowskiego", "dynamika", "mechanika Lagrange", "Tsiolkovsky's equation", "lagranżjan rakiety"]
---
Równanie Ciołkowskiego opisuje wyidealizowany, jednowymiarowy ruch rakiety. Jako równanie form różniczkowych ma niezwykle prostą postać
$$dv = -udm,$$
gdzie
* $v(t)$ - prędkość rakiety,
* $u$ - prędkość wyrzucanego paliwa w układzie związanym z rakietą,
* $m(t)$ - masa rakiety.

Zazwyczaj wyprowadza się je korzystając z zasady zachowania pędu, dzisiaj problem rozważymy od strony mechaniki Langrange.
# Problem
Mamy rakietę o masie $m(t_0) = m_0$ i prędkości $v(t_0) = v_0$, która wyrzuca paliwo w sposób ciągły i jednostajny, z prędkością **względem rakiety** $u$.
* Jak wygląda równanie ruchu rakiety?
* Jakie to równanie ma rozwiązanie?

# Rozwiązanie
Jeżeli rozpatrywany ruch jest wzdłuż $\xi$ oraz rakieta znajduje się w potencjale zależnym od $\xi(t)$, funkcja lagrange tego układu ma postać
$$\mathcal{L} = \frac{1}{2}m(t)\dot{\xi}(t)^2 - \frac{1}{2}\int\limits_0^t \dot{m}(\tau) \left(\dot{\xi}(\tau) - u\right)^2 d\tau - V(\xi(t), t).$$
Składnik zawierający całkę po czasie jest energią kinetyczną związaną z **łączną** masą wyrzuconą od czasu $\tau = 0$, do $\tau = t.$
Jeżeli rozpatrzymy podział przedziału
$$[0,t] = [0,t_1]\cup [t_1, t_2] \cup \dots \cup [t_n, t],$$
w jakimś przedziale $[t_{j-1}, t_{j}]$, rakieta ma prędkość średnią
$$\left< \dot{\xi} \right>_j = \frac{\xi(t_j) - \xi(t_{j-1}))}{t_j - t_{j-1}}$$
oraz wyrzuca paliwo ze średnią szybkością wyrzucania
$$\left< \dot{m} \right>_j = \frac{m(t_j) - m(t_{j-1}))}{t_j - t_{j-1}}.$$
Masa tego paliwa wynosi zatem $\left<m\right>_j = \left<\dot{m}\right>_j (t_j - t_{j-1}) \equiv \left< \dot{m} \right>_j \Delta t_j.$
Więc średnia energia kinetyczna na tym przedziale wynosi
$$\left< T \text{ }\right>_j = \frac{1}{2} \left<\dot{m}\right>_j \left( \left<\dot{\xi}\right>_j - u\right)^2 \Delta t_j.$$
Suma energii kinetycznych odpowiadających składowym podziału przedziału ma postać
$$\left< T \text{ } \right> = \frac{1}{2} \sum_{j = 1}^n \left<\dot{m}\right>_j \left( \left<\dot{\xi}\right>_j - u\right)^2 \Delta t_j.$$
W granicy $n\to \infty$, suma przechodzi w całkę pojawiającą się w funkcji Lagrange.

Mając lagranżjan, możemy już bez przeszkód skorzystać z równania Eulera - Lagrange
$$\frac{d}{dt} \frac{\partial \mathcal{L}}{\partial \dot{\xi}} = \frac{\partial \mathcal{L}}{\partial \xi}.$$
Prawa strona odpowiada sile pochodzącej od potencjału $V$,
$$\frac{\partial \mathcal{L}}{\partial \xi} = \frac{\partial V}{\partial \xi} = F.$$
To jeszcze lewa strona
$$\begin{align*} \frac{d}{dt} \frac{\partial \mathcal{L}}{\partial \dot{\xi}} &= \frac{d}{dt}\left( \frac{\partial}{\partial \dot{\xi}}\frac{1}{2}m\dot{\xi}^2 - \frac{\partial}{\partial \dot{\xi}}\frac{1}{2}\int\limits_0^t \dot{m} \left(\dot{\xi} - u\right)^2 d\tau  \right) = \cr
&= \frac{d}{dt} \left( m \dot{\xi} - \frac{1}{2}\int\limits_0^t \dot{m} \cdot 2 \left(\dot{\xi} - u\right) d\tau \right) = \cr
&= \dot{m}\dot{\xi} + m \ddot{\xi} - \dot{m}\left(\dot{\xi} - u\right) .\end{align*}$$
Po przyrównaniu lewej i prawej strony dostaniemy
$$F = m\ddot{\xi} + \dot{m} u.$$
Jest to równanie Ciołkowskiego z dodatkiem siły $F$.
Po podzieleniu obustronnie przez $m$, położeniu $F =0$ oraz wycałkowaniu po czasie dostaniemy
$$\Delta \dot{\xi} + u\int\limits_0^t \frac{1}{m} \frac{dm}{d\tau} d\tau = 0.$$
Z twierdzenia o zamianie zmiennych całkowania otrzymujemy
$$\Delta \dot{\xi} = -u \int\limits_{m_0}^{m}\frac{dm}{m} = u \ln\left(\frac{m_0}{m}\right).$$
Skoro $\dot{\xi} \equiv v$ oraz $v(0) = v_0$, ostatecznie mamy
$$v(m) = u \ln \left(\frac{m_0}{m}\right) + v_0.$$
