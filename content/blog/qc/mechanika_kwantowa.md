---
title: Elementarz mechaniki kwantowej
date: 2021-03-07T11:00:00
tags: [studia, mechanika kwantowa, fizyka]
draft: true
---

# Postulat 1

*Każdemu wyizolowanemu systemowi fizycznemu można przyporządkować przestrzeń wektorową na ciele zespolonym z iloczynem skalarnym (czyli przestrzeń Hilberta). Taką przestrzeń nazywamy **przestrzenią stanów** systemu. Taki system jest kompletnie opisywany przez jego **wektor stanu**, który jest unormowanym wektorem z przestrzeni stanów.*

Najprostszym takim stanem kwantowo-mechanicznym jest qubit postaci
$$|\psi\rangle = a |0\rangle + b|1\rangle,$$
gdzie
- $|0\rangle, |1\rangle \in \mathcal{H}$,
- $a, b\in \mathbb{C}$,
- $\langle\psi|\psi\rangle = 1 \implies |a|^2 + |b|^2 = 1.$

Kombinację liniową stanów $\sum\_i \alpha\_i |\psi\_i\rangle$ nazywamy superpozycją tych stanów.

# Postulat 2

*Ewolucję zamkniętego systemu kwantowego jest opisywana **transformacją unitarną**. Stan $|\psi\rangle$ w czasie $t$ jest związany ze stanem $|\psi'\rangle$ w czasie $t'$ operatorem unitarnym $U$, który zależy jedynie od tych czasów,*
$$|\psi'\rangle = U|\psi\rangle.$$

Przykładowymi operacjami unitarnymi są macierze Pauliego. Macierz $\mathbb{X}$ jest bramką logiczną *NOT* (bit flip), a macierz $\mathbb{Z}$ jest bramką odwracającą fazę (phase flip).

Inną ważną operacją jest macierz Hadamarda, która zamienia wektory bazowe (computational basis) na równe superpozycje,
$$H = \frac{1}{\sqrt{2}} \begin{bmatrix}1&1\cr 1&-1\end{bmatrix}.$$

# Postulat 3

Pomiary kwantowe opisywane są zbiorem $\\{M_m\\}$ operatorów pomiarowych. Pomiar jest aktem działania tymi operatorami na przestrzeń stanów systemu.

Prawdopodobieństwo otrzymania ze stanu $|\psi\rangle$ wyniku pomiaru $m$ wyraża się wzorem
$$p(m) = \langle \psi | M\_m\^\dagger M\_m | \psi \rangle.$$

Stan po pomiarze natomiast ma postać
$$\frac{M\_m |\psi\rangle}{\sqrt{\langle\psi|M\_m\^\dagger M\_m |\psi\rangle}}.$$

Operatory pomiarowe spełniają zależność
$$\sum\_m M\_m\^\dagger M\_m = \mathbb{I}.$$

## Przykład - pomiar qubitu

Niech $M\_0 = |0\rangle\langle 0|$ oraz $M\_1 = |1\rangle\langle 1|$ będą operatorami pomiarów na bazę obliczeniową (computational basis). Zauważmy, że $M\_i\^2 = M\_i$. Załóżmy, że badany stan to $|\psi\rangle = a|0\rangle + b|1\rangle$. Prawdopodobieństwo otrzymania wyniku $0$ to
$$p(0) = \langle \psi| M\_0\^\dagger M\_0 |\psi\rangle = \langle\psi|M\_0|\psi\rangle = |a|^2.$$

Stan po pomiarze to
$$\frac{M\_0|\psi\rangle}{|a|} = \frac{a}{|a|}|0\rangle.$$

## Dowód nierozróżnialności nieortogonalnych stanów kwantowych

Niech $f(j)$ będzie funkcją przyporządkowującą wyniki pomiarów $M$ do stanów $|\psi\rangle$.
	Przeprowadzimy dowód nie wprost. Załóżmy, że dla pewnych nieortogonalnych stanów $|\psi\_1\rangle$ i $|\psi\_2\rangle$ możliwe jest ich jednoznaczne rozróżnienie. Zakładamy zatem, że istnieje operator pomiaru, który w zadziałaniu na $|\psi\_1\rangle$ i $|\psi\_2\rangle$ zawsze produkuje różne rezultaty.
Jeżeli przygotowany jest stan $|\psi\_i\rangle$, to prawdopodobieństwo zmierzenia $j$ takiego, że $f(j) = i$, musi wynosić $1$. Zdefiniujmy operator
$$E\_i \equiv \sum\_{j: f(j) = i} M\_j\^\dagger M\_j.$$
Powyższą obserwację można zapisać jako
$$\langle\psi\_i|E\_1|\psi\_1\rangle = 1,\quad \langle\psi\_2|E\_2|\psi\_2\rangle = 1.$$

