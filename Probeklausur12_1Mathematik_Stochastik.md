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

# Probeklausur für Mathematik - Klasse 12: Stochastik

<br>

Swipe (Wische) entweder weiter oder klicke unten links auf neben der Seitenzahl auf den Pfeil nach rechts.

<br>

Diese Probearbeit hat mehr Aufgaben als die richtige Arbeit, damit du genug zum Üben hast. Es sind viele verschiedene Aufgabentypen abgebildet, sodass du alles nochmal bei der Bearbeitung dieser Aufgaben wiederholst.


## Aufgaben - HMF - Analysis



**Aufgabe 1:**



**1.1** Es ist jeweils genau eine Lösung richtig. Kreuzen Sie diese an.

Der Graph der Funktion $h$ mit $h(x)=x^2+e^x$ und $x \in \mathbb{R}$ verläuft durch den Punkt

<!-- data-randomize="true"  -->
- [[ ]] $(2|4+e)$. 
- [[X]] $(0|1)$. 
- [[ ]] $(1|0)$. 


Der Graph von $h$ hat an der Stelle $1$ eine Steigung von

<!-- data-randomize="true"  -->
- [[ ]] $0$. 
- [[ ]] $1+e$. 
- [[X]] $2+e$. 






**1.2** Gegeben sind die Funktionen $f$ und $g$ mit $f(x) = e^x$ und $g(x)=e\ln(x)+e$. Zeigen Sie, dass die Funktionen an der Stelle $1$ den gleichen Funktionswert und ihre Graphen dort die gleiche Steigung haben.


[[!]]
<script>true</script>
***********
$$
\begin{align*}
  f(1) & = e  \\
  g(1) & = e \ln(1) + e = e  \\
  f'(x) & = e^x  \\
  g'(x) & = \dfrac{e}{x}  \\
  f'(1) & = e  \\
  g'(1) & = e  \\
\end{align*}
$$
***********


---

---


**Aufgabe 2:** 

Gegeben sei die Funktionenschar $f_k$ mit $f_k(x)=ke^{kx}-x^3$ und $k \in \mathbb{R}$.

**2.1** Bestimmen Sie den Parameter $k$ so, dass der zugehörige Graph durch den Punkt $P(0|1)$ verläuft.

<!-- data-solution-button="5" -->
$k = $ [[  1  ]] 
***********
$$
\begin{align*}
  f_k(0) = 1 \;\; \Rightarrow \;\; k e^{k \cdot 0} - 0^3 = 1 \;\; \Rightarrow \;\; k = 1
\end{align*}
$$
***********


**2.2** Berechnen Sie den Parameter $k$ so, dass $\int\limits_0^2 f_k(x)dx = e-5$.

<!-- data-solution-button="5" -->
$k =$ [[  1/2  ]]
@Algebrite.check(1/2)
***********
$$
\begin{align*}
  \int\limits_0^2 f_k(x)dx & = e-5 \\
  \int\limits_0^2 ke^{kx}-x^3 dx & = e-5 \\
  \left[ e^{kx}-\dfrac{1}{4} x^4 \right]_0^2   & = e-5 \\
  e^{2k}-4-1   & = e-5 \\
  e^{2k}   & = e  \\
   2k    & = 1  \\
    k    & = \dfrac{1}{2}  \\
\end{align*}
$$
***********








## Aufgaben - HMF - Analytische Geometrie




**Aufgabe 1:**


Gegeben sind die Geraden  
$ g : \vec{x} = \left(\begin{array}{c} 3 \\ -3 \\ 3 \end{array} \right) + r \cdot \left(\begin{array}{c} 3 \\ 0 \\ -1 \end{array} \right) $  mit  $r \in \mathbb{R}$ und $h : \vec{x} =\left( \begin{array}{c} 3 \\ -3 \\ 3 \end{array} \right) + s \cdot \left( \begin{array}{c} 1 \\ 0 \\ 3 \end{array} \right)$  mit $s \in \mathbb{R}$. \



**1.1** Geben Sie die Koordinaten des Schnittpunkts von $g$ und $h$ an.   \


<!-- data-solution-button="3" -->
$S \left( \right.$ [[  3  ]] $\left| \right.$ [[  -3 ]] $\left| \right.$ [[  3  ]] $\left. \right)$


**1.2** Zeigen Sie, dass $g$ und $h$ orthogonal zueinander verlaufen.   \


[[!]]
<script>true</script>
***********
$$
\begin{align*}
  \circ \left( \begin{array}{c} 1 \\ 0 \\ 3 \end{array} \right) = 3 -3 = 0
\end{align*}
$$
***********


