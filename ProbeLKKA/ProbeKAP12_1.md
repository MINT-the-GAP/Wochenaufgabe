<!--
author: Martin Lommatzsch

version: 0.1.0

language: de

narrator: Deutsch Female

mode: Presentation

comment: Klausurähnliche Übungsaufgaben zu Schwingungen und Wellen für Physik in Klasse 12

tags: Physik, Klasse 12, Schwingungen, Wellen, Probeklausur

@style
main > *:not(:last-child) {
  margin-bottom: 3rem;
}

input {
  text-align: center;
}
@end

import: https://raw.githubusercontent.com/MINT-the-GAP/lia-DynFlex/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-timer/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-board-mode/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-marker/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-annotation/refs/heads/main/README.md
import: https://raw.githubusercontent.com/liaTemplates/algebrite/master/README.md
import: https://raw.githubusercontent.com/liaTemplates/JSXGraph/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-canvas-ocr/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-orthography/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-Mathe/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-kachel/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-navigation/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-resetter/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-coordinate/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-freeze-v2/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-mathpath/refs/heads/master/README.md

-->

# Probeleistungskontrolle für Physik – Klasse 12: Schwingungen und Wellen

> Stand: 05.11.2026

Diese Probeklausur enthält mehr Aufgaben als eine reguläre Klausur. Nutze sie, um unterschiedliche Aufgabenarten zu wiederholen und deinen Lösungsweg selbstständig zu kontrollieren.

> [!CAUTION]
> <h2>[Tutorial öffnen](https://liascript.github.io/course/?https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/Repetitorium/Erklaerungen/00_00_00_Tutorial.md)</h2>

Im Tutorial lernst du die Bedienung der Eingabefelder, Hinweise, Lösungen und Schreibflächen kennen. Kehre danach zu dieser Probeklausur zurück.

> [!IMPORTANT]
> Trage zu jeder physikalischen Größe die Einheit direkt in das Eingabefeld ein. Dezimalpunkt und Dezimalkomma werden akzeptiert. Winkel im Gradmaß benötigen das Gradzeichen.

Wische weiter oder nutze unten links den Pfeil neben der Seitenzahl.

## Schwingungen – Rechnungen

**Aufgabe 1**

Ein Federpendel mit der Masse $m=200\,\mathrm{g}$ und der Federkonstante $D=5\,\mathrm{N/m}$ schwingt mit der Amplitude $A=7\,\mathrm{cm}$. Die Anfangsphase beträgt $\varphi_0=90^\circ$.

__$a)\;\;$__ Berechne die Kreisfrequenz $\omega$. Runde auf zwei Nachkommastellen.

<!-- data-hint-button="1" data-solution-button="3" -->
$\omega\approx$ [[ 5.00 1/s ]] @canvas
@Algebrite.check2(`5/s`,`0.005/s`)
[[?]] Wandle die Masse zuerst in Kilogramm um und verwende $\omega=\sqrt{D/m}$.
[[?]] @Explain
******************
$$
\omega=\sqrt{\frac{D}{m}}
=\sqrt{\frac{5\,\mathrm{N/m}}{0{,}200\,\mathrm{kg}}}
=5{,}00\,\mathrm{s}^{-1}.
$$
******************

@resetter

@ADetails(`2=BE;Einheiten, Wurzeln`)

---

__$b)\;\;$__ Berechne die Elongation $y$ nach $t=0{,}30\,\mathrm{s}$. Runde auf zwei Nachkommastellen in Zentimetern.

<!-- data-hint-button="1" data-solution-button="3" -->
$y(0{,}30\,\mathrm{s})\approx$ [[ 0.50 cm ]] @canvas
@Algebrite.check2(`0.4951604117cm`,`0.005cm`)
[[?]] Setze in $y(t)=A\sin(\omega t+\varphi_0)$ ein und wandle $90^\circ$ in $\pi/2$ um.
[[?]] @Explain
******************
$$
\begin{align*}
y(0{,}30\,\mathrm{s})
&=7\,\mathrm{cm}\cdot
\sin\!\left(5\,\mathrm{s}^{-1}\cdot0{,}30\,\mathrm{s}+\frac{\pi}{2}\right)\\
&\approx0{,}50\,\mathrm{cm}.
\end{align*}
$$
******************

@resetter

@ADetails(`2=BE;Einheiten, Funktionen`)

**Aufgabe 2**

Eine Actionkamera der Masse $m=140\,\mathrm{g}$ schwingt nach

$$
y(t)=3{,}5\,\mathrm{cm}\cdot\sin\!\left(8\,\mathrm{s}^{-1}t+\frac{\pi}{3}\right).
$$

__$a)\;\;$__ Berechne die Federkonstante $D$. Runde auf zwei Nachkommastellen.

<!-- data-hint-button="1" data-solution-button="3" -->
$D\approx$ [[ 8.96 N/m ]] @canvas
@Algebrite.check2(`8.96N/m`,`0.005N/m`)
[[?]] Löse $\omega=\sqrt{D/m}$ nach $D$ auf.
[[?]] @Explain
******************
$$
D=m\omega^2
=0{,}140\,\mathrm{kg}\cdot(8\,\mathrm{s}^{-1})^2
=8{,}96\,\mathrm{N/m}.
$$
******************

@resetter

