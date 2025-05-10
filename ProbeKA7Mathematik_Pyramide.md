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

> Letztes Update am 10.05.2025 gegen 10 Uhr

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
 
