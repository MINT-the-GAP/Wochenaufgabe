<!--
version:  0.0.1

language: de

@style
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

-->

# Probeleistungskontrolle für Physik - Klasse 12: Wellenoptik

<br>

Swipe (Wische) entweder weiter oder klicke unten links auf neben der Seitenzahl auf den Pfeil nach rechts.

<br>

Diese Probearbeit hat mehr Aufgaben als die richtige Arbeit, damit du genug zum Üben hast. Es sind viele verschiedene Aufgabentypen abgebildet, sodass du alles nochmal bei der Bearbeitung dieser Aufgaben wiederholst.

<br>





## Aufgabe 1

Eine Wasserwelle läuft aus einem Bereich 1 (tieferes Wasser) in einen Bereich 2 (flacheres Wasser).  
Die Ausbreitungsgeschwindigkeit der Welle ändert sich dabei von $v_1$ zu $v_2$.  
Für den Übergang gilt das Snellius’sche Brechungsgesetz für Wellen:

$$
\frac{\sin(\alpha_1)}{\sin(\alpha_2)} \;=\; \frac{v_1}{v_2}
$$

Dabei ist  
- $\alpha_1$ der Einfallswinkel (gemessen gegen das Lot auf die Grenzlinie),  
- $\alpha_2$ der Brechungswinkel nach dem Übergang,  
- $v_1$ die Wellengeschwindigkeit vor dem Übergang,  
- $v_2$ die Wellengeschwindigkeit nach dem Übergang.

Gib Winkel in Grad mit 2 Dezimalstellen an.  

---

---

__$a)\;\;$__ Die Welle trifft mit dem Einfallswinkel $\alpha_1 = 30^\circ$ auf die Grenzschicht.  
Die Geschwindigkeiten sind $v_1 = 2{,}40\,\text{m/s}$ in Bereich 1 und $v_2 = 1{,}60\,\text{m/s}$ in Bereich 2.

Bestimme den Brechungswinkel $\alpha_2$.

$ \alpha_2 \approx $ [[ 19,47        ]]$^\circ$
******************
$$
\begin{align*}
\frac{\sin(\alpha_1)}{\sin(\alpha_2)} &= \frac{v_1}{v_2} \\
\Rightarrow \sin(\alpha_2)
&= \sin(\alpha_1) \cdot \frac{v_2}{v_1} \\[6pt]
\sin(\alpha_1) &= \sin(30^\circ) = 0{,}5 \\
\frac{v_2}{v_1} &= \frac{1{,}60}{2{,}40} = 0{,}666\ldots \\
\sin(\alpha_2) &= 0{,}5 \cdot 0{,}666\ldots = 0{,}333\ldots \\[6pt]
\alpha_2 &= \arcsin(0{,}333\ldots) \approx 19{,}47^\circ
\end{align*}
$$
******************


---

---


__$b)\;\;$__ Eine Wasserwelle läuft nun aus Bereich 1 in Bereich 2 mit  
$v_1 = 3\,\dfrac{\text{m}}{\text{s}}$.  
Die gemessenen Winkel sind $\alpha_1 = 40^\circ$ und $\alpha_2 = 25^\circ$.

Berechne die Wellengeschwindigkeit $v_2$ im Bereich 2.

$ v_2 \approx $ [[ 1,97       ]]$\,\dfrac{\text{m}}{\text{s}}$
******************
$$
\begin{align*}
\frac{\sin(\alpha_1)}{\sin(\alpha_2)} &= \frac{v_1}{v_2} \\
\Rightarrow v_2 &= v_1 \cdot \frac{\sin(\alpha_2)}{\sin(\alpha_1)} \\[8pt]
\sin(40^\circ) &\approx 0{,}6428 \\
\sin(25^\circ) &\approx 0{,}4226 \\[6pt]
v_2 &= 3{,}00\,\dfrac{\text{m}}{\text{s}} \cdot \frac{0{,}4226}{0{,}6428} \\
    &\approx 1{,}97\,\dfrac{\text{m}}{\text{s}}
\end{align*}
$$
******************


---

---



