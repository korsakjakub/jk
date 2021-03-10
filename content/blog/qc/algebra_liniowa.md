---
title: O algebrze liniowej
date: 2021-03-07T10:00:00
tags: [studia, algebra liniowa, matematyka]
---

# Przestrzeń wektorowa

Najbardziej elementarną częścią algebry liniowej jest pojęcie przestrzeni wektorowej. Żeby do niego dojść, trzeba najpierw zdefiniować ciało algebraiczne.

## Definicja (ciało)

Niech $\mathbb{F}$ będzie niepustym zbiorem i $0,1\in \mathbb{F}$ tak, że $0 \neq 1$ (w naszych rozważaniach zazwyczaj $\mathbb{F} = \mathbb{C}$). Niech
$$+,\cdot : \mathbb{F}^2 \to \mathbb{F}$$
będą działaniami dwuargumentowymi. Mówimy, że $(\mathbb{F}, 0, 1, +, \cdot)$ jest ciałem, jeżeli:

- $(\mathbb{F}, +)$ jest grupą przemienną,
- $(\mathbb{F}\setminus \\{0\\}, \cdot)$ jest grupą przemienną,
- $\forall \lambda, \mu, \nu \in \mathbb{F}$ zachodzi $\lambda(\mu+\nu) = \lambda \mu + \lambda \nu$

(ciałem nazywa się pierścień przemienny z jedynką, w którym każdy niezerowy element jest odwracalny).

## Definicja (przestrzeń wektorowa)

Niech $(V, +)$ będzie grupą abelową (przemienną), $\mathbb{F}$ będzie ciałem oraz
$$\cdot : \mathbb{F} \times V \to V.$$
Mówimy, że $(V, +, \cdot)$ jest przestrzenią wektorową nad ciałem $\mathbb{F}$ jeżeli $\forall \lambda, \mu \in \mathbb{F}$ i $u, w \in V$ zachodzi:

- $(\lambda + \mu) u = \lambda u + \mu u$
- $\lambda(u + w) = \lambda u + \lambda w$
- $\lambda(\mu \cdot u) = (\lambda \mu) u$
- $1 \cdot u = u$.

Elementy $V$ nazywami wektorami, a elementy $\mathbb{F}$ skalarami.

## Dodawanie wektorów

Niech $(\lambda_1, \dots, \lambda_n), (\mu_1,\dots,\mu_n) \in \mathbb{F}^n$. Wtedy mamy
$$(\lambda_1,\dots,\lambda_n) + (\mu_1,\dots,\mu_n) = (\lambda_1 + \mu_1,\dots,\lambda_n + \mu_n) \in \mathbb{F}^n$$

# Notacja Diraca

W mechanice kwantowej, a w szczególnośći w obliczeniach kwantowych wykorzystuje się notację Diraca. Bazuje ona na przedstawianiu stanów kwantowych $\psi$ jako wektory ket
$$|\psi\rangle$$
oraz wektorów sprzężonych bra
$$\langle\psi| = (|\psi\rangle)^*.$$

## Przestrzeń Hilberta

Wektory te żyją w przestrzeni Hilberta, która jest przestrzenią unitarną i zupełną. Oznacza to, że
- ma zdefiniowany iloczyn skalarny,
- traktowana jako przestrzeń metryczna z metryką indukowaną przez iloczyn skalarny jest zupełna, czyli każdy ciąg Cauchy ma granicę.

## Iloczyn skalarny w przestrzeni Hilberta

Iloczynem skalarnym nazywamy odwzorowanie $\langle \cdot | \cdot \rangle : V^2 \to \mathbb{C}$, które spełnia zależności:

1. Symetria:
	$$\langle \phi | \psi \rangle = \langle \psi | \phi\rangle^*.$$
2. Biliniowość:
	$$\langle \phi | a \psi + b \psi' \rangle = a \langle \phi | \psi \rangle + b \langle \phi | \psi' \rangle.$$
3. Dodatnio określoność:
	$$\langle \psi | \psi \rangle \ge 0.$$

W przestrzeni Hilberta $\mathcal{H} = \mathbb{C}^n$ definiuje się go jako
$$((y\_1,\dots, y\_n), (z\_1, \dots, z\_n)) \equiv \sum_i y\_i\^* z\_i.$$

## Norma

Norma wektora stanu jest zdefiniowana jako
$$\Vert \psi \Vert \equiv \sqrt{\langle \psi | \psi \rangle}.$$

