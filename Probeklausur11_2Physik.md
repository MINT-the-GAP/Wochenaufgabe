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

import: https://raw.githubusercontent.com/LiaTemplates/Tikz-Jax/main/README.md
import: https://raw.githubusercontent.com/LiaTemplates/mermaid_template/0.1.4/README.md

script: https://cdn.jsdelivr.net/gh/LiaTemplates/Tikz-Jax@main/dist/index.js


-->

# Klausurähnliche Aufgaben zum Üben

> Letztes Update am 08.03.2025 gegen 18 Uhr

Swipe (Wische) entweder weiter oder klicke unten links neben der Seitenzahl auf den Pfeil nach rechts.

Diese Probearbeit hat mehr Aufgaben als die richtige Arbeit, damit du genug zum Üben hast. Es sind viele verschiedene Aufgabentypen abgebildet, sodass du alles nochmal bei der Bearbeitung dieser Aufgaben wiederholst.


## Aufgabe 1


__$a)\;\;$__ **Skizziere** den Aufbau des Millikanversuchs.


[[!]]
<script>true</script>
***************************
<center>

```latex  @tikz 


  
  \begin{tikzpicture}[scale=0.55,>=latex,rotate=270 ]
			\coordinate[label=above:$$] (A) at (0,2);
			\coordinate[label=above:$$] (B) at (0,10); 
			\coordinate[label=above:$$] (A4) at (1,6);
			\coordinate[label=above:$+$] (A5) at (1,5); 
			\coordinate[label=above:$+$] (A6) at (1,4);
			\coordinate[label=above:$+$] (A7) at (1,3);    
			\coordinate[label=above:$+$] (A14) at (1,7);
			\coordinate[label=above:$+$] (A15) at (1,8); 
			\coordinate[label=above:$+$] (A16) at (1,9); 
			\coordinate[label=above:$$] (D) at (1,2); 
			\coordinate[label=above:$$] (C) at (1,10);
			
      
			
			\coordinate[label=below:$$] (Ar) at (8,2);
			\coordinate[label=below:$$] (Br) at (8,10); 
			\coordinate[label=below:$ $] (A4r) at (7,6);
			\coordinate[label=below:$-$] (A5r) at (7,5); 
			\coordinate[label=below:$-$] (A6r) at (7,4);
			\coordinate[label=below:$-$] (A7r) at (7,3);   
			\coordinate[label=below:$-$] (A14r) at (7,7);
			\coordinate[label=below:$-$] (A15r) at (7,8); 
			\coordinate[label=below:$-$] (A16r) at (7,9); 
			\coordinate[label=below:$$] (Dr) at (7,2); 
			\coordinate[label=below:$$] (Cr) at (7,10);
			
		
\draw[black, very thick]  (A) --(B)  --(C)  --(D) --(A) ; 
\draw[black, very thick]  (Ar) --(Br)  --(Cr)  --(Dr) --(Ar) ; 
  

 


\draw[->,red,very thick] (A5)--(A5r) ;
\draw[->,red,very thick] (A6)--(A6r) ;
\draw[->,red,very thick] (A7)--(A7r) ;  
\draw[->,red,very thick] (A14)--(A14r) ;
\draw[->,red,very thick] (A15)--(A15r) ;
\draw[->,red,very thick] (A16)--(A16r) ; 
 

\draw[->,blue,ultra thick] (2.5,6) -- (1.5,6)   node[midway, right] {$F_{el}$}  ; 
\draw[->,blue,ultra thick] (3.5,6) -- (2.5,6)   node[midway, left] {$F_A$}  ; 
\draw[->,blue,ultra thick] (3.5,6) -- (5.5,6)   node[midway, right] {$F$}  ; 


\draw[fill=blue!15,very thick]   (3.5,6) circle (0.25);




	\end{tikzpicture}

```

</center>
***************************


__$b)\;\;$__ **Beschreibe** die Durchführung des Millikanversuchs.


[[!]]
<script>true</script>
***************************
Beim Millikanversuch werden in einen Kondensator mittels eines Zerstäubers kleine Öltropfen gebracht. Diese Öltröpfchen werden dann mithilfe einer Lichtquelle ionisiert. Durch den Kondensator wirkt eine elektrische Kraft auf die Öltropfen. Durch ein Mikroskop kann nun beobachtet werden mit welcher Geschwindigkeit die Öltröpfen langsam durch die Gravitation zu Boden sinken. Durch die Sinkgeschwindigkeit kann über ein Kräftegleichgewicht die Größe des Öltröpfchens berechnet werden. Wenn der Öltropfen schwebt, kann durch ein weiteres Kräftegleichgewicht die Ladung des Tropfen berechnet werden.
***************************


<br>
<br>
<br>
<br>
<br>
<br>
<br>





## Aufgabe 2


Ein Plattenkondensator ähnelt einem Würfel mit einer Kantenlänge von $2,3\,$cm. Zwischen den Platten befindet sich Paraffin. Am Kondensator wurde eine Spannung von $1,2\,$V gemessen.  \

<br>

__$a)\;\;$__ **Berechne** die Ladungen auf den Kondensator 


[[!]]
<script>true</script>
***************************
$Q = U \epsilon_0 \epsilon_r \dfrac{A}{d} \approx 5,621 \cdot 10^{-13}\,$C
***************************

<br>

__$b)\;\;$__ **Berechne** das elektrische Feld zwischen den Platten. **Gib** die Eigenschaften des elektrischen Feldes **an**. Runde auf drei Nachkommastellen. \


[[ 52,174 ]]$\,\frac{\text{V}}{\text{m}}$
***************************
$E = \dfrac{U}{d} \approx  52,174 \,\frac{\text{V}}{\text{m}}$ \
Es handelt sich um ein homogenes Feld.
***************************

