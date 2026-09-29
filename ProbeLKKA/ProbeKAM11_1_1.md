<!--
author: Martin Lommatzsch
version: 1.0.0
language: de
narrator: Deutsch Female
mode: Presentation
comment: Zweite Probeklausur für Klasse 11 zur Analysis mit Ableitungen, Kurvendiskussion und Modellierung.
tags: Mathematik, Klasse 11, Probeklausur, Analysis, Ableitungen, Kurvendiskussion, Modellierung


import: https://raw.githubusercontent.com/MINT-the-GAP/lia-DynFlex/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-timer/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-board-mode/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-marker/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-annotation/refs/heads/main/README.md
import: https://raw.githubusercontent.com/liaTemplates/algebrite/master/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-canvas-ocr/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-orthography/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-Mathe/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-kachel/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-navigation/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-freeze-v2/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-mathpath/refs/heads/master/README.md

import: https://raw.githubusercontent.com/MINT-the-GAP/lia-llm/refs/heads/main/README.md

import: https://raw.githubusercontent.com/liaTemplates/JSXGraph/main/README.md

import: https://raw.githubusercontent.com/MINT-the-GAP/lia-coordinate/refs/heads/main/README.md

import: https://raw.githubusercontent.com/MINT-the-GAP/lia-loot/main/README.md

import: https://raw.githubusercontent.com/MINT-the-GAP/lia-pentominos/main/README.md


-->

# Probeklausur Klasse 11 – Analysisübungen

> Letztes Update am 30.09.2026

Swipe (Wische) entweder weiter oder klicke unten links neben der Seitenzahl auf den Pfeil nach rechts.

Diese Probearbeit enthält neue Aufgaben zu denselben Themenbereichen wie die erste Variante. Sie umfasst mehr Aufgaben als die eigentliche Klassenarbeit, damit du die verschiedenen Aufgabentypen ausführlich üben kannst.

---

**Aufgaben 1–5:** ohne Taschenrechner.

**Aufgaben 6–10:** mit Taschenrechner und zugelassener Formelsammlung.

## Aufgabe 1: Grundlegende Ableitungen

**Bestimme** jeweils die erste Ableitung.

<section class="dynFlex" data-basis="48" data-min="30">

<div class="flex-child">

__$a)\;\;$__ $f(x)=3x^5-4x^3+2x-6$

<!-- data-hint-button="2" data-solution-button="3" -->
$f'(x)=$ [[ 15*x^4-12*x^2+2 ]] @canvas
@Algebrite.check(`15*x^4-12*x^2+2`)
[[?]] Leite jeden Summanden mit der Potenzregel ab. Der konstante Summand fällt weg.
[[?]] @Explain
*****************
$$
f'(x)=15x^4-12x^2+2.
$$
*****************

@ADetails(`1=BE;Potenzen, Ableitungen, Potenzregel`)

</div>

<div class="flex-child">

__$b)\;\;$__ $g(x)=\dfrac23x^6+3x^4-7x+5$

<!-- data-hint-button="2" data-solution-button="3" -->
$g'(x)=$ [[ 4*x^5+12*x^3-7 ]] @canvas
@Algebrite.check(`4*x^5+12*x^3-7`)
[[?]] Multipliziere jeden Koeffizienten mit dem zugehörigen Exponenten.
[[?]] @Explain
*****************
$$
g'(x)=4x^5+12x^3-7.
$$
*****************

@ADetails(`1=BE;Potenzen, Ableitungen, Bruchkoeffizienten`)

</div>

</section>

<section class="dynFlex" data-basis="48" data-min="30">

<div class="flex-child">

__$c)\;\;$__ $h(x)=-\dfrac34x^4+\dfrac52x^2-9$

<!-- data-hint-button="2" data-solution-button="3" -->
$h'(x)=$ [[ -3*x^3+5*x ]] @canvas
@Algebrite.check(`-3*x^3+5*x`)
[[?]] Konstante Faktoren bleiben beim Ableiten erhalten. Die Ableitung einer Konstanten ist null.
[[?]] @Explain
*****************
$$
h'(x)=-3x^3+5x.
$$
*****************

@ADetails(`1=BE;Potenzen, Ableitungen, Potenzregel`)

</div>

<div class="flex-child">

__$d)\;\;$__ $k(x)=\dfrac27x^7-5x^3+4x$

<!-- data-hint-button="2" data-solution-button="3" -->
$k'(x)=$ [[ 2*x^6-15*x^2+4 ]] @canvas
@Algebrite.check(`2*x^6-15*x^2+4`)
[[?]] Verringere nach dem Multiplizieren den jeweiligen Exponenten um eins.
[[?]] @Explain
*****************
$$
k'(x)=2x^6-15x^2+4.
$$
*****************

