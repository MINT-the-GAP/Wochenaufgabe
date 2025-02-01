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


# Probeklassenarbeit für Mathematik - Klasse 7: Prozentrechnung

<br>

Swipe (Wische) entweder weiter oder klicke unten links auf neben der Seitenzahl auf den Pfeil nach rechts. 

<br>

Diese Probearbeit hat mehr Aufgaben als die richtige Arbeit, damit du genug zum Üben hast. Es sind viele verschiedene Aufgabentypen abgebildet, sodass du alles nochmal bei der Bearbeitung dieser Aufgaben wiederholst. 

## Aufgabe 1



**Gib** den darstellten roten Anteil vom Ganzen in der Prozentdarstellung **an**. **Gib** Periodizitäten gerundet auf zwei Nachkommastellen **an**. Falls ansonsten gerundet werden muss, **gib** zwei Nachkomma stellen **an**.

<br>
<br>

<section class="flex-container">

<div class="flex-child">



__$a)$__
 
<br>

```latex  @tikz
\begin{tikzpicture}[scale=2,>=latex]        
 
\draw[thick,fill=red,opacity=0.5] (0,0) -- (0:1)  arc (0:300:1) -- (0,0);  
\foreach \n in {60,120,...,360} { \draw[opacity=0.5,rotate=\n] (0,0) -- (0:1)  arc (0:60:1) -- (0,0); } 
\draw[thick] (0,0) circle (1cm);   
    
\end{tikzpicture}
``` 

<br>

[[83,33%]]


</div>


<br>
<br>
<br>
<br>


<div class="flex-child">



__$b)$__
 
<br>

```latex  @tikz
\begin{tikzpicture}[scale=2,>=latex]        
 
 
\draw[thick,fill=white,opacity=0.5] (0,0) rectangle (0.5,2); 
\draw[thick,fill=white,opacity=0.5] (0.5,0) rectangle (1,2); 
\draw[thick,fill=white,opacity=0.5] (1,0) rectangle (1.5,2); 
\draw[thick,fill=white,opacity=0.5] (1.5,0) rectangle (2,2); 
\draw[thick,fill=red,opacity=0.5] (2,0) rectangle (2.5,2); 
\draw[thick,fill=white,opacity=0.5] (2.5,0) rectangle (3,2);  
\draw[thick,fill=red,opacity=0.5] (3,0) rectangle (3.5,2); 
\draw[thick,fill=red,opacity=0.5] (3.5,0) rectangle (4,2);  
    
\end{tikzpicture}
``` 

<br>

[[37,5%]]


</div>
 


</section>







## Aufgabe 2



In einer Schulklasse kommen $15$ von $24$ Schülern mit dem Fahrrad. **Berechne** den prozentualen Anteil.

<br>
<br>

<section class="flex-container">

<div class="flex-child">

[[62,5%]]
***********
 
$p=\dfrac{W}{G} =\dfrac{15}{24} = \dfrac{5}{8} = 62,5 \% $
 
***********

 

</div>
 


</section>






## Aufgabe 3

Ein Kapital von $7500$€ wurde ein Jahr zu einem Jahreszins von $2\%$ angelegt. **Berechne** die resultierende Geldmenge.


 <br>
 <br>


<section class="flex-container">

<div class="flex-child">
 

[[6846]]
***********
$7500\,\text{€} \cdot 1,02 = 7650\,\text{€}$
***********
</div>

 


</section>




## Aufgabe 4

Die gesamte Downloaddauer beträgt $40\,$min. **Zeichne** in den Downloadbalken den dort beschriebenen Stand des Downloads **ein**.

 <br>
 <br>


<section class="flex-container">

<div class="flex-child">
 
```latex  @tikz
\begin{tikzpicture}[scale=1.5,>=latex]        
 
 
 \node[right] at (0,1) {Downloading... verbleibende Zeit: $12\,$min};
\draw[thick,fill=gray,opacity=0.5,rounded corners=2pt] (0,0) rectangle (10,0.5); 
%\draw[thick,fill=blue,opacity=0.5,rounded corners=2pt] (0.025,0.025) rectangle (7,0.475);  
    
\end{tikzpicture}
``` 
 
 <br>
 <br>
