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

# Probeleistungskontrolle für Physik - Klasse 9: Kinematik

<br>

> Letztes Update wurde am 18.04.2025 um 19:28 Uhr hochgeladen.

<br>

Swipe (Wische) entweder weiter oder klicke unten links auf neben der Seitenzahl auf den Pfeil nach rechts.

<br>

Diese Probearbeit hat mehr Aufgaben als die richtige Arbeit, damit du genug zum Üben hast. Es sind viele verschiedene Aufgabentypen abgebildet, sodass du alles nochmal bei der Bearbeitung dieser Aufgaben wiederholst.

<br>
<br>
<br>
<br>
<br>
<br>
<br>
 

## Aufgabe 1

Im folgenden Koordinatensystem wurden die Bewegungen von einigen Objekten darstellt. **Beantworte** die Teilaufgaben. (Das Rendern des Bildes kann einige Zeit dauern, hab ein wenig Geduld.)


<center>

```latex  @tikz
\begin{tikzpicture}[scale=2,>=latex]       



\draw[black!70, step=5mm,   thin, dashed] (-0,-0) grid (8,8);  

\draw[black!70, step=10mm,   thin] (-0,-0) grid (8,8);

  \coordinate (ya) at (0,-0.25);
  \coordinate (xa) at (-0.25,0);
  \coordinate (o) at (0,0);



  \coordinate (y) at (0,8.25);
    \coordinate (x) at (8.25,0);
    \draw[<->, black!100, thick] (y) node[above] {$x(t)$ in $\left[m\right]$} -- (0,0) --  (x) node[right]
    {$t$ in $\left[s\right]$};

\draw[-, black!100, thin]  (0,0.1) -- (0,-0.1) node[below=0.25cm,left] {0};
\draw[-, black!100, thin]  (1,0.1) -- (1,-0.1) node[below] {1};
\draw[-, black!100, thin]  (2,0.1) -- (2,-0.1) node[below] {2};
\draw[-, black!100, thin]  (3,0.1) -- (3,-0.1) node[below] {3};
\draw[-, black!100, thin]  (4,0.1) -- (4,-0.1) node[below] {4};
\draw[-, black!100, thin]  (5,0.1) -- (5,-0.1) node[below] {5};
\draw[-, black!100, thin]  (6,0.1) -- (6,-0.1) node[below] {6};
\draw[-, black!100, thin]  (7,0.1) -- (7,-0.1) node[below] {7};
\draw[-, black!100, thin]  (8,0.1) -- (8,-0.1) node[below] {8};
\draw[-, black!100, thin]  (0.1,1) -- (-0.1,1) node[left] {1};
\draw[-, black!100, thin]  (0.1,2) -- (-0.1,2) node[left] {2};
\draw[-, black!100, thin]  (0.1,3) -- (-0.1,3) node[left] {3};
\draw[-, black!100, thin]  (0.1,4) -- (-0.1,4) node[left] {4};
\draw[-, black!100, thin]  (0.1,5) -- (-0.1,5) node[left] {5};
\draw[-, black!100, thin]  (0.1,6) -- (-0.1,6) node[left] {6};
\draw[-, black!100, thin]  (0.1,7) -- (-0.1,7) node[left] {7};
\draw[-, black!100, thin]  (0.1,8) -- (-0.1,8) node[left] {8};
 


 \draw [ black!100, thick]  (ya) --(o) --  (xa);

	\draw[ultra thick,color=black, ] plot[samples=100, domain=-0:2] (\x, {\x*\x/4 + 2 } ) node[right] {$$}; 
	\draw[ultra thick,color=black, ] plot[samples=100, domain=2:4] (\x, { \x + 1 } ) node[right] {$$}; 
	\draw[ultra thick,color=black, ] plot[samples=100, domain=4:5.5] (\x, { 5 } ) node[right] {$$}; 
	\draw[ultra thick,color=black, ] plot[samples=100, domain=5.5:8] (\x, { -1/4*(\x - 5.5)*(\x - 5.5) + 5 } ) node[right] {$A$}; 

	\draw[ultra thick,color=red, ] plot[samples=100, domain=-0:2] (\x, {-\x/3 + 7 } ) node[right] {$$}; 
	\draw[ultra thick,color=red, ] plot[samples=100, domain=2:4.5] (\x, {-\x*1.75 + 3.5 + 6.333333333333 } ) node[right] {$$}; 
	\draw[ultra thick,color=red, ] plot[samples=100, domain=4.5:8] (\x, {1/4*(\x - 4.5)*(\x - 4.5) + 2 } ) node[right] {$B$};   

	\draw[ultra thick,color=blue, ] plot[samples=100, domain=0:3] (\x, { \x*2.5   } ) node[right] {$$}; 
	\draw[ultra thick,color=blue, ] plot[samples=100, domain=3:4.5] (\x, {7.5 } ) node[right] {$$}; 
	\draw[ultra thick,color=blue, ] plot[samples=100, domain=4.5:8] (\x, {  -1/8*(\x - 4.5)*(\x - 4.5) + 7.5   } ) node[right]  {$C$};  

	\draw[ultra thick,color=purple, ] plot[samples=100, domain=0:6.6666] (\x, {  \x*\x/10+3.5 } ) node[above] {$D$};   

	\draw[ultra thick,color=gray, ] plot[samples=100, domain=0:6] (\x, {\x*7/6 + 1 } ) node[right] {$E$};  

	\draw[ultra thick,color=orange, ] plot[samples=100, domain=2.5:4] (\x, {\x*1.66666666 - 4.16666666666 } ) node[right] {$$};
	\draw[ultra thick,color=orange, ] plot[samples=100, domain=4:6] (\x, { 2.5 } ) node[right] {$$};
	\draw[ultra thick,color=orange, ] plot[samples=100, domain=6:8] (\x, { 1/2*(\x - 6)*(\x - 6) + 2.5 } ) node[right] {$F$};  

  

	\draw[ultra thick,color=green, ] plot[samples=100, domain=2:4] (\x, {\x*3/4 - 1.5 } ) node[right] {$$};  
	\draw[ultra thick,color=green, ] plot[samples=100, domain=4:5] (\x, {\x*4 - 14.5 } ) node[right] {$$};  
	\draw[ultra thick,color=green, ] plot[samples=100, domain=5:8] (\x, {\x*4/5 + 1.5 } ) node[right] {$G$};  
    
\end{tikzpicture}
```

