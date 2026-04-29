<!--
version:  0.0.1
language: de


import: https://cdn.jsdelivr.net/gh/LiaTemplates/algebrite@master/README.md
import: https://cdn.jsdelivr.net/gh/LiaTemplates/JSXGraph@main/README.md

import: https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/main/README.md

import: https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/main/imports/KoordREADME.md

import: https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/main/imports/FreezeREADME.md


author: Martin Lommatzsch
-->

# Aufgaben für die Prüfungstage - Mathematik: Klasse 8




> Wenn du diese Aufgaben bearbeitest, solltest du nicht in ein anderes Fenster oder einen anderen Tab wechseln, sondern dich nur auf diese Aufgaben konzentrieren. Hole dir alle Materialien, die du zum Bearbeiten dieser Aufgaben brauchst. In deinem Fall solltest du dir Stifte und Papier holen, um dir zur Not Notizen machen zu können. Am Ende der Bearbeitung sendest du diese bearbeiteten Aufgaben an deinen Lehrer oder deine Lehrerin, sodass die Lehrkräfte sehen können, was du gemacht hast. <p align="right"> - Martin Lommatzsch </p>

> HINWEIS 1: <h3>Diese Aufgaben können abgegeben werden. Am Ende des Kurses kann der Kurs eingefroren werden. Dadurch entsteht ein Link, speichere diesen Link ab. Versende diesen Link via LernSax an deinen Lehrer oder deine Lehrerin, wenn deine Lehrkraft dies möchte. WICHTIG: Die Absprachen mit den jeweiligen Lehrkräften gelten. </h3>

> HINWEIS 2: <h3> Das Anzahl, wie oft du auf "Prüfen" drückst, wird auch erfasst. </h3>

> HINWEIS 3: <h3> Falls du eine Aufgabe gerade nicht bearbeiten möchtest, kannst du zur nächsten wechseln. Du kannst zu jeder Zeit zu dieser Aufgabe zurückkehren. Bearbeite am besten alle Aufgaben, bevor du alles einfrierst. </h3>


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









## Äquivalenzumformung





**_Aufgabe 1:_** **Berechne** den Wert der unbekannten Größe.


<section class="dynFlex">
<div class="flex-child">

__$a)\;\;$__ $   F = m a \;\;$  mit $\;\;a=2 \;\;\wedge\;\; F=30$

<!-- data-solution-timer="600s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$m$ = [[  15  ]] @canvas
************
$$
\begin{align*}
F &= m a \quad \left| :a \right. \\
m &= \dfrac{F}{a} \\ 
m &= \dfrac{30}{2}  \\
m &= 15  \\
\end{align*}
$$
************

@ADetails(2=BE;Äquivalenzumformung)

</div>
<div class="flex-child">

__$b)\;\;$__ $   U - T = \dfrac{1}{2} v \;\;$  mit $\;\; v=5 \;\;\wedge\;\; U=7$

<!-- data-solution-timer="600s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$T$ = [[  9/2  ]] @canvas
@Algebrite.check(9/2)
************
$$
\begin{align*}
U - T &= \dfrac{1}{2} v \quad \left| -U \right. \\
-T &= \dfrac{1}{2} v - U \quad \left| \cdot (-1) \right. \\
T &= U - \dfrac{1}{2}v \\ 
T &= 7 - \dfrac{1}{2}\cdot 5  \\
T &= 7 - \dfrac{5}{2}  \\
T &= \dfrac{14}{2} - \dfrac{5}{2}  \\
T &= \dfrac{9}{2} \\
\end{align*}
$$
************

@ADetails(2=BE;Äquivalenzumformung)

</div>
<div class="flex-child">

__$c)\;\;$__ $   r = 2x + 2y + z \;\;$  mit $\;\; r=12 \;\;\wedge\;\; x=0,4 \;\;\wedge\;\; z=1,5$