@ADetails(`1=BE;Potenzen, Ableitungen, Potenzregel`)

</div>

</section>

## Aufgabe 2: Höhere Ableitungen von Polynomfunktionen

<section class="dynFlex" data-basis="48" data-min="30">

<div class="flex-child">

__$a)\;\;$__ **Bestimme** die erste und die zweite Ableitung von

$$
p(x)=\frac13x^6-2x^4+3x^2-5.
$$

<!-- data-hint-button="2" data-solution-button="3" -->
$p'(x)=$ [[ 2*x^5-8*x^3+6*x ]] @canvas, $\qquad p''(x)=$ [[ 10*x^4-24*x^2+6 ]] @canvas
@Algebrite.check(`[2*x^5-8*x^3+6*x;10*x^4-24*x^2+6]`)
[[?]] Leite die Polynomfunktion zunächst einmal und das Ergebnis anschließend ein zweites Mal ab.
[[?]] @Explain
*****************
$$
\begin{aligned}
p'(x)&=2x^5-8x^3+6x,\\
p''(x)&=10x^4-24x^2+6.
\end{aligned}
$$
*****************

@ADetails(`2=BE;Potenzen, Ableitungen, Erste und zweite Ableitung`)

</div>

<div class="flex-child">

__$b)\;\;$__ **Bestimme** die erste und die zweite Ableitung von

$$
q(x)=-\frac12x^5+3x^3-4x+2.
$$

<!-- data-hint-button="2" data-solution-button="3" -->
$q'(x)=$ [[ -5/2*x^4+9*x^2-4 ]] @canvas, $\qquad q''(x)=$ [[ -10*x^3+18*x ]] @canvas
@Algebrite.check(`[-5/2*x^4+9*x^2-4;-10*x^3+18*x]`)
[[?]] Beachte, dass die Ableitung des konstanten Summanden null ist.
[[?]] @Explain
*****************
$$
\begin{aligned}
q'(x)&=-\frac52x^4+9x^2-4,\\
q''(x)&=-10x^3+18x.
\end{aligned}
$$
*****************

@ADetails(`2=BE;Potenzen, Ableitungen, Erste und zweite Ableitung`)

</div>

</section>

## Aufgabe 3: Tangente

Gegeben ist die Funktion

$$
p(x)=x^3-x^2-2x+4.
$$

**Bestimme** die Gleichung der Tangente an den Graphen von $p$ an der Stelle $x_0=2$.

<!-- data-hint-button="2" data-solution-button="3" -->
$t(x)=$ [[ 6*x-8 ]] @canvas
@Algebrite.check(`6*x-8`)
[[?]] Berechne $p(2)$ und $p'(2)$. Verwende anschließend die Punkt-Steigungs-Gleichung.
[[?]] @Explain
*****************
$$
p'(x)=3x^2-2x-2,\qquad p(2)=4,\qquad p'(2)=6.
$$

Damit gilt:

$$
t(x)=6(x-2)+4=6x-8.
$$
*****************

@ADetails(`4=BE;Gleichung, Tangente, Ableitungswert`)

## Aufgabe 4: Ableitung und Monotonie

Von einer differenzierbaren Funktion $f$ ist bekannt:

$$
f'(x)=(x+4)(x-2).
$$

**Wähle** die richtige Aussage aus.

<!-- data-hint-button="2" data-solution-button="3" -->
[(X)] $f$ steigt für $x<-4$ und $x>2$, fällt für $-4<x<2$, besitzt bei $x=-4$ einen lokalen Hochpunkt und bei $x=2$ einen lokalen Tiefpunkt.
[( )] $f$ fällt für $x<-4$ und $x>2$, steigt für $-4<x<2$, besitzt bei $x=-4$ einen lokalen Tiefpunkt und bei $x=2$ einen lokalen Hochpunkt.
[( )] $f$ steigt für alle reellen Zahlen und besitzt keine lokalen Extrempunkte.
[( )] $f$ fällt für alle reellen Zahlen und besitzt keine lokalen Extrempunkte.
[[?]] Untersuche das Vorzeichen der beiden Faktoren in den drei Intervallen.
[[?]] @Explain
*****************
Für $x<-4$ sind beide Faktoren negativ, also ist $f'(x)>0$. Zwischen $-4$ und $2$ ist genau ein Faktor negativ, also ist $f'(x)<0$. Für $x>2$ sind beide Faktoren positiv.

Damit wechselt $f'$ bei $x=-4$ von positiv zu negativ und bei $x=2$ von negativ zu positiv. Folglich liegt bei $x=-4$ ein lokaler Hochpunkt und bei $x=2$ ein lokaler Tiefpunkt vor.
*****************

@ADetails(`4=BE;Negative Zahlen, Ableitung, Monotonie, Extremstellen`)

## Aufgabe 5: Tangenten, Extrempunkte und Wendepunkte