</center>


__$a)\;\;$__ Wie lang macht das Objekt $A$ Pause? \
[[  1,5  ]] s



__$b)\;\;$__ Wie viele Sekunden liegen zwischen den Start der Bewegungen von Objekt $C$ und $F$? \
[[  2,5  ]] s



__$c)\;\;$__ Wie groß ist der größte Betrag der Geschwindigkeit von $B$? \
[[  1,75 ]] $\dfrac{\text{m}}{\text{s}}$



__$d)\;\;$__ Wenn die Objekte als Autos angesehen werden würden, mit welcher Geschwindigkeit relativ zur Straße würde dann das Auto $C$ das Auto $E$ überholen? \
[[  2,5  ]] $\dfrac{\text{m}}{\text{s}}$



__$e)\;\;$__ Wenn die Objekte als Autos angesehen werden würden, mit welcher Geschwindigkeit relativ zum Auto $B$ würde dann das Auto $A$ am Auto $B$ vorbeifahren? \
[[  2,75 ]] $\dfrac{\text{m}}{\text{s}}$



__$f)\;\;$__ Welches Objekt hat die größte Beschleunigung? \
[[   F   ]] 



__$g)\;\;$__ Wie groß ist die Beschleunigung von $B$ im letzten Segment? \
[[  0,5  ]] $\dfrac{\text{m}}{\text{s}^2}$


__$h)\;\;$__ Wie groß ist der größte Betrag der Geschwindigkeit von $G$? \
[[   4   ]] $\dfrac{\text{m}}{\text{s}}$


__$i)\;\;$__ Welche Geschwindigkeit besitzt das Objekt $F$ zum Zeitpunkt $t=7\,$s? \

[[   1   ]] $\dfrac{\text{m}}{\text{s}}$
[[?]] Skizziere eine Tangente an der Stelle der des Graphens. Die Tangente beschreibt die momentane Geschwindigkeit.



__$j)\;\;$__ Wie groß ist der Betrag der Beschleunigung von $C$ im letzten Segment? \
[[  0,25  ]] $\dfrac{\text{m}}{\text{s}^2}$



__$k)\;\;$__ Wie groß ist der Betrag der Beschleunigung von $D$? \
[[  0,2   ]] $\dfrac{\text{m}}{\text{s}^2}$



__$l)\;\;$__ Wie weit sind $G$ und $C$ bei $4\,$s von einander entfernt? \
[[   6   ]] $\text{m}$


<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

## Aufgabe 2


<center>