@ADetails(`2=BE;Einheiten, Potenzen`)

---

__$b)\;\;$__ Berechne die Elongation nach genau einer Periodendauer. Runde auf zwei Nachkommastellen in Zentimetern.

<!-- data-hint-button="1" data-solution-button="3" -->
$y(T)\approx$ [[ 3.03 cm ]] @canvas
@Algebrite.check2(`3.0310889132cm`,`0.005cm`)
[[?]] Nach einer Periodendauer hat sich die Phase um $2\pi$ vergrößert.
[[?]] @Explain
******************
$$
y(T)=3{,}5\,\mathrm{cm}\cdot
\sin\!\left(2\pi+\frac{\pi}{3}\right)
\approx3{,}03\,\mathrm{cm}.
$$
******************

@resetter

@ADetails(`2=BE;Einheiten, Funktionen`)

**Aufgabe 3**

Für ein Fadenpendel gilt

$$
y(t)=2{,}8\,\mathrm{cm}\cdot\sin\!\left(\pi\,\mathrm{s}^{-1}t+\frac{\pi}{6}\right),
\qquad g=9{,}81\,\mathrm{m/s^2}.
$$

__$a)\;\;$__ Berechne die Pendellänge $l$. Runde auf drei Nachkommastellen in Metern.

<!-- data-hint-button="1" data-solution-button="3" -->
$l\approx$ [[ 0.994 m ]] @canvas
@Algebrite.check2(`0.9939608115m`,`0.0005m`)
[[?]] Verwende $\omega=\sqrt{g/l}$ und löse nach $l$ auf.
[[?]] @Explain
******************
$$
l=\frac{g}{\omega^2}
=\frac{9{,}81\,\mathrm{m/s^2}}{(\pi\,\mathrm{s}^{-1})^2}
\approx0{,}994\,\mathrm{m}.
$$
******************

@resetter

@ADetails(`2=BE;Einheiten, Wurzeln`)

---

__$b)\;\;$__ Der Faden wird um $20\,\%$ verlängert. Berechne die neue Periodendauer $T_\mathrm{neu}$. Runde auf zwei Nachkommastellen.

<!-- data-hint-button="1" data-solution-button="3" -->
$T_\mathrm{neu}\approx$ [[ 2.19 s ]] @canvas
@Algebrite.check2(`2.1908902300s`,`0.005s`)
[[?]] Es gilt $l_\mathrm{neu}=1{,}2l$ und $T=2\pi\sqrt{l/g}$.
[[?]] @Explain
******************
Da $T$ proportional zu $\sqrt{l}$ ist und die ursprüngliche Periodendauer $2{,}00\,\mathrm{s}$ beträgt, gilt

$$
T_\mathrm{neu}=2{,}00\,\mathrm{s}\cdot\sqrt{1{,}2}
\approx2{,}19\,\mathrm{s}.
$$
******************

@resetter

@ADetails(`2=BE;Prozentrechnung, Wurzeln, Einheiten`)

**Aufgabe 4**

Eine Schaukel schwingt mit der Periodendauer $T=1{,}6\,\mathrm{s}$, der Amplitude $A=5\,\mathrm{cm}$ und der Anfangsphase $\varphi_0=-45^\circ$.

__$a)\;\;$__ Berechne die Kreisfrequenz $\omega$. Runde auf drei Nachkommastellen.

<!-- data-hint-button="1" data-solution-button="3" -->
$\omega\approx$ [[ 3.927 1/s ]] @canvas
@Algebrite.check2(`3.9269908170/s`,`0.0005/s`)
[[?]] Verwende $\omega=2\pi/T$.
[[?]] @Explain
******************
$$
\omega=\frac{2\pi}{T}
=\frac{2\pi}{1{,}6\,\mathrm{s}}
\approx3{,}927\,\mathrm{s}^{-1}.
$$
******************

@resetter

@ADetails(`2=BE;Einheiten, Verhältnisse`)

---

__$b)\;\;$__ Berechne die Elongation nach $t=0{,}50\,\mathrm{s}$. Runde auf zwei Nachkommastellen in Zentimetern.

<!-- data-hint-button="1" data-solution-button="3" -->
$y(0{,}50\,\mathrm{s})\approx$ [[ 4.62 cm ]] @canvas
@Algebrite.check2(`4.6193976626cm`,`0.005cm`)
[[?]] Setze $\varphi_0=-\pi/4$ in $y(t)=A\sin(\omega t+\varphi_0)$ ein.
[[?]] @Explain
******************
$$
y(0{,}50\,\mathrm{s})
=5\,\mathrm{cm}\cdot
\sin\!\left(3{,}92699\,\mathrm{s}^{-1}\cdot0{,}50\,\mathrm{s}-\frac{\pi}{4}\right)
\approx4{,}62\,\mathrm{cm}.
$$
******************

@resetter

@ADetails(`2=BE;Einheiten, Funktionen`)

## Wellen – Rechnungen

Für die folgenden Aufgaben gilt die Wellengleichung

$$
y(x,t)=A\sin\!\left(2\pi\left(\frac{t}{T}-\frac{x}{\lambda}\right)\right).
$$

**Aufgabe 1**

Eine Wasserwelle besitzt $T=0{,}80\,\mathrm{s}$, $A=3{,}6\,\mathrm{cm}$ und $\lambda=50\,\mathrm{cm}$.

