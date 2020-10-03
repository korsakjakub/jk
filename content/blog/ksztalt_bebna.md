---
title: "Czy można usłyszeć kształt bębna?"
date: 2020-09-14T20:39:43+02:00
draft: true
---

## Krótka odpowiedź: Trochę tak, trochę nie.

# Wstęp
Jeżeli wyobrazimy sobie dwuwymiarową membranę $\mathcal{M}(\mathcal{C}^\infty)$ (rozmaitość), ograniczoną brzegiem $\partial\mathcal{M}(\mathcal{C}^\infty)$ i wyprowadzimy z położenia równowagi, to składowa prostopadła do jej oryginalnej płaszczyzny
$$F(x,y,t) \equiv F(\rho, t)$$
spełnia równanie falowe
$$\ddot{F} = c^2 \Delta F,$$
gdzie $c$ jest pewną stałą. Dalej ustalimy takie jednostki, żeby $c^2 = 1.$

Rozwiązania tego problemu, które szczególnie nas interesują są postaci
$$F(\rho, t) = U(\rho)e^{i\omega t},$$
gdyż mogą reprezentować czyste tony produkowane przez membranę - czyli mody normalne. Aby je znaleźć, podstawiamy $$U(\rho)e^{i \omega t}$$
do równania falowego i otrzymujemy
$$\begin{align*}
\ddot{F} &= -\omega^2 U(\rho) e^{i \omega t} \cr
\Delta F &= \frac{1}{2} e^{i\omega t} \Delta U(\rho) \cr
e^{i\omega t} \neq 0 &\implies \Delta U(\rho) + \omega^2 U(\rho) = 0
\end{align*}.$$
Trzeba by jeszcze wziąć pod uwagę, że na brzegu membrana ma się nie wychylać. Można to zapisać warunkiem, czyli gdy $\rho$ dąży od wewnątrz do $\partial M$, to $U\to 0$.
Możnaby powiedzieć, że $\Delta$ to operator liniowy $L$ i wtedy otrzymamy zagadnienie własne:
$$L \psi = \lambda \psi,$$
gdzie $\lambda$ - wartości własne, a $\psi \in \mathcal{L}^2(\mathbb{R})$ to wektory własne.

Czyli dla zadanego regionu $\mathcal{M}$ ograniczonego gładką krzywą $\partial\mathcal{M}$, możemy dostać sekwencję liczb $\lambda_1, \lambda_2,\ldots$, które będą spełniały problem
$$L \psi = \lambda_n \psi.$$

# Problem
Chcielibyśmy zadać teraz pytanie odwrotne:

Czy jeżeli ktoś przyśle nam nagrany bardzo dobrym mikrofonem bęben, to czy mając słuch absolutny jesteśmy w stanie ten bęben narysować? Czyli co możemy powiedzieć o geometrii regionu $\mathcal{M}$ i $\partial\mathcal{M}$, jeżeli ktoś przyśle nam sms-em zbiór wszystkich wartości własnych $\lambda_1,\ldots, \lambda_m$.

Inaczej sformułowany problem brzmi: Czy istnieją dwa bębny o różnych kształtach, które brzmią dokładnie tak samo?

Czyli niech $\mathcal{M}_1$ i $\mathcal{M}_2$ - rozmaitości na $\mathbb{R}^2$ ograniczone odpowiednio $\partial\mathcal{M}_1$ i $\partial\mathcal{M}_2$.

Rozważmy problemy własne dla $L = \Delta$.
$$\begin{align*}
L U(\rho) &= \lambda U(\rho), \quad\rho\in \mathcal{M}_1 &L V(\rho) &= \eta V(\rho), \quad\rho\in \mathcal{M}_2 \cr
U &= 0, \quad\rho\in\partial\mathcal{M}_1 &V &= 0, \quad\rho\in\partial\mathcal{M}_2
\end{align*}$$
Niech teraz $\underset{n}{\forall}\quad\lambda_n = \eta_n$. Czy $\mathcal{M}_1$ i $\mathcal{M}_2$ są identyczne w sensie geometrii euklidesowej?

