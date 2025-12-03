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



An einem Gymnasium fahren 50 % der Schüler mit ÖPNV zur Schule, die übrigen 50 % kommen anders. In einer bestimmten Woche gilt:

- Unter den ÖPNV-Nutzern kommen 20 %** mindestens einmal zu spät.
- Unter den anderen kommen 10 % mindestens einmal zu spät.

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

__Aufgabe 2:__ **Berechne** die Wahrscheinlichkeit, dass ein Schüler zu spät kommt.

{{2}}
$$
\begin{align*} 
P(V) = P(Ö \cap V) + P(\bar{Ö} \cap V) = 0,15 \\
\end{align*}
$$

---

__Aufgabe 3:__ **Berechne** die Wahrscheinlichkeit, dass ein verspäteter Schüler den ÖPNV benutzte.

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


__Aufgabe 5:__ **Berechne** die Wahrscheinlichkeit, dass ein pünktlichter Schüler den ÖPNV benutzte.

{{5}}
$$
\begin{align*} 
&P( \bar{V}) = 1 -  P(V)  = 0,85 \\
&P(  Ö  \cap  \bar{V} )  = P(Ö) P(\left. \bar{V} \right|Ö) = 0,4 \\
&P(\left.Ö \right| \bar{V})  =   \dfrac{P(  Ö  \cap  \bar{V} )}{P( \bar{V})}    = \dfrac{8}{17} \\
\end{align*}
$$



#  Stochastik - Aufgabe 2: 

In einer Jahrgangsstufe werden 120 Schülern nach ihrer bevorzugten Fremdsprache gefragt. Zur Auswahl stehen Englisch und Französisch. Außerdem wird erfasst, ob sie regelmäßig Nachhilfe in Sprachen nehmen. Die Ergebnisse dieser Datenerfassungen sind:

+ 72 Schülern bevorzugen Englisch.
+ 48 Schülern bevorzugen Französisch.
+ Von den Englisch-Schülern nehmen 18 regelmäßig Nachhilfe.
+ Von den Französisch-Schülern nehmen 12 regelmäßig Nachhilfe.

__Aufgabe 1:__ Erstelle eine Vierfeldertafel mit absoluten Schülerzahlen zu diesem Sachzusammenhang.


{{1}}
|    | Nachhilfe ja | Nachhilfe nein | Summe |
|  Englisch     | 18 | 54 | 72  |
|  Französisch  | 12 | 36 | 48  |
| Summe         | 30 | 90 | 120 |



__Aufgabe 2:__ Berechne die Wahrscheinlichkeit, dass eine zufällig ausgewählte Person Französisch gewählt hat.

{{2}}
$$
\begin{align*} 
&P(F) = \dfrac{48}{120} = 0,4  \\
\end{align*}
$$



__Aufgabe 3:__ Berechne die Wahrscheinlichkeit, dass eine zufällig ausgewählte Person Nachhilfe in Anspruch nimmt.

{{3}}
$$
\begin{align*} 
&P(N) = \dfrac{30}{120} = 0,25 \\
\end{align*}
$$


__Aufgabe 4:__ Berechne die Wahrscheinlichkeit, dass eine zufällig ausgewählte Person Englisch gewählt hat und keine Nachhilfe in Anspruch nimmt.

{{3}}
$$
\begin{align*} 
&P(\bar{F} \cap \bar{N}) = \dfrac{54}{120} = 0,45 \\
\end{align*}
$$









#  Stochastik - Aufgabe 3: 


Eine Stadtbibliothek untersucht das Leseverhalten von 200 Jugendlichen. Es wird erfasst, ob sie Romane oder Sachbücher bevorzugen und ob sie regelmäßig die Bibliothek besuchen. Dabei wurde festgestellt, dass 120 Jugendliche Romane und 80 Jugendliche Sachbücher bevorzugen, während von den Roman-Lesern 90 und von den Sachbuch-Lesern 50 regelmäßig die Bibliothek besuchen.



__Aufgabe 1:__ Erstelle eine Vierfeldertafel mit absoluten Jugendlichenzahlen zu diesem Sachzusammenhang.


{{1}}
|    | Besuch ja | Besuch nein | Summe |
|  Romane       | 90 | 30 | 120  |
|  Sachbücher   | 50 | 30 | 80  |
| Summe         | 140 | 60 | 200 |



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

Im Schul-Leichtathletikteam wird diskutiert, ob gezieltes Aufwärmen vor dem Training die Verletzungsgefahr senkt. Über eine Saison wurden Daten erhoben und in einer Stichprobe erfasst. Hierfür wurde eine Stichprobe von 300 Probanten betrachtet, wovon 180 sich regelmäßig aufwärmten. Die gesamte Verletzungsquote betrog 12%, während in nur 10% der aufgewärmten Leichtathleten sich verletzten.




