<!--

version:  0.0.1
language: de
author: Martin Lommatzsch

@style
main > *:not(:last-child) {
  margin-bottom: 3rem;
}
@end

import: https://raw.githubusercontent.com/liaTemplates/algebrite/master/README.md
        https://raw.githubusercontent.com/liaTemplates/JSXGraph/main/README.md


import: https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/main/README.md

-->

# Probeleistungskontrolle für Physik - Klasse 10: Wellen


> Letzte Aktualisierung am 07.02. gegen 20:00 Uhr


> <h2> WICHTIGER HINWEIS: Ich teste auch neue Funktionen mit dieser Datei, sollte etwas seltsames angezeigt werden oder gar nicht zu sehen sein, bitte einfach die Datei aktualisieren. Ich versuche die auftretenden Bugs der neuen Features nach und nach zu beseitigen. <br> <p align="right"> -Lommatzsch </p> </h2>


Swipe (Wische) entweder weiter oder klicke unten links auf neben der Seitenzahl auf den Pfeil nach rechts.



Diese Probearbeit hat mehr Aufgaben als die richtige Arbeit, damit du genug zum Üben hast. Es sind viele verschiedene Aufgabentypen abgebildet, sodass du alles nochmal bei der Bearbeitung dieser Aufgaben wiederholst.

Oben links in der Kopfzeile dieses LiaScript-Kurses findest du einen Textmarker.

Bei den Aufgaben ist auch immer ein Stiftbutton eingeblendet, klicke auf diesen Button und erhalte eine Schreibfläche.















## Aufgabe 1






Ein Wagen der Masse $m$ ist an einer horizontalen Feder befestigt (reibungslos).  
Die Feder wird um $s = 2{,}8 \,\text{cm}$ zusammengedrückt und gespeichert ist dabei eine Spannenergie von $E_\text{sp} = 0{,}15 \,\text{mJ}$.  
Anschließend wird losgelassen und der Wagen führt eine harmonische Schwingung aus.

Hinweise und Gleichungen: \

- $E_\text{sp} = \dfrac{1}{2} D s^2$ \

- $\omega = \sqrt{\dfrac{D}{m}}$ \

- $T = \dfrac{2\pi}{\omega}$ \

- $x(t) = A \sin(\omega t + \varphi_0)$ \

- $v_\text{max} = A \cdot \omega$ \

- $F_\text{Feder,max} = D \cdot A$ \





---

---



__$a)\;\;$__ Bestimme die Federkonstante $D$ aus der gespeicherten Spannenergie.

@canvas

$ D \approx $ [[ 0,383        ]] $\,\dfrac{\text{N}}{\text{m}}$
@Algebrite.check2(0.383,0.01)
******************
$$
\begin{align*}
E_\text{sp} &= \frac{1}{2} D s^2 \\
\Rightarrow D &= \frac{2 E_\text{sp}}{s^2} \\[6pt]
s &= 0{,}028 \,\text{m} \quad,\quad
E_\text{sp} = 0{,}00015 \,\text{J} \\[6pt]
D &= \frac{2 \cdot 0{,}00015 \,\text{J}}{(0{,}028 \,\text{m})^2} \\
  &= \frac{0{,}00030}{0{,}000784} \,\frac{\text{J}}{\text{m}^2} \\
  &\approx 0{,}383 \,\dfrac{\text{N}}{\text{m}}
\end{align*}
$$
******************


---

---



__$b)\;\;$__ Berechne die Kreisfrequenz $\omega$ und die Periodendauer $T$ der Schwingung für die angehängte Masse $m = 0{,}180 \,\text{kg}$.

@canvas

$ \omega \approx $ [[ 1,458        ]]  $\dfrac{1}{\text{s}}$ \
@Algebrite.check2(1.458,0.01)
$ T \approx $ [[ 4,309       ]] $\,\text{s}$
@Algebrite.check2(4.309,0.01)
******************
$$
\begin{align*}
\omega &= \sqrt{\frac{D}{m}}
= \sqrt{\frac{0{,}383 \,\text{N/m}}{0{,}180 \,\text{kg}}} \\[6pt]
&\approx \sqrt{2{,}1278 \,\text{s}^{-2}}
\approx 1{,}458 \,\text{s}^{-1} \\[10pt]
T &= \frac{2\pi}{\omega}
= \frac{2\pi}{1{,}458 \,\text{s}^{-1}}
\approx 4{,}309 \,\text{s}
\approx 4{,}31 \,\text{s}
\end{align*}
$$
******************


