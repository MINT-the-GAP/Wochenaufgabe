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

# Probeleistungskontrolle für Physik - Klasse 11: Mechanik

<br>

Swipe (Wische) entweder weiter oder klicke unten links auf neben der Seitenzahl auf den Pfeil nach rechts.

<br>

Diese Probearbeit hat mehr Aufgaben als die richtige Arbeit, damit du genug zum Üben hast. Es sind viele verschiedene Aufgabentypen abgebildet, sodass du alles nochmal bei der Bearbeitung dieser Aufgaben wiederholst.

<br>





## Aufgabe 1



__$a)\;\;$__ Ein Pferd zieht einen Karren mit einer Masse von $75\,$kg einen Anstieg von $8\%$ mit konstanter Geschwindigkeit hinauf. Dabei wirkt eine Rollreibungskraft von $45\,$N auf den Karren.  
Berechne die aufgebrachte Zugkraft des Pferdes.  


$F_\text{Zug}=$[[  103,86  ]]N
@Algebrite.check(75*9.81*0.08 + 45)
************
$$
\begin{align*}
\text{Gegeben:}\quad 
m &= 75\,\text{kg}, \quad F_R = 45\,\text{N}, \quad \text{Steigung} = 8\% \\[4pt]
\tan\alpha &= 0{,}08 \;\;\Rightarrow\;\;\alpha \approx 4,574^\circ \\[6pt]
F_{G,\parallel} &= m \cdot g \cdot \sin\alpha 
\approx 75\,\text{kg} \cdot 9{,}81\,\frac{\text{m}}{\text{s}^2} \cdot 0{,}08 \\[4pt]
&\approx 58{,}86\,\text{N} \\[6pt]
\text{Konstante Geschwindigkeit:}\quad
0 &= F_\text{Zug} - F_R - F_{G,\parallel} \\[4pt]
F_\text{Zug} &= F_R + F_{G,\parallel} \\[4pt]
&= 45\,\text{N} + 58{,}86\,\text{N} \\[4pt]
&\approx 103{,}86\,\text{N} \approx 1{,}0\cdot 10^2\,\text{N}
\end{align*}
$$
************


---

---




__$b)\;\;$__ Eine Person schiebt einen Einkaufwagen mit einer Masse von $50\,$kg eine Rampe mit einer Steigung von $10\%$ hinauf. Der Wagen bewegt sich mit konstanter Geschwindigkeit. Die Rollreibungskraft beträgt $30\,$N.  
Berechne die aufgebrachte Schubkraft der Person.  


$F_\text{Schub}=$[[  79,05  ]]N
@Algebrite.check(50*9.81*0.10 + 30)
************
$$
\begin{align*}
\text{Gegeben:}\quad 
m &= 50\,\text{kg}, \quad F_R = 30\,\text{N}, \quad \text{Steigung} = 10\% \\[4pt]
\tan\alpha &= 0{,}10 \;\;\Rightarrow\;\;\alpha \approx 5,711^\circ \\[6pt]
F_{G,\parallel} &= m \cdot g \cdot \sin\alpha 
\approx 50\,\text{kg} \cdot 9{,}81\,\frac{\text{m}}{\text{s}^2} \cdot 0{,}10 \\[4pt]
&\approx 49{,}05\,\text{N} \\[6pt]
\text{Konstante Geschwindigkeit:}\quad
0 &= F_\text{Schub} - F_R - F_{G,\parallel} \\[4pt]
F_\text{Schub} &= F_R + F_{G,\parallel} \\[4pt]
&= 30\,\text{N} + 49{,}05\,\text{N} \\[4pt]
&\approx 79{,}05\,\text{N}
\end{align*}
$$
************








## Aufgabe 2


__$a)\;\;$__  
Eine Person steht auf einem Skateboard (Masse Person + Skateboard zusammen $80\,$kg) und hält einen schweren Rucksack mit der Masse $15\,$kg in den Händen. Die Person wirft den Rucksack kräftig nach vorne weg.  

**Begründe** mithilfe der Newtonschen Axiome, warum und in welche Richtung sich die Person auf dem Skateboard bewegt. Erkläre dabei insbesondere, welche Kräfte auftreten und warum sich das System so verhält.


[[!]]
<script>true</script>
******************

Zunächst betrachten wir das System „Person + Skateboard + Rucksack“:

1. **Vor dem Wurf**  
   - Alle stehen (noch) relativ zum Boden still.  
   - Die Gesamtimpuls des Systems ist Null.  
   - Nach dem I. Newton'schen Axiom (Trägheitsprinzip) bleibt der Zustand erhalten, solange keine äußere Kraft wirkt, die den Gesamtimpuls ändert.

