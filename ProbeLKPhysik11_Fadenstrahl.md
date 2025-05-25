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

# Probeleistungskontrolle für Physik - Klasse 11: Ionen in elektrischen und magnetischen Feldern

> Letztes Update: 25.05.2025 gegen 16:00 Uhr \

Swipe (Wische) entweder weiter oder klicke unten links auf neben der Seitenzahl auf den Pfeil nach rechts. \


Diese Probearbeit hat mehr Aufgaben als die richtige Arbeit, damit du genug zum Üben hast. Es sind viele verschiedene Aufgabentypen abgebildet, sodass du alles nochmal bei der Bearbeitung dieser Aufgaben wiederholst. Die Aufgaben sind in vielen Bereichen schwerer als die Aufgaben in der Leistungskontrolle. Diese Aufgaben dienen zur Vorbereitung. \

Die Aufgaben bauen aufeinander auf. Vorherige Rechnungen und Werte können auf die folgenden Aufgaben übertragen werden. \



## Aufgabe 1



__$a)\;\;$__ **Skizzieren** Sie eine Versuchsanordnung zur Massenspektroskopie von Gasen und **beschriften** Sie diese vollständig. \




[[!]]
<script>true</script>
************

Das Rendern der Lösung kann eine kurze Zeit dauern. \

<center>

