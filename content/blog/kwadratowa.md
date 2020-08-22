---
title: "Równanie kwadratowe"
date: 2020-08-22T18:42:20+02:00
draft: false
---

# Co to znaczy, że rozwiązujemy równanie kwadratowe?

Niech $f : \mathbf{R} \to \mathbf{R}$ będzie funkcją, która mapuje liczby rzeczywiste innym liczbom rzeczywistym. Niech $a,b,c\in \mathbf{R}\setminus \{0\}$ będą liczbami rzeczywistymi różnymi od zera. Jeżeli funkcja ta zadana będzie wzorem
$$ f(x) = ax^2 + bx + c,$$
to znalezienie takich argumentów $x_1$, $x_2$, które spełniają zależność
$$f(x_1) = 0,\quad f(x_2) = 0$$
będzie tożsame z rozwiązaniem równania postaci
$$ ax^2 + bx + c = 0.$$

Na chwilę zapomnijmy, że kojarzymy gotowy wzór na rozwiązania tego równania. Zamiast go podawać, chcielibyśmy go wyprowadzić z prostej geometrycznej obserwacji.

Niech $a>0$, $b>0$, $c<0$. Wtedy wiemy o wyglądzie tej funkcji cztery fakty
1. Ma kształt paraboli (jak każda funkcja kwadratowa),
2. Jej ramiona skierowane są w górę ($a>0$),
3. W punkcie $x = 0$, przyjmuje wartość ujemną ($f(0) = c < 0$),
4. Możliwe, że ten fakt będzie najmniej oczywisty: jej wierzchołek znajduje się w ujemnej półosi $OX$.

Dowód (punktu czwartego):

Niech $\alpha(x) = ax^2 + c$. O funkcji tej wiemy, że jest parzysta (przyjmuje takie same wartości dla argumentów dodatnich i ujemnych). Można to łatwo sprawdzić porównując
$$\alpha(x) = ax^2 + c \quad vs\quad \alpha(-x) = a(-x)^2 + c = ax^2 + c.$$
Skoro jest parzysta i ma kształt paraboli, to wiemy, że jej wierzchołek leży w punkcie $W = (p = 0, q = c)$. Dodajmy następnie do funkcji $\alpha(x)$ nową funkcję $\beta(x) = bx$. Jeżeli przyjmiemy, tak jak wcześniej, $b>0$, to zauważymy, że dla dodatnich $x$ funkcja $f(x) = \alpha(x) + \beta(x)$ jest przez $\beta$ zwiększana, a dla ujemnych zmniejszana. Oznacza to, że każdy punkt wykresu funkcji $f(x)$ podniesie się dla dodatnich $x$ dokładnie o $bx$, a dla $x$ ujemnych analogicznie się obniży.

Jeżeli funkcja $\alpha(x)$ wierzchołek ma w punkcie $W$, to łatwo już zauważyć, że funkcja $f$ wierzchołek musi mieć w półosi argumentów ujemnych właśnie ze względu na nieparzysty przyczynek wpływający od funkcji $\beta(x)$, c.n.u.

## Fakt:
Umiemy rozwiązywać funkcje typu $\alpha(x) = ax^2 + c$. Jeżeli postawimy warunek
$$\alpha(x) = 0,$$
to otrzymamy równanie
$$ax^2 + c = 0 \implies x^2 = -\frac{c}{a} \implies x = \pm \sqrt{-\frac{c}{a}}.$$
Dla stałych $a,c$ takich, że $a \cdot c < 0$, oba rozwiązania należą do zbioru liczb rzeczywistych.

(Fun fact: w przeciwnym przypadku otrzymujemy rozwiązania ze zbioru liczb zespolonych. Jeżeli $a\cdot c > 0$, to $x = \pm i \sqrt{\frac{c}{a}}$.)

## Obserwacja:
Skoro umiemy rozwiązywać równania typu $\alpha(x) = 0$, to czy potrafimy przedstawić ogólną funkcję $f(x)$ w postaci czegoś bardziej przypominającego $\alpha(x)$?