```latex  @tikz
\begin{tikzpicture}[scale=2,>=latex]       
 
\draw[black!70, step=5mm, very thin, dashed] (-0.5,-0.5) grid (10.5,10.5);  

\draw[black!70, step=10mm, very thin] (-0.5,-0.5) grid (10.5,10.5);

  \coordinate (ya) at (0,-0.75);
  \coordinate (xa) at (-0.75,0);
  \coordinate (o) at (0,0);

  \coordinate (y) at (0,10.75);
    \coordinate (x) at (10.75,0);
    \draw[<->, black!100, thick] (y) node[above] {$x$ in m} -- (0,0) --  (x) node[right]    {$t$ in s};

\draw[-, black!100, thin]  (0,0.1) -- (0,-0.1) node[below=0.25cm,left] {0};
\draw[-, black!100, thin]  (1,0.1) -- (1,-0.1) node[below] {1};
\draw[-, black!100, thin]  (2,0.1) -- (2,-0.1) node[below] {2};
\draw[-, black!100, thin]  (3,0.1) -- (3,-0.1) node[below] {3};
\draw[-, black!100, thin]  (4,0.1) -- (4,-0.1) node[below] {4};
\draw[-, black!100, thin]  (5,0.1) -- (5,-0.1) node[below] {5};
\draw[-, black!100, thin]  (6,0.1) -- (6,-0.1) node[below] {6};
\draw[-, black!100, thin]  (7,0.1) -- (7,-0.1) node[below] {7};
\draw[-, black!100, thin]  (8,0.1) -- (8,-0.1) node[below] {8};
\draw[-, black!100, thin]  (9,0.1) -- (9,-0.1) node[below] {9};
\draw[-, black!100, thin]  (10,0.1) -- (10,-0.1) node[below] {10};
\draw[-, black!100, thin]  (0.1,1) -- (-0.1,1) node[left] {10};
\draw[-, black!100, thin]  (0.1,2) -- (-0.1,2) node[left] {20};
\draw[-, black!100, thin]  (0.1,3) -- (-0.1,3) node[left] {30};
\draw[-, black!100, thin]  (0.1,4) -- (-0.1,4) node[left] {40};
\draw[-, black!100, thin]  (0.1,5) -- (-0.1,5) node[left] {50};
\draw[-, black!100, thin]  (0.1,6) -- (-0.1,6) node[left] {60};
\draw[-, black!100, thin]  (0.1,7) -- (-0.1,7) node[left] {70};
\draw[-, black!100, thin]  (0.1,8) -- (-0.1,8) node[left] {80};
\draw[-, black!100, thin]  (0.1,9) -- (-0.1,9) node[left] {90};
\draw[-, black!100, thin]  (0.1,10) -- (-0.1,10) node[left] {100};

\draw[-, black!100, thin]  (-1,0.1) -- (-1,-0.1) node[below] {};
\draw[-, black!100, thin]  (0.1,-1) -- (-0.1,-1) node[left] {};


 \draw [ black!100, thick]  (ya) --(o) --  (xa);


  \draw[thick,color=red, thick] plot[samples=50, domain=-0.0:10] (\x, \x*\x/10 ) node[right] {$x(t)$}; 

\end{tikzpicture}
```

</center>

<br>


**Bestimme** die durchschnittliche Geschwindigkeit der im Koordinatensystem dargestellten Bewegung zwischen $t=4,5\,$s und $t=10\,$s. \


$\Delta \bar{v} \approx$ [[  14,5  ]]  $\dfrac{\text{m}}{\text{s}}$
***********
$$
\begin{align*}
   \Delta \bar{v} & = \frac{\Delta \bar{x}}{\Delta \bar{t}} = \frac{79,75\,\text{m}}{5,5\,\text{s}} = 14,5\,\frac{\text{m}}{\text{s}}  \\
\end{align*}
$$

<center>

