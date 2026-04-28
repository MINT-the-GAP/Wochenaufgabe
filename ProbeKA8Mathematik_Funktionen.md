<!--
version:  0.0.1
language: de


import: https://cdn.jsdelivr.net/gh/LiaTemplates/algebrite@master/README.md
import: https://cdn.jsdelivr.net/gh/LiaTemplates/JSXGraph@main/README.md

import: https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/main/README.md

import: https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/main/imports/KoordREADME.md




author: Martin Lommatzsch
-->

# Probeklassenarbeit für Mathematik - Klasse 8: Funktionaler Zusammenhang


<br>

> Letztes Update am 28.04.2026 gegen 18 Uhr

<br>



Hier hast du nochmal eine Übersicht über die Menüleiste:

> <center> ![Bediehnungsübersicht](https://raw.githubusercontent.com/MINT-the-GAP/Wochenaufgabe/refs/heads/main/5/Deutsch/pics/tutorial.png) </center>

- 1. Inhaltsverzeichnis: Komme schnell zu deiner Aufgabe

- 2. Textmarker: Markiere dir wichtige Textpassagen

- 3. Schriftgrößenanpassung: Stelle dir die Schriftgröße für deinen optimalen Arbeitsmodus ein.

- 4. Darstellungsbreite: Es wird "Präsentation" empfohlen, aber probiere ruhig mal "Lehrbuch" aus.

- 5. Aussehen von LiaScript: Hier kannst du in den Dunkelmodus wechseln oder die Themefarben anpassen. Auch kannst du die Vorlesegeschwindigkeit sowie Stimmhöhe anpassen.

- 6. Automatische Übersetzung in andere Sprachen

- 7. Gruppenraum eröffnen: (für dich wohl unwichtig, aber für LehrerInnen eventuell interessanter)

- 8. Informationen zum Kurs: Hier steht, welche Version das Arbeitsblatt besitzt und wer das Arbeitsblatt erstellt hat.

Wenn du mit den Aufgaben beginnen willst, dann swipe (wische) entweder weiter oder klicke unten neben der Seitenzahl auf den Pfeil nach rechts.






---

---


<h2>**Schrifterkennung**</h2>



<center>

<!-- style="width:200px" -->
![Canvas](https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/Readme/canvas.png)

</center>

1. Öffnet oder schließt die Schreibfläche.

2. Macht die letzte Änderung auf der Schreibfläche rückgängig.

3. Stellt das letzte "Rückgängig machen" wieder her.

4. Radierer mit Submenü für Radierergröße oder komplettes löschen.

5. Stift mit Submenü für Farbauswahl, Stiftdicke und Transparenz.

6. Legt ein Grid oder Linien in den Hintergrund.

7. Lässt ein Feld ziehen, welches mittels Schrifterkennung an das Eingabefeld als Lösung übergibt.

Die Schreibfläche kann unten links oder rechts an den Ecke in der Größe beliebig verändert werden.


> **Steuerung mit Maus**

- Linke Maustaste: Zeichnen, Radieren, Ziehen

- Rechte Maustaste: Schreibfläche hin- und herziehen

- Mausrad: Zoom


> **Steuerung mit Touchscreen**

- Ein Finger:  Zeichnen, Radieren, Ziehen

- Zwei Finger (Abstand zwischen den Fingern gleichbleibend): Schreibfläche hin- und herziehen

- Zwei Finger (Abstand zwischen den Fingern verändern): Zoom









## Teil ohne Taschenrechner - Funktionen








<section class="dynFlex">
<div class="flex-child">

__$a)\;\;$__ **Berechne** den Funktionswert an der Stelle $x=-2$ von $ f(x)= -\dfrac{3}{4} x + \dfrac{5}{6} $.


<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$f(-2) =$ [[  7/3  ]] @canvas
@Algebrite.check(7/3)
************
$$
\begin{align*}
f(x=-2) &= -\dfrac{3}{4} \cdot (-2) + \dfrac{5}{6} = \dfrac{3}{2} + \dfrac{5}{6} = \dfrac{7}{3} \\
\end{align*}
$$
************


</div>
<div class="flex-child">

__$b)\;\;$__ **Berechne** den Variablenwert für den Funktionswert $f(x)=-1$ von $ f(x)= -\dfrac{3}{4} x + \dfrac{5}{6} $.


