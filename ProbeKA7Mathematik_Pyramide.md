<!--
version:  0.0.1

language: de

@style
main > *:not(:last-child) {
  margin-bottom: 3rem;
}

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

@round
<script>
  let value = `@input`;
  if (value.startsWith("@")) {
    ""
  } else {
    value = JSON.parse(value);
    value = value[0]
    value = value.replace(/,/g, ".");
    value = parseFloat(value);
    value = Math.round(value * Math.pow(10,@1)) / Math.pow(10,@1);
    value == @0
  }
</script>
@end

-->

# Probeklassenarbeit für Mathematik - Klasse 7: Pyramide und Dreiecke

<br>

> Letztes Update am 10.05.2025 gegen 17 Uhr

<br>

Swipe (Wische) entweder weiter oder klicke unten links auf neben der Seitenzahl auf den Pfeil nach rechts.

<br>

Diese Probearbeit hat mehr Aufgaben als die richtige Arbeit, damit du genug zum Üben hast. Es sind viele verschiedene Aufgabentypen abgebildet, sodass du alles nochmal bei der Bearbeitung dieser Aufgaben wiederholst.

## Aufgabe 1

**Zeichne** das Schrägbild der folgenden Pyramiden. (Es gibt für diese Aufgabe NOCH keine Musterlösung oder Bearbeitung in LiaScript.)

__$a)\;\;$__ $a=b=5\,$cm $\;\;\wedge\;\; k=7\,$cm \

__$b)\;\;$__ $a=6\,$cm $\;\;\wedge\;\; b=8\,$cm $\;\;\wedge\;\; k=7,5\,$cm \

__$c)\;\;$__ $a=5,5\,$cm $\;\;\wedge\;\; b=6\,$cm $\;\;\wedge\;\; k=3,5\,$cm \


<br>
<br>
<br>
<br>


## Aufgabe 2

**Zeichne** ein Netz der folgenden Pyramiden. (Es gibt für diese Aufgabe NOCH keine Musterlösung oder Bearbeitung in LiaScript, außer für die nötige Rechnung.)

__$a)\;\;$__ $a=b=4,5\,$cm $\;\;\wedge\;\; h_a=h_b=5\,$cm \

__$b)\;\;$__ $a=b=6\,$cm $\;\;\wedge\;\; k=4\,$cm \


[[!]]
<script>true</script>
***********

$$ 
\begin{align*}
    h_a^2 & = k^2 + \left(\dfrac{b}{2}\right)^2  \\
    h_a  & = \sqrt{ k^2 + \left(\dfrac{b}{2}\right)^2 }  \\
    h_a  & = \sqrt{ \left(4\,\text{cm}\right)^2 + \left(\dfrac{6\,\text{cm}}{2}\right)^2 }  \\
    h_a  & = \sqrt{ 16\,\text{cm}^2 + 9\,\text{cm}^2 }  \\
    h_a  & = \sqrt{ 25\,\text{cm}^2 }  \\
    h_a  & = 5\,\text{cm} \\
\end{align*}
$$

***********




<br>
<br>
<br>
<br>


## Aufgabe 3


**Konstruiere** die beschriebenen Dreiecke. **Konstruiere** anschließend den Umkreis und **gib** den Radius **an**. (Es gibt für diese Aufgabe NOCH keine zeichnerische Musterlösung oder Bearbeitung in LiaScript.)

__$a)\;\;$__ $a=4,5\,$cm $\;\;\wedge\;\; b=5\,$cm $\;\;\wedge\;\; c=6\,$cm \


<!-- data-solution-button="3" -->
$r=$  [[   3,1  ]] cm
@Algebrite.check2(3.1,0.1)

__$b)\;\;$__ $b=7\,$cm $\;\;\wedge\;\; \gamma= 65^\circ  \;\;\wedge\;\; \alpha= 50^\circ$ \


<!-- data-solution-button="3" -->
$r=$  [[   3,8  ]] cm
@Algebrite.check2(3.8,0.1)



<br>
<br>
<br>
<br>


## Aufgabe 4


**Konstruiere** die beschriebenen Dreiecke. **Konstruiere** anschließend den Innenkreis und **gib** den Radius **an**. (Es gibt für diese Aufgabe NOCH keine zeichnerische Musterlösung oder Bearbeitung in LiaScript.)

__$a)\;\;$__ $a=6,5\,$cm $\;\;\wedge\;\; b=3,5\,$cm $\;\;\wedge\;\; \gamma= 110^\circ$ \


<!-- data-solution-button="3" -->
$r=$  [[   1  ]] cm
@Algebrite.check2(1,0.1)


__$b)\;\;$__ $c=8\,$cm $\;\;\wedge\;\; \gamma= 75^\circ  \;\;\wedge\;\; \alpha= 55^\circ$ \


<!-- data-solution-button="3" -->
$r=$  [[   2  ]] cm
@Algebrite.check2(2,0.1)






<br>
<br>
<br>
<br>


