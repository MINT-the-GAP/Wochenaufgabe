<!--
author: Martin Lommatzsch
version: 0.2.0
language: de
narrator: Deutsch Female
mode: Presentation
comment: Probeklausur für Klasse 11 zur Analysis mit Ableitungen, Kurvendiskussion und Modellierung.
tags: Mathematik, Klasse 11, Probeklausur, Analysis, Ableitungen, Kurvendiskussion, Modellierung




import: https://raw.githubusercontent.com/MINT-the-GAP/lia-DynFlex/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-timer/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-board-mode/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-marker/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-annotation/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-canvas-ocr/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-orthography/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-Mathe/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-navigation/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-kachel/refs/heads/main/README.md

import: https://raw.githubusercontent.com/MINT-the-GAP/lia-llm/refs/heads/main/README.md

import: https://raw.githubusercontent.com/liaTemplates/algebrite/master/README.md
import: https://raw.githubusercontent.com/liaTemplates/JSXGraph/main/README.md

import: https://raw.githubusercontent.com/MINT-the-GAP/lia-resetter/main/README.md

import: https://raw.githubusercontent.com/MINT-the-GAP/lia-coordinate/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-mathpath/refs/heads/master/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-freeze-v2/main/README.md
-->

# Probeklausur Klasse 11 – Analysis




> Letztes Update am 20.09.2026 gegen 18:00 Uhr


Swipe (Wische) entweder weiter oder klicke unten links auf neben der Seitenzahl auf den Pfeil nach rechts.


Diese Probearbeit hat mehr Aufgaben als die richtige Arbeit, damit du genug zum Üben hast. Es sind viele verschiedene Aufgabentypen abgebildet, sodass du alles nochmal bei der Bearbeitung dieser Aufgaben wiederholst.

---

---


**Aufgaben 1–5:** ohne Taschenrechner.

**Aufgaben 6–10:** mit Taschenrechner und zugelassener Formelsammlung.



## Aufgabe 1: Grundlegende Ableitungen

**Bestimme** jeweils die erste Ableitung.

<section class="dynFlex" data-basis="48" data-min="30">

<div class="flex-child">

__$a)\;\;$__ $f(x)=5x^4-3x^2+7x-4$

<!-- data-hint-button="2" data-solution-button="3" -->
$f'(x)=$ [[ 20*x^3-6*x+7 ]]
@Algebrite.check(`20*x^3-6*x+7`)
[[?]] Leite jeden Summanden mit der Potenzregel ab. Der konstante Summand fällt weg.
*****************
$$
f'(x)=20x^3-6x+7.
$$
*****************

@resetter

@ADetails(`1=BE;Ableitungen, Polynomfunktionen, Potenzregel`)

</div>

<div class="flex-child">

__$b)\;\;$__ $g(x)=\dfrac34x^6-2x^3+5x-1$

<!-- data-hint-button="2" data-solution-button="3" -->
$g'(x)=$ [[ 9/2*x^5-6*x^2+5 ]]
@Algebrite.check(`9/2*x^5-6*x^2+5`)
[[?]] Leite jeden Summanden einzeln mit der Potenzregel ab.
*****************
$$
g'(x)=\frac92x^5-6x^2+5.
$$
*****************

@resetter

@ADetails(`1=BE;Ableitungen, Polynomfunktionen, Potenzregel`)

</div>

</section>

<section class="dynFlex" data-basis="48" data-min="30">

<div class="flex-child">

__$c)\;\;$__ $h(x)=-\dfrac25x^5+\dfrac32x^2-8$

<!-- data-hint-button="2" data-solution-button="3" -->
$h'(x)=$ [[ -2*x^4+3*x ]]
@Algebrite.check(`-2*x^4+3*x`)
[[?]] Konstante Faktoren bleiben beim Ableiten erhalten. Die Ableitung einer Konstanten ist null.
*****************
$$
h'(x)=-2x^4+3x.
$$
*****************

@resetter

@ADetails(`1=BE;Ableitungen, Polynomfunktionen, Potenzregel`)

</div>

<div class="flex-child">

__$d)\;\;$__ $k(x)=\dfrac15x^7-4x^3+2x$

<!-- data-hint-button="2" data-solution-button="3" -->
$k'(x)=$ [[ 7/5*x^6-12*x^2+2 ]]
@Algebrite.check(`7/5*x^6-12*x^2+2`)
[[?]] Multipliziere jeden Koeffizienten mit dem jeweiligen Exponenten und verringere den Exponenten um eins.
*****************
$$
k'(x)=\frac75x^6-12x^2+2.
$$
*****************

@resetter

@ADetails(`1=BE;Ableitungen, Polynomfunktionen, Potenzregel`)