Berechne die Elongation am Ort $x=15\,\mathrm{cm}$ zur Zeit $t=10\,\mathrm{s}$. Runde auf zwei Nachkommastellen in Zentimetern.

<!-- data-hint-button="1" data-solution-button="3" -->
$y(15\,\mathrm{cm},10\,\mathrm{s})\approx$ [[ 3.42 cm ]] @canvas
@Algebrite.check2(`3.4238034587cm`,`0.005cm`)
[[?]] Setze alle Längen in derselben Einheit ein.
[[?]] @Explain
******************
$$
y=3{,}6\,\mathrm{cm}\cdot
\sin\!\left(2\pi\left(\frac{10}{0{,}80}-\frac{15}{50}\right)\right)
\approx3{,}42\,\mathrm{cm}.
$$
******************

@resetter

@ADetails(`2=BE;Einheiten, Funktionen`)

---

---


**Aufgabe 2**

Eine Seilwelle besitzt $A=17\,\mathrm{mm}$ und $\lambda=35\,\mathrm{mm}$. Am Ort $x=9{,}0\,\mathrm{cm}$ wird zur Zeit $t=4{,}4\,\mathrm{s}$ die Elongation $y=10\,\mathrm{mm}$ gemessen. Für die zugehörige Phase $\phi$ gilt $0\leq\phi\leq\pi/2$.

Berechne die Periodendauer $T$. Runde auf drei Nachkommastellen.

<!-- data-hint-button="1" data-solution-button="3" -->
$T\approx$ [[ 1.647 s ]] @canvas
@Algebrite.check2(`1.6470042283s`,`0.0005s`)
[[?]] Bestimme zuerst $\phi=\arcsin(y/A)$ und löse $2\pi(t/T-x/\lambda)=\phi$ nach $T$ auf.
[[?]] @Explain
******************
Mit $\phi=\arcsin(10/17)$ folgt

$$
T=\frac{t}{x/\lambda+\phi/(2\pi)}
=\frac{4{,}4\,\mathrm{s}}{90/35+\arcsin(10/17)/(2\pi)}
\approx1{,}647\,\mathrm{s}.
$$
******************

@resetter

@ADetails(`3=BE;Äquivalenzumformung, Einheiten, Funktionen`)

**Aufgabe 3**

Eine Welle auf einem Slinky besitzt $A=17\,\mathrm{cm}$ und $T=1{,}1\,\mathrm{s}$. Am Ort $x=7{,}8\,\mathrm{cm}$ wird zur Zeit $t=4{,}4\,\mathrm{s}$ die Elongation $y=10\,\mathrm{cm}$ gemessen. Für die zugehörige Phase $\phi$ gilt $0\leq\phi\leq\pi/2$.

Berechne die Ausbreitungsgeschwindigkeit $c$. Runde auf vier Nachkommastellen in Metern pro Sekunde.

<!-- data-hint-button="1" data-solution-button="3" -->
$c\approx$ [[ 0.0182 m/s ]] @canvas
@Algebrite.check2(`0.0181822310m/s`,`0.00005m/s`)
[[?]] Bestimme zuerst die Wellenlänge aus der Wellengleichung und verwende danach $c=\lambda/T$.
[[?]] @Explain
******************
Aus $\phi=\arcsin(10/17)$ folgt

$$
\lambda=\frac{x}{t/T-\phi/(2\pi)}
\approx2{,}000\,\mathrm{cm}.
$$

Damit ist

$$
c=\frac{\lambda}{T}
\approx0{,}0182\,\mathrm{m/s}.
$$
******************

@resetter

@ADetails(`3=BE;Äquivalenzumformung, Einheiten, Funktionen`)

**Aufgabe 4**

Eine Wasserwelle besitzt $A=4{,}5\,\mathrm{cm}$, $T=0{,}50\,\mathrm{s}$ und $c=0{,}40\,\mathrm{m/s}$.

Berechne die Elongation am Ort $x=3{,}0\,\mathrm{cm}$ zur Zeit $t=1{,}0\,\mathrm{s}$. Runde auf zwei Nachkommastellen in Zentimetern.

<!-- data-hint-button="1" data-solution-button="3" -->
$y(3{,}0\,\mathrm{cm},1{,}0\,\mathrm{s})\approx$ [[ -3.64 cm ]] @canvas
@Algebrite.check2(`-3.6405764747cm`,`0.005cm`)
[[?]] Berechne zuerst $\lambda=cT$.
[[?]] @Explain
******************
Mit $\lambda=cT=0{,}20\,\mathrm{m}=20\,\mathrm{cm}$ folgt

$$
y=4{,}5\,\mathrm{cm}\cdot
\sin\!\left(2\pi\left(\frac{1{,}0}{0{,}50}-\frac{3{,}0}{20}\right)\right)
\approx-3{,}64\,\mathrm{cm}.
$$
******************

@resetter

@ADetails(`2=BE;Negative Zahlen, Einheiten, Funktionen`)

## Komplexe Aufgabe 1

Ein Wagen der Masse $m$ ist an einer horizontalen Feder befestigt. Reibung wird vernachlässigt. Die Feder wird um $s=2{,}8\,\mathrm{cm}$ zusammengedrückt; dabei ist die Spannenergie $E_\mathrm{sp}=0{,}15\,\mathrm{mJ}$ gespeichert.