```latex  @tikz
\begin{tikzpicture}[scale=1.75,>=latex]       

  
  
    \shade[left color=blue!25!white,right color=blue!25!white,opacity=1] (5.5,-2.5) -- (5.5,2.5) -- (6.5,2.5) -- (6.5,-2.5) -- (5.5,-2.5)    ;
    \coordinate[label=center:\Huge$\otimes$] (a4) at (6,2);
    \coordinate[label=center:\Huge$\otimes$] (a5) at (6,-2);
  
  \draw[ thick] (0.125,-0)  ellipse (0.05 and 0.05)  node[left] {$$}   ;
  \draw[ thick] (0.125,-0.2)  ellipse (0.05 and 0.05)  node[left] {$U_H$}   ;
  
  \draw (0.125,0) -- (0.125,0.5) -- (1,0.5) -- (1,0.25) -- (2,0.25) ; 
  \draw  (2,-0.25) -- (1,-0.25) -- (1,-0.7) -- (0.125,-0.7) -- (0.125,-0.2) ;
  
   \draw (2,0.25) arc (90:-90:0.05)  arc (90:-90:0.05)  arc (90:-90:0.05)  arc (90:-90:0.05)  arc (90:-90:0.05) node[below, black] {Heizspule} ;
   
  
  % to [R, l=$R_s$] (3,4) ;
  % to [C, l=$R_s$] (3,4) ;
  
  
  \draw[ thick,black!50 ] (1.75,0.5)--(3.25,0.5)  node[midway, above, black] {}   ;
  \draw[ thick,black!50 ] (1.75,-0.5)--(3.25,-0.5)  node[midway, below, black] {Wehnelt-Zylinder}   ;
  \draw[ thick,black!50 ] (1.75,0) ellipse (0.125 and 0.5)  node[left] {$$}   ;
  \draw[ thick,black!50 ] (3.25,0) ellipse (0.125 and 0.5)  node[left] {$$}   ;
   
  \draw (2.5,-0.5) -- (2.5,-1.5) node[below] {$-$}  ; 
  
  
  
  
  \draw[ thick] (2,1.625) ellipse (0.05 and 0.05)  node[left] {$$}   ;
  \draw[ thick] (2.2,1.625) ellipse (0.05 and 0.05)  node[above] {$U_B$}   ;
  
  \draw (0.5,0.5)--(0.5,1.625)--(2,1.625);
  \draw (4.15,0.5)--(4.15,1.625)--(2.2,1.625);
  
  \draw[ thick,black!50 ] (4,0.5)--(4.3,0.5)  node[midway, above, black] {}   ;
  \draw[ thick,black!50 ] (4,-0.5)--(4.3,-0.5)  node[midway, below, black] {Ringanode}   ;
  \draw[ thick,black!50 ] (4,0) ellipse (0.125 and 0.5)  node[left] {$$}   ;
  \draw[ thick,black!50 ] (4.3,0) ellipse (0.125 and 0.5)  node[left] {$$}   ;
  
  
  \draw (6,0.5)--(6,1) node[above] {$+$};
  \draw (6,-0.5)--(6,-1) node[below] {$U_A \;\; -$};
  \draw[thick] (5.5,0.5)--(6.5,0.5);
  \draw[thick] (5.5,-0.5)--(6.5,-0.5) node[midway, below, black] {Geschwindigkeitsfilter};
  
  \draw[red,->, thin, densely dashed] (5.6,0.5)--(5.6,-0.5);
  \draw[red,->, thin, densely dashed] (5.7,0.5)--(5.7,-0.5);
  \draw[red,->, thin, densely dashed] (5.8,0.5)--(5.8,-0.5);
  \draw[red,->, thin, densely dashed] (5.9,0.5)--(5.9,-0.5);
  \draw[red,->, thin, densely dashed] (6.0,0.5)--(6.0,-0.5);
  \draw[red,->, thin, densely dashed] (6.1,0.5)--(6.1,-0.5);
  \draw[red,->, thin, densely dashed] (6.2,0.5)--(6.2,-0.5);
  \draw[red,->, thin, densely dashed] (6.3,0.5)--(6.3,-0.5);
  \draw[red,->, thin, densely dashed] (6.4,0.5)--(6.4,-0.5);
  
   
  
    \shade[left color=blue!25!white,right color=blue!25!white,opacity=1] (7,-2.5) -- (7,2.5) -- (11,2.5) -- (11,-2.5) -- (7,-2.5)    ; 
    \shade[left color=red!66!white,right color=red!66!white,opacity=1] (7,0.2) -- (7,2.5) -- (7.1,2.5) -- (7.1,0.2) -- (7,0.2)    ; 
    \shade[left color=red!66!white,right color=red!66!white,opacity=1] (7,-0.2) -- (7,-2.5) -- (7.1,-2.5) node[midway, below, black] {Photoplatte} -- (7.1,-0.2) -- (7,-0.2)    ; 
  
    \coordinate[label=center:\Huge$\otimes$] (a) at (7.75,1);
    \coordinate[label=center:\Huge$\otimes$] (b) at (7.75,-1);
    \coordinate[label=center:\Huge$\otimes$] (c) at (9.75,1);
    \coordinate[label=center:\Huge$\otimes$] (d) at (9.75,-1);
  
  \draw[ultra thick] (7,2.5)--(7,0.2);
  \draw[ultra thick] (7,-2.5)--(7,-0.2);
  
  
  \draw[ultra thick, blue] (3.2,0)--(7,0)  ; 
  \draw[->,thick,blue!100,rotate=90 ] (0,-7)   arc (360:180:1.2cm and 1.2cm)    node[midway,right] {$1.$}   ;
  \draw[->,thick,blue!100,rotate=90 ] (0,-7)   arc (360:180:0.8cm and 0.8cm)    node[above right] {$2.$}   ;
  
  
    \shade[left color=green!44!white,right color=green!44!white,opacity=1] (2.25,-0.35) -- (2.25,0.35) -- (3,0.35) -- (3,-0.35) -- (2.25,-0.35)    ; 
    \coordinate[label=center:Gas] (gas) at (2.6,0);
  


\end{tikzpicture}
```

</center>

************




__$b)\;\;$__ Mit einer Zink-Hall-Sonde wurde eine Hall-Spannung von $7\,\mu$V gemessen. Die Hall-Sonde hat eine Dicke von $12\,\mu$m und eine Betriebsstromstärke von $2,29\,$A. **Berechnen** Sie die Stärke des Magnetfeldes $B$.  \


<!-- data-solution-button="3" -->
$B \approx$ [[  0,573144  ]] T
@Algebrite.check2(0.573144,0.001)
***********
$$
\begin{align*}
  U_H & = R_H \dfrac{B I}{ d} \quad \left| \cdot \dfrac{d}{ I R_H}  \right. \\
  B & =  \dfrac{d U_H}{I R_H}   \\
  B & =  \dfrac{12 \cdot 10^{-6}\, \text{m}  \cdot 7 \cdot 10^{-6}\, \text{V} }{2,29\,\text{A} \cdot 6,4 \cdot 10^{-11}\, \dfrac{\text{m}^3}{\text{C}}  } \\
  B & \approx  0,573144\, \text{T}  \\
