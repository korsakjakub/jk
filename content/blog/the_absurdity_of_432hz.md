---
title: "The Absurdity of magical properties of 432Hz"
date: 2026-09-21T12:00:00+02:00
draft: true
tags: ["shitpost"]
---

You must have heard at some point about the magical frequency of 432Hz.
More specifically about musical tuning where instead of our western A=440Hz we set A=432Hz.
There is an additional layer to this, when people also claim that equal temper tuning is wrong and babble about ancient Greeks and how they supposedly tuned their liras.

There is an incredibly simple argument to make that invalidates all of these, but we'll get to that.

# Why am I writing this post?
A couple of reasons, really.
First of all it's funny, second of all I kind of want to get it out of my system.

# Who is the target audience of this post?
Ideally people believing in those conspiracies, but I'm highly sceptical this post will ever reach them. And that they'll understand any of it if it does.

# Let's get started

There are numerous websites claiming A=432Hz is somehow magical, that it calms nerves, heals diseases and can make you a higher being.
The same websites then often go on about A=440Hz being some US gov. conspiracy and that it's exactly tuned to make the population docile etc.
The fascinating thing about all this crap is that the very basis of these arguments is complete and utter misunderstanding how anything in our physical world works.

The answer is: **units**.

If you're from STEM, or a slightly science inclined high schooler, you can probably infer the rest of this post.
In that case you can either close the tab or continue reading if you're into that kind of thing.

## Continue?
Great to have you there, thanks.
First I'm going to talk about why SI units are as arbitrary in this context as it can get.
Then let's go over a simple procedure with which we can generate much more convincing magical frequencies (and more!).

## Natural units
Every physicist learns them at some point.
The core idea is that instead of using SI units (or God forbid Imperial) we set as many of our physical constants to $1$ as possible.
For example in Special Relativity you might write things like $t' = \gamma\left(t - vx/c^2\right)$[^1] a lot and after some time you *will* just say $c=1$ and write $t' = \gamma\left(t - vx\right)$.
There are a couple flavours of natural units depending on the area in which they make calculations the simplest.
Today we'll use [Planck units](https://en.wikipedia.org/wiki/Planck_units) because I had to pick something.
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
