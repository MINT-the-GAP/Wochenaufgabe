<!--
version:  0.0.1
language: de

import: https://cdn.jsdelivr.net/gh/LiaTemplates/JSXGraph@main/README.md
import: https://cdn.jsdelivr.net/gh/LiaTemplates/algebrite@master/README.md


import: https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/main/imports/TafelREADME.md
import: https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/main/imports/MarkerREADME.md
import: https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/main/imports/FlexChildREADME.md
import: https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/main/imports/DeutschREADME.md
import: https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/main/imports/NavigationREADME.md
import: https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/main/imports/TimerREADME.md
import: https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/main/imports/OCRREADME.md



-->

# Probeleistungskontrolle für Physik - Klasse 8: Druck




> Letztes Update am 17.04.2026 gegen 10:00 Uhr



Swipe (Wische) entweder weiter oder klicke unten links auf neben der Seitenzahl auf den Pfeil nach rechts.



Diese Probearbeit hat mehr Aufgaben als die richtige Arbeit, damit du genug zum Üben hast. Es sind viele verschiedene Aufgabentypen abgebildet, sodass du alles nochmal bei der Bearbeitung dieser Aufgaben wiederholst.

## Druck im allgemeinen


Aufgabe 1: Ein Kleinwagen mit einer Masse von $1680\,\text{kg}$ soll einen Reifendruck von $2{,}1\,\text{bar}$ haben. **Berechne** die Auflagefläche eines einzelnen Reifens. Nimm an, dass das Auto auf vier Reifen gleichmäßig belastet ist.

<!-- data-solution-timer="240s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
[[   0.0196   ]] $\text{m}^2$ @canvas
@Algebrite.check2(0.0196,0.001)
**********************
$$
\begin{align*}
p &= 2{,}1\,\text{bar} = 210000\,\text{Pa} \\
A &= \frac{F}{p} = \frac{mg}{p} \\
A &= \frac{1680\,\text{kg} \cdot 9{,}81\,\frac{\text{N}}{\text{kg}}}{210000\,\frac{\text{N}}{\text{m}^2}} \\
A &= 0{,}07848\,\text{m}^2 \\
A_1 &= \frac{A}{4} = \frac{0{,}07848\,\text{m}^2}{4} \\
A_1 &= 0{,}01962\,\text{m}^2 \approx 0{,}0196\,\text{m}^2
\end{align*}
$$
**********************




Aufgabe 2: Auf eine rechteckige Bodenplatte mit der Fläche $A=2{,}5\,\text{m}^2$ wirkt ein Druck von $p=0{,}024\,\text{bar}$. **Berechne** die Masse, die auf der Bodenplatte steht. Runde auf ganze Kilogramm.

<!-- data-solution-timer="240s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
[[   612   ]] kg @canvas
@Algebrite.check(612)
**********************
$$
\begin{align*}
p &= 0{,}024\,\text{bar} = 2400\,\text{Pa} \\
p &= \frac{F}{A} = \frac{mg}{A} \\
m &= \frac{pA}{g} \\
m &= \frac{2400\,\frac{\text{N}}{\text{m}^2} \cdot 2{,}5\,\text{m}^2}{9{,}81\,\frac{\text{N}}{\text{kg}}} \\
m &= \frac{6000\,\text{N}}{9{,}81\,\frac{\text{N}}{\text{kg}}} \\
m &\approx 611{,}62\,\text{kg} \approx 612\,\text{kg}
\end{align*}
$$
**********************




Aufgabe 3: Ein Quader aus Aluminium $\left(\rho = 2{,}7\,\frac{\text{g}}{\text{cm}^3}\right)$ hat die Kantenlängen $a=8\,\text{cm}$, $b=5\,\text{cm}$ und $c=3\,\text{cm}$. Beim Aufstellen wird ein Auflagedruck von $1324{,}35\,\text{Pa}$ gemessen. **Berechne** die Auflagefläche.