<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$x =$ [[  22/9  ]] @canvas
@Algebrite.check(22/9)
************
$$
\begin{align*}
-1 &= -\dfrac{3}{4} x + \dfrac{5}{6} \quad \left| - \dfrac{5}{6} \right. \\
-\dfrac{11}{6} &= -\dfrac{3}{4} x  \quad \left| \cdot \left(-\dfrac{4}{3}\right) \right. \\
\dfrac{22}{9} &=  x
\end{align*}
$$
************


</div>
<div class="flex-child">

__$c)\;\;$__ **Berechne** die Nullstelle von $ f(x)= -\dfrac{3}{4} x + \dfrac{5}{6} $.


<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$x_N =$ [[  10/9  ]] @canvas
@Algebrite.check(10/9)
************
$$
\begin{align*}
f(x) \stackrel{!}{=} 0 &= -\dfrac{3}{4} x + \dfrac{5}{6}  \quad \left| + \dfrac{3}{4}x \right. \\
\dfrac{3}{4}x &= \dfrac{5}{6}  \quad \left| \cdot \dfrac{4}{3} \right. \\
x &= \dfrac{10}{9}
\end{align*}
$$
************


</div>
<div class="flex-child">

__$d)\;\;$__ **Berechne** die Nullstelle von $ g(x)= \dfrac{3}{2} x - \dfrac{7}{12} $.


<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$x_N =$ [[  7/18  ]] @canvas
@Algebrite.check(7/18)
************
$$
\begin{align*}
g(x) \stackrel{!}{=} 0 &= \dfrac{3}{2} x - \dfrac{7}{12} \quad \left| +\dfrac{7}{12} \right. \\
\dfrac{3}{2}x &= \dfrac{7}{12}  \quad \left| \cdot \dfrac{2}{3} \right. \\
x &= \dfrac{7}{18}
\end{align*}
$$
************


</div>
<div class="flex-child">

__$e)\;\;$__ **Berechne** die Schnittstelle von  $f(x)= -\dfrac{3}{4} x + \dfrac{5}{6}$ und $g(x) = \dfrac{3}{2} x - \dfrac{7}{12}$.


<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$x_S =$ [[  17/27  ]] @canvas
@Algebrite.check(17/27)
************
$$
\begin{align*}
-\dfrac{3}{4} x + \dfrac{5}{6} &\stackrel{!}{=} \dfrac{3}{2} x - \dfrac{7}{12} \quad \left| +\dfrac{3}{4}x \right. \\
\dfrac{5}{6} &= \dfrac{9}{4}x - \dfrac{7}{12} \quad \left| +\dfrac{7}{12} \right. \\
\dfrac{17}{12} &= \dfrac{9}{4}x \quad \left|  \cdot \dfrac{4}{9} \right. \\
\dfrac{17}{27} &= x  
\end{align*}
$$
************


</div>
<div class="flex-child">

__$f)\;\;$__ Der Graph der Funktion $h$ schneidet den Graph der Funktion $g$ an der Stelle $x=\dfrac{1}{2}$ und ist orthogonal zu $g(x) = \dfrac{3}{2} x - \dfrac{7}{12}$. **Berechne** den Funktionsterm von $ h(x) $. 


<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$h(x)=$ [[     -2/3*x+1/2     ]] @canvas
@Algebrite.check(-2/3*x+1/2)
************
$$
\begin{align*}
g\left( x = \dfrac{1}{2} \right) = \dfrac{3}{2} \cdot \dfrac{1}{2} - \dfrac{7}{12} = \dfrac{3}{4} - \dfrac{7}{12} = \dfrac{1}{6}
\end{align*}
$$
$$
\begin{align*}
m_g \cdot m_h = -1 \;\;\Rightarrow\;\; m_h = -\dfrac{2}{3}
\end{align*}
$$
$$
\begin{align*}
h(x) & = m_h x + n_h \\
 \dfrac{1}{6} & = -\dfrac{2}{3} \cdot \dfrac{1}{2} + n_h  \quad \left| + \dfrac{1}{3} \right. \\
 \dfrac{1}{2} & = n_h  \\
\Rightarrow\;\; h(x) & = -\dfrac{2}{3}x + \dfrac{1}{2}
\end{align*}
$$
************


</div>


<div class="flex-child">

__$g)\;\;$__ Der Graph der Funktion $k$ verläuft durch die Punkte $P(-3|4)$ und $Q(2|-5)$. **Berechne** den Funktionsterm von $ k(x) $. 


