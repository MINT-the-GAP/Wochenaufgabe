<!--
version:  0.0.1

language: de

@style
main > *:not(:last-child) {
  margin-bottom: 3rem;
}

input {
    text-align: center;
}

.flex-container {
    display: flex;
    flex-wrap: wrap;
    align-items: stretch;
    gap: 20px;
}

.flex-child {
    flex: 1;
    min-width: 350px;
    margin-right: 20px;
}

@media (max-width: 400px) {
    .flex-child {
        flex: 100%;
        margin-right: 0;
    }
}
@end

formula: \carry   \textcolor{red}{\scriptsize #1}
formula: \digit   \rlap{\carry{#1}}\phantom{#2}#2
formula: \permil  \text{‰}

import: https://raw.githubusercontent.com/liaTemplates/algebrite/master/README.md
import: https://raw.githubusercontent.com/LiaTemplates/Tikz-Jax/main/README.md
import: https://raw.githubusercontent.com/LiaTemplates/mermaid_template/0.1.4/README.md

script: https://cdn.jsdelivr.net/gh/LiaTemplates/Tikz-Jax@main/dist/index.js

@round
<script>
  let value = `@input`;
  if (value.startsWith("@")) {
    ""
  } else {
    value = JSON.parse(value);
    value = value[0]
    value = value.replace(/,/g, ".");
    value = parseFloat(value);
    value = Math.round(value * Math.pow(10,@1)) / Math.pow(10,@1);
    value == @0
  }
</script>
@end

-->

# Probeklassenarbeit für Mathematik - Klasse 8: Umgang mit Gleichungen

<br>

> Letztes Update am 04.11.2025 gegen 18 Uhr

<br>

Swipe (Wische) entweder weiter oder klicke unten links auf neben der Seitenzahl auf den Pfeil nach rechts.

<br>

Diese Probearbeit hat mehr Aufgaben als die richtige Arbeit, damit du genug zum Üben hast. Es sind viele verschiedene Aufgabentypen abgebildet, sodass du alles nochmal bei der Bearbeitung dieser Aufgaben wiederholst.

## Aufgabe 1 - Äquivalenzumformung

<div class="flex-child">
<!-- data-solution-button="5"-->
__$a)\;\;$__ $ \; 9x - \dfrac{3}{4} = 5x + \dfrac{9}{4} \;$ \
$x$ = [[  3/4  ]]
@Algebrite.check(3/4)
************
$$
\begin{align*}
9x - \dfrac{3}{4} &= 5x + \dfrac{9}{4} \quad \left| -5x \right. \\
4x - \dfrac{3}{4} &= \dfrac{9}{4} \quad \left| +\dfrac{3}{4} \right. \\
4x &= \dfrac{12}{4} = 3 \quad \left| :4 \right. \\
x &= \dfrac{3}{4}
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$b)\;\;$__ $ \; 3x + \dfrac{5}{2} = \dfrac{1}{2}x - 4 \;$ \
$x$ = [[  -13/5  ]]
@Algebrite.check(-13/5)
************
$$
\begin{align*}
3x + \dfrac{5}{2} &= \dfrac{1}{2}x - 4 \quad \left| -\dfrac{1}{2}x \right. \\
\left(3-\dfrac{1}{2}\right)x + \dfrac{5}{2} &= -4 \\
\dfrac{5}{2}x + \dfrac{5}{2} &= -4 \quad \left| -\dfrac{5}{2} \right. \\
\dfrac{5}{2}x &= -\dfrac{13}{2} \quad \left| :\dfrac{5}{2} \right. \\
x &= -\dfrac{13}{5}
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$c)\;\;$__ $  \; \dfrac{2}{3}x + 4 = \dfrac{5}{6}x - 2 \;$ \
$x$ = [[  36  ]]
@Algebrite.check(36)
************
$$
\begin{align*}
\dfrac{2}{3}x + 4 &= \dfrac{5}{6}x - 2 \quad \left| -\dfrac{5}{6}x \right. \\
\left(\dfrac{2}{3}-\dfrac{5}{6}\right)x + 4 &= -2 \\
-\dfrac{1}{6}x + 4 &= -2 \quad \left| -4 \right. \\
-\dfrac{1}{6}x &= -6 \quad \left| :\left(-\dfrac{1}{6}\right) \right. \\
x &= 36
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$d)\;\;$__ $ \; 3x - 7 = \dfrac{5}{2}x + 2 \;$ \
$x$ = [[  18  ]]
@Algebrite.check(18)
************
$$
\begin{align*}
3x - 7 &= \dfrac{5}{2}x + 2 \quad \left| -\dfrac{5}{2}x \right. \\
\left(3-\dfrac{5}{2}\right)x - 7 &= 2 \\
\dfrac{1}{2}x - 7 &= 2 \quad \left| +7 \right. \\
\dfrac{1}{2}x &= 9 \quad \left| :\dfrac{1}{2} \right. \\
x &= 18
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$e)\;\;$__ $ \; 3\left(x + \dfrac{2}{3}\right) - \dfrac{1}{2} = \dfrac{7}{3}x + \dfrac{5}{6} \;$ \
$x$ = [[  -1  ]]
@Algebrite.check(-1)
************
$$
\begin{align*}
3\!\left(x + \dfrac{2}{3}\right) - \dfrac{1}{2} &= \dfrac{7}{3}x + \dfrac{5}{6} \\
3x + 2 - \dfrac{1}{2} &= \dfrac{7}{3}x + \dfrac{5}{6} \\
3x + \dfrac{3}{2} &= \dfrac{7}{3}x + \dfrac{5}{6} \quad \left| -\dfrac{7}{3}x \right. \\
\left(3-\dfrac{7}{3}\right)x + \dfrac{3}{2} &= \dfrac{5}{6} \\
\dfrac{2}{3}x + \dfrac{3}{2} &= \dfrac{5}{6} \quad \left| -\dfrac{3}{2} \right. \\
\dfrac{2}{3}x &= -\dfrac{4}{6} = -\dfrac{2}{3} \quad \left| :\dfrac{2}{3} \right. \\
x &= -1
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$f)\;\;$__ $ \; \dfrac{8}{x-1} = \dfrac{12}{2x+5} \;$ \
$x$ = [[  -13  ]]
************
$$
\begin{align*}
\dfrac{8}{x-1} &= \dfrac{12}{2x+5} \quad \left| \cdot(x-1)(2x+5) \right. \\
8\,(2x+5) &= 12\,(x-1) \\
16x + 40 &= 12x - 12 \quad \left| -12x \right. \\
4x + 40 &= -12 \quad \left| -40 \right. \\
4x &= -52 \quad \left| :4 \right. \\
x &= -13 \qquad 
\end{align*}
$$
************
</div>