2. **Beim Wegwerfen des Rucksacks**  
   - Die Person übt auf den Rucksack eine Kraft $F$ nach vorne aus.  
   - Nach **Newtons III. Axiom (Actio = Reactio)** wirkt gleichzeitig eine gleich große, entgegengesetzt gerichtete Kraft $-F$ auf die Person.  
   - Diese Kraft beschleunigt die Person (mit Skateboard) nach hinten.

3. **Bewegungsrichtung**  
   - Der Rucksack erhält einen Impuls nach vorne.  
   - Nach **Impulserhaltung** (Folge aus dem II. und III. Newton'schen Axiom bei fehlenden äußeren Kräften) muss der Gesamtimpuls des Systems weiterhin Null bleiben.  
   - Daher bekommt die Person einen gleich großen Impuls in entgegengesetzter Richtung: Sie bewegt sich **nach hinten**.

3. **Bezug zu II. Newton'schen Axiom**  
   - Für die Person gilt: $\vec{F} = m \cdot \vec{a}$.  
   - Die Reaktionskraft des Rucksacks ist die resultierende Kraft auf die Person.  
   - Da die Masse der Person größer ist als die des Rucksacks, ist ihre Beschleunigung zwar kleiner, aber sie wird deutlich merklich zurückrollen.

**Kurzfassung:**  
Durch den Wurf des Rucksacks nach vorne wirkt nach III. Newton'schen Axiom eine gleich große Gegenkraft auf die Person. Da keine horizontalen äußeren Kräfte auf das Gesamtsystem wirken, bleibt der Gesamtimpuls erhalten: Der Rucksack erhält Impuls nach vorne, die Person (mit Skateboard) Impuls nach hinten und rollt daher rückwärts.

******************


---

---



__$b)\;\;$__  
Ein Auto fährt mit konstanter Geschwindigkeit auf einer geraden Landstraße. Der Fahrer lässt plötzlich das Lenkrad los. Kurz darauf fährt das Auto nach rechts von der Fahrbahn, weil der rechte Vorderreifen deutlich weniger Luftdruck hat als der linke.  

**Begründe** mithilfe der Newton'schen Axiome, warum sich das Auto trotz „Loslassen des Lenkrads“ von der Geraden weg bewegt. Gehe insbesondere auf wirkenden Kräfte an den Rädern ein.

[[!]]
<script>true</script>
************

1. **Idealfall ohne Störungen (I. Newton'schen Axiom)**  
   - Nach dem I. Newton'schen Axiom (Trägheitsprinzip) würde sich ein Körper ohne resultierende Kraft geradlinig und gleichförmig weiterbewegen.  
   - Wenn auf das Auto keine seitlich wirkenden Kräfte wirken würden, bliebe es auf einer geraden Bahn, auch wenn der Fahrer das Lenkrad loslässt.

2. **Reale Situation: Unterschiedlicher Reifendruck**  
   - Der rechte Vorderreifen hat deutlich weniger Luftdruck.  
   - Dadurch verformt sich der Reifen stärker und rollt schlechter.  
   - Es wirken am rechten Reifen größere Rollwiderstände und Reibkräfte als am linken Vorderreifen.

3. **Warum reicht „Loslassen des Lenkrads“ nicht, um die Gerade zu halten?**  
   - Das Loslassen des Lenkrads entfernt nur den aktiven Eingriff des Fahrers, ändert aber nichts an den physikalischen Kräften am Fahrzeug.  
   - Da die Kräfte an den Rädern nicht symmetrisch sind, wirkt eine seitliche resultierende Kraft bzw. ein Drehmoment.  
   - Nach Newton I würde das Auto nur dann geradeaus weiterfahren, wenn die seitlichen Kräfte sich gegenseitig aufheben – das tun sie hier aber nicht.

**Kurzfassung:**  
Nach dem I. Newton'schen Axiom würde das Auto ohne resultierende Kraft geradeaus fahren. Durch den unterschiedlich aufgepumpten Reifen entstehen jedoch ungleiche Reib- und Rollwiderstandskräfte an den Rädern. Diese erzeugen eine seitliche resultierende Kraft bzw. ein Drehmoment, sodass das Auto nach II. Newton'schen Axiom seine Geschwindigkeit in Richtung und Betrag ändert und nach rechts von der Fahrbahn abgelenkt wird – unabhängig davon, ob die Fahrerin/der Fahrer das Lenkrad festhält oder loslässt.
************









## Aufgabe 3


__$a)\;\;$__  **Bestimme** die Stärke der resultierenden Kraft und gib diese auf drei Nachkommastellen gerundet an.