<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$k(x)=$ [[     -9/5*x-7/5     ]] @canvas
@Algebrite.check(-9/5*x-7/5)
************
$$
\begin{align*}
m_k &= \dfrac{y_Q-y_P}{x_Q-x_P} \\
    &= \dfrac{-5-4}{2-(-3)} \\
    &= \dfrac{-9}{5}
\end{align*}
$$
$$
\begin{align*}
k(x) &= m_k x + n_k \\
4 &= -\dfrac{9}{5} \cdot (-3) + n_k \\
4 &= \dfrac{27}{5} + n_k \quad \left| - \dfrac{27}{5} \right. \\
-\dfrac{7}{5} &= n_k
\end{align*}
$$
$$
\begin{align*}
\Rightarrow\;\; k(x) &= -\dfrac{9}{5}x - \dfrac{7}{5}
\end{align*}
$$
************


</div>


<div class="flex-child">

__$h)\;\;$__  **Berechne** die Nullstelle der Funktion von $ p(n) = 3(n-4) + 2n - 8 $. 

<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$n_N =$ [[  4  ]] @canvas
@Algebrite.check(4)
************
$$
\begin{align*}
p(n) \stackrel{!}{=} 0 &= 3(n-4) + 2n - 8 \\
0 &= 3n - 12 + 2n - 8 \\
0 &= 5n - 20 \quad \left| +20 \right. \\
20 &= 5n \quad \left| :5 \right. \\
4 &= n
\end{align*}
$$
************



</div>
<div class="flex-child">

__$i)\;\;$__ **Berechne** die Nullstelle der Funktion $ z(x) = \dfrac{2}{5-3x}+7 $. 


<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$x_N =$ [[  37/21  ]] @canvas
@Algebrite.check(37/21)
************
$$
\begin{align*}
z(x) \stackrel{!}{=} 0 &= \dfrac{2}{5-3x}+7 \quad \left| -7 \right. \\
-7 &= \dfrac{2}{5-3x} \quad \left| \cdot (5-3x) \right. \\
-7(5-3x) &= 2 \\
-35 + 21x &= 2 \quad \left| +35 \right. \\
21x &= 37 \quad \left| :21 \right. \\
x &= \dfrac{37}{21}
\end{align*}
$$
************


</div>

<div class="flex-child">

__$j)\;\;$__ **Berechne** den Ordinatenabschnitt der Funktion $ z(x) = \dfrac{2}{5-3x}+7 $. 


<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$z(0) =$ [[  37/5  ]] @canvas
@Algebrite.check(37/5)
************
$$
\begin{align*}
z(0) &= \dfrac{2}{5-3 \cdot 0}+7 \\
     &= \dfrac{2}{5}+7 \\
     &= \dfrac{2}{5}+\dfrac{35}{5} \\
     &= \dfrac{37}{5}
\end{align*}
$$
Der Ordinatenabschnitt liegt also bei $S_y\left(0\middle|\dfrac{37}{5}\right)$.
************


</div>

<div class="flex-child">

__$k)\;\;$__ **Berechne** die Polstelle der Funktion $ z(x) = \dfrac{2}{5-3x}+7 $. 


<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$x_P =$ [[  5/3  ]] @canvas
@Algebrite.check(5/3)
************
$$
\begin{align*}
5-3x &\stackrel{!}{=} 0 \quad \left| +3x \right. \\
5 &= 3x \quad \left| :3 \right. \\
\dfrac{5}{3} &= x
\end{align*}
$$
Die Funktion hat also bei $x=\dfrac{5}{3}$ eine Polstelle.
************


</div>


<div class="flex-child">

<div class="flex-child">

__$l)\;\;$__ **Berechne** die Schnittstelle von $g(x) = \dfrac{3}{2} x - \dfrac{7}{12}$ mit $-g(x+2)-1$.


<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$x_S =$ [[  -17/18  ]] @canvas
@Algebrite.check(-17/18)
************
$$
\begin{align*}
g(x) &= -g(x+2)-1
\end{align*}
$$

$$
\begin{align*}
\dfrac{3}{2}x-\dfrac{7}{12} &= -\left(\dfrac{3}{2}(x+2)-\dfrac{7}{12}\right)-1 \\
\dfrac{3}{2}x-\dfrac{7}{12} &= -\left(\dfrac{3}{2}x+3-\dfrac{7}{12}\right)-1 \\
\dfrac{3}{2}x-\dfrac{7}{12} &= -\left(\dfrac{3}{2}x+\dfrac{29}{12}\right)-1 \\
\dfrac{3}{2}x-\dfrac{7}{12} &= -\dfrac{3}{2}x-\dfrac{29}{12}-1 \\
\dfrac{3}{2}x-\dfrac{7}{12} &= -\dfrac{3}{2}x-\dfrac{41}{12}
\end{align*}
$$

