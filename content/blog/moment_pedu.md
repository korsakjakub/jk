---
title: "Algebra operatorów translacji w mechanice kwantowej"
subtitle: "Notatki z AGQM"
date: 2022-04-24T11:00:00+02:00
draft: true
categories: ["fizyka", "studia"]
tags: ["fizyka", "studia", "mechanika kwantowa"]
---

# Udowodnij relację

$$ \left(\frac{i}{\hbar}\hat{p}\right)^n \hat{B}(x) = \sum_{\nu = 0}^n \binom{n}{\nu} \frac{\partial^\nu \hat{B}}{\partial x^\nu} \left(\frac{i}{\hbar}\hat{p}\right)^{n - \nu},$$

gdzie $\hat{p} = (\hbar/i)\partial_x$ jest określone dla każdego różniczkowalnego operatora $\hat{B}(x)$.

# Rozwiązanie

Relację udowodnimy metodą indukcji. Dla $n = 0$ relacja jest spełniona identycznościowo.

Załóżmy zatem, że dla pewnego $n$ jest ona prawdziwa i sprawdźmy czy jest również dla $n-1$.

$$ \left(\frac{i}{\hbar}\hat{p}\right)^{n-1} \hat{B}(x) = \sum_{\nu = 0}^{n-1} \binom{n-1}{\nu} \frac{\partial^\nu \hat{B}}{\partial x^\nu} \left(\frac{i}{\hbar}\hat{p}\right)^{n - 1 -\nu}.$$

Zadziałajmy na lewą stronę operatorem $i\hat{p}/\hbar$,

$$\begin{align*}\left(\frac{i}{\hbar}\hat{p}\right)^n \hat{B}(x) &= \left(\frac{i}{\hbar}\hat{p}\right)\left(\left(\frac{i}{\hbar}\hat{p}\right)^{n-1} \hat{B}(x)\right) \cr
&= \left(\frac{i}{\hbar}\hat{p}\right)\sum_{\nu = 0}^{n-1} \binom{n-1}{\nu} \frac{\partial^\nu \hat{B}}{\partial x^\nu} \left(\frac{i}{\hbar}\hat{p}\right)^{n - 1 -\nu} \cr
&= \sum_{\nu = 0}^{n-1} \binom{n-1}{\nu} \left(\frac{i}{\hbar}\left[\hat{p}, \frac{\partial^\nu \hat{B}}{\partial x^\nu}\right]\left(\frac{i}{\hbar}\hat{p}\right)^{n-1-\nu} + \frac{\partial^\nu \hat{B}}{\partial x^\nu}\left(\frac{i}{\hbar}\hat{p}\right)^{n-\nu} \right) \cr
&= \sum_{\nu = 0}^{n-1} \binom{n-1}{\nu} \frac{\partial^{\nu+1} \hat{B}}{\partial x^{\nu + 1}} \left(\frac{i}{\hbar}\hat{p}\right)^{n-(\nu+1)} + \sum_{\nu = 0}^{n-1}\binom{n-1}{\nu}\frac{\partial^\nu \hat{B}}{\partial x^\nu}\left(\frac{i}{\hbar}\hat{p}\right)^{n-\nu}
\end{align*}$$

Ciąg dalszy nastąpi