**1.3** Die Ebene $E$ enthält die Geraden $g$ und $h$.  
Bestimmen Sie eine Gleichung von $E$ in Koordinatenform.  


[[!]]
<script>true</script>
***********
$\left(\begin{array}{c} 0 \\ 1 \\ 0 \end{array} \right)$ ist orthogonal zu $g$ und $h$. $S$ soll auf $E$ liegen, also gilt: \
$E: 0 x_1 + 1 x_2 + 0 x_3 = \left(\begin{array}{c} 3 \\ -3 \\ 3 \end{array} \right) \circ \left(\begin{array}{c} 0 \\ 1 \\ 0 \end{array} \right) = -3  $ \
$E: x_2 = -3  $
***********


---

---




**Aufgabe 2:**


Gegeben sind die Gerade $g$ und die Ebene $E$ durch  

$ g : \vec{x} = \left(\begin{array}{c} 1 \\ 1 \\ 4 \end{array} \right) + r \cdot \left(\begin{array}{c} 0 \\ -3 \\ -4 \end{array} \right) \quad\text{und}\quad E : 4x_2 - 3x_3 = 25. $


**2.1** In jeder Zeile ist genau eine Aussage richtig. Kreuzen Sie diese an.

Die Gerade $g$ ist parallel zur ...  

<!-- data-randomize="true"  -->
- [[ ]] $x_1x_2$-Ebene. 
- [[ ]] $x_1x_3$-Ebene. 
- [[X]] $x_2x_3$-Ebene.

Die Gerade $g$ hat zur $x_2x_3$-Ebene den Abstand ...  

<!-- data-randomize="true"  -->
- [[ ]] $0$. 
- [[X]] $1$. 
- [[ ]] $4$.



Die Gerade $g$ ...  

<!-- data-randomize="true"  -->
- [[ ]] verläuft orthogonal zu $E$.  
- [[X]] verläuft echt parallel zu $E$. 
- [[ ]] liegt in $E$.
 


**2.2** Berechnen Sie den Abstand der Ebene $E$ vom Ursprung.  



<!-- data-solution-button="5" data-show-partial-solution -->
$d =$ [[  5  ]] $LE$
@Algebrite.check(5)
***********
$$
\begin{align*}
d = \left| \dfrac{-25}{\sqrt{4^2+3^2}} \right| = \dfrac{25}{5} = 5
\end{align*}
$$
***********




## Aufgaben - HMF - Stochastik


**Aufgabe 1:**

Ein Glücksrad mit drei gleich großen Sektoren ist mit den Ziffern $1$, $2$ und $3$ beschriftet. Das Glücksrad wird zweimal gedreht.

**1.1** Die Zufallsgröße $X$ gibt die Summe der beiden erzielten Zahlen an. Ergänzen Sie in der folgenden Tabelle die fehlenden Werte.

<!-- data-solution-button="5" data-show-partial-solution -->
|       |  |  |  |  |  |
| $k$      | $2$ | $3$ | $4$ | $5$ | $6$ |
| $P(X=k)$ | $\dfrac{1}{9}$ |  [[ 2/9 ]]  | $\dfrac{1}{3}$ | [[ 2/9 ]] | [[ 1/9 ]] |
@Algebrite.check(2/9;2/9;1/9)


**1.2** Betrachtet werden die Ereignisse $A$ und $B$:

• $A:$ "Es wird $(1;3)$, $(2;2)$ oder $(3;1)$ erzielt."

• $B:$ "Beim ersten Drehen wird eine $2$ erzielt."

Untersuchen Sie, ob $A$ und $B$ stochastisch unabhängig sind.




[[!]]
<script>true</script>
***********
 Wegen $P(A) \cdot P(B) = \dfrac{1}{3} \cdot  \dfrac{1}{3} =  \dfrac{1}{9} = P((2;2)) = P (A \cap B)$ sind $A$ und $B$ stochastisch unabhängig.
***********



---

---




**Aufgabe 2:**

Die Zufallsgrößen $X$ und $Y$ können jeweils die Werte $3$, $4$ und $5$ annehmen.

**2.1** Für die Zufallsgröße $X$ gilt: $P(X=3) = \dfrac{1}{3}, P(X=4) = \dfrac{1}{4}$. Bestimmen Sie den Erwartungswert von $X$.


<!-- data-solution-button="5" data-show-partial-solution -->
$E(X)=$ [[ 49/12 ]]
@Algebrite.check(49/12)
***********
 $P(X=5)  = 1 - \dfrac{1}{3} - \dfrac{1}{4} = \dfrac{5}{12} $

 $E(X) = \dfrac{1}{3} \cdot 3 +  \dfrac{1}{4} \cdot 4 +  \dfrac{5}{12} \cdot 5  = \dfrac{49}{12} $