```latex  @tikz
\begin{tikzpicture}[scale=2,>=latex]       

\draw[black!70, step=5mm, very thin, dashed] (-0.5,-0.5) grid (10.5,10.5);  

\draw[black!70, step=10mm, very thin] (-0.5,-0.5) grid (10.5,10.5);

  \coordinate (ya) at (0,-0.75);
  \coordinate (xa) at (-0.75,0);
  \coordinate (o) at (0,0);

  \coordinate (y) at (0,10.75);
    \coordinate (x) at (10.75,0);
    \draw[<->, black!100, thick] (y) node[above] {$x$ in m} -- (0,0) --  (x) node[right]    {$t$ in s};

\draw[-, black!100, thin]  (0,0.1) -- (0,-0.1) node[below=0.25cm,left] {0};
\draw[-, black!100, thin]  (1,0.1) -- (1,-0.1) node[below] {1};
\draw[-, black!100, thin]  (2,0.1) -- (2,-0.1) node[below] {2};
\draw[-, black!100, thin]  (3,0.1) -- (3,-0.1) node[below] {3};
\draw[-, black!100, thin]  (4,0.1) -- (4,-0.1) node[below] {4};
\draw[-, black!100, thin]  (5,0.1) -- (5,-0.1) node[below] {5};
\draw[-, black!100, thin]  (6,0.1) -- (6,-0.1) node[below] {6};
\draw[-, black!100, thin]  (7,0.1) -- (7,-0.1) node[below] {7};
\draw[-, black!100, thin]  (8,0.1) -- (8,-0.1) node[below] {8};
\draw[-, black!100, thin]  (9,0.1) -- (9,-0.1) node[below] {9};
\draw[-, black!100, thin]  (10,0.1) -- (10,-0.1) node[below] {10};
\draw[-, black!100, thin]  (0.1,1) -- (-0.1,1) node[left] {10};
\draw[-, black!100, thin]  (0.1,2) -- (-0.1,2) node[left] {20};
\draw[-, black!100, thin]  (0.1,3) -- (-0.1,3) node[left] {30};
\draw[-, black!100, thin]  (0.1,4) -- (-0.1,4) node[left] {40};
\draw[-, black!100, thin]  (0.1,5) -- (-0.1,5) node[left] {50};
\draw[-, black!100, thin]  (0.1,6) -- (-0.1,6) node[left] {60};
\draw[-, black!100, thin]  (0.1,7) -- (-0.1,7) node[left] {70};
\draw[-, black!100, thin]  (0.1,8) -- (-0.1,8) node[left] {80};
\draw[-, black!100, thin]  (0.1,9) -- (-0.1,9) node[left] {90};
\draw[-, black!100, thin]  (0.1,10) -- (-0.1,10) node[left] {100};

\draw[-, black!100, thin]  (-1,0.1) -- (-1,-0.1) node[below] {};
\draw[-, black!100, thin]  (0.1,-1) -- (-0.1,-1) node[left] {};


 \draw [ black!100, thick]  (ya) --(o) --  (xa);


  \draw[thick,color=red] plot[samples=50, domain=-0.0:10] (\x, \x*\x/10 ) node[right] {$x(t)$}; 
	
  \draw[thick,color=blue] (4.5,2.025) -- (10,10) ; 
  \draw[thick,color=blue,dashed] (4.5,2.025) -- (4.5,10) node[midway, left] {$\bar{x}=79,75\,$m} -- (10,10) node[midway, above] {$\bar{t}=5,5\,$s}  ; 
 
 % \draw[thick,color=purple] plot[samples=50, domain=2:6.5] (\x, \x-2.5 ) node[right] {$$}; 
 % \draw[thick,color=purple,dashed] (3,0.5) -- (6,0.5) node[midway, below] {$t_5=3\,$s} -- (6,3.5) node[midway, right] {$x_5=30\,$m}  ; 
 
 % \draw[thick,color=olive] plot[samples=50, domain=6.5:10] (\x, 9/5*\x-8.125 ) node[right] {$$}; 
 % \draw[thick,color=olive,dashed] (7,4.5) -- (9.5,4.5) node[midway, below] {$t_9=2,5\,$s} -- (9.5,9) node[midway, right] {$x_9=45\,$m}  ; 

\end{tikzpicture}
```

</center>

***********


**Bestimme** anschließend die momentane Geschwindigkeiten bei $t=5\,$s. \


$v_5 \approx$ [[  10  ]] $\dfrac{\text{m}}{\text{s}}$
***********
$$
\begin{align*}
   v_5 & = \frac{\Delta x_5}{\Delta t_5} = \frac{30\,\text{m}}{3\,\text{s}} = 10\,\frac{\text{m}}{\text{s}}  \\
\end{align*}
$$

<center>

```latex  @tikz
\begin{tikzpicture}[scale=2,>=latex]       

\draw[black!70, step=5mm, very thin, dashed] (-0.5,-0.5) grid (10.5,10.5);  

\draw[black!70, step=10mm, very thin] (-0.5,-0.5) grid (10.5,10.5);

  \coordinate (ya) at (0,-0.75);
  \coordinate (xa) at (-0.75,0);
  \coordinate (o) at (0,0);

  \coordinate (y) at (0,10.75);
    \coordinate (x) at (10.75,0);
    \draw[<->, black!100, thick] (y) node[above] {$x$ in m} -- (0,0) --  (x) node[right]    {$t$ in s};

\draw[-, black!100, thin]  (0,0.1) -- (0,-0.1) node[below=0.25cm,left] {0};
\draw[-, black!100, thin]  (1,0.1) -- (1,-0.1) node[below] {1};
\draw[-, black!100, thin]  (2,0.1) -- (2,-0.1) node[below] {2};
\draw[-, black!100, thin]  (3,0.1) -- (3,-0.1) node[below] {3};
\draw[-, black!100, thin]  (4,0.1) -- (4,-0.1) node[below] {4};
\draw[-, black!100, thin]  (5,0.1) -- (5,-0.1) node[below] {5};
\draw[-, black!100, thin]  (6,0.1) -- (6,-0.1) node[below] {6};
\draw[-, black!100, thin]  (7,0.1) -- (7,-0.1) node[below] {7};
\draw[-, black!100, thin]  (8,0.1) -- (8,-0.1) node[below] {8};
\draw[-, black!100, thin]  (9,0.1) -- (9,-0.1) node[below] {9};
\draw[-, black!100, thin]  (10,0.1) -- (10,-0.1) node[below] {10};
\draw[-, black!100, thin]  (0.1,1) -- (-0.1,1) node[left] {10};
\draw[-, black!100, thin]  (0.1,2) -- (-0.1,2) node[left] {20};
\draw[-, black!100, thin]  (0.1,3) -- (-0.1,3) node[left] {30};
\draw[-, black!100, thin]  (0.1,4) -- (-0.1,4) node[left] {40};
\draw[-, black!100, thin]  (0.1,5) -- (-0.1,5) node[left] {50};
\draw[-, black!100, thin]  (0.1,6) -- (-0.1,6) node[left] {60};
\draw[-, black!100, thin]  (0.1,7) -- (-0.1,7) node[left] {70};
\draw[-, black!100, thin]  (0.1,8) -- (-0.1,8) node[left] {80};
\draw[-, black!100, thin]  (0.1,9) -- (-0.1,9) node[left] {90};
\draw[-, black!100, thin]  (0.1,10) -- (-0.1,10) node[left] {100};

\draw[-, black!100, thin]  (-1,0.1) -- (-1,-0.1) node[below] {};
\draw[-, black!100, thin]  (0.1,-1) -- (-0.1,-1) node[left] {};


 \draw [ black!100, thick]  (ya) --(o) --  (xa);


  \draw[thick,color=red] plot[samples=50, domain=-0.0:10] (\x, \x*\x/10 ) node[right] {$x(t)$}; 
	
 % \draw[thick,color=blue] (4.5,2.025) -- (10,10) ; 
 % \draw[thick,color=blue,dashed] (4.5,2.025) -- (4.5,10) node[midway, left] {$\bar{x}=79,75\,$m} -- (10,10) node[midway, above] {$\bar{t}=5,5\,$s}  ; 
 
  \draw[thick,color=purple] plot[samples=50, domain=2:6.5] (\x, \x-2.5 ) node[right] {$$}; 
  \draw[thick,color=purple,dashed] (3,0.5) -- (6,0.5) node[midway, below] {$t_5=3\,$s} -- (6,3.5) node[midway, right] {$x_5=30\,$m}  ; 
 
 % \draw[thick,color=olive] plot[samples=50, domain=6.5:10] (\x, 9/5*\x-8.125 ) node[right] {$$}; 
 % \draw[thick,color=olive,dashed] (7,4.5) -- (9.5,4.5) node[midway, below] {$t_9=2,5\,$s} -- (9.5,9) node[midway, right] {$x_9=45\,$m}  ; 

\end{tikzpicture}
```

