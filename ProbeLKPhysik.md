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



# Aufgabe 1



Ein Objekt fällt reibungsfrei aus einer Höhe von $5\,$m und hat zu Beginn des Falls schon eine kinetische Energie von $0,25\,$J. Berechne die Geschwindigkeit, mit der das Objekt auf den Boden auftrifft. Das objekt besitzt eine Masse von $150\,$g. Runde auf zwei Nachkommastellen.

<section class="flex-container">

<div class="flex-child">

$v=$ [[10,07]] $\dfrac{\text{m}}{\text{s}}$
***********
$$
\begin{align*}
E_{kin} + E_{pot} & = E'_{kin} + E'_{pot} \\
E_{kin} + E_{pot} & = E'_{kin} + \rlap{\,/}E'_{pot} \\
E_{kin} + mgh & = \frac{1}{2} m v^2  \quad \left| \cdot 2  \right. \\
2E_{kin} + 2mgh & =   m v^2  \quad \left| :m  \right. \\
\frac{2E_{kin}}{m} + 2gh & =    v^2    \\
v & = \sqrt{\frac{2E_{kin}}{m} + 2gh}    \\
v & = \sqrt{\frac{2 \cdot 0,25\,\text{J}}{0,15\,\text{kg}} + 2 \cdot 9,81\,\dfrac{\text{m}}{\text{s}^2} \cdot \, 5 \text{m}}    \\
v & \approx  10,07 \dfrac{\text{m}}{\text{s}}
\end{align*}
$$
***********



</div>
 


</section>

