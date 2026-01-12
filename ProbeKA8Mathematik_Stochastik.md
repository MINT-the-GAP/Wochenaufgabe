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


/* SVG-Rahmen */
svg.tree3 {
  width: 900px;          /* gewünschte Gesamtbreite */
  max-width: 100%;
  height: auto;
  font-family: sans-serif;
}

/* ALLES, was im foreignObject steht */
svg.tree3 foreignObject {
  font-size: 0.55em;        /* Basisgröße für Text & TeX */
  line-height: 1.4;
  text-align: center;
}

/* LiaScript-Quizcontainer im foreignObject */
svg.tree3 foreignObject .lia-quiz {
  display: inline-flex;
  flex-direction: column;
  align-items: center;
  gap: 0;                 /* KEINE extra Lücke mehr zwischen Input / Buttons / Feedback */
}

/* Alle automatischen Abstände im Quiz-Block killen */
svg.tree3 foreignObject .lia-quiz * {
  margin: 0 !important;
  padding: 0 !important;
}

/* explizit alle <br>, die LiaScript ggf. einfügt, unsichtbar machen */
svg.tree3 foreignObject .lia-quiz br {
  display: none !important;
  height: 0 !important;
  line-height: 0 !important;
}

/* Eingabefeld (aus [[ ... ]]) */
svg.tree3 foreignObject .lia-input,
svg.tree3 foreignObject input {
  font-size: 1.3em !important;
  width: 2.8em;
  padding: 0.1em !important;
  box-sizing: border-box;
  line-height: 1.0 !important;
}

/* Prüfen-/Auflösen-Buttons im foreignObject verkleinern und nach oben ziehen */
svg.tree3 foreignObject .lia-btn,
svg.tree3 foreignObject button {
  font-size: 1.3em !important;
  padding: 0.1em 0.3em !important;
  line-height: 1.0 !important;
  margin-top: -1.4em !important;
}

/* Feedback-Text (Richtig/Falsch/Aufgelöst) an Boxbreite anpassen */
svg.tree3 foreignObject .lia-quiz span,
svg.tree3 foreignObject .lia-quiz p,
svg.tree3 foreignObject .lia-quiz div {
  max-width: 100% !important;
  white-space: normal !important;
  word-wrap: break-word;
  margin-top: 0.1em !important;
  text-align: center;
}


/* SVG-Rahmen */
svg.tree2 {
  width: 750px;          /* gewünschte Gesamtbreite */
  max-width: 100%;
  height: auto;
  font-family: sans-serif;
}

/* ALLES, was im foreignObject steht */
svg.tree2 foreignObject {
  font-size: 10px;        /* Basisgröße für Text & TeX */
  line-height: 1.2;
  text-align: center;
}

/* LiaScript-Quizcontainer im foreignObject */
svg.tree2 foreignObject .lia-quiz {
  display: inline-flex;
  flex-direction: column;
  align-items: center;
  gap: 0;                 /* KEINE extra Lücke mehr zwischen Input / Buttons / Feedback */
}

/* Alle automatischen Abstände im Quiz-Block killen */
svg.tree2 foreignObject .lia-quiz * {
  margin: 0 !important;
  padding: 0 !important;
}

/* explizit alle <br>, die LiaScript ggf. einfügt, unsichtbar machen */
svg.tree2 foreignObject .lia-quiz br {
  display: none !important;
  height: 0 !important;
  line-height: 0 !important;
}

/* Eingabefeld (aus [[ ... ]]) */
svg.tree2 foreignObject .lia-input,
svg.tree2 foreignObject input {
  font-size: 10px !important;
  width: 2.5em;
  padding: 0.1em !important;
  box-sizing: border-box;
  line-height: 1.0 !important;
}

/* Prüfen-/Auflösen-Buttons im foreignObject verkleinern und nach oben ziehen */
svg.tree2 foreignObject .lia-btn,
svg.tree2 foreignObject button {
  font-size: 10px !important;
  padding: 0.1em 0.3em !important;
  line-height: 1.0 !important;
  /* kritischer Punkt: die „zusätzliche Zeile“ kompensieren */
  margin-top: -1.4em !important;
}


@end