</div>

</section>

## Aufgabe 2: Höhere Ableitungen von Polynomfunktionen

<section class="dynFlex" data-basis="48" data-min="30">

<div class="flex-child">

__$a)\;\;$__ **Bestimme** die erste und die zweite Ableitung von

$$p(x)=\frac12x^5-3x^3+4x^2-7.$$

<!-- data-hint-button="2" data-solution-button="3" -->
$p'(x)=$ [[ 5/2*x^4-9*x^2+8*x ]], $\qquad p''(x)=$ [[ 10*x^3-18*x+8 ]]
@Algebrite.check([ `5/2*x^4-9*x^2+8*x`; `10*x^3-18*x+8` ])
[[?]] Leite die Polynomfunktion zunächst einmal und das Ergebnis anschließend ein zweites Mal ab.
*****************
$$
\begin{aligned}
p'(x)&=\frac52x^4-9x^2+8x,\\
p''(x)&=10x^3-18x+8.
\end{aligned}
$$
*****************

@resetter

@ADetails(`2=BE;Ableitungen, Polynomfunktionen, Erste und zweite Ableitung`)

</div>

<div class="flex-child">

__$b)\;\;$__ **Bestimme** die erste und die zweite Ableitung von

$$q(x)=-\frac13x^6+2x^4-5x+1.$$

<!-- data-hint-button="2" data-solution-button="3" -->
$q'(x)=$ [[ -2*x^5+8*x^3-5 ]], $\qquad q''(x)=$ [[ -10*x^4+24*x^2 ]]
@Algebrite.check([ `-2*x^5+8*x^3-5`; `-10*x^4+24*x^2` ])
[[?]] Beachte beim ersten Ableiten, dass die Ableitung des konstanten Summanden null ist.
*****************
$$
\begin{aligned}
q'(x)&=-2x^5+8x^3-5,\\
q''(x)&=-10x^4+24x^2.
\end{aligned}
$$
*****************

@resetter

@ADetails(`2=BE;Ableitungen, Polynomfunktionen, Erste und zweite Ableitung`)

</div>

</section>

## Aufgabe 3: Tangente

Gegeben ist die Funktion

$$p(x)=x^3-2x^2+1.$$

**Bestimme** die Gleichung der Tangente an den Graphen von $p$ an der Stelle $x_0=2$.

<!-- data-hint-button="2" data-solution-button="3" -->
$t(x)=$ [[ 4*x-7 ]]
@Algebrite.check(`4*x-7`)
[[?]] Berechne $p(2)$ und $p'(2)$. Verwende anschließend $t(x)=p'(2)(x-2)+p(2)$.
*****************
$$
p'(x)=3x^2-4x,\qquad
p(2)=1,\qquad
p'(2)=4.
$$

Damit gilt:

$$
t(x)=4(x-2)+1=4x-7.
$$
*****************

@resetter

@ADetails(`4=BE;Tangente, Ableitungswert, Punkt-Steigungs-Gleichung`)

## Aufgabe 4: Ableitung und Monotonie

Von einer differenzierbaren Funktion $f$ ist bekannt:

$$f'(x)=(x+1)(x-3).$$

**Wähle** die richtige Aussage aus.

<!-- data-hint-button="2" data-solution-button="3" -->
[(X)] $f$ steigt für $x<-1$ und $x>3$, fällt für $-1<x<3$, besitzt bei $x=-1$ einen lokalen Hochpunkt und bei $x=3$ einen lokalen Tiefpunkt.
[( )] $f$ fällt für $x<-1$ und $x>3$, steigt für $-1<x<3$, besitzt bei $x=-1$ einen lokalen Tiefpunkt und bei $x=3$ einen lokalen Hochpunkt.
[( )] $f$ steigt auf ganz $\mathbb R$ und besitzt keine lokalen Extrempunkte.
[( )] $f$ fällt auf ganz $\mathbb R$ und besitzt keine lokalen Extrempunkte.

[[?]] Untersuche das Vorzeichen der beiden Faktoren in den drei Intervallen.
*****************
Für $x<-1$ sind beide Faktoren negativ, also ist $f'(x)>0$. Zwischen $-1$ und $3$ ist genau ein Faktor negativ, also ist $f'(x)<0$. Für $x>3$ sind beide Faktoren positiv.

Damit wechselt $f'$ bei $x=-1$ von positiv zu negativ und bei $x=3$ von negativ zu positiv. Folglich liegt bei $x=-1$ ein lokaler Hochpunkt und bei $x=3$ ein lokaler Tiefpunkt vor.
*****************

@resetter

@ADetails(`4=BE;Ableitung, Monotonie, Extremstellen, Vorzeichenwechsel`)