Es gelten

$$
E_\mathrm{sp}=\frac12Ds^2,\qquad
\omega=\sqrt{\frac Dm},\qquad
T=\frac{2\pi}{\omega}.
$$

__$a)\;\;$__ Bestimme die Federkonstante $D$. Runde auf drei Nachkommastellen in Newton pro Meter.

<!-- data-hint-button="1" data-solution-button="3" -->
$D\approx$ [[ 0.383 N/m ]] @canvas
@Algebrite.check2(`0.3826530612N/m`,`0.0005N/m`)
[[?]] Rechne Zentimeter in Meter und Millijoule in Joule um. Stelle danach die Gleichung für die Spannenergie nach $D$ um.
[[?]] @Explain
******************
$$
\begin{align*}
D&=\frac{2E_\mathrm{sp}}{s^2}
=\frac{2\cdot0{,}00015\,\mathrm{J}}{(0{,}028\,\mathrm{m})^2}\\
&\approx0{,}383\,\mathrm{N/m}.
\end{align*}
$$
******************

@resetter

@ADetails(`2=BE;Einheiten, Äquivalenzumformung`)

---

__$b)\;\;$__ Für $m=0{,}180\,\mathrm{kg}$: Berechne die Kreisfrequenz $\omega$ auf drei Nachkommastellen und die Periodendauer $T$ auf zwei Nachkommastellen.

<!-- data-hint-button="1" data-solution-button="3" -->
$\omega\approx$ [[ 1.458 1/s ]] @canvas, $\quad T\approx$ [[ 4.31 s ]] @canvas
@Algebrite.check2(`[1.4580296088/s;4.3093674293s]`,`[0.0005/s;0.005s]`)
[[?]] Verwende möglichst den ungerundeten Wert der Federkonstante.
[[?]] @Explain
******************
$$
\begin{align*}
\omega&=\sqrt{\frac{0{,}382653\,\mathrm{N/m}}{0{,}180\,\mathrm{kg}}}
\approx1{,}458\,\mathrm{s}^{-1},\\
T&=\frac{2\pi}{\omega}\approx4{,}31\,\mathrm{s}.
\end{align*}
$$
******************

@resetter

@ADetails(`3=BE;Wurzeln, Einheiten`)

---

__$c)\;\;$__ Für denselben Wagen werden nun $A=2{,}8\,\mathrm{cm}$ und $\varphi_0=\pi/4$ betrachtet. Gib zuerst den dimensionslosen Faktor $x(t)/A$ an. Schreibe im Eingabefeld `w` für $\omega$.

<!-- data-hint-button="1" data-solution-button="3" -->
$\dfrac{x(t)}A=$ [[ sin(w*t+pi/4) ]] @canvas
@Algebrite.check(`sin(w*t+pi/4)`)
[[?]] Setze die Anfangsphase in $x(t)=A\sin(\omega t+\varphi_0)$ ein.
[[?]] @Explain
******************
$$
x(t)=A\sin\!\left(\omega t+\frac{\pi}{4}\right).
$$
******************

@resetter

@ADetails(`2=BE;Gleichung, Funktionen`)

Berechne anschließend die Auslenkung $x(0{,}50\,\mathrm{s})$. Runde auf zwei Nachkommastellen in Zentimetern.

<!-- data-hint-button="1" data-solution-button="3" -->
$x(0{,}50\,\mathrm{s})\approx$ [[ 2.80 cm ]] @canvas
@Algebrite.check2(`2.7955504625cm`,`0.005cm`)
[[?]] Setze $t=0{,}50\,\mathrm{s}$ ein. Der Sinus erwartet das Bogenmaß.
[[?]] @Explain
******************
$$
x(0{,}50\,\mathrm{s})
=2{,}8\,\mathrm{cm}\cdot
\sin\!\left(1{,}45803\,\mathrm{s}^{-1}\cdot0{,}50\,\mathrm{s}+\frac{\pi}{4}\right)
\approx2{,}80\,\mathrm{cm}.
$$
******************

@resetter

@ADetails(`2=BE;Einheiten, Funktionen`)

---

__$d)\;\;$__ Bestimme die maximale Geschwindigkeit $v_\mathrm{max}$ und die maximale Rückstellkraft $F_\mathrm{max}$. Runde beide Größen in SI-Einheiten auf vier Nachkommastellen.

<!-- data-hint-button="1" data-solution-button="3" -->
$v_\mathrm{max}\approx$ [[ 0.0408 m/s ]] @canvas, $\quad F_\mathrm{max}\approx$ [[ 0.0107 N ]] @canvas
@Algebrite.check2(`[0.0408248290m/s;0.0107142857N]`,`[0.00005m/s;0.00005N]`)
[[?]] Verwende $v_\mathrm{max}=A\omega$ und $F_\mathrm{max}=DA$.
[[?]] @Explain
******************
$$
\begin{align*}
v_\mathrm{max}&=A\omega
=0{,}028\,\mathrm{m}\cdot1{,}45803\,\mathrm{s}^{-1}
\approx0{,}0408\,\mathrm{m/s},\\
F_\mathrm{max}&=DA
=0{,}382653\,\mathrm{N/m}\cdot0{,}028\,\mathrm{m}
\approx0{,}0107\,\mathrm{N}.
\end{align*}
$$
******************