</center>

***********



**Bestimme** anschließend die momentane Geschwindigkeiten bei $t=9\,$s. \



$v_9 \approx$ [[  18  ]] $\dfrac{\text{m}}{\text{s}}$
***********
$$
\begin{align*}
   v_9 & = \frac{\Delta x_9}{\Delta t_9} = \frac{45\,\text{m}}{2,5\,\text{s}} = 18\,\frac{\text{m}}{\text{s}}  \\
\end{align*}
$$

<center>

```latex  @tikz
\begin{tikzpicture}[scale=2,>=latex]       

\draw[black!70, step=5mm, very thin, dashed] (-0.5,-0.5) grid (10.5,10.5);  

\draw[black!70, step=10mm, very thin] (-0.5,-0.5) grid (10.5,10.5);

  \coordinate (ya) at (0,-0.75);
  \coordinate (xa) at (-0.75,0);
  \coordinate (o) at (0,0);

  \coordinate (y) at (0,10.75);
    \coordinate (x) at (10.75,0);
    \draw[<->, black!100, thick] (y) node[above] {$x$ in m} -- (0,0) --  (x) node[right]    {$t$ in s};

\draw[-, black!100, thin]  (0,0.1) -- (0,-0.1) node[below=0.25cm,left] {0};
\draw[-, black!100, thin]  (1,0.1) -- (1,-0.1) node[below] {1};
\draw[-, black!100, thin]  (2,0.1) -- (2,-0.1) node[below] {2};
\draw[-, black!100, thin]  (3,0.1) -- (3,-0.1) node[below] {3};
\draw[-, black!100, thin]  (4,0.1) -- (4,-0.1) node[below] {4};
\draw[-, black!100, thin]  (5,0.1) -- (5,-0.1) node[below] {5};
\draw[-, black!100, thin]  (6,0.1) -- (6,-0.1) node[below] {6};
\draw[-, black!100, thin]  (7,0.1) -- (7,-0.1) node[below] {7};
\draw[-, black!100, thin]  (8,0.1) -- (8,-0.1) node[below] {8};
\draw[-, black!100, thin]  (9,0.1) -- (9,-0.1) node[below] {9};
\draw[-, black!100, thin]  (10,0.1) -- (10,-0.1) node[below] {10};
\draw[-, black!100, thin]  (0.1,1) -- (-0.1,1) node[left] {10};
\draw[-, black!100, thin]  (0.1,2) -- (-0.1,2) node[left] {20};
\draw[-, black!100, thin]  (0.1,3) -- (-0.1,3) node[left] {30};
\draw[-, black!100, thin]  (0.1,4) -- (-0.1,4) node[left] {40};
\draw[-, black!100, thin]  (0.1,5) -- (-0.1,5) node[left] {50};
\draw[-, black!100, thin]  (0.1,6) -- (-0.1,6) node[left] {60};
\draw[-, black!100, thin]  (0.1,7) -- (-0.1,7) node[left] {70};
\draw[-, black!100, thin]  (0.1,8) -- (-0.1,8) node[left] {80};
\draw[-, black!100, thin]  (0.1,9) -- (-0.1,9) node[left] {90};
\draw[-, black!100, thin]  (0.1,10) -- (-0.1,10) node[left] {100};

\draw[-, black!100, thin]  (-1,0.1) -- (-1,-0.1) node[below] {};
\draw[-, black!100, thin]  (0.1,-1) -- (-0.1,-1) node[left] {};


 \draw [ black!100, thick]  (ya) --(o) --  (xa);


  \draw[ultra thick,color=red] plot[samples=50, domain=-0.0:10] (\x, \x*\x/10 ) node[right] {$x(t)$}; 
	
 % \draw[thick,color=blue] (4.5,2.025) -- (10,10) ; 
 % \draw[thick,color=blue,dashed] (4.5,2.025) -- (4.5,10) node[midway, left] {$\bar{x}=79,75\,$m} -- (10,10) node[midway, above] {$\bar{t}=5,5\,$s}  ; 
 
 % \draw[thick,color=purple] plot[samples=50, domain=2:6.5] (\x, \x-2.5 ) node[right] {$$}; 
 % \draw[thick,color=purple,dashed] (3,0.5) -- (6,0.5) node[midway, below] {$t_5=3\,$s} -- (6,3.5) node[midway, right] {$x_5=30\,$m}  ; 
 
  \draw[thick,color=olive] plot[samples=50, domain=6.5:10] (\x, 9/5*\x-8.125 ) node[right] {$$}; 
  \draw[thick,color=olive,dashed] (7,4.5) -- (9.5,4.5) node[midway, below] {$t_9=2,5\,$s} -- (9.5,9) node[midway, right] {$x_9=45\,$m}  ; 

\end{tikzpicture}
```