$$
\begin{align*}
\dfrac{3}{2}x-\dfrac{7}{12} &= -\dfrac{3}{2}x-\dfrac{41}{12} \quad \left| +\dfrac{3}{2}x \right. \\
3x-\dfrac{7}{12} &= -\dfrac{41}{12} \quad \left| +\dfrac{7}{12} \right. \\
3x &= -\dfrac{34}{12} \\
3x &= -\dfrac{17}{6} \quad \left| :3 \right. \\
x &= -\dfrac{17}{18}
\end{align*}
$$

$$
\begin{align*}
g\left(-\dfrac{17}{18}\right)
&= \dfrac{3}{2}\cdot\left(-\dfrac{17}{18}\right)-\dfrac{7}{12} \\
&= -\dfrac{17}{12}-\dfrac{7}{12} \\
&= -2
\end{align*}
$$

$$
\begin{align*}
\Rightarrow\;\; S\left(-\dfrac{17}{18}\middle|-2\right)
\end{align*}
$$
************


</div>




</div>


</section>






## Teil ohne Taschenrechner - Allgemeineres





folgt




## Komplexaufgabe 1


folgt







## Komplexaufgabe 2


Gegeben seien die Punkte $A(4|-2)$ und $B(-3|2)$ durch die die Funktion $f$ verläuft. Berechne den Flächeninhalt eines Vierecks, dass durch die Nullstelle und Polstelle von $g(x)=\dfrac{-1}{4-\frac{5}{4}x}+0,2$ und dem Schnittpunkt von $f$ mit $h(x)=\dfrac{2}{3} x + \dfrac{7}{4}$ beschrieben wird. Bei dem Viereck handelt es sich um ein Parallelogramm.



<!-- data-solution-timer="900s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$A =$ [[  50/13  ]] FE @canvas
@Algebrite.check(50/13)
************
Zuerst wird der Funktionsterm von $f$ bestimmt.

$$
\begin{align*}
m_f &= \dfrac{2-(-2)}{-3-4} \\
    &= \dfrac{4}{-7} \\
    &= -\dfrac{4}{7}
\end{align*}
$$

$$
\begin{align*}
f(x) &= -\dfrac{4}{7}x+n \\
-2 &= -\dfrac{4}{7}\cdot 4+n \\
-2 &= -\dfrac{16}{7}+n \quad \left|+\dfrac{16}{7}\right. \\
\dfrac{2}{7} &= n
\end{align*}
$$

$$
\begin{align*}
\Rightarrow\;\; f(x)&=-\dfrac{4}{7}x+\dfrac{2}{7}
\end{align*}
$$

Nun wird der Schnittpunkt von $f$ und $h$ berechnet.

$$
\begin{align*}
-\dfrac{4}{7}x+\dfrac{2}{7} &= \dfrac{2}{3}x+\dfrac{7}{4}
\end{align*}
$$

$$
\begin{align*}
-48x+24 &= 56x+147 \quad \left| -56x-24 \right. \\
-104x &= 123 \quad \left| :(-104) \right. \\
x &= -\dfrac{123}{104}
\end{align*}
$$

$$
\begin{align*}
h\left(-\dfrac{123}{104}\right)
&= \dfrac{2}{3}\cdot\left(-\dfrac{123}{104}\right)+\dfrac{7}{4} \\
&= -\dfrac{41}{52}+\dfrac{91}{52} \\
&= \dfrac{25}{26}
\end{align*}
$$

Damit gilt:

$$
\begin{align*}
S\left(-\dfrac{123}{104}\middle|\dfrac{25}{26}\right)
\end{align*}
$$

Nun werden Nullstelle und Polstelle von $g$ berechnet.

$$
\begin{align*}
g(x) &= \dfrac{-1}{4-\frac{5}{4}x}+\dfrac{1}{5}
\end{align*}
$$

Nullstelle:

$$
\begin{align*}
0 &= \dfrac{-1}{4-\frac{5}{4}x}+\dfrac{1}{5}
\quad \left|-\dfrac{1}{5}\right. \\
-\dfrac{1}{5} &= \dfrac{-1}{4-\frac{5}{4}x}
\end{align*}
$$

