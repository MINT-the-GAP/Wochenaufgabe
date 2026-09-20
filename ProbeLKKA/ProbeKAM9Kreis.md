<!--
author: Martin Lommatzsch
version: 0.1.0
language: de
narrator: Deutsch Female
mode: Presentation
comment: Probeklassenarbeit für Klasse 9 zu Potenzen, linearen Funktionen, Cavalieri und Kreiskörpern. Mit Hinweisen, mathematischer Eingabeprüfung und ausführlichen Musterlösungen.
tags: Mathematik, Klasse 9, Probeklassenarbeit, Potenzen, Wurzeln, Lineare Funktionen, Cavalieri, Kreis, Prisma, Kegel, Pyramide, Kugel



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

# Probeklassenarbeit Klasse 9 – Potenzen und Kreiskörper



> Letztes Update am 20.09.2026 gegen 18:00 Uhr


Swipe (Wische) entweder weiter oder klicke unten links auf neben der Seitenzahl auf den Pfeil nach rechts.


Diese Probearbeit hat mehr Aufgaben als die richtige Arbeit, damit du genug zum Üben hast. Es sind viele verschiedene Aufgabentypen abgebildet, sodass du alles nochmal bei der Bearbeitung dieser Aufgaben wiederholst.

---

---



**Aufgaben 1–4:** ohne Taschenrechner.

**Aufgaben 5–7:** mit Taschenrechner.

---

---

---

---


> [!CAUTION]
> <h2> @Explain(Tutorial) </h2>


---

---

---

---

## Aufgabe 1: Potenzgesetze und Wurzeln

**Vereinfache** die Terme so weit wie möglich. Alle Variablen stehen für positive reelle Zahlen.

<section class="dynFlex" data-basis="48%" data-min="30%">

<div class="flex-child">

__$a)\;\;$__  $x^{-4}\cdot(x^3)^2\cdot x^5$

<!-- data-hint-button="2" data-solution-button="3" -->
Ergebnis: [[ x^7 ]] @canvas
@Algebrite.check(`x^7`)
[[?]] Beim Potenzieren einer Potenz werden die Exponenten multipliziert. Beim Multiplizieren von Potenzen mit gleicher Basis werden sie addiert.
*****************
$$
x^{-4}\cdot(x^3)^2\cdot x^5
=x^{-4}\cdot x^6\cdot x^5
=x^{-4+6+5}=x^7.
$$
*****************

@resetter

@ADetails(`1=BE;Potenzen, Potenz einer Potenz, Negative Exponenten`)

</div>

<div class="flex-child">

__$b)\;\;$__  $\dfrac{a^2b^{-3}}{a^{-1}b^2}\cdot b$

<!-- data-hint-button="2" data-solution-button="3" -->
$=$ [[ a^3/b^4 ]] @canvas
@Algebrite.check(`a^3/b^4`)
[[?]] Fasse die Potenzen von $a$ und von $b$ getrennt zusammen. Beachte das Minus vor dem Exponenten im Nenner.
*****************
$$
\frac{a^2b^{-3}}{a^{-1}b^2}\cdot b
=a^{2-(-1)}b^{-3-2+1}
=a^3b^{-4}=\frac{a^3}{b^4}.
$$
*****************

@resetter

@ADetails(`1=BE;Potenzen, Quotient, Negative Exponenten`)

</div>

<div class="flex-child">

__$c)\;\;$__  $\dfrac{\sqrt[6]{t^{18}}}{t}$

<!-- data-hint-button="2" data-solution-button="3" -->
$=$  [[ t^2 ]] @canvas
@Algebrite.check(`t^2`)
[[?]] Schreibe die sechste Wurzel als Potenz mit dem Exponenten $\frac16$.
*****************
Wegen $t>0$ gilt:

$$
\frac{\sqrt[6]{t^{18}}}{t}
=\frac{t^{18/6}}{t}
=t^{3-1}=t^2.
$$
*****************

@resetter

@ADetails(`1=BE;Wurzeln, Rationale Exponenten, Potenzgesetze`)

</div>

<div class="flex-child">

__$d)\;\;$__ $\sqrt{\dfrac{u^3}{u^{-2}\cdot u^{-1}}}$

<!-- data-hint-button="2" data-solution-button="3" -->
$=$  [[ u^3 ]] @canvas
@Algebrite.check(`u^3`)
[[?]] Prüfe zuerst den Term unter der Wurzel. Ist danach noch ein Rechenschritt nötig?
*****************
$$
\sqrt{\frac{u^3}{u^{-2}\cdot u^{-1}}}
=\sqrt{\frac{u^3}{u^{-3}}}
=\sqrt{u^{3-(-3)}}
=\sqrt{u^6}=u^3.
$$


*****************

@resetter

@ADetails(`1=BE;Potenzen, Wurzeln, Fehleranalyse`)

</div>

<div class="flex-child">

__$e)\;\;$__  $\left(\dfrac{p^2}{q}\right)^3\cdot\left(\dfrac{q^2}{p}\right)^2$

<!-- data-hint-button="2" data-solution-button="3" -->
$=$  [[ p^4*q ]] @canvas
@Algebrite.check(`p^4*q`)
[[?]] Potenziere in beiden Brüchen jeweils Zähler und Nenner. Kürze anschließend gleiche Basen.
*****************
$$
\left(\frac{p^2}{q}\right)^3\cdot\left(\frac{q^2}{p}\right)^2
=\frac{p^6}{q^3}\cdot\frac{q^4}{p^2}
=p^{6-2}q^{4-3}=p^4q.
$$
*****************

@resetter

@ADetails(`1=BE;Potenzgesetze, Potenzen von Brüchen, Kürzen`)

</div>

<div class="flex-child">

__$f)\;\;$__  $\left(\dfrac{\sqrt[3]{v^6}}{v^3}\right)^{-2}$

<!-- data-hint-button="2" data-solution-button="3" -->
$=$  [[ v^2 ]] @canvas
@Algebrite.check(`v^2`)
[[?]] Vereinfache zuerst die Wurzel und dann den Bruch in der Klammer. Wende zuletzt den äußeren Exponenten an.
*****************
$$
\left(\frac{\sqrt[3]{v^6}}{v^3}\right)^{-2}
=\left(\frac{v^2}{v^3}\right)^{-2}
=\left(v^{-1}\right)^{-2}=v^2.
$$

Der äußere Exponent $-2$ bedeutet das Quadrieren des Kehrwerts. Er bedeutet nicht, dass das Ergebnis negativ wird.
*****************

@resetter

@ADetails(`1=BE;Wurzeln, Negative Exponenten, Potenz einer Potenz`)

</div>

<div class="flex-child">

__$g)\;\;$__ $\left(\dfrac{r^2}{s^{-1}}\right)^3:\left(\dfrac{s^2}{r^{-1}}\right)^2$

<!-- data-hint-button="2" data-solution-button="3" -->
$=$  [[ r^4/s ]] @canvas
@Algebrite.check(`r^4/s`)
[[?]] Potenziere zuerst beide Brüche. Fasse anschließend die Potenzen gleicher Basis zusammen.
*****************
$$
\left(\frac{r^2}{s^{-1}}\right)^3:\left(\frac{s^2}{r^{-1}}\right)^2
= (r^2s)^3:(s^2r)^2
=\frac{r^6s^3}{r^2s^4}
=\frac{r^4}{s}.
$$
*****************

@resetter

@ADetails(`1=BE;Potenzgesetze, Potenzen von Brüchen, Negative Exponenten`)

</div>

<div class="flex-child">

__$h)\;\;$__ $\sqrt[4]{\left(\dfrac{m^3}{m^7}\right)^{-3}}$