<!-- data-solution-timer="600s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$y$ = [[  97/20  ]] @canvas
@Algebrite.check(97/20)
************
$$
\begin{align*}
r &= 2x + 2y + z \quad \left| -2x  \right. \\
r -2x &=  2y + z \quad \left|  - z \right. \\
r - 2x - z &= 2y \quad \left| :2 \right. \\
y &= \dfrac{r - 2x - z}{2} \\ 
y &= \dfrac{12 - 2\cdot 0,4 - 1,5}{2} \\
y &= \dfrac{12 - 0,8 - 1,5}{2} \\
y &= \dfrac{9,7}{2} \\
y &= \dfrac{97}{20} \\
\end{align*}
$$
************

@ADetails(2=BE;Äquivalenzumformung)

</div>
<div class="flex-child">

__$d)\;\;$__ $   pV = \dfrac{3}{2}kNT \;\;$  mit $\;\; N=100 \;\;\wedge\;\; k=5 \;\;\wedge\;\; p=30 \;\;\wedge\;\; V=20$

<!-- data-solution-timer="600s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$T$ = [[  4/5  ]] @canvas
@Algebrite.check(4/5)
************
$$
\begin{align*}
pV &= \dfrac{3}{2}kNT \quad \left| : \left(\dfrac{3}{2}kN\right) \right. \\
T &= \dfrac{pV}{\dfrac{3}{2}kN} \\ 
T &= \dfrac{30\cdot 20}{\dfrac{3}{2}\cdot 5 \cdot 100} \\
T &= \dfrac{600}{750}  \\
T &= \dfrac{4}{5}  \\
\end{align*}
$$
************

@ADetails(2=BE;Äquivalenzumformung)

</div>
<div class="flex-child">

__$e)\;\;$__ $   8ab - c = cb + b \;\;$  mit $\;\; b=3 \;\;\wedge\;\; c=0,75$


<!-- data-solution-timer="600s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$a$ = [[  1/4  ]] @canvas
@Algebrite.check(1/4)
************
$$
\begin{align*}
8ab - c &= cb + b \quad \left| +c \right. \\
8ab &= cb + b + c \quad \left| : (8b) \right. \\
a &= \dfrac{cb + b + c}{8b} \\ 
a &= \dfrac{0,75\cdot 3 + 3 + 0,75}{8\cdot 3} \\
a &= \dfrac{2,25 + 3 + 0,75}{24} \\
a &= \dfrac{6}{24} \\
a &= \dfrac{1}{4} \\
\end{align*}
$$
************

@ADetails(2=BE;Äquivalenzumformung)

</div>
<div class="flex-child">

__$f)\;\;$__ $   G\dfrac{M m}{r} = F \;\;$  mit $\;\; F=120 \;\;\wedge\;\; M=4,5 \;\;\wedge\;\; m=9,5 \;\;\wedge\;\; G=1,2$

<!-- data-solution-timer="600s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$r$ = [[  4275/10000  ]] @canvas
@Algebrite.check(4275/10000)
************
$$
\begin{align*}
\dfrac{G M m}{r} &= F \quad \left| \cdot r \right. \\
G M m &= F r \quad \left| :F \right. \\
r &= \dfrac{G M m}{F} \\ 
r &= \dfrac{1,2\cdot 4,5 \cdot 9,5}{120}  \\
r &= \dfrac{51,3}{120}  \\
r &= 0,4275  \\
\end{align*}
$$
************

@ADetails(2=BE;Äquivalenzumformung)

</div>
<div class="flex-child">

__$g)\;\;$__ $  \dfrac{A}{B} = \dfrac{C}{D} \;\;$  mit $\;\; A=0,2 \;\;\wedge\;\; B=0,5 \;\;\wedge\;\; C=6$

<!-- data-solution-timer="600s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$D$ = [[  15  ]] @canvas
************
$$
\begin{align*}
\dfrac{A}{B} &= \dfrac{C}{D} \quad \left| \cdot D \right. \\
\dfrac{A}{B}D &= C \quad \left| \cdot B \right. \\
AD &= BC \quad \left| :A \right. \\
D &= \dfrac{B C}{A} \\ 
D &= \dfrac{0,5\cdot 6}{0,2}  \\
D &= \dfrac{3}{0,2}  \\
D &= 15
\end{align*}
$$
************

