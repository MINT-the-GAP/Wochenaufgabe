<!--
author: Martin Lommatzsch
version: 1.0.1
language: de
narrator: Deutsch Female
mode: Presentation
edit: true

comment: Interaktive SchulLia-Fassung der Qualifikation zur sächsischen Mathematik-Olympiade für Klasse 5.
tags: Mathematik, Klasse 5, Mathematik-Olympiade



import: https://raw.githubusercontent.com/MINT-the-GAP/lia-DynFlex/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-timer/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-board-mode/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-marker/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-annotation/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-canvas-ocr/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-orthography/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-Mathe/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-navigation/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-kachel/refs/heads/main/README.md

import: https://raw.githubusercontent.com/MINT-the-GAP/lia-llm/refs/heads/main/README.md

import: https://raw.githubusercontent.com/liaTemplates/algebrite/master/README.md
import: https://raw.githubusercontent.com/liaTemplates/JSXGraph/main/README.md

import: https://raw.githubusercontent.com/MINT-the-GAP/lia-resetter/main/README.md

import: https://raw.githubusercontent.com/MINT-the-GAP/lia-coordinate/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-freeze-v2/main/README.md

import: https://raw.githubusercontent.com/MINT-the-GAP/lia-loot/main/README.md


-->

# Qualifikation zur sächsischen Mathematik-Olympiade

**Geschwister-Scholl-Gymnasium Freiberg · Mathematik 5**

**Erlaubte Hilfsmittel:** *Geodreieck und Zirkel* (werden digital zur Verfügung gestellt.)

> **Hinweis:** Der Lösungsweg mit Begründungen und Nebenrechnungen soll deutlich erkennbar in logisch und grammatisch einwandfreien Sätzen dargestellt werden. Zur Lösungsgewinnung herangezogene Aussagen sind zu beweisen, falls sie nicht aus dem Schulunterricht bekannt sind.

Mit dem Stiftsymbol an einem Zahlenfeld kannst du eine Rechnung handschriftlich eingeben. In den Geometrieaufgaben stehen die Zeichenwerkzeuge direkt im Koordinatensystem-Feld bereit.

---

---


> <h3>Dieses Aufgabenset kann abgegeben werden. Richte dich dabei nach deiner Lehrkraft. Am Ende kannst du den Kurs einfrieren und den entstandenen Link über LernSax versenden.</h3>




## Aufgabe 1 – Einkaufswagen

Eine Schlange aus zehn zusammengeschobenen Einkaufswagen hat eine Länge von $4\,\mathrm{m}$, während eine Schlange aus sieben zusammengeschobenen Einkaufswagen eine Länge von $3\,\mathrm{m}$ hat.

**Ermittle** die Länge eines einzigen Einkaufswagens.

[[___]]

<!-- data-solution-timer="5s"
data-solution-timer-start="oncheck"
data-solution-timer-badge="off" -->
Ein Einkaufswagen ist [[ 1 ]] $\mathrm{m}$ lang. @canvas
********************************

Die drei zusätzlichen Einkaufswagen verlängern die Schlange zusammen um

$$
4\,\mathrm{m}-3\,\mathrm{m}=1\,\mathrm{m}.
$$

Jeder weitere eingeschobene Wagen verlängert die Schlange daher um

$$
1\,\mathrm{m}:3=\frac13\,\mathrm{m}.
$$

Bei sieben Wagen gibt es nach dem ersten Wagen sechs solche Verlängerungen. Sie sind zusammen

$$
6\cdot\frac13\,\mathrm{m}=2\,\mathrm{m}
$$

lang. Für den ersten, vollständigen Einkaufswagen bleiben damit

$$
3\,\mathrm{m}-2\,\mathrm{m}=1\,\mathrm{m}.
$$

**Ein Einkaufswagen ist $1\,\mathrm{m}$ lang.**

********************************


@ADetails(5; Aufgabe 1)


## Aufgabe 2 – Gläserklingen