Możemy spróbować po prostu przesunąć funkcję $f(x)$ w prawo (lub w lewo dla $b<0$)!

Tego typu przekształcenia dokonuje się zamianą zmiennych. Wyobraźmy sobie nowy układ współrzędnych, który od oryginalnego $(x,f(x))$ różni się tylko położeniem pionowej osi. Nowe zmienne nazwijmy jakoś ładnie, na przykład $\heartsuit$. Czyli nasz nowy układ współrzędnych ma postać $(\heartsuit, f(\heartsuit)).$

O ile chcemy ten wykres przesunąć?

No, chcielibyśmy, żeby wierzchołek znajdował się tak jak dla $\alpha(x)$ w argumencie równym zero.

Współrzędne wierzchołka można znaleźć w sposób następujący (dla znających definicję pochodnej w punkcie):

Skoro wierzchołek jest punktem, w którym funkcja nie ma nachylenia (jest ono równe zero), to można to przełożyć na język matematyki stwierdzeniem, że
$$f'(x = p) = 0,$$
gdzie $p$ - argument wierzchołka. Pochodną funkcji $f(x)$ można łatwo obliczyć. Ma ona postać:
$$f'(x) = 2ax + b.$$
Jeżeli skorzystamy z tych dwóch stwierdzeń, otrzymamy wzór na poziomą składową wierzchołka $W = (p,q):$
$$f'(p) = 0 \implies 2ap + b = 0 \implies p = -\frac{b}{2a}.$$
Wiemy zatem, że nowe współrzędne ($\heartsuit$) należy powiązać ze starymi wzorem
$$x = \heartsuit - \frac{b}{2a}.$$
Żeby zdecydować, czy powinien tu być znak plus, czy minus można na przykład położyć $x = p = -\frac{b}{2a}$ i sprawdzić, że rzeczywiście wtedy $\heartsuit = 0$.

Zapiszmy funkcję $f$ w nowych współrzędnych:
$$\begin{align*}0 = f(x) &= ax^2 + bx + c = \cr
&= a\left(\heartsuit - \frac{b}{2a}\right)^2 + b\left(\heartsuit-\frac{b}{2a}\right) + c = \cr
&= a\heartsuit^2 - \heartsuit b + \frac{b^2}{4a} + b\heartsuit - \frac{b^2}{2a} + c = \cr
&= a\heartsuit^2 - \frac{b^2}{4a} + c.\end{align*}$$
Otrzymujemy więc równanie
$$0 = a\heartsuit^2 - \frac{b^2}{4a} + c.$$
Zatem
$$\heartsuit^2 = \frac{b^2}{4a^2} - \frac{4a\cdot c}{4a\cdot a} = \frac{b^2 - 4ac}{4a^2}.$$
Tak jak z $\alpha(x)$, rozwiązujemy:
$$\heartsuit = \pm \frac{\sqrt{b^2 - 4ac}}{2a}.$$
Pamiętamy definicję serduszka: $\heartsuit = x + \frac{b}{2a}$. Więc jeżeli chcemy wrócić do oryginalnych zmiennych, to otrzymamy
$$x = -\frac{b}{2a} \pm \frac{\sqrt{b^2 - 4ac}}{2a} = \frac{-b\pm \sqrt{b^2 - 4ac}}{2a}.$$
Jeżeli wprowadzimy nowe oznaczenie: $\Delta = b^2 - 4ac$, to otrzymamy wzór, który pojawia się w podręcznikach:
$$x = \frac{-b\pm \sqrt{\Delta}}{2a}.$$

(Kontynuacja fun factu: analogicznie do poprzedniego warunku $c\cdot a > 0$, mamy tutaj $b^2 - 4ac < 0$, które generuje rozwiązania ze zbioru liczb zespolonych. Wtedy po prostu piszemy przed pierwiastkiem kwadratowym jednostkę urojoną $i$ i mamy problem z głowy. No i piękne ciało algebraicznie domknięte!)