@ADetails(2=BE;Äquivalenzumformung)

</div>
</section>








## Funktionen




<section class="dynFlex">
<div class="flex-child">

__$a)\;\;$__ **Berechne** den Funktionswert an der Stelle $x=-2$ von $ f(x)= \dfrac{2}{3} x + \dfrac{3}{2} $.


<!-- data-solution-timer="600s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$x_N =$ [[  1/6  ]] @canvas
@Algebrite.check(1/6)
************
$$
\begin{align*}
f(x=-2) &= \dfrac{2}{3} \cdot (-2) + \dfrac{3}{2} = -\dfrac{4}{3} + \dfrac{3}{2} = \dfrac{1}{6} \\
\end{align*}
$$
************

@ADetails(1=BE;Lineare Funktionen, Punkt)

</div>
<div class="flex-child">

__$b)\;\;$__ **Berechne** den Variablenwert für den Funktionswert $f(x)=4$ von $ f(x)= \dfrac{2}{3} x + \dfrac{3}{2} $.


<!-- data-solution-timer="600s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$x =$ [[  15/4  ]] @canvas
@Algebrite.check(15/4)
************
$$
\begin{align*}
4 &= \dfrac{2}{3} x + \dfrac{3}{2} \quad \left| - \dfrac{3}{2} \right. \\
\dfrac{5}{2} &= \dfrac{2}{3} x  \quad \left| \cdot \dfrac{3}{2} \right. \\
\dfrac{15}{4} &=  x
\end{align*}
$$
************

@ADetails(2=BE;Lineare Funktionen, Punkt)

</div>
<div class="flex-child">

__$c)\;\;$__ **Berechne** die Nullstelle von $ f(x)= \dfrac{2}{3} x + \dfrac{3}{2} $.


<!-- data-solution-timer="600s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$x_N =$ [[  -9/4  ]] @canvas
@Algebrite.check(-9/4)
************
$$
\begin{align*}
f(x) \stackrel{!}{=} 0 &= \dfrac{2}{3} x + \dfrac{3}{2}  \quad \left| - \dfrac{3}{2} \right. \\
-\dfrac{3}{2} &= \dfrac{2}{3} x  \quad \left| \cdot \dfrac{3}{2} \right. \\
-\dfrac{9}{4} &=  x
\end{align*}
$$
************

@ADetails(2=BE;Lineare Funktionen, Nullstelle)

</div>
<div class="flex-child">

__$d)\;\;$__ **Berechne** die Nullstelle von $ g(x)= -2 x + \dfrac{5}{8} $.


<!-- data-solution-timer="600s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$x_N =$ [[  5/16  ]] @canvas
@Algebrite.check(5/16)
************
$$
\begin{align*}
g(x) \stackrel{!}{=} 0 &= -2 x + \dfrac{5}{8} \quad \left| +2x \right. \\
2x &= \dfrac{5}{8}  \quad \left| : 2 \right. \\
x &= \dfrac{5}{16}
\end{align*}
$$
************

@ADetails(2=BE;Lineare Funktionen, Nullstelle)

</div>
<div class="flex-child">

__$e)\;\;$__ **Berechne** die Schnittstelle von  $f(x)= \dfrac{2}{3} x + \dfrac{3}{2}$ und $g(x) = -2 x + \dfrac{5}{8}$


<!-- data-solution-timer="600s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$x_S =$ [[  -21/64  ]] @canvas
@Algebrite.check(-21/64)
************
$$
\begin{align*}
\dfrac{2}{3} x + \dfrac{3}{2} &\stackrel{!}{=} -2 x + \dfrac{5}{8} \quad \left| +2x \right. \\
\dfrac{8}{3} x + \dfrac{3}{2} &=  \dfrac{5}{8} \quad \left| -\dfrac{3}{2} \right. \\
\dfrac{8}{3} x &=  -\dfrac{7}{8} \quad \left|  \cdot \dfrac{3}{8} \right. \\
x &= -\dfrac{21}{64}  
\end{align*}
$$
************

@ADetails(2=BE;Lineare Funktionen, Schnittstelle)