Bei einer Silvesterparty stoßen die Gäste mit ihren Gläsern an. Jedes Paar stößt genau einmal miteinander an.

**Bestimme**, wie oft bei $12$ Gästen der Klang zweier aneinandergeschlagener Gläser erklingt.

[[___]]

<!-- data-solution-timer="5s"
data-solution-timer-start="oncheck"
data-solution-timer-badge="off" -->
Die Gläser erklingen insgesamt [[ 66 ]] Mal. @canvas
********************************

Die erste Person stößt mit $11$ anderen Personen an. Bei der zweiten Person ist eine Begegnung bereits gezählt, also kommen nur noch $10$ neue hinzu. So geht es weiter:

$$
11+10+9+8+7+6+5+4+3+2+1=66.
$$

Die Rechnung $12\cdot11$ würde jedes Paar zweimal zählen. Gleichwertig ist deshalb

$$
\frac{12\cdot11}{2}=66.
$$

**Der Klang ertönt $66$-mal.**

********************************



@ADetails(5; Aufgabe 2)


## Aufgabe 3 – Quadrat im Kreis

In einem Quadrat befindet sich ein maximal großer Kreis, in dem wiederum ein maximal großes Quadrat liegt.

**Beweise**, dass der Flächeninhalt des inneren Quadrats genau halb so groß ist wie der des äußeren Quadrats. Schreibe einen vollständigen Beweis.


@Koordinatensystem(`xmin=-4.6;xmax=4.6;ymin=-4.6;ymax=4.6;width=430;id=MO3FIGUR;achsen=0;grid=0;border=0`)

@Flaeche(`MO3FIGUR;[[-4;-4];[4;-4];[4;4];[-4;4]];#f0decc;1;inhalt=0;umfang=0`)
@Punkt(`MO3FIGUR;M3=0;0;0;#000000;0;fix`)
@Kreis(`MO3FIGUR;k3fill=0;M3;#92dcec;1;radius=4;inhalt=0;umfang=0`)
@Flaeche(`MO3FIGUR;[[-2.828427;-2.828427];[2.828427;-2.828427];[2.828427;2.828427];[-2.828427;2.828427]];#ffabab;1;inhalt=0;umfang=0`)

@Strecke(`MO3FIGUR;[[-4;-4];[4;-4];[4;4];[-4;4];[-4;-4]];#222222;qa3=0;design=-;3px`)
@Kreis(`MO3FIGUR;k3rand=0;M3;#222222;0;radius=4;inhalt=0;umfang=0`)
@Strecke(`MO3FIGUR;[[-2.828427;-2.828427];[2.828427;-2.828427];[2.828427;2.828427];[-2.828427;2.828427];[-2.828427;-2.828427]];#222222;qi3=0;design=-;3px`)




Formuliere nun deinen Beweis im Antwortfeld und ergänze es gerne durch eine Zeichnung in der Canvas.


@canvas