---

---



__$c)\;\;$__ Die Schwingung startet NICHT im Extrempunkt, sondern mit einer Phasenverschiebung  
$\varphi_0 = \dfrac{\pi}{4}$. Die Amplitude sei $A = 2{,}8 \,\text{cm}$.

1. Gib die vollständige Schwingungsgleichung $x(t)$ an.  
2. Berechne daraus die momentane Auslenkung $x(0{,}50 \,\text{s})$ in Zentimeter.

@canvas


$ x(0.50\,\text{s}) \approx $ [[ 2,796        ]] cm
@Algebrite.check2(2.796,0.01)
******************
$$
\begin{align*}
x(t) &= A \sin(\omega t + \varphi_0) \\[4pt]
A &= 0{,}028 \,\text{m}, \quad
\omega \approx 1{,}458 \,\text{s}^{-1}, \quad
\varphi_0 = \frac{\pi}{4} \\[6pt]
\Rightarrow x(t)
&= 0{,}028 \,\text{m} \cdot
\sin \!\big( 1{,}458\, t + \frac{\pi}{4} \big) \\[10pt]
x(0{,}50 \,\text{s})
&= 0{,}028 \,\text{m} \cdot
\sin \!\big( 1{,}458 \cdot 0{,}50 + \frac{\pi}{4} \big) \\
&\approx 0{,}02796 \,\text{m} \\
&\approx 2{,}80 \,\text{cm}
\end{align*}
$$
******************


---

---


__$d)\;\;$__ Bestimme zwei charakteristische Größen dieser Schwingung:

1. die maximale Geschwindigkeit $v_\text{max}$,  
2. die maximale Rückstellkraft $F_\text{Feder,max}$ der Feder auf vier Nachkommastellen genau.

@canvas

$ v_\text{max} \approx $ [[ 0,0408        ]]  $\,\dfrac{\text{m}}{\text{s}}$ \
$ F_\text{Feder,max} \approx $ [[ 0,0107        ]] N
******************
$$
\begin{align*}
v_\text{max} &= A \cdot \omega \\
&= 0{,}028 \,\text{m} \cdot 1{,}458 \,\text{s}^{-1} \\
&\approx 0{,}0408 \,\text{m/s} \\[12pt]
F_\text{Feder,max} &= D \cdot A \\
&= 0{,}383 \,\text{N/m} \cdot 0{,}028 \,\text{m} \\
&\approx 0{,}0107 \,\text{N}
\end{align*}
$$
******************






















## Aufgabe 2




Eine mechanische Welle breitet sich entlang einer Schnur in $+x$-Richtung aus.  
Für ihre Auslenkung gilt:

$$
y(x;t) \;=\; A \,\sin\!\left(
2\pi \left[
\frac{t}{T} \;-\; \frac{x}{\lambda}
\right]
\right)
$$

mit  

- $A$: Amplitude (maximale Auslenkung),  \

- $T$: Periodendauer,  \

- $\lambda$: Wellenlänge,  \

- $y(x;t)$: momentane Elongation der Schnur an der Stelle $x$ zur Zeit $t$.\

Runde sinnvoll (3 signifikante Stellen).


---

---

__$a)\;\;$__ Eine Welle wird beschrieben durch  
Amplitude $A = 1{,}5 \,\text{cm}$,  
Periodendauer $T = 0{,}75 \,\text{s}$,  
Wellenlänge $\lambda = 36 \,\text{cm}$.

Bestimme die momentane Auslenkung $y(x;t)$ an der Stelle $x = 5{,}0 \,\text{cm}$ zum Zeitpunkt $t = 2{,}4 \,\text{s}$.

@canvas

