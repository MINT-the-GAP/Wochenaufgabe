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

In einer Jahrgangsstufe werden 120 SchülerInnen nach ihrer bevorzugten Fremdsprache gefragt. Zur Auswahl stehen Englisch und Französisch. Außerdem wird erfasst, ob sie regelmäßig Nachhilfe in Sprachen nehmen. Die Ergebnisse dieser Datenerfassungen sind:

+ 72 SchülerInnen bevorzugen Englisch.
+ 48 SchülerInnen bevorzugen Französisch.
+ Von den Englisch-SchülerInnen nehmen 18 regelmäßig Nachhilfe.
+ Von den Französisch-SchülerInnen nehmen 12 regelmäßig Nachhilfe.

__Aufgabe 1:__ Erstelle eine Vierfeldertafel mit absoluten SchülerInnenzahlen zu diesem Sachzusammenhang.


{{1}}
|    | Nachhilfe ja | Nachhilfe nein | Summe |
|  Englisch     | 18 | 54 | 72  |
|  Französisch  | 12 | 36 | 48  |
| Summe         | 30 | 90 | 120 |



__Aufgabe 2:__ Berechne die Wahrscheinlichkeit, dass eine zufällig ausgewählt Person Französisch gewählt hat.

{{2}}
$$
\begin{align*} 
&P(F) = \dfrac{48}{120} = 0,4  \\
\end{align*}
$$



__Aufgabe 3:__ Berechne die Wahrscheinlichkeit, dass eine zufällig ausgewählt Person Nachhilfe in Anspruch nimmt.

{{3}}
$$
\begin{align*} 
&P(N) = \dfrac{30}{120} = 0,25 \\
\end{align*}
$$


__Aufgabe 4:__ Berechne die Wahrscheinlichkeit, dass eine zufällig ausgewählt Person Englisch gewählt hat und keine Nachhilfe in Anspruch nimmt.

{{3}}
$$
\begin{align*} 
&P(\bar{F} \cap \bar{N}) = \dfrac{54}{120} = 0,45 \\
\end{align*}
$$









#  Stochastik - Aufgabe 3: 


Eine Stadtbibliothek untersucht das Leseverhalten von 200 Jugendlichen. Es wird erfasst, ob sie Romane oder Sachbücher bevorzugen und ob sie regelmäßig die Bibliothek besuchen. Dabei wurde festgestellt, dass 120 Jugendliche Romane und 80 Jugendliche Sachbücher bevorzugen, während von den Roman-Lesern 90 und von den Sachbuch-Lesern 50 regelmäßig die Bibliothek regelmäßig die Bibliothek besuchen.



__Aufgabe 1:__ Erstelle eine Vierfeldertafel mit absoluten SchülerInnenzahlen zu diesem Sachzusammenhang.


{{1}}
|    | Besuch ja | Besuch nein | Summe |
|  Romane       | 90 | 30 | 120  |
|  Sachbücher   | 50 | 30 | 80  |
| Summe         | 140 | 60 | 120 |



__Aufgabe 2:__ Berechne die Wahrscheinlichkeit, dass eine zufällig ausgewählt Person Romane bevorzugt.

{{2}}
$$
\begin{align*} 
&P(R) = \dfrac{120}{200} = 0,6  \\
\end{align*}
$$



__Aufgabe 3:__ Berechne die Wahrscheinlichkeit, dass eine zufällig ausgewählt Person die Bibliothek regelmäßig aufsucht.

{{3}}
$$
\begin{align*} 
&P(B) = \dfrac{140}{200} = 0,7  \\
\end{align*}
$$



__Aufgabe 3:__ Berechne die Wahrscheinlichkeit, dass eine zufällig ausgewählt Person Sachbücher bevorzugt und die Bibliothek nicht regelmäßig aufsucht.

{{4}}
$$
\begin{align*} 
&P(\bar{R} \cap \bar{B}) = \dfrac{30}{200} = 0,15  \\
\end{align*}
$$










