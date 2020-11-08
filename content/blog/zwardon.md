---
title: "Zwardoń"
date: 2020-05-20T10:03:39+02:00
draft: false
tags: [liceum, matematyka, kinematyka]
---
# Zadanie
Ze Zwardonia do odległej o $15$ km Milówki wyruszył pieszo turysta. Godzinę później, z Milówki do Zwardonia wyjechał samochód, który minął turystę po $15$ minutach jazdy. Po półgodzinnym postoju w Zwardoniu, kierowca ruszył w drogę powrotną. Po raz kolejny minął turystę zmierzającego do Milówki po $50$ minutach od ich ostatniego spotkania. Oblicz, ile czasu zajęła turyście droga ze Zwardonia do Milówki. Przyjmij, że turysta przeszedł całą drogę ze stałym tempem, a kierowca jechał w obie strony ze stałą prędkością.
![](/zwardon.png)
# Rozwiązanie
Niech położenie turysty od czasu - $\tau(t)$, położenie samochodu od czasu - $s(t)$. W oznaczeniach takich jak na rysunku, można przedstawić te funkcje następująco
$$ \begin{align*}
\tau(t) &= v_{\tau} t \cr
s(t) &= \begin{cases}M - v_s(t-t_0) & t < T \cr
0 & t\in [T, T + t_{p_s}] \cr
v_s(t-t_1) & t > T + t_{p_s}.\end{cases}
\end{align*} $$
Z treści zadania wynika, że nastąpiły dwa spotkania samochodu i turysty. Znamy ich położenia w czasie - odpowiednio $t_{p_1} = 60 + 15$ min oraz $t_{p_2} = 60 + 15 + 50$ min.
Jako, że podczas spotkania i turysta i samochód zajmują to samo położenie w przestrzeni, można zapisać
$$\begin{align*}
x_{p_1} &= v_\tau t_{p_1} = M - v_s(t_{p_1} - t_0), \cr
x_{p_2} &= v_\tau t_{p_2} = v_s(t_{p_2} - t_1).
\end{align*}$$
Poza tym, można zapisać związek między prędkością samochodu a czasem pomiędzy spotkaniami:
$$\frac{x_{p_1}}{v_s} + t_{p_s} + \frac{x_{p_2}}{v_s} = t_{p_2} - t_{p_1}.$$
Po odrzuceniu równości zawierającej wyraz $v_s t_1$, otrzymujemy układ czterech równań na cztery niewiadome ($x_{p_1}, x_{p_2},v_\tau, v_s$).
Można zapisać go na przykład w postaci równania macierzowego
$$\begin{bmatrix}x_{p_1}\cr x_{p_2}\cr v_s\cr v_\tau\end{bmatrix} \begin{bmatrix}
1&1&t_{p_1} + t_{p_s} - t_{p_2}& 0\cr
1&0&t_{p_1} - t_0& 0\cr
0&1&0&-t_{p_2}\cr
1&0&0&-t_{p_1}
\end{bmatrix} =
\begin{bmatrix} 0\cr M\cr 0\cr 0\end{bmatrix}.$$
Jeżeli odwrócimy tę macierz, dostaniemy bardzo łatwo wszystkie niewiadome. Naszym zadaniem jest obliczenie czasu potrzebnego turyście do przejścia drogi między Zwardoniem i Milówką. Jest to po prostu $t = M/v_\tau$. Macierz odwrócimy metodą dopełnień algebraicznych, czyli za pomocą zależności między macierzą odwrotną ($A^{-1}$), macierzą dołączoną ($A^D$) i wyznacznikiem macierzy ($\det A$),
$$A^{-1} = \frac{A^D}{\det A}.$$
Macierz dołączona jest po prostu transponowaną macierzą dopełnień algebraicznych.
Wyznacznik obliczymy korzystając z rozwinięcia Laplace'a.
Rozwiniemy wokół czwartego wiersza.
$$\begin{align*}
\det A &= (-1)^{4+1} \cdot 1 \cdot
\begin{vmatrix}
1&t_{p_1} + t_{p_s} - t_{p_2}&0\cr
0&t_{p_1} - t_0&0\cr
1&0&-t_{p_2}
\end{vmatrix} + (-1)^{4+4} \cdot (-t_{p_1}) \begin{vmatrix}
1&1&t_{p_1}+t_{p_s} - t_{p_2}\cr
1&0&t_{p_1} - t_0\cr
0&1&0
\end{vmatrix} = \cr
&= (-1)(-t_{p_2})(t_{p_1} - t_0) + (-t_{p_1})(t_0 - t_{p_1}) - t_{p_1}(t_{p_1} + t_{p_s} - t_{p_2}) = \cr
&= -t_0(t_{p_1} + t_{p_2}) + t_{p_1}(2t_{p_2} - t_{p_s}).
\end{align*}$$
Po wstawieniu do wzoru dostaniemy wektor
$$\begin{bmatrix}
x_{p_1} \cr x_{p_2} \cr v_s \cr v_\tau
\end{bmatrix} =
\begin{bmatrix}
-\frac{M t_{p_1} (t_{p_1} - t_{p_2} + t_{p_s})}{-t_0 t_{p_1} - t_0 t_{p_2} + 2 t_{p_1} t_{p_2} - t_{p_1} t_{p_s}} \cr
\frac{M t_{p_2} (-t_{p_1} + t_{p_2} - t_{p_s})}{-t_0 t_{p_1} - t_0 t_{p_2} + 2 t_{p_1} t_{p_2} - t_{p_1} t_{p_s}}\cr
-\frac{M(t_{p_1} + t_{p_2})}{t_0 t_{p_1} + t_0 t_{p_2} - 2 t_{p_1} t_{p_2} + t_{p_1} t_{p_s}}\cr
-\frac{M(t_{p_1} - t_{p_2} + t_{p_s})}{t_0 t_{p_1} + t_0 t_{p_2} - 2 t_{p_1} t_{p_2}+t_{p_1}t_{p_s}}
\end{bmatrix}.$$
Możemy podstawić liczby z zadania, dostaniemy
$$\begin{bmatrix}
x_{p_1} \cr x_{p_2} \cr v_s \cr v_\tau
\end{bmatrix} =
\begin{bmatrix}
5\cr \frac{25}{3}\cr \frac{2}{3}\cr \frac{1}{15}
\end{bmatrix}
$$
Jednostki prędkości tutaj mamy w $\frac{\text{km}}{\text{min}}$, więc ostatecznie, czas podróży turysty wynosi
$$t = \frac{M}{v_\tau} = 225 \text{minut} = 3 \text{h }45 \text{minut}.$$
