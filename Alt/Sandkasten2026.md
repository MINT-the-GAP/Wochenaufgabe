<!--
version: 1.1.0
language: de
narrator: Deutsch Female

persistent: true
edit: true

comment: Fächerbezogener Beispielkurs mit interaktiven Elemente in LiaScript für den Schulunterricht
author: Martin Lommatzsch, André Dietrich, Sebastian Zug


import: https://raw.githubusercontent.com/MINT-the-GAP/lia-DynFlex/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-timer/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-board-mode/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-marker/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-annotation/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-canvas-ocr/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-orthography/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-Mathe/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-kachel/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-mathpath/refs/heads/master/README.md

import: https://raw.githubusercontent.com/MINT-the-GAP/lia-llm/refs/heads/main/README.md

import: https://raw.githubusercontent.com/liaTemplates/algebrite/master/README.md
import: https://raw.githubusercontent.com/liaTemplates/JSXGraph/main/README.md
import: https://raw.githubusercontent.com/LiaTemplates/ABCjs/main/README.md
import: https://raw.githubusercontent.com/LiaTemplates/Speech-Recognition-Quiz/main/README.md
import: https://raw.githubusercontent.com/LiaTemplates/AVR8js/main/README.md
import: https://raw.githubusercontent.com/LiaTemplates/PeriodicTable/main/README.md

import: https://raw.githubusercontent.com/MINT-the-GAP/lia-resetter/main/README.md

import: https://raw.githubusercontent.com/MINT-the-GAP/lia-coordinate/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-freeze-v2/main/README.md



















eingabe: <script input="number" input-always-active modify="false" value="0" default="0">@input</script>



-->


















































# Demo Kurs "LiaScript in der Schule"


[![LiaScript](https://raw.githubusercontent.com/LiaScript/LiaScript/master/badges/course.svg)](https://liascript.github.io/course/?https://raw.githubusercontent.com/MINT-the-GAP/Wochenaufgabe/refs/heads/main/Alt/Sandkasten2026.md)


> Dieser Kurs demonstriert mögliche Formate interaktiver Inhalte in [LiaScript](https://liascript.github.io/) für verschiedene Fächer.

LiaScipt ist eine Beschreibungssprache für Lehr-Lerninhalte, die an der TU Bergakademie Freiberg seit 2017 entwickelt und durch eine internationalen Community genutzt und erweitert wird. Das besondere daran ist, dass die Idee einer einfachen Syntax wie Markdown mit der Möglichkeit kombiniert wird, interaktive Elemente wie Quiz, Simulationen, Programmierumgebungen, Formeleditoren, Tabellenkalkulationen und vieles mehr einzubinden [Link](https://open-educational-resources.de/warum-braucht-offene-bildung-eine-eigene-sprache-warum-liascript/). Bislang werden diese Möglichkeiten aber eher in der universitären Lehre eingesetzt.

Ich, Martin Lommatzsch, bin Fachlehrer am Geschwister-Scholl-Gymnasium in Freiberg und nutze LiaScript intensiv in meinem Unterricht. Eine umfangreiche Aufgabensammlung, die natürlich beliebig genutzt, kopiert und angepasst werden darf, findet sich unter [https://mint-the-gap.github.io/Aufgabensammlung/].

> Mit dem hier vorliegenden Kurs möchte ich eine Brücke schlagen und die Potentiale für andere Fächer aufzeigen. Werfen Sie gern einen Blick auf den "Code" dahinter. Klicken Sie im Kurs einfach auf den "Edit" Button, den ich im Bild markiert habe.

![Schaltfläche zum Öffnen des Live-Editors](../pic/LinkToLiveEditor.png)

> ***(Einige Beispiele sind mehr oder weniger zufällig Fächern zugeordnet und können mit anderen Beispielen auch verknüpft werden. Ein Blick in jeden Fachbereich lohnt sich.)***

Ich freue mich über Rückmeldungen, Anregungen und Fragen. Kontaktieren Sie mich gern per Mail:\
`m.lommatzsch@gsg-freiberg.lernsax.de`

Viel Spaß damit!

Freiberg, Februar 2026

_PS: Vielen Dank bei den MitstreiterInnen aus der TU Bergakademie für die Unterstützung bei der Umsetzung!_



---

---


Auf den folgenden Seiten werden die Features von SchulLia vorgestellt.


> Import

`import: https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/main/README.md`






## Mathematik





**Aufgabe 1:** **Berechne** den Wert des Terms. (DynFlex-, Canvas- und Timer-Demo)


<section class="dynFlex">


<div class="flex-child">

__$a)\;\;$__  

<!-- data-solution-timer="20s" -->
$ 14000+795= $ [[            14795           ]]
@Algebrite.check(14795)

@canvas


</div>
<div class="flex-child">

__$b)\;\;$__ **Berechne** $$\int\limits_{-\infty}^{1} 3x e^{-x^2} dx$$ und **gib** den Wert mittels der Schrifterkennung **ein**.  \



<!-- data-solution-timer="15s" data-solution-timer-start="oncheck" -->
 [[            -0,551819            ]] 
@Algebrite.check2(-0.551819,0.01)

@canvas

</div>
<div class="flex-child">

__$c)\;\;$__ Wie viel sind $400\%$ von $125\,$€?  \



<!-- data-solution-timer="10s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->
 [[  500  ]]€ 
@Algebrite.check(500)
************
$$
\begin{align*}
400\% \cdot 125\,\text{€}
&= 4,00 \cdot 125\,\text{€} \\
&= 500\,\text{€} 
\end{align*}
$$
************

@canvas

</div>
<div class="flex-child">

__$d)\;\;$__ Wie viel sind $7\%$ von $900\,$€?  \



<!-- data-solution-timer="10s" data-solution-timer-start="onclick" -->
 [[  63  ]]€ 
@Algebrite.check(63)
************
$$
\begin{align*}
7\% \cdot 900\,\text{€}
&= 0,07 \cdot 900\,\text{€} \\
&= 63\,\text{€} 
\end{align*}
$$
************

@canvas

</div>
<div class="flex-child">

__$e)\;\;$__ Wie viel sind $12\%$ von $750\,$€?  \