## Aufgabe 5: Tangenten und Wendepunkte

**Wähle** alle mathematisch richtigen Aussagen aus.

<!-- data-hint-button="2" data-solution-button="3" -->
[[X]] Eine differenzierbare Funktion kann auch in einem Wendepunkt eine Tangente besitzen.
[[ ]] Für jeden Wendepunkt $W(x_W\mid f(x_W))$ muss $f'(x_W)=0$ gelten.
[[X]] Wechselt $f''$ an einer Stelle das Vorzeichen, liegt dort ein Wechsel des Krümmungsverhaltens vor.
[[X]] Ist eine Funktion an einer inneren lokalen Extremstelle differenzierbar, verläuft die Tangente dort parallel zur Abszissenachse.
[[?]] Unterscheide zwischen der Steigung der Tangente und dem Krümmungsverhalten des Graphen.
*****************
Richtig sind die erste, dritte und vierte Aussage.

Eine Tangente beschreibt die lokale Steigung. Sie kann den Graphen in einem Wendepunkt schneiden. Für einen Wendepunkt ist eine waagerechte Tangente nicht notwendig; beispielsweise besitzt $f(x)=x^3+x$ bei $x=0$ einen Wendepunkt mit $f'(0)=1$.
*****************

@resetter

@ADetails(`4=BE;Tangente, Wendepunkt, Krümmungsverhalten, Extremstelle`)


## Aufgabe 6: Geführte Kurvendiskussion

Gegeben ist die Funktion

$$
f(x)=\frac14x^3-\frac32x^2-x+6.
$$

<section class="dynFlex" data-basis="48" data-min="30">

<div class="flex-child">

__$a)\;\;$__ **Gib** den Definitionsbereich $D_f$ und den Wertebereich $W_f$ **an**.

<!-- data-hint-button="2" data-solution-button="3" -->
$D_f=$ [[($\mathbb{R}$)|$[-2;6]$|$[0;\infty)$]],
$W_f=$ [[($\mathbb{R}$)|$[-6;6]$|$[0;\infty)$]]
[[?]] $f$ ist eine Polynomfunktion dritten Grades mit positivem Leitkoeffizienten.
*****************
Für eine Polynomfunktion gilt $D_f=\mathbb R$. Wegen des ungeraden Grades und des positiven Leitkoeffizienten nimmt $f$ beliebig kleine und beliebig große Werte an. Daher ist auch $W_f=\mathbb R$.
*****************

@resetter

@ADetails(`2=BE;Kurvendiskussion, Definitionsbereich, Wertebereich`)

</div>

<div class="flex-child">

__$b)\;\;$__ **Berechne** den Schnittpunkt des Graphen mit der Ordinatenachse.

<!-- data-hint-button="2" data-solution-button="3" -->
$S_y=(0\mid$ [[ 6 ]] $)$
@Algebrite.check(6)
[[?]] Setze $x=0$ in den Funktionsterm ein.
*****************
$$f(0)=6.$$

Der Graph schneidet die Ordinatenachse im Punkt

$$S_y(0\mid6).$$
*****************

@resetter

@ADetails(`1=BE;Kurvendiskussion, Ordinatenachsenabschnitt, Funktionswert`)

</div>

<div class="flex-child">

__$c)\;\;$__ **Untersuche**, ob der Graph symmetrisch zur Ordinatenachse oder zum Ursprung ist.

<!-- data-hint-button="2" data-solution-button="3" -->
[( )] Der Graph ist symmetrisch zur Ordinatenachse.
[( )] Der Graph ist symmetrisch zum Ursprung.
[(X)] Keine der beiden Symmetrien liegt vor.
[[?]] Vergleiche $f(-x)$ mit $f(x)$ und mit $-f(x)$.
*****************
$$
f(-x)=-\frac14x^3-\frac32x^2+x+6.
$$

Dieser Term stimmt weder mit $f(x)$ noch mit $-f(x)$ überein. Daher liegt weder eine Symmetrie zur Ordinatenachse noch eine Punktsymmetrie zum Ursprung vor.
*****************

@resetter

@ADetails(`2=BE;Kurvendiskussion, Symmetrie, Funktionsterm`)

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
*****************
Der Summand höchsten Grades ist $\frac14x^3$. Deshalb gilt:

$$
\lim_{x\to-\infty}f(x)=-\infty,
\qquad
\lim_{x\to+\infty}f(x)=+\infty.
$$
*****************

@resetter

@ADetails(`2=BE;Kurvendiskussion, Verhalten im Unendlichen, Leitkoeffizient`)

</div>

</section>

<section class="dynFlex" data-basis="48" data-min="30">

<div class="flex-child">