__$c)\;\;$__ Leite eine allgemeine Gleichung für $\alpha_2$ her.  



[[!]]
<script>true</script>
******************
$$
\begin{align*}
\frac{\sin(\alpha_1)}{\sin(\alpha_2)} &= \frac{v_1}{v_2} \\[6pt]
\Rightarrow \sin(\alpha_2)
&= \sin(\alpha_1)\,\frac{v_2}{v_1} \\[6pt]
\Rightarrow \alpha_2
&= \arcsin \!\left(
\sin(\alpha_1)\,\frac{v_2}{v_1}
\right)
\end{align*}
$$
******************




---

---






__$d)\;\;$__ Es wird eine Wasserwelle beobachtet, die von Bereich 1 nach Bereich 2 übergeht.  
Es wurde gemessen: $\alpha_1 = 35^\circ$ und $\alpha_2 = 50^\circ$.  
Ist $v_2$ größer oder kleiner als $v_1$? Begründe mit dem Brechungsgesetz.



[[!]]
<script>true</script>
******************
$$
\begin{align*}
\frac{\sin(\alpha_1)}{\sin(\alpha_2)} &= \frac{v_1}{v_2} \\
\text{Wenn } \alpha_2 > \alpha_1,\; \sin(\alpha_2) > \sin(\alpha_1). \\
\Rightarrow \frac{\sin(\alpha_1)}{\sin(\alpha_2)} < 1. \\
\Rightarrow \frac{v_1}{v_2} < 1. \\
\Rightarrow v_2 > v_1.
\end{align*}
$$
******************














## Aufgabe 2






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



<br>
<br>
<br>


---

---



__$a)\;\;$__ Bestimme die Federkonstante $D$ aus der gespeicherten Spannenergie.

$ D \approx $ [[ 0,383        ]] $\,\dfrac{\text{N}}{\text{m}}$
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

$ \omega \approx $ [[ 1,458        ]]  $\dfrac{1}{\text{s}}$ \
$ T \approx $ [[ 4,31       ]] $\,\text{s}$
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


$ x(0.50\,\text{s}) \approx $ [[ 2,80        ]] cm
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
















## Aufgabe 3





Es wird ein verlustfreien LC-Schwingkreis aus einer Spule mit Induktivität $L$ und einem Kondensator mit Kapazität $C$ betrachtet.

Zu Beginn ($t = 0$) ist der Kondensator vollständig aufgeladen mit der Spannung $U_0$. Es fließt zum Zeitpunkt $t=0$ noch kein Strom ($i(0)=0$).

Für einen idealen LC-Schwingkreis gilt:  \
- Kreisfrequenz: $\omega = \dfrac{1}{\sqrt{L \, C}}$  \
- Periodendauer: $T = \dfrac{2\pi}{\omega}$  \
- Kondensatorspannung: $u_C(t) = U_0 \cos(\omega t)$  \
- Stromstärke im Kreis: $i(t) = C \, \dfrac{du_C}{dt} = -C \, U_0 \, \omega \, \sin(\omega t)$  \


<br>

Gegeben:   \
- $L = 20 \,\text{mH} = 20 \cdot 10^{-3}\,\text{H}$   \
- $C = 4{,}7 \,\mu\text{F} = 4{,}7 \cdot 10^{-6}\,\text{F}$   \
- $U_0 = 5{,}0 \,\text{V}$   \

<br>
<br>
<br>


---

---

__$a)\;\;$__ Berechne die Kreisfrequenz $\omega$ und die Periodendauer $T$ (auf drei Nachkommastellen) der Schwingung.

$ \omega \approx $ [[ 3260        ]] $\,\dfrac{1}{\text{s}}$ \
$ T \approx $ [[ 0,002        ]] s
******************
$$
\begin{align*}
\omega &= \frac{1}{\sqrt{L C}}
= \frac{1}{\sqrt{(20 \cdot 10^{-3}\,\text{H}) \cdot (4{,}7 \cdot 10^{-6}\,\text{F})}} \\
&\approx 3{,}26 \cdot 10^{3} \,\text{s}^{-1} \\[10pt]
T &= \frac{2\pi}{\omega}
= \frac{2\pi}{3{,}26 \cdot 10^{3}\,\text{s}^{-1}} \\
&\approx 1{,}93 \cdot 10^{-3}\,\text{s}
= 1{,}93 \,\text{ms}
\end{align*}
$$
******************