## Aufgabe 2 - Ungleichungen


**Berechne** den gesuchten Wert innerhalb der Lösungsmenge, die die Ungleichung beschreibt.


<div class="flex-child">
__$a)\;\;$__ $\dfrac{3}{4}x - 2 < \dfrac{1}{3}x - \dfrac{1}{6}$

<!-- data-solution-button="5"-->
$\mathbb{L} = \left\{ x \in \mathbb{Q} \,\right|\, x < $ [[ 22/5 ]] $\left. \right\}$
@Algebrite.check(22/5)
******************
$$
\begin{align*}
\dfrac{3}{4}x - 2 &< \dfrac{1}{3}x - \dfrac{1}{6} \quad \left| \;-\dfrac{1}{3}x \right. \\
\left(\dfrac{3}{4}-\dfrac{1}{3}\right)x - 2 &< -\dfrac{1}{6} \\
\dfrac{5}{12}x - 2 &< -\dfrac{1}{6} \quad \left| \;+2 \right. \\
\dfrac{5}{12}x &< \dfrac{11}{6} \quad \left| \;\cdot \dfrac{12}{5} \right. \\
x &< \dfrac{22}{5}
\end{align*}
$$
******************
</div>

<div class="flex-child">
__$b)\;\;$__ $-\dfrac{2}{5}x + \dfrac{7}{3} \ge \dfrac{1}{5}x + 1$

<!-- data-solution-button="10"-->
$\mathbb{L} = \left\{ x \in \mathbb{R} \,\right|\, x \le $ [[ 20/9 ]] $\left. \right\}$
@Algebrite.check(20/9)
******************
$$
\begin{align*}
-\dfrac{2}{5}x + \dfrac{7}{3} &\ge \dfrac{1}{5}x + 1 \quad \left| \;+\dfrac{2}{5}x \right. \\
\dfrac{7}{3} &\ge \dfrac{3}{5}x + 1 \quad \left| \;-1 \right. \\
\dfrac{4}{3} &\ge \dfrac{3}{5}x \quad \left| \;\cdot \dfrac{5}{3} \right. \\
x &\le \dfrac{20}{9}
\end{align*}
$$
******************
</div>