$$
\begin{align*}
-\left(4-\dfrac{5}{4}x\right) &= -5 \\
-4+\dfrac{5}{4}x &= -5 \quad \left| +4 \right. \\
\dfrac{5}{4}x &= -1 \quad \left| \cdot \dfrac{4}{5} \right. \\
x &= -\dfrac{4}{5}
\end{align*}
$$

Also gilt:

$$
\begin{align*}
N\left(-\dfrac{4}{5}\middle|0\right)
\end{align*}
$$

Polstelle:

$$
\begin{align*}
4-\dfrac{5}{4}x &\stackrel{!}{=} 0 \\
4 &= \dfrac{5}{4}x \quad \left| \cdot \dfrac{4}{5} \right. \\
\dfrac{16}{5} &= x
\end{align*}
$$

Für das Parallelogramm wird die Polstelle als Punkt auf der $x$-Achse verwendet:

$$
\begin{align*}
P\left(\dfrac{16}{5}\middle|0\right)
\end{align*}
$$

Die Grundseite des Parallelogramms liegt auf der $x$-Achse.

$$
\begin{align*}
a &= \dfrac{16}{5}-\left(-\dfrac{4}{5}\right) \\
  &= \dfrac{20}{5} \\
  &= 4
\end{align*}
$$

Die Höhe entspricht dem Abstand des Schnittpunktes $S$ von der $x$-Achse.

$$
\begin{align*}
h_a &= \dfrac{25}{26}
\end{align*}
$$

Damit ergibt sich der Flächeninhalt:

$$
\begin{align*}
A &= a \cdot h_a \\
  &= 4 \cdot \dfrac{25}{26} \\
  &= \dfrac{100}{26} \\
  &= \dfrac{50}{13}
\end{align*}
$$

$$
\begin{align*}
\Rightarrow\;\; A &= \dfrac{50}{13}\;\text{FE}
\end{align*}
$$
************


## Komplexaufgabe 3



Auf dem Schulhof soll eine trapezförmige Fläche gepflastert werden. In einer Planzeichnung entspricht eine Längeneinheit einem Meter.

Die untere linke Ecke der Fläche wird durch die Nullstelle der Funktion  
$g(x)=\dfrac{-2}{3-4x}+\dfrac{1}{3}$  
festgelegt. Die untere rechte Ecke liegt auf der $x$-Achse genau unter der Polstelle von $g$.

Die obere linke Ecke entsteht durch den Schnittpunkt der Funktion $f$ mit  
$h(x)=\dfrac{3}{2}x+1$.

Der Graph von $f$ verläuft durch die Punkte $A\left(-1\middle|\dfrac{17}{8}\right)$ und $B\left(3\middle|-\dfrac{7}{8}\right)$.  
Die obere rechte Ecke liegt senkrecht über der Polstelle von $g$ auf gleicher Höhe wie der Schnittpunkt von $f$ und $h$.

**Berechne** den Flächeninhalt der trapezförmigen Fläche.


<!-- data-solution-timer="900s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$A =$ [[  125/96  ]] $\mathrm{m}^2$ @canvas
@Algebrite.check(125/96)
************
Zuerst wird der Funktionsterm von $f$ bestimmt.

$$
\begin{align*}
m_f &= \dfrac{-\dfrac{7}{8}-\dfrac{17}{8}}{3-(-1)} \\
    &= \dfrac{-\dfrac{24}{8}}{4} \\
    &= \dfrac{-3}{4} \\
    &= -\dfrac{3}{4}
\end{align*}
$$

$$
\begin{align*}
f(x) &= -\dfrac{3}{4}x+n \\
\dfrac{17}{8} &= -\dfrac{3}{4}\cdot(-1)+n \\
\dfrac{17}{8} &= \dfrac{3}{4}+n \\
\dfrac{17}{8} &= \dfrac{6}{8}+n \quad \left|-\dfrac{6}{8}\right. \\
\dfrac{11}{8} &= n
\end{align*}
$$

Damit gilt:

$$
\begin{align*}
f(x)&=-\dfrac{3}{4}x+\dfrac{11}{8}
\end{align*}
$$

Nun wird der Schnittpunkt von $f$ und $h$ berechnet.

$$
\begin{align*}
-\dfrac{3}{4}x+\dfrac{11}{8} &= \dfrac{3}{2}x+1
\end{align*}
$$