<!-- data-hint-button="2" data-solution-button="3" -->
$=$ [[ m^3 ]] @canvas
@Algebrite.check(`m^3`)
[[?]] Vereinfache zuerst den Bruch in der Klammer. Wende danach den äußeren Exponenten und zuletzt die Wurzel an.
*****************
$$
\sqrt[4]{\left(\frac{m^3}{m^7}\right)^{-3}}
=\sqrt[4]{\left(m^{-4}\right)^{-3}}
=\sqrt[4]{m^{12}}
=m^3.
$$
*****************

@resetter

@ADetails(`1=BE;Potenzgesetze, Negative Exponenten, Vierte Wurzel`)

</div>

<div class="flex-child">

__$i)\;\;$__ $\dfrac{\sqrt[4]{81a^8b^4}}{3ab}$

<!-- data-hint-button="2" data-solution-button="3" -->
$=$  [[ a ]] @canvas
@Algebrite.check(`a`)
[[?]] Schreibe die Faktoren unter der Wurzel als vierte Potenzen. Nutze, dass $a$ und $b$ positiv sind.
*****************
Wegen $a>0$ und $b>0$ gilt:

$$
\frac{\sqrt[4]{81a^8b^4}}{3ab}
=\frac{\sqrt[4]{3^4\cdot(a^2)^4\cdot b^4}}{3ab}
=\frac{3a^2b}{3ab}=a.
$$
*****************

@resetter

@ADetails(`1=BE;Vierte Wurzel, Potenzgesetze, Kürzen`)

</div>

</section>

## Aufgabe 2: Lineare Funktionen

Gegeben seien die Funktionen
$$
f(x)=\frac23x-\frac12
\qquad\text{und}\qquad
g(x)=-\frac34x+\frac52
$$
gegeben. **Gib** alle Ergebnisse als exakte Werte **an**.


__$a)\;\;$__ **Vervollständige** die Wertetabelle für $f$.

<!-- data-hint-button="2" data-solution-button="3" data-type="none" data-sortable="false" -->
| $x$ | $-3$ | [[ 3/2 ]] @canvas | $3$ | [[ 6 ]] @canvas |
|:---:|:---:|:---:|:---:|:---:|
| $f(x)$ | [[ -5/2 ]] @canvas | $\frac12$ | [[ 3/2 ]] @canvas | $\frac72$ |
@Algebrite.check([3/2;6;-5/2;3/2])
*****************
$
f(-3)=-\frac52,
\qquad
f(3)=\frac32.
$

Aus $f(x)=\frac12$ folgt $x=\frac32$; aus $f(x)=\frac72$ folgt $x=6$.
*****************

@resetter

@ADetails(`4=BE;Lineare Funktionen, Wertetabelle, Funktionswert, Gleichung`)


---


<section class="dynFlex" data-basis="48%" data-min="30%">

<div class="flex-child">


__$b)\;\;$__ **Berechne** die Nullstellen von $f$ und $g$.

<!-- data-hint-button="2" data-solution-button="3" -->
$x_{N_f}=$ [[ 3/4 ]]; $x_{N_g}=$ [[ 10/3 ]] @canvas
@Algebrite.check([3/4;10/3])
[[?]] Setze den jeweiligen Funktionsterm gleich null.
*****************
$
\frac23x-\frac12=0
\quad\Longrightarrow\quad
x_{N_f}=\frac34,
$
$
-\frac34x+\frac52=0
\quad\Longrightarrow\quad
x_{N_g}=\frac{10}{3}.
$
*****************

@resetter

@ADetails(`3=BE;Lineare Funktionen, Nullstellen, Bruchrechnung`)

</div>

<div class="flex-child">

__$c)\;\;$__ **Berechne** den Schnittpunkt der Graphen von $f$ und $g$.

<!-- data-hint-button="2" data-solution-button="3" -->
$S\bigl($ [[ 36/17 ]] $\mid$ [[ 31/34 ]] $\bigr)$ @canvas
@Algebrite.check([36/17;31/34])
[[?]] Setze $f(x)=g(x)$. Setze die gefundene Stelle danach in einen Funktionsterm ein.
*****************
$
\frac23x-\frac12=-\frac34x+\frac52
\quad\Longrightarrow\quad
\frac{17}{12}x=3
\quad\Longrightarrow\quad
x=\frac{36}{17}.
$

$
f\left(\frac{36}{17}\right)
=\frac{24}{17}-\frac12
=\frac{31}{34}.
$

Damit ist $S\left(\frac{36}{17}\mid\frac{31}{34}\right)$.
*****************

@resetter

@ADetails(`4=BE;Lineare Funktionen, Schnittpunkt, Gleichsetzen, Bruchrechnung`)

</div>

<div class="flex-child">

__$d)\;\;$__ Der Graph von $h$ verläuft orthogonal zum Graphen von $g$. Beide Graphen schneiden sich an der Stelle $x=-2$. **Bestimme** den Funktionsterm von $h$.

<!-- data-hint-button="2" data-solution-button="3" -->
$h(x)=$ [[ 4/3*x+20/3 ]] @canvas
@Algebrite.check(`4/3*x+20/3`)
[[?]] Für orthogonale Geraden gilt $m_g\cdot m_h=-1$. Berechne außerdem $g(-2)$.
*****************
Aus $m_g=-\frac34$ folgt $m_h=\frac43$. Der gemeinsame Punkt ist
$
(-2\mid g(-2))=(-2\mid4).
$

Mit $h(x)=\frac43x+b$ erhält man
$
4=\frac43\cdot(-2)+b
\quad\Longrightarrow\quad
b=\frac{20}{3}.
$

Also gilt $h(x)=\frac43x+\frac{20}{3}$.
*****************

@resetter

@ADetails(`4=BE;Lineare Funktionen, Orthogonalität, Steigung, Funktionsterm`)

</div>

</section>

---

<section class="dynFlex" data-basis="48%" data-min="30%">

<div class="flex-child">

__$e)\;\;$__ Der Graph von $k$ verläuft durch $P\left(-2\mid\frac73\right)$ und $Q\left(4\mid-\frac53\right)$. **Bestimme** den Funktionsterm von $k$.

<!-- data-hint-button="2" data-solution-button="3" -->
$k(x)=$ [[ -2/3*x+1 ]] @canvas
@Algebrite.check(`-2/3*x+1`)
[[?]] Berechne zuerst die Steigung aus den Koordinatenunterschieden.
*****************
$
m_k=\frac{-\frac53-\frac73}{4-(-2)}
=\frac{-4}{6}
=-\frac23.
$

Einsetzen von $P$ in $k(x)=-\frac23x+b$ ergibt $b=1$. Somit gilt
$
k(x)=-\frac23x+1.
$
*****************

@resetter

@ADetails(`3=BE;Lineare Funktionen, Zwei Punkte, Steigung, Funktionsterm`)

</div>

<div class="flex-child">

__$f)\;\;$__ **Bestimme** den Term einer zu $f$ parallelen linearen Funktion $p$, deren Graph den Graphen von $g$ auf der Ordinatenachse schneidet.

<!-- data-hint-button="2" data-solution-button="3" -->
$p(x)=$ [[ 2/3*x+5/2 ]] @canvas
@Algebrite.check(`2/3*x+5/2`)
[[?]] Parallele Geraden haben dieselbe Steigung. Auf der Ordinatenachse gilt $x=0$.
*****************
Wegen der Parallelität ist $m_p=\frac23$. Der gemeinsame Punkt auf der Ordinatenachse ist
$
(0\mid g(0))=\left(0\mid\frac52\right).
$

Daher lautet der Funktionsterm
$
p(x)=\frac23x+\frac52.
$
*****************

@resetter

@ADetails(`3=BE;Lineare Funktionen, Parallelität, Ordinatenachse, Funktionsterm`)

</div>

<div class="flex-child">

__$g)\;\;$__ **Bestimme** den Funktionsterm des dargestellten Graphen $u$.