**Wähle** alle mathematisch richtigen Aussagen aus.

<!-- data-hint-button="2" data-solution-button="3" -->
[[X]] Eine Tangente in einem Wendepunkt kann eine von null verschiedene Steigung besitzen.
[[ ]] Jeder Wendepunkt besitzt eine waagerechte Tangente.
[[X]] Wechselt $f'$ an einer Stelle von negativ zu positiv, besitzt $f$ dort einen lokalen Tiefpunkt.
[[X]] Ist eine Funktion an einer inneren lokalen Maximalstelle differenzierbar, gilt dort $f'(x)=0$.
[[?]] Unterscheide zwischen Steigung, Krümmungsverhalten und Vorzeichenwechsel der ersten Ableitung.
[[?]] @Explain
*****************
Richtig sind die erste, dritte und vierte Aussage.

Ein Wendepunkt beschreibt einen Wechsel des Krümmungsverhaltens; seine Tangente muss nicht waagerecht sein. Ein Vorzeichenwechsel von $f'$ von negativ zu positiv kennzeichnet einen lokalen Tiefpunkt. An einer inneren differenzierbaren lokalen Extremstelle ist die Ableitung null.
*****************

@ADetails(`4=BE;Gleichung, Tangente, Wendepunkt, Extremstelle`)

## Aufgabe 6: Geführte Kurvendiskussion

Gegeben ist die Funktion

$$
f(x)=\frac14x^3-\frac34x^2-\frac94x+\frac{11}{4}.
$$

<section class="dynFlex" data-basis="48" data-min="30">

<div class="flex-child">

__$a)\;\;$__ **Gib** den Definitionsbereich $D_f$ und den Wertebereich $W_f$ **an**.

<!-- data-hint-button="2" data-solution-button="3" -->
$D_f=$ [[($\mathbb{R}$)|$[-2;6]$|$[0;\infty)$]], $W_f=$ [[($\mathbb{R}$)|$[-4;4]$|$[0;\infty)$]]
[[?]] $f$ ist eine Polynomfunktion dritten Grades mit positivem Leitkoeffizienten.
[[?]] @Explain
*****************
Für eine Polynomfunktion gilt $D_f=\mathbb R$. Wegen des ungeraden Grades und des positiven Leitkoeffizienten nimmt $f$ beliebig kleine und beliebig große Werte an. Daher ist auch $W_f=\mathbb R$.
*****************

@ADetails(`2=BE;Mengen, Kurvendiskussion, Definitionsbereich, Wertebereich`)

</div>

<div class="flex-child">

__$b)\;\;$__ **Berechne** den Schnittpunkt des Graphen mit der Ordinatenachse.

<!-- data-hint-button="2" data-solution-button="3" -->
$S_y=(0\mid$ [[ 11/4 ]] @canvas $)$
@Algebrite.check(`11/4`)
[[?]] Setze $x=0$ in den Funktionsterm ein.
[[?]] @Explain
*****************
$$
f(0)=\frac{11}{4}.
$$

Der Graph schneidet die Ordinatenachse im Punkt

$$
S_y\left(0\,\middle|\,\frac{11}{4}\right).
$$
*****************

@ADetails(`1=BE;Terme, Kurvendiskussion, Ordinatenachsenabschnitt`)

</div>

<div class="flex-child">

__$c)\;\;$__ **Untersuche**, ob der Graph symmetrisch zur Ordinatenachse oder zum Ursprung ist.

<!-- data-hint-button="2" data-solution-button="3" -->
[( )] Der Graph ist symmetrisch zur Ordinatenachse.
[( )] Der Graph ist symmetrisch zum Ursprung.
[(X)] Keine der beiden Symmetrien liegt vor.
[[?]] Vergleiche $f(-x)$ mit $f(x)$ und mit $-f(x)$.
[[?]] @Explain
*****************
Es gilt

$$
f(-x)=-\frac14x^3-\frac34x^2+\frac94x+\frac{11}{4}.
$$

Dieser Term stimmt weder mit $f(x)$ noch mit $-f(x)$ überein. Der Graph ist weder zur Ordinatenachse noch zum Ursprung symmetrisch.
*****************

@ADetails(`2=BE;Terme, Kurvendiskussion, Symmetrie`)

</div>

<div class="flex-child">

__$d)\;\;$__ **Bestimme** das Verhalten von $f$ für $x\to-\infty$ und $x\to+\infty$.

<!-- data-hint-button="2" data-solution-button="3" -->
[[
(Der Graph verläuft links nach unten und rechts nach oben.)
|Der Graph verläuft links nach oben und rechts nach unten.
|Der Graph verläuft links und rechts nach oben.
|Der Graph verläuft links und rechts nach unten.
]]
[[?]] Für große Beträge von $x$ bestimmt der Summand $\frac14x^3$ das Verhalten.
[[?]] @Explain
*****************
Der Summand höchsten Grades ist $\frac14x^3$. Deshalb gilt:

$$
\lim_{x\to-\infty}f(x)=-\infty,\qquad
\lim_{x\to+\infty}f(x)=+\infty.
$$
*****************

@ADetails(`2=BE;Potenzen, Kurvendiskussion, Verhalten im Unendlichen`)

</div>

</section>

<section class="dynFlex" data-basis="48" data-min="30">

<div class="flex-child">

__$e)\;\;$__ **Berechne** die Nullstellen von $f$.

<!-- data-hint-button="2" data-solution-button="3" -->
$x_1=$ [[ 1-2*sqrt(3) ]] @canvas, $\quad x_2=$ [[ 1 ]] @canvas, $\quad x_3=$ [[ 1+2*sqrt(3) ]] @canvas
@Algebrite.check(`[1-2*sqrt(3);1;1+2*sqrt(3)]`)
[[?]] Schreibe den Funktionsterm mithilfe der Substitution $u=x-1$ um und faktorisiere.
[[?]] @Explain
*****************
Mit $u=x-1$ gilt:

$$
f(x)=\frac14u^3-3u=\frac14u(u^2-12).
$$

Damit ist $u=0$ oder $u=\pm2\sqrt3$. Wegen $x=u+1$ lauten die Nullstellen:

$$
x_1=1-2\sqrt3,\qquad x_2=1,\qquad x_3=1+2\sqrt3.
$$
*****************

@ADetails(`4=BE;Gleichung, Kurvendiskussion, Nullstellen, Faktorisieren`)

</div>

<div class="flex-child">

__$f)\;\;$__ **Berechne** die Extrempunkte von $f$ und **bestimme** ihre Art.

<!-- data-hint-button="2" data-solution-button="3" -->
$H($ [[ -1 ]] @canvas $\mid$ [[ 4 ]] @canvas $)$, $\qquad T($ [[ 3 ]] @canvas $\mid$ [[ -4 ]] @canvas $)$
@Algebrite.check(`[-1;4;3;-4]`)
[[?]] Löse $f'(x)=0$ und untersuche das Vorzeichen von $f''$ an den beiden Stellen.
[[?]] @Explain
*****************
$$
f'(x)=\frac34x^2-\frac32x-\frac94
=\frac34(x+1)(x-3),
\qquad
f''(x)=\frac32x-\frac32.
$$

Für $x=-1$ ist $f''(-1)<0$, für $x=3$ ist $f''(3)>0$. Mit $f(-1)=4$ und $f(3)=-4$ erhält man:

$$
H(-1\mid4),\qquad T(3\mid-4).
$$
*****************

@ADetails(`5=BE;Gleichung, Kurvendiskussion, Extrempunkte, Ableitungen`)

</div>

<div class="flex-child">

__$g)\;\;$__ **Berechne** den Wendepunkt von $f$.

<!-- data-hint-button="2" data-solution-button="3" -->
$W($ [[ 1 ]] @canvas $\mid$ [[ 0 ]] @canvas $)$
@Algebrite.check(`[1;0]`)
[[?]] Löse $f''(x)=0$ und prüfe die Stelle mit $f'''(x)$.
[[?]] @Explain
*****************
$$
f''(x)=\frac32x-\frac32
\quad\Longrightarrow\quad
f''(x)=0\iff x=1.
$$

Da $f'''(x)=\frac32\ne0$ und $f(1)=0$ gilt, lautet der Wendepunkt:

$$
W(1\mid0).
$$

Mit $u=x-1$ gilt $f(x)=\frac14u^3-3u$. Daher ist der Graph punktsymmetrisch zum Wendepunkt $W$.
*****************

@ADetails(`4=BE;Gleichung, Kurvendiskussion, Wendepunkt, Ableitungen`)

</div>

</section>

## Aufgabe 7: Modellierung – Besucherzahlen eines Jugendzentrums

Die wöchentliche Besucherzahl eines Jugendzentrums wird während einer zehnwöchigen Veranstaltungsreihe durch

$$
N(t)=-0{,}025t^3+0{,}30t^2+0{,}60t+1
$$

modelliert. Dabei ist $t$ die Zeit in Wochen seit dem Start und $N(t)$ die Besucherzahl in Tausend. Das Modell wird für $0\le t\le10$ verwendet.

In der sechsten Woche wird eine Prognose für die neunte Woche erstellt.

<section class="dynFlex" data-basis="48" data-min="30">

<div class="flex-child">

__$a)\;\;$__ **Berechne** die Modellwerte zum Start und nach sechs Wochen.

