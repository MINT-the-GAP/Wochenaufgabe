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

# Probeleistungskontrolle für Physik - Klasse 7: Energie


<br>

Swipe (Wische) entweder weiter oder klicke unten links auf neben der Seitenzahl auf den Pfeil nach rechts. 

<br>

Diese Probearbeit hat mehr Aufgaben als die richtige Arbeit, damit du genug zum Üben hast. Es sind viele verschiedene Aufgabentypen abgebildet, sodass du alles nochmal bei der Bearbeitung dieser Aufgaben wiederholst. 


## Aufgabe 1



Ein Objekt fällt reibungsfrei aus einer Höhe von $5\,$m und hat zu Beginn des Falls schon eine kinetische Energie von $0,25\,$J. **Berechne** die Geschwindigkeit, mit der das Objekt auf den Boden auftrifft. Das objekt besitzt eine Masse von $150\,$g. Runde auf zwei Nachkommastellen. 

<br>

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





## Aufgabe 2



**Fülle den Lücken in den Sätzen aus.** \

<br>

<section class="flex-container">

<div class="flex-child">

Die Ladung der Gravitation heißt [[Masse]].  

<br>

Wenn eine Ladung positiv geladen ist, dann handelt es sich um die [[elektrische]] Kraft.  

<br>

Eine Kraft, die von einer Punktladung aus auf eine Testladung wirkt, wird in der Entfernung [[schwächer]], da die [[Feldlinien]] einen immer größeren Abstand zu einander haben.  

<br>

Wird eine [[Äquipotentiallinie]] verlassen, dann wird Energie umgewandelt. Somit wird [[Arbeit]] verrichtet.  

<br>

[[Energie]] kann niemals verbraucht oder erzeugt, sondern nur [[umgewandelt]] werden.  

<br>
   


</div>
 


</section>





## Aufgabe 3



Ein Auto mit einer Masse von $1,4\,$t beschleundigt in $9\,$s von $50\,\dfrac{\text{km}}{\text{h}}$ auf $90\,\dfrac{\text{km}}{\text{h}}$. **Berechne** die erbrachte Leistung. Runde auf zwei Nachkommastellen.

<br>

<section class="flex-container">

<div class="flex-child">

$P=$ [[33607,68]] W
***********
$$
\begin{align*}
P & = \frac{W}{t}  \\
P & = \frac{\Delta E}{t}  \\
P & = \frac{E_{kin,2} - E_{kin,1}}{t}  \\
P & = \frac{\dfrac{1}{2} m v_2^2 - \dfrac{1}{2} m v_1^2}{t}  \\ 
P & = \frac{\dfrac{1}{2} \cdot 1,4\,\text{t} \cdot  \left( 90 \,\dfrac{\text{km}}{\text{h}} \right)^2 - \dfrac{1}{2} \cdot 1,4\,\text{t}  \cdot  \left( 50 \,\dfrac{\text{km}}{\text{h}} \right)^2 }{9\,\text{s}}  \\ 
P & = \frac{\dfrac{1}{2} \cdot 1400\,\text{kg} \cdot  \left( 90 \,\dfrac{1000\,\text{m}}{3600\,\text{s}} \right)^2 - \dfrac{1}{2} \cdot 1400\,\text{kg}  \cdot  \left( 50 \,\dfrac{1000\,\text{m}}{3600\,\text{s}} \right)^2 }{9\,\text{s}}  \\ 
\end{align*}
$$
***********



</div>
 


</section>





## Aufgabe 4



$a)\;\;$ Gegeben sei die dargestellte Ladungskonfiguration von $Q_-$ und $Q_+$, welche homogen auf den gezeichneten Linien verteilt sind. **Zeichne** die Äquipotentiallinien **ein**.

<br>

<section class="flex-container">

<div class="flex-child">
 
<center>
```latex  @tikz
\begin{tikzpicture}[scale=2,>=latex]       

     \coordinate[label=center:$.$]  (a) at (-1,-1);  
     \coordinate[label=center:$.$]  (b) at (9,8);   

     \coordinate[label=center:$Q_-$] (Q2) at (4,3.25);
		 \coordinate[label=center:$Q_+$] (Q1) at (7.5,3.25);		

	\draw (4,3.25) ellipse (0.5cm and 0.5cm);
	\draw (4,3.25) ellipse (3.0cm and 3.0cm);
    
\end{tikzpicture}
```
</center>

***********

 <center>