</center>

***********



<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

## Aufgabe 3


Ein Autofahrer ist in seinem SUV mit einer Geschwindigkeit von $175\,\dfrac{\text{km}}{\text{h}}$ unterwegs.\

__$a)\;\;$__ Der Fahrer besitzt eine Reaktionszeit von $0,7\,$s. **Berechne**, wie weit der SUV sich fortbewegt, bevor eine Bremsung beginnen kann. (Runde auf drei Nachkommastellen.) \


$x_R(t) \approx$ [[  34,029  ]] m
***********
$$
\begin{align*}
   x_R(t) & = v t = 175 \frac{\text{km}}{\text{h}} \cdot 0,7\,\text{s} = 175 \dfrac{\text{1000m}}{\text{3600s}}  \cdot 0,7\,\text{s} \approx 34,029 \,\text{m}   \\
\end{align*}
$$
***********


<br>
<br>
__$b)\;\;$__ Die Bremsen des SUV haben eine Beschleunigung von $4,1\,\dfrac{\text{m}}{\text{s}^2}$. **Berechne** die Bremsdauer. (Runde auf drei Nachkommastellen.)  \



$t_B \approx$ [[  11,856  ]] s
***********
$$
\begin{align*}
   v(t) & = a t + v_0  \quad \left|  -v_0  \right.  \\
   v(t) - v_0 & = a t     \quad \left|  : a  \right.  \\
   \dfrac{v(t) - v_0}{a} & =  t    \\
   \dfrac{0 \frac{\text{m}}{\text{s}} - 175 \dfrac{\text{1000m}}{\text{3600s}}}{- 4,1\,\dfrac{\text{m}}{\text{s}^2}} & =  t \approx 11,856\,\text{s}   \\
\end{align*}
$$
***********


<br>
<br>
__$c)\;\;$__ **Berechne** den Bremsweg des SUVs. (Runde auf drei Nachkommastellen.) \


$x_B(t) \approx$ [[  288,176  ]] m
***********
$$
\begin{align*}
   x_B(t) & = \dfrac{1}{2}at^2 + v t \\
   x_B(t) & = \dfrac{1}{2} \cdot \left( - 4,1\,\dfrac{\text{m}}{\text{s}^2} \right) \cdot (11,856\,\text{s})^2 + 175 \dfrac{\text{1000m}}{\text{3600s}}  \cdot 11,856\,\text{s} \\
   x_B(t) & \approx 288,176 \,\text{m}   \\
\end{align*}
$$
***********


<br>
<br>
__$d)\;\;$__ **Berechne** den Anhalteweg des SUVs. (Runde auf drei Nachkommastellen.) \


$x_A(t) \approx$ [[  322,203  ]] m
***********
$$
\begin{align*}
   x_A(t) & = x_B(t) + x_R(t) \approx 322,203 \,\text{m} \\
\end{align*}
$$
***********


<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

## Aufgabe 4