@Koordinatensystem(`xmin=-5;xmax=5;ymin=-3;ymax=5;width=560;id=PLK9A2g;achsen=1;grid=1;border=0`)
@AchsenBeschriftung(`id=PLK9A2g;xlabel=$x$;ylabel=$y$`)
@PlotFunktion(`PLK9A2g;u;-2/3*x+1;#0072B2`)
@Punkt(`PLK9A2g;P;-3;3;#D55E00;1;fix`)
@Punkt(`PLK9A2g;Q;3;-1;#D55E00;1;fix`)

<!-- data-hint-button="2" data-solution-button="3" -->
$u(x)=$ [[ -2/3*x+1 ]] @canvas
@Algebrite.check(`-2/3*x+1`)
[[?]] Lies die Punkte $P$ und $Q$ ab. Berechne daraus die Steigung und anschließend den Ordinatenabschnitt.
*****************
Aus $P(-3\mid3)$ und $Q(3\mid-1)$ folgt
$
m_u=\frac{-1-3}{3-(-3)}=-\frac23.
$

Mit $P$ erhält man $3=-\frac23\cdot(-3)+b$, also $b=1$. Daher gilt
$
u(x)=-\frac23x+1.
$
*****************

@resetter

@ADetails(`3=BE;Lineare Funktionen, Graph ablesen, Steigung, Ordinatenabschnitt`)

</div>

</section>


## Aufgabe 3: Höhen von Spitzkörpern

**Berechne** jeweils die senkrechte Körperhöhe. **Gib** alle Ergebnisse als exakte Werte **an**.

<section class="dynFlex" data-basis="48%" data-min="30%">

<div class="flex-child">

__$a)\;\;$__ Ein Spitzkörper hat das Volumen $V=540\,\mathrm{cm}^3$ und den Grundflächeninhalt $G=90\,\mathrm{cm}^2$.

<!-- data-hint-button="2" data-solution-button="3" -->
$h=$ [[ 18 ]] $\mathrm{cm}$ @canvas
@Algebrite.check(18)
[[?]] Stelle $V=\frac13Gh$ nach $h$ um.
*****************
$$
h=\frac{3V}{G}
=\frac{3\cdot540\,\mathrm{cm}^3}{90\,\mathrm{cm}^2}
=18\,\mathrm{cm}.
$$
*****************

@resetter

@ADetails(`2=BE;Spitzkörper, Volumen, Höhe, Gleichung umstellen`)

</div>

<div class="flex-child">

__$b)\;\;$__ Eine quadratische Pyramide hat die Grundkante $a=8\,\mathrm{cm}$ und das Volumen $V=640\,\mathrm{cm}^3$.

<!-- data-hint-button="2" data-solution-button="3" -->
$h=$ [[ 30 ]] $\mathrm{cm}$ @canvas
@Algebrite.check(30)
[[?]] Für die quadratische Grundfläche gilt $G=a^2$.
*****************
$$
G=8^2\,\mathrm{cm}^2=64\,\mathrm{cm}^2,
\qquad
h=\frac{3\cdot640}{64}\,\mathrm{cm}
=30\,\mathrm{cm}.
$$
*****************

@resetter

@ADetails(`3=BE;Pyramide, Quadratische Grundfläche, Volumen, Höhe`)

</div>

<div class="flex-child">

__$c)\;\;$__ Eine Pyramide besitzt eine $12\,\mathrm{cm}$ lange und $7\,\mathrm{cm}$ breite rechteckige Grundfläche. Ihr Volumen beträgt $0{,}504\,\mathrm{dm}^3$.

<!-- data-hint-button="2" data-solution-button="3" -->
$h=$ [[ 18 ]] $\mathrm{cm}$ @canvas
@Algebrite.check(18)
[[?]] Rechne das Volumen zuerst in Kubikzentimeter um und bestimme dann $G$.
*****************
$$
V=0{,}504\,\mathrm{dm}^3=504\,\mathrm{cm}^3,
\qquad
G=12\cdot7\,\mathrm{cm}^2=84\,\mathrm{cm}^2.
$$

$$
h=\frac{3\cdot504}{84}\,\mathrm{cm}
=18\,\mathrm{cm}.
$$
*****************

@resetter

@ADetails(`4=BE;Pyramide, Rechteckige Grundfläche, Volumeneinheiten, Höhe`)

</div>

</section>

---

<section class="dynFlex" data-basis="48%" data-min="30%">

<div class="flex-child">

__$d)\;\;$__ Die Grundfläche einer Pyramide ist ein Dreieck mit $g=12\,\mathrm{cm}$ und der zugehörigen Dreieckshöhe $h_g=5\,\mathrm{cm}$. Das Volumen beträgt $360\,\mathrm{cm}^3$.

<!-- data-hint-button="2" data-solution-button="3" -->
$h=$ [[ 36 ]] $\mathrm{cm}$ @canvas
@Algebrite.check(36)
[[?]] Berechne die Grundfläche mit $G=\frac12g h_g$.
*****************
$$
G=\frac12\cdot12\cdot5\,\mathrm{cm}^2
=30\,\mathrm{cm}^2,
\qquad
h=\frac{3\cdot360}{30}\,\mathrm{cm}
=36\,\mathrm{cm}.
$$
*****************

@resetter

@ADetails(`4=BE;Pyramide, Dreieckige Grundfläche, Volumen, Höhe`)

</div>

<div class="flex-child">

__$e)\;\;$__ Ein Kegel hat den Durchmesser $d=10\,\mathrm{cm}$ und das Volumen $V=200\pi\,\mathrm{cm}^3$.

<!-- data-hint-button="2" data-solution-button="3" -->
$h=$ [[ 24 ]] $\mathrm{cm}$ @canvas
@Algebrite.check(24)
[[?]] Halbiere den Durchmesser. Setze $G=\pi r^2$ in $h=\frac{3V}{G}$ ein.
*****************
$$
r=5\,\mathrm{cm},
\qquad
G=25\pi\,\mathrm{cm}^2.
$$

$$
h=\frac{3\cdot200\pi}{25\pi}\,\mathrm{cm}
=24\,\mathrm{cm}.
$$
*****************

@resetter

@ADetails(`4=BE;Kegel, Durchmesser, Kreisfläche, Volumen, Höhe`)

</div>

<div class="flex-child">

__$f)\;\;$__ Ein Zylinder mit $r_Z=4\,\mathrm{cm}$ und $h_Z=6\,\mathrm{cm}$ hat dasselbe Volumen wie ein Kegel mit $r_K=6\,\mathrm{cm}$. **Bestimme** die Kegelhöhe $h_K$.

<!-- data-hint-button="2" data-solution-button="3" -->
$h_K=$ [[ 8 ]] $\mathrm{cm}$ @canvas
@Algebrite.check(8)
[[?]] Setze die Volumenformeln gleich. Der Faktor $\pi$ kürzt sich.
*****************
$$
\pi r_Z^2h_Z
=\frac13\pi r_K^2h_K.
$$

$$
h_K
=\frac{3r_Z^2h_Z}{r_K^2}
=\frac{3\cdot4^2\cdot6}{6^2}\,\mathrm{cm}
=8\,\mathrm{cm}.
$$
*****************

@resetter

@ADetails(`4=BE;Kegel, Zylinder, Gleiches Volumen, Höhe, Gleichung umstellen`)

</div>

</section>




## Aufgabe 5: Prisma mit zusammengesetzter Grundfläche

Die Grundfläche eines geraden Prismas besteht aus einem gleichschenkligen Dreieck und zwei außen angesetzten Halbkreisen. Die Grundseite des Dreiecks ist $a=13{,}6\,\mathrm{cm}$ lang, die beiden gleich langen Seiten haben jeweils die Länge $s=11{,}3\,\mathrm{cm}$.

