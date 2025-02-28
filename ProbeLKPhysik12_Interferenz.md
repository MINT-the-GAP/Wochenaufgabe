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

# Probeleistungskontrolle für Physik - Klasse 12: Wellenoptik

<br>

Swipe (Wische) entweder weiter oder klicke unten links auf neben der Seitenzahl auf den Pfeil nach rechts.

<br>

Diese Probearbeit hat mehr Aufgaben als die richtige Arbeit, damit du genug zum Üben hast. Es sind viele verschiedene Aufgabentypen abgebildet, sodass du alles nochmal bei der Bearbeitung dieser Aufgaben wiederholst.

<br>

$$
\textbf{Weitere Hilfen:}  \begin{align*}
\text{Einfachspalt:}\;\; 	& \Delta s =  \frac{2k+1}{2} \lambda  = b \sin  \left(\alpha\right)    \qquad \text{mit:} \;\; k \in \mathbb{N} \;\; ,   \\
\text{Doppelspalt:}\;\; 	& \Delta s =  k \lambda   = d \sin  \left(\alpha\right)    \qquad \text{mit:} \;\; k \in \mathbb{N} \;\; ,   \\
\text{Gitter:}\;\; 				& \Delta s =  k \lambda   = g \sin  \left(\alpha\right)    \qquad \text{mit:} \;\; k \in \mathbb{N} \;\; .   
\end{align*} 
$$

## Aufgabe 1

Es wird eine Schale betrachtet, die mit Wasser gefüllt ist. In der Schale steht ein Spiegel. Nun wird mit einer Taschenlampe auf den Spiegel geleuchtet und die Reflexion des Lichtes am Spiegel an einem Schirm beobachtet. **Beschreibe** und **Erkläre** die Beobachtungen, die gemacht werden können.


<center>

```latex  @tikz
\begin{tikzpicture}[scale=1,>=latex]       

				
				
				\draw[blue!50, fill=blue!50]  (0,-0.5) -- (0,-2) -- (-4,-2) -- (-4,-0.5);
				\draw[ultra thick]  (0,0) -- (0,-2) -- (-4,-2)  node[midway, below] {\Large Schale mit Wasser} -- (-4,0);
				\draw[ultra thick]  (-2,-2) -- (-5,1)  node[above] {\Large Spiegel} ;
				\draw[dashed, very thick] (-3,-2) to[out=100,in=210] (-2.75,-1.25); \node at (-2.66,-1.75) {\Large $\beta$}; 
				
				
				\draw[dashed, very thick] (1.5,2.5) -- (3,2.5)  ; 
				\draw[dashed, very thick] (2.5,2.5) to[out=80,in=330] (2.0,3.5); \node at (2.15,2.75) {\Large $\alpha$}; 
				\begin{scope}[rotate=40]
				\draw[<->, ultra thick, dashed] (3.85,-0.66)  arc (-45:45:3); 
				\draw[thick, fill=gray!60] (2,1) rectangle (5,2) node[midway,rotate=40] {\large Taschenlampe}; 
				\draw[yellow!50, fill=yellow!50] (2,1.2) -- (2,1.8) -- (1,2) -- (1,1) -- (2,1.2); 					
				\end{scope}
    
\end{tikzpicture}
```

</center>



[[!]]
<script>true</script>
************
Auf dem Schirm wird das komplette Farbspektrum des Lichts.
<center>

```latex  @tikz
\begin{tikzpicture}[x=1mm,y=1mm, scale=1.25, xscale=-0.5]
  \foreach \wav in {400, 400.25,...,750}{
      \definecolor{tmpcolor}{wave}{\wav}
      \colorlet{mycolor}[rgb]{tmpcolor}
   \begin{scope}[scale=0.475]
		 \fill[fill=mycolor,draw=mycolor,ultra thin] (\wav,1) rectangle +(0.25mm,50mm);
	 \end{scope}   
  }   

\end{tikzpicture}

```

</center>
An der Reflexion kann erkannt werden, dass die Ränder der Reflexion einmal rötlich und einmal bläulich sind. Unter besonderen Winkeln kann man so sogar alle Farben des Regenbogens entdecken. Die Aufreihung dieser Farben wird Farbspektrum genannt. Man kann daraus schlussfolgern, dass weißes Licht aus allen anderen Farben zusammengesetzt ist. Da das Licht erst durchs Wasser diesen Effekt offenbart, kann auch geschlussfolgert werden, dass sich die einzelnen Farben anders beim Wechsel des Mediums Luft zu Wasser verhalten. Die Farben werden unterschiedlich gebrochen. Dieses Phänomen wird Dispersion genannt.

************