$ y(5{,}0\text{ cm};\,2{,}4\text{ s}) \approx $ [[ 0,562        ]] cm
******************
$$
\begin{align*}
y(x;t) &= A \sin\!\left(
2\pi\left[
\frac{t}{T} - \frac{x}{\lambda}
\right]\right) \\[8pt]
A &= 1{,}5 \,\text{cm}, \quad
T = 0{,}75 \,\text{s}, \quad
\lambda = 36 \,\text{cm}, \\
t &= 2{,}4 \,\text{s}, \quad
x = 5{,}0 \,\text{cm} \\[8pt]
\Rightarrow y(5{,}0\text{ cm};2{,}4\text{ s})
&= 1{,}5\,\text{cm} \cdot
\sin\!\left(
2\pi \left[
\frac{2{,}4}{0{,}75} - \frac{5{,}0}{36}
\right]\right) \approx 3{,}0611 \\[4pt]
2\pi \cdot 3{,}0611 &\approx 19{,}223 \\[4pt]
\sin(19{,}223) &\approx 0{,}3746 \\[4pt]
\Rightarrow y \approx 1{,}5\,\text{cm} \cdot 0{,}3746
\approx 0{,}562 \,\text{cm}
\end{align*}
$$
******************




---

---





__$b)\;\;$__ Eine andere Welle hat Amplitude $A = 6{,}0 \,\text{mm}$ und Wellenlänge $\lambda = 10{,}0 \,\text{mm}$.  
Nach einer Zeit $t = 3{,}5 \,\text{s}$ misst man an der Stelle $x = 4{,}0 \,\text{cm}$ eine Elongation von $y = 5{,}2 \,\text{mm}$.

Bestimme daraus die Periodendauer $T$ der Welle.


@canvas

$ T \approx $ [[ 0,840        ]] s
@Algebrite.check2(0.840,0.01)
******************
$$
\begin{align*}
y(x;t) &= A \sin\!\left(
2\pi\left[
\frac{t}{T} - \frac{x}{\lambda}
\right]\right) \\[8pt]
\Rightarrow
\frac{y(x;t)}{A}
&= \sin\!\left(
2\pi\left[
\frac{t}{T} - \frac{x}{\lambda}
\right]\right) \\[6pt]
\arcsin\!\left(\frac{y}{A}\right)
&= 2\pi \left[
\frac{t}{T} - \frac{x}{\lambda}
\right] \\[10pt]
\Rightarrow
\frac{t}{T}
&=
\frac{1}{2\pi}\arcsin\!\left(\frac{y}{A}\right)
+ \frac{x}{\lambda} \\[10pt]
\Rightarrow
T
&= \frac{t}{
\frac{1}{2\pi}\arcsin\!\left(\frac{y}{A}\right)
+ \frac{x}{\lambda}
}
\end{align*}
$$

Jetzt Zahlen einsetzen (achte auf gleiche Einheiten!):
- $A = 6{,}0 \,\text{mm}$  
- $y = 5{,}2 \,\text{mm}$  
- $\lambda = 10{,}0 \,\text{mm}$  
- $x = 4{,}0 \,\text{cm} = 40{,}0 \,\text{mm}$  
- $t = 3{,}5 \,\text{s}$

$$
\frac{y}{A} = \frac{5{,}2}{6{,}0} \approx 0{,}8667,
\quad
\arcsin(0{,}8667) \approx 1{,}0485 \,\text{rad}
$$

$$
\frac{1}{2\pi}\arcsin\!\left(\frac{y}{A}\right)
\approx
\frac{1{,}0485}{2\pi}
\approx 0{,}1669
$$

$$
\frac{x}{\lambda}
=
\frac{40{,}0\,\text{mm}}{10{,}0\,\text{mm}}
= 4{,}000
$$

$$
\Rightarrow
\frac{t}{T}
=
0{,}1669 + 4{,}000
= 4{,}1669
\quad\Rightarrow\quad
T
= \frac{3{,}5\,\text{s}}{4{,}1669}
\approx 0{,}840 \,\text{s}
$$
******************




---

---






__$c)\;\;$__ Eine Welle hat Amplitude $A = 12{,}0 \,\text{cm}$.  
Zum Zeitpunkt $t = 3{,}0 \,\text{s}$ beobachtet man an der Stelle $x = 8{,}0 \,\text{cm}$ eine Auslenkung $y = 4{,}5 \,\text{cm}$.  
Die Periodendauer beträgt $T = 1{,}20 \,\text{s}$.