@Koordinatensystem(`xmin=-12;xmax=12;ymin=-2.2;ymax=13;width=720;id=PLK9PrismaBasis;achsen=0;grid=0;border=0`)

@Flaeche(`PLK9PrismaBasis;[[-12;-2.2];[12;-2.2];[12;13];[-12;13]];#ffffff;1;inhalt=0;umfang=0`)

@Punkt(`PLK9PrismaBasis;PLK9PB_A=0;-6.8;0;#000000;0;fix`)
@Punkt(`PLK9PrismaBasis;PLK9PB_B=0;6.8;0;#000000;0;fix`)
@Punkt(`PLK9PrismaBasis;PLK9PB_C=0;0;9.024965374;#000000;0;fix`)
@Punkt(`PLK9PrismaBasis;PLK9PB_L=0;-3.4;4.512482687;#000000;0;fix`)
@Punkt(`PLK9PrismaBasis;PLK9PB_R=0;3.4;4.512482687;#000000;0;fix`)

@Flaeche(`PLK9PrismaBasis;[PLK9PB_A;PLK9PB_B;PLK9PB_C];#c8edf5;1;inhalt=0;umfang=0`)
@Kreissektor(`PLK9PrismaBasis;[PLK9PB_L;PLK9PB_C;PLK9PB_A];#c8edf5;1;PLK9PB_HalbL=0;inhalt=0;umfang=0`)
@Kreissektor(`PLK9PrismaBasis;[PLK9PB_R;PLK9PB_B;PLK9PB_C];#c8edf5;1;PLK9PB_HalbR=0;inhalt=0;umfang=0`)
@Kreissektor(`PLK9PrismaBasis;[PLK9PB_L;PLK9PB_C;PLK9PB_A];#171717;0;PLK9PB_RandL=0;inhalt=0;umfang=0`)
@Kreissektor(`PLK9PrismaBasis;[PLK9PB_R;PLK9PB_B;PLK9PB_C];#171717;0;PLK9PB_RandR=0;inhalt=0;umfang=0`)

@Strecke(`PLK9PrismaBasis;[PLK9PB_A;PLK9PB_C];#c8edf5;;-;4px`)
@Strecke(`PLK9PrismaBasis;[PLK9PB_C;PLK9PB_B];#c8edf5;;-;4px`)
@Strecke(`PLK9PrismaBasis;[PLK9PB_A;PLK9PB_C];#555555;;-;1px;linestyle=dashed`)
@Strecke(`PLK9PrismaBasis;[PLK9PB_C;PLK9PB_B];#555555;;-;1px;linestyle=dashed`)
@Strecke(`PLK9PrismaBasis;[PLK9PB_A;PLK9PB_B];#171717;;-;2px`)
@Strecke(`PLK9PrismaBasis;[[0;0];[0;9.024965374]];#555555;;-;1px;linestyle=dashed`)
@Strecke(`PLK9PrismaBasis;[[0;0];[0.35;0];[0.35;0.35];[0;0.35]];#171717;;-;1px`)

@Strecke(`PLK9PrismaBasis;[[-6.8;-0.8];[6.8;-0.8]];#171717;;-;1px;linestyle=dashed`)
@Strecke(`PLK9PrismaBasis;[[-6.8;0];[-6.8;-1.05]];#171717;;-;1px;linestyle=dashed`)
@Strecke(`PLK9PrismaBasis;[[6.8;0];[6.8;-1.05]];#171717;;-;1px;linestyle=dashed`)

@KoordText(`PLK9PrismaBasis;[0;-1.38];$a=13{,}6\,\mathrm{cm}$;#171717;1`)
@KoordText(`PLK9PrismaBasis;[-4.8;5.1];$s=11{,}3\,\mathrm{cm}$;#171717;1`)
@KoordText(`PLK9PrismaBasis;[4.8;5.1];$s=11{,}3\,\mathrm{cm}$;#171717;1`)
@KoordText(`PLK9PrismaBasis;[0.65;3.8];$h_{\triangle}$;#171717;1`)

Das Prisma hat die Höhe $k=18{,}7\,\mathrm{cm}$.

<section class="dynFlex" data-basis="48%" data-min="30%">

<div class="flex-child">

__$a)\;\;$__ **Berechne** die Dreieckshöhe $h_\triangle$.

<!-- data-hint-button="2" data-solution-button="3" -->
$h_\triangle\approx$ [[ 9,02 ]] $\mathrm{cm}$ @canvas
@Algebrite.check2(`sqrt(11.3^2-(13.6/2)^2)`,0.005)
[[?]] Die Dreieckshöhe halbiert die Grundseite. Eine Kathete ist daher $6{,}8\,\mathrm{cm}$ lang.
*****************
$$
\begin{aligned}
h_\triangle^2+6{,}8^2&=11{,}3^2,\\
h_\triangle&=\sqrt{11{,}3^2-6{,}8^2}\,\mathrm{cm}\\
&=\sqrt{81{,}45}\,\mathrm{cm}
\approx9{,}02\,\mathrm{cm}.
\end{aligned}
$$
*****************

@resetter

@ADetails(`3=BE;Satz des Pythagoras, Gleichschenkliges Dreieck, Dreieckshöhe`)

</div>

<div class="flex-child">

__$b)\;\;$__ **Berechne** den Flächeninhalt $G$ der zusammengesetzten Grundfläche.

<!-- data-hint-button="2" data-solution-button="3" -->
$G\approx$ [[ 161,66 ]] $\mathrm{cm}^2$ @canvas
@Algebrite.check2(`0.5*13.6*sqrt(11.3^2-(13.6/2)^2)+pi*(11.3/2)^2`,0.005)
[[?]] Addiere die Dreiecksfläche und die Flächen der beiden Halbkreise. Rechne mit der ungerundeten Dreieckshöhe.
*****************
Die beiden Halbkreise ergeben zusammen einen Kreis mit
$$
r=\frac{11{,}3}{2}\,\mathrm{cm}=5{,}65\,\mathrm{cm}.
$$

Damit gilt:
$$
\begin{aligned}
G
&=\frac12\cdot13{,}6\cdot\sqrt{81{,}45}
+\pi\cdot5{,}65^2\;\mathrm{cm}^2\\
&\approx161{,}66\,\mathrm{cm}^2.
\end{aligned}
$$
*****************

@resetter

@ADetails(`4=BE;Zusammengesetzte Fläche, Dreieck, Halbkreise, Flächeninhalt`)

</div>

<div class="flex-child">

__$c)\;\;$__ **Berechne** das Volumen $V$ des Prismas.

<!-- data-hint-button="2" data-solution-button="3" -->
$V\approx$ [[ 3022,99 ]] $\mathrm{cm}^3$ @canvas
@Algebrite.check2(`(0.5*13.6*sqrt(11.3^2-(13.6/2)^2)+pi*(11.3/2)^2)*18.7`,0.005)
[[?]] Verwende $V=G\cdot H$ und den ungerundeten Flächeninhalt aus b).
*****************
$$
\begin{aligned}
V
&=G\cdot H\\
&=\left(\frac12\cdot13{,}6\cdot\sqrt{81{,}45}
+\pi\cdot5{,}65^2\right)\cdot18{,}7\;\mathrm{cm}^3\\
&\approx3022{,}99\,\mathrm{cm}^3.
\end{aligned}
$$
*****************

@resetter

@ADetails(`3=BE;Prisma, Grundfläche, Volumen`)

</div>

</section>

---

<section class="dynFlex" data-basis="48%" data-min="30%">

<div class="flex-child">

__$d)\;\;$__ Das massive Prisma besteht aus einem Material mit der Dichte $\rho=0{,}83\,\frac{\mathrm{g}}{\mathrm{cm}^3}$. **Berechne** seine Masse $m$.

