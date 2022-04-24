---
title: "Zasady zachowania w stałym polu magnetycznym"
subtitle: Zabawa z lagranżjanami"
date: 2022-04-24T10:00:00+02:00
draft: false
categories: ["fizyka", "studia"]
tags: ["fizyka", "studia", "elektrodynamika klasyczna"]
---

# Dla lagranżjanu cząstki w stałym polu $\mathbf{B}$, znajdź zasady zachowania

Lagranżjan nierelatywistycznej cząstki o masie $m$ i ładunku $q$ w polu elektromagnetycznym z potencjałem skalarnym $V$ oraz potencjałem wektorowym $\mathbf{A}$ ma postać

$$ L = \frac{m}{2}\dot{\mathbf{x}}^2 + \frac{q}{c} \mathbf{A}\cdot \dot{\mathbf{x}} - qV. $$

Kanoniczny pęd zadany jest wzorem

$$ \mathbf{p} = \frac{\partial L}{\partial \dot{\mathbf{x}}} = m \dot{\mathbf{x}} + \frac{q}{c} \mathbf{A}. $$

Z kolei pochodna po zmiennych $x_i$ to

$$ \frac{\partial L}{\partial x_i} = \frac{q}{c} \frac{\partial \mathbf{A}}{\partial x_i} \cdot \dot{\mathbf{x}} - q \frac{\partial V}{\partial x_i}. $$

Korzystając z równań Eulera-Lagrange'a, otrzymujemy warunek na prawo zachowania

$$ 0 = \frac{d}{dt} \frac{\partial L}{\partial \dot{x}_i} - \frac{\partial L}{\partial x_i} = \frac{d}{dt}\left[\frac{\partial L}{\partial \dot{x}_i} - G_i\right]. $$

W szczególności, w stałej indukcji magnetycznej $B$, możemy przykładowo zadać potencjał wektorowy $\mathbf{A} = \frac{1}{2}\mathbf{B}\times \mathbf{x}$ oraz potencjał skalarny $V = 0$.

Otrzymujemy zatem 

$$\begin{align*}\frac{\partial L}{\partial x_i} &= \frac{q}{c}\sum_k \dot{x}_k \frac{\partial A_k}{\partial x_i}\cr
&= \frac{q}{2c} \sum_k \dot{x}_k \frac{\partial}{\partial x_i} \left( \sum_{lm} \varepsilon_{klm} B_l x_m\right)\cr
&= \frac{q}{2c} \sum_k \dot{x}_k \sum_l \varepsilon_{kli} B_l. \end{align*}$$
Zatem w zapisie wektorowym mamy
$$ \frac{\partial L}{\partial \mathbf{x}} = \frac{q}{c} \dot{\mathbf{x}} \times \mathbf{B} = \frac{d}{dt} \left(\frac{q}{2c}\mathbf{x}\times \mathbf{B}\right) = \frac{d}{dt} \mathbf{G}.$$
Skorzystaliśmy tu z naszego założenia o stałej indukcji magnetycznej. Dzięki tego mogliśmy napisać $\dot{\mathbf{x}}\times \mathbf{B} = d/dt (\mathbf{x} \times \mathbf{B}) $.

Prawo zachowania związane z symetrią translacyjną ma postać
$$\frac{d}{dt}\left(\mathbf{p} - \frac{q}{2c} \mathbf{x}\times \mathbf{B}\right) = 0.$$