***********


**2.2** Für die Zufallsgrößen $Y$ gilt: $P(Y=3) = \dfrac{1}{3}$, $P(Y=4) \geq \dfrac{1}{6}$ und  $P(Y=5) \geq \dfrac{1}{6}$. Bestimmen Sie alle Werte, die für den Erwartungswert von $Y$ infrage kommen. 


<!-- data-solution-button="5" data-show-partial-solution -->
 [[ 23/6 ]] $ \leq E(Y) \leq $ [[ 25/6 ]]
@Algebrite.check(23/6;25/6)
***********
Für $P(Y=5)  = \dfrac{3}{6}$ ist $ E(Y) = \dfrac{1}{3} \cdot +  \dfrac{1}{6} \cdot 4 +  \dfrac{3}{6} \cdot 5  = \dfrac{25}{6} $

Für $P(Y=5)  = \dfrac{1}{6}$ ist $ E(Y) = \dfrac{1}{3} \cdot +  \dfrac{3}{6} \cdot 4 +  \dfrac{1}{6} \cdot 5  = \dfrac{23}{6} $

 $ \dfrac{23}{6} \leq E(Y) \leq \dfrac{25}{6} $
***********









## Aufgabe Stochastik

Ein bekannter Video-Streamingdienst bietet einen kostenpflichtigen Zugang zu Spielfilmen und
Serien an. Personen, die davon gegen Zahlung einer monatlichen Gebühr Gebrauch machen,
werden im Folgenden als Abonnenten bezeichnet. Sie haben sich entweder für das Spielfilmpaket
oder für das Komplettpaket entschieden, das neben den Spielfilmen auch noch Serien
enthält.


Unter den Abonnenten sind $70\%$ höchstens $40$ Jahre alt. Von diesen haben 80% das
Komplettpaket gewählt. Unter denjenigen Abonnenten, die älter als $40$ Jahre sind, haben
sich 50% für das Komplettpaket entschieden.

$a)\;\;$ Stellen Sie den Sachverhalt in einem beschrifteten Baumdiagramm dar. 


[[!]]
<script>true</script>
***********
$P(A) = 0{,}7 \quad\text{(höchstens 40 Jahre alt)}, \qquad P(\overline{A}) = 0{,}3 \quad\text{(älter als 40 Jahre)}$ \
$B:$ Ein Abonnent hat das Komplettpaket. \


<!-- style="width:500px" -->
![](Baumprobe.png)
***********



---

---




$b)\;\;$ Eine unter allen Abonnenten zufällig ausgewählte Person hat sich für das Komplettpaket
entschieden.
Bestimmen Sie die Wahrscheinlichkeit dafür, dass sie höchstens $40$ Jahre alt ist.  



<!-- data-solution-button="5" data-show-partial-solution -->
[[  5600/71  ]] $\%$
@Algebrite.check2(5600/71,0.01)
***********
$$
\begin{align*}
P(K) &= P(A \cap K) + P(\overline{A} \cap K)
     = 0{,}56 + 0{,}15
     = 0{,}71 \\
P(A \mid K) 
&= \dfrac{P(A \cap K)}{P(K)}
= \dfrac{0{,}56}{0{,}71}
= \dfrac{56}{71}
\approx 0{,}789 \quad (\approx 78{,}9\,\%)
\end{align*}
$$
***********




---

---



$c)\;\;$ Unter allen Abonnenten werden $250$ zufällig ausgewählt.
Berechnen Sie die Wahrscheinlichkeit dafür, dass

• weniger als $170$ Abonnenten höchstens $40$ Jahre alt sind;


<!-- data-solution-button="5" data-show-partial-solution -->
[[  22,2759  ]] $\%$
@Algebrite.check2(22.2759,0.01)
***********
$$
\begin{align*}
P(X < 170) = \sum_{k=0}^{169} \binom{250}{k} 0{,}7^k 0{,}3^{250-k}
\approx 0{,}222759
\end{align*}
$$
***********






• die Anzahl der Abonnenten, die höchstens $40$ Jahre alt sind, um maximal 10 von
ihrem Erwartungswert abweicht.


<!-- data-solution-button="5" data-show-partial-solution -->
[[  85,29744  ]] $\%$
@Algebrite.check2(85.29744,0.01)
***********
$$
\begin{align*}
\text{Bedingung: } &|X - 175| \le 10 \;\Longleftrightarrow\; 165 \le X \le 185  \\
P(165 \le X \le 185) &= \sum_{k=165}^{185} \binom{250}{k} 0{,}7^k 0{,}3^{250-k}
\approx 0{,}85297
\end{align*}
$$
***********
 