__$e)\;\;$__ **Berechne** die Nullstellen von $f$.

<!-- data-hint-button="2" data-solution-button="3" -->
$x_1=$ [[ -2 ]], $\quad x_2=$ [[ 2 ]], $\quad x_3=$ [[ 6 ]]
@Algebrite.check([ -2; 2; 6 ])
[[?]] Multipliziere die Gleichung zunächst mit $4$. Eine ganzzahlige Nullstelle lässt sich durch Probieren finden; anschließend kannst du faktorisieren.
*****************
$$
\begin{aligned}
f(x)
&=\frac14\left(x^3-6x^2-4x+24\right)\\
&=\frac14(x+2)(x-2)(x-6).
\end{aligned}
$$

Damit lauten die Nullstellen:

$$x_1=-2,\qquad x_2=2,\qquad x_3=6.$$
*****************

@resetter

@ADetails(`4=BE;Kurvendiskussion, Nullstellen, Faktorisieren`)

</div>

<div class="flex-child">

__$f)\;\;$__ **Berechne** die Extrempunkte von $f$. Runde die Koordinaten auf zwei Nachkommastellen.

<!-- data-hint-button="2" data-solution-button="3" -->
$H($ [[ -0,31 ]] $\mid$ [[ 6,16 ]] $)$, $\qquad T($ [[ 4,31 ]] $\mid$ [[ -6,16 ]] $)$
@Algebrite.check2([ -0.3094010768; 6.1584028714; 4.3094010768; -6.1584028714 ],[ 0.015; 0.015; 0.015; 0.015 ])
[[?]] Löse $f'(x)=0$ und untersuche anschließend das Vorzeichen von $f''$ an den beiden Stellen.
*****************
$$
f'(x)=\frac34x^2-3x-1,
\qquad
f''(x)=\frac32x-3.
$$

Aus $f'(x)=0$ folgt:

$$
x=2\pm\frac{4\sqrt3}{3}.
$$

Für $x_H=2-\frac{4\sqrt3}{3}$ ist $f''(x_H)<0$, für $x_T=2+\frac{4\sqrt3}{3}$ ist $f''(x_T)>0$. Mit den zugehörigen Funktionswerten erhält man:

$$
H\left(2-\frac{4\sqrt3}{3}\,\middle|\,\frac{32\sqrt3}{9}\right)
\approx H(-0{,}31\mid6{,}16),
$$

$$
T\left(2+\frac{4\sqrt3}{3}\,\middle|\,-\frac{32\sqrt3}{9}\right)
\approx T(4{,}31\mid-6{,}16).
$$
*****************

@resetter

@ADetails(`5=BE;Kurvendiskussion, Extrempunkte, Ableitungen, notwendige und hinreichende Bedingung`)

</div>

<div class="flex-child">

__$g)\;\;$__ **Berechne** den Wendepunkt von $f$.

<!-- data-hint-button="2" data-solution-button="3" -->
$W($ [[ 2 ]] $\mid$ [[ 0 ]] $)$
@Algebrite.check([ 2; 0 ])
[[?]] Löse $f''(x)=0$ und prüfe die Stelle mit $f'''(x)$.
*****************
$$
f''(x)=\frac32x-3
\quad\Longrightarrow\quad
f''(x)=0\iff x=2.
$$

Da

$$f'''(x)=\frac32\ne0,$$

liegt bei $x=2$ eine Wendestelle vor. Außerdem ist $f(2)=0$. Somit lautet der Wendepunkt:

$$W(2\mid0).$$

Schreibt man $u=x-2$, so gilt $f(2+u)=\frac14u^3-4u$. Der Graph ist daher punktsymmetrisch zum Wendepunkt $W$.
*****************

@resetter

@ADetails(`4=BE;Kurvendiskussion, Wendepunkt, Ableitungen, Punktsymmetrie`)

</div>

</section>

## Aufgabe 7: Modellierung – Entwicklung einer Lernplattform

Die Zahl der aktiven Konten einer neuen Lernplattform wird für die ersten zwölf Wochen durch

$$
N(t)=-0{,}02t^3+0{,}30t^2+0{,}80t+2
$$

modelliert. Dabei ist $t$ die Zeit in Wochen seit dem Start und $N(t)$ die Anzahl der aktiven Konten in **Tausend**. Das Modell wird für $0\le t\le12$ verwendet.

In der achten Woche wird eine Prognose für die elfte Woche erstellt.

<section class="dynFlex" data-basis="48" data-min="30">

<div class="flex-child">

__$a)\;\;$__ **Berechne** die Zahl der aktiven Konten zum Start und nach acht Wochen. **Gib** die Ergebnisse in Tausend **an**.