<!-- data-hint-button="2" data-solution-button="3" -->
$N(0)=$ [[ 1 ]] @canvas, $\qquad N(6)=$ [[ 10 ]] @canvas
@Algebrite.check(`[1;10]`)
[[?]] Setze $t=0$ beziehungsweise $t=6$ in die Funktionsgleichung ein.
[[?]] @Explain
*****************
$$
N(0)=1,\qquad
N(6)=-0{,}025\cdot6^3+0{,}30\cdot6^2+0{,}60\cdot6+1=10.
$$

Zum Start entspricht der Modellwert $1000$ Besuchen pro Woche, nach sechs Wochen $10\,000$ Besuchen pro Woche.
*****************

@ADetails(`3=BE;Terme, Modellierung, Funktionswerte`)

</div>

<div class="flex-child">

__$b)\;\;$__ **Bestimme** im Modellzeitraum den Zeitpunkt, zu dem die Besucherzahl maximal ist, und **berechne** den maximalen Modellwert. Runde auf zwei Nachkommastellen.

<!-- data-hint-button="2" data-solution-button="3" -->
$t_{\max}\approx$ [[ 8,90 ]] @canvas, $\qquad N_{\max}\approx$ [[ 12,48 ]] @canvas
@Algebrite.check2(`[8.8989794856;12.4787753827]`,`[0.015;0.015]`,units=0)
[[?]] Löse $N'(t)=0$, berücksichtige nur Lösungen im Modellzeitraum und vergleiche mit den Randwerten.
[[?]] @Explain
*****************
$$
N'(t)=-0{,}075t^2+0{,}60t+0{,}60.
$$

Aus $N'(t)=0$ folgt:

$$
t=4\pm2\sqrt6.
$$

Nur

$$
t_{\max}=4+2\sqrt6\approx8{,}90
$$

liegt im Modellzeitraum. Dort wechselt $N'$ von positiv zu negativ. Es gilt:

$$
N(t_{\max})\approx12{,}48.
$$

Die maximale Besucherzahl beträgt nach dem Modell etwa $12\,480$ Besuche pro Woche.
*****************

@ADetails(`5=BE;Runden, Modellierung, Maximum, Ableitungen`)

</div>

</section>

<section class="dynFlex" data-basis="48" data-min="30">

<div class="flex-child">

__$c)\;\;$__ **Bestimme** den Wendepunkt des Modells und die momentane Änderungsrate an dieser Stelle. **Interpretiere** die Ergebnisse im Sachzusammenhang.

<!-- data-hint-button="2" data-solution-button="3" -->
$t_W=$ [[ 4 ]] @canvas, $\quad N(t_W)=$ [[ 6,6 ]] @canvas, $\quad N'(t_W)=$ [[ 1,8 ]] @canvas
@Algebrite.check2(`[4;6.6;1.8]`,`[0.005;0.005;0.005]`,units=0)
[[?]] Löse $N''(t)=0$. Setze den Zeitpunkt anschließend in $N$ und $N'$ ein.
[[?]] @Explain
*****************
$$
N''(t)=-0{,}15t+0{,}60.
$$

Daraus folgt $N''(t)=0$ für $t=4$. Weiter gilt:

$$
N(4)=6{,}6,\qquad N'(4)=1{,}8.
$$

Nach vier Wochen entspricht der Modellwert $6600$ Besuchen pro Woche. Zu diesem Zeitpunkt ist die Zunahme der wöchentlichen Besucherzahl mit $1800$ Besuchen pro Woche und Woche am größten. Danach steigt die Besucherzahl zunächst weiter, die momentane Zunahme wird jedoch kleiner.
*****************

@ADetails(`4=BE;Terme, Modellierung, Wendepunkt, Änderungsrate`)

</div>

<div class="flex-child">

__$d)\;\;$__ **Bestimme** die Tangente an den Graphen von $N$ an der Stelle $t=6$. **Verwende** diese Tangente als lineare Prognose für die neunte Woche.

<!-- data-hint-button="2" data-solution-button="3" -->
$T(t)=$ [[ 1.5*t+1 ]] @canvas, $\qquad T(9)=$ [[ 14,5 ]] @canvas
@Algebrite.check(`[1.5*t+1;14.5]`)
[[?]] Berechne $N(6)$ und $N'(6)$. Setze beide Werte in $T(t)=N'(6)(t-6)+N(6)$ ein.
[[?]] @Explain
*****************
$$
N(6)=10,\qquad N'(6)=1{,}5.
$$

Damit lautet die Tangente:

$$
T(t)=1{,}5(t-6)+10=1{,}5t+1.
$$

Die lineare Prognose für die neunte Woche ist:

$$
T(9)=14{,}5.
$$

Die Tangente prognostiziert somit $14\,500$ Besuche pro Woche.
*****************

@ADetails(`5=BE;Gleichung, Modellierung, Tangente, Lineare Prognose`)