<!-- data-hint-button="2" data-solution-button="3" -->
$m\approx$ [[ 2509,08 ]] $\mathrm{g}$ @canvas
@Algebrite.check2(`0.83*(0.5*13.6*sqrt(11.3^2-(13.6/2)^2)+pi*(11.3/2)^2)*18.7`,0.005)
[[?]] Verwende $m=\rho\cdot V$ mit dem ungerundeten Volumen aus c).
*****************
$$
\begin{aligned}
m
&=\rho\cdot V\\
&=0{,}83\,\frac{\mathrm{g}}{\mathrm{cm}^3}
\cdot3022{,}990687\ldots\,\mathrm{cm}^3\\
&\approx2509{,}08\,\mathrm{g}.
\end{aligned}
$$
*****************

@resetter

@ADetails(`3=BE;Prisma, Dichte, Masse, Volumen`)

</div>

<div class="flex-child">

__$e)\;\;$__ **Berechne** den Oberflächeninhalt $O$ des Prismas.

<!-- data-hint-button="2" data-solution-button="3" -->
$O\approx$ [[ 1241,48 ]] $\mathrm{cm}^2$ @canvas
@Algebrite.check2(`2*(0.5*13.6*sqrt(11.3^2-(13.6/2)^2)+pi*(11.3/2)^2)+(13.6+pi*11.3)*18.7`,0.005)
[[?]] Zum äußeren Umfang gehören die Grundseite und die beiden Halbkreisbögen. Die gestrichelten Durchmesser werden nicht mitgezählt.
*****************
Die beiden Halbkreisbögen haben zusammen die Länge eines Kreisumfangs mit $r=5{,}65\,\mathrm{cm}$:
$$
u_G=13{,}6+2\pi\cdot5{,}65
=13{,}6+11{,}3\pi
\approx49{,}10\,\mathrm{cm}.
$$

Mit $O=2G+u_GH$ folgt:
$$
\begin{aligned}
O
&=2\cdot161{,}657256\ldots
+(13{,}6+11{,}3\pi)\cdot18{,}7\;\mathrm{cm}^2\\
&\approx1241{,}48\,\mathrm{cm}^2.
\end{aligned}
$$
*****************

@resetter

@ADetails(`5=BE;Prisma, Oberfläche, Grundfläche, Umfang, Halbkreisbogen`)

</div>


</section>

---




__$f)\;\;$__ Eine quaderförmige Verpackung soll das Prisma ohne Spielraum umschließen. Ihre Kanten verlaufen parallel zur Dreiecksgrundseite, zur Dreieckshöhe und zu den Seitenkanten des Prismas. Bezeichne die zugehörigen Kantenlängen mit $l$, $b$ und $h_Q$. Aus der Geometrie der Grundfläche ergeben sich

$$
l=s+\frac a2,
\qquad
b=\frac{s+h_\triangle}{2},
\qquad
h_Q=k.
$$

Für Klebe- und Verschlusslaschen werden $10\,\%$ mehr Karton als der Oberflächeninhalt des Quaders benötigt. **Berechne** den Oberflächeninhalt des Quaders $O_Q$ und die benötigte Kartonfläche $A_\mathrm{Karton}$.

<!-- data-hint-button="2" data-solution-button="3" -->
$O_Q\approx$ [[ 1424,90 ]] $\mathrm{cm}^2$; $A_\mathrm{Karton}\approx$ [[ 1567,39 ]] $\mathrm{cm}^2$ @canvas
@Algebrite.check([1424.90;1567.39])
[[?]] Berechne zuerst $l$, $b$ und $h_Q$. Verwende danach $O_Q=2(lb+lh_Q+bh_Q)$ und rechne mit der ungerundeten Dreieckshöhe.
*****************
Die Kantenlängen der Verpackung sind:
$$
\begin{aligned}
l&=11{,}3+\frac{13{,}6}{2}
=18{,}1\,\mathrm{cm},\\
b&=\frac{11{,}3+\sqrt{81{,}45}}{2}\,\mathrm{cm}
\approx10{,}1624827\,\mathrm{cm},\\
h_Q&=18{,}7\,\mathrm{cm}.
\end{aligned}
$$

Damit ergibt sich:
$$
\begin{aligned}
O_Q
&=2(lb+lh_Q+bh_Q)\\
&\approx1424{,}90\,\mathrm{cm}^2.
\end{aligned}
$$

Für die Laschen werden zusätzlich $10\,\%$ benötigt:
$$
A_\mathrm{Karton}
=1{,}10\cdot O_Q
\approx1567{,}39\,\mathrm{cm}^2.
$$
*****************

@resetter

@ADetails(`4=BE;Quader, Oberflächeninhalt, Verpackung, Prozentrechnung`)






## Aufgabe 6: Eine Pyramide wird aus einem Zylinder herausgeschnitten

Ein massiver zylindrischer Rohling aus Stahl hat vor der Bearbeitung die Masse

$$m=6{,}84\,\mathrm{kg}$$

und die Dichte

$$\rho=7{,}85\,\frac{\mathrm{g}}{\mathrm{cm}^3}.$$

Von einer Grundfläche aus wird eine **gerade quadratische Pyramide** aus dem Zylinder herausgeschnitten:

- Die quadratische Grundfläche der Pyramide liegt in der oberen Grundfläche des Zylinders.
- Ihre vier Eckpunkte liegen auf dem kleineren, zum Zylinder konzentrischen Kreis $k$.
- Der Kreis $k$ hat einen um $20\,\%$ kleineren Flächeninhalt als die Grundfläche des Zylinders. Es gilt also $A_k=0{,}80A_Z$.
- Die Pyramidenspitze liegt auf der Zylinderachse. Die Aussparung reicht $75\,\%$ der Zylinderhöhe tief in den Zylinder hinein.

@Koordinatensystem(`xmin=-2;xmax=22;ymin=-1.5;ymax=12.5;width=900;id=PLK9ZylinderPyramide;achsen=0;grid=0;border=0`)

@Flaeche(`PLK9ZylinderPyramide;[[-2;-1.5];[22;-1.5];[22;12.5];[-2;12.5]];#ffffff;1;inhalt=0;umfang=0`)

@Flaeche(`PLK9ZylinderPyramide;[[1;0];[7;0];[7;10];[1;10]];#c8edf5;1;inhalt=0;umfang=0`)
@Strecke(`PLK9ZylinderPyramide;[[1;0];[7;0];[7;10];[1;10];[1;0]];#171717;;-;2px`)
@Flaeche(`PLK9ZylinderPyramide;[[1.316718427;10];[6.683281573;10];[4;2.5]];#ffffff;1;inhalt=0;umfang=0`)
@Strecke(`PLK9ZylinderPyramide;[[1.316718427;10];[6.683281573;10];[4;2.5];[1.316718427;10]];#171717;;-;2px`)
@Strecke(`PLK9ZylinderPyramide;[[4;10];[4;2.5]];#555555;;-;1px;linestyle=dashed`)
@Strecke(`PLK9ZylinderPyramide;[[0.45;0];[0.45;10]];#555555;;-;1px;linestyle=dashed`)
@Strecke(`PLK9ZylinderPyramide;[[0.2;0];[0.7;0]];#555555;;-;1px`)
@Strecke(`PLK9ZylinderPyramide;[[0.2;10];[0.7;10]];#555555;;-;1px`)
@Strecke(`PLK9ZylinderPyramide;[[3.78;2.72];[4;2.72];[4;2.5]];#555555;;-;1px`)
@KoordText(`PLK9ZylinderPyramide;[4;11.5];$\text{Achsenschnitt}$;#171717;1`)
@KoordText(`PLK9ZylinderPyramide;[-0.15;5];$h_Z$;#171717;1`)
@KoordText(`PLK9ZylinderPyramide;[4.55;6.25];$h_P$;#171717;1`)
@KoordText(`PLK9ZylinderPyramide;[4.3;2.15];$S$;#171717;1`)