<!-- data-hint-button="2" data-solution-button="3" -->
$N(0)=$ [[ 2 ]] Tausend, $\qquad N(8)=$ [[ 17,36 ]] Tausend
@Algebrite.check2([ 2; 17.36 ],[ 0.005; 0.005 ])
[[?]] Setze $t=0$ beziehungsweise $t=8$ in die Funktionsgleichung ein.
*****************
$$
N(0)=2,
\qquad
N(8)=-0{,}02\cdot8^3+0{,}30\cdot8^2+0{,}80\cdot8+2=17{,}36.
$$

Zum Start gibt es dem Modell zufolge $2000$ aktive Konten, nach acht Wochen etwa $17\,360$.
*****************

@resetter

@ADetails(`3=BE;Modellierung, Funktionswerte, Einheiten interpretieren`)

</div>

<div class="flex-child">

__$b)\;\;$__ **Bestimme** im Modellzeitraum den Zeitpunkt, zu dem die Zahl der aktiven Konten maximal ist, und **berechne** diese maximale Anzahl.

<!-- data-hint-button="2" data-solution-button="3" -->
$t_{\max}\approx$ [[ 11,19 ]] Wochen, $\qquad N_{\max}\approx$ [[ 20,49 ]] Tausend
@Algebrite.check2([ 11.1913918737; 20.4934675396 ],[ 0.015; 0.015 ])
[[?]] Löse $N'(t)=0$. Berücksichtige nur Lösungen im Modellzeitraum und vergleiche gegebenenfalls mit den Randwerten.
*****************
$$
N'(t)=-0{,}06t^2+0{,}60t+0{,}80.
$$

Aus $N'(t)=0$ erhält man:

$$
t=\frac{15\pm\sqrt{345}}{3}.
$$

Nur

$$
t_{\max}=\frac{15+\sqrt{345}}3\approx11{,}19
$$

liegt im Modellzeitraum. Dort wechselt $N'$ von positiv zu negativ. Die Randwerte sind kleiner. Somit gilt:

$$
N(t_{\max})\approx20{,}49.
$$

Die maximale Zahl beträgt nach dem Modell etwa $20\,490$ aktive Konten.
*****************

@resetter

@ADetails(`5=BE;Modellierung, Maximum, Ableitungen, Randwerte`)

</div>

</section>

<section class="dynFlex" data-basis="48" data-min="30">

<div class="flex-child">

__$c)\;\;$__ **Bestimme** den Wendepunkt des Modells und die momentane Änderungsrate an dieser Stelle. **Interpretiere** die Ergebnisse im Sachzusammenhang.

<!-- data-hint-button="2" data-solution-button="3" -->
$t_W=$ [[ 5 ]] Wochen, $\quad N(t_W)=$ [[ 11 ]] Tausend, $\quad N'(t_W)=$ [[ 2,3 ]] Tausend Konten pro Woche
@Algebrite.check2([ 5; 11; 2.3 ],[ 0.005; 0.005; 0.005 ])
[[?]] Löse $N''(t)=0$. Setze den Zeitpunkt anschließend in $N$ und $N'$ ein.
*****************
$$
N''(t)=-0{,}12t+0{,}60.
$$

Daraus folgt $N''(t)=0$ für $t=5$. Weiter gilt:

$$
N(5)=11,
\qquad
N'(5)=2{,}3.
$$

Nach fünf Wochen gibt es dem Modell zufolge $11\,000$ aktive Konten. Zu diesem Zeitpunkt ist die wöchentliche Zunahme mit etwa $2300$ Konten pro Woche am größten. Danach wächst die Zahl weiterhin, die momentane Zunahme wird jedoch kleiner.
*****************

@resetter

@ADetails(`4=BE;Modellierung, Wendepunkt, Änderungsrate, Interpretation`)

</div>

</section>

<section class="dynFlex" data-basis="48" data-min="30">

<div class="flex-child">

__$d)\;\;$__ **Bestimme** die Tangente an den Graphen von $N$ an der Stelle $t=8$. **Verwende** diese Tangente als lineare Prognose für die Zahl der aktiven Konten in der elften Woche.

<!-- data-hint-button="2" data-solution-button="3" -->
$T(t)=$ [[ 1.76*t+3.28 ]], $\qquad T(11)=$ [[ 22,64 ]] Tausend
@Algebrite.check([ 1.76*t+3.28; 22.64 ])
[[?]] Berechne $N(8)$ und $N'(8)$. Setze beide Werte in $T(t)=N'(8)(t-8)+N(8)$ ein.
*****************
$$
N(8)=17{,}36,
\qquad
N'(8)=1{,}76.
$$

Damit lautet die Tangente:

$$
\begin{aligned}
T(t)
&=1{,}76(t-8)+17{,}36\\
&=1{,}76t+3{,}28.
\end{aligned}
$$

Die tangentiale Prognose für die elfte Woche ist:

$$
T(11)=22{,}64.
$$

Die Tangente prognostiziert also etwa $22\,640$ aktive Konten.
*****************

@resetter

@ADetails(`5=BE;Modellierung, Tangente, Lineare Prognose, Ableitungswert`)

</div>

<div class="flex-child">

__$e)\;\;$__ **Vergleiche** die tangentiale Prognose aus d) mit dem Modellwert $N(11)$. **Berechne** die absolute Abweichung in Tausend Konten und **beurteile** die Prognose.

<!-- data-hint-button="2" data-solution-button="3" -->
$N(11)=$ [[ 20,48 ]] Tausend, $\qquad$ absolute Abweichung: [[ 2,16 ]] Tausend
@Algebrite.check2([ 20.48; 2.16 ],[ 0.005; 0.005 ])
[[?]] Berechne zuerst $N(11)$ und bilde anschließend den Betrag der Differenz zu $T(11)$.
*****************
$$
N(11)
=-0{,}02\cdot11^3+0{,}30\cdot11^2+0{,}80\cdot11+2
=20{,}48.
$$

$$
\left|T(11)-N(11)\right|
=|22{,}64-20{,}48|
=2{,}16.
$$

Die Tangente überschätzt den Modellwert um $2160$ aktive Konten.
*****************

@resetter

**Wähle** die passende Beurteilung aus.

<!-- data-hint-button="2" data-solution-button="3" -->
[(X)] Die Tangente überschätzt den Wert, weil die momentane Zunahme nach der achten Woche weiter abnimmt.
[( )] Die Tangente unterschätzt den Wert, weil die momentane Zunahme nach der achten Woche größer wird.
[( )] Die Tangente liefert für alle zukünftigen Wochen exakt dieselben Werte wie das kubische Modell.
[[?]] Untersuche das Vorzeichen von $N''(t)$ für $t>8$.
*****************
Für $t>8$ ist $N''(t)<0$. Die Steigung des Modellgraphen nimmt also ab. Die Tangente setzt dagegen die Steigung aus der achten Woche unverändert fort und liegt deshalb in der elften Woche über dem Modellgraphen.

Eine Tangente ist eine lokale lineare Näherung. Mit wachsendem Abstand vom Berührpunkt kann die Abweichung deutlich größer werden.
*****************

@resetter

@ADetails(`3=BE;Modellierung, Prognose, Abweichung, Beurteilen`)

</div>

</section>

## Aufgabe 8: Extrempunkte

**Berechne** jeweils alle Extrempunkte und **bestimme** ihre Art.

<section class="dynFlex" data-basis="48" data-min="30">

<div class="flex-child">

__$a)\;\;$__ $f(x)=x^3-3x^2-9x+5$

<!-- data-hint-button="2" data-solution-button="3" -->
$H($ [[ -1 ]] $\mid$ [[ 10 ]] $)$, $\qquad T($ [[ 3 ]] $\mid$ [[ -22 ]] $)$
@Algebrite.check([ -1; 10; 3; -22 ])
[[?]] Löse $f'(x)=0$ und untersuche das Vorzeichen von $f''$ an den gefundenen Stellen.
*****************
$$
f'(x)=3x^2-6x-9=3(x+1)(x-3),
\qquad
f''(x)=6x-6.
$$

Damit sind $x=-1$ und $x=3$ die möglichen Extremstellen. Es gilt:

$$
f''(-1)=-12<0,
\qquad
f''(3)=12>0.
$$

Mit $f(-1)=10$ und $f(3)=-22$ erhält man

$$H(-1\mid10),\qquad T(3\mid-22).$$
*****************

@resetter

@ADetails(`3=BE;Extrempunkte, Erste und zweite Ableitung, Klassifikation`)

</div>

<div class="flex-child">

__$b)\;\;$__ $g(x)=\dfrac14x^4-2x^2+3$

<!-- data-hint-button="2" data-solution-button="3" -->
$T_1($ [[ -2 ]] $\mid$ [[ -1 ]] $)$, $\quad H($ [[ 0 ]] $\mid$ [[ 3 ]] $)$, $\quad T_2($ [[ 2 ]] $\mid$ [[ -1 ]] $)$
@Algebrite.check([ -2; -1; 0; 3; 2; -1 ])
[[?]] Faktorisiere $g'(x)$ vollständig. Es entstehen drei mögliche Extremstellen.
*****************
$$
g'(x)=x^3-4x=x(x-2)(x+2),
\qquad
g''(x)=3x^2-4.
$$