</div>
<div class="flex-child">

__$f)\;\;$__ Der Graph der Funktion $h$ schneidet den Graph der Funktion $g$ an der Stelle $x=-\dfrac{1}{2}$ und ist orthogonal zu $g(x) = -2 x + \dfrac{5}{8}$. Berechne den Funktionsterm von $ h(x) $ 


<!-- data-solution-timer="600s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$h(x)=$ [[     1/2*x+15/8     ]] @canvas
@Algebrite.check(1/2*x+15/8)
************
$$
\begin{align*}
g\left( x = -\dfrac{1}{2} \right) = -2 \cdot \left( -\dfrac{1}{2} \right) + \dfrac{5}{8} = \dfrac{13}{8}
\end{align*}
$$
$$
\begin{align*}
m_g \cdot m_h = -1 \;\;\Rightarrow\;\; m_h = \dfrac{1}{2}
\end{align*}
$$
$$
\begin{align*}
h(x) & = m_h x + n_h \\
 \dfrac{13}{8} & = \dfrac{1}{2} \cdot \left( -\dfrac{1}{2} \right) + n_h  \quad \left| + \dfrac{1}{4} \right. \\
 \dfrac{15}{8} & = n_h  \\
\Rightarrow\;\; h(x) & = \dfrac{1}{2}x + \dfrac{15}{8}
\end{align*}
$$
************

@ADetails(3=BE;Lineare Funktionen, Orthogonal, Schnittstelle)

</div>
</section>









## Stochastik



In den dargestellten Gefäßen befinden sich Kugeln unterschiedlicher Farben. 


<section class="dynFlex">

<div class="flex-child">
__$a)\;\;$__ 

<!-- style="width:350px" -->
![](https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/Repetitorium/Kap7/urne23.png)


</div>
<div class="flex-child">



<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
**Gib** die absolute Häufigkeit der blauen Kugeln **an**.\
$\#(B)=$ [[  9  ]]

@ADetails(BE=1;Stochastik)

</div>
<div class="flex-child">

**Gib** die relative Häufigkeit der nicht grauen Kugeln **an**.

<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$p(\bar{G})=$ [[  13/19  ]]  
@Algebrite.check(13/19)

@ADetails(BE=1;Stochastik)

</div>
<div class="flex-child">

<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
**Gib** die Wahrscheinlichkeit **an**, eine blaue Kugel zu ziehen.\
$P(R)=$ [[  9/19  ]] 
@Algebrite.check(9/19)

@ADetails(BE=1;Stochastik)

</div>
<div class="flex-child">

<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
**Gib** die Chance **an**, eine violette oder graue Kugel im Vergleich zu den anderen Kugeln zu ziehen.\
$R(\bar{B})=$ [[  10:9  ]] 

@ADetails(BE=1;Stochastik)

</div>
<div class="flex-child">

<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
**Gib** die Wahrscheinlichkeit **an**, eine blaue oder graue Kugel zu ziehen.\
$P(B \cup G)=$ [[  15/19  ]] 
@Algebrite.check(15/19)

@ADetails(BE=1;Stochastik)

</div>
<div class="flex-child">

<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
**Gib** die Chance **an**, eine violette Kugel im Vergleich zu den anderen Kugeln zu ziehen.\
$R(V)=$ [[  4:15  ]] 

@ADetails(BE=1;Stochastik)


</div>
</section>








## Geometrie im Koordinatensystem




@Koordinatensystem(`xmin=-10;xmax=10;ymin=-10;ymax=10;width=700;id=A1`)

@AchsenBeschriftung(`id=A1;xlabel=$x$;ylabel=$y$`)



<section class="dynFlex">
<div class="flex-child">

__$a)\;\;$__ **Gib** die Koordinaten des Punktes $A$ **an**.


@Punkt(`A1;A;-5;-3;fix`)

<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$A \left(\right.$ [[  -5  ]] $\left.\right| $ [[  -3  ]] $\left.\right)$
@Algebrite.check([-5;-3])

@ADetails(1=BE;Koordinatensystem)

</div>
<div class="flex-child">