@Punkt(`PLK9ZylinderPyramide;PLK9ZPM=0;16;5;#171717;0;fix`)
@Kreis(`PLK9ZylinderPyramide;PLK9ZylinderGrundkreis=0;PLK9ZPM;#c8edf5;1;radius=3;inhalt=0;umfang=0`)
@Kreis(`PLK9ZylinderPyramide;PLK9ZylinderKontur=0;PLK9ZPM;#171717;0;radius=3;inhalt=0;umfang=0`)
@Kreis(`PLK9ZylinderPyramide;PLK9PyramidenUmkreis=0;PLK9ZPM;#555555;0;radius=2.683281573;inhalt=0;umfang=0;linestyle=dashed`)
@Flaeche(`PLK9ZylinderPyramide;[[16;7.683281573];[18.683281573;5];[16;2.316718427];[13.316718427;5]];#ffffff;1;inhalt=0;umfang=0`)
@Strecke(`PLK9ZylinderPyramide;[[16;7.683281573];[18.683281573;5];[16;2.316718427];[13.316718427;5];[16;7.683281573]];#171717;;-;2px`)
@Strecke(`PLK9ZylinderPyramide;[[16;5];[19;5]];#555555;;-;1px;linestyle=dashed`)
@Strecke(`PLK9ZylinderPyramide;[[16;5];[18.683281573;5]];#171717;;-;1px`)
@KoordText(`PLK9ZylinderPyramide;[16;11.5];$\text{Draufsicht}$;#171717;1`)
@KoordText(`PLK9ZylinderPyramide;[17.35;5.45];$r$;#171717;1`)
@KoordText(`PLK9ZylinderPyramide;[19.35;5.45];$R$;#171717;1`)
@KoordText(`PLK9ZylinderPyramide;[16;0.9];$A_k=0{,}80A_Z$;#171717;1`)

*Achsenschnitt und Draufsicht sind nicht maßstabsgetreu. Die weißen Flächen zeigen die pyramidenförmige Aussparung.*

<section class="dynFlex" data-basis="48%" data-min="30%">

<div class="flex-child">

__$a)\;\;$__ **Berechne** aus Masse und Dichte das Volumen $V_Z$ des zylindrischen Rohlings.

<!-- data-hint-button="2" data-solution-button="3" -->
$V_Z\approx$ [[ 871,34 ]] $\mathrm{cm}^3$ @canvas
@Algebrite.check2(`6840/7.85`,0.005)
[[?]] Rechne die Masse zuerst in Gramm um. Stelle dann $\rho=\frac{m}{V}$ nach $V$ um.
*****************
Zunächst wird die Masse in Gramm umgerechnet:

$$m=6{,}84\,\mathrm{kg}=6840\,\mathrm{g}.$$

Mit $\rho=\frac{m}{V}$ folgt:

$$
\begin{aligned}
V_Z&=\frac{m}{\rho}\\
&=\frac{6840\,\mathrm{g}}{7{,}85\,\frac{\mathrm{g}}{\mathrm{cm}^3}}\\
&\approx871{,}34\,\mathrm{cm}^3.
\end{aligned}
$$
*****************

@resetter

@ADetails(`3=BE;Dichte, Masse, Volumen, Einheiten umrechnen`)

</div>

<div class="flex-child">

__$b)\;\;$__ Die Körperhöhe des Zylinders beträgt $h_Z=15{,}4\,\mathrm{cm}$. **Berechne** den Radius $R$ seiner Grundfläche.

<!-- data-hint-button="2" data-solution-button="3" -->
$R\approx$ [[ 4,24 ]] $\mathrm{cm}$ @canvas
@Algebrite.check2(`sqrt((6840/7.85)/(pi*15.4))`,0.005)
[[?]] Setze das Volumen aus a) in $V_Z=\pi R^2h_Z$ ein und stelle die Formel nach $R$ um.
*****************
Für den Zylinder gilt:

$$V_Z=\pi R^2h_Z.$$

Nach $R$ umgestellt erhält man:

$$
\begin{aligned}
R&=\sqrt{\frac{V_Z}{\pi h_Z}}\\
&=\sqrt{\frac{871{,}337\ldots\,\mathrm{cm}^3}
{\pi\cdot15{,}4\,\mathrm{cm}}}\\
&\approx4{,}24\,\mathrm{cm}.
\end{aligned}
$$
*****************

@resetter

@ADetails(`4=BE;Zylinder, Volumen, Radius, Formel umstellen`)

</div>

<div class="flex-child">

__$c)\;\;$__ **Berechne** den Radius $r$ des kleineren Kreises $k$, auf dem die vier Eckpunkte des Grundquadrats liegen.

<!-- data-hint-button="2" data-solution-button="3" -->
$r\approx$ [[ 3,80 ]] $\mathrm{cm}$ @canvas
@Algebrite.check2(`sqrt(0.8)*sqrt((6840/7.85)/(pi*15.4))`,0.005)
[[?]] „$20\,\%$ kleiner“ bedeutet $A_k=0{,}80A_Z$. Vergleiche $\pi r^2$ mit $\pi R^2$.
*****************
Für die beiden Kreisflächen gilt:

$$
A_k=0{,}80A_Z.
$$

Daher ist

$$
\begin{aligned}
\pi r^2&=0{,}80\pi R^2,\\
r^2&=0{,}80R^2,\\
r&=\sqrt{0{,}80}\,R.
\end{aligned}
$$

Mit dem ungerundeten Radius aus b) folgt:

$$
r=\sqrt{0{,}80}\cdot4{,}2438\ldots\,\mathrm{cm}
\approx3{,}80\,\mathrm{cm}.
$$

Der Radius ist also nicht einfach um $20\,\%$ kleiner, weil sich die Prozentangabe auf den **Flächeninhalt** bezieht.
*****************

@resetter

@ADetails(`3=BE;Kreisfläche, Prozentrechnung, Radius, Formel umstellen`)

</div>

</section>

---

<section class="dynFlex" data-basis="48%" data-min="30%">

<div class="flex-child">

__$d)\;\;$__ **Bestimme** die Höhe $h_P$ der herausgeschnittenen Pyramide.

<!-- data-hint-button="2" data-solution-button="3" -->
$h_P=$ [[ 11,55 ]] $\mathrm{cm}$ @canvas
@Algebrite.check2(`0.75*15.4`,0.005)
[[?]] Die Höhe der geraden Pyramide ist hier gleich der Tiefe, bis zu der die Aussparung in den Zylinder hineinreicht.
*****************
Die Aussparung reicht $75\,\%$ der Zylinderhöhe tief in den Zylinder. Deshalb gilt:

$$
h_P=0{,}75h_Z
=0{,}75\cdot15{,}4\,\mathrm{cm}
=11{,}55\,\mathrm{cm}.
$$
*****************

@resetter

@ADetails(`2=BE;Pyramide, Körperhöhe, Prozentrechnung`)

</div>

<div class="flex-child">

__$e)\;\;$__ **Berechne** das Volumen $V_P$ der herausgeschnittenen quadratischen Pyramide.

<!-- data-hint-button="2" data-solution-button="3" -->
$V_P\approx$ [[ 110,94 ]] $\mathrm{cm}^3$ @canvas
@Algebrite.check2(`(1/3)*(sqrt(2)*sqrt(0.8)*sqrt((6840/7.85)/(pi*15.4)))^2*(0.75*15.4)`,0.005)
[[?]] Der Durchmesser $2r$ des kleineren Kreises ist die Diagonale des Grundquadrats. Bestimme daraus zuerst die Quadratseite oder direkt die Quadratfläche.
*****************
Die Diagonale $d_Q$ des Grundquadrats ist der Durchmesser des kleineren Kreises:

$$d_Q=2r.$$

Für ein Quadrat mit Seitenlänge $a$ gilt $d_Q=a\sqrt2$. Daher ist

$$
a=\frac{2r}{\sqrt2}=\sqrt2\,r
$$

und damit

$$
G_P=a^2=2r^2.
$$

Mit dem ungerundeten Wert $r=3{,}7958\ldots\,\mathrm{cm}$ aus c) ergibt sich:

$$
G_P=2\cdot(3{,}7958\ldots\,\mathrm{cm})^2
\approx28{,}82\,\mathrm{cm}^2.
$$

Das Volumen der Pyramide beträgt:

$$
\begin{aligned}
V_P&=\frac13G_Ph_P\\
&=\frac13\cdot28{,}8161\ldots\,\mathrm{cm}^2
\cdot11{,}55\,\mathrm{cm}\\
&\approx110{,}94\,\mathrm{cm}^3.
\end{aligned}
$$
*****************

@resetter

@ADetails(`5=BE;Quadrat im Kreis, Diagonale, Pyramide, Grundfläche, Volumen`)

</div>

</section>


## Aufgabe 7: Vom Zylinder über den Kegel zur Pyramide

Ein massiver Zylinder aus Messing hat die Masse

$$m=5{,}37\,\mathrm{kg}$$

und die Dichte

$$\rho=8{,}40\,\frac{\mathrm{g}}{\mathrm{cm}^3}.$$

Seine Körperhöhe beträgt $h_Z=14{,}6\,\mathrm{cm}$. Der Zylinder wird ohne Materialverlust zu einem geraden Kreiskegel umgeformt. Der Kegel besitzt dieselbe Körperhöhe wie der Zylinder.

Für einen weiteren Entwurf wird anschließend eine gerade quadratische Pyramide betrachtet. Die benötigten Größen werden in den Teilaufgaben festgelegt.

@Koordinatensystem(`xmin=-1;xmax=30;ymin=-1.5;ymax=11.5;width=920;id=PLK9Koerperkette;achsen=0;grid=0;border=0`)

@Flaeche(`PLK9Koerperkette;[[-1;-1.5];[30;-1.5];[30;11.5];[-1;11.5]];#ffffff;1;inhalt=0;umfang=0`)

@Flaeche(`PLK9Koerperkette;[[1;1];[6.5;1];[6.5;8.5];[1;8.5]];#c8edf5;1;inhalt=0;umfang=0`)
@Strecke(`PLK9Koerperkette;[[1;1];[6.5;1];[6.5;8.5];[1;8.5];[1;1]];#171717;;-;2px`)
@Strecke(`PLK9Koerperkette;[[0.4;1];[0.4;8.5]];#555555;;-;1px;linestyle=dashed`)
@Strecke(`PLK9Koerperkette;[[0.15;1];[0.65;1]];#555555;;-;1px`)
@Strecke(`PLK9Koerperkette;[[0.15;8.5];[0.65;8.5]];#555555;;-;1px`)
@KoordText(`PLK9Koerperkette;[3.75;10.3];$\text{Zylinder}$;#171717;1`)
@KoordText(`PLK9Koerperkette;[-0.05;4.75];$h_Z$;#171717;1`)
@KoordText(`PLK9Koerperkette;[3.75;5.15];$V_Z$;#171717;1`)

@Flaeche(`PLK9Koerperkette;[[10;1];[17;1];[13.5;8.5]];#c8edf5;1;inhalt=0;umfang=0`)
@Strecke(`PLK9Koerperkette;[[10;1];[17;1];[13.5;8.5];[10;1]];#171717;;-;2px`)
@Strecke(`PLK9Koerperkette;[[13.5;1];[13.5;8.5]];#555555;;-;1px;linestyle=dashed`)
@Strecke(`PLK9Koerperkette;[[13.5;1];[17;1]];#555555;;-;1px`)
@Strecke(`PLK9Koerperkette;[[13.5;1.25];[13.75;1.25];[13.75;1]];#555555;;-;1px`)
@KoordText(`PLK9Koerperkette;[13.5;10.3];$\text{Kegel}$;#171717;1`)
@KoordText(`PLK9Koerperkette;[14.05;4.75];$h_K$;#171717;1`)
@KoordText(`PLK9Koerperkette;[15.25;0.55];$r$;#171717;1`)
@KoordText(`PLK9Koerperkette;[16.15;5.1];$\ell$;#171717;1`)

@Flaeche(`PLK9Koerperkette;[[20.5;2.1];[25.4;1.2];[24.5;9]];#c8edf5;1;inhalt=0;umfang=0`)
@Flaeche(`PLK9Koerperkette;[[25.4;1.2];[28.5;2.7];[24.5;9]];#c8edf5;1;inhalt=0;umfang=0`)
@Flaeche(`PLK9Koerperkette;[[28.5;2.7];[23.6;3.6];[24.5;9]];#c8edf5;1;inhalt=0;umfang=0`)
@Flaeche(`PLK9Koerperkette;[[23.6;3.6];[20.5;2.1];[24.5;9]];#c8edf5;1;inhalt=0;umfang=0`)
@Strecke(`PLK9Koerperkette;[[20.5;2.1];[25.4;1.2];[28.5;2.7]];#171717;;-;2px`)
@Strecke(`PLK9Koerperkette;[[28.5;2.7];[23.6;3.6];[20.5;2.1]];#555555;;-;1px;linestyle=dashed`)
@Strecke(`PLK9Koerperkette;[[24.5;9];[20.5;2.1];[24.5;9];[25.4;1.2];[24.5;9];[28.5;2.7]];#171717;;-;2px`)
@Strecke(`PLK9Koerperkette;[[24.5;9];[23.6;3.6]];#555555;;-;1px;linestyle=dashed`)
@Strecke(`PLK9Koerperkette;[[24.5;9];[24.5;2.4]];#555555;;-;1px;linestyle=dashed`)
@Strecke(`PLK9Koerperkette;[[20.5;2.1];[28.5;2.7]];#555555;;-;1px;linestyle=dashed`)
@Strecke(`PLK9Koerperkette;[[24.5;2.65];[24.75;2.65];[24.75;2.4]];#555555;;-;1px`)
@KoordText(`PLK9Koerperkette;[24.5;10.3];$\text{Pyramide}$;#171717;1`)
@KoordText(`PLK9Koerperkette;[23.9;5.8];$h_P$;#171717;1`)
@KoordText(`PLK9Koerperkette;[26.25;6.1];$s$;#171717;1`)
@KoordText(`PLK9Koerperkette;[22.4;1.7];$d_P$;#171717;1`)

*Die Skizzen sind nicht maßstabsgetreu. Verwende in aufeinanderfolgenden Teilaufgaben möglichst die ungerundeten Zwischenergebnisse.*

<section class="dynFlex" data-basis="48%" data-min="30%">

<div class="flex-child">

__$a)\;\;$__ **Berechne** das Volumen $V_Z$ des Zylinders.

<!-- data-hint-button="2" data-solution-button="3" -->
$V_Z\approx$ [[ 639,29 ]] $\mathrm{cm}^3$ @canvas
@Algebrite.check2(`5370/8.4`,0.005)
[[?]] Rechne die Masse in Gramm um und stelle $\rho=\frac{m}{V}$ nach $V$ um.
*****************
Die Masse beträgt

$$m=5{,}37\,\mathrm{kg}=5370\,\mathrm{g}.$$

Aus $\rho=\frac{m}{V}$ folgt:

$$
\begin{aligned}
V_Z&=\frac{m}{\rho}\\
&=\frac{5370\,\mathrm{g}}{8{,}40\,\frac{\mathrm{g}}{\mathrm{cm}^3}}\\
&\approx639{,}29\,\mathrm{cm}^3.
\end{aligned}
$$
*****************