@resetter

@ADetails(`3=BE;Einheiten, Verhältnisse`)

## Idealer LC-Schwingkreis

Ein idealer LC-Schwingkreis besteht aus einer Spule mit $L=20\,\mathrm{mH}$ und einem Kondensator mit $C=4{,}7\,\mu\mathrm{F}$. Zu Beginn ist der Kondensator auf $U_0=5{,}0\,\mathrm{V}$ aufgeladen; es gilt $i(0)=0$.

$$
\omega=\frac1{\sqrt{LC}},\qquad
T=\frac{2\pi}{\omega},\qquad
u_C(t)=U_0\cos(\omega t),\qquad
i(t)=C\frac{du_C}{dt}.
$$

__$a)\;\;$__ Berechne $\omega$ auf ganze $\mathrm{s}^{-1}$ und $T$ auf drei Nachkommastellen in Millisekunden.

<!-- data-hint-button="1" data-solution-button="3" -->
$\omega\approx$ [[ 3262 1/s ]] @canvas, $\quad T\approx$ [[ 1.926 ms ]] @canvas
@Algebrite.check2(`[3261.6403652672/s;1.9263881371ms]`,`[0.5/s;0.0005ms]`)
[[?]] Wandle Millihenry und Mikrofarad in die SI-Einheiten um.
[[?]] @Explain
******************
$$
\begin{align*}
\omega&=\frac1{\sqrt{(20\cdot10^{-3}\,\mathrm{H})(4{,}7\cdot10^{-6}\,\mathrm{F})}}
\approx3262\,\mathrm{s}^{-1},\\
T&=2\pi\sqrt{LC}\approx1{,}926\,\mathrm{ms}.
\end{align*}
$$
******************

@resetter

@ADetails(`3=BE;Einheiten, Wurzeln`)

---

__$b)\;\;$__ Stelle $u_C(t)$ und $i(t)$ mit Zahlenwerten und Einheiten auf. Runde $\omega$ auf ganze $\mathrm{s}^{-1}$ und die Stromamplitude auf vier Nachkommastellen in Ampere.

<!-- data-hint-button="1" -->
[[!]]
<script>true</script>
******************
Da der Kondensator zu Beginn vollständig geladen ist, startet seine Spannung beim positiven Maximum. Deshalb wird die Spannung durch eine Kosinusfunktion beschrieben. Die Stromstärke folgt aus der zeitlichen Ableitung der Kondensatorspannung:

$$
\begin{aligned}
u_C(t)&\approx5{,}0\,\mathrm{V}\cos(3262\,\mathrm{s}^{-1}t),\\
i(t)&=-CU_0\omega\sin(\omega t)
\approx-0{,}0766\,\mathrm{A}\sin(3262\,\mathrm{s}^{-1}t).
\end{aligned}
$$

Das Minuszeichen zeigt, dass die Stromrichtung während der anfänglichen Entladung der festgelegten positiven Bezugsrichtung entgegengesetzt ist.
******************

@resetter

@ADetails(`4=BE;Gleichung, Funktionen`)

---

__$c)\;\;$__ Bestimme $u_C$ und $i$ zum Zeitpunkt $t=0{,}25\,\mathrm{ms}$. Runde die Spannung auf drei und die Stromstärke auf vier Nachkommastellen.

<!-- data-hint-button="1" data-solution-button="3" -->
$u_C\approx$ [[ 3.428 V ]] @canvas, $\quad i\approx$ [[ -0.0558 A ]] @canvas
@Algebrite.check2(`[3.4278495092V;-0.0558006650A]`,`[0.0005V;0.00005A]`)
[[?]] Es gilt $0{,}25\,\mathrm{ms}=0{,}00025\,\mathrm{s}$.
[[?]] @Explain
******************
$$
\begin{align*}
u_C&=5{,}0\,\mathrm{V}\cos(\omega t)\approx3{,}428\,\mathrm{V},\\
i&=-CU_0\omega\sin(\omega t)\approx-0{,}0558\,\mathrm{A}.
\end{align*}
$$
******************

@resetter

@ADetails(`3=BE;Negative Zahlen, Einheiten, Funktionen`)

---

__$d)\;\;$__ Interpretiere das Vorzeichen des Stroms aus Teilaufgabe c). Warum ist $i$ negativ, obwohl $u_C$ noch positiv ist? Begründe mit $i=C\,du_C/dt$ in ganzen Sätzen.

<!-- data-hint-button="1" -->
[[!]]
<script>true</script>
******************
Die Kondensatorspannung ist noch positiv, nimmt aber ab. Daher gilt $du_C/dt<0$ und wegen $i=C\,du_C/dt$ auch $i<0$. Das Vorzeichen beschreibt eine Stromrichtung entgegen der gewählten positiven Richtung. Dabei wird elektrische Feldenergie des Kondensators in magnetische Feldenergie der Spule umgewandelt; im idealen Schwingkreis bleibt die Gesamtenergie erhalten.
******************

@resetter

@ADetails(`2=BE;Negative Zahlen, Energieumwandlung`)

## Komplexe Aufgabe 2

Eine mechanische Welle breitet sich entlang einer Schnur in positiver Ortsrichtung aus:

$$
y(x,t)=A\sin\!\left(2\pi\left(\frac tT-\frac x\lambda\right)\right).
$$

__$a)\;\;$__ Gegeben sind $A=1{,}5\,\mathrm{cm}$, $T=0{,}75\,\mathrm{s}$ und $\lambda=36\,\mathrm{cm}$. Bestimme $y$ an der Stelle $x=5{,}0\,\mathrm{cm}$ zur Zeit $t=2{,}4\,\mathrm{s}$. Runde auf drei Nachkommastellen in Zentimetern.

<!-- data-hint-button="1" data-solution-button="3" -->
$y(5{,}0\,\mathrm{cm},2{,}4\,\mathrm{s})\approx$ [[ 0.562 cm ]] @canvas
@Algebrite.check2(`0.5619098901cm`,`0.0005cm`)
[[?]] Berechne zuerst $t/T-x/\lambda$.
[[?]] @Explain
******************
$$
\begin{align*}
y&=1{,}5\,\mathrm{cm}\cdot
\sin\!\left(2\pi\left(\frac{2{,}4}{0{,}75}-\frac{5{,}0}{36}\right)\right)\\
&\approx0{,}562\,\mathrm{cm}.
\end{align*}
$$
******************

@resetter

@ADetails(`3=BE;Einheiten, Funktionen`)

---

__$b)\;\;$__ Eine andere Welle besitzt $A=6{,}0\,\mathrm{mm}$ und $\lambda=10{,}0\,\mathrm{mm}$. Nach $t=3{,}5\,\mathrm{s}$ wird bei $x=4{,}0\,\mathrm{cm}$ die Elongation $y=5{,}2\,\mathrm{mm}$ gemessen. Die Phase liegt zwischen $0$ und $\pi/2$. Bestimme $T$ auf drei Nachkommastellen.

<!-- data-hint-button="1" data-solution-button="3" -->
$T\approx$ [[ 0.840 s ]] @canvas
@Algebrite.check2(`0.8399588055s`,`0.0005s`)
[[?]] Verwende wegen des vorgegebenen Phasenintervalls den Hauptwert von $\arcsin(y/A)$.
[[?]] @Explain
******************
$$
T=\frac{t}{x/\lambda+\arcsin(y/A)/(2\pi)}
=\frac{3{,}5\,\mathrm{s}}{40/10+\arcsin(5{,}2/6{,}0)/(2\pi)}
\approx0{,}840\,\mathrm{s}.
$$

Ohne die Phasenbedingung wären wegen der Periodizität des Sinus mehrere Lösungen möglich.
******************

@resetter

@ADetails(`3=BE;Äquivalenzumformung, Einheiten, Funktionen`)

---

__$c)\;\;$__ Eine Welle besitzt $A=12{,}0\,\mathrm{cm}$ und $T=1{,}20\,\mathrm{s}$. Zur Zeit $t=3{,}0\,\mathrm{s}$ wird bei $x=8{,}0\,\mathrm{cm}$ die Elongation $y=4{,}5\,\mathrm{cm}$ gemessen. Die Phase liegt zwischen $0$ und $\pi/2$. Bestimme $\lambda$ und $c$. Runde sinnvoll.

<!-- data-hint-button="1" data-solution-button="3" -->
$\lambda\approx$ [[ 3.28 cm ]] @canvas, $\quad c\approx$ [[ 0.0273 m/s ]] @canvas
@Algebrite.check2(`[3.2802730669cm;0.0273356089m/s]`,`[0.005cm;0.00005m/s]`)
[[?]] Stelle zuerst nach $x/\lambda$ um. Verwende für $c=\lambda/T$ die Wellenlänge in Metern.
[[?]] @Explain
******************
$$
\lambda=
\frac{x}{t/T-\arcsin(y/A)/(2\pi)}
\approx3{,}28\,\mathrm{cm}.
$$

Damit gilt

$$
c=\frac{\lambda}{T}
\approx\frac{0{,}0328\,\mathrm{m}}{1{,}20\,\mathrm{s}}
\approx0{,}0273\,\mathrm{m/s}.
$$
******************

@resetter

@ADetails(`4=BE;Äquivalenzumformung, Einheiten, Verhältnisse`)

---

__$d)\;\;$__ Erkläre, warum in a) der Betrag der momentanen Auslenkung kleiner als die Amplitude ist. Erläutere außerdem die physikalische Bedeutung von $\lambda$ und $T$ und begründe $c=\lambda/T$ mit den Ergebnissen aus c).

<!-- data-hint-button="1" -->
[[!]]
<script>true</script>
******************
Die Amplitude ist der größte mögliche Betrag der Auslenkung. In a) ist der Sinuswert etwa $0{,}3746$, daher gilt $y\approx1{,}5\,\mathrm{cm}\cdot0{,}3746\approx0{,}562\,\mathrm{cm}$.

Die Wellenlänge ist die räumliche Periode, beispielsweise der Abstand benachbarter Wellenberge. Die Periodendauer ist die Zeit für eine vollständige Schwingung an einem festen Ort. In dieser Zeit wandert die Wellenform eine Wellenlänge weiter. Daher gilt $c=\lambda/T\approx0{,}0273\,\mathrm{m/s}$.
******************

@resetter

@ADetails(`3=BE;Verhältnisse, Funktionen`)