Auf einem Flugzeugträger fährt ein Matrose mit einer Geschwindigkeit von $14\,\dfrac{\text{km}}{\text{h}}$ zur Oberfläche des Decks entgegen der Fahrtrichtung des Schiffs. Der Flugzeugträger fährt mit einer Geschwindigkeit von $32\,\dfrac{\text{km}}{\text{h}}$ zur Wasseroberfläche, während dem Schiff ein Motorboot mit einer Geschwindigkeit von $45\,\dfrac{\text{km}}{\text{h}}$ zum Schiff entgegen kommt. 
**Berechne** die Geschwindigkeit des Motorboots aus der Sicht des Fahrradfahrers. \


[[   5   ]] $\dfrac{\text{km}}{\text{h}}$
***********
$$
\begin{align*}
   32\,\dfrac{\text{km}}{\text{h}} - 14\,\dfrac{\text{km}}{\text{h}} = 18\,\dfrac{\text{km}}{\text{h}} \\
   45\,\dfrac{\text{km}}{\text{h}} - 32\,\dfrac{\text{km}}{\text{h}} = 13\,\dfrac{\text{km}}{\text{h}} \\
   18\,\dfrac{\text{km}}{\text{h}} - 13\,\dfrac{\text{km}}{\text{h}} = 5\,\dfrac{\text{km}}{\text{h}} \\
\end{align*}
$$
***********

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

## Aufgabe 5

Ein Fluss besitzt eine Fließgeschwindigkeit von $7\,\dfrac{\text{km}}{\text{\text{h}}}$ zur Erde. Aus dem Fluss rudert ein Mensch mit einer Geschwindigkeit von $11\,\dfrac{\text{km}}{\text{\text{h}}}$ in Richtung der Fließgeschindigkeit des Flusses, während auf dem Deich ein Jogger mit $8\,\dfrac{\text{km}}{\text{\text{h}}}$ zum Boden entgegen der Fließrichtung läuft.  
**Berechne** die Geschwindigkeit des Joggers aus der Sicht des Ruderers. \


[[   26  ]] $\dfrac{\text{km}}{\text{h}}$
***********
$$
\begin{align*}
   7\,\dfrac{\text{km}}{\text{h}} + 11\,\dfrac{\text{km}}{\text{h}} = 18\,\dfrac{\text{km}}{\text{h}} \\
   18\,\dfrac{\text{km}}{\text{h}} + 8\,\dfrac{\text{km}}{\text{h}} = 26\,\dfrac{\text{km}}{\text{h}} \\
\end{align*}
$$
***********

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

## Herausforderungsaufgabe 

> Diese Aufgabe stellt eine kleine Herausforderung da. Solltest du diese Aufgabe lösen können, sollte dich in der Leistungskontrolle kaum noch was überraschen können. 


<br>

Bei einem Überholmanöver muss das dahinterliegende Fahrzeug die Geschwindigkeit erhöhen, es darf den Sicherheitsabstand von $10\,$m nicht unterschreiten und nicht schneller als die maximale Geschwindigkeitsbegrenzung werden. \


<br>
<br>

__$a)\;\;$__ Lies die weiteren Aufgabenteile und **skizziere** den Überholvorgang. \


[[!]]
<script>true</script>
***********

<center>

```latex  @tikz
\begin{tikzpicture}[scale=1,>=latex]       

\draw[ultra thick, white] (-1,3) -- (-1,3) ;
\draw[ultra thick, white] (-1,-1) -- (-1,-1) ;
\draw[ultra thick, white] (13,3) -- (13,3) ;

\draw[ultra thick] (0,0) -- (2,0) node[midway, below] {$l_1=4,5\,\text{m}$} -- (2,1) -- (0,1) -- (0,0) ;


\draw[ultra thick, |<->|] (2,-0.25) -- (4,-0.25)  node[midway, below] {$s=10\,\text{m}$} ;

\draw[ultra thick] (4,0) -- (8,0) node[midway, below] {$l_2=17\,\text{m}$} -- (8,1) -- (4,1) -- (4,0) ;

\draw[ultra thick, |<->|] (8,-0.25) -- (10,-0.25)  node[midway, below] {$s=10\,\text{m}$} ;


\draw[ultra thick, dashed] (10,0) -- (12,0) node[midway, below] {$l_1=4,5\,\text{m}$} -- (12,1) -- (10,1) -- (10,0) ;

\draw[ultra thick,red, |->] (0,2.5) -- (7,2.5) node[midway, above] {$a > 0$};
\draw[ultra thick,orange, |->] (7,2.5) -- (11,2.5)  node[midway, above] {$a = 0$};

\end{tikzpicture}
```

</center>

***********

<br>
<br>

__$b)\;\;$__ Das dahinterliegende Fahrzeug hat vor dem Überholmanöver die gleiche Geschwindigkeit wie das Fahrzeug davor von $70\,\dfrac{\text{km}}{\text{h}}$. Insgesamt ist eine Geschwindigkeit von $100\,\dfrac{\text{km}}{\text{h}}$ erlaubt. **Berechne**, wie lang eine Beschleunigung auf die maximal erlaubte Geschwindigkeit dauern würde, wenn das Fahrzeug mit $3,4\,\dfrac{\text{m}}{\text{s}^2}$ beschleunigt. (Runde auf drei Nackommastellen.) \