## Nierówność Cauchy-Schwartz

$$|\langle \psi | \phi\rangle| \le \Vert \psi \Vert \Vert \phi \Vert.$$

# Macierze i operatory liniowe

## Iloczyn tensorowy (iloczyn Kroneckera)

Niech $A \in \mathbb{M}\_{n\times m}[\mathbb{C}]$ oraz $B \in \mathbb{M}\_{p\times q}[\mathbb{C}]$ będą macierzami. Ich iloczyn tensorowy $A \otimes B \in \mathbb{M}\_{pm \times qn}[\mathbb{C}]$ jest macierzą blokową postaci

$$(A \otimes B)\_{ij} = [a\_{ij} B].$$

## Iloczyn zewnętrzny (outer product)
Dla iloczynu wektorów typu $|\psi\rangle\langle \phi| = \begin{bmatrix}p^1\cr \vdots \cr p^n\end{bmatrix} [q\_1,\dots q\_m]^* = \begin{bmatrix}p^1q\_1^* & \dots & p^1q\_m^*\cr \vdots & \ddots & \vdots \cr p^nq\_1^* & \dots & p^nq\_m^*\end{bmatrix}\in \mathbb{M}\_{m\times n}[\mathbb{C}].$

## Sprzężenie Hermitowskie

Sprzężenie hermitowskie macierzy $A^\dagger = (A^T)^*$ wygląda tak

$$\begin{bmatrix} a&b \cr c & d\end{bmatrix}^\dagger = \begin{bmatrix} a\^* & c\^* \cr b\^* & d\^*\end{bmatrix}$$


## Macierze Pauliego

$$\sigma\_0 \equiv \mathbb{I} \equiv \begin{bmatrix}1&0\cr 0&1\end{bmatrix}$$
$$\sigma\_1 \equiv \mathbb{X} \equiv \begin{bmatrix}0&1\cr 1&0\end{bmatrix}$$
$$\sigma\_2 \equiv \mathbb{Y} \equiv \begin{bmatrix}0&-i\cr i&0\end{bmatrix}$$
$$\sigma\_3 \equiv \mathbb{Z} \equiv \begin{bmatrix}1&0\cr 0&-1\end{bmatrix}$$

## Generowanie bazy ortonormalnej (Gram-Schmidt)

Niech $|w_i\rangle$ - wektory bazowe z przestrzeni wektorowej $V$ z iloczynem skalarnym, $\dim V = d$. Zdefiniujmy pierwszy wektor nowej bazy ortonormalnej przez
$$|v\_1\rangle \equiv \frac{|w\_1\rangle}{\Vert |w\_1\rangle\Vert},$$

następne dla $1 \le k \le d-1$ definiujemy rekurencyjnie

$$|v\_{k+1}\rangle \equiv \frac{|w\_{k+1}\rangle - \sum\_{i=1}\^k \langle v\_i | w\_{k+1}\rangle | v\_i \rangle}{\Vert|w\_{k+1}\rangle - \sum\_{i=1}\^k \langle v\_i | w\_{k+1}\rangle | v\_i \rangle\Vert}$$


## Rozkład własny

Wektory własne operatora $A$ to takie wektory ($|\psi\rangle$), które spełniają
$$A |\psi\rangle = \lambda |\psi\rangle,$$
gdzie $\lambda\in\mathbb{C}$ - wartość własna. Zbiór wszystkich wartości własnych
$$\Lambda \equiv \\{ \lambda\_1,\dots,\lambda\_n \\}$$
nazywamy widmem macierzy $A$. Wektory własne są ortonormalne, co oznacza, że tworzą bazę ortonormalną
$$|\Psi\rangle \equiv \\{ |\psi\_1\rangle, \dots, |\psi\_1\rangle\\}.$$

Wartości własne macierzy są rozwiązaniami równania wielomianowego
$$\mathbb{C}\_{\dim(A)}[\lambda]\ni \det(A - \lambda \mathbb{I}) = 0$$

Reprezentacją własną operatora liniowego $A$ nazywamy
$$A = \sum\_i \lambda\_i |i\rangle\langle i|,$$
gdzie $\lambda\_i$ - wartości własne oraz $|i\rangle$ - wektory własne. Reprezentacja własna jest równoważna reprezentacji w kombinacji operatorów rzutowych na podprzestrzeń własną operatora.

## Operator rzutowy