<br>
<br>
<br>
<br>
<br>
<br>
<br>


## Aufgabe 2


Bei einem Doppelspaltexperiment mit einem Spaltabstand von $0,375\,$mm wurde auf einem Schirm in $3,2\,$m Entfernung der Abstand zwischen dem 3. linksseitigen und 3. rechtsseitigem Maximum von $27,8\,$mm gemessen. **Bestimme** gerundet auf volle Nanometer die Wellenlänge des verwendeten Lasers. **Gib** die Farbe des Lasers **an**.


<br>

$\lambda \approx$ [[  543  ]] nm
***********
$$
\begin{align*}
  k \lambda &= d \sin \alpha  \qquad \text{mit:} \;\;   \alpha = \arctan \left(\frac{h}{l}\right)  \\
  \lambda &= \frac{d}{k} \sin  \left( \arctan \left(\frac{h}{l}\right) \right) \approx 543\,\text{nm} \qquad    \\
\end{align*}
$$

Die Farbe des Lasers ist grün.

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

**Vervollständige** den Lückentext.

Wenn das durch [[  Beugung  ]] am Spalt entstehende Interferenzmuster vertikal ist, dann ist die Orientierung des Spaltes [[  horizontal  ]]. \
Je kleiner der Spalt ist, desto [[  größer  ]] sind die Abstände der Interferenzmaxima auf dem [[  Schirm  ]]. \
Je größer der Abstand zwischen Schirm und Spalt ist, desto [[  größer  ]] sind die Abstände  der Interferenzmaxima auf dem Schirm. \
Bei einem Gitter sind die [[  Abstände  ]] zwischen den Interferenzmaxima größer als bei einem Doppelspalt. 

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>



## Aufgabe 4


Ein monochromatisches Licht befindet sich in einem Medium mit dem Brechungsindex $n=1,459$. Das Licht trifft unter dem Winkel $\alpha$ auf die Mediumsgrenze hin zu Luft. **Berechne** unter welchem Winkel der Lichtstrahl dem Medium nicht entkommen kann und somit total reflektiert wird. **Runde** falls nötig auf drei Nachkommastellen.


<br>

$\alpha=$ [[  43,267  ]]$^\circ$
***********
$$
\begin{align*}
  \dfrac{\sin(\alpha)}{\sin(\beta)} & = \dfrac{n_L}{n_{\alpha}}  \quad \left| \cdot  \sin(\beta) \right. \\
  \sin(\alpha) & = \dfrac{n_L}{n_{\alpha}} \sin(\beta)   \\
 \Rightarrow\;\; \alpha & = \arcsin \left( \dfrac{n_L}{n_{\alpha}} \sin(\beta) \right)  \\
  \alpha & = \arcsin \left( \dfrac{1}{1,459} \sin(90^\circ) \right)  \\
  \alpha & \approc 43,267^\circ
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




## Aufgabe 5


Bei einem Gitterexperiment wurde ein Gitter mit $4250$ Spalte auf $2\,$cm sowie ein Laser mit der Wellenlänge von $635\,$nm verwendet. Die Abstände auf dem Schirm vom 0. bis zum 4. Maximum betrugen $1,75\,$m. **Berechne** gerundet auf drei Nachkommastellen den Abstand zwischen Schirm und Gitter.


<br>

$l\approx$ [[  2,729  ]] m
***********
$$
\begin{align*}
  k \lambda &= g \sin \alpha  \qquad \text{mit:} \;\;   \alpha = \arctan \left(\frac{h}{l}\right)  \\
 k \lambda &= g \sin  \left( \arctan \left(\frac{h}{l}\right) \right)  \quad \left| :g \right.   \\
 \dfrac{k \lambda}{ g} &=  \sin  \left( \arctan \left(\frac{h}{l}\right) \right)     \\
\Rightarrow\;\; \arcsin  \left(\dfrac{k \lambda}{ g} \right)  &=  \arctan \left(\frac{h}{l}\right)     \\
\Rightarrow\;\; \tan \left( \arcsin  \left(\dfrac{k \lambda}{ g} \right) \right)  &=  \frac{h}{l}   \quad \left| \cdot l \right.     \\
l \tan \left( \arcsin  \left(\dfrac{k \lambda}{ g} \right) \right)  &=  h   \quad \left| : \tan \left( \arcsin  \left(\dfrac{k \lambda}{ g} \right) \right) \right.     \\
l   &=  \frac{h}{\tan \left( \arcsin  \left(\dfrac{k \lambda}{ g} \right) \right)}  \quad \text{mit:} \;\; g = \dfrac{0,02\,\text{m}}{4250}   \\
l   & \approx  2,729 \,\text{m}  \\
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