<div class="flex-child">
__$c)\;\;$__ $-\dfrac{3}{4}x + 5 < \dfrac{1}{2}x + 1$

<!-- data-solution-button="20"-->
$\mathbb{L} = \left\{ x \in \mathbb{Z} \,\right|\, x \ge $ [[ 4 ]] $\left. \right\}$
@Algebrite.check(4)
******************
$$
\begin{align*}
-\dfrac{3}{4}x + 5 &< \dfrac{1}{2}x + 1 \quad \left| \;+\dfrac{3}{4}x \right. \\
5 &< \left(\dfrac{1}{2}+\dfrac{3}{4}\right)x + 1 \\
5 &< \dfrac{5}{4}x + 1 \quad \left| \;-1 \right. \\
4 &< \dfrac{5}{4}x \quad \left| \;\cdot \dfrac{4}{5} \right. \\
x &> \dfrac{16}{5} \;\;\Rightarrow\;\; x \ge 4 \text{ für } \mathbb{Z}
\end{align*}
$$
******************
</div>

<div class="flex-child">
__$d)\;\;$__ $\dfrac{5}{6}x - 2 \le \dfrac{1}{3} - \dfrac{1}{2}x$

<!-- data-solution-button="50"-->
$\mathbb{L} = \left\{ x \in \mathbb{Z} \,\right|\, x \le $ [[ 1 ]] $\left. \right\}$
@Algebrite.check(1)
******************
$$
\begin{align*}
\dfrac{5}{6}x - 2 &\le \dfrac{1}{3} - \dfrac{1}{2}x \quad \left| \;+\dfrac{1}{2}x \right. \\
\left(\dfrac{5}{6}+\dfrac{1}{2}\right)x - 2 &\le \dfrac{1}{3} \\
\dfrac{4}{3}x - 2 &\le \dfrac{1}{3} \quad \left| \;+2 \right. \\
\dfrac{4}{3}x &\le \dfrac{7}{3} \quad \left| \;\cdot \dfrac{3}{4} \right. \\
x &\le \dfrac{7}{4} \;\;\Rightarrow\;\; x \le 1 \text{ für } \mathbb{Z}
\end{align*}
$$
******************
</div>

<div class="flex-child">
__$e)\;\;$__ $\dfrac{2}{5}x + 3 > \dfrac{7}{5} - \dfrac{3}{5}x$

<!-- data-solution-button="50"-->
$\mathbb{L} = \left\{ x \in \mathbb{Q} \,\right|\, x > $ [[ -8/5 ]] $\left. \right\}$
@Algebrite.check(-8/5)
******************
$$
\begin{align*}
\dfrac{2}{5}x + 3 &> \dfrac{7}{5} - \dfrac{3}{5}x \quad \left| \;+\dfrac{3}{5}x \right. \\
\dfrac{5}{5}x + 3 &> \dfrac{7}{5} \quad \left| \;-3 \right. \\
x &> \dfrac{7}{5} - 3 = -\dfrac{8}{5}
\end{align*}
$$
******************
</div>

<div class="flex-child">
__$f)\;\;$__ $-\dfrac{3}{2}x + \dfrac{1}{2} \ge \dfrac{1}{4}x - 3$

<!-- data-solution-button="50"-->
$\mathbb{L} = \left\{ x \in \mathbb{R} \,\right|\, x \le $ [[ 2 ]] $\left. \right\}$
@Algebrite.check(2)
******************
$$
\begin{align*}
-\dfrac{3}{2}x + \dfrac{1}{2} &\ge \dfrac{1}{4}x - 3 \quad \left| \;-\dfrac{1}{4}x \right. \\
-\left(\dfrac{3}{2}+\dfrac{1}{4}\right)x + \dfrac{1}{2} &\ge -3 \\
-\dfrac{7}{4}x + \dfrac{1}{2} &\ge -3 \quad \left| \;-\dfrac{1}{2} \right. \\
-\dfrac{7}{4}x &\ge -\dfrac{7}{2} \quad \left| \;:\left(-\dfrac{7}{4}\right) \right. \\
x &\le 2
\end{align*}
$$
******************
</div>



## Aufgabe 3 - Gleichungssysteme