#  Stochastik - Aufgabe 4: 

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

__Aufgabe 3:__ **Berechne** die Wahrscheinlichkeit, dass es sich bei retournierter Ware um Bekleidung handelt.

{{3}}
$$
\begin{align*} 
 P(\left. B \right| R)  =  \dfrac{P(B \cap R)}{P(R)} = \dfrac{8}{11} \\
\end{align*}
$$

---

__Aufgabe 4:__ **Zeige**, dass es sich um eine bedingte Wahrscheinlichkeit handelt.

{{4}}
$$
\begin{align*} 
&P(B \cap R) = P(B) \cdot P(\left. R \right|B) = 0,08 \\
&P(B) \cdot P(R) = 0,044 \neq P(B \cap R) \qquad _{\Box}  \\
\end{align*}
$$

---


__Aufgabe 5:__ **Berechne** die Wahrscheinlichkeit, dass es sich bei nicht-retournierter Ware um Bekleidung handelt.

{{5}}
$$
\begin{align*} 
&P( \bar{R}) = 1 -  P(R)  = 0,89 \\
&P(  B  \cap  \bar{R} )  = P(B) P(\left. \bar{R} \right|B) = 0,32 \\
&P(\left.B \right| \bar{R})  =   \dfrac{P(  B  \cap  \bar{R} )}{P( \bar{R})}    = \dfrac{32}{89} \\
\end{align*}
$$









#  Stochastik - Aufgabe 5: 

Im Schul-Leichtathletikteam wird diskutiert, ob gezieltes Aufwärmen vor dem Training die Verletzungsgefahr senkt. Über eine Saison wurden Daten erhoben und in einer Stichprobe erfasst. Hierfür wurde eine Stichprobe von 300 Probanten betrachtet, wovon 180 sich regelmäßig aufwärmten. Die Verletzungsquote betrog dabei 12%, während in nur 10% der aufgewärmten LeichtathletInnen sich verletzten.




__Aufgabe 1:__ Erstelle eine Vierfeldertafel mit absoluten LeichtathletInnenzahlen zu diesem Sachzusammenhang.


{{1}}
|               | $A$ | $\bar{A}$ | Summe |
|  $V$          | 18   |  18   | 36    |
|  $\bar{V}$    | 162  |  102  |  264  |
| Summe         | 180  |  120  | 300   |


---


__Aufgabe 2:__ Berechne die Wahrscheinlichkeit, dass eine Person, die sich nicht aufgewärmt hat, sich verletzte.


{{2}}
$$
\begin{align*} 
P( \left. V \right| \bar{A} ) =  \dfrac{P(  V \cap \bar{A} ) }{P(\bar{A})} = 0,15  \\
\end{align*}
$$


---

__Aufgabe 3:__ Berechne die Wahrscheinlichkeit, dass eine verletzte Person sich abgewärmt hatte.


{{3}}
$$
\begin{align*} 
P( \left. A \right| V )  =  \dfrac{P(  A \cap V ) }{P(\bar{V})}  =  0,5  \\
\end{align*}
$$



---

__Aufgabe 4:__ Berechne die Wahrscheinlichkeit, dass eine zufällig gewählte unverletzte Person sich nicht aufgewärmt hat.


{{4}}
$$
\begin{align*} 
P( \left. \bar{A} \right| \bar{V} ) =   \dfrac{P(  \bar{A} \cap \bar{V} ) }{P(\bar{V})}  = \dfrac{17}{44}  \\
\end{align*}
$$


---


__Aufgabe 5:__ **Zeige**, dass es sich um eine bedingte Wahrscheinlichkeit handelt.

{{5}}
$$
\begin{align*} 
&P(V \cap A) = 0,01 \\
&P(V) = 0,12 \neq P(V \cap A) \qquad _{\Box}  \\
\end{align*}
$$
