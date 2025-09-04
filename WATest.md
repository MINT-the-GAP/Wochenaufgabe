<!--
version:  0.0.2
language: de

tags: Demo
comment: Fächerbezogener Beispielkurs mit interaktiven Elemente in LiaScript für den Schulunterricht
author: Martin Lommatzsch, André Dietrich, Sebastian Zug


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


import: https://raw.githubusercontent.com/liaTemplates/ABCjs/main/README.md
        https://raw.githubusercontent.com/LiaTemplates/Speech-Recognition-Quiz/refs/heads/main/README.md
        https://raw.githubusercontent.com/liaTemplates/AVR8js/main/README.md
        https://raw.githubusercontent.com/liaTemplates/JSXGraph/main/README.md
        https://raw.githubusercontent.com/LiaTemplates/mec2/main/README.md
        https://raw.githubusercontent.com/LiaTemplates/CollaborativeDrawing/main/README.md
        https://raw.githubusercontent.com/LiaTemplates/SpreadSheet/refs/heads/main/README.md
        https://github.com/LiaTemplates/PeriodicTable/blob/main/README.md

persistent: true

edit: true

eingabe: <script input="number" input-always-active modify="false" value="0" default="0">@input</script>

-->




# Stochastik - Aufgabe 1: 



An einem Gymnasium fahren **50 %** der SchülerInnen mit **ÖPNV** zur Schule, die übrigen **50 %** kommen **anders**. In einer bestimmten Woche gilt:

- Unter den ÖPNV-NutzerInnen kommen **20 %** mindestens einmal zu spät.
- Unter den anderen kommen **10 %** mindestens einmal zu spät.

__Aufgabe 1:__ **Skizziere** ein Baumdiagramm mit zwei Stufen. Zuerst die Betrachtung des ÖPNVs.

{{1}}
$$
\begin{align*} 
&P(Ö)= 0,5 \;\;\wedge\;\; P(\bar{Ö})=0,5 \;\;\wedge\;\; P(\left. V \right|Ö)=0,2 \;\;\wedge\;\; P(\left. V \right|\bar{Ö})=0,1 \\
&P(Ö \cap V) = P(Ö) \cdot P(\left. V \right|Ö) = 0,1 \\
&P(\bar{Ö} \cap V) = P(\bar{Ö}) \cdot P(\left. V \right|\bar{Ö}) = 0,05
\end{align*}
$$

---

__Aufgabe 2:__ **Berechne** die Wahrscheinlichkeit, dass eine SchülerIn zu spät kommt.

{{2}}
$$
\begin{align*} 
P(V) = P(Ö \cap V) + P(\bar{Ö} \cap V) = 0,15 \\
\end{align*}
$$

---

__Aufgabe 3:__ **Berechne** die Wahrscheinlichkeit, dass eine verspätet SchülerIn den ÖPNV benutzte.

{{3}}
$$
\begin{align*} 
 P(\left. Ö \right| V)  =  \dfrac{P(Ö \cap V)}{P(V)} = 0,\bar{6} \\
\end{align*}
$$

---

__Aufgabe 4:__ **Zeige**, dass es sich um eine bedingte Wahrscheinlichkeit handelt.

{{4}}
$$
\begin{align*} 
&P(Ö \cap V) = P(Ö) \cdot P(\left. V \right|Ö) = 0,1 \\
&P(Ö) \cdot P(V) = 0,075 \neq P(Ö \cap V) \qquad _{\Box}  \\
\end{align*}
$$

---


__Aufgabe 5:__ **Berechne** die Wahrscheinlichkeit, dass eine pünktlichte SchülerIn den ÖPNV benutzte.

{{5}}
$$
\begin{align*} 
&P( \bar{V}) = 1 -  P(V)  = 0,85 \\
&P(  Ö  \cap  \bar{V} )  = P(Ö) P(\left. \bar{V} \right|Ö) = 0,4 \\
&P(\left.Ö \right| \bar{V})  =   \dfrac{P(  Ö  \cap  \bar{V} )}{P( \bar{V})}    = \dfrac{8}{17} \\
\end{align*}
$$








#  Stochastik - Aufgabe 2: 

Ein Online-Shop unterscheidet Bestellungen nach Bekleidung und Nicht-Bekleidung. In der betrachteten Woche gilt: 40% der Bestellungen sind Bekleidung. Aber es kommen auch regelmäßig Rückgabenwünsche herein. Bei Bekleidung werden 20% der Bestellungen retourniert und 5% der Nicht-Bekleidung werden zurückgegeben.


__Aufgabe 1:__ **Skizziere** ein Baumdiagramm mit zwei Stufen. Zuerst die Betrachtung der Kategorien.

{{1}}
$$
\begin{align*} 
&P(B)= 0,4 \;\;\wedge\;\; P(\bar{B})=0,6 \;\;\wedge\;\; P(\left. R \right|B)=0,2 \;\;\wedge\;\; P(\left. R \right|\bar{B})=0,05 \\
&P(B \cap R) = P(B) \cdot P(\left. R \right|B) = 0,08 \\
&P(\bar{B} \cap R) = P(\bar{B}) \cdot P(\left. R \right|\bar{B}) = 0,03
\end{align*}
$$



---

__Aufgabe 2:__ **Berechne** die Wahrscheinlichkeit, für eine Retour.

{{2}}
$$
\begin{align*} 
P(R) = P(B \cap R) + P(\bar{B} \cap R) = 0,11 \\
\end{align*}
$$

---

__Aufgabe 3:__ **Berechne** die Wahrscheinlichkeit, dass eine verspätet SchülerIn den ÖPNV benutzte.

{{3}}
$$
\begin{align*} 
 P(\left. Ö \right| V)  =  \dfrac{P(Ö \cap V)}{P(V)} = 0,\bar{6} \\
\end{align*}
$$

---

__Aufgabe 4:__ **Zeige**, dass es sich um eine bedingte Wahrscheinlichkeit handelt.

{{4}}
$$
\begin{align*} 
&P(Ö \cap V) = P(Ö) \cdot P(\left. V \right|Ö) = 0,1 \\
&P(Ö) \cdot P(V) = 0,075 \neq P(Ö \cap V) \qquad _{\Box}  \\
\end{align*}
$$

---


__Aufgabe 5:__ **Berechne** die Wahrscheinlichkeit, dass eine pünktlichte SchülerIn den ÖPNV benutzte.

{{5}}
$$
\begin{align*} 
&P( \bar{V}) = 1 -  P(V)  = 0,85 \\
&P(  Ö  \cap  \bar{V} )  = P(Ö) P(\left. \bar{V} \right|Ö) = 0,4 \\
&P(\left.Ö \right| \bar{V})  =   \dfrac{P(  Ö  \cap  \bar{V} )}{P( \bar{V})}    = \dfrac{8}{17} \\
\end{align*}
$$


