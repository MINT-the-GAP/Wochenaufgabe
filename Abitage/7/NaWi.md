<!--
version:  0.0.1
language: de

mode: Presentation



import: https://cdn.jsdelivr.net/gh/LiaTemplates/algebrite@master/README.md
import: https://cdn.jsdelivr.net/gh/LiaTemplates/JSXGraph@main/README.md


import: https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/main/README.md

import: https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/main/imports/KoordREADME.md

import: https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/main/imports/FreezeREADME.md


author: Martin Lommatzsch
-->

# Aufgaben für die Prüfungstage - Physik: Klasse 7




> [!NOTE]
> Wenn du diese Aufgaben bearbeitest, solltest du nicht in ein anderes Fenster oder einen anderen Tab wechseln, sondern dich nur auf diese Aufgaben konzentrieren. Hole dir alle Materialien, die du zum Bearbeiten dieser Aufgaben brauchst. In deinem Fall solltest du dir Stifte und Papier holen, um dir zur Not Notizen machen zu können. Am Ende der Bearbeitung sendest du diese bearbeiteten Aufgaben an deinen Lehrer oder deine Lehrerin, sodass die Lehrkräfte sehen können, was du gemacht hast. <p align="right"> - Martin Lommatzsch </p>


> [!CAUTION]
> HINWEIS 1: <h3>Diese Aufgaben können abgegeben werden. Am Ende des Kurses kann der Kurs eingefroren werden. Dadurch entsteht ein Link, speichere diesen Link ab. Versende diesen Link via LernSax an deinen Lehrer oder deine Lehrerin, wenn deine Lehrkraft dies möchte. WICHTIG: Die Absprachen mit den jeweiligen Lehrkräften gelten. </h3>

> [!TIP]
> HINWEIS 2: <h3> Das Anzahl, wie oft du auf "Prüfen" drückst, wird auch erfasst. </h3>

> [!IMPORTANT]
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








## Kraft


Ein Quader mit den Maßen $a=3\,\text{cm}$, $b=1{,}5\,\text{cm}$ und $c=5\,\text{cm}$ besteht aus Platin mit einer Dichte von $21{,}45\,\dfrac{\text{g}}{\text{cm}^3}$. Dieser Quader wird an eine Feder gehängt, welche sich um $4\,\text{cm}$ ausdehnt. **Berechne** die Federkonstante der verwendeten Feder.



<!-- data-solution-timer="600s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
[[   118,3638   ]] @canvas
@Algebrite.check2(118.3638,0.01)
**********************
$$
\begin{align*}
V &= a \cdot b \cdot c \\
V &= 3\,\text{cm} \cdot 1{,}5\,\text{cm} \cdot 5\,\text{cm} \\
V &= 22{,}5\,\text{cm}^3
\end{align*}
$$

$$
\begin{align*}
m &= V \cdot \rho \\
m &= 22{,}5\,\text{cm}^3 \cdot 21{,}45\,\dfrac{\text{g}}{\text{cm}^3} \\
m &= 482{,}625\,\text{g} = 0{,}482625\,\text{kg}
\end{align*}
$$

$$
\begin{align*}
F &= m \cdot g \\
F &= 0{,}482625\,\text{kg} \cdot 9{,}81\,\dfrac{\text{N}}{\text{kg}} \\
F &\approx 4{,}7346\,\text{N}
\end{align*}
$$

$$
\begin{align*}
F &= D \cdot s \\
D &= \frac{F}{s} \\
D &= \frac{4{,}7346\,\text{N}}{0{,}04\,\text{m}} \\
D &\approx 118{,}3638\,\frac{\text{N}}{\text{m}}
\end{align*}
$$
**********************


@ADetails(6=BE;Kraft)




## Energie




Aufgabe 1: Ein Objekt mit der Masse von $750\,\text{g}$ befindet sich in einer Höhe über dem Erdboden, sodass es eine potentielle Energie von $275\,\text{J}$ besitzt. Berechne die Höhe, in der sich das Objekt befindet. 