<center>
<!-- style="width:400px" -->
![](Superp1.png)
</center>


$F_\text{Res}\approx$[[  2,236  ]]N
@Algebrite.check(2.236)
************

<center>
<!-- style="width:400px" -->
![](Superp1L.png)
</center>


************

---

---



__$b)\;\;$__  **Bestimme** die Stärke der resultierenden Kraft und gib diese auf drei Nachkommastellen gerundet an.


<center>
<!-- style="width:400px" -->
![](Superp2.png)
</center>


$F_\text{Res}\approx$[[  5,000  ]]N
@Algebrite.check(5.000)
************

<center>
<!-- style="width:400px" -->
![](Superp2L.png)
</center>


************

---

---



__$c)\;\;$__  **Bestimme** die Stärke der resultierenden Kraft und gib diese auf drei Nachkommastellen gerundet an.


<center>
<!-- style="width:400px" -->
![](Superp3.png)
</center>


$F_\text{Res}\approx$[[  4,123  ]]N
@Algebrite.check(4.123)
************

<center>
<!-- style="width:400px" -->
![](Superp3L.png)
</center>


************




## Aufgabe 4


Eine Industriewaschmaschine schleudert Wäsche in einem runden Trommelbehälter. Der Radius der Trommel beträgt $0{,}30\,$m. Im Schleudergang dreht sich die Trommel mit $900$ Umdrehungen pro Minute. In der Trommel befindet sich unter anderem ein nasses Handtuch mit der Masse $0{,}40\,$kg. 

$a)\;\;$ **Bestimme** zunächst die Umlauffrequenz $f$ in $\text{Hz}$. 

<!-- data-solution-button="5"-->
$f=$ [[  15  ]] Hz
@Algebrite.check([15])
******************
$$
\begin{align*}
\text{Gegeben:}\quad n &= 900~\frac{\text{Umdrehungen}}{\text{min}}, \quad r = 0{,}30~\text{m} \\[4pt]
\text{Zuerst in Hz (Umdrehungen pro Sekunde):}\quad
f &= \frac{n}{60} = \frac{900}{60} = 15~\text{Hz} \\[6pt]
\end{align*}
$$
******************


$b)\;\;$ **Berechne** die Bahngeschwindigkeit $v$ des Handtuchs am Trommelrand. 
Gib die Geschwindigkeit gerundet auf drei Nachkommastellen in $\dfrac{\text{m}}{\text{s}}$ an. 


<!-- data-solution-button="5"-->
$v\approx$ [[  28,274  ]] $\dfrac{\text{m}}{\text{s}}$
@Algebrite.check(28.274)
******************
$$
\begin{align*}
v &= \omega \cdot r = 30\pi \cdot 0{,}30~\text{m} \\[4pt]
  &= 9\pi~\frac{\text{m}}{\text{s}} \\[4pt]
  &\approx 28{,}274~\frac{\text{m}}{\text{s}}
\end{align*}
$$
******************


$c)\;\;$ **Berechne** die auf das Handtuch wirkende Zentripetalkraft während des Schleudergangs. 
Gib das Ergebnis in Newton an und runde auf drei Nachkommastellen. 

<!-- data-solution-button="5"-->
$F_\text{Z}=$ [[  1065,917  ]] N
@Algebrite.check(1065.917)
******************
$$
F_\text{Z} = m \cdot \frac{v^2}{r}
$$

Mit $m = 0{,}40~\text{kg}$, $v = 9\pi~\dfrac{\text{m}}{\text{s}}$ und $r = 0{,}30~\text{m}$:

$$
\begin{align*}
F_\text{Z} 
&= 0{,}40~\text{kg} \cdot \frac{(9\pi)^2}{0{,}30~\text{m}} \\[4pt]
&= 0{,}40 \cdot \frac{81\pi^2}{0{,}30} \\[4pt]
&= \frac{0{,}40}{0{,}30} \cdot 81\pi^2 \\[4pt]
&= \frac{4}{3} \cdot 81\pi^2 \\[4pt]
&= 108\pi^2~\text{N} \\[4pt]
&\approx 1065,917~\text{N}
\end{align*}
$$

Die Zentripetalkraft auf das Handtuch beträgt also ungefähr $1{,}07\cdot 10^3\,\text{N}$.
******************