```latex  @tikz
\begin{tikzpicture}[scale=2,>=latex]       

     \coordinate[label=center:$.$]  (a) at (-1,-1);  
     \coordinate[label=center:$.$]  (b) at (9,8);   

     \coordinate[label=center:$Q_-$] (Q2) at (4,3.25);
		 \coordinate[label=center:$Q_+$] (Q1) at (7.5,3.25);		

	\draw (4,3.25) ellipse (0.5cm and 0.5cm);
	\draw (4,3.25) ellipse (3.0cm and 3.0cm);

    
	\draw[thick, red] (4,3.25) circle (2.75cm);
	\draw[thick, orange] (4,3.25) circle (2.25cm);
	\draw[thick, yellow] (4,3.25) circle (1.75cm);
	\draw[thick, green] (4,3.25) circle (1.25cm);
	\draw[thick, blue] (4,3.25) circle (0.75cm);
    
\end{tikzpicture}
```
</center>

***********


</div>
 

<br>
<br>
<br>



$b)\;\;$ Gegeben seien die dargestellten Stabmagnete. **Zeichne** die magnetischen Feldlinien **ein**.





<div class="flex-child">
  
<center>
```latex  @tikz 
\begin{tikzpicture}[scale=2,>=latex]       


     \coordinate[label=center:$.$]  (a) at (-2,-1);  
     \coordinate[label=center:$.$]  (b) at (8,5);   

		\begin{scope}[xshift=1cm, yshift=2cm]	
		\begin{scope}[rotate = 90]			
    \shade[left color=red!80!white,right color=red!80!white,opacity=1] (0,-0.05) -- (0.75,-0.05)  -- (0.75,1)  -- (0,1)  -- (0,-0.05)   ;
    \shade[left color=green!80!white,right color=green!80!white,opacity=1] (0,0) -- (0.75,0)  -- (0.75,-1)  -- (0,-1)  -- (0,0)   ;    
    \coordinate[label=center:\large$N$] (a) at (0.375,0.5);
    \coordinate[label=center:\large$S$] (b) at (0.375,-0.5);
		\end{scope} \end{scope}
		
		\begin{scope}[xshift=5cm, yshift=2cm]	
		\begin{scope}[rotate = 90]			
    \shade[left color=red!80!white,right color=red!80!white,opacity=1] (0,-0.05) -- (0.75,-0.05)  -- (0.75,1)  -- (0,1)  -- (0,-0.05)   ;
    \shade[left color=green!80!white,right color=green!80!white,opacity=1] (0,0) -- (0.75,0)  -- (0.75,-1)  -- (0,-1)  -- (0,0)   ;    
    \coordinate[label=center:\large$N$] (a) at (0.375,0.5);
    \coordinate[label=center:\large$S$] (b) at (0.375,-0.5);
		\end{scope}\end{scope} 
    
\end{tikzpicture} 
```
</center>