<!-- data-solution-timer="600s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
[[   37.3768   ]] @canvas
@Algebrite.check2(37.3768,0.01)
**********************
$$
\begin{align*}
m &= 750\,\text{g} = 0{,}75\,\text{kg} \\
E_{\text{pot}} &= mgh \\
h &= \frac{E_{\text{pot}}}{mg} \\
h &= \frac{275\,\text{J}}{0{,}75\,\text{kg} \cdot 9{,}81\,\dfrac{\text{m}}{\text{s}^2}} \\
h &\approx 37{,}3768\,\text{m}
\end{align*}
$$
**********************


@ADetails(3=BE;Energie)

---

---




Aufgabe 2: Das Objekt aus Aufgabe 1 befindet sich nun auf dem Mond mit $g_{\text{Mond}}=1{,}62\,\dfrac{\text{m}}{\text{s}^2}$. Berechne die Höhe, in der sich das Objekt bei gleicher potentieller Energie von $275\,\text{J}$ befinden würde. 



<!-- data-solution-timer="600s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
[[   226.3374   ]] @canvas
@Algebrite.check2(226.3374,0.01)
**********************
$$
\begin{align*}
m &= 750\,\text{g} = 0{,}75\,\text{kg} \\
E_{\text{pot}} &= mgh \\
h &= \frac{E_{\text{pot}}}{mg} \\
h &= \frac{275\,\text{J}}{0{,}75\,\text{kg} \cdot 1{,}62\,\dfrac{\text{m}}{\text{s}^2}} \\
h &\approx 226{,}3374\,\text{m}
\end{align*}
$$
**********************


@ADetails(3=BE;Energie)






## Einheiten



<section class="dynFlex">

<div class="flex-child">


<!-- data-solution-timer="300s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
__$a)\;\;$__ $0,06\,\text{m} =$ [[   60   ]] $\text{mm}$
@Algebrite.check(60)

@ADetails(1=BE;Einheiten)

</div>

<div class="flex-child">

<!-- data-solution-timer="300s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
__$b)\;\;$__ $1,75\,\text{t} =$ [[   1750   ]] $\text{kg}$
@Algebrite.check(1750)

@ADetails(1=BE;Einheiten)

</div>

<div class="flex-child">

<!-- data-solution-timer="300s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
__$c)\;\;$__ $370\,\text{g} =$ [[   0,37   ]] $\text{kg}$
@Algebrite.check(0.37)

@ADetails(1=BE;Einheiten)

</div>

<div class="flex-child">

<!-- data-solution-timer="300s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
__$d)\;\;$__ $1446\,\text{min} =$ [[   24,1   ]] $\text{h}$
@Algebrite.check(24.1)

@ADetails(1=BE;Einheiten)

</div>

<div class="flex-child">

<!-- data-solution-timer="300s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
__$e)\;\;$__ $15\,\text{s} =$ [[   0,25   ]] $\text{min}$
@Algebrite.check(0.25)

@ADetails(1=BE;Einheiten)

</div>

<div class="flex-child">

<!-- data-solution-timer="300s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
__$f)\;\;$__ $24\,\text{min} =$ [[   0,4   ]] $\text{h}$
@Algebrite.check(0.4)

@ADetails(1=BE;Einheiten)

</div>

<div class="flex-child">

<!-- data-solution-timer="300s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
__$g)\;\;$__ $450\,\text{cm}^2 =$ [[   4,5   ]] $\text{dm}^2$
@Algebrite.check(4.5)

@ADetails(1=BE;Einheiten)

</div>

<div class="flex-child">

<!-- data-solution-timer="300s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
__$h)\;\;$__ $8,23\,\text{m}^2 =$ [[   82300   ]] $\text{cm}^2$
@Algebrite.check(82300)

@ADetails(1=BE;Einheiten)

</div>

<div class="flex-child">

<!-- data-solution-timer="300s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
__$i)\;\;$__ $0,04\,\text{m}^3 =$ [[   40   ]] $\text{dm}^3$
@Algebrite.check(40)

@ADetails(1=BE;Einheiten)

</div>

<div class="flex-child">

<!-- data-solution-timer="300s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
__$j)\;\;$__ $5,3\,\text{dm}^3 =$ [[   5300   ]] $\text{cm}^3$
@Algebrite.check(5300)

@ADetails(1=BE;Einheiten)

</div>

</section>