<!-- data-solution-button="5"-->
__$a)\;\;$__  
$$
\begin{align*}
I.& \qquad 3x + y = 10 \\  
II.& \qquad x + 2y = 10
\end{align*}
$$  
$x$ = [[  2  ]]  und  $y$ = [[  4  ]]
************
$$
\begin{align*}
I. &\qquad 3x + y = 10 \quad \left| -3x \right. \\
II. &\qquad x + 2y = 10 \\ \hline
I. &\qquad y = 10 - 3x \\
I. \cap II. &\qquad x + 2(10 - 3x) = 10 \\
&\qquad x + 20 - 6x = 10 \quad \left| -20 \right. \\
&\qquad -5x = -10 \quad \left| :(-5) \right. \\
&\qquad x = 2 \\
x \cap I. &\qquad 3\cdot 2 + y = 10 \\
&\qquad 6 + y = 10 \quad \left| -6 \right. \\
&\qquad y = 4
\end{align*}
$$
************

---

---



<!-- data-solution-button="5"-->
__$b)\;\;$__  
$$
\begin{align*}
I.& \qquad 2x + y = 13 \\  
II.& \qquad x + 2y = 17
\end{align*}
$$  
$x$ = [[  3  ]]  und  $y$ = [[  7  ]]
************
$$
\begin{align*}
I. &\qquad 2x + y = 13 \quad \left| -2x \right. \\
II. &\qquad x + 2y = 17 \\ \hline
I. &\qquad y = 13 - 2x \\
I. \cap II. &\qquad x + 2(13 - 2x) = 17 \\
&\qquad x + 26 - 4x = 17 \quad \left| -26 \right. \\
&\qquad -3x = -9 \quad \left| :(-3) \right. \\
&\qquad x = 3 \\
x \cap I. &\qquad 2\cdot 3 + y = 13 \\
&\qquad 6 + y = 13 \quad \left| -6 \right. \\
&\qquad y = 7
\end{align*}
$$
************

---

---



<!-- data-solution-button="5"-->
__$c)\;\;$__  
$$
\begin{align*}
I.& \qquad 5x - y = 19 \\  
II.& \qquad 2x + 3y = 11
\end{align*}
$$  
$x$ = [[  4  ]]  und  $y$ = [[  1  ]]
************
$$
\begin{align*}
I. &\qquad 5x - y = 19 \quad \left| -5x \right. \\
II. &\qquad 2x + 3y = 11 \\ \hline
I. &\qquad -y = 19 - 5x \quad \Rightarrow \quad y = 5x - 19 \\
I. \cap II. &\qquad 2x + 3(5x - 19) = 11 \\
&\qquad 2x + 15x - 57 = 11 \quad \left| +57 \right. \\
&\qquad 17x = 68 \quad \left| :17 \right. \\
&\qquad x = 4 \\
x \cap I. &\qquad 5\cdot 4 - y = 19 \\
&\qquad 20 - y = 19 \quad \left| -20 \right. \\
&\qquad -y = -1 \quad \Rightarrow \quad y = 1
\end{align*}
$$
************





---

---


<!-- data-solution-button="5"-->
__$d)\;\;$__  
$$
\begin{align*}
I.& \qquad 2x + y + z = 5 \\  
II.& \qquad x - 2y + 3z = 0 \\  
III.& \qquad 4x + y - z = -3
\end{align*}
$$  
$x$ = [[  -1  ]], $y$ = [[  4  ]], $z$ = [[  3  ]]
************
$$
\begin{align*}
I.& \; 2x + y + z = 5 \\
II.& \; x - 2y + 3z = 0 \\
III.& \; 4x + y - z = -3 \\ \hline
\text{Aus } I:& \; y = 5 - 2x - z \\
\text{In } II:& \; x - 2(5 - 2x - z) + 3z = 0 \\
& \; x - 10 + 4x + 2z + 3z = 0 \\
& \; 5x + 5z = 10 \quad \Rightarrow \quad x + z = 2 \quad (A) \\
\text{In } III:& \; 4x + (5 - 2x - z) - z = -3 \\
& \; 2x + 5 - 2z = -3 \\
& \; x - z = -4 \quad (B) \\ \hline
(A)+(B):& \; (x+z) + (x - z) = 2 + (-4) \Rightarrow 2x = -2 \Rightarrow x = -1 \\
& \; z = 2 - x = 3 \\
\text{In } I:& \; 2(-1) + y + 3 = 5 \Rightarrow y = 4
\end{align*}
$$
************