formula: \carry   \textcolor{red}{\scriptsize #1}
formula: \digit   \rlap{\carry{#1}}\phantom{#2}#2
formula: \permil  \text{‰}

import: https://raw.githubusercontent.com/liaTemplates/algebrite/master/README.md
import: https://raw.githubusercontent.com/LiaTemplates/Tikz-Jax/main/README.md
import: https://raw.githubusercontent.com/LiaTemplates/mermaid_template/0.1.4/README.md

script: https://cdn.jsdelivr.net/gh/LiaTemplates/Tikz-Jax@main/dist/index.js

@round
<script>
  let value = `@input`;
  if (value.startsWith("@")) {
    ""
  } else {
    value = JSON.parse(value);
    value = value[0]
    value = value.replace(/,/g, ".");
    value = parseFloat(value);
    value = Math.round(value * Math.pow(10,@1)) / Math.pow(10,@1);
    value == @0
  }
</script>
@end

-->

# Probeklassenarbeit für Mathematik - Klasse 8: Grundlagen der Stochastik

<br>

> Letztes Update am 09.01.2026 gegen 18 Uhr

<br>

Swipe (Wische) entweder weiter oder klicke unten links auf neben der Seitenzahl auf den Pfeil nach rechts.

<br>

Diese Probearbeit hat mehr Aufgaben als die richtige Arbeit, damit du genug zum Üben hast. Es sind viele verschiedene Aufgabentypen abgebildet, sodass du alles nochmal bei der Bearbeitung dieser Aufgaben wiederholst.

## Aufgabe 1 - Wahrscheinlichkeiten

In den dargestellten Gefäßen befinden sich Kugeln unterschiedlicher Farben. 



<!-- Stochastik Grundlagen 0028 -->



<section class="flex-container">

<div class="flex-child">
__$a)\;\;$__ 

<!-- style="width:350px" -->
![](https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/Repetitorium/Kap7/urne23.png)


</div>
<div class="flex-child">


**Gib** die absolute Häufigkeit der blauen Kugeln **an**.\
$\#(B)=$ [[  9  ]]

**Gib** die relative Häufigkeit der nicht grauen Kugeln **an**.\
$p(\bar{G})=$ [[ 13/19  ]]
@Algebrite.check(13/19)

**Gib** die Wahrscheinlichkeit **an**, eine blaue Kugel zu ziehen.\
$P(R)=$ [[  9/19  ]]
@Algebrite.check(9/19)

**Gib** die Chance **an**, eine violette oder graue Kugel im Vergleich zu den anderen Kugeln zu ziehen.\
$R(\bar{B})=$ [[  10:9  ]]

**Gib** die Wahrscheinlichkeit **an**, eine blaue oder graue Kugel zu ziehen.\
$P(B \cup G)=$ [[  15/19  ]]
@Algebrite.check(15/19)

**Gib** die Chance **an**, eine violette Kugel im Vergleich zu den anderen Kugeln zu ziehen.\
$R(V)=$ [[  4:15  ]]


</div>
</section>

---



<section class="flex-container">

<div class="flex-child">
__$b)\;\;$__

<!-- style="width:350px" -->
![](https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/Repetitorium/Kap7/urne24.png)


</div>
<div class="flex-child">


**Gib** die absolute Häufigkeit der grünen Kugeln **an**.\
$\#(G)=$ [[  10  ]]

**Gib** die relative Häufigkeit der orangen Kugeln **an**.\
$p(O)=$ [[  5/20  ]]
@Algebrite.check(5/20)

**Gib** die Wahrscheinlichkeit **an**, keine rote Kugel zu ziehen.\
$P(\bar{R})=$ [[  15/20  ]]
@Algebrite.check(15/20)

**Gib** die Chance **an**, eine grüne Kugel im Vergleich zu den anderen Kugeln zu ziehen.\
$R(G)=$ [[  10:10  ]]

**Gib** die Wahrscheinlichkeit **an**, eine orange oder grüne Kugel zu ziehen.\
$P(O \cup G)=$ [[  15/20  ]]
@Algebrite.check(15/20)

**Gib** die Wahrscheinlichkeit **an**, keine grüne Kugel zu ziehen.\
$P(\bar{G})=$ [[  10/20  ]]
@Algebrite.check(10/20)


</div>
</section>


---


<section class="flex-container">

<div class="flex-child">
__$c)\;\;$__

<!-- style="width:350px" -->
![](https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/Repetitorium/Kap7/urne25.png)


</div>
<div class="flex-child">


**Gib** die absolute Häufigkeit der violetten und grauen Kugeln **an**.\
$\#(V \cup G)=$ [[  11  ]]

**Gib** die relative Häufigkeit der blauen Kugeln **an**.\
$p(B)=$ [[  8/22  ]]
@Algebrite.check(8/22)

**Gib** die Wahrscheinlichkeit **an**, keine grüne Kugel zu ziehen.\
$P(G \cup B \cup V)=$ [[  18/22  ]]
@Algebrite.check(18/22)

**Gib** die Chance **an**, eine graue Kugel im Vergleich zu den anderen Kugeln zu ziehen.\
$R(R)=$ [[  7:15  ]]

**Gib** die Wahrscheinlichkeit **an**, keine violette oder blaue Kugel zu ziehen.\
$P(\bar{B} \cup \bar{V})=$ [[  11/22  ]]
@Algebrite.check(11/22)

**Gib** die Chance **an**, keine violette Kugel im Vergleich zu den anderen Kugeln zu ziehen.\
$R(\bar{V})=$ [[  19:3  ]]


</div>

</section>






## Aufgabe 2 - Mengenauswertung

Gegeben sei die folgende Ergebnismenge: \
$\{ 83,46,55,64,91,75,61,39,84,55,47 \}$


<section class="flex-container">

<div class="flex-child">

<!-- data-solution-button="5" -->
__$a)\;\;$__ **Gib** die Spannweite **an**.\
$R=$ [[ 52  ]]
*******************
$R = x_{max} - x_{min} = 91 - 39 = 52$
*******************


</div>
<div class="flex-child">

<!-- data-solution-button="5" -->
__$b)\;\;$__ **Gib** den Median **an**.\
$\tilde{x}=$ [[  61  ]]
*******************
$\{ 39,46,47,55,55,\textcolor{red}{61},64,75,83,84,91 \}$
*******************


</div>
<div class="flex-child">

<!-- data-solution-button="5" -->
__$c)\;\;$__ **Gib** das arithmetische Mittel gerundet auf drei Nachkommastellen **an**.\
$\bar{x}=$ [[  63,636  ]]


</div> 

</section>






## Aufgabe 3 - Erweiterte Mengenauswertung

$a)\;\;$ Bei einem Glückspiel erhält ein Spieler beim Würfeln mit zwei vierseitgen Würfeln 15€ ausgezahlt, wenn dieser einen Pasch erwürfelt. Ansonsten würde der Spieler nichts bekommen. **Berechne** die Startgebühr, sodass es ein faires Spiel ist.


<!-- data-solution-button="5" -->
[[  5  ]] 
@Algebrite.check(5)
**********
$$
\begin{align*}
  \text{Gewinnereignisse:}& \left\{ \left\{ 1;1 \right\}; \left\{ 2;2 \right\};\left\{ 3;3 \right\};\left\{ 4;4 \right\} \right\} \\
  \text{Verlustereignisse:}& \left\{ \left\{ 1;2 \right\}; \left\{ 2;1 \right\};\left\{ 1;3 \right\};\left\{ 3;1 \right\} ;\left\{ 3;2 \right\};\left\{ 2;3 \right\} ;\left\{ 4;1 \right\} ;\left\{ 4;2 \right\} ;\left\{ 4;3 \right\} ;\left\{ 3;4 \right\} ;\left\{ 2;4 \right\} ;\left\{ 1;4 \right\}  \right\} \\
  P(G) & = \dfrac{4}{16} = \dfrac{1}{4} \\
  \bar{x} \stackrel{!}{=} 0 & = \dfrac{1}{4} \cdot 15\text{€} + \dfrac{3}{4} x \quad \left| \cdot 4 \right. \\
   0 & = 15\text{€} + 3 x \quad \left| -15\text{€} \right. \\
   -15\text{€} & = 3 x \quad \left| :3 \right. \\
   -5\text{€} & =  x \\