***********
<center>
```latex  @tikz 
\begin{tikzpicture}[scale=2,>=latex]       


     \coordinate[label=center:$.$]  (a) at (-2,-1);  
     \coordinate[label=center:$.$]  (b) at (8,5);    
        
        \begin{scope}[xshift=1cm, yshift=2cm]			
        
        \begin{scope}[yshift=0.375cm, decoration={    markings,    mark=at position 0.5 with {\arrow{>}}}]	 
		\draw[blue, thick,postaction={decorate}] (3,0) to[out=180,in=0] (1,0) ; 
		\draw[blue, thick,postaction={decorate}] (3.5,0) to[out=170,in=10] (0.5,0) ; 
		\draw[blue, thick,postaction={decorate}] (3.5,0) to[out=150,in=30] (0.5,0) ; 
		\draw[blue, thick,postaction={decorate}] (3.5,0) to[out=120,in=60] (0.5,0) ; 
		\draw[blue, thick,postaction={decorate}] (3.5,0.25) to[out=90,in=90] (0.5,0.25) ;  
		\draw[blue, thick,postaction={decorate}] (3.625,0.375) to[out=90,in=90] (4.375,0.375) ; 
		\draw[blue, thick,postaction={decorate}] (5.5,0.25) to[out=200,in=0] (4.5,0.05) ; 
		\draw[blue, thick,postaction={decorate}] (5.5,0.0) to[out=180,in=0] (4.5,0.0) ; 
		\draw[blue, thick,postaction={decorate}] (-0.375,0.375) to[out=90,in=90] (0.375,0.375) ; 
		\draw[blue, thick,postaction={decorate}] (-1,0.05) to[out=0,in=330] (-1.5,0.25) ; 
		\draw[blue, thick,postaction={decorate}] (-1,0.0) to[out=0,in=180] (-1.5,0.0) ; 
		\end{scope}
		
		\begin{scope}[yscale=-1]
		\begin{scope}[yshift=-0.375cm, decoration={    markings,    mark=at position 0.5 with {\arrow{>}}}]	 
		\draw[blue, thick,postaction={decorate}] (3,0) to[out=180,in=0] (1,0) ; 
		\draw[blue, thick,postaction={decorate}] (3.5,0) to[out=170,in=10] (0.5,0) ; 
		\draw[blue, thick,postaction={decorate}] (3.5,0) to[out=150,in=30] (0.5,0) ; 
		\draw[blue, thick,postaction={decorate}] (3.5,0) to[out=120,in=60] (0.5,0) ; 
		\draw[blue, thick,postaction={decorate}] (3.5,0.25) to[out=90,in=90] (0.5,0.25) ;  
		\draw[blue, thick,postaction={decorate}] (3.625,0.375) to[out=90,in=90] (4.375,0.375) ; 
		\draw[blue, thick,postaction={decorate}] (5.5,0.25) to[out=200,in=0] (4.5,0.05) ; 
		\draw[blue, thick,postaction={decorate}] (5.5,0.0) to[out=180,in=0] (4.5,0.0) ; 
		\draw[blue, thick,postaction={decorate}] (-0.375,0.375) to[out=90,in=90] (0.375,0.375) ; 
		\draw[blue, thick,postaction={decorate}] (-1,0.05) to[out=0,in=330] (-1.5,0.25) ; 
		\draw[blue, thick,postaction={decorate}] (-1,0.0) to[out=0,in=180] (-1.5,0.0) ; 
		\end{scope}\end{scope}
        
        \end{scope}


		\begin{scope}[xshift=1cm, yshift=2cm]	
		\begin{scope}[rotate = 90]			
    \shade[left color=red!80!white,right color=red!80!white,opacity=1] (0,-0.05) -- (0.75,-0.05)  -- (0.75,1)  -- (0,1)  -- (0,-0.05)   ;
    \shade[left color=green!80!white,right color=green!80!white,opacity=1] (0,0) -- (0.75,0)  -- (0.75,-1)  -- (0,-1)  -- (0,0)   ;    
    \coordinate[label=center:\large$N$] (a) at (0.375,0.5);
    \coordinate[label=center:\large$S$] (b) at (0.375,-0.5);
		\end{scope} \end{scope}
		
		\begin{scope}[xshift=5cm, yshift=2cm]	
		\begin{scope}[rotate = 90]			
    \shade[left color=red!80!white,right color=red!80!white,opacity=1] (0,-0.05) -- (0.75,-0.05)  -- (0.75,1)  -- (0,1)  -- (0,-0.05)   ;
    \shade[left color=green!80!white,right color=green!80!white,opacity=1] (0,0) -- (0.75,0)  -- (0.75,-1)  -- (0,-1)  -- (0,0)   ;    
    \coordinate[label=center:\large$N$] (a) at (0.375,0.5);
    \coordinate[label=center:\large$S$] (b) at (0.375,-0.5);
		\end{scope}\end{scope} 
    
\end{tikzpicture} 
```
</center>
***********

</div>





</section>


 




## Aufgabe 5

$a)\;\;$  **Begründe**, warum Arbeit nicht gemessen werden kann. 


<br>

<section class="flex-container">

<div class="flex-child">
  

 
   


***********
Arbeit ist eine Prozessgröße, die den Unterschied zwischen zwei Energiezuständen beschreibt. Wie dieser Prozess ausgestaltet ist, ist nicht zu messen, da durch den Vergleich von zwei zeitlichen Messwerten schon eine Differenz von Energien betrachtet wird. 
***********

</div>


<br>
<br>
<br>
<br>
<br>

 

Der gezeigte Graph (links) stellt die Feldliniendichte als Funktion dar, welche von einer Punktladung ausgeht (rechte Darstellung). 

<br>


