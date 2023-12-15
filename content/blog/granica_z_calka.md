---
title: "Granica z całką"
date: 2023-12-15T10:03:39+02:00
draft: false
tags: [liceum, matematyka, kinematyka]
---
Zadanie z [Jedno Zadanie Dziennie](https://www.facebook.com/jednozadaniedziennie)
![](https://scontent-waw1-1.xx.fbcdn.net/v/t39.30808-6/409985564_1088506618787192_6723531400838331671_n.jpg?_nc_cat=105&ccb=1-7&_nc_sid=dd5e9f&_nc_ohc=8NI59bW-fjcAX8j5eMf&_nc_ht=scontent-waw1-1.xx&oh=00_AfARer4nCyDHMSnD_vt2gFdi-NDkPv27ahvpuEa0bKAp-Q&oe=6580E0BE)

Zacznijmy od 

$$(a+b)^n = \sum_{k=0}^n \begin{pmatrix}n\cr k\end{pmatrix} a^{n-k} b^k.$$

W naszym przypadku to pod całką, to $a = 1$ oraz $b = -x^2/n$. To lecimy

$$=\lim_{n\to \infty} \int_0^{\sqrt{n}} \sum_{k=0}^n \begin{pmatrix}n\cr k\end{pmatrix}\left(\frac{x^2}{n}\right)^k \cdot (-1)^k dx.$$

Dużo można wyciągnąć przed całkę

$$=\lim_{n\to \infty} \sum_{k=0}^n (-1)^k \begin{pmatrix}n\cr k\end{pmatrix}\int_0^{\sqrt{n}} \frac{x^{2k}}{n^k} dx.$$

Wyrażenie pod całką łatwo obliczamy

$$=\lim_{n\to \infty} \sum_{k=0}^n (-1)^k \begin{pmatrix}n\cr k\end{pmatrix} \frac{\sqrt{n}}{2k+1}.$$

Okazuje się, że część tego napisu możemy ładnie przehandlować na stosunek podwójnych silni. Otóż, zachodzi taka równość: $\sum_{k=0}^n \begin{pmatrix}n \cr k \end{pmatrix} \frac{(-1)^k}{2k+1} = (2n)!! / (2n+1)!!$.

$$=\lim_{n\to \infty} \sqrt{n}\frac{(2n)!!}{(2n+1)!!}.$$

Dalej, możemy połączyć to z wynikiem z [Całek Wallisa](https://en.wikipedia.org/wiki/Wallis%27_integrals), który ma postać $(2p)!! / (2p - 1)!! \sim \sqrt{\pi p}$ dla dużych $p$.
Zamienimy sobie zmienne $2p := 2n+1;\quad 2p-1 := 2n;\quad p := n+1/2$ i możemy zapisać wtedy

$$= \lim_{n\to \infty} \sqrt{n} \frac{1}{\sqrt{\pi p}}  = \lim_{n\to \infty} \sqrt{n} \frac{1}{\sqrt{\pi (n+1/2)}}.$$

Teraz już będzie łatwo:

$$= \frac{1}{\sqrt{\pi}} \lim_{n\to \infty} \sqrt{\frac{n}{n+1/2}} = \frac{1}{\sqrt{\pi}}.$$