<!-- data-solution-timer="10s" data-solution-timer-start="onclick" data-solution-timer-badge="off" -->
 [[  90  ]]€ 
@Algebrite.check(90)
************
$$
\begin{align*}
12\% \cdot 750\,\text{€}
&= 0,12 \cdot 750\,\text{€} \\
&= 90\,\text{€}
\end{align*}
$$
************

@canvas

</div>
<div class="flex-child">

__$f)\;\;$__ Wie viel sind $4\%$ von $1\,250\,$€?  \


<!-- data-solution-button="5" -->
 [[  50  ]]€ 
@Algebrite.check(50)
************
$$
\begin{align*}
4\% \cdot 1\,250\,\text{€}
&= 0,04 \cdot 1\,250\,\text{€} \\
&= 50\,\text{€}
\end{align*}
$$
************

@canvas


</div>


</section>




---

---




**Aufgabe 2:** **Stelle** die passende Teilung der Fläche **ein** und **markiere** den passenden Anteil, sodass der Bruch dargestellt wird.



<section class="dynFlex">

<div class="flex-child">

__$a)\;\;$__ $\dfrac{3}{4}$

@circleQuiz(3/4)

`@circleQuiz(3/4)`

</div>

<div class="flex-child">

__$b)\;\;$__ $\dfrac{7}{10}$

@rectQuiz(7/10)

`@rectQuiz(7/10)`

</div>

</section>






---

---



__Aufgabe 3:__ Randomaufgaben gehen auch, aber hier ist aktuell ein Bug.


---

---



__Aufgabe 4:__ 



@Koordinatensystem(`xmin=-1;xmax=10;ymin=-1;ymax=10;width=700;id=A1`)

@AchsenBeschriftung(`id=A1;xlabel=$x$;ylabel=$y$`)

__$a)\;\;$__ **Ziehe** den Punkt $A$ **auf** die Koordinaten $(1|4)$.