$$
\begin{align*}
-\dfrac{3}{4}x+\dfrac{11}{8} &= \dfrac{3}{2}x+1 \quad \left| \cdot 8 \right. \\
-6x+11 &= 12x+8 \quad \left| -12x-11 \right. \\
-18x &= -3 \quad \left| :(-18) \right. \\
x &= \dfrac{1}{6}
\end{align*}
$$

$$
\begin{align*}
h\left(\dfrac{1}{6}\right)
&= \dfrac{3}{2}\cdot\dfrac{1}{6}+1 \\
&= \dfrac{3}{12}+1 \\
&= \dfrac{1}{4}+1 \\
&= \dfrac{5}{4}
\end{align*}
$$

Der Schnittpunkt ist also:

$$
\begin{align*}
S\left(\dfrac{1}{6}\middle|\dfrac{5}{4}\right)
\end{align*}
$$

Nun werden Nullstelle und Polstelle von $g$ berechnet.

$$
\begin{align*}
g(x)&=\dfrac{-2}{3-4x}+\dfrac{1}{3}
\end{align*}
$$

Nullstelle:

$$
\begin{align*}
0 &= \dfrac{-2}{3-4x}+\dfrac{1}{3} \quad \left|-\dfrac{1}{3}\right. \\
-\dfrac{1}{3} &= \dfrac{-2}{3-4x}
\end{align*}
$$

$$
\begin{align*}
-\dfrac{1}{3}(3-4x)&=-2 \quad \left| \cdot (-3) \right. \\
3-4x&=6 \quad \left| -3 \right. \\
-4x&=3 \quad \left| :(-4) \right. \\
x&=-\dfrac{3}{4}
\end{align*}
$$

Damit ist die untere linke Ecke:

$$
\begin{align*}
N\left(-\dfrac{3}{4}\middle|0\right)
\end{align*}
$$

Polstelle:

$$
\begin{align*}
3-4x &\stackrel{!}{=} 0 \\
3 &= 4x \quad \left| :4 \right. \\
\dfrac{3}{4} &= x
\end{align*}
$$

Die untere rechte Ecke liegt also bei:

$$
\begin{align*}
P\left(\dfrac{3}{4}\middle|0\right)
\end{align*}
$$

Die obere rechte Ecke liegt senkrecht über $P$ auf gleicher Höhe wie $S$:

$$
\begin{align*}
R\left(\dfrac{3}{4}\middle|\dfrac{5}{4}\right)
\end{align*}
$$

Damit besitzt das Trapez die Eckpunkte:

$$
\begin{align*}
N\left(-\dfrac{3}{4}\middle|0\right),\quad
P\left(\dfrac{3}{4}\middle|0\right),\quad
R\left(\dfrac{3}{4}\middle|\dfrac{5}{4}\right),\quad
S\left(\dfrac{1}{6}\middle|\dfrac{5}{4}\right)
\end{align*}
$$

Die untere Grundseite ist:

$$
\begin{align*}
a &= \dfrac{3}{4}-\left(-\dfrac{3}{4}\right) \\
  &= \dfrac{6}{4} \\
  &= \dfrac{3}{2}
\end{align*}
$$

Die obere Grundseite ist:

$$
\begin{align*}
c &= \dfrac{3}{4}-\dfrac{1}{6} \\
  &= \dfrac{9}{12}-\dfrac{2}{12} \\
  &= \dfrac{7}{12}
\end{align*}
$$

Die Höhe beträgt:

$$
\begin{align*}
h &= \dfrac{5}{4}
\end{align*}
$$

Nun wird der Flächeninhalt des Trapezes berechnet.

$$
\begin{align*}
A &= \dfrac{a+c}{2}\cdot h \\
  &= \dfrac{\dfrac{3}{2}+\dfrac{7}{12}}{2}\cdot\dfrac{5}{4} \\
  &= \dfrac{\dfrac{18}{12}+\dfrac{7}{12}}{2}\cdot\dfrac{5}{4} \\
  &= \dfrac{\dfrac{25}{12}}{2}\cdot\dfrac{5}{4} \\
  &= \dfrac{25}{24}\cdot\dfrac{5}{4} \\
  &= \dfrac{125}{96}
\end{align*}
$$

$$
\begin{align*}
\Rightarrow\;\; A &= \dfrac{125}{96}\;\mathrm{m}^2
\end{align*}
$$
************