\end{align*}
$$
Eine Startgebühr von 5€ wäre fair.
**********

$b)\;\;$ Gegeben sei eine Menge $\{ 97,21,34,17,86,54,75,29,24,89,31 \}$. Bestimme die Zahl, die der Menge hingefügt werden muss, sodass der Median $\tilde{x}=42,5$ wäre.

<!-- data-solution-button="5" -->
[[  51  ]] 
@Algebrite.check(51)
**********
$\{ 17,21,24,29,31,34,\textcolor{red}{51},54,75,86,89,97 \}$
**********

$c)\;\;$ Gegeben sei eine Menge $\{ 97,21,34,17,86,54,75,29,24,89,31 \}$. Bestimme die Anzahl der Elemente, die mindestens hinzugefügt werden müssen, sodass der Median $\tilde{x}=75$ wäre.

<!-- data-solution-button="5" -->
[[  4  ]] 
@Algebrite.check(4)
**********
$\{ 17,21,24,29,31,34,54,75,86,89,97,\textcolor{red}{x},\textcolor{red}{x},\textcolor{red}{x},\textcolor{red}{x} \}$
**********



$d)\;\;$ Gegeben sei eine Menge $\{ 90,21,34,17,86,54,75,29,24,89,31 \}$. Berechne die Differenz zwischen dem Median und dem arithmetischen Mittel.


<!-- data-solution-button="5" -->
[[  16  ]] 
@Algebrite.check(16)
**********
$$
\begin{align*}
\{ 17,21,24,29,31,\textcolor{red}{34},54,75,86,89,90 \} \;\;\Rightarrow\;\; \tilde{x} &= 34 \\
\dfrac{17+21+24+29+31+34+54+75+86+89+90}{11} \;\;\Rightarrow\;\; \bar{x} &= 50 \\
\bar{x} - \tilde{x} & = 16
\end{align*}
$$
**********







## Aufgabe 4 - Kombinatorik

<!-- Chance 0025 -->


**Bestimme** die Anzahl der Permutationen.



<section class="flex-container">

<div class="flex-child">

__$a)\;\;$__ Es gibt $5$ unterschiedliche Kugeln. 

<!-- data-solution-button="5" -->
[[  120    ]] 
**********
$6! = 720$
**********

</div>
<div class="flex-child">


__$b)\;\;$__ Es gibt $13$ rote und $2$ blaue Kugeln.

<!-- data-solution-button="5" -->
[[  105    ]] 
**********
$\dfrac{15!}{13!2!} = 105$
**********


</div>
<div class="flex-child">


__$c)\;\;$__ Es gibt $1$ rote, $2$ grüne und $9$ blaue Kugeln.

<!-- data-solution-button="5" -->
[[   660   ]] 
**********
$\dfrac{12!}{9!2!1!} = 660$
**********

</div>
</section>



## Aufgabe 5 - Baumdiagramme 1



**Gib** die im gezeigten Baumdiagramm fehlen Werte **an**.