__Aufgabe 1:__ Erstelle eine Vierfeldertafel mit absoluten Leichtathletenzahlen zu diesem Sachzusammenhang.


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





#  Stochastik - Aufgabe 6: 



Gegeben ist eine Zufallsvariable $X$ mit $X \sim B(n=5, p)$.

Es soll überprüft werden, ob die Erfolgswahrscheinlichkeit $p$ eher
„normal“ ($p = 0{,}5$) oder eher „erhöht“ ($p = 0{,}8$) ist.

Es wird folgender Test verwendet (Entscheidungsregel):

> Wenn in den $5$ Versuchen mindestens $4$ Erfolge auftreten ($X \ge 4$),
> dann wird die Nullhypothese verworfen.  
> Sonst ($X \le 3$) wird die Nullhypothese beibehalten.


__$a)\;\;$__ **Formuliere** die Nullhypothese $H_0$ und die Gegenhypothese (alternative Hypothese) $H_1$.


[[!]]
<script>true</script>
********************

Es werden zwei feste Werte für $p$ verglichen:

- Nullhypothese:  
  $H_0:\; p = 0{,}5$

- Gegenhypothese:  
  $H_1:\; p = 0{,}8$

********************

__$b)\;\;$__ **Bestimme** den $\alpha$-Fehler dieses Tests. 
Das ist die Wahrscheinlichkeit, dass $H_0$ verworfen wird, obwohl in Wirklichkeit $p = 0{,}5$ gilt.

$\alpha = $ [[ 18,75 ]]$\,\%$
@Algebrite.check(18.75)
********************
$\alpha = P(X \ge 4 \mid p = 0{,}5) = P(X = 4 \mid p = 0{,}5) + P(X = 5 \mid p = 0{,}5)$.

Mit $X \sim B(5, 0{,}5)$ gilt allgemein
$P(X = k) = \binom{5}{k} \cdot 0{,}5^k \cdot 0{,}5^{5-k} = \binom{5}{k} \cdot 0{,}5^5$.

Also
$P(X = 4) = \binom{5}{4} \cdot 0{,}5^4 \cdot 0{,}5^1 = 5 \cdot 0{,}5^4 \cdot 0{,}5^1$,

$P(X = 5) = \binom{5}{5} \cdot 0{,}5^5 = 1 \cdot 0{,}5^5$.

Damit
$\alpha = (5 + 1) \cdot 0{,}5^5 = 6 \cdot \dfrac{1}{32} = \dfrac{6}{32} = \dfrac{3}{16} = 0{,}1875$.

In Prozent: $\alpha = 18{,}75\%$.

********************



__$c)\;\;$__ **Bestimme** den $\beta$-Fehler dieses Tests.
Das ist die Wahrscheinlichkeit, dass $H_0$ **nicht** verworfen wird, obwohl in Wirklichkeit $p = 0{,}8$ gilt. \


$\beta \approx $ [[ 26,27 ]]$\,\%$
@Algebrite.check2(26.27,0.01)
********************
Wir betrachten nun $X \sim B(5, 0{,}8)$ und berechnen
$\beta = P(X \le 3 \mid p = 0{,}8)$.

Bequemer ist:
$\beta = 1 - P(X \ge 4 \mid p = 0{,}8) = 1 - \bigl(P(X = 4) + P(X = 5)\bigr)$.

Nun
$P(X = 4) = \binom{5}{4} \cdot 0{,}8^4 \cdot 0{,}2^1 = 5 \cdot 0{,}8^4 \cdot 0{,}2$,

$P(X = 5) = \binom{5}{5} \cdot 0{,}8^5 \cdot 0{,}2^0 = 1 \cdot 0{,}8^5$.

Also
$P(X = 4) = 5 \cdot 0{,}8^4 \cdot 0{,}2 = 5 \cdot 0{,}4096 \cdot 0{,}2 = 0{,}4096$,

$P(X = 5) = 0{,}8^5 = 0{,}32768$.

Damit
$P(X \ge 4) = 0{,}4096 + 0{,}32768 = 0{,}73728$

und
$\beta = 1 - 0{,}73728 = 0{,}26272$.

In Prozent: $\beta \approx 26{,}3\%$.

********************

__$d)\;\;$__ **Erkläre** in eigenen Worten, was $\alpha$- und $\beta$-Fehler in dieser Situation bedeuten.



[[!]]
<script>true</script>
********************