## Brechung von Wasserwellen

Eine Wasserwelle läuft aus einem Bereich 1 in einen Bereich 2 mit anderer Wassertiefe. Es gilt

$$
\frac{\sin(\alpha_1)}{\sin(\alpha_2)}=\frac{v_1}{v_2}.
$$

Die Winkel werden gegen das Lot auf die Grenzlinie gemessen.

__$a)\;\;$__ Gegeben sind $\alpha_1=30^\circ$, $v_1=2{,}40\,\mathrm{m/s}$ und $v_2=1{,}60\,\mathrm{m/s}$. Bestimme $\alpha_2$ auf zwei Nachkommastellen.

<!-- data-hint-button="1" data-solution-button="3" -->
$\alpha_2\approx$ [[ 19.47° ]] @canvas
<script>
const raw = window.normalizeInputToArray(String('@input'))[0] ?? '';
const normalized = raw
  .replace(/\\(?:mathrm|text)\{(deg|°)\}/g, '$1')
  .replace(/\^\{\\circ\}|\^\\circ|\\circ/g, '°')
  .trim();
const angle = normalized.match(/^([+-]?(?:\d+(?:[.,]\d*)?|[.,]\d+))\s*(?:°|deg)$/i);
angle !== null && Math.abs(Number(angle[1].replace(',', '.')) - 19.4712206345) <= 0.005;
</script>
[[?]] Stelle nach $\sin(\alpha_2)$ um und verwende den Arkussinus im Gradmaß.
[[?]] @Explain
******************
$$
\alpha_2=
\arcsin\!\left(\sin(30^\circ)\frac{1{,}60}{2{,}40}\right)
\approx19{,}47^\circ.
$$
******************

@resetter

@ADetails(`2=BE;Verhältnisse, Einheiten`)

---

__$b)\;\;$__ Gegeben sind $v_1=3{,}00\,\mathrm{m/s}$, $\alpha_1=40^\circ$ und $\alpha_2=25^\circ$. Berechne $v_2$ auf zwei Nachkommastellen.

<!-- data-hint-button="1" data-solution-button="3" -->
$v_2\approx$ [[ 1.97 m/s ]] @canvas
@Algebrite.check2(`1.9724525683m/s`,`0.005m/s`)
[[?]] Es gilt $v_2=v_1\sin(\alpha_2)/\sin(\alpha_1)$.
[[?]] @Explain
******************
$$
v_2=3{,}00\,\mathrm{m/s}\cdot
\frac{\sin(25^\circ)}{\sin(40^\circ)}
\approx1{,}97\,\mathrm{m/s}.
$$
******************

@resetter

@ADetails(`2=BE;Verhältnisse, Einheiten`)

---

__$c)\;\;$__ Leite aus dem Brechungsgesetz eine allgemeine Gleichung für $\alpha_2$ her. Zeige die Umformungsschritte. Es gelten $v_1,v_2>0$ und $0^\circ\leq\alpha_1,\alpha_2\leq90^\circ$.

<!-- data-hint-button="1" -->
[[!]]
<script>true</script>
******************
Zuerst wird der Sinus des Brechungswinkels isoliert. Da die betrachteten Winkel zwischen $0^\circ$ und $90^\circ$ liegen, kann anschließend der Hauptwert des Arkussinus verwendet werden:

$$
\begin{align*}
\frac{\sin(\alpha_1)}{\sin(\alpha_2)}&=\frac{v_1}{v_2}\\
\sin(\alpha_2)&=\sin(\alpha_1)\frac{v_2}{v_1}\\
\alpha_2&=\arcsin\!\left(\sin(\alpha_1)\frac{v_2}{v_1}\right).
\end{align*}
$$

Damit lässt sich der Brechungswinkel aus dem Einfallswinkel und dem Verhältnis der beiden Wellengeschwindigkeiten bestimmen.
******************

@resetter

@ADetails(`3=BE;Äquivalenzumformung, Verhältnisse`)

---

__$d)\;\;$__ Bei einem weiteren Übergang werden $\alpha_1=35^\circ$ und $\alpha_2=50^\circ$ gemessen. Ist $v_2$ größer oder kleiner als $v_1$? Begründe mit dem Brechungsgesetz in ganzen Sätzen.

<!-- data-hint-button="1" -->
[[!]]
<script>true</script>
******************
Zwischen $0^\circ$ und $90^\circ$ wächst der Sinus mit dem Winkel. Daher gilt

$$
\frac{v_1}{v_2}
=\frac{\sin(35^\circ)}{\sin(50^\circ)}
\approx0{,}749<1.
$$

Somit ist $v_2>v_1$: Die Welle breitet sich nach dem Übergang schneller aus.
******************

@resetter

@ADetails(`2=BE;Verhältnisse, Funktionen`)

## Übungen an Graphen

Die beiden Kurven zeigen dieselbe Welle zu den Zeitpunkten $t_1=0\,\mathrm{s}$ und $t_2=4\,\mathrm{s}$. Die zweite Kurve ist gegenüber der ersten in positiver Ortsrichtung verschoben.