<!-- data-group="true" data-show-partial-solution="true"  data-text-solved="Richtig!"  data-text-failed="Falsch!"  data-text-resolved="Aufgelöst!" -->
<svg class="tree2" viewBox="0 0 480 320">

  <defs>
    <!-- Latex-ähnliche Pfeilspitze, innen weiß, schwarz umrandet -->
    <marker id="arrow-white" markerWidth="10" markerHeight="10"
            refX="7" refY="3.5" orient="auto" markerUnits="strokeWidth">
      <path d="M0,0 L7,3.5 L0,7 z"
            fill="white" stroke="black" stroke-width="0.6" />
    </marker>
  </defs>

  <!-- =======================
       Kanten des Baumdiagramms
       ======================= -->

  <!-- 1. Stufe: Start -> A und Start -> ¬A -->
  <line x1="200" y1="40" x2="103.12" y2="117.52"
        stroke="black" stroke-width="3.5" stroke-linecap="butt" />
  <line x1="200" y1="40" x2="100" y2="120"
        stroke="white" stroke-width="2.25" stroke-linecap="butt"
        marker-end="url(#arrow-white)" />

  <line x1="200" y1="40" x2="296.88" y2="117.52"
        stroke="black" stroke-width="3.5" stroke-linecap="butt" />
  <line x1="200" y1="40" x2="300" y2="120"
        stroke="white" stroke-width="2.25" stroke-linecap="butt"
        marker-end="url(#arrow-white)" />

  <!-- 2. Stufe links: A -> B|A und A -> ¬B|A -->
  <line x1="100" y1="140" x2="41.8" y2="256.44"
        stroke="black" stroke-width="3.5" stroke-linecap="butt" />
  <line x1="100" y1="140" x2="40" y2="260"
        stroke="white" stroke-width="2.25" stroke-linecap="butt"
        marker-end="url(#arrow-white)" />

  <line x1="100" y1="140" x2="158.2" y2="256.44"
        stroke="black" stroke-width="3.5" stroke-linecap="butt" />
  <line x1="100" y1="140" x2="160" y2="260"
        stroke="white" stroke-width="2.25" stroke-linecap="butt"
        marker-end="url(#arrow-white)" />

  <!-- 2. Stufe rechts: ¬A -> B|¬A und ¬A -> ¬B|¬A -->
  <line x1="300" y1="140" x2="241.8" y2="256.44"
        stroke="black" stroke-width="3.5" stroke-linecap="butt" />
  <line x1="300" y1="140" x2="240" y2="260"
        stroke="white" stroke-width="2.25" stroke-linecap="butt"
        marker-end="url(#arrow-white)" />

  <line x1="300" y1="140" x2="358.2" y2="256.44"
        stroke="black" stroke-width="3.5" stroke-linecap="butt" />
  <line x1="300" y1="140" x2="360" y2="260"
        stroke="white" stroke-width="2.25" stroke-linecap="butt"
        marker-end="url(#arrow-white)" />


  <!-- =======================
       Knoten-Beschriftungen
       ======================= -->

  <!-- Start (ungekippt, im Zentrum oben) -->
  <foreignObject x="168" y="12" width="64" height="40">
    <b><big><big>Start</big></big></b>
  </foreignObject>

  <!-- Knoten der 1. Stufe: P(A), P(¬A) -->
  <foreignObject x="76" y="122" width="90" height="40">
    $P(A) = $ [[  7/8  ]]
  </foreignObject>

  <foreignObject x="276" y="122" width="90" height="40">
    $P(\bar{A}) = 12,5\% $  
  </foreignObject>

  <!-- Blattknoten: P(B ∩ A), … -->
  <foreignObject x="12" y="265" width="60" height="50">
    $P(B \cap A) \\ = $ [[  7/10  ]]
  </foreignObject>

  <foreignObject x="132" y="265" width="60" height="50">
    $P(\bar{B} \cap A) \\ = $  [[  7/40  ]]
  </foreignObject>

  <foreignObject x="212" y="265" width="60" height="50">
    $P(B \cap \bar{A}) \\ = $  [[  1/32  ]]
  </foreignObject>

  <foreignObject x="332" y="265" width="60" height="50">
    $P(\bar{B} \cap \bar{A}) \\ = $  [[  3/32  ]]
  </foreignObject>


  <!-- ===================================
       Pfad-Beschriftungen mit Eingabefeld
       (Boxen um den Pfad-Mittelpunkt zentriert)
       =================================== -->

  <!-- 1. Stufe: P(A), Pfad-Mittelpunkt (150,80) -->
  <foreignObject x="90" y="60" width="120" height="60"
                 transform="rotate(-40 150 80)">
    <!-- data-text-solved="Richtig!"  data-text-failed="Falsch!"  data-text-resolved="Aufgelöst!"  -->
    $P(A) =  $ [[  7/8  ]]
  </foreignObject>

  <!-- 1. Stufe: P(¬A), Pfad-Mittelpunkt (250,80) -->
  <foreignObject x="190" y="60" width="120" height="60"
                 transform="rotate(40 250 80)">
    <!-- data-text-solved="Richtig!"  data-text-failed="Falsch!"  data-text-resolved="Aufgelöst!"  -->
    $P(\bar{A}) =$ [[  1/8  ]] 
  </foreignObject>


  <!-- 2. Stufe links: P(B|A), Pfad-Mittelpunkt (70,200) -->
  <foreignObject x="10" y="170" width="120" height="60"
                 transform="rotate(-64 79 195)">
    <!-- data-text-solved="Richtig!"  data-text-failed="Falsch!"  data-text-resolved="Aufgelöst!"  -->
    $P(B \mid A) = \frac{4}{5} $ 
  </foreignObject>

  <!-- 2. Stufe links: P(¬B|A), Pfad-Mittelpunkt (130,200) -->
  <foreignObject x="70" y="170" width="120" height="60"
                 transform="rotate(64 121 195)">
    <!-- data-text-solved="Richtig!"  data-text-failed="Falsch!"  data-text-resolved="Aufgelöst!"  -->
    $P(\bar{B} \mid A) =  $[[   1/5   ]]
  </foreignObject>


  <!-- 2. Stufe rechts: P(B|¬A), Pfad-Mittelpunkt (270,200) -->
  <foreignObject x="210" y="170" width="120" height="60"
                 transform="rotate(-64 279 195)">
    <!-- data-text-solved="Richtig!"  data-text-failed="Falsch!"  data-text-resolved="Aufgelöst!"  -->
    $P(B \mid \bar{A}) =$   [[   1/4   ]]
  </foreignObject>

  <!-- 2. Stufe rechts: P(¬B|¬A), Pfad-Mittelpunkt (330,200) -->
  <foreignObject x="270" y="170" width="120" height="60"
                 transform="rotate(64 321 195)">
    <!-- data-text-solved="Richtig!"  data-text-failed="Falsch!"  data-text-resolved="Aufgelöst!"  -->
    $P(\bar{B} \mid \bar{A}) = 0,75$ 
  </foreignObject>

</svg>
@Algebrite.check([ 7/8 ; 7/10 ; 7/40 ; 1/32 ; 3/32 ; 7/8 ; 1/8 ; 1/5 ; 1/4 ])




## Aufgabe 6 - Baumdiagramme 2


In einem Gefäß befinden sich 5 schwarze (S), 7 grüne (G) und 11 weiße (W) Kugeln für zwei Ziehungen mit Zurücklegen. 





 __$a) \;\;$__ **Skizziere** ein Baumdiagramm für den beschriebenen Fall. 



[[!]]
<script>true</script>
*************




<!-- data-group="true" data-show-partial-solution="true"
     data-text-solved="Richtig!" data-text-failed="Falsch!"
     data-text-resolved="Aufgelöst!" -->