<!-- data-solution-button="off" data-llm-textarea="7" -->
[[Antwort]]
```text @LLMQuiz(0.66;solution=1;feedback=1)
Bezeichne die Seitenlänge des äußeren Quadrats mit $a$. Weil der Kreis im äußeren Quadrat maximal groß ist, besitzt er den Durchmesser $a$.

Das innere Quadrat ist in den Kreis eingeschrieben. Seine beiden Diagonalen sind deshalb ebenfalls Durchmesser des Kreises und jeweils $a$ lang. Die Diagonalen zerlegen das innere Quadrat in vier kongruente rechtwinklige Dreiecke. Jedes dieser Dreiecke hat die Kathetenlängen $\frac a2$ und $\frac a2$ und damit den Flächeninhalt
$$
\frac{1}{2}\cdot\frac{ a}{2}\cdot\frac{ a}{2}=\frac{a^2}{8}.
$$
Somit gilt
$$
A_{\mathrm{innen}}=4\cdot\frac{a^2}{8}=\frac{a^2}{2}.
$$
Das äußere Quadrat besitzt den Flächeninhalt
$$
A_{\mathrm{außen}}=a^2.
$$
Also ist
$$
A_{\mathrm{innen}}=\frac{1}{2}A_{\mathrm{außen}}.
$$
<!-- lia-llm:alternative -->
Die Seitenlänge des äußeren Quadrats sei $a$. Der Durchmesser des einbeschriebenen Kreises ist dann ebenfalls $a$. Da das innere Quadrat maximal groß ist, liegen seine vier Eckpunkte auf dem Kreis. Seine Diagonale stimmt deshalb mit einem Kreisdurchmesser überein und hat die Länge $a$.

Für die Seitenlänge $b$ des inneren Quadrats gilt nach dem Satz des Pythagoras
$$
b^2+b^2=a^2.
$$
Damit folgt $2b^2=a^2$ und somit
$$
A_{\mathrm{innen}}=b^2=\frac{a^2}{2}.
$$
Wegen $A_{\mathrm{außen}}=a^2$ gilt daher
$$
A_{\mathrm{innen}}=\frac12A_{\mathrm{außen}}.
$$
<!-- lia-llm:alternative -->
Es sei $a$ die Seitenlänge des äußeren Quadrats und $b$ die Seitenlänge des inneren Quadrats. Der maximal große Kreis besitzt den Durchmesser $a$. Zugleich ist die Diagonale des einbeschriebenen inneren Quadrats ein Durchmesser dieses Kreises. Daher gilt
$$
b\sqrt2=a.
$$
Durch Quadrieren ergibt sich $2b^2=a^2$ und damit $b^2=\frac{a^2}{2}$. Also sind
$$
A_{\mathrm{innen}}=b^2=\frac{a^2}{2}
\quad\text{und}\quad
A_{\mathrm{außen}}=a^2.
$$
Folglich ist der Flächeninhalt des inneren Quadrats halb so groß wie der des äußeren Quadrats.
<!-- lia-llm:alternative -->
Der Mittelpunkt beider Quadrate und des Kreises werde als Ursprung eines Koordinatensystems gewählt. Hat das äußere Quadrat die Seitenlänge $a$, so beträgt der Kreisradius $\frac a2$. Die Eckpunkte des inneren Quadrats können wegen der Drehsymmetrie bei
$$
\left(\frac a2,0\right),\quad
\left(0,\frac a2\right),\quad
\left(-\frac a2,0\right),\quad
\left(0,-\frac a2\right)
$$
angesetzt werden. Für eine Seite $b$ des inneren Quadrats gilt dann
$$
b^2=\left(\frac a2\right)^2+\left(\frac a2\right)^2=\frac{a^2}{2}.
$$
Somit ist $A_{\mathrm{innen}}=b^2=\frac{a^2}{2}$. Da $A_{\mathrm{außen}}=a^2$ gilt, folgt $A_{\mathrm{innen}}=\frac12A_{\mathrm{außen}}$.
<!-- lia-llm:alternative -->
Die Seitenlänge des äußeren Quadrats sei $a$. Deshalb hat der maximal große Kreis den Radius $\frac a2$ und den Durchmesser $a$. Beide Diagonalen des maximalen inneren Quadrats verbinden gegenüberliegende Punkte des Kreises und sind daher jeweils $a$ lang.

Für ein Quadrat mit den Diagonalen $d_1$ und $d_2$ gilt
$$
A=\frac{d_1\cdot d_2}{2}.
$$
Damit besitzt das innere Quadrat den Flächeninhalt
$$
A_{\mathrm{innen}}=\frac{a\cdot a}{2}=\frac{a^2}{2}.
$$
Der Flächeninhalt des äußeren Quadrats ist $A_{\mathrm{außen}}=a^2$. Also gilt $A_{\mathrm{innen}}=\frac12A_{\mathrm{außen}}$.
<!-- lia-llm:alternative -->
Die Seitenlänge des äußeren Quadrats sei $a$. Der Kreis berührt alle vier Seiten in deren Mittelpunkten. Ein Quadrat, dessen Eckpunkte diese vier Berührpunkte sind, ist im Kreis maximal groß. Die vier Flächen zwischen innerem und äußerem Quadrat sind kongruente rechtwinklige Dreiecke mit den Kathetenlängen $\frac a2$.

Jedes dieser Dreiecke hat den Flächeninhalt
$$
\frac12\cdot\frac a2\cdot\frac a2=\frac{a^2}{8}.
$$
Zusammen besitzen sie den Flächeninhalt $4\cdot\frac{a^2}{8}=\frac{a^2}{2}$. Vom äußeren Quadrat mit $A_{\mathrm{außen}}=a^2$ bleibt daher
$$
A_{\mathrm{innen}}=a^2-\frac{a^2}{2}=\frac{a^2}{2}
$$
übrig. Somit gilt $A_{\mathrm{innen}}=\frac12A_{\mathrm{außen}}$.
<!-- lia-llm:alternative -->
Der Radius des Kreises sei $r$. Weil der Kreis im äußeren Quadrat maximal groß ist, hat dieses Quadrat die Seitenlänge $2r$. Daher beträgt sein Flächeninhalt
$$
A_{\mathrm{außen}}=(2r)^2=4r^2.
$$
Die Diagonalen des inneren Quadrats sind Durchmesser des Kreises und somit jeweils $2r$ lang. Mit der Flächenformel für ein Quadrat über seine Diagonalen folgt
$$
A_{\mathrm{innen}}=\frac{2r\cdot2r}{2}=2r^2.
$$
Deshalb ist
$$
\frac{A_{\mathrm{innen}}}{A_{\mathrm{außen}}}
=\frac{2r^2}{4r^2}=\frac12.
$$
<!-- lia-llm:alternative -->
Der Kreisradius werde mit $r$ bezeichnet. Das äußere Quadrat hat wegen des einbeschriebenen Kreises die Seitenlänge $2r$ und somit den Flächeninhalt $4r^2$. Sei $b$ die Seitenlänge des inneren Quadrats. Dessen Diagonale ist der Kreisdurchmesser $2r$.

Die halbe Diagonale bildet mit den halben Seitenlängen ein rechtwinkliges Dreieck. Nach dem Satz des Pythagoras gilt
$$
r^2=\left(\frac b2\right)^2+\left(\frac b2\right)^2
=\frac{b^2}{2}.
$$
Daraus folgt $b^2=2r^2$ und damit $A_{\mathrm{innen}}=2r^2$. Im Vergleich zu $A_{\mathrm{außen}}=4r^2$ ergibt sich
$$
A_{\mathrm{innen}}=\frac12A_{\mathrm{außen}}.
$$
```