Niech $W$ będzie $k$-wymiarową podprzestrzenią wektorową $d$-wymiarowej przestrzeni $V$. Korzystając z ortogonalizacji Grama-Schmidta można utworzyć ortonormalną bazę $|1\rangle,\dots,|d\rangle$ nad $V$ w taki sposób, że $|1\rangle,\dots,|k\rangle$ jest ortonormalną bazą nad $W$. Projektorem z przestrzeni $V$ na podprzestrzeń $W$ nazywamy wtedy operator
$$P \equiv \sum\_{i = 1}\^k |i\rangle\langle i |.$$

## Operator normalny

Operatorem normalnym nazywamy operator liniowy i ograniczony $\mathcal{N}: \mathcal{H} \to \mathcal{H}$, który komutuje ze swoim sprzężeniem, czyli spełnia warunek
$$\mathcal{N}\mathcal{N}\^* = \mathcal{N}\^*\mathcal{N}.$$

Operatorami normalnym są na przykład operatory:
- unitarne ($\mathcal{N}\^* = \mathcal{N}^{-1}$)
- samosprzężone ($\mathcal{N}\^* = \mathcal{N}$)
- rzutu ortogonalnego ($\mathcal{N} = \mathcal{N}\^* = \mathcal{N}\^2$)

## Twierdzenie spektralne
Dowolny operator normalny $\mathcal{N}$ określony na przestrzeni wektorowej $V$ jest diagonalny w pewnej ortonormalnej bazie na $V$. Zachodzi również implikacja w drugą stronę, każdy diagonalizowalny operator jest operatorem normalnym.

Oznacza to, że każdy operator normalny można zapisać w reprezentacji własnej.

## Superoperatory liniowe

Istnieje wiele ważnych odwzorowań, które przekształcają operatory liniowe i macierze. Wychodząc z definicji funkcji $f: \mathbb{C} \to \mathbb{C}$, można łatwo rozszerzyć jej definicję na macierze normalne (w tym podzbiór macierzy hermitowskich) następującą konstrukcją:

Niech $A = \sum\_a a |a\rangle \langle a|$ będzie rozkładem spektralnym operatora normalnego $A$. Zdefiniujmy następnie
$$f(A) \equiv \sum\_a f(a) |a\rangle\langle a|.$$ W ten sposób można łatwo zdefiniować na przykład eksponens macierzy
$$\exp(\theta \mathbb{Z}) = \begin{bmatrix}e\^\theta &0\cr 0 & e\^{-\theta}\end{bmatrix},$$
ponieważ $\mathbb{Z}$ ma widmo $\Lambda = \\{|0\rangle, |1\rangle\\}$.

### Ślad

Ślad macierzy jest definiowany jako suma jej elementów diagonalnych:
$$\mathrm{tr}(A) \equiv \sum\_i A\_{ii}.$$
Naturalnie, jest on zależny od bazy oraz cykliczny, czyli zachodzi
$$\mathrm{tr}(AB) = \mathrm{tr}(BA).$$
Ślad jest również liniowy, czyli
$$\mathrm{tr}(A + zB) = \mathrm{tr}(A) + z \\,\mathrm{tr}(B).$$
Z cykliczności wynika niezmienniczość pod wpływem transformacji unitarnych:
$$\mathrm{tr}(UAU\^\dagger) = \mathrm{tr}(U\^\dagger U A) = \mathrm{tr}(A).$$

Dla pewnego wektora $|\psi\rangle$ należącego do bazy ortonormalnej $|i\rangle$ zachodzi
$$\mathrm{tr}(A|\psi\rangle\langle\psi|) = \sum\_i \langle i|A|\psi\rangle\langle\psi |i\rangle = \langle \psi|A|\psi\rangle.$$

## Reguły komutacji macierzy Pauliego

Niech $\varepsilon$ - tensor zupełnie antysymetryczny. Wtedy
$$[\sigma\_j,\sigma\_k] = 2 i \sum\_{l = 1}\^3 \varepsilon\_{jkl} \sigma\_l.$$

## Rozkład według wartości osobliwych (singular value decomposition)

Niech $A\in \mathbb{M}\_{n\times n}[\mathbb{C}]$ będzie kwadratową macierzą. Wtedy istnieją macierze unitarne $U$ oraz $V$, które wraz z dodatniookreśloną macierzą diagonalną $D$ spełniają zależność
$$A = U D V.$$
