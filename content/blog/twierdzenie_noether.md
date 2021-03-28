---
title: "Twierdzenie Noether"
date: 2021-03-11T14:41:30+01:00
draft: true
---

Twierdzenie Noether pozwala połączyć istnienie symetrii w systemach fizycznych z odpowiednimi prawami zachowania.

Potrzebujemy najpierw zalegalizować terminy "symetria" oraz "prawo zachowania".

# Prawo zachowania

Zasada najmniejszego działania mówi, że dla funkcjonału działania zdefiniowanego przez
$$S[x\^i(t)] = \int\limits_C \mathcal{L} (x\^i, \dot{x}\^i, t)dt$$
zachodzi $\delta S = 0$. Trajektorie $x\^i(t)$, które tę zależność spełniają są rozwiązaniami równań Eulera-Lagrange'a
$$x\^i(t): \left(\partial\_{x\^i} - \frac{d}{dt} \partial\_{\dot{x}\^i} \right)\mathcal{L} = 0.$$

Jeżeli pewna wartość $f(x\^i(t), \dot{x}\^i(t), \dots)$ spełnia warunek
$$\left.\dot{f}\right|\_{x\^i(t)} = 0,$$
to mówimy, że jest ona zachowana wzdłuż trajektorii $x\^i(t).$

# Symetrie

Symetrią nazywamy transformacje
$$x\^i(t) \to \lambda\^i(x\^j(t), t),$$
takie, że
$$\forall x\^i(t)\quad S[x\^i(t)] = S[\lambda\^i(x\^j(t), t)].$$

W szczególności dla
$$x\^i \to x\^{'i} = x\^i + \varepsilon\^i(x),$$
$$\delta x\^i = x\^{'i} - x\^i = \varepsilon\^i(x)$$
zachodzi
$$\forall x\^i(t)\quad \delta\_\varepsilon S = S[x\^i + \varepsilon\^i(x)] - S[x\^i] = 0.$$

# Twierdzenie Noether

Niech akcja ma symetrię w
$$\delta x\^i = x\^{'i} - x\^i = \varepsilon\^i(x).$$
Wtedy funkcja
$$I = \frac{\mathcal{L}(x\^i(\lambda))}{\partial \dot{x}^i} \varepsilon\^i(x)$$
jest zachowana.

# Dowód

$$\begin{align*} 0 &\equiv \delta\_\varepsilon S[x\^i(t)] \equiv\cr
&\equiv \sum\_{i = 1}\^N \int\limits\_{t\_1}\^{t\_2} \left( \frac{\partial \mathcal{L}(x\^i(t))}{\partial x\^i(t)}\varepsilon\^i(x) + \left(\frac{\partial \mathcal{L}(\dot{x}\^i(t))}{\partial x\^i(t)}\right)\frac{d \varepsilon\^i(x)}{dt}\right)dt\end{align*}$$