<svg class="tree3" viewBox="70 0 850 700">

  <defs>
    <!-- Latex-ähnliche Pfeilspitze, innen weiß, schwarz umrandet -->
    <marker id="arrow-white" markerWidth="10" markerHeight="10"
            refX="7" refY="3.5" orient="auto" markerUnits="strokeWidth">
      <path d="M0,0 L7,3.5 L0,7 z"
            fill="white" stroke="black" stroke-width="0.6" />
    </marker>
  </defs>

  <!-- =======================
       Kanten des Baumdiagramms
       3 Ausgänge: S, G, W
       und je 3 Folgezweige
       ======================= -->

  <!-- Startknoten: (120, 360) -->

  <!-- 1. Stufe: Start -> S (etwas höher gesetzt) -->
  <line x1="120" y1="360" x2="320" y2="150"
        stroke="black" stroke-width="3.5" stroke-linecap="butt" />
  <line x1="120" y1="360" x2="320" y2="150"
        stroke="white" stroke-width="2.25" stroke-linecap="butt"
        marker-end="url(#arrow-white)" />

  <!-- 1. Stufe: Start -> G (Mitte) -->
  <line x1="120" y1="360" x2="320" y2="360"
        stroke="black" stroke-width="3.5" stroke-linecap="butt" />
  <line x1="120" y1="360" x2="320" y2="360"
        stroke="white" stroke-width="2.25" stroke-linecap="butt"
        marker-end="url(#arrow-white)" />

  <!-- 1. Stufe: Start -> W (etwas tiefer gesetzt) -->
  <line x1="120" y1="360" x2="320" y2="570"
        stroke="black" stroke-width="3.5" stroke-linecap="butt" />
  <line x1="120" y1="360" x2="320" y2="570"
        stroke="white" stroke-width="2.25" stroke-linecap="butt"
        marker-end="url(#arrow-white)" />


  <!-- 2. Stufe: je 3 Ausgänge von S, G, W, mit größeren Abständen:
       S-Kinder: y =  60, 150, 240
       G-Kinder: y = 300, 360, 420
       W-Kinder: y = 480, 570, 660
  -->

  <!-- Von S (320,150) zu (650, 60), (650,150), (650,240) -->

  <!-- S -> S | S -->
  <line x1="435" y1="150" x2="650" y2="60"
        stroke="black" stroke-width="3.5" stroke-linecap="butt" />
  <line x1="435" y1="150" x2="650" y2="60"
        stroke="white" stroke-width="2.25" stroke-linecap="butt"
        marker-end="url(#arrow-white)" />

  <!-- S -> G | S -->
  <line x1="435" y1="150" x2="650" y2="150"
        stroke="black" stroke-width="3.5" stroke-linecap="butt" />
  <line x1="435" y1="150" x2="650" y2="150"
        stroke="white" stroke-width="2.25" stroke-linecap="butt"
        marker-end="url(#arrow-white)" />

  <!-- S -> W | S -->
  <line x1="435" y1="150" x2="650" y2="240"
        stroke="black" stroke-width="3.5" stroke-linecap="butt" />
  <line x1="435" y1="150" x2="650" y2="240"
        stroke="white" stroke-width="2.25" stroke-linecap="butt"
        marker-end="url(#arrow-white)" />


  <!-- Von G (320,360) zu (650,300), (650,360), (650,420) -->

  <!-- G -> S | G -->
  <line x1="435" y1="360" x2="650" y2="300"
        stroke="black" stroke-width="3.5" stroke-linecap="butt" />
  <line x1="435" y1="360" x2="650" y2="300"
        stroke="white" stroke-width="2.25" stroke-linecap="butt"
        marker-end="url(#arrow-white)" />

  <!-- G -> G | G -->
  <line x1="435" y1="360" x2="650" y2="360"
        stroke="black" stroke-width="3.5" stroke-linecap="butt" />
  <line x1="435" y1="360" x2="650" y2="360"
        stroke="white" stroke-width="2.25" stroke-linecap="butt"
        marker-end="url(#arrow-white)" />

  <!-- G -> W | G -->
  <line x1="435" y1="360" x2="650" y2="420"
        stroke="black" stroke-width="3.5" stroke-linecap="butt" />
  <line x1="435" y1="360" x2="650" y2="420"
        stroke="white" stroke-width="2.25" stroke-linecap="butt"
        marker-end="url(#arrow-white)" />


  <!-- Von W (320,570) zu (650,480), (650,570), (650,660) -->

  <!-- W -> S | W -->
  <line x1="435" y1="570" x2="650" y2="480"
        stroke="black" stroke-width="3.5" stroke-linecap="butt" />
  <line x1="435" y1="570" x2="650" y2="480"
        stroke="white" stroke-width="2.25" stroke-linecap="butt"
        marker-end="url(#arrow-white)" />

  <!-- W -> G | W -->
  <line x1="435" y1="570" x2="650" y2="570"
        stroke="black" stroke-width="3.5" stroke-linecap="butt" />
  <line x1="435" y1="570" x2="650" y2="570"
        stroke="white" stroke-width="2.25" stroke-linecap="butt"
        marker-end="url(#arrow-white)" />

  <!-- W -> W | W -->
  <line x1="435" y1="570" x2="650" y2="660"
        stroke="black" stroke-width="3.5" stroke-linecap="butt" />
  <line x1="435" y1="570" x2="650" y2="660"
        stroke="white" stroke-width="2.25" stroke-linecap="butt"
        marker-end="url(#arrow-white)" />


  <!-- =======================
       Knoten-Beschriftungen
       ======================= -->

  <!-- Start -->
  <foreignObject x="35" y="345" width="120" height="50">
    <big><big><b>Start</b></big></big>
  </foreignObject>

  <!-- 1. Stufe: P(S), P(G), P(W) am Knoten -->
  <foreignObject x="295" y="140" width="160" height="80">
    <!-- data-text-solved="Richtig!" data-text-failed="Falsch!" data-text-resolved="Aufgelöst!" -->
    $P(S) = \frac{5}{23} $ 
  </foreignObject>

  <foreignObject x="295" y="350" width="160" height="80">
    <!-- data-text-solved="Richtig!" data-text-failed="Falsch!" data-text-resolved="Aufgelöst!" -->
    $P(G) = \frac{7}{23} $ 
  </foreignObject>

  <foreignObject x="295" y="560" width="160" height="80">
    <!-- data-text-solved="Richtig!" data-text-failed="Falsch!" data-text-resolved="Aufgelöst!" -->
    $P(W) = \frac{11}{23} $ 
  </foreignObject>


  <!-- 2. Stufe: Knoten-Beschriftungen (S/G/W-Bereiche am Ende der Zweige) -->

  <!-- Aus S kommend: S,S / G,S / W,S -->
  <foreignObject x="630" y="50" width="200" height="60">
    <!-- data-text-solved="Richtig!" data-text-failed="Falsch!" data-text-resolved="Aufgelöst!" -->
    $P(S \cap S) = \frac{5}{23} \cdot \frac{5}{23}$ 
  </foreignObject>

  <foreignObject x="630" y="140" width="200" height="60">
    <!-- data-text-solved="Richtig!" data-text-failed="Falsch!" data-text-resolved="Aufgelöst!" -->
    $P(G \cap S) = \frac{5}{23} \cdot \frac{7}{23}$ 
  </foreignObject>

  <foreignObject x="630" y="230" width="200" height="60">
    <!-- data-text-solved="Richtig!" data-text-failed="Falsch!" data-text-resolved="Aufgelöst!" -->
    $P(W \cap S) = \frac{5}{23} \cdot \frac{11}{23}$ 
  </foreignObject>

  <!-- Aus G kommend: S,G / G,G / W,G -->
  <foreignObject x="630" y="290" width="200" height="60">
    <!-- data-text-solved="Richtig!" data-text-failed="Falsch!" data-text-resolved="Aufgelöst!" -->
    $P(S \cap G) = \frac{7}{23} \cdot \frac{5}{23}$ 
  </foreignObject>

  <foreignObject x="630" y="350" width="200" height="60">
    <!-- data-text-solved="Richtig!" data-text-failed="Falsch!" data-text-resolved="Aufgelöst!" -->
    $P(G \cap G) = \frac{7}{23} \cdot \frac{7}{23}$ 
  </foreignObject>

  <foreignObject x="630" y="410" width="200" height="60">
    <!-- data-text-solved="Richtig!" data-text-failed="Falsch!" data-text-resolved="Aufgelöst!" -->
    $P(W \cap G) = \frac{}{23} \cdot \frac{11}{23}$ 
  </foreignObject>

  <!-- Aus W kommend: S,W / G,W / W,W -->
  <foreignObject x="630" y="470" width="200" height="60">
    <!-- data-text-solved="Richtig!" data-text-failed="Falsch!" data-text-resolved="Aufgelöst!" -->
    $P(S \cap W) = \frac{11}{23} \cdot \frac{5}{23}$ 
  </foreignObject>

  <foreignObject x="630" y="560" width="200" height="60">
    <!-- data-text-solved="Richtig!" data-text-failed="Falsch!" data-text-resolved="Aufgelöst!" -->
    $P(G \cap W) = \frac{11}{23} \cdot \frac{7}{23}$ 
  </foreignObject>

  <foreignObject x="630" y="650" width="200" height="60">
    <!-- data-text-solved="Richtig!" data-text-failed="Falsch!" data-text-resolved="Aufgelöst!" -->
    $P(W \cap W) = \frac{11}{23} \cdot \frac{11}{23}$ 
  </foreignObject>


  <!-- ===================================
       Pfad-Beschriftungen mit Eingabefeld
       passend zur Linienneigung
       =================================== -->

  <!-- 1. Stufe: P(S), P(G), P(W) auf den Pfaden -->

  <!-- Start -> S, Mittelpunkt ca. (220,255), Winkel ~ -45° -->
  <foreignObject x="160" y="228" width="130" height="80"
                 transform="rotate(-50 220 255)">
    <!-- data-text-solved="Richtig!" data-text-failed="Falsch!" data-text-resolved="Aufgelöst!" -->
    $P(S) = \frac{5}{23} $ 
  </foreignObject>

  <!-- Start -> G, Mittelpunkt (220,360), horizontal -->
  <foreignObject x="170" y="330" width="130" height="80">
    <!-- data-text-solved="Richtig!" data-text-failed="Falsch!" data-text-resolved="Aufgelöst!" -->
    $P(G) = \frac{7}{23} $ 
  </foreignObject>

  <!-- Start -> W, Mittelpunkt ca. (220,465), Winkel ~ +45° -->
  <foreignObject x="130" y="435" width="140" height="80"
                 transform="rotate(45 220 465)">
    <!-- data-text-solved="Richtig!" data-text-failed="Falsch!" data-text-resolved="Aufgelöst!" -->
    $P(W) = \frac{11}{23} $ 
  </foreignObject>


  <!-- 2. Stufe: Pfad-Beschriftungen von S aus -->
  <!-- Mittelpunkte:
       S->S|S: (485,105), S->G|S: (485,150), S->W|S: (485,195)
  -->

  <foreignObject x="490" y="100" width="150" height="80"
                 transform="rotate(-25 485 105)">
    <!-- data-text-solved="Richtig!" data-text-failed="Falsch!" data-text-resolved="Aufgelöst!" -->
    $P(S \mid S) = \frac{5}{23} \cdot \frac{5}{23}$ 
  </foreignObject>

  <foreignObject x="490" y="155" width="150" height="80">
    <!-- data-text-solved="Richtig!" data-text-failed="Falsch!" data-text-resolved="Aufgelöst!" -->
    $P(G \mid S) = \frac{5}{23} \cdot \frac{7}{23}$ 
  </foreignObject>

  <foreignObject x="490" y="175" width="150" height="80"
                 transform="rotate(25 485 195)">
    <!-- data-text-solved="Richtig!" data-text-failed="Falsch!" data-text-resolved="Aufgelöst!" -->
    $P(W \mid S) = \frac{5}{23} \cdot \frac{11}{23}$ 
  </foreignObject>


  <!-- 2. Stufe: Pfad-Beschriftungen von G aus -->
  <!-- Mittelpunkte:
       G->S|G: (485,330), G->G|G: (485,360), G->W|G: (485,390)
  -->

  <foreignObject x="490" y="315" width="150" height="80"
                 transform="rotate(-15 485 330)">
    <!-- data-text-solved="Richtig!" data-text-failed="Falsch!" data-text-resolved="Aufgelöst!" -->
    $P(S \mid G) = \frac{5}{23} \cdot \frac{7}{23}$ 
  </foreignObject>

  <foreignObject x="490" y="364" width="150" height="80">
    <!-- data-text-solved="Richtig!" data-text-failed="Falsch!" data-text-resolved="Aufgelöst!" -->
    $P(G \mid G) = \frac{7}{23} \cdot \frac{7}{23}$ 
  </foreignObject>

  <foreignObject x="490" y="380" width="150" height="80"
                 transform="rotate(15 485 390)">
    <!-- data-text-solved="Richtig!" data-text-failed="Falsch!" data-text-resolved="Aufgelöst!" -->
    $P(W \mid G) = \frac{7}{23} \cdot \frac{11}{23}$ 
  </foreignObject>


  <!-- 2. Stufe: Pfad-Beschriftungen von W aus -->
  <!-- Mittelpunkte:
       W->S|W: (485,525), W->G|W: (485,570), W->W|W: (485,615)
  -->

  <foreignObject x="490" y="523" width="150" height="80"
                 transform="rotate(-25 485 525)">
    <!-- data-text-solved="Richtig!" data-text-failed="Falsch!" data-text-resolved="Aufgelöst!" -->
    $P(S \mid W) = \frac{11}{23} \cdot \frac{5}{23}$ 
  </foreignObject>

  <foreignObject x="490" y="572" width="150" height="80">
    <!-- data-text-solved="Richtig!" data-text-failed="Falsch!" data-text-resolved="Aufgelöst!" -->
    $P(G \mid W) = \frac{11}{23} \cdot \frac{7}{23}$ 
  </foreignObject>

  <foreignObject x="490" y="592" width="150" height="80"
                 transform="rotate(25 485 615)">
    <!-- data-text-solved="Richtig!" data-text-failed="Falsch!" data-text-resolved="Aufgelöst!" -->
    $P(W \mid W) = \frac{11}{23} \cdot \frac{11}{23}$ 
  </foreignObject>