@ErzeugePunkt(`A1;A;1;4`,`<!-- data-solution-timer="90s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->`)



---

---



__Aufgabe 5:__ Graph rekonstruieren

@Koordinatensystem(`xmin=-4;xmax=5;ymin=-4;ymax=7;width=800;id=S2026R`)

@AchsenBeschriftung(`id=S2026R;xlabel=$x$;ylabel=$y$`)

@Punkt(`S2026R;A;0;1;fix`)
@Punkt(`S2026R;B;2;5;fix`)

@Schar(`f;x;mx+n;S2026R;term=1;#0077ff`)

**Stelle** die Schieberegler $m$ und $n$ so **ein**, dass die Gerade $f(x)=mx+n$ durch die Punkte $A(0|1)$ und $B(2|5)$ verläuft. **Überprüfe** anschließend deine Einstellung.

@Rekonstruktion(`S2026R;2x+1;0.1`)
[[?]] Lies den Achsenabschnitt bei $A$ ab. Von $A$ nach $B$ gehst du zwei Einheiten nach rechts und vier Einheiten nach oben.
*****************
Der Achsenabschnitt ist $n=1$. Die Steigung beträgt $m=\dfrac{5-1}{2-0}=2$.

Mit $m=2$ und $n=1$ erhältst du $f(x)=2x+1$. Es gilt $f(0)=1$ und $f(2)=5$.
*****************

---

---



__Aufgabe 6:__ **Gib** für $f(x)=2x-1$ die Wertepaare zu $x=-1$, $x=0$ und $x=2$ in die Tabelle **ein** und **beobachte** die zugehörigen Punkte im Koordinatensystem.



@Koordinatensystem(`xmin=-7;xmax=7;ymin=-5;ymax=5;width=800;id=A12`)

@AchsenBeschriftung(`id=A12;xlabel=$x$;ylabel=$y$`)


@Tabelle(`n=3;x;f;P;id=A12`)






---

---



__Aufgabe 7:__ 


@Koordinatensystem(`xmin=-7;xmax=7;ymin=-5;ymax=5;width=800;id=A4`)

@AchsenBeschriftung(`id=A4;xlabel=$x$;ylabel=$y$`)

Ziehe den Punkt auf den Graphen von $f(x)=2x-4$.

@PunktGraph(`A4;A;f;2x-4;0.05`) \











---

---



__Aufgabe 8:__ **Gib** den ungefähren Wert der abgebildeten Objekte **an**.

<section class="dynFlex">

<div class="flex-child">


__$a)\;\;$__

![Holzperlen](https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/circa5.jpg)

[[ 380  ]] Holzperlen
@Algebrite.check_margin(350,410)


</div>
<div class="flex-child">


__$b)\;\;$__

![Reiskörner](https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/circa6.jpg)

[[ 2000 ]] Reiskörner
@Algebrite.check_margin(1800,2300)


</div>
</section>


---

---


__Aufgabe 9:__ Schreibe den Term $4+5*2-7$ in das Fenster. Drück dann unten links das Symbol </>.

``` Maxima
8+9
```
@Algebrite.eval



---

---

__Aufgabe 10:__ Gib den Term `x ^ 2 - 2 * x + 1` in einer beliebigen Umformung in das Lösungsfeld ein.

[[  x ^ 2 - 2 * x + 1  ]]
@Algebrite.check(x^2-2*x+1)

---

---






__Aufgabe 11:__ Dreieck konstruieren

@Koordinatensystem(`xmin=-2;xmax=7;ymin=-2;ymax=6;width=800;id=S2026K`)

@AchsenBeschriftung(`id=S2026K;xlabel=$x$;ylabel=$y$`)

@DGS(`S2026K;tools=[200;510;610;920]`)

**Konstruiere** ein rechtwinkliges Dreieck mit den Seitenlängen $3$, $4$ und $5$ Längeneinheiten. Öffne das Werkzeugmenü oben links und nutze das Vieleckwerkzeug. **Schließe** das Dreieck, indem du nach dem dritten Eckpunkt erneut den ersten auswählst. Lage und Orientierung sind frei. Für genaue Positionen kannst du per Rechtsklick auf einen Punkt seine Koordinaten bearbeiten.