$t_B \approx$ [[  2,451  ]] s 
***********
$$
\begin{align*}
   v(t) & = at + v_0 \quad \left| -v_0 \right.   \\
   v(t) -v_0 & = at   \quad \left| :a \right.   \\
   \dfrac{v(t) -v_0}{a} & = t     \\
   \dfrac{100\,\dfrac{\text{km}}{\text{h}} - 70\,\dfrac{\text{km}}{\text{h}}}{3,4\,\dfrac{\text{m}}{\text{s}^2}} & = t  \\
   \dfrac{30\,\dfrac{\text{1000m}}{\text{3600s}} }{3,4\,\dfrac{\text{m}}{\text{s}^2}} & = t  \approx 2,451 \,\text{s} \\
\end{align*}
$$
***********



<br>
<br>

__$c)\;\;$__ Das dahinterliegende Fahrzeug hat eine Länge von $4,5\,$m. Das Fahrzeug davor hat eine Länge von $17\,$m. **Berechne** Die Strecke die während der Beschleunigungsphase im Bezug zum zu überholenden Auto zurückgelegt wird. (Runde auf drei Nackommastellen.) \


$x_B(t) \approx$ [[  10,212  ]] m
***********
$$
\begin{align*}
   x_B(t) & = \dfrac{1}{2} a t^2 + v_0 t 
   x_B(t) & = \dfrac{1}{2} \cdot 3,4\,\dfrac{\text{m}}{\text{s}^2} \cdot \left(2,451 \,\text{s}\right)^2 \approx 10,212 \,\text{m} \\
\end{align*}
$$
***********

<br>
<br>

__$d)\;\;$__ Das dahinterliegende Fahrzeug hat eine Länge von $4,5\,$m. Das Fahrzeug davor hat eine Länge von $17\,$m. **Berechne** Die Strecke die während der Beschleunigungsphase auf der Straße zurückgelegt wird. (Runde auf drei Nackommastellen.) \


$x_{B,S}(t) \approx$ [[  57,870  ]] m
***********
$$
\begin{align*}
   x_{B,S}(t) & = \dfrac{1}{2} a t^2 + v_0 t 
   x_{B,S}(t) & = \dfrac{1}{2} \cdot 3,4\,\dfrac{\text{m}}{\text{s}^2} \cdot \left(2,451 \,\text{s}\right)^2 + 70\,\dfrac{\text{1000m}}{\text{3600s}} \cdot 2,451 \,\text{s} \approx 57,870 \,\text{m} \\
\end{align*}
$$
***********


<br>
<br>

__$e)\;\;$__ **Berechne** die Dauer beim Überholmanöver, die mit konstanter Geschwindigkeit gefahren werden muss. \


$t_k \approx$ [[  6,205  ]] s
***********
$$
\begin{align*}
   \delta l & = l - x_B(t)  \\
   \delta l & = 4,5\,\text{m} + 10 \,\text{m} + 17\,\text{m} + 10 \,\text{m} - 10,212 \,\text{m} \approx 51,712 \,\text{m} \\
   \Rightarrow\;\; l & = \Delta v t \quad \left| :v \right. \\
   \dfrac{l}{\Delta v} & = t     \\
   \dfrac{51,712 \,\text{m}}{ 30\,\dfrac{\text{1000m}}{\text{3600s}} } & \approx t    \approx  6,205  \,\text{s}  \\
\end{align*}
$$
***********


<br>
<br>

__$f)\;\;$__ **Berechne** die auf der Straße zurückgelegte Strecke während des Überholmanövers. \


$x(t) \approx$ [[  230,245  ]] m
***********
$$
\begin{align*}
   x_S(t) & = v t = 100\,\dfrac{\text{1000m}}{\text{3600s}} \cdot 6,205  \,\text{s} \approx  172,375  \,\text{m} \\
   x(t) & = x_{B,S}(t) + x_S(t)   \\
   x(t) & = 57,870  \,\text{m} + 172,375  \,\text{m} \approx 230,245 \,\text{m} \\
\end{align*}
$$
***********

<br>
<br>

__$g)\;\;$__ **Begründe**, warum die errechneten Werte nicht der Realität entsprechen können. \


[[!]]
<script>true</script>
***********

In der Realität gibt es keine konstante Beschleunigung bei Autos, da der Motor unterschiedlich auf die diversen Geschwindigkeiten aufgrund der Reibung reagiert. Auch ist eine Straße niemals komplett gerade und der Windeinfluss ist auch nicht zu vernachlässigen. Somit würde die gesamten realen Werte nochmals höher ausfallen als die hier berechneten.

***********




<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>