---
title: "The Absurdity of magical properties of 432Hz"
date: 2026-09-21T12:00:00+02:00
draft: true
tags: ["shitpost"]
---

There are numerous websites claiming A=432Hz is somehow magical, that it calms nerves, heals diseases and can make you a higher being.
The same websites then often go on about A=440Hz being some US gov. conspiracy to make the population docile etc.
The fascinating thing about all this crap is that the very basis of these arguments is complete and utter misunderstanding how anything in our physical world works.



## Natural units
Every physicist learns them at some point.
The core idea is that instead of using SI units (or God forbid Imperial) we set as many of our physical constants to $1$ as possible.
For example in Special Relativity you might write things like $t' = \gamma\left(t - vx/c^2\right)$[^1] a lot and after some time you *will* just say $c=1$ and write $t' = \gamma\left(t - vx\right)$.
There are a couple flavours of natural units depending on the area in which they make calculations the simplest.
Today we'll use [Planck units](https://en.wikipedia.org/wiki/Planck_units) because I say so.
Planck units are based on [$G$](https://en.wikipedia.org/wiki/Gravitational_constant), [$\hbar$](https://en.wikipedia.org/wiki/Planck_constant#Reduced_Planck_constant), [$c$](https://en.wikipedia.org/wiki/Speed_of_light) and [$k_B$](https://en.wikipedia.org/wiki/Boltzmann_constant). 

I encourage you to try to figure out how to combine these to get units of:
1. length
2. mass
3. temperature

and calculate something like your height.

In the meantime let me show you how to find frequency (Hz) using these.

$$\begin{align}
1 \text{Hz} &= 1 \text{s}^{-1} \cr
t_P &= \sqrt{\frac{\hbar G}{c^5}} \cr
f_P &= 1/t_P = \sqrt{\frac{c^5}{\hbar G}}
\end{align}$$


## my new magical frequency that at least makes some physical sense

$$\mathcal{f}_\text{much better} = \pi \cdot \phi \cdot 2^{1/\alpha} f_P \approx 541.2\quad Hz$$


[^1]: $\gamma = 1/\sqrt{1-v^2/c^2}$