## Geschwindigkeit

Aufgabe 1: Ein Auto hat am Anfang einer Reise nach $40\,\text{min}$ eine Strecke von $55\,\text{km}$ zurückgelegt, danach brauchte das Auto für $30\,\text{km}$ insgesamt $12\,\text{min}$ und am Ende brauchte es nochmal $15\,\text{min}$ für $40\,\text{km}$.


<section class="dynFlex">

<div class="flex-child">

__$a)\;\;$__ **Berechne** die Geschwindigkeit im ersten Abschnitt in SI-Einheiten.


<!-- data-solution-timer="300s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
[[   22,9167   ]] $\dfrac{\text{m}}{\text{s}}$ @canvas
@Algebrite.check2(22.9167,0.01)
**********************
$$
\begin{align*}
v_1 &= \frac{x_1}{t_1} \\
v_1 &= \frac{55\,\text{km}}{40\,\text{min}} \\
v_1 &= \frac{55000\,\text{m}}{40 \cdot 60\,\text{s}} \\
v_1 &= \frac{55000}{2400}\,\frac{\text{m}}{\text{s}} \\
v_1 &\approx 22{,}9167\,\frac{\text{m}}{\text{s}}
\end{align*}
$$
**********************

@ADetails(2=BE;Geschwindigkeit)

</div>

<div class="flex-child">


__$b)\;\;$__ **Berechne** die Geschwindigkeit im zweiten Abschnitt in SI-Einheiten.


<!-- data-solution-timer="300s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
[[   41,6667   ]] $\dfrac{\text{m}}{\text{s}}$ @canvas
@Algebrite.check2(41.6667,0.01)
**********************
$$
\begin{align*}
v_2 &= \frac{x_2}{t_2} \\
v_2 &= \frac{30\,\text{km}}{12\,\text{min}} \\
v_2 &= \frac{30000\,\text{m}}{12 \cdot 60\,\text{s}} \\
v_2 &= \frac{30000}{720}\,\frac{\text{m}}{\text{s}} \\
v_2 &\approx 41{,}6667\,\frac{\text{m}}{\text{s}}
\end{align*}
$$
**********************

@ADetails(2=BE;Geschwindigkeit)

</div>

<div class="flex-child">


__$c)\;\;$__ **Berechne** die Geschwindigkeit im dritten Abschnitt in SI-Einheiten.


<!-- data-solution-timer="300s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
[[   44,4444   ]] $\dfrac{\text{m}}{\text{s}}$ @canvas
@Algebrite.check2(44.4444,0.01)
**********************
$$
\begin{align*}
v_3 &= \frac{x_3}{t_3} \\
v_3 &= \frac{40\,\text{km}}{15\,\text{min}} \\
v_3 &= \frac{40000\,\text{m}}{15 \cdot 60\,\text{s}} \\
v_3 &= \frac{40000}{900}\,\frac{\text{m}}{\text{s}} \\
v_3 &\approx 44{,}4444\,\frac{\text{m}}{\text{s}}
\end{align*}
$$
**********************

@ADetails(2=BE;Geschwindigkeit)

</div>

<div class="flex-child">


__$d)\;\;$__ **Berechne** die durchschnittliche Reisegeschwindigkeit in SI-Einheiten.


<!-- data-solution-timer="300s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
[[   31,0945   ]] $\dfrac{\text{m}}{\text{s}}$ @canvas
@Algebrite.check2(31.0945,0.01)
**********************
$$
\begin{align*}
\bar{v} &= \frac{x_1+x_2+x_3}{t_1+t_2+t_3} \\
\bar{v} &= \frac{55\,\text{km}+30\,\text{km}+40\,\text{km}}{40\,\text{min}+12\,\text{min}+15\,\text{min}} \\
\bar{v} &= \frac{125000\,\text{m}}{67 \cdot 60\,\text{s}} \\
\bar{v} &= \frac{125000}{4020}\,\frac{\text{m}}{\text{s}} \\
\bar{v} &= \frac{6250}{201}\,\frac{\text{m}}{\text{s}} \\
\bar{v} &\approx 31{,}0945\,\frac{\text{m}}{\text{s}}
\end{align*}
$$
**********************