***********
```latex  @tikz
\begin{tikzpicture}[scale=1.5,>=latex]        
 
 
 \node[right] at (0,1) {Downloading... verbleibende Zeit: $12\,$min};
\draw[thick,fill=gray,opacity=0.5,rounded corners=2pt] (0,0) rectangle (10,0.5); 
\draw[thick,fill=blue,opacity=0.5,rounded corners=2pt] (0.025,0.025) rectangle (7,0.475);  
    
\end{tikzpicture}
``` 
 
 <br>

$1- \dfrac{12\,\text{min}}{40\,\text{min}} = 70\% $
***********
</div>

 


</section>






## Aufgabe 5

Bei Befragungen wurden jeweils insgesamt $44000$ Menschen interviewt. **Bestimme** die Anzahl der Menschen, die aus dem Kreisdiagramm die jeweiligen Antworten gaben.

  <br>  
  <br>

<section class="flex-container">

<div class="flex-child">
 
 <br>
 <br>

```latex  @tikz
\begin{tikzpicture}[scale=1.5,>=latex]        
 
 
    \foreach \start/\end/\middle/\percent/\anchor		/\color		/\name			/\smeter in 	{
							0			/90		/45			/25{,}0		 /above			/blue!		/a 						/1 				,
							90		/210	/150		/33{,}3		/above			/red!			/b						/1 						,
							210		/310	/260		/27{,}8		/below			/green!		/c						/1 						,
							310		/360	/340		/13{,}9		/right			/orange!	/d						/1 						 	}
  {
    \draw[fill=\color , opacity=0.25 , thick] (0,0) -- (\end:2.4cm) arc (\end:\start:2.4cm)
      node[opacity=0.99] at (\middle:1.5cm) {\percent \%};
    \draw (\middle:2.4cm) -- (\middle:2.65cm) ;
		\node (A) at (\middle:2.85cm)   {$\name$};
  };
    
\end{tikzpicture}
``` 
 
 <br>
 <br>
*********** 

$p_i  = \dfrac{W}{G} \quad \left| \cdot G \right. $  <br>
$G \cdot p_i  = W  $  <br>
$a: \;\; G \cdot p_a  =44000 \cdot 0,25 = 11000  $  <br>
$b: \;\; G \cdot p_b  =44000 \cdot 0,333 = 14652  $  <br>
$c: \;\; G \cdot p_c  =44000 \cdot 0,278 = 12232  $  <br>
$d: \;\; G \cdot p_d  =44000 \cdot 0,139 = 6116  $  <br>
***********
</div>

 


</section>






## Aufgabe 6

Ein gebrauchter PKW wurde für $12880$€ verkauft. Das waren $70\%$ des Neuwertes. **Berechne** den Neuwert.

  <br>  
  <br>

<section class="flex-container">

<div class="flex-child">
[[18400]] $€$   
*********** 

$p  = \dfrac{W}{G} \quad \left| \cdot G \right. $  <br>
$G \cdot p  = W  \quad \left| : p \right. $  <br>
$G  = \dfrac{W}{p}   $  <br>
$12880\,\text{€} : \dfrac{70}{100} = 12880\,\text{€} \cdot \dfrac{100}{70} = 18400 \,\text{€} $
***********
</div>

 


</section>



## Aufgabe 7

Es wurde eine Umgehungsstraße von $3500\,$m Länge gebaut. $37\%$ der Straße sind bereits fertiggestellt. **Berechne**, wie viel Meter noch gebaut werden müssen.

  <br>  
  <br>

<section class="flex-container">

<div class="flex-child">
[[2205]] $\,\text{m}$   
*********** 
 
$3500\,\text{m} \cdot (1-0,37) = 2205 \,\text{m} \qquad$
***********
</div>

 


</section>


## Aufgabe 8

Nach einer Mieterhöhung von $4\%$ muss eine Familie jetzt $883,60$€ an Miete zahlen. **Berechne**, wie hoch die Miete vor der Erhöhung war.

  <br>  
  <br>

