---
title: "Jak łatwo przesunąć statek"
subtitle: "czyli co ma zasada zachowania pędu wspólnego z ruchem środka masy?"
date: 2020-10-03T16:22:39+02:00
draft: false
categories: ["fizyka", "liceum"]
tags: ["fizyka", "liceum", "pęd", "kinematyka"]
---
# Na jakie pytania chcielibyśmy odpowiedzieć?
1. Dlaczego, gdy schodzimy z roweru wodnego (na przykład wchodząc na brzeg lub skacząc do wody), zaczyna on od nas uciekać?
2. Czy jesteśmy w stanie przyspieszyć rejs statkiem bez jakiejkolwiek znajomości obsługi statku?
# Problem
Często pojawiające się w różnych podręcznikach zadanie z zasady zachowania pędu brzmi następująco:

O ile przesunie się łódka, jeżeli człowiek najpierw stojący przy jednym jej brzegu przejdzie na brzeg przeciwny?

Rozwiązanie wymaga przyrównania środków masy układu człowiek-łódka przed i po przejściu na przeciwny brzeg łódki; argumentuje się wtedy zazwyczaj, że ten warunek wynika z zasady zachowania pędu... Ale w jaki dokładnie sposób?

Można zadać jeszcze ważniejsze z punktu widzenia fizyki pytanie:
- Co się stanie jeżeli łódka miała jakąś niezerową prędkość?

# Plan podboju kosmosu:
Spróbujemy wyjść z Zasady zachowania pędu i w jakiś sposób dojść do sensownych warunków, których rozwiązanie da nam odpowiedzi na nurtujące nas pytania.

## Ale najpierw
Kiedy w ogóle możemy skorzystać z zasady zachowania pędu?

Spójrzmy na drugą zasadę dynamiki Newtona:
$$F_{\text{zewnętrzne}}(t) = m_i \cdot a_i(t).$$
Przyjmijmy oznaczenia $P(t) = \sum_i p_i(t)= \sum_i m_iv_i(t)$ - pęd układu ($\sum$ oznacza sumę po wszystkich działających indeksach $i$. W późniejszych rozważaniach postaram się sumiennie zapominać o jej zapisywaniu).

Jeżeli założymy, że masa całego układu się nie zmienia, możemy napisać
$$F_{\text{zewnętrzne}} = \frac{d}{dt}P(t) = m_i \frac{d}{dt}v_i(t) = m_i a_i(t).$$
Teraz przypomnijmy sobie co to znaczy, że pęd jest zachowany. Powiedzmy, że pęd jest zachowany na przedziale czasu $\mathbb{T} \equiv ]t_p, t_k[$. Niech $t_1, t_2\in \mathbb{T}$ - jakieś punkty w czasie.  Wtedy możemy powiedzieć, że
$$\text{zachowany pęd} \iff p_i(t_2) - p_i(t_1) = 0 \implies p_i(t_2) = p_i(t_1),$$
czyli na przedziale otwartym $\mathbb{T}$, na którym pęd miał być zachowany, jego zmiana jest równa zero.

Teraz rozważmy $t\in \mathbb{T}$. Skoro przedział $\mathbb{T}$ jest otwarty, zawsze możemy wybrać sobie jakieś małe $\Delta t$, takie że $t + \Delta t$ wciąż będzie należało do $\mathbb{T}$. Druga zasada dynamiki przyjmuje postać
$$F_\text{zewnętrzne} = m_i \frac{d}{dt} v_i(t) = m_i \lim_{\Delta t \to 0} \frac{1}{\Delta t}\left( v_i(t+\Delta t) - v_i(t)\right),$$
ale przecież $t$ oraz $t+\Delta t$ należą do $\mathbb{T}$! Czyli ich różnica musi być równa zero, bo mamy zachowany pęd!

Otrzymujemy więc warunek
$$\underset{t\in\mathbb{T}}{\forall}\quad F_\text{zewnętrzne}(t) \equiv 0,$$
gdzie znaczek "odwrócone A" oznacza "dla każdego".

Wiemy więc, że stwierdzenie, że pęd jest zachowany oznacza tyle samo, co stwierdzenie, że na układ nie działają żadne siły zewnętrzne.

# Weźmy się do pracy
Cały układ łódka-człowiek porusza się ze stałą prędkością (w tym też równą zero).

Tak jak wcześniej ustalmy sobie przedział otwarty $\mathbb{T} = ]t_p, t_k[$, w którym pęd układu ma być zachowany.
Jeżeli weźmiemy sobie teraz punkt $t_1\in\mathbb{T}$, możemy bez ogródek napisać warunek na zasadę zachowania pędu układu:
$$\underset{t\in\mathbb{T}}{\forall}P(t) = P(t_1) \implies \underset{t\in\mathbb{T}}{\forall}p_i(t) = p_i(t_1) \implies \underset{t\in\mathbb{T}}{\forall}m_i v_i(t) = m_i v_i(t_1).$$
Skoro oba punkty czasu należą do $\mathbb{T}$, który jest przedziałem otwartym, to zawsze można znaleźć takie $\Delta t$, żeby $t + \Delta t$ również należał do $\mathbb{T}$. Przepiszmy więc powyższy warunek zamieniając $v_i$ na pochodną położeń $\frac{d}{dt}r_i$
$$m_i \lim_{\Delta t\to 0}\frac{r_i(t+\Delta t) - r_i(t)}{\Delta t} = m_i v_i(t_1).$$
Załóżmy teraz na przykład, że ustalamy taki inercjalny układ odniesienia, w którym łódka się nie porusza. W związku z tym mamy $p_i(t_1) = 0 \implies v_i(t_1) = 0.$ Dostajemy nieco uproszczoną wersję
$$m_i \lim_{\Delta t\to 0} \frac{1}{\Delta t} \left(r_i(t+\Delta t) - r_i(t)\right) = m_i \frac{d}{dt}r_i(t) = 0,$$
lecz wciąż coś tu nie gra...
Skorzystajmy z Twierdzenia Stokes'a dla jednego wymiaru (zasadnicze twierdzenie rachunku różniczkowego).
$$m_i \int_{t_1}^{t_c} \frac{d r_i}{dk}(k)dk = m_i\left(r_i(t_c) - r_i(t_1)\right) = 0,$$
czyli ostatecznie
$$m_i r_i(t_c) = m_i r_i(t_1).$$ Jest to warunek równoważny braku przesunięcia środka masy układu (przy założeniu stałej masy), czyli
$$r_{c_1} = \frac{m_i r_i(t_c)}{m_i} = r_{c_2} = \frac{m_i r_i(t_1)}{m_i}.$$

A co, jeżeli łódka poruszała się ze stałą prędkością, która akurat nie wynosiła zero? Rozwiązanie można otrzymać najprościej chyba powołując się na zasadę względności Galileusza.
Za pomocą transformacji $x_G = x + V t$, gdzie
- $x_G$ - nowe poruszające się współrzędne,
- $V$ - stała prędkość, z którą porusza się układ $x_G$,

można już łatwo obliczyć łączne przesunięcie łódki.