---

---


$d)\;\;$ Bestimmen Sie die Anzahl der Abonnenten, die man mindestens zufällig auswählen
müsste, damit unter ihnen mit einer Wahrscheinlichkeit von mindestens $99\%$ mehr als
20 Personen älter als $40$ Jahre sind. 




<!-- data-solution-button="5" data-show-partial-solution -->
[[  104  ]] 
@Algebrite.check(104)
***********

$Y$: Anzahl der Abonnenten, die älter als $40$ Jahre sind, $Y \sim \text{Bin}(n, q = 0{,}3)$. \

Gesucht ist die kleinste natürliche Zahl $n$ mit $P(Y > 20) \ge 0{,}99$. \

$$
\begin{align*}
P(Y > 20) &\ge 0{,}99 \quad\text{für}\quad n = 104,  \\
P(Y > 20) &\approx 0{,}9910 \quad\text{bei } n = 104,  \\
P(Y > 20) &\approx 0{,}9895 \quad\text{bei } n = 103 < 0{,}99.  \\
&\Rightarrow \text{Gesuchte Mindestanzahl: } n = 104.  \\
\end{align*}
$$
***********






---

---




Der Anteil der zufriedenen Abonnenten von derzeit $60\%$ soll gesteigert werden. Dazu
wird ein Algorithmus entwickelt, der jedem Abonnenten täglich individuell einen Spielfilm
vorschlägt. Als Basis für die Entscheidung über den dauerhaften Einsatz des Algorithmus
plant das Management einen Probebetrieb. Im Anschluss soll die Nullhypothese „Der Anteil
der zufriedenen Abonnenten beträgt höchstens $60\%$.“ mithilfe einer Stichprobe von $200$
zufällig ausgewählten Abonnenten auf einem Signifikanzniveau von $5\%$ getestet werden.

$f)\;\;$ Geben Sie an, welche Überlegung des Managements zur Wahl dieser Nullhypothese
geführt haben könnte.  


[[!]]
<script>true</script>
***********
Es soll möglichst vermieden werden, den Algorithmus dauerhaft ein-
zusetzen, obwohl der Einsatz des Algorithmus die Zufriedenheit unter den
Abonnenten nicht erhöht. 
***********



---

---


Für den beschriebenen Test ergibt sich ${132; 133; …; 200}$ als Ablehnungsbereich der
Nullhypothese.

$g)\;\;$ Zur Bestimmung der unteren Grenze dieses Ablehnungsbereichs wurden zunächst folgen-
de Lösungsschritte ausgeführt: \
• $Z$: Anzahl der zufriedenen Abonnenten in der Stichprobe \
• $P_{200;0{,}6}(Z \ge 132) \approx 0{,}047$ \

Begründen Sie, dass die beiden Lösungsschritte zur Bestimmung der unteren Grenze
nicht ausreichend sind, und ergänzen Sie diese geeignet.  




[[!]]
<script>true</script>
***********
Es könnte eine natürliche Zahl $k$ mit $k < 132$ geben, für die $P_{200;0{,}6}(Z \ge 131) > 0{,}05.$ gilt.
Mit $P_{200;0{,}6}(Z \ge 132) \approx 0{,}0475 < 0{,}05$ und $P_{200;0{,}6}(Z \ge 131) \approx 0{,}0639 > 0{,}05$ ist $132$ die untere Grenze des Ablehnungsbereichs.
***********




---

---



$h)\;\;$ Weisen Sie nach, dass die Wahrscheinlichkeit für einen Fehler zweiter Art bei diesem
Ablehnungsbereich der Nullhypothese mehr als $90\%$ betragen könnte. 




[[!]]
<script>true</script>
***********
Zum Beispiel für

$$
\begin{align*}
p_1 = 0{,}61
\end{align*}
$$

gilt:

$$
\begin{align*}
\beta(0{,}61) = P_{200;0{,}61}(Z \le 131)
= \sum_{k=0}^{131} \binom{200}{k} 0{,}61^k \cdot 0{,}39^{200-k}
\approx 0{,}917.
\end{align*}
$$


Damit ist

$$
\begin{align*}
\beta(0{,}61) \approx 91{,}7\,\% > 90\,\%.
\end{align*}
$$

Es könnte also durchaus sein, dass der tatsächliche Anteil zufriedener Abonnenten bereits
bei $p_1 = 0{,}61$ liegt, der Test mit dem oben angegebenen Ablehnungsbereich die
Nullhypothese $H_0$ jedoch in über $90\%$ der Fälle nicht verwirft. Die
Wahrscheinlichkeit für einen Fehler zweiter Art kann somit mehr als $90\,\%$ betragen.

***********