\end{align*}
$$

***********


__$c)\;\;$__ In das Massenspektrometer wurde eine unbekannte Substanz durch eingespeißt. Die Substanz wurde durch Verdampfungsprozesse in ihre molekularen Bestandteile zerlegt und in der Versuchsanordnung mit einer Elementarladung negativ ionisiert. **Berechnen** Sie die Geschwindigkeit, die bei einer Ablenkspannung von $2250\,$V, im Kondensator mit dem Plattenabstand von $d=4\,$cm, erreicht werden muss.



<!-- data-solution-button="3" -->
$v \approx$ [[  98142,857143  ]] $\dfrac{\text{m}}{\text{s}}$
@Algebrite.check2(98142.857143,0.01)
***********
$$
\begin{align*}
  F_L & = F_{el} \\
  qvB & = qE  \quad \left| : q  \right.  \\
  vB & = E  \quad \left| : B  \right.  \\
  v & = \frac{E}{B} \\
  v & = \frac{U_A}{d B} \\ 
  v & = \frac{2250\, \text{V}}{0,04\, \text{m} \cdot 0,573144\, \text{T}} \\  
  v & \approx 98142,857143\,\frac{\text{m}}{\text{s}} \\  
\end{align*}
$$

***********






__$d)\;\;$__ Im folgenden Bild sind die Messungen der Massenspektroskopie zu erkennen. Dabei wurden die Radien des Signals auf eine Photoplatte aufgetragen. **Bestimmen** Sie die Radien durch eine geeignete Messung. (Hier gilt: $r_1 < r_2 < r_3 < r_4$.)


![Messungen](https://bildung-bedeutet-freiheit.de/Messung.jpg)

<!-- data-solution-button="3" -->
$r_1 \approx$ [[ 1,8323 ]] cm 
@Algebrite.check2(1.8323,0.06)

<!-- data-solution-button="3" -->
$r_2 \approx$ [[ 4,0632 ]] cm
@Algebrite.check2(4.0632,0.06)

<!-- data-solution-button="3" -->
$r_3 \approx$ [[ 4,4760 ]] cm
@Algebrite.check2(4.4760,0.06)

<!-- data-solution-button="3" -->
$r_4 \approx$ [[ 4,6854 ]] cm
@Algebrite.check2(4.6854,0.06)




__$e)\;\;$__ Jeder Bereich der ein Molekül darstellt wurde ausgezählt und somit die prozentuale Zusammensatzung der Substanz bestimmt. Die Ergebnisse wurden in einem Säulendiagramm visualisiert. **Ordnen** Sie den ermittelten Radien aus Aufgabe 4 die Moleküle im folgenden Säulendiagramm **zu** und **begründen** Sie diese Zuordnung kurz.


![Messungen](https://bildung-bedeutet-freiheit.de/Messung2.jpg)

<!-- data-solution-button="3" -->
$r_1:$ [[($H_2O$)|$C_2H_5_OH$|$CO_2$|$Ar$]] \
$r_2:$ [[$H_2O$|$C_2H_5_OH$|$CO_2$|($Ar$)]] \
$r_3:$ [[$H_2O$|$C_2H_5_OH$|($CO_2$)|$Ar$]] \
$r_4:$ [[$H_2O$|($C_2H_5_OH$)|$CO_2$|$Ar$]] \


[[!]]
<script>true</script>
***********
 An der Dichte der Punkte auf der Photoplatte kann die relative Häufigkeit erkannt werden. Auch kann erkannt werden, dass massereichere Moleküle einen größeren Radius beschreiben.
***********



__$f)\;\;$__ **Bestimmen** Sie mit dem Periodensystem im Tafelwerk die Massen der Moleküle aus Aufgabenteil $e)$.

<!-- data-solution-button="3" -->
$m_1 \approx$ [[ 29,9146 ]] $\cdot 10^{-27}$kg 
@Algebrite.check2(29.9146,0.05)
***********
 $ 1,66054 \cdot  10^{-27} \,\text{kg} \cdot (15,999 +2 \cdot 1,008) \approx 29,9146 \cdot  10^{-27} \,\text{kg} $
***********