---

---




<!-- data-solution-button="5"-->
__$e)\;\;$__  
$$
\begin{align*}
I.& \qquad x + y + z = 5 \\  
II.& \qquad 2x - y + z = 13 \\  
III.& \qquad 3x + 2y - z = 5
\end{align*}
$$  
$x$ = [[  4  ]], $y$ = [[  -2  ]], $z$ = [[  3  ]]
************
$$
\begin{align*}
I.& \; x + y + z = 5 \\
II.& \; 2x - y + z = 13 \\
III.& \; 3x + 2y - z = 5 \\ \hline
(I)+(III):& \; (x+3x) + (y+2y) + (z - z) = 5 + 5 \\
& \; 4x + 3y = 10 \quad (A) \\
(II)+(III):& \; (2x+3x) + (-y+2y) + (z - z) = 13 + 5 \\
& \; 5x + y = 18 \quad (B) \\ \hline
3\cdot(B) - (A):& \; (15x + 3y) - (4x + 3y) = 54 - 10 \\
& \; 11x = 44 \Rightarrow x = 4 \\
\text{In } (B):& \; 5\cdot 4 + y = 18 \Rightarrow y = -2 \\
\text{In } I:& \; 4 + (-2) + z = 5 \Rightarrow z = 3
\end{align*}
$$
************








## Aufgabe 4 - Textaufgaben - Äquivalenzumformung

__$a)\;\;$__ Zwei Zisternen ändern ihren Füllstand gleichmäßig:  
Zisterne A hat anfangs $120$ cm Wasser und verliert pro Stunde $2{,}5$ cm.  
Zisterne B hat anfangs $60$ cm und gewinnt pro Stunde $5$ cm (Zulauf).  
**Berechne**, nach wie vielen Stunden beide Zisternen den gleichen Füllstand haben.

<!-- data-solution-button="5"-->
$x$ = [[ 8 ]]
@Algebrite.check(8)
************
$$
\textbf{Gleichung aus dem Text:}\quad 
120 - 2{,}5x \;\stackrel{!}{=}\; 60 + 5x
$$

$$
\begin{align*}
120 - 2{,}5x &= 60 + 5x \quad \left|\, -60 \right.\\[2pt]
60 - 2{,}5x &= 5x \quad \left|\, +2{,}5x \right.\\[2pt]
60 &= 7{,}5x \quad \left|\, :7{,}5 \right.\\[2pt]
x &= 8
\end{align*}
$$

Deutung: Nach $8$ Stunden sind die Füllstände gleich.
************

---

---




__$b)\;\;$__ Zwei Personen sparen mit linearem Zuwachs:  
Plan A startet bei $150\,€$ und steigt pro Woche um $9\,€$.  
Plan B startet bei $318\,€$ und steigt pro Woche um $3\,€$.  
**Berechne**, nach wie vielen Wochen beide Kontostände gleich sind.

<!-- data-solution-button="5"-->
$x$ = [[ 28 ]]
@Algebrite.check(28)
************
$$
\textbf{Gleichung aus dem Text:}\quad 
150 + 9x \;\stackrel{!}{=}\; 318 + 3x
$$

$$
\begin{align*}
150 + 9x &= 318 + 3x \quad \left|\, -150 \right.\\[2pt]
9x &= 168 + 3x \quad \left|\, -3x \right.\\[2pt]
6x &= 168 \quad \left|\, :6 \right.\\[2pt]
x &= 28
\end{align*}
$$

Deutung: Nach $28$ Wochen sind die Kontostände gleich.
************



---

---



__$c)\;\;$__ Zwei Freundinnen schauen dieselbe Serie auf unterschiedlichen Ständen:  
Person A startet bei Folge $5$ und schaut pro Woche $3$ Folgen.  
Person B startet bei Folge $20$ und schafft pro Woche $1$ Folge.  
**Berechne**, nach wie vielen Wochen beide bei derselben Folgennummer sind.

<!-- data-solution-button="5"-->
$x$ = [[ 15/2 ]]
@Algebrite.check(15/2)
************
$$
\textbf{Gleichung aus dem Text:}\quad 
5 + 3x \;\stackrel{!}{=}\; 20 + 1\cdot x
$$