@KonstruktionQuiz(`S2026K;3;offen;W90,S3,S4,S5;streckentoleranz=0.15;winkeltoleranz=1`,`<!-- data-solution-button="3" -->`)
[[?]] Zeichne zwei zueinander senkrechte Seiten der Längen $4$ und $3$ mit gemeinsamem Anfangspunkt. Verbinde ihre freien Endpunkte und schließe das Vieleck.
*****************
Eine mögliche Lösung hat die Eckpunkte $A(0|0)$, $B(4|0)$ und $C(0|3)$. Wähle sie mit dem Vieleckwerkzeug in der Reihenfolge $A\rightarrow B\rightarrow C\rightarrow A$.

Die Seiten $AB$ und $AC$ sind $4$ bzw. $3$ Längeneinheiten lang und stehen senkrecht aufeinander. Die dritte Seite ist $\sqrt{4^2+3^2}=5$ Längeneinheiten lang.
*****************

---

---

__Aufgabe 12:__ GeoGebra


??[](https://www.bildung-bedeutet-freiheit.de/GeoGebra/Downloadbalken.html)


---

---


__Aufgabe 13:__ Eigene Lernspiele

??[](https://bildung-bedeutet-freiheit.de/viervieren/index.html)

---

---

__Aufgabe 14:__ Dynamische Geometrie erkunden

@Koordinatensystem(`xmin=-5;xmax=5;ymin=-3;ymax=6;width=800;id=S2026D`)

@AchsenBeschriftung(`id=S2026D;xlabel=$x$;ylabel=$y$`)

@Punkt(`S2026D;A;-3;-1`)
@Punkt(`S2026D;B;3;-1`)
@Punkt(`S2026D;C;1;3`)

@DGS(`S2026D`)

**Verbinde** die Punkte $A$, $B$ und $C$ mit dem Vieleckwerkzeug zu einem Dreieck. **Konstruiere** mit dem Mittelpunktwerkzeug die Mittelpunkte der Seiten $AB$ und $AC$ und **verbinde** diese mit einer Strecke. Für jeden Mittelpunkt wählst du die beiden Endpunkte der jeweiligen Seite aus.

**Verschiebe** anschließend die Eckpunkte des Dreiecks im Mausmodus. **Beschreibe**, wie die Verbindungsstrecke der Mittelpunkte zur Seite $BC$ liegt und wie sich ihre Längen zueinander verhalten. Über das Werkzeugmenü oben links kannst du weitere DGS-Werkzeuge ausprobieren.

<details>
<summary>Beobachtung zum Vergleichen</summary>

Solange die drei Eckpunkte ein Dreieck bilden, bleibt die Verbindungsstrecke der beiden Seitenmittelpunkte parallel zur Seite $BC$ und halb so lang wie diese. Die konstruierten Mittelpunkte passen sich beim Verschieben automatisch an.

</details>




















## Deutsch


**Aufgabe 1:** 
**Fülle** die Tabelle zu den Adjektiven **aus**.

<center>
<!-- data-solution-button="10" 
data-show-partial-solution 
data-randomize="true" 
data-type="none" 
data-sortable="false" 
style="max-width:800px;" -->
|  Positiv         |  Komparativ        |  Superlativ              |
|:----------------:|:------------------:|:------------------------:|
|  groß            | [[  größer     ]]  | [[  am größten        ]] |
|  [[ klug     ]]  | klüger             | [[  am klügsten       ]] |
|  gut             | [[  besser     ]]  | [[  am besten         ]] |
|  [[ nett     ]]  | [[  netter     ]]  |       am nettesten       |
</center>



---

---


**Aufgabe 2:** Hör dir den Satz an und schreib ihn korrekt in das Eingabefeld.


@diktat(Das Kind liest laut in einem neuen Buch.)



---

---



**Aufgabe 3:** Setze das Komma an die richtige Stelle.


@orthography(`<!-- data-solution-timer="15s" data-solution-timer-start="oncheck" data-solution-timer-badge="off" -->`,`Das ist der Tag an dem ich geblitzt wurde.`,`Das ist der Tag, an dem ich geblitzt wurde.`)



---

---



**Aufgabe 4:** **Markiere** @markedred(das Subjekt in rot), @markedblue(das Prädikat in blau) und @markedgreen(das Objekt in grün).



<section class="dynFlex">

<div class="flex-child">

__$a)\;\;$__
<div class="markerquiz">
@markred(Der Hund) @markblue(frisst) @markgreen(das Futter).
@TextmarkerQuiz
</div>


</div>

<div class="flex-child">

__$b)\;\;$__
<div class="markerquiz">
@markred(Die Lehrerin) @markblue(lobt) @markgreen(den Schüler).
@TextmarkerQuiz
</div>