<!-- data-solution-button="3" -->
$m_2 \approx$ [[ 66,3386 ]] $\cdot 10^{-27}$kg 
@Algebrite.check2(66.3386,0.05)
***********
 $ 1,66054 \cdot  10^{-27} \,\text{kg} \cdot 39,95 \approx 66,3386\cdot  10^{-27} \,\text{kg} $
***********

<!-- data-solution-button="3" -->
$m_1 \approx$ [[ 73,077 ]] $\cdot 10^{-27}$kg 
@Algebrite.check2(73.077,0.05)
***********
 $ 1,66054 \cdot  10^{-27} \,\text{kg} \cdot (2 \cdot 15,999 + 12,01) \approx 73,077 \cdot  10^{-27} \,\text{kg} $
***********

<!-- data-solution-button="3" -->
$m_1 \approx$ [[ 76,4961 ]] $\cdot 10^{-27}$kg 
@Algebrite.check2(76.4961,0.05)
***********
 $ 1,66054 \cdot  10^{-27} \,\text{kg} \cdot (15,999 +2 \cdot 12,01 + 6 \cdot 1,008) \approx 76,4961 \cdot  10^{-27} \,\text{kg} $
***********



__$g)\;\;$__ **Zeigen** Sie durch die Berechnung der zu erwartenden Radien bei einfach negativ ionisierten Molekülen, dass Ihre Messungen Aufgabe $d)$ nicht stimmen.



<!-- data-solution-button="3" -->
$r_1 \approx$ [[ 3,1971 ]] cm 
@Algebrite.check2(3.1971,0.001)
***********
$$
\begin{align*}
  F_L & = F_{Z} \\
  qvB & = \frac{m_1 v^2}{r_1}  \quad \left| \cdot r  \right.  \\
  qvB r_1 & =  m_1 v^2   \quad \left| : qvB  \right.  \\
  r_1 & =  \frac{m_1 v^2}{qvB }      \\
  r_1 & =  \frac{m_1 v}{qB}      \\
  r_1 & =  \frac{ 29,9146 \cdot  10^{-27} \,\text{kg} \cdot  98142,857143\,\frac{\text{m}}{\text{s}} }{1,6022 \cdot 10^{-19}\, \text{C} \cdot 0,573144\, \text{T}}      \\
  r_1 & \approx  3,1971 \,\text{cm}       \\
\end{align*}
$$
***********

<!-- data-solution-button="3" -->
$r_2 \approx$ [[ 7,08997 ]] cm
@Algebrite.check2(7.08997,0.001)
***********
$$
\begin{align*}
  F_L & = F_{Z} \\
  qvB & = \frac{m_2 v^2}{r_2}  \quad \left| \cdot r  \right.  \\
  qvB r_2 & =  m_2 v^2   \quad \left| : qvB  \right.  \\
  r_2 & =  \frac{m_2 v^2}{qvB }      \\
  r_2 & =  \frac{m_2 v}{qB}      \\
  r_2 & =  \frac{ 66,3386\cdot  10^{-27} \,\text{kg} \cdot  98142,857143\,\frac{\text{m}}{\text{s}} }{1,6022 \cdot 10^{-19}\, \text{C} \cdot 0,573144\, \text{T}}      \\
  r_2 & \approx 7,08997  \,\text{cm}       \\
\end{align*}
$$
***********

<!-- data-solution-button="3" -->
$r_3 \approx$ [[ 7,8101 ]] cm
@Algebrite.check2(7.8101,0.001)
***********
$$
\begin{align*}
  F_L & = F_{Z} \\
  qvB & = \frac{m_3 v^2}{r_3}  \quad \left| \cdot r  \right.  \\
  qvB r_3 & =  m_3 v^2   \quad \left| : qvB  \right.  \\
  r_3 & =  \frac{m_3 v^2}{qvB }      \\
  r_3 & =  \frac{m_3 v}{qB}      \\
  r_3 & =  \frac{ 73,077 \cdot  10^{-27} \,\text{kg} \cdot  98142,857143\,\frac{\text{m}}{\text{s}} }{1,6022 \cdot 10^{-19}\, \text{C} \cdot 0,573144\, \text{T}}      \\
  r_3 & \approx  7,8101 \,\text{cm}       \\
\end{align*}
$$
***********