$$
\begin{align*}
5 + 3x &= 20 + x \quad \left|\, -5 \right.\\[2pt]
3x &= 15 + x \quad \left|\, -x \right.\\[2pt]
2x &= 15 \quad \left|\, :2 \right.\\[2pt]
x &= \dfrac{15}{2}
\end{align*}
$$

Deutung: Nach $\dfrac{15}{2}=7{,}5$ Wochen sind beide gleichauf.
************



---

---



__$d)\;\;$__ Zwei Schüler lesen dasselbe Buch:  
Schüler A hat bereits $40$ Seiten gelesen und liest täglich $18$ Seiten.  
Schüler B hat bereits $120$ Seiten gelesen und liest täglich $6$ Seiten.  
**Berechne**, nach wie vielen Tagen beide die gleiche Seitenzahl erreicht haben.

<!-- data-solution-button="5"-->
$x$ = [[ 20/3 ]]
@Algebrite.check(20/3)
************
$$
\textbf{Gleichung aus dem Text:}\quad 
40 + 18x \;\stackrel{!}{=}\; 120 + 6x
$$

$$
\begin{align*}
40 + 18x &= 120 + 6x \quad \left|\, -40 \right.\\[2pt]
18x &= 80 + 6x \quad \left|\, -6x \right.\\[2pt]
12x &= 80 \quad \left|\, :12 \right.\\[2pt]
x &= \dfrac{20}{3}
\end{align*}
$$

Deutung: Nach $\dfrac{20}{3}\approx 6{,}7$ Tagen sind beide auf derselben Seite.
************




---

---

__$e)\;\;$__ Ein Artikelbestand ändert sich linear:  
Filiale A hat $260$ Stück und verkauft täglich $8$ Stück.  
Filiale B hat $80$ Stück und erhält täglich $12$ Stück nachgeliefert.  
**Berechne**, nach wie vielen Tagen beide Filialen gleich viele Stück auf Lager haben.

<!-- data-solution-button="5"-->
$x$ = [[ 9 ]]
@Algebrite.check(9)
************
$$
\textbf{Gleichung aus dem Text:}\quad 
260 - 8x \;\stackrel{!}{=}\; 80 + 12x
$$

$$
\begin{align*}
260 - 8x &= 80 + 12x \quad \left|\, -80 \right.\\[2pt]
180 - 8x &= 12x \quad \left|\, +8x \right.\\[2pt]
180 &= 20x \quad \left|\, :20 \right.\\[2pt]
x &= 9
\end{align*}
$$

Deutung: Nach $9$ Tagen sind die Bestände gleich.
************


---

---

__$f)\;\;$__ Zwei Sektoren eines Stadions füllen sich bzw. leeren sich linear:  
Sektor A startet mit $140$ Personen und es kommen pro Minute $12$ hinzu.  
Sektor B startet mit $332$ Personen und es gehen pro Minute $8$ hinaus.  
**Berechne**, nach wie vielen Minuten beide Sektoren gleich viele Personen enthalten.

<!-- data-solution-button="5"-->
$x$ = [[ 48/5 ]]
@Algebrite.check(48/5)
************
$$
\textbf{Gleichung aus dem Text:}\quad 
140 + 12x \;\stackrel{!}{=}\; 332 - 8x
$$

$$
\begin{align*}
140 + 12x &= 332 - 8x \quad \left|\, -140 \right.\\[2pt]
12x &= 192 - 8x \quad \left|\, +8x \right.\\[2pt]
20x &= 192 \quad \left|\, :20 \right.\\[2pt]
x &= \dfrac{192}{20} \;=\; \dfrac{48}{5}
\end{align*}
$$

Deutung: Nach $\dfrac{48}{5}=9{,}6$ Minuten sind die Personenzahlen gleich.
************



## Aufgabe 5 - Textaufgaben - Ungleichungen




__$a)\;\;$__ Für eine Klassenarbeit sind bereits 15 Kopien vorhanden. Ein Zusatzpaket enthält jeweils 8 Kopien.  
**Berechne** die kleinste natürliche Zahl $x$ (Zusatzpakete), sodass insgesamt mindestens $95$ Kopien vorliegen.

<!-- data-solution-button="5"-->
$\mathbb{L} = \{ x \in \mathbb{N} \;|\; x \geq $ [[ 10 ]] $\}$
@Algebrite.check(10)
******************
$$
\begin{align*}
15 + 8x &\ge 95 \\
8x &\ge 95-15 = 80 \quad \left|\, :8 \right. \\
x &\ge 10
\end{align*}
$$
******************