<center>
```latex  @tikz 
\begin{tikzpicture}[scale=2,>=latex]       



      \draw[black!70, step=1.0644*5mm,   thin, dashed] (-1.0644*1,-1.0644*4) grid (1.0644*4,1.0644*1);  
      \draw[black!70, step=1.0644*10mm,   thin] (-1.0644*1,-1.0644*4) grid (1.0644*4,1.0644*1);

  \coordinate (ya) at (0,-1.0644*4.25);
  \coordinate (xa) at (-1.0644*1.25,0);
  \coordinate (o) at (0,0);
 
  \coordinate (y) at (0,1.25*1.0644);
    \coordinate (x) at (1.25*4.0644,0);
    \draw[<->, black!100, thick] (y) node[above] {$V(r)$} -- (0,0) --  (x) node[right]  {$r$};

\draw[-, black!100, thin]  (1.0644*0,0.1) -- (1.0644*0,-0.1) node[below=0.25cm,left] {0};
\draw[-, black!100, thin]  (1.0644*1,0.1) -- (1.0644*1,-0.1) node[below] {}; 
\draw[-, black!100, thin]  (1.0644*2,0.1) -- (1.0644*2,-0.1) node[below] {}; 
\draw[-, black!100, thin]  (1.0644*3,0.1) -- (1.0644*3,-0.1) node[below] {}; 
\draw[-, black!100, thin]  (1.0644*4,0.1) -- (1.0644*4,-0.1) node[below] {}; 
\draw[-, black!100, thin]  (0.1,1.0644*1) -- (-0.1,1.0644*1) node[left] {}; 

\draw[-, black!100, thin]  (-1.0644*1,0.1) -- (-1.0644*1,-0.1) node[below] {}; 
\draw[-, black!100, thin]  (0.1,-1.0644*1) -- (-0.1,-1.0644*1) node[left] {};
\draw[-, black!100, thin]  (0.1,-1.0644*2) -- (-0.1,-1.0644*2) node[left] {};
\draw[-, black!100, thin]  (0.1,-1.0644*3) -- (-0.1,-1.0644*3) node[left] {};
\draw[-, black!100, thin]  (0.1,-1.0644*4) -- (-0.1,-1.0644*4) node[left] {};


\draw[fill=blue, thin]  (0,-1.0644*4) circle (1.0644*0.25);

 \draw [ black!100, thick]  (ya) --(o) --  (xa);


	\draw[ultra thick,color=black, ] plot[samples=100, domain=0.25:4.33] (1.0644*\x, {-1.0644/\x} ) node[below] {$$}; 
	\draw[ultra thick,color=blue, ] plot[samples=100, domain=0.25:0.33] (1.0644*\x, {-1.0644/\x} ) node[below] {$$};  
	\draw[ultra thick,color=green, ] plot[samples=100, domain=0.33:0.5] (1.0644*\x, {-1.0644/\x} ) node[below] {$$};  
	\draw[ultra thick,color=yellow, ] plot[samples=100, domain=0.5:0.9] (1.0644*\x, {-1.0644/\x} ) node[below] {$$}; 
	\draw[ultra thick,color=orange, ] plot[samples=100, domain=0.9:1.5] (1.0644*\x, {-1.0644/\x} ) node[below] {$$};  
	\draw[ultra thick,color=red, ] plot[samples=100, domain=1.5:4.33] (1.0644*\x, {-1.0644/\x} ) node[below] {$$};  
		 
    
    
    
    \begin{scope}[xshift=9cm,yshift=-1.75cm] 
    \draw[<->, black!100, thick] (-3,0) -- (3,0) node[right]  {$r$};
    \draw[<->, black!100, thick] (0,-3) -- (0,3) node[right]  {$r$};
    \begin{scope}[rotate=45]
    \draw[<->, black!100, thick] (-3,0) -- (3,0) node[right]  {$r$};
    \draw[<->, black!100, thick] (0,-3) -- (0,3) node[right]  {$r$};
    \end{scope}
    \draw[ultra thick,fill=blue] (0,0) circle (0.25cm);
    \draw[ultra thick,blue] (0,0) circle (0.5cm);
    \draw[ultra thick,green] (0,0) circle (1cm);
    \draw[ultra thick,yellow] (0,0) circle (1.5cm);
    \draw[ultra thick,orange] (0,0) circle (2.0cm);
    \draw[ultra thick,red] (0,0) circle (2.5cm);
    
    \end{scope}
    
\end{tikzpicture} 
```
</center>

<br>
 
<div class="flex-child">
  
$b)\;\;$ **Erkläre**, wie am Graphen erkannt werden kann, dass Arbeit verrichtet wird.  


<br>



***********
Wenn sich ein Objekt in diesem Potential bewegt, dann wird durch die Veränderung des Ortes (Abszissenwerte) ein neuer Potentialwert (Ordinatenwert) zugeordnet. Dieser Unterschied der Ordinatenwerte gibt Aufschluss auf die verrichtete Arbeit.
***********

</div>




<div class="flex-child">
  
$c)\;\;$ **Beschreibe**, wie sich der gleiche Arbeitswert am Graphen an unterschiedlichen Orten $r$ darstellt.  


<br>



***********
Befindet man sich dicht am Koordinatenursprung wird der Potentialunterschied bei einer kleinen Ortsveränderung sehr groß, während bei einer weiteren Entfernung vom Koordinatenursprung der Ortsunterschied deutlich größer sein muss, um den gleichen Potentialunterschiedswert zu erreichen. Dies wird auch die "Goldene Regel" genannt, da man entweder viel Kraft über wenig Strecke oder wenig Kraft über viel Strecke ausüben muss, um die gleiche Arbeit zu verrichten. (Wie beim Hebelgesetz) 
***********

</div>





</section>


 