<!-- data-solution-timer="300s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
[[   24   ]] $\text{cm}^2$ @canvas
@Algebrite.check(24)
**********************
$$
\begin{align*}
V &= a \cdot b \cdot c = 8\,\text{cm} \cdot 5\,\text{cm} \cdot 3\,\text{cm} = 120\,\text{cm}^3 \\
m &= \rho \cdot V = 2{,}7\,\frac{\text{g}}{\text{cm}^3} \cdot 120\,\text{cm}^3 = 324\,\text{g} = 0{,}324\,\text{kg} \\
F &= mg = 0{,}324\,\text{kg} \cdot 9{,}81\,\frac{\text{N}}{\text{kg}} = 3{,}17844\,\text{N} \\
p &= \frac{F}{A} \\
A &= \frac{F}{p} = \frac{3{,}17844\,\text{N}}{1324{,}35\,\frac{\text{N}}{\text{m}^2}} \\
A &= 0{,}0024\,\text{m}^2 \\
A &= 24\,\text{cm}^2
\end{align*}
$$

Die Seitenflächen des Quaders sind:
$$
\begin{align*}
a \cdot b &= 8\,\text{cm} \cdot 5\,\text{cm} = 40\,\text{cm}^2 \\
a \cdot c &= 8\,\text{cm} \cdot 3\,\text{cm} = 24\,\text{cm}^2 \\
b \cdot c &= 5\,\text{cm} \cdot 3\,\text{cm} = 15\,\text{cm}^2
\end{align*}
$$

Also liegt der Quader auf der Seitenfläche $8\,\text{cm} \times 3\,\text{cm}$.
**********************




## Schweredruck


Aufgabe 1: In einem Süßwasserbecken soll der hydrostatische Druck $p=1{,}8\,\text{bar}$ betragen. Berechne die Tauchtiefe. Verwende $\rho_{\text{Wasser}}=1000\,\dfrac{\text{kg}}{\text{m}^3}$.

<!-- data-solution-timer="240s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
[[   18.3486   ]] m @canvas
@Algebrite.check2(18.3486,0.01)
**********************
$$
\begin{align*}
p &= 1{,}8\,\text{bar} = 180000\,\text{Pa} \\
p &= \rho g h \\
h &= \frac{p}{\rho g} \\
h &= \frac{180000\,\text{Pa}}{1000\,\frac{\text{kg}}{\text{m}^3} \cdot 9{,}81\,\frac{\text{N}}{\text{kg}}} \\
h &\approx 18{,}3486\,\text{m}
\end{align*}
$$
**********************



Aufgabe 2: Berechne die Tauchtiefe in Glycerin mit der Dichte $\rho_{\text{Glycerin}}=1260\,\dfrac{\text{kg}}{\text{m}^3}$, bei der ein hydrostatischer Druck von $p=2{,}5\,\text{bar}$ erreicht wird.

<!-- data-solution-timer="240s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
[[   20.2256   ]] m @canvas
@Algebrite.check2(20.2256,0.01)
**********************
$$
\begin{align*}
p &= 2{,}5\,\text{bar} = 250000\,\text{Pa} \\
p &= \rho g h \\
h &= \frac{p}{\rho g} \\
h &= \frac{250000\,\text{Pa}}{1260\,\frac{\text{kg}}{\text{m}^3} \cdot 9{,}81\,\frac{\text{N}}{\text{kg}}} \\
h &\approx 20{,}2256\,\text{m}
\end{align*}
$$
**********************




Aufgabe 3: Zeige, dass die Umrechnung zwischen Zentimeter-Wassersäule und Pascal korrekt ist. Berechne dazu zunächst den Druck einer Wassersäule von $35\,\text{cm}$ und leite daraus den Druck für $1\,\text{cm}$ Wassersäule ab. Verwende $\rho_{\text{Wasser}}=1000\,\dfrac{\text{kg}}{\text{m}^3}$. 

<!-- data-solution-timer="300s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
[[   98.1   ]] Pa @canvas
@Algebrite.check2(98.1,0.1)
**********************
$$
\begin{align*}
h &= 35\,\text{cm} = 0{,}35\,\text{m} \\
p &= \rho g h \\
p &= 1000\,\frac{\text{kg}}{\text{m}^3} \cdot 9{,}81\,\frac{\text{N}}{\text{kg}} \cdot 0{,}35\,\text{m} \\
p &= 3433{,}5\,\text{Pa}
\end{align*}
$$