</svg>




*************





<section class="flex-container">

<div class="flex-child">




 __$b) \;\;$__ **Bestimme**, wie hoch die Wahrscheinlichkeit ist bei der ersten Ziehung eine grüne Kugel zu ziehen. Gib die Wahrscheinlichkeit in Prozent an.



<!-- data-solution-button="10"-->
[[  30,435  ]]$\%$.
@Algebrite.check2(700/23,0.001)
*************
$$
\begin{align*}
   \frac{7}{23} & \approx 30,435\%
\end{align*}
$$
*************




</div>
<div class="flex-child">



 __$c) \;\;$__ **Bestimme**, wie hoch die Wahrscheinlichkeit ist erst eine schwarze dann eine weiße Kugel hintereinander zu ziehen. Gib die Wahrscheinlichkeit in Prozent an. 



<!-- data-solution-button="10"-->
[[  10,397  ]]$\%$.
@Algebrite.check2(5500/529,0.001)
*************
$$
\begin{align*}
   \frac{5}{23} \cdot \frac{11}{23} \approx 10,397\%
\end{align*}
$$
*************




</div>
<div class="flex-child">




 __$d) \;\;$__ **Bestimme**, wie viele Pfade für die Möglichkeit existieren genau eine weiße und eine grüne Kugeln zu ziehen. 