Aus $g'(x)=0$ folgen $x=-2$, $x=0$ und $x=2$. Wegen

$$
g''(-2)>0,
\qquad
g''(0)<0,
\qquad
g''(2)>0
$$

und $g(-2)=g(2)=-1$ sowie $g(0)=3$ lauten die Extrempunkte:

$$T_1(-2\mid-1),\qquad H(0\mid3),\qquad T_2(2\mid-1).$$
*****************

@resetter

@ADetails(`3=BE;Extrempunkte, Polynomfunktion vierten Grades, Klassifikation`)

</div>

</section>

<section class="dynFlex" data-basis="48" data-min="30">

<div class="flex-child">

__$c)\;\;$__ $h(x)=\dfrac13x^3-\dfrac12x^2-6x+2$

Runde die Koordinaten auf zwei Nachkommastellen.

<!-- data-hint-button="2" data-solution-button="3" -->
$H($ [[ -2 ]] $\mid$ [[ 9,33 ]] $)$, $\qquad T($ [[ 3 ]] $\mid$ [[ -11,50 ]] $)$
@Algebrite.check2([ -2; 9.3333333333; 3; -11.5 ],[ 0.015; 0.015; 0.015; 0.015 ])
[[?]] Die Gleichung $h'(x)=0$ lässt sich faktorisieren.
*****************
$$
h'(x)=x^2-x-6=(x+2)(x-3),
\qquad
h''(x)=2x-1.
$$

Somit liegt bei $x=-2$ ein Hochpunkt und bei $x=3$ ein Tiefpunkt vor. Die Funktionswerte sind

$$
h(-2)=\frac{28}{3}\approx9{,}33,
\qquad
h(3)=-\frac{23}{2}=-11{,}50.
$$

Also gilt:

$$H(-2\mid9{,}33),\qquad T(3\mid-11{,}50).$$
*****************

@resetter

@ADetails(`3=BE;Extrempunkte, Faktorisieren, Runden`)

</div>

</section>

## Aufgabe 9: Wendepunkte

**Berechne** jeweils alle Wendepunkte.

<section class="dynFlex" data-basis="48" data-min="30">

<div class="flex-child">

__$a)\;\;$__ $p(x)=x^3-6x^2+9x+2$

<!-- data-hint-button="2" data-solution-button="3" -->
$W($ [[ 2 ]] $\mid$ [[ 4 ]] $)$
@Algebrite.check([ 2; 4 ])
[[?]] Löse $p''(x)=0$ und überprüfe die Stelle mithilfe von $p'''(x)$.
*****************
$$
p''(x)=6x-12
\quad\Longrightarrow\quad
p''(x)=0\iff x=2.
$$

Da $p'''(x)=6\ne0$ und $p(2)=4$ gilt, lautet der Wendepunkt

$$W(2\mid4).$$
*****************

@resetter

@ADetails(`3=BE;Wendepunkt, Zweite und dritte Ableitung`)

</div>

<div class="flex-child">

__$b)\;\;$__ $q(x)=\dfrac14x^4-3x^2+2x+1$

Runde die Koordinaten auf zwei Nachkommastellen.

<!-- data-hint-button="2" data-solution-button="3" -->
$W_1($ [[ -1,41 ]] $\mid$ [[ -6,83 ]] $)$, $\qquad W_2($ [[ 1,41 ]] $\mid$ [[ -1,17 ]] $)$
@Algebrite.check2([ -1.4142135624; -6.8284271247; 1.4142135624; -1.1715728753 ],[ 0.015; 0.015; 0.015; 0.015 ])
[[?]] Aus $q''(x)=0$ entstehen zwei Lösungen. Berechne anschließend beide Funktionswerte.
*****************
$$
q''(x)=3x^2-6
\quad\Longrightarrow\quad
x=\pm\sqrt2.
$$

Da $q'''(x)=6x$ an beiden Stellen ungleich null ist, liegen zwei Wendestellen vor. Die exakten Punkte sind

$$
W_1(-\sqrt2\mid-4-2\sqrt2),
\qquad
W_2(\sqrt2\mid-4+2\sqrt2).
$$

Gerundet erhält man

$$W_1(-1{,}41\mid-6{,}83),\qquad W_2(1{,}41\mid-1{,}17).$$
*****************

@resetter

@ADetails(`3=BE;Wendepunkte, Polynomfunktion vierten Grades, Runden`)

</div>

</section>

<section class="dynFlex" data-basis="48" data-min="30">

<div class="flex-child">

__$c)\;\;$__ $r(x)=-\dfrac12x^3+\dfrac34x^2+4x-1$

<!-- data-hint-button="2" data-solution-button="3" -->
$W($ [[ 1/2 ]] $\mid$ [[ 9/8 ]] $)$
@Algebrite.check([ 1/2; 9/8 ])
[[?]] Löse $r''(x)=0$ und setze die gefundene Stelle anschließend in $r$ ein.
*****************
$$
r''(x)=-3x+\frac32
\quad\Longrightarrow\quad
r''(x)=0\iff x=\frac12.
$$

Wegen $r'''(x)=-3\ne0$ liegt dort eine Wendestelle vor. Außerdem gilt $r\left(\frac12\right)=\frac98$. Damit lautet der Wendepunkt