## Dygresja
Niech $\Omega = [0,a]\subset\mathbb{R}^2$ - zbiór domknięty. Rozważmy problem
$$\begin{align*}
\psi_{,xx}(x) &= \lambda \psi(x), \quad x\in\Omega \cr
\psi(0) &= \psi(a) = 0
.\end{align*}$$
Rozwiązaniem tego problemu są funkcje
$$\psi_m(x) = \sin\Big(\frac{m\pi}{a}x\Big),$$
z wartościami własnymi $\lambda_m = \left(\frac{m\pi}{a}\right)^2$, dla $m\in \mathbb{N}$. Zdefiniujmy sobie funkcję, która będzie nam zliczać wartości własne poniżej jakiegoś progu.

$$N(\lambda) := \left| \\{ m: \lambda_m < \lambda \\} \right|.$$
Dla naszych $\lambda_m$ mamy
$$N(\lambda) = \left| \left\\{ m: \left(\frac{m\pi}{a}\right)^2 < \lambda \right\\} \right| = \max \left\\{ m: m < \frac{a}{\pi} \sqrt{\lambda}\right\\}.$$
Więc dla $\lambda \to \infty$, $N(\lambda) < \frac{a}{\pi}\sqrt{\lambda}$. Czyli
$$\lim_{\lambda\to \infty} \frac{N(\lambda)}{\sqrt{\lambda}} = \frac{a}{\pi}$$
Ale $\Omega = [0,a]$, więc $a = |\Omega|$. Czyli dla struny, możemy już z samej liczby wartości własnych wnioskować coś na temat jej długości.