@Koordinatensystem(`xmin=0;xmax=8;ymin=-3;ymax=3;width=700;id=wellenbilder;statisch=1;achsen=1;grid=1;border=0`)
@AchsenBeschriftung(`id=wellenbilder;xlabel=$x\,\mathrm{in}\,\mathrm{m}$;ylabel=$y\,\mathrm{in}\,\mathrm{m}$`)
@PlotFunktion(`wellenbilder;kurve1=0;2.5*sin(2.64555170828614167*x);#1565c0;linestyle=solid`)
@PlotFunktion(`wellenbilder;kurve2=0;2.5*sin(2.64555170828614167*x-2);#d32f2f;linestyle=dashed`)

**Blau:** $t_1=0\,\mathrm{s}$  **Rot gestrichelt:** $t_2=4\,\mathrm{s}$

__$a)\;\;$__ Bestimme die Amplitude $A$ und die Wellenlänge $\lambda$ aus dem Diagramm. Runde $\lambda$ auf drei Nachkommastellen.

<!-- data-hint-button="1" data-solution-button="3" -->
$A=$ [[ 2.50 m ]] @canvas, $\quad\lambda\approx$ [[ 2.375 m ]] @canvas
@Algebrite.check2(`[2.5m;2.375m]`,`[0.005m;0.0005m]`)
[[?]] Die Amplitude ist der größte Betrag der Auslenkung. Die Wellenlänge ist der Abstand zweier benachbarter Wellenberge.
[[?]] @Explain
******************
Aus dem Ordinatenwert der Wellenberge folgt $A=2{,}50\,\mathrm{m}$. Der Abstand benachbarter Wellenberge beträgt

$$
\lambda=\frac{2\pi}{2{,}6455517083\,\mathrm{m}^{-1}}
=2{,}375\,\mathrm{m}.
$$
******************

@resetter

@ADetails(`3=BE;Einheiten, Verhältnisse`)

---

__$b)\;\;$__ Verwende die kleinste positive Verschiebung zwischen den Kurven. Bestimme die Verschiebung $\Delta x$, die Ausbreitungsgeschwindigkeit $c$ und die Periodendauer $T$. Runde sinnvoll.

<!-- data-hint-button="1" data-solution-button="3" -->
$\Delta x\approx$ [[ 0.756 m ]] @canvas, $\quad c\approx$ [[ 0.189 m/s ]] @canvas, $\quad T\approx$ [[ 12.566 s ]] @canvas
@Algebrite.check2(`[0.7559859797m;0.1889964949m/s;12.5663706144s]`,`[0.0005m;0.0005m/s;0.0005s]`)
[[?]] Die Phasenverschiebung beträgt $2$ rad. Es gilt $\Delta x=\Delta\varphi/k$, danach $c=\Delta x/\Delta t$ und $T=\lambda/c$.
[[?]] @Explain
******************
$$
\begin{align*}
\Delta x&=\frac{2}{2{,}6455517083\,\mathrm{m}^{-1}}
\approx0{,}756\,\mathrm{m},\\
c&=\frac{\Delta x}{4\,\mathrm{s}}
\approx0{,}189\,\mathrm{m/s},\\
T&=\frac{\lambda}{c}
\approx12{,}566\,\mathrm{s}.
\end{align*}
$$
******************

@resetter

@ADetails(`5=BE;Einheiten, Verhältnisse`)

## Übungen an Graphen

Das Diagramm zeigt die Schwingung

$$
y(t)=2{,}5\,\mathrm{m}\cdot e^{-t/(4\,\mathrm{s})}\cos(12\,\mathrm{s}^{-1}t).
$$

@Koordinatensystem(`xmin=0;xmax=6;ymin=-3;ymax=3;width=700;id=daempfung;statisch=1;achsen=1;grid=1;border=0`)
@AchsenBeschriftung(`id=daempfung;xlabel=$t\,\mathrm{in}\,\mathrm{s}$;ylabel=$y\,\mathrm{in}\,\mathrm{m}$`)
@PlotFunktion(`daempfung;schwingung=0;2.5*exp(-x/4)*cos(12*x);#6a1b9a;linestyle=solid`)
@PlotFunktion(`daempfung;huelle_oben=0;2.5*exp(-x/4);#757575;linestyle=dashed`)
@PlotFunktion(`daempfung;huelle_unten=0;-2.5*exp(-x/4);#757575;linestyle=dashed`)

**Violett:** $y(t)$  **Grau gestrichelt:** $+A(t)$ und $-A(t)$

Beschreibe den Verlauf und erkläre, woran eine gedämpfte Schwingung erkennbar ist. Gehe auch auf die Einhüllende und die Energieübertragung ein.

<!-- data-hint-button="1" -->
[[!]]
<script>true</script>
******************
Der Kosinus verursacht den regelmäßigen Vorzeichenwechsel der Auslenkung. Der Faktor $e^{-t/(4\,\mathrm{s})}$ verkleinert den größten möglichen Betrag fortlaufend. Die Einhüllenden

$$
A(t)=\pm2{,}5\,\mathrm{m}\,e^{-t/(4\,\mathrm{s})}
$$

nähern sich mit der Zeit der Nulllinie. Daran ist die Dämpfung erkennbar. Durch Reibung oder andere dissipative Wechselwirkungen wird Schwingungsenergie an die Umgebung übertragen; deshalb nimmt die Amplitude ab.
******************

@resetter

@ADetails(`4=BE;Funktionen, Negative Zahlen`)