__$b)\;\;$__ **Gib** die Koordinaten des Punktes $C$ **an**, sodass das Parallelogramm $\Box ABCD$ entsteht. (Der Punkt $C$ ist zu Hilfe beweglich.)


@Punkt(`A1;B;4;-2;fix`)
@Punkt(`A1;D;-3;6;fix`)
@Punkt(`A1;C;-3;-8.5`)

<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$C \left(\right.$ [[  6  ]] $\left.\right| $ [[  7  ]] $\left.\right)$
@Algebrite.check([6;7])

@ADetails(1=BE;Koordinatensystem)

</div>
<div class="flex-child">

__$c)\;\;$__ **Gib** die Koordinaten des Schnittpunktes $M$ der Diagonalen des Parallelogramms $\Box ABCD$ **an**. (Der Punkt $M$ ist zu Hilfe beweglich.)



@Punkt(`A1;M;-2;-8.5`)

<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$M \left(\right.$ [[  0,5  ]] $\left.\right| $ [[  2  ]] $\left.\right)$
@Algebrite.check([0.5;2])

@ADetails(1=BE;Koordinatensystem)

</div>

<div class="flex-child">

__$d)\;\;$__ **Gib** die Koordinaten des Punktes $F$ **an**, sodass ein symmetrisches Drachenviereck $\Box AEFG$ mit dem Flächeninhalt von $A=22\,FE$ entsteht. (Der Punkt $F$ ist zu Hilfe beweglich.)


@Punkt(`A1;E;-3;-1;fix`)
@Punkt(`A1;G;-7;-1;fix`)
@Punkt(`A1;F;-4;-8.5`)

<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$F \left(\right.$ [[  -5  ]] $\left.\right| $ [[  8  ]] $\left.\right)$
@Algebrite.check([-5;8])

@ADetails(1=BE;Koordinatensystem)

</div>


<div class="flex-child">

__$e)\;\;$__ Die Punkte $G$, $E$ und $D$ beschreiben ein Rechteck. **Gib** den Umfang dieses Rechtecks **an**.


<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$u =$ [[  22  ]] $LE$ @canvas
@Algebrite.check(22)

@ADetails(1=BE;Koordinatensystem)

</div>

<div class="flex-child">

__$f)\;\;$__ **Gib** die Länge der Strecke $\overline{PB}$ **an**.


@Punkt(`A1;P;1;-6;fix`)


<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$\left| \overline{PB} \right| =$ [[  5  ]] $LE$ @canvas
@Algebrite.check(5)

@ADetails(1=BE;Koordinatensystem)

</div>



<div class="flex-child">

__$g)\;\;$__ **Gib** die korrekte Winkelart **an**.

<!-- data-solution-timer="450s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$\measuredangle GAE$ ist ein [[Nullwinkel|spitzer Winkel|(rechter Winkel)|stumpfer Winkel|gestreckter Winkel|überstumpfer Winkel|voller Winkel]]
@ADetails(1=BE;Koordinatensystem,Winkel)

</div>

<div class="flex-child">

__$h)\;\;$__ **Gib** die korrekte Winkelart **an**.

<!-- data-solution-timer="450s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$\measuredangle GBD$ ist ein [[Nullwinkel|spitzer Winkel|rechter Winkel|stumpfer Winkel|gestreckter Winkel|(überstumpfer Winkel)|voller Winkel]]
@ADetails(1=BE;Koordinatensystem,Winkel)

</div>

<div class="flex-child">

__$i)\;\;$__ **Gib** die korrekte Winkelart **an**.

<!-- data-solution-timer="450s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$\measuredangle EDP$ ist ein [[Nullwinkel|(spitzer Winkel)|rechter Winkel|stumpfer Winkel|gestreckter Winkel|überstumpfer Winkel|voller Winkel]]
@ADetails(1=BE;Koordinatensystem,Winkel)

</div>

<div class="flex-child">

__$i)\;\;$__ **Gib** die korrekte Winkelart **an**.