## Aufgabe 5

Gegeben sei eine Pyramide mit quadratischer Grundfläche mit einer Seitenlänge $a$ von $7,5\,$cm und einer Manteldreieckshöhe von $5,5\,$cm zu $a$. Berechne den Oberflächeninhalt der Pyramide.

<!-- data-solution-button="3" -->
$O=$  [[   138,75  ]] cm$^2$
***********************

$$ 
\begin{align*}
    O_P & = a^2 + 2 a h_a \\
    & = \left( 7,5 \,\text{cm}\right)^2 + 2 \cdot 7,5 \,\text{cm} \cdot 5,5 \,\text{cm} \\
    & = 138,75\,\text{cm}^2 \\
\end{align*}
$$

***********************



<br>
<br>
<br>
<br>


## Aufgabe 6

Gegeben sei eine Pyramide mit quadratischer Grundfläche mit einer Seitenlänge von $4,5\,$cm und einer Körperhöhe von $9,2\,$cm. Die Pyramide besteht aus einem Material mit einer Dichte von $7\,\dfrac{\text{g}}{\text{cm}^3}$. Berechne die Masse der Pyramide.

<!-- data-solution-button="3" -->
$m=$  [[   0,4347  ]] kg
***********************

$$ 
\begin{align*}
    V_P & = \dfrac{1}{3} a^2 k \\
    & = \dfrac{1}{3} \left( 4,5 \,\text{cm}\right)^2  \cdot 9,2 \,\text{cm}  \\
    & = 62,1\,\text{cm}^3 \\
\end{align*}
$$
<br>
$$
\begin{align*}
    \rho & = \dfrac{m}{V}  \quad \left|  \cdot V  \right.  \\
    m & = V \cdot \rho   \\
    & = 62,1\,\text{cm}^3 \cdot  7\,\dfrac{\text{g}}{\text{cm}^3}  \\
    & = 434,7\,\text{g}  \\
    & = 0,4347\,\text{kg}  \\
\end{align*}
$$

***********************


<br>
<br>
<br>
<br>


## Aufgabe 7


Gegeben sei eine Pyramide mit quadratischer Grundfläche mit einer Höhe von $24\,$cm und einer Masse von $18,816\,$kg. Die Pyramide besteht aus einem Material mit einer Dichte von $12\,\dfrac{\text{g}}{\text{cm}^3}$. Berechne den Oberflächeninhalt der Pyramide.




<!-- data-solution-button="3" -->
$O=$  [[   137200  ]] cm$^2$
***********************

$$ 
\begin{align*}
    \rho & = \dfrac{m}{V}  \quad \left|  \cdot V  \right.  \\
    V \cdot \rho & = m  \quad \left|  : \rho  \right.   \\
    V & = \dfrac{m}{\rho}   \\
    & = \dfrac{18816\,\text{g} }{  12\,\frac{\text{g}}{\text{cm}^3} } \\
    & = 1568\,\text{cm}^3  \\
\end{align*}
$$
<br>
$$
\begin{align*}
    V_P & = \dfrac{1}{3} a^2 k  \quad \left|  \cdot 3  \right.   \\
    3 V_P & =  a^2 k  \quad \left|  :k  \right.   \\
    \dfrac{3 V_P}{k} & =  a^2     \\
    \Rightarrow\;\;  a & =  \sqrt{\dfrac{3 V_P}{k}}     \\
    a & =  \sqrt{\dfrac{3 \cdot 1568\,\text{cm}^3}{ 24\,\text{cm}}}     \\
    a & =  \sqrt{\dfrac{1568\,\text{cm}^3}{ 8\,\text{cm}}}     \\
    a & =  \sqrt{196\,\text{cm}^2}     \\
    a & =  14\,\text{cm}     \\
\end{align*}
$$
<br>
$$
\begin{align*}
    h_a^2 & = k^2 + \left(\dfrac{b}{2}\right)^2 \qquad \text{mit:} \;\; a=b \\
    h_a^2 & = k^2 + \left(\dfrac{a}{2}\right)^2  \\
    h_a  & = \sqrt{ k^2 + \left(\dfrac{a}{2}\right)^2 }  \\
    h_a  & = \sqrt{ \left(24\,\text{cm}\right)^2 + \left(\dfrac{14\,\text{cm}}{2}\right)^2 }  \\
    h_a  & = \sqrt{ 576\,\text{cm}^2 + 49\,\text{cm}^2 }  \\
    h_a  & = \sqrt{ 625\,\text{cm}^2 }  \\
    h_a  & = 25\,\text{cm} \\
\end{align*}
$$
<br>
$$
\begin{align*}
    O_P & = a^2 + 2 a h_a \\
    & = \left( 14 \,\text{cm}\right)^2 + 2 \cdot 14 \,\text{cm} \cdot 25 \,\text{cm} \\
    & = 137200\,\text{cm}^2 \\
\end{align*}
$$

***********************


<br>
<br>
<br>
<br>