## Pytanie: A co jak zamiast struny jest membrana (prześcieradło)?
Niech $\Omega = [0,a]\times[0,b]$ i niech $\psi(x,y) = \alpha(x)\beta(y)$.
Wtedy
$$\begin{align*}
&\Delta \psi = \alpha''\beta + \alpha\beta\'\' = \lambda \alpha\beta\cr
&\frac{\alpha''}{\alpha}(x) + \frac{\beta''}{\beta}(y) = \lambda\cr
&\alpha\'\' = p^2 \alpha \implies \alpha(x) = A \sin(px) + B \cos(px)\cr
&\beta\'\' = q^2\beta \implies \beta(y) = C \sin(qy) + D \cos(qy)\cr
&\alpha(0) = \alpha(a) = \beta(0) = \beta(b) \implies B = 0, D = 0\cr
&p = \frac{j\pi}{a},\quad q = \frac{k\pi}{b},\quad j,k \in \mathbb{N}
.\end{align*}$$
Więc $\psi_{j,k}(x,y) = \sin\left(\frac{j\pi}{a} x\right)\sin\left(\frac{k\pi}{b} y\right)$ i $\lambda_{j,k} = \left(\frac{j\pi}{a}\right)^2 + \left(\frac{k\pi}{b}\right)^2.$ Teraz nasza funkcja do zliczania wartości własnych wynosi
$$N(\lambda) = \left|\left\\{ (j,k) : \lambda_{j,k} < \lambda \right\\}\right| = \left|\left\\{ (j,k) : \left(\frac{j\pi}{a}\right)^2 + \left(\frac{k\pi}{b}\right)^2 < \lambda \right\\}\right|$$
Niech $E_\lambda = \left\\{(x,y)\in\mathbb{R}_+^2 : \left(\frac{x\pi}{a\sqrt{\lambda}}\right)^2 + \left(\frac{y\pi}{b\sqrt{\lambda}}\right)^2 \le 1\right\\}$ będzie prawą górną ćwiartką elipsy. W takim razie $N(\lambda)$ odpowiada łącznemu polu kwadratów $[j-1,j]\times[k-1,k]$ zawartych w $E_\lambda$ (jak na rysunku po lewej).
![](/eigen\_elipsa.png)
W takim razie możemy napisać
$$N(\lambda) = \sum_{(j,k): \lambda_{j,k} < \lambda} \mathrm{pole}([j-1,j]\times[k-1,k]) \le \mathrm{pole}(E_\lambda).$$
Ale skoro $E_\lambda$ - elipsa, to znamy wzór na jej pole: $P = \pi \cdot u v$, gdzie $u,v$ - półosie.
$$\mathrm{pole}(E_\lambda) = \underbrace{\frac{1}{4}}_{\text{tylko ćwiartka}} \cdot \pi \cdot \frac{a\sqrt{\lambda}}{\pi} \cdot\frac{b\sqrt{\lambda}}{\pi} = \frac{\lambda}{4\pi} \cdot ab = \frac{\lambda}{4\pi} \cdot |\Omega|.$$
W takim razie
$$N(\lambda) < \frac{|\Omega|}{4\pi} \lambda.$$
Sprawdzimy jakiego rzędu jest następny wyraz - żeby to zrobić, przesuniemy układ współrzędnych o jednostkę w prawo i jednostkę w górę. Czyli w nowej obciętej elipsie mieści się mniej kwadratów (rysunek, prawa strona). Pole nowej elipsy, to pole $E_\lambda$ zmniejszone o $1 \times b\sqrt{\lambda}/\pi + 1 \times a\sqrt{\lambda}/\pi + 1$ (prostokąty mają boki: $(1,b\sqrt{\lambda}/\pi)$ i $(1,a\sqrt{\lambda}/\pi)$ odpowiednio.

Czyli
$$N(\lambda) = \frac{|\Omega|}{4\pi}\lambda - \frac{\sqrt{\lambda}}{\pi}(a+b) - 1 = \frac{|\Omega|}{4\pi}\lambda - \frac{\sqrt{\mathrm{obw}(\Omega)}}{2\pi}\sqrt{\lambda} - 1.$$
Możemy więc już powiedzieć, że
$$\lim_{\lambda\to\infty} \frac{N(\lambda)}{\lambda} = \frac{|\Omega|}{4\pi}.$$

## Wniosek
Wygląda na to, że czasami można przybliżyć pole membrany, pod warunkiem, że mamy dostatecznie dużo jej wartości własnych. W ogólności mówi o tym

## Twierdzenie (Weyl)
Niech $\mathcal{M}$ - rozmaitość z brzegiem, $\dim(\mathcal{M}) = n$. Dla problemu własnego
$$\begin{align*}
\Delta \psi &= \lambda \psi, \quad\rho\in \mathcal{M}\cr
\psi &= 0, \quad \rho\in\partial\mathcal{M}
,\end{align*}$$
liczba wartości własnych poniżej progu $\lambda$ w stosunku do pewnej potęgi wartości tego progu w granicy wynosi
$$\lim_{\lambda\to \infty}\frac{N(\lambda)}{\lambda^{n/2}} = \frac{\omega_n}{(2\pi)^n}\mathrm{vol}(\Omega),$$
gdzie $\omega_n$ - objętość kuli z $\mathbb{R}^n$ o promieniu jeden.

### Przykład
Dla $n = 1$ (struna)
$$\lim_{\lambda\to \infty}\frac{N(\lambda)}{\lambda} = \frac{\omega_1}{(2\pi)^1}|\Omega| = \frac{2}{2\pi}|\Omega| = \frac{|\Omega|}{\pi}.$$
Dla $n = 2$ (membrana)
$$\lim_{\lambda\to \infty}\frac{N(\lambda)}{\lambda} = \frac{\omega_2}{(2\pi)^2}|\Omega| = \frac{\pi}{4\pi^2}|\Omega| = \frac{|\Omega|}{4\pi}.$$

## A teraz coś z zupełnie innej beczki

Zastanówmy się nad problemem dyfuzji czegoś początkowo skoncentrowanego w punkcie $\rho \equiv (x_0,y_0)$ przenikającego przez płaszczyznę $\Omega\subset\mathbb{R}^2$ otoczoną brzegiem $\Gamma$. Zakładamy, że na brzegu to ,,coś'' znika i nie odkłada się na nim.

Stężenie ,,czegoś'' $P_\Omega(r = (x,y),t)$ spełnia równanie dyfuzji
$$\dot{P}_\Omega = \Delta P_\Omega,$$
z warunkiem brzegowym
$$\lim_{r\to\Gamma} P_\Omega(r,t) = 0$$
i warunkiem początkowym
$$\lim_{t\to 0} \left< T(P_\Omega),\varphi\right> = \left<\delta_\rho, \varphi\right>,$$
gdzie $T\in D^\star$ - dystrybucja, $\varphi\in D$ - funkcja próbna.

Niech $\lambda_n$ - wartości własne i $\psi_n(r)$ - funkcje własne (z warunkiem normalizacji). Jeżeli weźmiemy sobie na przykład
$$P_\Omega(r,t) = \sum_{n=1}^\infty e^{-\lambda_n t} \psi_n(\rho) \psi_n(r),$$
to możemy to wsadzić do równania dyfuzji i dostaniemy
$$\dot{P}_\Omega = -\sum_{n=1}^\infty \lambda_n e^{-\lambda_n t} \psi_n(\rho)\psi_n(r) = \Delta P_\Omega = \sum_{n=1}^\infty e^{-\lambda_n t} \psi_n(\rho) \Delta \psi_n(r).$$
Czyli dla jakiegoś $n$
$$-\lambda_n \psi_n(r) = \Delta \psi_n(r).$$
I skoro mamy warunek znikania na brzegu, to znaczy, że
$$\lim_{r\to\Gamma}P_\Omega = 0 = \lim_{r\to\Gamma}\sum_{n=1}^\infty e^{-\lambda_n t} \psi_n(\rho) \psi_n(r) \implies \lim_{r\to\Gamma} \sum_{n=1}^\infty \psi_n(r) = 0.$$
Czyli na przykład fajne $\psi_n$, które to spełniają to takie, że
$$\lim_{r\to\Gamma}\psi_n(r) = 0.$$

### Bardziej obrazowo - co tu się mniej więcej dzieje?
Trzymamy nad blatem na jakiejś wysokości słoik miodu i zaczynamy go wylewać małym strumieniem nad środkiem blatu. W takim razie te cząsteczki miodu, które dopiero co dotknęły stołu jeszcze nie wiedzą co za straszne rzeczy je czekają na brzegu. Więc jeżeli uznamy, że $t\to 0$, to można przypuszczać, że miód nie ,,czuje'' warunku brzegowego.

Oznacza to, że chcielibyśmy rozważyć taką funkcję stężenia $P_0(r,t)$, która spełnia takie samo równanie dyfuzji jak $P_\Omega$, czyli
$$\dot{P}_0 = \Delta P_0,$$
ma nałożony taki sam warunek brzegowy $\lim_{t\to 0} \left<T(P_0),\varphi\right> = \left<\delta_\rho,\varphi\right>$ oraz
$$\lim_{t\to 0} \frac{P_\Omega}{P_0} = 1.$$
Różni się od $P_\Omega$ jedynie brakiem ograniczenia w przestrzeni. Dodatkowo załóżmy jeszcze, że tak samo jak $P_\Omega$, $P_0$ jest nieujemne - czyli w żadnym punkcie stołu nie ma ujemnej wartości miodu.

Z analizy III pamiętamy, że rozwiązanie tego problemu ma postać
$$P_0(r,t) = \frac{1}{4\pi a^2 t} \int_{\mathbb{R}} ds f(s) \exp\left(-\frac{\Vert r-s\Vert^2}{4a^2 t}\right),$$
gdzie
- $a$ - współczynnik dyfuzji, u nas $a=1$,
- $f$ - warunek początkowy, u nas $\delta_\rho$.

Ale $<\delta_\rho,\varphi> = \varphi(\rho)$, więc
$$P_0(r,t) = \frac{1}{4\pi t} \exp\left(-\frac{\Vert r-\rho\Vert^2}{4 t}\right).$$

**Notacja:** $A(a)\underset{a\to b}{\sim} B(a)$ oznacza tyle:
$$\lim_{a\to b} \frac{A}{B} = 1.$$
(starałem się jej unikać, bo mi się nie podoba, ale tutaj będzie dużo prościej)

$$P_\Omega(r,t) = \sum_{n=1}^\infty e^{-\lambda_n t}\psi_n(\rho)\psi_n(r) \underset{t\to 0}{\sim} \frac{1}{4\pi t} \exp\left(- \frac{\Vert r-\rho \Vert^2}{4 t}\right).$$
Z dużą dozą ostrożności powiedzmy, że $\rho = r$. Wtedy wychodzi
$$\sum_{n=1}^\infty e^{-\lambda_n t}\psi_n^2(r) \underset{t\to 0}{\sim} \frac{1}{4\pi t}.$$
Teraz, jeżeli jeszcze szczelniej zamkniemy oczy i scałkujemy obustronnie korzystając przy okazji z warunku normalizacyjnego dla $\psi$, to dostaniemy
$$\sum_{n=1}^\infty e^{-\lambda_n t} \underset{t\to 0}{\sim} \frac{|\Omega|}{4\pi t},$$
bo $\int_\Omega dr \psi^2 = 1$, $\int_\Omega dr = |\Omega|$.

Trzeba teraz na chwilkę pogrzebać w teorii miary. Niech $\Lambda = \\{\lambda_1, \lambda_2, \ldots \\}$ - zbiór wszystkich wartości własnych.

Mamy ich przeliczalnie dużo, więc niech $\mu(\lambda) = \sum_{\lambda_n<\lambda} \psi_n^2$ - miara (taka do zliczania). W takim razie zachodzi
$$\int_\Lambda e^{-\lambda t} d\mu \underset{t\to 0}{\sim} \sum_{\lambda_n \in \Lambda} e^{-\lambda_n t} \psi_n^2 = \sum_{n = 1}^\infty e^{-\lambda_n t} \psi_n^2.$$

### Przerywnik - Twierdzenie Tauberiańskie(?) (Hardy-Littlewood-Karamata)
Niech
$$\omega(\lambda) = \int_\Lambda e^{-\lambda t} d\mu(\lambda).$$
Wtedy dla $\alpha\in \mathbb{R}_+$
$$\mu(\lambda) \underset{\lambda\to\infty}{\sim} \frac{C}{\Gamma(\alpha+1)}\lambda^\alpha.$$

### Wracamy do naszego problemu:
Zapisujemy to, czego się właśnie dowiedzieliśmy:
$$\int_\Lambda e^{-\lambda t} d\mu \underset{t\to 0}{\sim} \sum_{n=1}^\infty e^{-\lambda_n t} \psi_n^2 \underset{t\to 0}{\sim} \frac{1}{4\pi t} = \frac{1}{4\pi} \int_0^\infty e^{-\lambda t}d\lambda.$$
Skoro mamy twierdzenie Tauberiańskie, to znaczy, że
$$\mu(\lambda) = \sum_{\lambda_n < \lambda} \psi_n^2 \underset{\lambda\to \infty}{\sim} \frac{C}{\Gamma(\alpha+1)}\lambda^\alpha,$$
ale u nas
$$\sum_{\lambda_n < \lambda} \psi_n^2  \underset{\lambda\to\infty}{\sim} \frac{1}{4\pi} \lambda,$$
czyli $\alpha = 1$ i $C = \frac{1}{4\pi}$.

Co teraz? Scałkujmy obustronnie
$$\sum_{\lambda_n<\lambda} \int_\Omega \psi_n^2 \underset{\lambda\to\infty}{\sim} \frac{\lambda}{4\pi}\int_\Omega 1,$$
czyli
$$\sum_{\lambda_n < \lambda} 1 \underset{\lambda\to\infty}{\sim} \frac{|\Omega|}{4\pi} \lambda.$$
Zauważmy, że to po lewej stronie, to jest definicja naszej wspaniałej funkcji zliczającej wartości własne!
$$N(\lambda) \underset{\lambda\to\infty}{\sim} \frac{|\Omega|}{4\pi}\lambda \implies \lim_{\lambda\to\infty} \frac{N(\lambda)}{\lambda} = \frac{|\Omega|}{4\pi}.$$
Oznacza to, że nie uwolnimy się od Twierdzenia Weyl'a.


## Co jeszcze?

Dalej rozważając równanie dyfuzji, zobaczymy co można zauważyć w pobliżu brzegu naszej membrany (albo gdy miód dociera do krawędzi stołu).

Wcześniej stwierdziliśmy, że na samym początku, to ,,coś'' co dyfuzuje, nie czuje brzegu. Ale po jakimś czasie, kiedy pierwsze cząsteczki zbliżą się do niego, to pewnie coś się zmieni.

Niech $\rho = (x,y) \in \Omega$ - punkt z warunku początkowego i niech $q\in \Gamma$ będzie punktem należącym do brzegu z warunkiem, że $\Vert \rho - q\Vert$ ma być najmniejsze możliwe dla ustalonego $\rho$.

Niech $l(\rho)$ - linia prostopadła do odcinka łączącego $q$ i $\rho$, przechodząca przez $q$. Możliwe, że w miarę jak cząstka będzie poruszać się w stronę $\Gamma$, to coraz bardziej ten brzeg będzie jej przypominał prostą $l(\rho)$ (rysunek po lewej).
![](/membrane.png)
Załóżmy jednak na razie, że $t$ jest dostatecznie małe, żeby można było przybliżać
$$P_\Omega \underset{t\to 0}{\sim} P_{l(\rho)}.$$
Tak jak wcześniej, $P_{l(\rho)}$ ma spełniać równanie dyfuzji z warunkiem początkowym
$$\lim_{t\to 0}\left<T(P_{l(\rho)}),\varphi\right> = \left<\delta_\rho,\varphi\right>,$$
ale z warunkiem brzegowym
$$\lim_{r\to l(\rho)}P_{l(\rho)}(r,t) = 0$$

Możemy nawet odważnie przypuścić, że
$$\int_\Omega P_\Omega(\rho,t) \underset{t\to 0}{\sim} \int_\Omega P_{l(\rho)}(\rho,t).$$

Żeby znaleźć rozwiązanie równania dyfuzji dla $P_{l(\rho)}$, wyobraźmy sobie następującą sytuację:

Kiedy nasza ,,fala dyfuzji'' dociera do $l(\rho)$, powinna odbić się od jakiejś wirtualnej ,,fali dyfuzji'' pochodzącej z punktu $\rho'$ leżącego na przedłużeniu odcinka $|\rho-q|$ i odległego od $\rho$ o $2\delta$. Nasze rozwiązanie w pobliżu $l(\rho)$ powinno więc być superpozycją rozwiązań od punktów $r = \rho$ i $r = \rho'$. Zatem mamy
$$P_{l(\rho)}(\rho,t) = \frac{1}{4\pi t} - \frac{1}{4\pi t}\exp\left(-\frac{(2\delta)^2}{4t}\right),$$
gdzie $\delta = \Vert q - \rho \Vert$ jest minimalną odległością między $\rho$ i brzegiem $\Gamma$.

Wtedy
$$\int_\Omega P_\Omega(\rho,t) = \sum_{n=1}^\infty e^{-\lambda_n t} \underset{t\to 0}{\sim} \frac{|\Omega|}{4\pi t} - \frac{1}{4 \pi t}\int_\Omega e^{-\delta^2/t}.$$
Żeby dowiedzieć się o co tu chodzi, musimy obliczyć tę całkę. Pomyślmy przez chwilę nad krzywą $\Gamma(\delta)$ składającą się z punktów oddalonych od $\Gamma$ o $\delta$ od wewnątrz (rysunek po prawej stronie).
Dla dostatecznie małych $\delta$, $\Gamma(\delta)$ powinna przypominać $\Gamma$. Skoro rozważana całka ma postać
$$\int_\Omega e^{-2\delta^2/t},$$
to znaczy, że największe przyczynki będą pochodziły właśnie od małych $\delta$. Niech $L(\delta)$ - długość brzegu $\Gamma(\delta)$. Chcielibyśmy całkować po brzegach na odległości $\delta$ od zera aż do pewnej niewielkiej $\delta_0$. Zachodzi zatem
$$\int_\Omega \exp\left(-\frac{\delta^2}{t}\right) = \int_0^{\delta_0} \exp{-\frac{\delta^2}{t}}L(\delta)d\delta + \text{coś małego}.$$
Zamiana zmiennych: niech $\xi = \frac{1}{\sqrt{t}} \delta$, więc $d\xi = \frac{1}{\sqrt{t}} d\delta$. Więc po podstawieniu
$$\int_0^{\delta_0} \exp\left(-\frac{\delta^2}{t}\right)L(\delta)d\delta = \sqrt{t} \int_0^{\delta_0/\sqrt{t}} e^{-\xi^2}L(\xi\sqrt{t})d\xi.$$
Biorąc tylko pierwszy wyraz rozwinięcia $L(\xi\sqrt{t}) \approx L(0) \equiv L$, dostajemy
$$\int_\Omega \exp\left(-\frac{\delta^2}{t}\right) \underset{t\to 0}{\sim} L\sqrt{t}\int_0^\infty e^{-\xi^2}d\xi = L\frac{\sqrt{\pi t}}{2}.$$
Wracając do stężenia $P_{l(\rho)}$, możemy podstawić wynik naszej całki
$$\int_\Omega P_\Omega = \sum_{n = 1}^\infty e^{-\lambda_n t} \underset{t\to 0}{\sim} \frac{|\Omega|}{4\pi t} - \frac{1}{4\pi t} \cdot L \frac{\sqrt{\pi t}}{2} = \frac{|\Omega|}{4\pi t} - \frac{L}{8\sqrt{\pi t}}.$$
Oznacza to, że na dodatek możemy usłyszeć obwód naszej membrany.

### Rzutem na taśmę - Nierówność izoperymetryczna
Dla dowolnej figury płaskiej zachodzi
$$\frac{4\pi A}{p^2} \le 1,$$
gdzie:
* $A$ - pole powierzchni
* $p$ - obwód.

Równość zachodzi jedynie dla koła.

Oznacza to, że znając spektrum wartości własnych pewnej okrągłej membrany, możemy używać go jako kryterium do sprawdzania, czy inne membrany są okrągłe.