</div>


</section>




---

---




__Aufgabe 5:__ **Gib** die passende Wortart **an**.


groß  [[(Adjektiv)|Adverb|Artikel|Interjektion|Konjunktion|Numeral|Nomen|Präposition|Pronomen|Substantiv|Verb]]  \












## Englisch / Fremdsprachen

_Zunächst starten wir mit der Überprüfung des Internetbrowsers - LiaScript evaluiert, ob die von Ihnen verwendete Variante Sprachaufnahme unterstützt. Wenn der Hinweis auf einen anderen Browser erscheint, wechseln Sie bitte. Die Spracheingabe und die damit verbundenen Aufgaben werden sonst nicht funktionieren._

@SpeechRecognition.support

__Exercise 1:__ Speak out loud

<section class="dynFlex">

<div class="flex-child">

__$a)\;\;$__ Say 'Good morning' in English.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(en-US,`Good morning`)


</div>
<div class="flex-child">

__$b)\;\;$__ Say 'Hello' in English.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(en-US,`Hello`)


</div>
<div class="flex-child">

__$c)\;\;$__ Say 'Cucumber' in English.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(en-US,`Cucumber`)

</div>
<div class="flex-child">

__$d)\;\;$__ Say 'Geld' in English.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(en-US,`Money`)

</div>
</section>


---

---



__Exercise 2:__ Drag the correct words into the gaps. 

> (Hinweis: Auf Touchbildschirmen bitte aktuell noch erst das Feld mit der Lücke antippen dann das gewünschte Wort.)

Ellen goes to school. [->[ He | (She) | It ]] wants to learn.  [->[ His | (Her) | Its ]] first subject today is math. 


---

---


__Exercise 3:__ Fill out the table with the irregular verbs.


<!-- data-solution-button="2" data-show-partial-solution -->
|  simple present  |  simple past |  past participle |
|:----:|:-----:|:-----:|
|  put   | [[  put     ]]  | [[  put     ]]  |
|  go   | [[  went    ]]  | [[  gone    ]]  |
|  eat   | [[  ate     ]]  | [[  eaten   ]]  |
|  shake   | [[  shook   ]]  | [[  shaken  ]]  |
|  steal   | [[  stole   ]]  | [[  stolen  ]]  |



---

---




__Aufgabe 4:__ Sprich das angegebene Wort in der angegebenen Sprache.

@SpeechRecognition.support


<section class="dynFlex">

<div class="flex-child">