Skoro $\sum\_i E\_i = \mathbb{I}$, to
$$\sum\_i \langle \psi\_1| E\_i | \psi\_1\rangle = 1,$$
a skoro wiemy, że $\langle\psi\_1|E\_1|\psi\_1\rangle = 1$, to musi zachodzić $\langle\psi\_1|E\_2|\psi\_1\rangle = 0$, zatem
$$\sqrt{E\_2}|\psi\_1\rangle = 0.$$
Załóżmy, że $|\psi\_2\rangle = \alpha|\psi\_1\rangle + \beta|\psi\^\perp\rangle$ z warunkiem normalizacyjnym $|\alpha|^2 + |\beta|^2 = 1$ oraz $|\alpha| \neq 0 \implies |\beta| < 1$. Zatem
$$\sqrt{E\_2}|\psi\_2\rangle = \beta\sqrt{E\_2}|\psi\^\perp\rangle,$$
co implikuje sprzeczność, postaci
$$\langle \psi\_2 | E\_2 | \psi\_2\rangle = |\beta|^2 \langle\psi\^\perp|E\_2|\psi\^\perp\rangle \le |\beta|^2 < 1,$$
co kończy dowód.

## Pomiary rzutowe

Niech $M$ będzie obserwablą z przestrzeni stanów mierzonego systemu. Obserwablę można zapisać w reprezentacji widmowej
$$M = \sum\_m m P\_m,$$
gdzie $P\_m$ jest operatorem rzutowym na przestrzeń własną $M$ z wartościami własnymi $m$. Prawdopodobieństwo otrzymania z pomiaru rzutowego stanu kwantowego $|\psi\rangle$, wyniku $m$ wynosi
$$p(m) = \langle\psi|P\_m|\psi\rangle.$$

Przy założeniu otrzymania w wyniku pomiaru $m$, stan kwantowy przechodzi w
$$\frac{P\_m|\psi\rangle}{\sqrt{p(m)}}.$$

TODO: Dokończyć

# Operator gęstości

Operator gęstości jest przydatnym narzędziem do opisywania systemów z niecałkiem określonymi stanami (mieszanymi). Jako, że jest to uogólnienie, to wcześniejsze postulaty można przepisać na język operatorów gęstości. Najpierw pokażę, jak konstruować macierze gęstości z kombinacji stanów czystych, później przejdziemy do przeformułowania postulatów mechaniki kwantowej do formy bardziej ogólnej, opartej na wewnętrznej naturze operatorów gęstości.

Niech $\mathcal{E} = \\{p\_i, |\psi\_i\rangle\\}$ będzie zbiorem stanów czystych. Operator gęstości definiujemy jako
$$\rho \equiv \sum\_{i\in \mathcal{E}} p\_i |\psi\_i\rangle\langle\psi\_i|.$$

## Ewolucja stanu
Niech $|\psi\_i\rangle$ przedstawia stan początkowy systemu z prawdopodobieństwem $p\_i$. Po ewolucji unitarnej stan ten będzie miał postać $U|\psi\_i\rangle$ z prawdopodobieństwem $p\_i$. Zatem w języku operatorów gęstości mamy
$$\rho = \sum\_{i\in \mathcal{E}} p\_i|\psi\_i\rangle\langle\psi\_i| \overset{\to}{U} \rho' = \sum\_{i\in\mathcal{E}}p\_i U|\psi\_i\rangle\langle\psi\_i|U\^\dagger = U\rho U\^\dagger.$$

## Pomiary
Załóżmy, że dokonujemy pomiaru operatorem $M\_m$. Prawdopodobieństwo otrzymania wyniku $m$ pod warunkiem, że stan wynosił $|\psi\_i\rangle$ wynosi

$$p(m|i) = \langle\psi\_i|M\_m\^\dagger M\_m|\psi\_i\rangle = \mathrm{tr}(M\_m\^\dagger M\_m|\psi\_i\rangle\langle\psi\_i|).$$

Zatem prawdopodobieństwo otrzymania wyniku $m$ dla dowolnego stanu to
$$\begin{align*} p(m) &= \sum\_i p(m|i) p\_i =\cr
&= \sum\_i p\_i \mathrm{tr}(M\_m\^\dagger M\_m |\psi\_i\rangle\langle \psi\_i|) = \cr
&= \mathrm{tr}(M\_m\^\dagger M\_m \rho).\end{align*}$$