@resetter

@ADetails(`3=BE;Dichte, Masse, Zylinder, Volumen, Einheiten umrechnen`)

</div>

<div class="flex-child">

__$b)\;\;$__ Der Kegel hat dasselbe Volumen und dieselbe Körperhöhe wie der Zylinder. **Berechne** den Radius $r$ seiner Grundfläche.

<!-- data-hint-button="2" data-solution-button="3" -->
$r\approx$ [[ 6,47 ]] $\mathrm{cm}$ @canvas
@Algebrite.check2(`sqrt(3*(5370/8.4)/(pi*14.6))`,0.005)
[[?]] Setze $V_K=V_Z$ und $h_K=14{,}6\,\mathrm{cm}$ in $V_K=\frac13\pi r^2h_K$ ein.
*****************
Für den Kegel gilt:

$$
V_K=\frac13\pi r^2h_K.
$$

Nach $r$ umgestellt:

$$
\begin{aligned}
r&=\sqrt{\frac{3V_K}{\pi h_K}}\\
&=\sqrt{\frac{3\cdot639{,}2857\ldots\,\mathrm{cm}^3}
{\pi\cdot14{,}6\,\mathrm{cm}}}\\
&\approx6{,}47\,\mathrm{cm}.
\end{aligned}
$$
*****************

@resetter

@ADetails(`4=BE;Kegel, Volumen, Radius, Formel umstellen`)

</div>

<div class="flex-child">

__$c)\;\;$__ **Berechne** den Umfang $U_K$ des Grundkreises des Kegels.

<!-- data-hint-button="2" data-solution-button="3" -->
$U_K\approx$ [[ 40,63 ]] $\mathrm{cm}$ @canvas
@Algebrite.check2(`2*pi*sqrt(3*(5370/8.4)/(pi*14.6))`,0.005)
[[?]] Verwende den ungerundeten Radius aus b) in $U_K=2\pi r$.
*****************
Mit dem ungerundeten Radius $r=6{,}4663\ldots\,\mathrm{cm}$ gilt:

$$
\begin{aligned}
U_K&=2\pi r\\
&=2\pi\cdot6{,}4663\ldots\,\mathrm{cm}\\
&\approx40{,}63\,\mathrm{cm}.
\end{aligned}
$$
*****************

@resetter

@ADetails(`2=BE;Kreis, Umfang, Kegelgrundfläche`)

</div>

</section>

---

<section class="dynFlex" data-basis="48%" data-min="30%">

<div class="flex-child">

__$d)\;\;$__ **Berechne** den Mantelflächeninhalt $M_K$ des Kegels.

<!-- data-hint-button="2" data-solution-button="3" -->
$M_K\approx$ [[ 324,38 ]] $\mathrm{cm}^2$ @canvas
@Algebrite.check2(`pi*sqrt(3*(5370/8.4)/(pi*14.6))*sqrt(14.6^2+3*(5370/8.4)/(pi*14.6))`,0.005)
[[?]] Bestimme zuerst die Mantellinie $\ell$ mit dem Satz des Pythagoras. Danach gilt $M_K=\pi r\ell$.
*****************
Radius, Körperhöhe und Mantellinie bilden ein rechtwinkliges Dreieck:

$$
\begin{aligned}
\ell&=\sqrt{h_K^2+r^2}\\
&=\sqrt{(14{,}6\,\mathrm{cm})^2+
(6{,}4663\ldots\,\mathrm{cm})^2}\\
&\approx15{,}9679\,\mathrm{cm}.
\end{aligned}
$$

Damit ist der Mantelflächeninhalt

$$
\begin{aligned}
M_K&=\pi r\ell\\
&=\pi\cdot6{,}4663\ldots\,\mathrm{cm}
\cdot15{,}9679\ldots\,\mathrm{cm}\\
&\approx324{,}38\,\mathrm{cm}^2.
\end{aligned}
$$
*****************

@resetter

@ADetails(`4=BE;Kegel, Mantellinie, Satz des Pythagoras, Mantelfläche`)

</div>

<div class="flex-child">

__$e)\;\;$__ Nun wird eine **gerade quadratische Pyramide** betrachtet. Ihre Höhe $h_P$ ist genauso lang wie der Umfang $U_K$ des Kegelgrundkreises. Der Inhalt ihrer quadratischen Grundfläche $G_P$ ist genauso groß wie der Mantelflächeninhalt $M_K$ des Kegels. **Berechne** die Diagonalenlänge $d_P$ der quadratischen Grundfläche.

<!-- data-hint-button="2" data-solution-button="3" -->
$d_P\approx$ [[ 25,47 ]] $\mathrm{cm}$ @canvas
@Algebrite.check2(`sqrt(2*pi*sqrt(3*(5370/8.4)/(pi*14.6))*sqrt(14.6^2+3*(5370/8.4)/(pi*14.6)))`,0.005)
[[?]] Für die Quadratseite $a$ gilt $a^2=G_P$. Die Diagonale eines Quadrats hat die Länge $d_P=a\sqrt2$.
*****************
Der Grundflächeninhalt der Pyramide entspricht dem Kegelmantel:

$$
G_P=M_K=324{,}3798\ldots\,\mathrm{cm}^2.
$$

Für ein Quadrat gilt $G_P=a^2$ und $d_P=a\sqrt2$. Daher kann die Diagonale direkt aus dem Flächeninhalt berechnet werden:

$$
\begin{aligned}
d_P&=\sqrt{G_P}\cdot\sqrt2\\
&=\sqrt{2G_P}\\
&=\sqrt{2\cdot324{,}3798\ldots\,\mathrm{cm}^2}\\
&\approx25{,}47\,\mathrm{cm}.
\end{aligned}
$$
*****************

@resetter

@ADetails(`4=BE;Quadrat, Grundfläche, Diagonale, Wurzel`)

</div>

<div class="flex-child">

__$f)\;\;$__ Die Spitze der geraden Pyramide liegt senkrecht über dem Mittelpunkt ihrer Grundfläche. **Berechne** die Seitenkante $s$ von der Pyramidenspitze zu einer Ecke der Grundfläche.

<!-- data-hint-button="2" data-solution-button="3" -->
$s\approx$ [[ 42,58 ]] $\mathrm{cm}$ @canvas
@Algebrite.check2(`sqrt((2*pi*sqrt(3*(5370/8.4)/(pi*14.6)))^2+(sqrt(2*pi*sqrt(3*(5370/8.4)/(pi*14.6))*sqrt(14.6^2+3*(5370/8.4)/(pi*14.6)))/2)^2)`,0.005)
[[?]] Mittelpunkt, Pyramidenspitze und eine Grundecke bilden ein rechtwinkliges Dreieck. Die Strecke vom Mittelpunkt zur Ecke ist die halbe Grundflächendiagonale.
*****************
Die Pyramidenhöhe ist gleich dem in c) berechneten Kreisumfang:

$$
h_P=U_K=40{,}6290\ldots\,\mathrm{cm}.
$$

Vom Mittelpunkt des Grundquadrats bis zu einer Ecke beträgt die Entfernung $\frac{d_P}{2}$. Mit dem Satz des Pythagoras folgt:

$$
\begin{aligned}
s&=\sqrt{h_P^2+\left(\frac{d_P}{2}\right)^2}\\
&=\sqrt{(40{,}6290\ldots\,\mathrm{cm})^2+
\left(\frac{25{,}4708\ldots\,\mathrm{cm}}2\right)^2}\\
&\approx42{,}58\,\mathrm{cm}.
\end{aligned}
$$
*****************

@resetter

@ADetails(`4=BE;Pyramide, Seitenkante, Grundflächendiagonale, Satz des Pythagoras`)

</div>

</section>