@ADetails(2=BE;Geschwindigkeit)

</div>

</section>





## Elektrizitätslehre


$a)\;\;$ **Berechne** den Gesamtwiderstand der dargestellten Schaltung.

<center>
<!-- style="width:400px" -->
![](https://raw.githubusercontent.com/MINT-the-GAP/Wochenaufgabe/refs/heads/main/Zeug/GesamtWiderstand1.PNG)
</center>



<!-- data-solution-timer="600s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$R_{Gesamt} \approx$ [[  1157,233  ]]$\,\Omega$
@Algebrite.check2(1157.233,0.01)
*****************************

1. Schritt: Serienschaltung rechts zusammenfassen

Rechts unten liegen $1\,\text{k}\Omega$ und $47\,\Omega$ in Reihe:

$$
\begin{align*} 
R_{\text{rechts}} = R_3 + R_4 
= 1000\,\Omega + 47\,\Omega 
= 1047\,\Omega
\end{align*}
$$

---

2. Schritt: Parallelschaltung bilden

Der $2\,\text{k}\Omega$–Widerstand liegt parallel zu diesem rechten Zweig ($1047\,\Omega$).

Parallelschaltung zweier Widerstände:

$$
\begin{align*} 
\frac{1}{R_\parallel}
= \frac{1}{R_2} + \frac{1}{R_{\text{rechts}}}
= \frac{1}{2000\,\Omega} + \frac{1}{1047\,\Omega}
\end{align*}
$$

Rechnen:

$$
\begin{align*} 
R_\parallel 
= \frac{R_2 \cdot R_{\text{rechts}}}{R_2 + R_{\text{rechts}}}
= \frac{2000 \cdot 1047}{2000 + 1047}\,\Omega
\approx 687{,}233\,\Omega
\end{align*}
$$

---

3. Schritt: Gesamte Serienschaltung

Der $470\,\Omega$–Widerstand liegt in Reihe mit dem gesamten Parallelnetzwerk:

$$
\begin{align*} 
R_\text{ges} = R_1 + R_\parallel
= 470\,\Omega + 687{,}233\,\Omega
\approx 1157{,}233\,\Omega
\end{align*}
$$

*****************************


@ADetails(4=BE;Elektrizitätslehre)


---

---




$b)\;\;$ An der darstellten Schaltung liegt eine Spannung von $24\,$V an. **Berechne** die resultierende Stromstärke.



<!-- data-solution-timer="600s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
$I_{Gesamt} \approx$ [[  20,739  ]]$\,$mA
@Algebrite.check2(20.739,0.01)
*****************************
$$
\begin{align*} 
U & = R_\text{ges}I \quad \left| : R_\text{ges} \right. \\
I &= \frac{U}{R_\text{ges}}\\
&= \frac{24\,\text{V}}{1157{,}233\,\Omega}\\
&\approx 0{,}020739\,\text{A}\\
&\approx 20{,}739\,\text{mA}
\end{align*}
$$

*****************************


@ADetails(3=BE;Elektrizitätslehre)


---

---




$c)\;\;$ **Kreuze an**, ob die Aussage "wahr", "falsch" oder "nicht entscheidbar" ist.


<!-- data-randomize="true" data-show-partial-solution="true"  data-solution-timer="600s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
- [[wahr]   (falsch)    [nicht entscheidbar]]
- [ [X]       [ ]             [ ]     ]  Durch den rechten Leiter fließt ungefähr ein Drittel des Stroms.
- [ ( )       (X)             ( )     ]  Wenn man an der Stelle des $470\,\Omega$-Widerstandes ein Amperemeter schalten würde, würde die Gesamtstromstärke sinken.
- [ [X]       [ ]             [ ]     ]  Die Spannung am $2k\,\Omega$-Widerstand ist größer als am $1k\,\Omega$-Widerstand.
- [ ( )       (X)             ( )     ]  Würde man eine Lampe vor dem $2k\,\Omega$-Widerstand bzw. dem $1k\,\Omega$-Widerstand schalten, wäre die am $2k\,\Omega$-Widerstand heller.



@ADetails(BE=4;Elektrizitätslehre)






# Abgabe



@Abgabe

@Auswertung(F12;Tab;Time)