1. Bestimme aus diesen Angaben die Wellenlänge $\lambda$.  
2. Berechne daraus die Ausbreitungsgeschwindigkeit $c$ der Welle.


@canvas

$ \lambda \approx $ [[ 3,28        ]] cm


@canvas

$ c \approx $ [[ 0,0273        ]] $\,\dfrac{\text{m}}{\text{s}}$
@Algebrite.check2(0.0273,0.01)
******************
$$
\begin{align*}
y(x;t) &= A \sin\!\left(
2\pi\left[
\frac{t}{T} - \frac{x}{\lambda}
\right]\right) \\[8pt]
\frac{y}{A}
&= \sin\!\left(
2\pi \left[
\frac{t}{T} - \frac{x}{\lambda}
\right]\right) \\[8pt]
\arcsin\!\left(\frac{y}{A}\right)
&= 2\pi \left[
\frac{t}{T} - \frac{x}{\lambda}
\right] \\[10pt]
\frac{1}{2\pi}\arcsin\!\left(\frac{y}{A}\right)
&= \frac{t}{T} - \frac{x}{\lambda}
\end{align*}
$$

Nach $\lambda$ umstellen:
$$
\frac{x}{\lambda}
= \frac{t}{T} - \frac{1}{2\pi}\arcsin\!\left(\frac{y}{A}\right)
\quad\Rightarrow\quad
\lambda
= \frac{x}{
\frac{t}{T} -
\frac{1}{2\pi}\arcsin\!\left(\frac{y}{A}\right)
}
$$

Zahlen einsetzen:  \
- $A = 12{,}0 \,\text{cm}$  \
- $y = 4{,}5 \,\text{cm}$  \
- $x = 8{,}0 \,\text{cm}$  \
- $t = 3{,}0 \,\text{s}$  \
- $T = 1{,}20 \,\text{s}$  \

$$
\frac{y}{A} = \frac{4{,}5}{12{,}0} = 0{,}375
\quad\Rightarrow\quad
\arcsin(0{,}375) \approx 0{,}3844 \,\text{rad}
$$

$$
\frac{1}{2\pi} \cdot 0{,}3844
\approx 0{,}06118
\quad,\quad
\frac{t}{T} = \frac{3{,}0}{1{,}20} = 2{,}50
$$

$$
\frac{x}{\lambda}
= 2{,}50 - 0{,}06118
= 2{,}43882
\quad\Rightarrow\quad
\lambda
= \frac{8{,}0 \,\text{cm}}{2{,}43882}
\approx 3{,}28 \,\text{cm}
$$

Die Ausbreitungsgeschwindigkeit $c$ ist
$$
c = \frac{\lambda}{T}
= \frac{3{,}28 \,\text{cm}}{1{,}20 \,\text{s}}
\approx 2{,}73 \,\frac{\text{cm}}{\text{s}}
= 2{,}73 \cdot 10^{-2} \,\frac{\text{m}}{\text{s}}
$$
******************



---

---





__$d)\;\;$__ Physikalische Einordnung (Antwort in Worten, aber begründe mit Zahlen aus a)–c)):

- In Teilaufgabe a) hattest du $A = 1{,}5\,\text{cm}$, aber die berechnete momentane Auslenkung war nur $0{,}562\,\text{cm}$.  
  Warum ist $y$ kleiner als $A$?  
- In Teilaufgabe c) hast du gesehen, dass aus $\lambda$ und $T$ direkt die Ausbreitungsgeschwindigkeit $c$ folgt.  
  Erkläre in einem Satz, was $\lambda$ und $T$ physikalisch jeweils bedeuten und warum $c = \dfrac{\lambda}{T}$ sinnvoll ist.

@canvas

[[!]]
<script>true</script>
******************
Amplitude $A$: größter möglicher Betrag der Auslenkung. \
Momentane Elongation $y$: aktueller Wert zu diesem Ort und Zeitpunkt. \
$\lambda$: räumliche Periode der Welle, 
$T$: zeitliche Periode der Welle. \
$\Rightarrow c = \frac{\lambda}{T}$ bedeutet: pro Schwingungsdauer T läuft die Wellenform eine Wellenlänge weiter.
******************