---

---



__$b)\;\;$__ Stelle die zeitabhängige Spannung $u_C(t)$ am Kondensator und den zeitabhängigen Strom $i(t)$ im Schwingkreis auf.

Gib beide Funktionen explizit an.



[[!]]
<script>true</script>
******************
$$
\begin{align*}
u_C(t) &= U_0 \cos(\omega t)
= 5{,}0\,\text{V} \cdot \cos\!\big(3{,}26 \cdot 10^{3} \, t\big) \\[8pt]
i(t) &= - C \, U_0 \, \omega \, \sin(\omega t) \\
&= - (4{,}7 \cdot 10^{-6}\,\text{F}) \cdot (5{,}0\,\text{V}) \cdot
(3{,}26 \cdot 10^{3}\,\text{s}^{-1}) \cdot \sin\!\big(3{,}26 \cdot 10^{3} \, t\big) \\
&\approx -7{,}66 \cdot 10^{-2}\,\text{A} \cdot \sin\!\big(3{,}26 \cdot 10^{3} \, t\big) \\
&\approx -0{,}0766\,\text{A} \cdot \sin\!\big(3{,}26 \cdot 10^{3} \, t\big)
\end{align*}
$$
******************



---

---


__$c)\;\;$__ Bestimme die momentane Kondensatorspannung $u_C(t)$ und die momentane Stromstärke $i(t)$ zum Zeitpunkt $t = 0{,}25 \,\text{ms}$.


$ u_C(0,25\text{ ms}) \approx $ [[ 3,430        ]] V \
$ i(0,25\text{ ms}) \approx $ [[ -0.056        ]] A
******************
$$
\begin{align*}
t &= 0{,}25 \,\text{ms}
= 0{,}00025 \,\text{s} \\[6pt]
\omega t &= (3{,}26 \cdot 10^{3}\,\text{s}^{-1}) \cdot (0{,}00025\,\text{s})
\approx 0{,}815 \,\text{rad} \\[10pt]
u_C(t) &= 5{,}0\,\text{V} \cdot \cos(0{,}815)
\approx 3{,}43\,\text{V} \\[10pt]
i(t) &= -0{,}0766\,\text{A} \cdot \sin(0{,}815)
\approx -0{,}0558\,\text{A} \\
&\approx -5{,}58 \cdot 10^{-2}\,\text{A}
\end{align*}
$$
******************

---

---



__$d)\;\;$__ Interpretiere das Vorzeichen des Stroms aus Teilaufgabe $c)$.

Warum ist $i(0{,}25\,\text{ms})$ negativ, obwohl $u_C(0{,}25\,\text{ms})$ noch positiv ist?


[[!]]
<script>true</script>
******************
$$
u_C(t) > 0 \;\Rightarrow\; Kondensator hat noch Ladung \\
i(t) < 0 \;\Rightarrow\; Ladung fließt gerade ab \text{ (Entladung)} \\
\Rightarrow\; Energie wandert von C über die Spule ins Magnetfeld der Spule.
$$
******************











## Aufgabe 4




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

$ T \approx $ [[ 0,840        ]] s
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

$ \lambda \approx $ [[ 3,28        ]] cm

$ c \approx $ [[ 0,0273        ]] $\,\dfrac{\text{m}}{\text{s}}$
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


[[!]]
<script>true</script>
******************
Amplitude $A$: größter möglicher Betrag der Auslenkung. \
Momentane Elongation $y$: aktueller Wert zu diesem Ort und Zeitpunkt. \
$\lambda$: räumliche Periode der Welle, 
$T$: zeitliche Periode der Welle. \
$\Rightarrow c = \frac{\lambda}{T}$ bedeutet: pro Schwingungsdauer T läuft die Wellenform eine Wellenlänge weiter.
******************