@ADetails(5; Aufgabe 3)


## Aufgabe 4 – Folgen

**Gib** jeweils die nächsten beiden Glieder der Folgen **an**.

__$a)\;\;$__ 

<!-- data-solution-timer="5s"
data-solution-timer-start="oncheck"
data-solution-timer-badge="off" -->
$1\quad 4\quad 9\quad 16\quad 25\quad$ [[ 36 ]] @canvas $\quad$ [[ 49 ]] @canvas
********************************

Es handelt sich um die Quadratzahlen:

$$
1^2,\quad2^2,\quad3^2,\quad4^2,\quad5^2,\quad
\boxed{6^2=36},\quad\boxed{7^2=49}.
$$

********************************


@ADetails(2; Aufgabe 4)


__$b)\;\;$__ 

<!-- data-solution-timer="5s"
data-solution-timer-start="oncheck"
data-solution-timer-badge="off" -->
$1\quad 2\quad 6\quad 24\quad 120\quad$ [[ 720 ]] @canvas $\quad$ [[ 5040 ]] @canvas
********************************

Jedes Glied wird mit der nächsten natürlichen Zahl multipliziert:

$$
1\cdot2=2,\quad2\cdot3=6,\quad6\cdot4=24,\quad24\cdot5=120,
$$

also