</div>

</section>

<section class="dynFlex" data-basis="48" data-min="30">

<div class="flex-child">

__$e)\;\;$__ **Vergleiche** die tangentiale Prognose aus d) mit dem Modellwert $N(9)$. **Berechne** die absolute Abweichung der Modellwerte und **beurteile** die Prognose. Runde auf zwei Nachkommastellen.

<!-- data-hint-button="2" data-solution-button="3" -->
$N(9)\approx$ [[ 12,48 ]] @canvas, $\qquad$ absolute Abweichung: [[ 2,03 ]] @canvas
@Algebrite.check2(`[12.475;2.025]`,`[0.015;0.015]`,units=0)
[[?]] Berechne zuerst $N(9)$ und bilde anschließend den Betrag der Differenz zu $T(9)$.
[[?]] @Explain
*****************
$$
N(9)=-0{,}025\cdot9^3+0{,}30\cdot9^2+0{,}60\cdot9+1=12{,}475.
$$

$$
\left|T(9)-N(9)\right|
=|14{,}5-12{,}475|
=2{,}025.
$$

Die Tangente überschätzt den Modellwert um etwa $2030$ Besuche pro Woche.
*****************

**Wähle** die passende Beurteilung aus.

<!-- data-hint-button="2" data-solution-button="3" -->
[(X)] Die Tangente überschätzt den Modellwert, weil die momentane Zunahme nach der sechsten Woche weiter abnimmt.
[( )] Die Tangente unterschätzt den Modellwert, weil die momentane Zunahme nach der sechsten Woche größer wird.
[( )] Die Tangente liefert für alle späteren Wochen exakt dieselben Werte wie das kubische Modell.
[[?]] Untersuche das Vorzeichen von $N''(t)$ für $t>6$.
[[?]] @Explain
*****************
Für $t>6$ ist $N''(t)<0$. Die Steigung des Modellgraphen nimmt also ab. Die Tangente setzt dagegen die Steigung aus der sechsten Woche unverändert fort und liegt deshalb in der neunten Woche über dem Modellgraphen.

Eine Tangente ist nur eine lokale lineare Näherung. Mit wachsendem Abstand vom Berührpunkt kann die Abweichung größer werden.
*****************

@ADetails(`3=BE;Negative Zahlen, Modellierung, Prognose, Abweichung`)

</div>

</section>

## Aufgabe 8: Extrempunkte

**Berechne** jeweils alle Extrempunkte und **bestimme** ihre Art.

<section class="dynFlex" data-basis="48" data-min="30">

<div class="flex-child">

__$a)\;\;$__ $f(x)=x^3-12x+1$

<!-- data-hint-button="2" data-solution-button="3" -->
$H($ [[ -2 ]] @canvas $\mid$ [[ 17 ]] @canvas $)$, $\qquad T($ [[ 2 ]] @canvas $\mid$ [[ -15 ]] @canvas $)$
@Algebrite.check(`[-2;17;2;-15]`)
[[?]] Löse $f'(x)=0$ und untersuche das Vorzeichen von $f''$ an den gefundenen Stellen.
[[?]] @Explain
*****************
$$
f'(x)=3x^2-12=3(x-2)(x+2),\qquad f''(x)=6x.
$$

Damit sind $x=-2$ und $x=2$ die möglichen Extremstellen. Es gilt:

$$
f''(-2)<0,\qquad f''(2)>0.
$$

Mit $f(-2)=17$ und $f(2)=-15$ erhält man:

$$
H(-2\mid17),\qquad T(2\mid-15).
$$
*****************

@ADetails(`3=BE;Gleichung, Extrempunkte, Ableitungen, Klassifikation`)

</div>

<div class="flex-child">

__$b)\;\;$__ $g(x)=\dfrac14x^4-\dfrac92x^2+2$

<!-- data-hint-button="2" data-solution-button="3" -->
$T_1($ [[ -3 ]] @canvas $\mid$ [[ -73/4 ]] @canvas $)$, $\quad H($ [[ 0 ]] @canvas $\mid$ [[ 2 ]] @canvas $)$, $\quad T_2($ [[ 3 ]] @canvas $\mid$ [[ -73/4 ]] @canvas $)$
@Algebrite.check(`[-3;-73/4;0;2;3;-73/4]`)
[[?]] Faktorisiere $g'(x)$ vollständig. Es entstehen drei mögliche Extremstellen.
[[?]] @Explain
*****************
$$
g'(x)=x^3-9x=x(x-3)(x+3),\qquad g''(x)=3x^2-9.
$$

Aus $g'(x)=0$ folgen $x=-3$, $x=0$ und $x=3$. Wegen

$$
g''(-3)>0,\qquad g''(0)<0,\qquad g''(3)>0
$$