---

---




__$b)\;\;$__ Für das Fliesenlegen sind 7 Reservefliesen vorhanden. Jede zusätzliche Schachtel enthält 18 Fliesen.  
**Berechne** die kleinste natürliche Zahl $x$ (Schachteln), sodass insgesamt mindestens 250 Fliesen zur Verfügung stehen.

<!-- data-solution-button="5"-->
$\mathbb{L} = \{ x \in \mathbb{N} \;|\; x \geq $ [[ 14 ]] $\}$
@Algebrite.check(14)
******************
$$
\begin{align*}
7 + 18x &\ge 250 \\
18x &\ge 243 \quad \left|\, :18 \right. \\
x &\ge \dfrac{243}{18} = 13{,}5 \;\Rightarrow\; x \ge 14 \text{ für } \mathbb{N}
\end{align*}
$$
******************


---

---



__$c)\;\;$__ Für ein Festival sind bereits 56 Armbänder vorhanden. Jede Lieferung bringt 25 weitere Armbänder.  
**Berechne** die kleinste natürliche Zahl $x$ (Lieferungen), damit mindestens 600 Armbänder verfügbar sind.

<!-- data-solution-button="5"-->
$\mathbb{L} = \{ x \in \mathbb{N} \;|\; x \geq $ [[ 22 ]] $\}$
@Algebrite.check(22)
******************
$$
\begin{align*}
56 + 25x &\ge 600 \\
25x &\ge 544 \quad \left|\, :25 \right. \\
x &\ge 21{,}76 \;\Rightarrow\; x \ge 22 \text{ für } \mathbb{N}
\end{align*}
$$
******************


---

---



__$d)\;\;$__ Ein Spendenlauf hat bereits $320\,\text{€}$ eingebracht. Pro verkauftem Ticket kommen $\dfrac{25}{2}\,\text{€}$ hinzu.  
**Berechne** die kleinste natürliche Zahl $x$ (verkaufte Tickets), um mindestens $1000\,\text{€}$ zu erreichen.

<!-- data-solution-button="5"-->
$\mathbb{L} = \{ x \in \mathbb{N} \;|\; x \geq $ [[ 55 ]] $\}$
@Algebrite.check(55)
******************
$$
\begin{align*}
320 + \dfrac{25}{2}x &\ge 1000 \\
\dfrac{25}{2}x &\ge 680 \quad \left|\, \cdot \dfrac{2}{25} \right. \\
x &\ge \dfrac{1360}{25} = 54{,}4 \;\Rightarrow\; x \ge 55 \text{ für } \mathbb{N}
\end{align*}
$$
******************


---

---



__$e)\;\;$__ Auf einem Tablet sind noch $8\,\text{GB}$ frei. Jede Bereinigung schafft zusätzlich $\dfrac{6}{5}\,\text{GB}$ Platz.  
**Berechne** die kleinste natürliche Zahl $x$ (Bereinigungen), damit mindestens $20\,\text{GB}$ frei sind.

<!-- data-solution-button="5"-->
$\mathbb{L} = \{ x \in \mathbb{N} \;|\; x \geq $ [[ 10 ]] $\}$
@Algebrite.check(10)
******************
$$
\begin{align*}
8 + \dfrac{6}{5}x &\ge 20 \\
\dfrac{6}{5}x &\ge 12 \quad \left|\, \cdot \dfrac{5}{6} \right. \\
x &\ge 10
\end{align*}
$$
******************



---

---





__$f)\;\;$__ Ein Cloud-Konto hat maximal $200$ GB Speicher. Bereits belegt sind $112$ GB. Jedes neue Backup benötigt im Durchschnitt $\dfrac{35}{3}$ GB (durch variable Datenmengen).  
**Berechne** die Anzahl der Backups $x$, sodass die Kapazität überschritten wird.

<!-- data-solution-button="5"-->
$\mathbb{L} = \{ x \in \mathbb{N} \;|\; x \geq $ [[ 8 ]] $\}$
@Algebrite.check(8)
******************
$$
\begin{align*}
112 + \dfrac{35}{3}x &> 200 \quad \left| \; -112 \; \right. \\
\dfrac{35}{3}x &> 88 \quad \left| \; :\dfrac{35}{3} \; \right. \\
x &> \dfrac{264}{35} \\[4pt]
\Rightarrow\;\; \mathbb{N}\text{:}\quad x &\ge 8
\end{align*}
$$
******************