<!-- data-solution-timer="450s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$\measuredangle BAG$ ist ein [[Nullwinkel|spitzer Winkel|rechter Winkel|(stumpfer Winkel)|gestreckter Winkel|überstumpfer Winkel|voller Winkel]]
@ADetails(1=BE;Koordinatensystem,Winkel)

</div>

<div class="flex-child">

__$j)\;\;$__ **Gib** Flächeninhalt des Dreiecks $\Delta GPE$ **an**.

<!-- data-solution-timer="450s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$A =$ [[  10  ]] cm$^2$ @canvas
@Algebrite.check(10)

@ADetails(1=BE;Koordinatensystem,Dreieck)

</div>

<div class="flex-child">

__$k)\;\;$__ **Gib** Flächeninhalt des Dreiecks $\Delta EBD$ **an**.

<!-- data-solution-timer="450s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$A =$ [[   24,5   ]] cm$^2$ @canvas
@Algebrite.check(24.5)

@ADetails(1=BE;Koordinatensystem,Dreieck)

</div>


</section>




## Geometrieaufgaben







**_Aufgabe 1:_** Berechne den Flächeninhalt eines Rechtecks mit den Maßen $a=\dfrac{48}{27}\,$cm und $b=\dfrac{15}{8}\,$cm. \


<!-- data-solution-timer="600s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$A=$[[  10/3  ]]cm$^2$ @canvas
@Algebrite.check(10/3)
************
$$
\begin{align*}
A &= a \cdot b \\
  &= \dfrac{48}{27}\,\text{cm} \cdot \dfrac{15}{8}\,\text{cm} \\
  &= \dfrac{48 \cdot 15}{27 \cdot 8}\,\text{cm}^2 \\
  &= \dfrac{720}{216}\,\text{cm}^2 \\
  &= \dfrac{10}{3}\,\text{cm}^2 \\
  &\approx 3{,}33\,\text{cm}^2
\end{align*}
$$
************

@ADetails(2=BE;Rechteck,Bruchrechnung)

--- 

--- 


**_Aufgabe 2:_** Gegeben sei eine Pyramide mit quadratischer Grundfläche mit einer Seitenlänge $a$ von $7,5\,$cm und einer Manteldreieckshöhe von $5,5\,$cm zu $a$. **Berechne** den Oberflächeninhalt der Pyramide.

<!-- data-solution-timer="600s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$O=$  [[   138,75  ]] cm$^2$ @canvas
@Algebrite.check(138.75)
***********************

$$ 
\begin{align*}
    O_P & = a^2 + 2 a h_a \\
    & = \left( 7,5 \,\text{cm}\right)^2 + 2 \cdot 7,5 \,\text{cm} \cdot 5,5 \,\text{cm} \\
    & = 138,75\,\text{cm}^2 \\
\end{align*}
$$

***********************




@ADetails(2=BE;Pyramide,Bruchrechnung)


--- 

--- 





**_Aufgabe 3:_** Berechne das Volumen eines Quaders mit den Maßen $a=\dfrac{11}{18}\,$cm, $b=\dfrac{5}{28}\,$cm und $c=\dfrac{21}{55}\,$cm. \



<!-- data-solution-timer="600s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$V=$[[  1/24  ]]cm$^3$ @canvas
@Algebrite.check(1/24)
************
$$
\begin{align*}
V &= a \cdot b \cdot c \\[4pt]
  &= \dfrac{11}{18}\,\text{cm} \cdot \dfrac{5}{28}\,\text{cm}
     \cdot \dfrac{21}{55}\,\text{cm} \\[4pt]
  &= \dfrac{11 \cdot 5 \cdot 21}{18 \cdot 28 \cdot 55}\,\text{cm}^3 \\[6pt]
\text{Kürzen:} \quad
  &\dfrac{11}{55} = \dfrac{1}{5}, \quad
    \dfrac{21}{28} = \dfrac{3}{4} \\[4pt]
V &= \dfrac{1 \cdot 5 \cdot 3}{18 \cdot 4 \cdot 5}\,\text{cm}^3 \\[4pt]
  &= \dfrac{15}{360}\,\text{cm}^3
   = \dfrac{1}{24}\,\text{cm}^3