- Der $\alpha$-Fehler (ca. $18{,}75\%$):  
  Das ist die Wahrscheinlichkeit, dass der Test sagt  
  „$p = 0{,}8$ (erhöht)“ und die Nullhypothese $H_0: p = 0{,}5$
  verwirft, obwohl in Wirklichkeit $p = 0{,}5$ ist.

- Der $\beta$-Fehler (ca. $26{,}3\%$):  
  Das ist die Wahrscheinlichkeit, dass der Test bei der Nullhypothese
  $H_0: p = 0{,}5$ bleibt, also nicht verwirft,
  obwohl in Wirklichkeit $p = 0{,}8$ ist.

********************









#  Stochastik - Aufgabe 7: 



Gegeben ist eine Zufallsvariable $X$ mit $X \sim B(n = 20, p)$.

Es soll überprüft werden, ob die Erfolgswahrscheinlichkeit $p$ eher
„normal“ ($p = 0{,}2$) oder „leicht erhöht“ ($p = 0{,}3$) ist.

Es wird folgender Test verwendet (Entscheidungsregel):

> Wenn in den $20$ Versuchen mindestens $6$ Erfolge auftreten ($X \ge 6$),
> dann wird die Nullhypothese verworfen.  
> Sonst ($X \le 5$) wird die Nullhypothese beibehalten.

---

__$a)\;\;$__ **Formuliere** die Nullhypothese $H_0$ und die Gegenhypothese (alternative Hypothese) $H_1$.

[[!]]
<script>true</script>
********************

Es werden zwei feste Werte für $p$ verglichen:

- Nullhypothese:  
  $H_0:\; p = 0{,}2$

- Gegenhypothese:  
  $H_1:\; p = 0{,}3$

********************

__$b)\;\;$__ **Bestimme** den $\alpha$-Fehler dieses Tests.  
Das ist die Wahrscheinlichkeit, dass $H_0$ verworfen wird, obwohl in Wirklichkeit $p = 0{,}2$ gilt.

$\alpha \approx $ [[ 19,58 ]]$\,\%$
@Algebrite.check2(19.58,0.01)
********************

Der $\alpha$-Fehler ist
$\alpha = P(X \ge 6 \mid p = 0{,}2)$.

Bequemer ist die Rechnung über das Komplement:
$\alpha = 1 - P(X \le 5 \mid p = 0{,}2)$.

Mit $X \sim B(20, 0{,}2)$ gilt allgemein
$P(X = k) = \binom{20}{k} \cdot 0{,}2^k \cdot 0{,}8^{20-k}$.

Also
$P(X \le 5) = \displaystyle\sum_{k=0}^{5} \binom{20}{k} \cdot 0{,}2^k \cdot 0{,}8^{20-k}$

und damit
$\alpha = 1 - \displaystyle\sum_{k=0}^{5} \binom{20}{k} \cdot 0{,}2^k \cdot 0{,}8^{20-k} \approx 0{,}1958$.

In Prozent: $\alpha \approx 19{,}58\%$.

********************

__$c)\;\;$__ **Bestimme** den $\beta$-Fehler dieses Tests.  
Das ist die Wahrscheinlichkeit, dass $H_0$ nicht verworfen wird, obwohl in Wirklichkeit $p = 0{,}3$ gilt.

$\beta \approx $ [[ 41,64 ]]$\,\%$
@Algebrite.check2(41.64,0.01)
********************

Jetzt gilt $X \sim B(20, 0{,}3)$.

Der $\beta$-Fehler ist
$\beta = P(X \le 5 \mid p = 0{,}3)$,

denn dann wird $H_0$ beibehalten.

Wir berechnen
$\beta = \displaystyle\sum_{k=0}^{5} \binom{20}{k} \cdot 0{,}3^k \cdot 0{,}7^{20-k}$

und erhalten näherungsweise
$\beta \approx 0{,}4164$.

In Prozent: $\beta \approx 41{,}64\%$.

********************

__$d)\;\;$__ **Erkläre** in eigenen Worten, was $\alpha$- und $\beta$-Fehler in dieser Situation bedeuten.

[[!]]
<script>true</script>
********************

- Der $\alpha$-Fehler (ca. $19{,}58\%$):  
  Das ist die Wahrscheinlichkeit, dass der Test $H_0$ verwirft und sich
  für $p = 0{,}3$ entscheidet, obwohl in Wirklichkeit $p = 0{,}2$ ist.

- Der $\beta$-Fehler (ca. $41{,}64\%$):  
  Das ist die Wahrscheinlichkeit, dass der Test $H_0$ beibehält
  (also $p = 0{,}2$ nicht verwirft),  
  obwohl in Wirklichkeit $p = 0{,}3$ ist.

********************