---

---



__$g)\;\;$__ Ein Fachbereich verfügt über ein maximales Budget von $3000\,€$. Bereits verplant sind $1260\,€$. Jede zusätzliche AG-Förderung kostet im Durchschnitt $\dfrac{621}{4}\,€$.  
**Berechne** die Anzahl der zusätzlichen AG-Förderungen $x$, sodass das Budget überschritten wird.

<!-- data-solution-button="5"-->
$\mathbb{L} = \{ x \in \mathbb{N} \;|\; x \geq $ [[ 12 ]] $\}$
@Algebrite.check(12)
******************
$$
\begin{align*}
1260 + \dfrac{621}{4}x &> 3000 \quad \left| \; -1260 \; \right. \\
\dfrac{621}{4}x &> 1740 \quad \left| \; :\dfrac{621}{4} \; \right. \\
x &> \dfrac{6960}{621} \\[4pt]
\Rightarrow\;\; \mathbb{N}\text{:}\quad x &\ge 12
\end{align*}
$$
******************

















## Aufgabe 6 - Textaufgaben - Gleichungssysteme







<!-- data-solution-button="5"-->
__$a)\;\;$__  
Ein Bäcker teilt seinen 8-Stunden-Tag auf zwei Öfen auf. Ofen A liefert 30 Stück pro Stunde, Ofen B 45 Stück pro Stunde. Insgesamt produziert er 325 Stück.  
**Berechne** die Arbeitszeiten an Ofen A ($x$) und Ofen B ($y$).

$x$ = [[  7/3  ]] und $y$ = [[  17/3  ]]
@Algebrite.check([ 7/3; 17/3 ])
************
Bezeichne mit $x$ die Zeit an Ofen A (h) und mit $y$ die Zeit an Ofen B (h).
$$
\begin{align*}
I.& \qquad x + y = 8 \\
II.& \qquad 30x + 45y = 325 \\ \hline
30\cdot I\!:& \qquad 30x + 30y = 240 \\ \hline
II - (30\cdot I)\!:& \qquad (30x + 45y) - (30x + 30y) = 325 - 240 \\
& \qquad 15y = 85 \;\Rightarrow\; y = \dfrac{85}{15} = \dfrac{17}{3} \\[6pt]
x \cap I\!:& \qquad x + \dfrac{17}{3} = 8 
\;\Rightarrow\; x = 8 - \dfrac{17}{3} 
= \dfrac{24 - 17}{3} 
= \dfrac{7}{3}
\end{align*}
$$
Die Arbeitszeiten betragen $ \dfrac{7}{3}\,\text{h}$ (Ofen A) und $ \dfrac{17}{3}\,\text{h}$ (Ofen B).
************


---

---


<!-- data-solution-button="5"-->
__$b)\;\;$__  
Zwei Drucker übernehmen nacheinander Teile eines Auftrags innerhalb eines 6-Stunden-Fensters.  
Drucker A (Zeit $x$) schafft 90 Seiten pro Stunde, Drucker B (Zeit $y$) 120 Seiten pro Stunde. Insgesamt werden 645 Seiten gedruckt.  
**Berechne** die Einsatzzeiten $x$ und $y$.

$x$ = [[  5/2  ]] und $y$ = [[  7/2  ]]
@Algebrite.check([ 5/2; 7/2 ])
************
$$
\begin{align*}
I.& \qquad x + y = 6 \\
II.& \qquad 90x + 120y = 645 \\ \hline
90\cdot I\!:& \qquad 90x + 90y = 540 \\ \hline
II - (90\cdot I)\!:& \qquad (90x + 120y) - (90x + 90y) = 645 - 540 \\
& \qquad 30y = 105 \;\Rightarrow\; y = \dfrac{105}{30} = \dfrac{7}{2} \\[6pt]
x \cap I\!:& \qquad x + \dfrac{7}{2} = 6 
\;\Rightarrow\; x = 6 - \dfrac{7}{2} 
= \dfrac{12 - 7}{2} 
= \dfrac{5}{2}
\end{align*}
$$
Die Einsatzzeiten betragen $ \dfrac{5}{2}\,\text{h}$ (Drucker A) und $ \dfrac{7}{2}\,\text{h}$ (Drucker B).
************