und $g(-3)=g(3)=-\frac{73}{4}$ sowie $g(0)=2$ lauten die Extrempunkte:

$$
T_1\left(-3\,\middle|\,-\frac{73}{4}\right),\quad
H(0\mid2),\quad
T_2\left(3\,\middle|\,-\frac{73}{4}\right).
$$
*****************

@ADetails(`3=BE;Potenzen, Extrempunkte, Polynomfunktion vierten Grades`)

</div>

</section>

<section class="dynFlex" data-basis="48" data-min="30">

<div class="flex-child">

__$c)\;\;$__ $h(x)=\dfrac13x^3-\dfrac32x^2-4x+1$

Runde die Ordinaten der Extrempunkte auf zwei Nachkommastellen.

<!-- data-hint-button="2" data-solution-button="3" -->
$H($ [[ -1 ]] @canvas $\mid$ [[ 3,17 ]] @canvas $)$, $\qquad T($ [[ 4 ]] @canvas $\mid$ [[ -17,67 ]] @canvas $)$
@Algebrite.check2(`[-1;3.1666666667;4;-17.6666666667]`,`[0.015;0.015;0.015;0.015]`,units=0)
[[?]] Die Gleichung $h'(x)=0$ lässt sich faktorisieren.
[[?]] @Explain
*****************
$$
h'(x)=x^2-3x-4=(x+1)(x-4),\qquad h''(x)=2x-3.
$$

Somit liegt bei $x=-1$ ein Hochpunkt und bei $x=4$ ein Tiefpunkt vor. Die Funktionswerte sind:

$$
h(-1)=\frac{19}{6}\approx3{,}17,\qquad
h(4)=-\frac{53}{3}\approx-17{,}67.
$$

Also gilt:

$$
H(-1\mid3{,}17),\qquad T(4\mid-17{,}67).
$$
*****************

@ADetails(`3=BE;Runden, Extrempunkte, Faktorisieren`)

</div>

</section>

## Aufgabe 9: Wendepunkte

**Berechne** jeweils alle Wendepunkte.

<section class="dynFlex" data-basis="48" data-min="30">

<div class="flex-child">

__$a)\;\;$__ $p(x)=x^3-3x^2+2x+4$

<!-- data-hint-button="2" data-solution-button="3" -->
$W($ [[ 1 ]] @canvas $\mid$ [[ 4 ]] @canvas $)$
@Algebrite.check(`[1;4]`)
[[?]] Löse $p''(x)=0$ und überprüfe die Stelle mithilfe von $p'''(x)$.
[[?]] @Explain
*****************
$$
p''(x)=6x-6
\quad\Longrightarrow\quad
p''(x)=0\iff x=1.
$$

Da $p'''(x)=6\ne0$ und $p(1)=4$ gilt, lautet der Wendepunkt:

$$
W(1\mid4).
$$
*****************

@ADetails(`3=BE;Gleichung, Wendepunkt, Zweite und dritte Ableitung`)

</div>

<div class="flex-child">

__$b)\;\;$__ $q(x)=\dfrac14x^4-\dfrac{27}{8}x^2+2x+1$

Runde die Koordinaten auf zwei Nachkommastellen.

<!-- data-hint-button="2" data-solution-button="3" -->
$W_1($ [[ -1,5 ]] @canvas $\mid$ [[ -8,33 ]] @canvas $)$, $\qquad W_2($ [[ 1,5 ]] @canvas $\mid$ [[ -2,33 ]] @canvas $)$
@Algebrite.check2(`[-1.5;-8.328125;1.5;-2.328125]`,`[0.015;0.015;0.015;0.015]`,units=0)
[[?]] Aus $q''(x)=0$ entstehen zwei Lösungen. Berechne anschließend beide Funktionswerte.
[[?]] @Explain
*****************
$$
q''(x)=3x^2-\frac{27}{4}
\quad\Longrightarrow\quad
x=\pm\frac32.
$$

Da $q'''(x)=6x$ an beiden Stellen ungleich null ist, liegen zwei Wendestellen vor. Die exakten Punkte sind:

$$
W_1\left(-\frac32\,\middle|\,-\frac{533}{64}\right),\qquad
W_2\left(\frac32\,\middle|\,-\frac{149}{64}\right).
$$

Gerundet erhält man:

$$
W_1(-1{,}50\mid-8{,}33),\qquad
W_2(1{,}50\mid-2{,}33).
$$
*****************

@ADetails(`3=BE;Runden, Wendepunkte, Polynomfunktion vierten Grades`)

</div>

</section>

<section class="dynFlex" data-basis="48" data-min="30">

<div class="flex-child">

__$c)\;\;$__ $r(x)=-\dfrac13x^3+2x^2+x-3$

<!-- data-hint-button="2" data-solution-button="3" -->
$W($ [[ 2 ]] @canvas $\mid$ [[ 13/3 ]] @canvas $)$
@Algebrite.check(`[2;13/3]`)
[[?]] Löse $r''(x)=0$ und setze die gefundene Stelle anschließend in $r$ ein.
[[?]] @Explain
*****************
$$
r''(x)=-2x+4
\quad\Longrightarrow\quad
r''(x)=0\iff x=2.
$$

Wegen $r'''(x)=-2\ne0$ liegt dort eine Wendestelle vor. Außerdem gilt $r(2)=\frac{13}{3}$. Damit lautet der Wendepunkt:

$$
W\left(2\,\middle|\,\frac{13}{3}\right).
$$
*****************

@ADetails(`3=BE;Gleichung, Wendepunkt, Bruchkoordinaten`)

</div>

</section>

## Aufgabe 10: Tangenten

<section class="dynFlex" data-basis="48" data-min="30">

<div class="flex-child">

__$a)\;\;$__ Gegeben ist $p(x)=\dfrac13x^3-x^2-2x+5$.

**Bestimme** die Tangente an den Graphen von $p$ an der Stelle $x_0=3$.

<!-- data-hint-button="2" data-solution-button="3" -->
$t(x)=$ [[ x-4 ]] @canvas
@Algebrite.check(`x-4`)
[[?]] Berechne $p(3)$ und $p'(3)$ und verwende die Punkt-Steigungs-Gleichung.
[[?]] @Explain
*****************
$$
p'(x)=x^2-2x-2,\qquad p(3)=-1,\qquad p'(3)=1.
$$

Damit gilt:

$$
t(x)=x-3-1=x-4.
$$
*****************

@ADetails(`3=BE;Gleichung, Tangente, Ableitungswert`)

</div>

<div class="flex-child">

__$b)\;\;$__ Gegeben ist $q(x)=-\dfrac12x^4+x^2-3x+2$.

**Bestimme** die Tangente an den Graphen von $q$ an der Stelle $x_0=-1$.

<!-- data-hint-button="2" data-solution-button="3" -->
$t(x)=$ [[ -3*x+5/2 ]] @canvas
@Algebrite.check(`-3*x+5/2`)
[[?]] Bestimme den Berührpunkt und die Steigung der Tangente bei $x_0=-1$.
[[?]] @Explain
*****************
$$
q'(x)=-2x^3+2x-3,\qquad
q(-1)=\frac{11}{2},\qquad
q'(-1)=-3.
$$

Somit lautet die Tangente:

$$
t(x)=-3(x+1)+\frac{11}{2}=-3x+\frac52.
$$
*****************

@ADetails(`3=BE;Gleichung, Tangente, Polynomfunktion vierten Grades`)

</div>

</section>

<section class="dynFlex" data-basis="48" data-min="30">

<div class="flex-child">

__$c)\;\;$__ Gegeben sind

$$
r(x)=x^3-3x^2-4x+2
$$

und die Gerade $k(x)=-x+2$.

**Bestimme** die beiden Stellen, an denen die Tangenten an den Graphen von $r$ parallel zu $k$ verlaufen. Die Tangenten haben die Form $t_i(x)=-x+b_i$. Runde die gesuchten Werte auf zwei Nachkommastellen.

<!-- data-hint-button="2" data-solution-button="3" -->
$x_1\approx$ [[ -0,41 ]] @canvas, $\quad b_1\approx$ [[ 2,66 ]] @canvas, $\qquad x_2\approx$ [[ 2,41 ]] @canvas, $\quad b_2\approx$ [[ -8,66 ]] @canvas
@Algebrite.check2(`[-0.4142135624;2.6568542495;2.4142135624;-8.6568542495]`,`[0.015;0.015;0.015;0.015]`,units=0)
[[?]] Parallele Geraden besitzen dieselbe Steigung. Löse daher $r'(x)=-1$.
[[?]] @Explain
*****************
$$
r'(x)=3x^2-6x-4.
$$

Aus $r'(x)=-1$ folgt:

$$
3x^2-6x-3=0
\quad\Longrightarrow\quad
x_{1,2}=1\pm\sqrt2.
$$

Für $x_1=1-\sqrt2$ ergibt sich $b_1=-3+4\sqrt2$, für $x_2=1+\sqrt2$ gilt $b_2=-3-4\sqrt2$. Damit lauten die beiden Tangenten:

$$
t_1(x)=-x-3+4\sqrt2,\qquad
t_2(x)=-x-3-4\sqrt2.
$$

Gerundet erhält man:

$$
x_1\approx-0{,}41,\quad b_1\approx2{,}66,\qquad
x_2\approx2{,}41,\quad b_2\approx-8{,}66.
$$
*****************

@ADetails(`3=BE;Runden, Tangenten, Parallelität, Ableitungswert`)

</div>

</section>