<!-- data-solution-button="3" -->
$r_4 \approx$ [[ 8,1756 ]] cm
@Algebrite.check2(8.1756,0.001)
***********
$$
\begin{align*}
  F_L & = F_{Z} \\
  qvB & = \frac{m_4 v^2}{r_4}  \quad \left| \cdot r  \right.  \\
  qvB r_4 & =  m_4 v^2   \quad \left| : qvB  \right.  \\
  r_4 & =  \frac{m_4 v^2}{qvB }      \\
  r_4 & =  \frac{m_4 v}{qB}      \\
  r_4 & =  \frac{ 76,4961 \cdot  10^{-27} \,\text{kg} \cdot  98142,857143\,\frac{\text{m}}{\text{s}} }{1,6022 \cdot 10^{-19}\, \text{C} \cdot 0,573144\, \text{T}}      \\
  r_4 & \approx  8,1756 \,\text{cm}       \\
\end{align*}
$$
***********

__$h)\;\;$__ **Berechnen** Sie für die einzelnen Moleküle die benötigten Beschleunigungsspannungen. \




<!-- data-solution-button="3" -->
$U_{B,1} \approx$ [[ 899,194974 ]] V
@Algebrite.check2(899.194974,0.003)
***********
$$
\begin{align*}
  E_{el} & = E_{kin} \\
  U_{B,1} e & = \frac{1}{2} m_1 v^2 \quad \left| : e  \right.   \\
  U_{B,1}  & = \frac{m_1 v^2}{2 e}  \\
  U_{B,1}  & = \frac{29,9146 \cdot  10^{-27} \,\text{kg} \left( 98142,857143\,\frac{\text{m}}{\text{s}} \right)^2}{2 \cdot 1,6022 \cdot 10^{-19}\, \text{C}}  \\
  U_{B,1} & \approx  899,194974 \,\text{V}       \\
\end{align*}
$$
***********



<!-- data-solution-button="3" -->
$U_{B,2} \approx$ [[ 1994,054266 ]] V
@Algebrite.check2(1994.054266,0.003)
***********
$$
\begin{align*}
  E_{el} & = E_{kin} \\
  U_{B,2} e & = \frac{1}{2} m_2 v^2 \quad \left| : e  \right.   \\
  U_{B,2}  & = \frac{m_2 v^2}{2 e}  \\
  U_{B,2}  & = \frac{66,3386 \cdot  10^{-27} \,\text{kg} \left( 98142,857143\,\frac{\text{m}}{\text{s}} \right)^2}{2 \cdot 1,6022 \cdot 10^{-19}\, \text{C}}  \\
  U_{B,2} & \approx  1994,054266 \,\text{V}       \\
\end{align*}
$$
***********



<!-- data-solution-button="3" -->
$U_{B,3} \approx$ [[ 2196,602033 ]] V
@Algebrite.check2(2196.602033,0.003)
***********
$$
\begin{align*}
  E_{el} & = E_{kin} \\
  U_{B,3} e & = \frac{1}{2} m_3 v^2 \quad \left| : e  \right.   \\
  U_{B,3}  & = \frac{m_3 v^2}{2 e}  \\
  U_{B,3}  & = \frac{73,077 \cdot  10^{-27} \,\text{kg} \left( 98142,857143\,\frac{\text{m}}{\text{s}} \right)^2}{2 \cdot 1,6022 \cdot 10^{-19}\, \text{C}}  \\
  U_{B,3} & \approx  2196,602033 \,\text{V}       \\
\end{align*}
$$
***********



<!-- data-solution-button="3" -->
$U_{B,4} \approx$ [[ 2299,375847 ]] V
@Algebrite.check2(2299.375847,0.003)
***********
$$
\begin{align*}
  E_{el} & = E_{kin} \\
  U_{B,4} e & = \frac{1}{2} m_4 v^2 \quad \left| : e  \right.   \\
  U_{B,4}  & = \frac{m_4 v^2}{2 e}  \\
  U_{B,4}  & = \frac{76,4961 \cdot  10^{-27} \,\text{kg} \left( 98142,857143\,\frac{\text{m}}{\text{s}} \right)^2}{2 \cdot 1,6022 \cdot 10^{-19}\, \text{C}}  \\
  U_{B,4} & \approx  2299,375847 \,\text{V}       \\
\end{align*}
$$
***********