$$
\begin{align*}
35\,\text{cm Wassersäule} &\widehat{=} 3433{,}5\,\text{Pa} \\
1\,\text{cm Wassersäule} &\widehat{=} \frac{3433{,}5\,\text{Pa}}{35} \\
1\,\text{cm Wassersäule} &\widehat{=} 98{,}1\,\text{Pa}
\end{align*}
$$
**********************




## Auftrieb



Aufgabe 1: Ein vollständig eingetauchter Kupferwürfel mit der Kantenlänge $2{,}4\,\text{cm}$ befindet sich in Meerwasser mit der Dichte $\rho = 1030\,\dfrac{\text{kg}}{\text{m}^3}$. 

<!-- data-solution-timer="240s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
[[   0.1397   ]] N @canvas
@Algebrite.check2(0.1397,0.01)
**********************
$$
\begin{align*}
a &= 2{,}4\,\text{cm} = 0{,}024\,\text{m} \\
V &= a^3 = \left(0{,}024\,\text{m}\right)^3 = 0{,}000013824\,\text{m}^3 \\
F_A &= \rho \cdot g \cdot V \\
F_A &= 1030\,\frac{\text{kg}}{\text{m}^3} \cdot 9{,}81\,\frac{\text{N}}{\text{kg}} \cdot 0{,}000013824\,\text{m}^3 \\
F_A &\approx 0{,}1397\,\text{N}
\end{align*}
$$
**********************





Aufgabe 2: Ein vollständig eingetauchter Körper mit dem Volumen $V=3{,}5\,\text{dm}^3$ erfährt in einer Flüssigkeit eine Auftriebskraft von $35{,}1934\,\text{N}$. Berechne die Dichte der Flüssigkeit. Runde auf ganze $\dfrac{\text{kg}}{\text{m}^3}$.

<!-- data-solution-timer="240s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
[[   1025   ]] $\dfrac{\text{kg}}{\text{m}^3}$ @canvas
@Algebrite.check(1025)
**********************
$$
\begin{align*}
V &= 3{,}5\,\text{dm}^3 = 0{,}0035\,\text{m}^3 \\
F_A &= \rho \cdot g \cdot V \\
\rho &= \frac{F_A}{g \cdot V} \\
\rho &= \frac{35{,}1934\,\text{N}}{9{,}81\,\frac{\text{N}}{\text{kg}} \cdot 0{,}0035\,\text{m}^3} \\
\rho &\approx 1025\,\frac{\text{kg}}{\text{m}^3}
\end{align*}
$$

Das passt näherungsweise zu Meerwasser.
**********************


\vspace{2em}


Aufgabe 3: Die gemessene Auftriebskraft eines unförmigen Körpers beträgt in Ethanol $0{,}4\,\text{N}$. Berechne die Kantenlänge eines Würfels, der in Ethanol dieselbe Auftriebskraft erfahren würde. Verwende $\rho_{\text{Ethanol}}=789\,\dfrac{\text{kg}}{\text{m}^3}$.

<!-- data-solution-timer="300s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
[[   3,7248   ]] cm @canvas
@Algebrite.check2(3.7248,0.01)
**********************
$$
\begin{align*}
F_A &= \rho \cdot g \cdot V \\
V &= \frac{F_A}{\rho \cdot g} \\
V &= \frac{0{,}4\,\text{N}}{789\,\frac{\text{kg}}{\text{m}^3} \cdot 9{,}81\,\frac{\text{N}}{\text{kg}}} \\
V &\approx 0{,}000051679\,\text{m}^3
\end{align*}
$$

Für den Würfel gilt:
$$
\begin{align*}
V &= a^3 \\
a &= \sqrt[3]{V} = \sqrt[3]{0{,}000051679\,\text{m}^3} \\
a &\approx 0{,}037248\,\text{m} = 3{,}7248\,\text{cm}
\end{align*}
$$
**********************