<section class="flex-container">

<div class="flex-child">
[[849,615]] $\,\text{€}$   
*********** 
 
$883,60\,\text{€} \cdot \dfrac{100}{104} = 849,615 \,\text{€} \qquad$
***********
</div>

 


</section>



## Aufgabe 9

Eine Uhr wird mit einem Nettopreis von $109,24$€ beworben, sodass noch $19\%$ Steuern beim Kauf hinzu kommen. Da nach dem Kauf ein Mangel an der Uhr festgestellt wurde, gibt der Händler dem Kunden $10\%$ vom bezahlten Preis zurück. **Berechne**, wie viel Geld der Kunde für die Uhr ausgegeben hat. 

  <br>  
  <br>

<section class="flex-container">

<div class="flex-child">
[[116,996]] $\,\text{€}$   
*********** 
 
$109,24\,\text{€} \cdot  1,19  = 129,996 \,\text{€} \qquad$   <br>
$129,996\,\text{€} \cdot  0,9  = 116,996 \,\text{€} \qquad$ 
***********
</div>

 


</section>




## Aufgabe 10

Jedes Jahr bekommt ein Bankkunde $2\%$ Zinsen auf seine Ersparnisse. Hierbei wurden $4400$€ eingezahlt. **Berechne**, wie viel Geld sich nach drei Jahren auf dem Konto befinden.

  <br>  
  <br>


<section class="flex-container">

<div class="flex-child">
[[4669,3152]] $\,\text{€}$   
*********** 
 
$4400\,\text{€} \cdot 1,02 = 4488 \,\text{€} \qquad$   <br>
$4488\,\text{€} \cdot 1,02 = 4577,76 \,\text{€} \qquad$   <br>
$4577,76\,\text{€} \cdot 1,02 = 4669,3152 \,\text{€} \qquad$ 
***********
</div>

 


</section>



## Aufgabe 11

In der gegebenen Tabelle sind die absoluten Stimmen bei einer Umfrage für die Wahlmöglichkeiten und prozentuale Anteile dargestellt. \

  <br>  
  <br>

$a)\;\;$ **Fülle** die fehlenden Tabellenfelder **aus**. **Runde** auf drei Nachkommastellen bei den relativen Anteilen.

  <br> 
  <br>  

| Wahloption | absolute Stimmenanzahl |  relativer Stimmenanteil in $\%$ | 
| :------: | :------: | :------: |
| A     |   2600   |    [[18,056]]   |  
| B     |   4400   |    [[30,556]]   |  
| C     |   1900   |    [[21,528]]   |  
| D     |   3100   |    [[13,194]]   |  
| E     |   [[2400]]   |    $16,\bar{6}$  |  

  <br>  
  <br>

<section class="flex-container">

<div class="flex-child"> 


$b)\;\;$ **Zeichne** ein Kreisdiagramm zu den Werten aus der Tabelle.


  <br> 

*********** 
  
```latex  @tikz
\begin{tikzpicture}[scale=4,>=latex]        
 
\draw[thick,fill=red,opacity=0.95] (0,0) -- (0:1)  arc (0:-60:1) -- (0,0); \node at (-30:0.5) {$A$} ;
\draw[thick,fill=green,opacity=0.95] (0,0) -- (300:1)  arc (300:225:1) -- (0,0);  \node at (260:0.5) {$B$} ;
\draw[thick,fill=blue,opacity=0.95] (0,0) -- (225:1)  arc (225:115:1) -- (0,0);  \node at (170:0.5) {$C$} ;
\draw[thick,fill=orange,opacity=0.95] (0,0) -- (115:1)  arc (115:47.5:1) -- (0,0);  \node at (85:0.5) {$D$} ;
\draw[thick,fill=gray,opacity=0.95] (0,0) -- (47.5:1)  arc (47.5:0:1) -- (0,0);   \node at (22:0.5) {$E$} ;
\draw[thick] (0,0) circle (1cm);   
    
\end{tikzpicture}
``` 

***********
</div>

 


</section>