$$W\left(\frac12\,\middle|\,\frac98\right).$$
*****************

@resetter

@ADetails(`3=BE;Wendepunkt, Bruchkoordinaten, Ableitungen`)

</div>

</section>

## Aufgabe 10: Tangenten

<section class="dynFlex" data-basis="48" data-min="30">

<div class="flex-child">

__$a)\;\;$__ Gegeben ist $p(x)=\dfrac12x^3-2x^2+x+3$.

**Bestimme** die Tangente an den Graphen von $p$ an der Stelle $x_0=2$.

<!-- data-hint-button="2" data-solution-button="3" -->
$t(x)=$ [[ -x+3 ]]
@Algebrite.check(`-x+3`)
[[?]] Berechne $p(2)$ und $p'(2)$ und verwende die Punkt-Steigungs-Gleichung.
*****************
$$
p'(x)=\frac32x^2-4x+1,
\qquad
p(2)=1,
\qquad
p'(2)=-1.
$$

Damit gilt:

$$t(x)=-(x-2)+1=-x+3.$$
*****************

@resetter

@ADetails(`3=BE;Tangente, Ableitungswert, Punkt-Steigungs-Gleichung`)

</div>

<div class="flex-child">

__$b)\;\;$__ Gegeben ist $q(x)=-\dfrac14x^4+x^2+2x-1$.

**Bestimme** die Tangente an den Graphen von $q$ an der Stelle $x_0=-1$.

<!-- data-hint-button="2" data-solution-button="3" -->
$t(x)=$ [[ x-5/4 ]]
@Algebrite.check(`x-5/4`)
[[?]] Bestimme den Berührpunkt und die Steigung der Tangente bei $x_0=-1$.
*****************
$$
q'(x)=-x^3+2x+2,
\qquad
q(-1)=-\frac94,
\qquad
q'(-1)=1.
$$

Somit lautet die Tangente:

$$t(x)=x+1-\frac94=x-\frac54.$$
*****************

@resetter

@ADetails(`3=BE;Tangente, Polynomfunktion vierten Grades, Punkt-Steigungs-Gleichung`)

</div>

</section>

<section class="dynFlex" data-basis="48" data-min="30">

<div class="flex-child">

__$c)\;\;$__ Gegeben sind

$$r(x)=x^3-3x^2-x+5$$

und die Gerade $k(x)=2x-4$.

**Bestimme** die beiden Stellen, an denen die Tangenten an den Graphen von $r$ parallel zu $k$ verlaufen. Die Tangenten haben die Form $t_i(x)=2x+b_i$. Runde die gesuchten Werte auf zwei Nachkommastellen.

<!-- data-hint-button="2" data-solution-button="3" -->
$x_1\approx$ [[ -0,41 ]], $\quad b_1\approx$ [[ 5,66 ]], $\qquad x_2\approx$ [[ 2,41 ]], $\quad b_2\approx$ [[ -5,66 ]]
@Algebrite.check2([ -0.4142135624; 5.6568542495; 2.4142135624; -5.6568542495 ],[ 0.015; 0.015; 0.015; 0.015 ])
[[?]] Parallele Geraden besitzen dieselbe Steigung. Löse daher $r'(x)=2$.
*****************
$$
r'(x)=3x^2-6x-1.
$$

Aus $r'(x)=2$ folgt:

$$
3x^2-6x-3=0
\quad\Longrightarrow\quad
x_{1,2}=1\pm\sqrt2.
$$

Für $x_1=1-\sqrt2$ ergibt sich $b_1=4\sqrt2$, für $x_2=1+\sqrt2$ gilt $b_2=-4\sqrt2$. Damit lauten die beiden Tangenten:

$$
t_1(x)=2x+4\sqrt2,
\qquad
t_2(x)=2x-4\sqrt2.
$$

Gerundet erhält man

$$
x_1\approx-0{,}41,
\quad b_1\approx5{,}66,
\qquad
x_2\approx2{,}41,
\quad b_2\approx-5{,}66.
$$
*****************

@resetter

@ADetails(`3=BE;Tangenten, Parallelität, Ableitungswert, Runden`)

</div>

</section>