__$a)\;\;$__ Sprich 'Danke' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Merci`)


</div>
<div class="flex-child">


__$b)\;\;$__ Sprich 'Danke' auf spanisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(es-ES,`Gracias`)

</div>
<div class="flex-child">

__$c)\;\;$__ Sprich 'Danke' auf russisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(ru-RU,`Спасибо`)

</div>
</section>

Es werden noch viele weitere Sprachen unterstützt.
























## Naturwissenschaften





__Aufgabe 1:__ **Wähle** die Reaktionsprodukte **aus**, die eine vollständige Verbrennung korrekt beschreiben.

> (Klicke auf die Glühlampe, um einen Hinweis zu erhalten, bevor du die Aufgabe überprüfst oder lösen lässt.)

$2C_3H_8 + 10 O_2 \longrightarrow$ [[$6CO+8H_2O+2O_3$|$4CO_2+2CO+8H_2O$|($6CO_2+8H_2O$)|$6CHO_2+4H_2O$|$3C_2O_4+8H_2O$]]
[[?]] Es wird wohl Kohlenstoffdioxid und Wasser übrig bleiben.
[[?]] Du hattest schon einen Tipp.
[[?]] Nun reicht es aber!
[[?]] Keine Tipps mehr!



---

---


__Aufgabe 2:__ Zieh den Gesang der Amsel in das Feld.


> (Hinweis: Auf Touchbildschirmen bitte aktuell noch erst das Feld mit der Lücke antippen dann die gewünschte Tonspur.)

[->[ ?[Song and calls uttered by a House Sparrow, recorded at Cowley, Gloucestershire, England](https://upload.wikimedia.org/wikipedia/commons/b/ba/House_Sparrows_%28Passer_domesticus%29_%28W1CDR0001537_BD13%29.ogg)<!-- style="height:100px" --> | (?[Reviergesang männliche Amsel, Juni 2020 Wien](https://upload.wikimedia.org/wikipedia/commons/8/8a/2020-06-22_Amsel_4_Uhr_fr%C3%BCh_Wien.ogg) <!-- style="height:100px" --> ) | ?[The calls of a Blue Tit, recorded at Cowley, Gloucestershire, England](https://upload.wikimedia.org/wikipedia/commons/d/d7/Blue_Tit_%28Cyanistes_caeruleus%29_%28W1CDR0001535_BD30%29.ogg)<!-- style="height:100px" --> ]]

<small><small><small><small><small> Quellen: Reviergesang männliche Amsel, Juni 2020 Wien, Song and calls uttered by a House Sparrow, recorded at Cowley, Gloucestershire, England, The calls of a Blue Tit, recorded at Cowley, Gloucestershire, England </small></small></small></small></small>

---

---

__Aufgabe 3:__ Fülle die Lücken aus. (Die Lücken sind verknüpft mit einander.)


Es gibt [[  positive  ]] und [[  negative  ]] elektrische Ladungen.
<script>
@input.map(s => s.trim().toLowerCase()).sort().join() === "negative,positive"
</script>



---

---

__Aufgabe 4:__ Ein Objekt bewegt sich mit $4\,\dfrac{\text{m}}{\text{s}}$. Fülle die Tabelle aus, sortiere danach nach der Zeit und lass dir die Werte als Funktion anzeigen.

> (Kann somit auch zur Messwerterfassung genutzt werden.)

<!-- style="width:500px" -->
|  $t$ in [s]  |  $x$ in [m] |
|:----:|:-----:|
|  1   |  @eingabe   |
|  5   |  @eingabe   |
|  3   |  @eingabe   |
|  4   |  @eingabe   |
|  2   |  @eingabe   |
|  6   |  @eingabe   |
|  7   |  @eingabe   |


Musterlösungsanzeige auch ohne Eingabe ist möglich:

[[!]]
<script>true</script>
***************************

Es sollte eine lineare Ursprungsgerade zu erkennen sein, wenn alle Werte richtig berechnet wurden.

***************************



---

---



__Aufgabe 5:__ **Gib** mithilfe des Periodensystems **an**, wer Germanium entdeckt hat.

@PeriodicTable

Der Entdecker von Germanium hieß: [[   Clemens Winkler   ]].

---

---


__Aufgabe 6:__ Auch Experimente an Robotern aus der Ferne mit den Remote-Laboren durch `edrys` sind möglich. (Hier durch ein Video vorgestellt)

!?[](https://www.youtube.com/watch?v=6ZjGHorc2ds)


---

---


__Aufgabe 7:__ Untersuche das Schneckenhaus in 3D.

??[](https://sketchfab.com/3d-models/sea-snail-shell-6515f625857041ad87bb6e2e5e5f6206)


---

---

__Aufgabe 8:__ PhET-Simulationen sind einfach einzubinden.

??[](https://phet.colorado.edu/sims/html/sound-waves/latest/sound-waves_all.html)






## Informatik


__Aufgabe 1:__ Korrigiere den Fehler im Code und lass dir die Anzahl der Buchstaben der Nachricht ausgeben. Drück dazu mal unten links dieses </> Symbol.

``` js
var message = "Dies ist die Nachricht"
console.log(message)
message.leangth
```
<script>@input </script>




__Aufgabe 2:__ Schreib den Code so um, dass die LEDs von rechts nach Links blinken. Drück dazu mal unten links dieses </> Symbol.


<lia-keep>
<div id="led-exercise">
<wokwi-led color="red"   pin="13" label="13"></wokwi-led>
<wokwi-led color="green" pin="12" label="12"></wokwi-led>
<wokwi-led color="blue"  pin="11" label="11"></wokwi-led>
<wokwi-led color="blue"  pin="10" label="10"></wokwi-led>
</div>
</lia-keep>

``` cpp
byte leds[] = {13, 12, 11, 10};
void setup() {
  Serial.begin(115200);
  for (byte i = 0; i < sizeof(leds); i++) {
    pinMode(leds[i], OUTPUT);
  }
}