\end{align*}
$$
************

@ADetails(2=BE;Quader,Bruchrechnung)


## Sachaufgaben



**_Aufgabe 1:_** Ein Behälter wird täglich mit vier Litern Wasser aufgefüllt. Zu Beginn sind bereits zwei Liter enthalten.  
Ein zweiter Behälter enthält anfangs 14 Liter Wasser, verliert jedoch jeden Tag einen Liter.  
**Berechne**, nach wie vielen Tagen beide Behälter gleich viel Wasser enthalten.


<!-- data-solution-timer="600s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$x$ = [[  12/5  ]] @canvas
@Algebrite.check(12/5)
************
$$
\textbf{Gleichung aus dem Text:}\quad 
4x + 2 \;\stackrel{!}{=}\; 14 - x
$$

$$
\begin{align*}
4x + 2 &= 14 - x \quad \left|\, +x \right.\\[2pt]
5x + 2 &= 14 \quad \left|\, -2 \right.\\[2pt]
5x &= 12 \quad \left|\, :5 \right.\\[2pt]
x &= \dfrac{12}{5}
\end{align*}
$$

$$
\begin{align*}
\textbf{Probe:}\quad 
&\underbrace{4\cdot \dfrac{12}{5} + 2}_{\text{1. Behälter}} 
= \dfrac{48}{5} + \dfrac{10}{5} = \dfrac{58}{5} = 11,6   \\
&\quad\text{und}\quad    \\
\underbrace{14 - \dfrac{12}{5}}_{\text{2. Behälter}}
&= \dfrac{70}{5} - \dfrac{12}{5} = \dfrac{58}{5} = 11,6
\end{align*}
$$


Deutung: Nach $\dfrac{12}{5} = 2{,}4$ Tagen haben beide Behälter gleich viel Wasser.
************



@ADetails(4=BE;Sachaufgaben,Äquivalenzumformung)


--- 

--- 


**_Aufgabe 2:_** Ein Mensch bearbeitet an einem Nachmittag zwei Textkapitel. Insgesamt arbeitet dieser 5 Stunden. Beim ersten Kapitel ($x$) schafft er 60 Seiten pro Stunde, beim zweiten ($y$) 40 Seiten pro Stunde. Am Ende hast der Mensch zusammen 255 Seiten bearbeitet. 
**Berechne** die Arbeitszeiten für beide Kapitel.


<!-- data-solution-timer="600s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$x$ = [[  11/4  ]] @canvas und $y$ = [[  9/4  ]] @canvas
@Algebrite.check([ 11/4; 9/4 ])
************
Bezeichne mit $x$ die Zeit am ersten Kapitel (in Stunden) und mit $y$ die Zeit am zweiten Kapitel.
$$
\begin{align*}
I.& \qquad x + y = 5 \\
II.& \qquad 60x + 40y = 255 \\ \hline
40\cdot I\!:& \qquad 40x + 40y = 200 \\ \hline
II - (40\cdot I)\!:& \qquad (60x + 40y) - (40x + 40y) = 255 - 200 \\
& \qquad 20x = 55 \;\Rightarrow\; x = \dfrac{55}{20} = \dfrac{11}{4} \\[6pt]
x \cap I\!:& \qquad \dfrac{11}{4} + y = 5 
\;\Rightarrow\; y = 5 - \dfrac{11}{4} 
= \dfrac{20 - 11}{4} 
= \dfrac{9}{4}
\end{align*}
$$
Die Arbeitszeiten betragen $ \dfrac{11}{4}\,\text{h}$ (erstes Kapitel) und $ \dfrac{9}{4}\,\text{h}$ (zweites Kapitel).
************


@ADetails(4=BE;Sachaufgaben,Gleichungssystem)







# Abgabe

> <h3>Diese Aufgaben werden abgegeben. Am Ende des Kurses kann der Kurs eingefroren werden. Dadurch entsteht ein Link, versende diesen Link via LernSax an deinen Lehrer oder deine Lehrerin. </h3>

@Abgabe

@Auswertung(F12;Tab;Time)