<!-- data-solution-button="10"-->
[[   1   ]] 
@Algebrite.check(1)
*************
WW
*************




</div>
<div class="flex-child">




 __$e) \;\;$__ **Bestimme**, wie viele Pfade für die Möglichkeit existieren mindestens eine schwarze Kugel zu ziehen. 



<!-- data-solution-button="10"-->
[[   3   ]] 
@Algebrite.check(3)
*************
$$
  SS, SW, SG
$$
*************




</div>
<div class="flex-child">




 __$f) \;\;$__ **Bestimme**, wie viele Pfade für die Möglichkeit existieren von jeder Kugel eine zu ziehen, wenn drei mal gezogen würde. 




<!-- data-solution-button="10"-->
[[   6   ]] 
@Algebrite.check(6)
*************
$$
  SGW, SWG, WSG, GSW, GWS, WGS
$$
*************




</div>
<div class="flex-child">




 __$g) \;\;$__ **Bestimme**, wie hoch die Wahrscheinlichkeit ist jede Kugelfarbe bei drei Ziehungen mit Zurücklegen einmal zu ziehen. Gib die Wahrscheinlichkeit in Prozent an. 



<!-- data-solution-button="10"-->
[[  18,986  ]]$\%$.
@Algebrite.check2(231000/12167,0.001)
*************
$$
\begin{align*}
6 \cdot \frac{5}{23} \cdot \frac{7}{23} \cdot \frac{11}{23} \approx 18,986 \%
\end{align*}
$$
*************




</div>
<div class="flex-child">




 __$h) \;\;$__ **Bestimme**, wie hoch die Wahrscheinlichkeit bei drei Ziehungen mit Zurücklegen ist, bei der erst eine schwarze, dann eine grüne und abschließend eine weiße Kugel zu ziehen. Gib die Wahrscheinlichkeit in Prozent an. 



<!-- data-solution-button="10"-->
[[   3,164  ]]$\%$.
@Algebrite.check2(38500/12167,0.001)
*************
$$
\begin{align*}
   \frac{5}{23} \cdot \frac{7}{23} \cdot \frac{11}{23} \approx 3,164\%
\end{align*}
$$
*************




</div>
<div class="flex-child">




 __$i) \;\;$__ **Bestimme**, wie hoch die Wahrscheinlichkeit bei drei Ziehungen mit Zurücklegen ist höchstens zwei schwarze Kugel zu ziehen. Gib die Wahrscheinlichkeit in Prozent an. 



<!-- data-solution-button="10"-->
[[  86,241  ]]$\%$.
@Algebrite.check2(1049300/12167,0.001)
*************
$$
\begin{align*}
  1 -  \left(\frac{7}{23}\right)^3 -  \left(\frac{11}{23}\right)^3 \approx 86,241 \%
\end{align*}
$$
*************



</div>
</section>





## Aufgabe 7 - Lineare Funktionen