$$
120\cdot6=\boxed{720},\qquad720\cdot7=\boxed{5040}.
$$

********************************


@ADetails(2; Aufgabe 4)


__$c)\;\;$__ (Zeichne deine Lösungen in die beiden Canvas)

<span style="display:inline-block;width:min(68%,38rem);min-width:min(100%,20rem);vertical-align:middle;margin:.4rem 1rem 1rem 0"><svg viewBox="0 0 600 110" role="img" aria-labelledby="spiegelfolge-titel spiegelfolge-beschreibung" style="display:block;width:100%;height:auto"><title id="spiegelfolge-titel">Folge aus gespiegelten Ziffern</title><desc id="spiegelfolge-beschreibung">Die Ziffern eins bis fünf sind jeweils mit ihrem Spiegelbild an einer senkrechten Achse überlagert.</desc><g fill="currentColor" font-family="Arial,Helvetica,sans-serif" font-size="72" text-anchor="middle"><g transform="translate(60 82)"><text>1</text><text transform="scale(-1 1)">1</text></g><g transform="translate(180 82)"><text>2</text><text transform="scale(-1 1)">2</text></g><g transform="translate(300 82)"><text>3</text><text transform="scale(-1 1)">3</text></g><g transform="translate(420 82)"><text>4</text><text transform="scale(-1 1)">4</text></g><g transform="translate(540 82)"><text>5</text><text transform="scale(-1 1)">5</text></g></g></svg></span> [[ 66 ]] @canvas $\qquad$ [[ 77 ]] @canvas
********************************

Die Folge verwendet nacheinander die Ziffern $1,2,3,4,5,\boxed{6},\boxed{7}$ und überlagert jede Ziffer mit ihrem Spiegelbild an einer senkrechten Achse:

<svg viewBox="0 0 260 110" role="img" aria-label="Die gespiegelten Ziffern sechs und sieben" style="display:block;width:min(100%,17rem);height:auto;margin:.5rem auto">
  <g fill="currentColor" font-family="Arial,Helvetica,sans-serif" font-size="72" text-anchor="middle">
    <g transform="translate(70 82)"><text>6</text><text transform="scale(-1 1)">6</text></g>
    <g transform="translate(190 82)"><text>7</text><text transform="scale(-1 1)">7</text></g>
  </g>
</svg>

********************************


@ADetails(2; Aufgabe 4)


## Aufgabe 5 – Flächen zerlegen

**Unterteile** jede farbige Fläche in gleich große Stücke mit jeweils gleicher Form:

- die **blaue** Fläche in zwei Stücke,
- die **orangefarbene** Fläche in drei Stücke,
- die **grüne** Fläche in vier Stücke,
- die **rote** Fläche in fünf Stücke.

Öffne links oben das DGS-Menü. Zeichne mit **Strecke** oder **Freihand** direkt in die Figur. Das Geodreieck hilft bei geraden Linien; mit **Radierer**, **Rückgängig** und **Wiederholen** kannst du korrigieren.


<section class="dynFlex">

<div class="flex-child">


@Koordinatensystem(`xmin=-1.2;xmax=5.2;ymin=-1.2;ymax=5.2;width=560;id=mo5_zerlegung;achsen=0;grid=0;border=1`)

@Flaeche(`mo5_zerlegung;[[0;2];[1;2];[1;3];[2;3];[2;4];[0;4]];#80ff80;1;inhalt=0;umfang=0`)
@Flaeche(`mo5_zerlegung;[[3;2];[4;2];[4;4];[2;4];[2;3];[3;3]];#92dcec;1;inhalt=0;umfang=0`)
@Flaeche(`mo5_zerlegung;[[0;0];[2;0];[2;1];[1;1];[1;2];[0;2]];#ffbf80;1;inhalt=0;umfang=0`)
@Flaeche(`mo5_zerlegung;[[2;0];[4;0];[4;2];[2;2]];#ff8080;1;inhalt=0;umfang=0`)