<br>

__$c)\;\;$__ Eine negative frei bewegliche Testladung mit einer Ladung von $25000e$ befindet sich $14\,$mm weit entfernt von der negativ geladenen Platte des Kondensators. **Berechne** die resultierende Überführungsarbeit.

[[!]]
<script>true</script>
***************************
$q = 25000e \approx 4,006 \cdot 10^{-15}\,$C   \
$W = F x = qEx \approx 1,881 \cdot 10^{-15} \,$J
***************************



<br>
<br>
<br>
<br>
<br>
<br>
<br>





## Aufgabe 3

Vor einem Plattenkondensator mit einem Flächeninhalt von $5,4\,$cm$^2$ und einen Plattenabstand von $1,7\,$mm wurde ein Widerstand mit einer Querschnittsfläche von $3,7$mm$^2$ und einer Länge von $1,3\,$cm verbaut. Der Widerstand besteht aus Kohlenstoff $\left(\rho=3,5\, \dfrac{\Omega\text{mm}^2}{\text{m}}\right)$ und im Kondensator befindet sich Bernstein. 


<br>

__$a)\;\;$__ **Berechne** die Kapazität des Kondensators. 

[[!]]
<script>true</script>
***************************
$C =  \epsilon_0 \epsilon_r \dfrac{A}{d} \approx 7,875  \cdot 10^{-11}\,$F
***************************

<br>

__$b)\;\;$__ **Berechne** den Widerstandswert des Widerstands. 

[[!]]
<script>true</script>
***************************
$R = \rho \dfrac{l}{A} \approx 0,0123\,\Omega $
***************************



<br>

__$c)\;\;$__ **Berechne** die Halbwertszeit der gespeicherten Ladungen auf dem Kondensator in dieser Schaltung.

[[!]]
<script>true</script>
***************************
$\tau = RC = 9,684 \cdot 10^{-13}\,$s
***************************




<br>

__$d)\;\;$__ Der Kondensator wird gegen einen anderen mit der Kapazität von $470\mu F$ ausgetauscht. Der vorgeschaltete Widerstand hat einen Wert von $4,7k\Omega$. Die Spannung des vollgeladenen Kondensators beträgt $725\,$mV. **Berechne** nach welcher Zeit die Spannung nur noch $480\,$mV beträgt.

[[!]]
<script>true</script>
***************************
$$
\begin{align*}     
		U(t) & = U_0 e^{- \frac{1}{RC} t} \\
		\Rightarrow\;\; - RC \ln\left(\frac{U(t)}{U_0}\right) &= t \approx 0,911\,\text{s}
\end{align*} 
$$
***************************





<br>
<br>
<br>
<br>
<br>
<br>
<br>





## Aufgabe 4

Bearbeite alle Teilaufgaben zur Braun'schen Röhre.

__$a)\;\;$__ **Berechne** die Geschwindigkeit in $x$-Richtung der Elektronen für eine Beschleunigungsspannung $U_B=7,8kV$. 

[[!]]
<script>true</script>
***************************
$$
\begin{align*}     
	E_{kin} & = E_{el}  \\
	\dfrac{1}{2}m_e v^2 & = U_B e  \\
	v & = \sqrt{\dfrac{2 U_B e}{m_e}}  \\
	v & \approx 52382390,262 \,\dfrac{\text{m}}{\text{s}}  \\
\end{align*} 
$$
***************************


<br>

__$b)\;\;$__ **Berechne** die $y$-Ablenkung im homogenen elektrischen Feld des Kondensators mit $d=3,5mm$ mit der Ablenkspannung $U_A=125V$ mit einer Länge von $1,75cm$. 

[[!]]
<script>true</script>
***************************
$$
\begin{align*}     
	F = m_e a_y & = Ee = \dfrac{U_A}{d}e \quad \left| : m_e \right. \\
	        a_y & = \dfrac{U_A e}{d m_e} \\
	        t_s & = \dfrac{s}{v_x} \\
    \Rightarrow\;\; y & = \dfrac{1}{2} a_y t_s^2 \\
        y & = \dfrac{1}{2} \dfrac{U_A e}{d m_e} \dfrac{s^2}{v_x^2}  \\
        y & \approx 0,351\,\text{mm}
\end{align*} 
$$
***************************


<br>

__$c)\;\;$__ **Berechne** die $y$-Geschwindigkeit nach dem Kondensator. 


[[!]]
<script>true</script>
***************************
$$
\begin{align*}     
	v & = a_y t_s \\
	v & = \dfrac{U_A e}{d m_e} \dfrac{s}{v_x} \\
	v & \approx  2098653,456  \,\dfrac{\text{m}}{\text{s}}  \\
\end{align*} 
$$
***************************


<br>

__$d)\;\;$__ **Berechne** die gesamte $y$-Ablenkung, wenn nach dem Kondensator eine freie Flugstrecke von $5\,$cm vorzufinden ist. 


[[!]]
<script>true</script>
***************************
$$
\begin{align*}     
	y_2 &= y_1 + y(t_l)  =  \frac{1}{2}  \frac{U_A e}{d m_e} \left( \frac{s}{v_{x,0}} \right)^2   + \frac{U_A e}{d m_e}  \frac{s}{v_{x,0}} \frac{l}{v_{x,0}} =  \frac{U_A e s}{d m_e v_{x,0}^2} \left( \frac{s}{2} + l \right) \\
  \Rightarrow\;\;  y_2 & =    \frac{s U_A}{2 d U_B}    \left( \frac{s}{2} + l \right) \;\; \\
    y_2 & \approx 0,094\,\text{mm}
\end{align*} 
$$
***************************

<br>
<br>
<br>
<br>
<br>
<br>
<br>