**Fülle** die leeren Felder der Wertetabelle für die gegebene Funktion **aus**.




__$a)\;\;$__ Gegeben sei die lineare Funktion $f(x) = 5 \cdot x - 2$. 

<!-- data-type="none"
data-sortable="false" data-show-partial-solution="true" data-solution-button="10"  -->
|   x   |    3     |     5    |    8     |    11    |
| :---: | :------: | :------: | :------: | :------: |
|  f(x) | [[ 12 ]] | [[ 23 ]] | [[ 38 ]] | [[ 53 ]] |



__$b)\;\;$__ Gegeben sei die lineare Funktion $f(x) = 3 \cdot x + 7$. 


<!-- data-type="none"
data-sortable="false" data-show-partial-solution="true" data-solution-button="10"  -->
|   x   | [[  2 ]] |     7    | [[ 12 ]] |    15    |
| :---: | :------: | :------: | :------: | :------: |
|  f(x) |    13    | [[ 28 ]] |    43    | [[ 52 ]] |



__$c)\;\;$__ Gegeben sei die lineare Funktion $f(x) = \dfrac{5}{3} \cdot x + \dfrac{3}{4}$. Berechne die Nullstelle (die Stelle, an der der Graph die Abszisse schneidet). 

<!-- data-solution-button="10"-->
[[  -0,45  ]] 
@Algebrite.check(-9/20)
*************
$$
\begin{align*}
  f(x) \stackrel{!}{=} 0 &= \dfrac{5}{3} \cdot x + \dfrac{3}{4}  \quad \left| -\dfrac{3}{4} \right. \\
   -\dfrac{3}{4} &= \dfrac{5}{3} \cdot x  \quad \left| : \dfrac{5}{3} \right. \\
    x &=  -\dfrac{3}{4} : \dfrac{5}{3} \\
    x & =  -\dfrac{3}{4} \cdot  \dfrac{3}{5} \\
    x & =  -\dfrac{9}{20}  \\
\end{align*}
$$
*************

__$d)\;\;$__ Gegeben sei die lineare Funktion $f(x) = \dfrac{7}{8} \cdot x + \dfrac{6}{5}$. Berechne den Ordinatenabschnitt (der Funktionswert, bei dem der Graph die Ordinate schneidet). 

<!-- data-solution-button="10"-->
[[   6/5   ]] 
@Algebrite.check(6/5)
*************
$$
\begin{align*}
  f(x\stackrel{!}{=} 0)  & = \dfrac{7}{8} \cdot 0 + \dfrac{6}{5} = \dfrac{6}{5}
\end{align*}
$$
*************





## Aufgabe 8 - Ungleichungen


Ein Wassertank enthält anfangs $30\,\mathrm{l}$. Durch ein Leck verliert der Tank pro Minute $\dfrac{7}{4}\,\mathrm{l}$.  
**Berechne** die Anzahl der Minuten, sodass der Inhalt höchstens $20\,\mathrm{l}$ beträgt.

<!-- data-solution-button="50"-->
$\mathbb{L} = \{ x \in \mathbb{R} \;|\; x \geq $ [[ 40/7 ]] $\}$
@Algebrite.check(40/7)
******************
$$
\begin{align*}
30 - \dfrac{7}{4}x &\le 20 \quad \left| \; -30 \; \right. \\
-\dfrac{7}{4}x &\le -10 \quad \left| \; \cdot(-1) \; \right. \\
\dfrac{7}{4}x &\ge 10 \quad \left| \; :\dfrac{7}{4} \; \right. \\
x &\ge \dfrac{40}{7} \\[4pt]
\end{align*}
$$
******************






## Aufgabe 9 - Gleichungssysteme


Für eine Nussmischung werden Mandeln (6 €/kg), Erdnüsse (4 €/kg) und Cashews (10 €/kg) gemischt. Insgesamt entstehen $ \dfrac{15}{2}\,\text{kg} $ Mischung. Der Materialwert beträgt 47 €. Außerdem werden um ein halbes Kilogramm mehr Erdnüsse als Mandeln verwendet.  
**Berechne** die eingesetzten Kilogramm der drei Sorten.

<!-- data-solution-button="50"-->
$x$ = [[  5/2  ]], $y$ = [[  3  ]] und $z$ = [[  2  ]]
@Algebrite.check([ 5/2; 3; 2 ])
************
Bezeichne mit $x$ die Kilogramm Mandeln, mit $y$ die Kilogramm Erdnüsse und mit $z$ die Kilogramm Cashews.
$$
\begin{align*}
I.& \qquad x + y + z = \dfrac{15}{2} \\
II.& \qquad 6x + 4y + 10z = 47 \\
III.& \qquad y = x + \dfrac{1}{2} \\ \hline
I \cap III:& \qquad x + \left(x + \dfrac{1}{2}\right) + z = \dfrac{15}{2} \\
& \qquad 2x + z = 7 \quad \text{(IV)} \\[6pt]
II \cap III:& \qquad 6x + 4\!\left(x + \dfrac{1}{2}\right) + 10z = 47 \\
& \qquad 10x + 2 + 10z = 47 \\
& \qquad 10x + 10z = 45 \quad \left| :5 \right. \\
& \qquad 2x + 2z = 9 \quad \text{(V)} \\ \hline
\text{(V)} - 2\cdot\text{(IV)}:& \qquad (2x + 2z) - (4x + 2z) = 9 - 14 \\
& \qquad -2x = -5 \;\Rightarrow\; x = \dfrac{5}{2} \\[6pt]
III:& \qquad y = x + \dfrac{1}{2} = \dfrac{5}{2} + \dfrac{1}{2} = 3 \\[6pt]
IV:& \qquad 2\cdot \dfrac{5}{2} + z = 7 \;\Rightarrow\; 5 + z = 7 \;\Rightarrow\; z = 2
\end{align*}
$$
Es werden $ \dfrac{5}{2}\,\text{kg} $ Mandeln, $ 3\,\text{kg} $ Erdnüsse und $ 2\,\text{kg} $ Cashews verwendet.
************