int i = 0;
void loop() {
  Serial.print("LED: ");
  Serial.println(i);
  digitalWrite(leds[i], HIGH);
  delay(250);
  digitalWrite(leds[i], LOW);
  i = (i + 1) % sizeof(leds);
}
```
@AVR8js.sketch(led-exercise)


[[!]]
<script>true</script>
***************************

Dies hier könnte eine Lösung sein:

<lia-keep>
<div id="led-solution">
<wokwi-led color="red"   pin="13" label="13"></wokwi-led>
<wokwi-led color="green" pin="12" label="12"></wokwi-led>
<wokwi-led color="blue"  pin="11" label="11"></wokwi-led>
<wokwi-led color="blue"  pin="10" label="10"></wokwi-led>
</div>
</lia-keep>

``` cpp
byte leds[] = {13, 12, 11, 10};
void setup() {
  Serial.begin(115200);
  for (byte i = 0; i < sizeof(leds); i++) {
    pinMode(leds[i], OUTPUT);
  }
}

int i = sizeof(leds) - 1;
void loop() {
  Serial.print("LED: ");
  Serial.println(i);
  digitalWrite(leds[i], HIGH);
  delay(250);
  digitalWrite(leds[i], LOW);
  i = (i + sizeof(leds) - 1) % sizeof(leds);
}
```
@AVR8js.sketch(led-solution)


***************************








## Musik / Kunst




<section class="dynFlex">
<div class="flex-child">

__Aufgabe 1:__ Höre dir die beiden Töne über die Wiedergabe an und benenne das Intervall.

``` abc  @ABCJS.render
X: 1
M: 4/4
L: 1/2
K: C
G C |]
```

Intervall: [[  Quinte  ]]

</div>
<div class="flex-child">

__Aufgabe 2:__ Höre dir den Dreiklang über die Wiedergabe an und entscheide, ob es sich um einen Dur- oder Moll-Dreiklang handelt.

``` abc  @ABCJS.render
X: 1
M: 4/4
L: 1/1
K: C
[Ace] |]
```

Dreiklangsart: [[Dur|(Moll)]]

</div>
</section>

---

__Aufgabe 3:__ Ziehe das Bild des Komponisten hinter seinen Namen.


> (Hinweis: Auf Touchbildschirmen bitte aktuell noch erst das Feld mit der Lücke antippen dann das gewünschte Bild.)

<!-- data-randomize="true"  -->
Bach:    [->[( ![](https://raw.githubusercontent.com/MINT-the-GAP/Wochenaufgabe/refs/heads/main/pic/bach.jpg)<!-- style="height:150px" --> )]] \
Mozart:  [->[( ![](https://upload.wikimedia.org/wikipedia/commons/c/cc/Mozart_Portrait_Croce.jpg)<!-- style="height:150px" --> )]] \
Puccini:  [->[( ![](https://upload.wikimedia.org/wikipedia/commons/9/9b/GiacomoPuccini.jpg)<!-- style="height:150px" --> )]] \






## Geschichte / Geographie / GRW

__Aufgabe 1:__ Ordne die Kriege chronologisch. Fange links bei dem Krieg an, der am weitesten in der Vergangenheit liegt. (Quizanzeige ist jedes mal anders.)


> (Hinweis: Auf Touchbildschirmen bitte aktuell noch erst das Feld mit der Lücke antippen dann das gewünschte Wort.)

<!-- data-randomize="true"  -->
 [->[ (Punische Kriege) ]] [->[ (Dreißigjähriger Krieg) ]] [->[ (1. Weltkrieg) ]] [->[ (2. Weltkrieg) ]] [->[ (Vietnamkrieg) ]]




---


__Aufgabe 2:__ **Ordne** die Verfassungsorgane der Exekutive, Legislative oder Judikative **zu**. (Die Reihenfolge wird zufällig gewählt.)


<!-- data-randomize="true"  -->
- [[Exekutive]   (Legislative)    [Judikative]]
- [    [ ]           [X]             [ ]     ]  Bundestag
- [    ( )           ( )             (X)     ]  Bundesverfassungsgericht
- [    [X]           [ ]             [ ]     ]  Bundeskanzler
- [    ( )           (X)             ( )     ]  Bundesrat
- [    [X]           [ ]             [ ]     ]  Bundesregierung


---


__Aufgabe 3:__ Wer war der erste Bundeskanzler der Bundesrepublik Deutschland? Wähle aus. (Die Reihenfolge wird zufällig gewählt.)

<!-- data-randomize="true"  -->
- [[ ]] Helmut Schmidt
- [[ ]] Theodor Heuss
- [[X]] Konrad Adenauer
- [[ ]] Willy Brandt




## Deutsch als Zweitsprache / Inklusion

{{0-1}}
***************************
In LiaScript kann man jeden Course automatisch übersetzen lassen:


![](https://raw.githubusercontent.com/MINT-the-GAP/Wochenaufgabe/refs/heads/main/pic/DaZ1.png)


{{|> Deutsch female}} Und man kann jeden Text vorlesen lassen. Auch in anderen Sprachen.

***************************

{{1}}
***************************
Zur besseren Fokussierung kann man auch nur den aktuellen Inhalt einblenden und den Rest ausblenden.
***************************




## Freie Antworten mit LLM-Prüfung

Hier wird deine Antwort sinngemäß mit einer Musterlösung verglichen. Du kannst eigene Worte verwenden.

> **Hinweis zum Download:** Beim ersten Aufruf dieses Quiz lädt dein Browser ein KI-Modell für die Auswertung herunter. Das kann je nach Internetverbindung etwas dauern. Die Modelldateien werden im Browser zwischengespeichert und bei späteren Aufrufen normalerweise wiederverwendet. Deine Antwort wird auf deinem Gerät ausgewertet.

**Aufgabe:** **Beschreibe** die Seitenlängen und die Innenwinkel eines Quadrats.

<!-- data-solution-button="off" data-llm-textarea="3" -->
[[Antwort]]
[[?]] Denke an die Längen aller vier Seiten und an die Größe der Winkel.
```text @LLMQuiz(0.66;solution=1;feedback=1,`Beschreibe die Seitenlängen und die Innenwinkel eines Quadrats.`)
Ein Quadrat hat vier gleich lange Seiten. Alle vier Innenwinkel sind rechte Winkel, also jeweils 90 Grad groß.
```

## Zusätzliche Informationen für Lehrkräfte

+ Ist die Versionsnummer 1.0.0 oder größer, dann werden die Eingaben, die getätigt wurden auch lokal auf dem Endgerät der Schülerinnen und Schüler abgespeichert.
+ Über Opal gibt es eine Integrationsmöglichkeit für eine Rückmeldung der Schülerinnen- und Schülerleistungen für die Lehrkräfte.
+ Dieser Kommentar sollte individuell bearbeitet immer am Anfang des Dokuments im Editor stehen.


```
<!--
version:  0.0.1
language: de
narrator: Deutsch female
comment: Beschreibung des Kurses bitte hier. 
author: Name
-->
```