@Strecke(`mo5_zerlegung;[[2;0];[2;4]];#111111;;-;4px`)
@Strecke(`mo5_zerlegung;[[0;2];[4;2]];#111111;;-;4px`)
@Flaeche(`mo5_zerlegung;[[1;1];[2;1];[2;2];[3;2];[3;3];[1;3]];#111111;1;inhalt=0;umfang=0`)
@Strecke(`mo5_zerlegung;[[0;0];[4;0];[4;4];[0;4];[0;0]];#111111;;-;5px`)

@DGS(`mo5_zerlegung;tools=[310;910;920];restrictions=[300;400]`)



</div>

</section>



[[!]]
<script>true</script>
********************************

**Eine mögliche Zerlegung:**

@Koordinatensystem(`xmin=-1.2;xmax=5.2;ymin=-1.2;ymax=5.2;width=560;id=mo5_loesung;achsen=0;grid=0;border=1`)

@Flaeche(`mo5_loesung;[[0;2];[1;2];[1;3];[2;3];[2;4];[0;4]];#80ff80;1;inhalt=0;umfang=0`)
@Flaeche(`mo5_loesung;[[3;2];[4;2];[4;4];[2;4];[2;3];[3;3]];#92dcec;1;inhalt=0;umfang=0`)
@Flaeche(`mo5_loesung;[[0;0];[2;0];[2;1];[1;1];[1;2];[0;2]];#ffbf80;1;inhalt=0;umfang=0`)
@Flaeche(`mo5_loesung;[[2;0];[4;0];[4;2];[2;2]];#ff8080;1;inhalt=0;umfang=0`)

@Strecke(`mo5_loesung;[[2;0];[2;4]];#111111;;-;4px`)
@Strecke(`mo5_loesung;[[0;2];[4;2]];#111111;;-;4px`)
@Flaeche(`mo5_loesung;[[1;1];[2;1];[2;2];[3;2];[3;3];[1;3]];#111111;1;inhalt=0;umfang=0`)
@Strecke(`mo5_loesung;[[0;0];[4;0];[4;4];[0;4];[0;0]];#111111;;-;5px`)

@Strecke(`mo5_loesung;[[1;4];[1;3.5];[0.5;3.5];[0.5;2.5];[1;2.5]];#111111;;-;3px`)
@Strecke(`mo5_loesung;[[1;3.5];[1.5;3.5];[1.5;3]];#111111;;-;3px`)
@Strecke(`mo5_loesung;[[0;3];[0.5;3]];#111111;;-;3px`)

@Strecke(`mo5_loesung;[[3;3];[4;4]];#111111;;-;3px`)

@Strecke(`mo5_loesung;[[0;1];[1;1];[1;0]];#111111;;-;3px`)

@Strecke(`mo5_loesung;[[2.4;0];[2.4;2]];#111111;;-;3px`)
@Strecke(`mo5_loesung;[[2.8;0];[2.8;2]];#111111;;-;3px`)
@Strecke(`mo5_loesung;[[3.2;0];[3.2;2]];#111111;;-;3px`)
@Strecke(`mo5_loesung;[[3.6;0];[3.6;2]];#111111;;-;3px`)

- **Blau:** Die Diagonale ist eine Spiegelachse und erzeugt zwei kongruente Teile.
- **Orange:** Es entstehen drei kongruente Einheitsquadrate.
- **Grün:** Die große L-Form besteht aus vier kongruenten, halb so großen L-Formen.
- **Rot:** Fünf gleich breite Rechtecke zerlegen das Quadrat.

********************************



@ADetails(4; Aufgabe 5)


# Abgabe

> <h3>Kontrolliere, ob du alle Aufgaben bearbeitet hast. Friere anschließend den Kurs ein und sende den entstandenen Link über LernSax.</h3>

@Abgabe

@Auswertung(F12;Tab;Time;Send)
