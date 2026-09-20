<!--
version:  0.2.0
language: en
narrator: Deutsch Female

tags: Presentation, Teacher training, LiaScript, lia-coordinate, DGS, Mathematics, OER
comment:  lia-coordinate in the classroom: representations, tasks, teaching choices
          and the path from a visual DGS construction to a reusable worksheet.
author:   Martin Lommatzsch
mode: Presentation
persistent: true
edit: true

import: https://raw.githubusercontent.com/MINT-the-GAP/lia-DynFlex/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-timer/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-board-mode/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-marker/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-annotation/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-canvas-ocr/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-orthography/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-Mathe/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-kachel/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-navigation/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-mathpath/refs/heads/master/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-llm/refs/heads/main/README.md
import: https://raw.githubusercontent.com/liaTemplates/algebrite/master/README.md
import: https://raw.githubusercontent.com/liaTemplates/JSXGraph/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-resetter/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-coordinate/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-freeze-v2/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-loot/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-pentominos/main/README.md


-->

# lia-coordinate in the classroom

@autoscrolling(off)




    --{{0}}--
Hallo mein Name ist Martin Lommatzsch und ich Ihnen heute zeigen, wie wir mit LiaScript interaktive Mathematikaufgaben
erstellen können. Die Grundlage dafür ist JSXGraph. Das Template lia-coordinate von mir ermöglicht dabei einen Zugang über Makros.
Ich zeige zuerst einige Aufgaben aus Sicht der Lernenden. Danach wechseln wir 
in die Rolle der Lehrkraft und bauen selbst eine Konstruktion, die wir in einen
LiaScript-Kurs übernehmen können.



> <h2> LiaScript - OER-eLearning with JXSGraph </h2>
> <h2> Quizzes $\cdot$ Dynamic Geometry System $\cdot$ Export to Courses </h2>

<h3> September 2026, Freiberg </h3>






---

---


<section class="dynFlex">

<div class="flex-child">

![logo](https://raw.githubusercontent.com/MINT-the-GAP/Wochenaufgabe/refs/heads/main/Zeug/Logo.png)

</div>
<div class="flex-child">

<center>

<!-- style="max-width:250px" -->
![logo](https://raw.githubusercontent.com/MINT-the-GAP/Wochenaufgabe/refs/heads/main/Bilder/lrLia.png)


<big><h2> Martin Lommatzsch</h2></big>
<small> Geschwister-Scholl-Gymnasium Freiberg </small>





</center>

</div>
<div class="flex-child">


<!-- style="max-width:600px" -->
![partner_map](https://github.com/LiaPlayground/Saechsischer_Schulinformatik_Tag_2026/blob/main/pic/LiaScript_Meets_OER.png?raw=true "OER-Logo - Quelle: Jonathasmello - Eigenes Werk, CC BY 3.0, [https://commons.wikimedia.org/w/index.php?curid=18460156](https://commons.wikimedia.org/w/index.php?curid=18460156) erweitert um LiaScript-Logo")
</div>

</section>






<center>

---

---

<img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/0.png" width="80" height="80">  $\;\qquad\;$
<img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/1.png" width="80" height="80">  $\;\qquad\;$
<img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/2.png" width="80" height="80">  $\;\qquad\;$
<img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/3.png" width="80" height="80">  $\;\qquad\;$
<img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/4.png" width="80" height="80">  $\;\qquad\;$
<img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/5.png" width="80" height="80"> 

</center>
















## <img alt="" src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/1.png" width="40" height="40"> LiaScript: the foundation for interactive courses

    --{{0}}--
Bevor wir in die Mathematik in der Schule einsteigen, kurz zur Grundlage: LiaScript ist eine
Scriptsprache für interaktive Kurse und basiert auf Markdown. 
LiaScript ist kostenfrei und Open Source. Wenn wir unsere Materialien unter einer
offenen Lizenz als OER veröffentlichen, können andere sie nutzen, anpassen und
weiterentwickeln. Für den Unterricht ist außerdem praktisch, dass die Lernenden
ihre eigenen Geräte verwenden können: Smartphone, Tablet oder Laptop.
Ein moderner Browser genügt. Es braucht keine vorherige App-Installation und
keinen eigenen Schulserver oder ein Lernmanagementsystem. Es gibt auch kein
Pflichtkonto; der Lernfortschritt kann lokal im Browser gespeichert werden. Und LiaScript ist Datenschutzkonform.
Die Kursdateien können an unterschiedlichen Orten liegen. Wir sind also nicht an
eine Plattform gebunden. Bereits geladene Inhalte lassen sich auch offline
weiterbearbeiten, soweit die benötigten Ressourcen lokal verfügbar sind.
Online-Dienste brauchen weiterhin eine Verbindung. Der für mich entscheidende
Punkt sind die Makros: Darin lassen sich auch komplexe Anwendungen verpacken. 
Wie das bei JSXGraph aussieht, veranschauliche ich in den nächsten Folien nachdem 
ich die Bedarfe aus der Sicht einer Lehrkraft dargestellt habe.


<section class="dynFlex" data-basis="49%">

<div class="flex-child">

{{1}}
*************
> <h3> Markdown-based </h3>

A readable language for writing courses with quizzes, feedback and interaction.
*************



{{2}}
*************
> <h3> Open education </h3>

**Free to use** and open source. Create, share and adapt freely accessible **Open Educational Resources (OER)**.
*************

{{3}}
*************
> <h3> Bring your own device (BYOD) </h3>

Use your own smartphone, tablet or laptop with a modern browser.
*************

{{4}}
*************
> <h3> No installation or school server </h3>

Open a course link. No app installation, dedicated school server or LMS required.
*************


</div>
<div class="flex-child">


{{5}}
*************
> <h3> Privacy-friendly </h3>

No account required. Learning progress can be stored locally in the browser.
*************


{{6}}
*************
> <h3> Decentralised </h3>

Host your course files where you choose. Learners open them in a browser.
*************


{{7}}
*************
> <h3> Offline access </h3>

Keep working with previously loaded course content and locally available resources.
*************



{{8}}
*************
> <h3> Extensible through macros </h3>

Reusable **macros** package media, simulations and tools such as **JSXGraph** into simple building blocks.
Use ready-made macros **without programming knowledge**.
*************


</div>

</section>












## <img alt="" src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/2.png" width="40" height="40"> What do STEM teachers need?

    --{{0}}--
Was brauchen wir im MINT-Unterricht eigentlich? 
Wir brauchen Darstellungen von Graphen und geometrischen Figuren.
Die Lernenden sollten Längen und Winkel mit dem Geodreick messen können.
Die Lernenden sollte auch selbst geometrische Figuren mit Geodreieck und Zirkel konstruieren können. Die Lernenden brauchen an dieser Stelle auch eine Rückmeldung bezüglich der Korrektheit ihrer Konstruktion. 
Bei beim Setzen von Punkten oder beim Zeichnen von Graphen sollte eine Rückmeldung erfolgen. 
Aber auch komplett freie Aufgabenstellungen brauchen ein dynamisches Geometriesystem zur Unterstützung. 
Und wie Sie sehen können ist alles über LiaScript-Makros ohne große Programmierkenntnisse einbettbar.
Ich möchte Ihnen im folgenden ein paar Beispiele zeigen.

<div class="coord-slide">

Start with a drawing board: `@CoordinateSystem`

{{1}}
- **Display graphs and geometric figures** $\;\;\Longrightarrow\;\;$ `@PlotFunction`, `@Area`, `@Circle`

{{2}}
- **Measure angles and lengths, and check answers** $\;\;\Longrightarrow\;\;$ `@SetSquare` + LiaScript quiz `[[...]]`

{{3}}
- **Construct with a set square and compass, and check the result** $\;\;\Longrightarrow\;\;$ `@SetSquare`, `@Compass`, `@DGS` + `@ConstructionQuiz`

{{4}}
- **Place points and check their positions** $\;\;\Longrightarrow\;\;$ `@CreatePoint`

{{5}}
- **Draw graphs and check the result** $\;\;\Longrightarrow\;\;$ `@Reconstruction`

{{6}}
- **Use a dynamic geometry system for complex tasks and visual authoring** $\;\;\Longrightarrow\;\;$ `@DGS`

</div>













## <img alt="" src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/3.png" width="40" height="40"> CreatePoint: place a point at a target position

    --{{0}}--
Wir beginnen mit einer einfachen Aufgabe: Der Punkt A soll die Koordinaten zwei
und drei haben. Ich erzeuge den Punkt und ziehe ihn auf seine Position, was LiaScript dann überprüft und rückmeldet.

<div class="coord-slide">

<section class="dynFlex" data-basis="49%">

<div class="flex-child">

@CoordinateSystem(`xmin=-3;xmax=5;ymin=-2;ymax=5;width=800;id=slide1;achsen=1;grid=1;border=1`)

</div>
<div class="flex-child">

**Place** $A$ at the coordinates $(2|3)$.

@CreatePoint(`slide1;A;2;3`,`<!-- data-hint-button="1" data-solution-button="3" -->`)
[[?]] The abscissa is 2 and the ordinate is 3.
**************************************************
$A(2,3)$: abscissa 2, ordinate 3. In $(3|2)$, the coordinates are reversed.
**************************************************

> **Match coordinates to a position.**

**Options:** target coordinates, hint and solution.

**Code example**

``` markdown

@CoordinateSystem(`xmin=-3;xmax=5;ymin=-2;ymax=5;width=800;id=slide1;achsen=1;grid=1;border=1`)
@CreatePoint(`slide1;A;2;3`,`<!-- -->`)

```

- `id=slide1` connects the coordinate system and the quiz.
- `A` names the point that learners create and move.
- `2;3` sets the target: abscissa $2$, ordinate $3$.
- The second argument is a LiaScript quiz comment; add hint and solution options there.

</div>

</section>

</div>
























## <img alt="" src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/3.png" width="40" height="40"> Reconstruction: adjust the graph

    --{{0}}--
Jetzt soll ein ganzer Graph zu vorgegebenen Eigenschaften passen. Über Schieberegler und durch das Panning 
kann der Graph an die gewünschte Position gebracht werden und LiaScript überprüft dann wieder alles.

<div class="coord-slide">

<section class="dynFlex" data-basis="49%">

<div class="flex-child">

@CoordinateSystem(`xmin=-4;xmax=7;ymin=-3;ymax=6;width=800;id=slide2;achsen=1;grid=1;border=1`)
@Schar(`g;x;a*(x-b)^2+c;slide2;term=1;#b41f65`)
@Point(`slide2;S;1;-2;#ff00ff;1;fix`)
@Point(`slide2;P;3;0;#ff00ff;1;fix`)

</div>
<div class="flex-child">

**Adjust** the parabola to have vertex $S(1,-2)$ and pass through $P(3,0)$.

@ReconstructionWithOptions(`slide2;0.5*(x-1)^2-2;0.1`,`<!-- data-hint-button="1" data-solution-button="3" -->`)
[[?]] First determine the vertex shift. Then use the other point to find the vertical scale factor.
**************************************************
A valid setting is $a=0.5$, $b=1$, $c=-2$,
since $0= a\cdot(3-1)^2-2$ gives $a=0.5$.
**************************************************

> **Turn given properties into a graph.**

**Options:** target expression · tolerance · expression display and sliders

**Justify** your settings.

**Code example**

``` markdown
@CoordinateSystem(`xmin=-4;xmax=7;ymin=-3;ymax=6;width=800;id=slide2;achsen=1;grid=1;border=1`)
@Schar(`g;x;a*(x-b)^2+c;slide2;term=1;#b41f65`)
@Point(`slide2;S;1;-2;#ff00ff;1;fix`)
@Point(`slide2;P;3;0;#ff00ff;1;fix`)
@Reconstruction(`slide2;0.5*(x-1)^2-2;0.1`)
```

- The shared board ID connects the graph, the given points and the quiz.
- `@Schar` adds sliders: `a` controls the vertical scale and direction of opening; `(b,c)` is the vertex.
- `@Point(...;fix)` places the two given points and prevents learners from moving them.
- `@Reconstruction` checks the graph against the target expression with tolerance `0.1`; use `@ReconstructionWithOptions` for custom quiz controls.

</div>

</section>

</div>















## <img alt="" src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/3.png" width="40" height="40"> ConstructionQuiz: sides and angles

    --{{0}}--
Bei der nächsten Aufgabe sollen mehrere Eigenschaften gleichzeitig stimmen:
Wir brauchen ein rechtwinkliges Dreieck mit den Seitenlängen drei, vier und fünf. Das zeichne ich mal so ein.
Ich schließe das Dreieck, indem ich den ersten Punkt noch einmal
anklicke, und lasse es prüfen. Mit der Einstellung offen gebe ich keine
feste Reihenfolge der Merkmale vor. Rechts stehen außerdem die Toleranzen für
Längen und Winkel. Über das DGS-Makro wähle ich aus, welche Werkzeuge zur Verfügung
stehen. Die automatische Prüfung bewertet die fertige Figur.

<div class="coord-slide">

<section class="dynFlex" data-basis="49%">

<div class="flex-child">

@CoordinateSystem(`xmin=-1;xmax=7;ymin=-1;ymax=5;width=800;id=slide3;achsen=1;grid=1;border=1`)
@DGS(`slide3;tools=[200;310;410;510;920]`)


</div>
<div class="flex-child">

**Construct** a right-angled triangle with side lengths of $3$, $4$ and $5$ units.
**Close** the polygon by clicking the first point again.

@ConstructionQuiz(`slide3;3;offen;S3,S4,S5,W90;streckentoleranz=0.15;winkeltoleranz=1`,`<!-- data-hint-button="1" data-solution-button="3" -->`)
[[?]] Draw two perpendicular sides of lengths 4 and 3. Then join their free endpoints.
**************************************************
Example: $A(0,0)$, $B(4,0)$, $C(4,3)$. Side lengths: $4$, $3$, $5$ units; angle at $B$: $90^\circ$.
**************************************************

> **Side lengths and angles are checked together.**

**Options:** number of vertices · fixed/unordered sequence of features · tolerances

**Code example**

``` markdown
@CoordinateSystem(`xmin=-1;xmax=7;ymin=-1;ymax=5;width=800;id=slide3;achsen=1;grid=1;border=1`)
@DGS(`slide3;tools=[200;310;410;510;920]`)
@ConstructionQuiz(`slide3;3;offen;S3,S4,S5,W90;streckentoleranz=0.15;winkeltoleranz=1`,`<!-- -->`)

```

- The same board ID connects the coordinate system, the DGS tools and the quiz.
- `tools=[200;310;410;510;920]` enables points, segments, perpendiculars, polygons and the eraser.
- `3;offen;S3,S4,S5,W90` requires three vertices, sides of $3$, $4$, $5$ units and a $90^\circ$ angle, without a prescribed feature order.
- `streckentoleranz=0.15` allows a length deviation of $0.15$ units; `winkeltoleranz=1` allows an angle deviation of $1^\circ$.

</div>

</section>

</div>
















## <img alt="" src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/3.png" width="40" height="40"> AreaQuiz: from area to shape

    --{{0}}--
Hier drehen wir eine bekannte Aufgabenstellung um. Vorgegeben ist ein
Flächeninhalt von zwölf Flächeneinheiten; die Lernenden sollen ein passendes
Viereck herstellen. Ich zeichne als Beispiel so ein Rechteck mit den Seitenlängen, schließe es und prüfe. 
Die Aufgabe lässt also verschiedene Lösungen zu. Dabei muss die Figur
überhaupt kein Rechteck sein: Geprüft werden vier Eckpunkte und der Flächeninhalt.
Im Makro sind das die Angaben vier und zwölf, gefolgt von der Toleranz.

<div class="coord-slide">

<section class="dynFlex" data-basis="49%">

<div class="flex-child">

@CoordinateSystem(`xmin=-1;xmax=7;ymin=-1;ymax=5;width=800;id=slide4;achsen=1;grid=1;border=1`)
@DGS(`slide4;tools=[200;510;920]`)

</div>
<div class="flex-child">

**Construct** a quadrilateral with an area of $12$ square units.

@AreaQuiz(`slide4;4;12;0.5`,`<!-- data-hint-button="1" data-solution-button="3" -->`)
[[?]] The area of a rectangle is the product of its side lengths.
**************************************************
A rectangle with sides of $4$ units and $3$ units has an area of $12$ square units; so does one with sides of $6$ units and $2$ units.
**************************************************

> **Different shapes can have the same area.**

**Options:** number of vertices · target area · tolerance

**Code example**

``` markdown
@CoordinateSystem(`xmin=-1;xmax=7;ymin=-1;ymax=5;width=800;id=slide4;achsen=1;grid=1;border=1`)
@DGS(`slide4;tools=[200;510;920]`)
@AreaQuiz(`slide4;4;12;0.15`,`<!-- -->`)
```

- `slide4` connects the board, tools and quiz; `200;510;920` enables points, polygons and the eraser.
- `4` requires a closed polygon with four vertices.
- `12;0.15` sets the target area to $12$ square units, with an absolute tolerance of $0.15$ square units.
- The check accepts any quadrilateral meeting these conditions; it does not require a rectangle.

</div>

</section>

</div>















## <img alt="" src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/3.png" width="40" height="40"> PerimeterQuiz: specify the perimeter

    --{{0}}--
Auf dieser Folie ist der Umfang vorgegeben: vierzehn Längeneinheiten.
Die beiden Aufgaben zusammen machen den Unterschied zwischen Umfang und
Flächeninhalt gut sichtbar. Technisch tausche ich dafür AreaQuiz gegen
PerimeterQuiz aus und gebe den gewünschten Umfang an. Die Zahl der Eckpunkte
und die Toleranz bleiben eigene Angaben. Auch hier sind Rechtecke lediglich
unsere Beispiele; verlangt ist allgemein ein Viereck.

<div class="coord-slide">

<section class="dynFlex" data-basis="49%">

<div class="flex-child">

@CoordinateSystem(`xmin=-1;xmax=7;ymin=-1;ymax=5;width=800;id=slide5;achsen=1;grid=1;border=1`)
@DGS(`slide5;tools=[200;510;920]`)

</div>
<div class="flex-child">

**Construct** a quadrilateral with a perimeter of $14$ units.

@PerimeterQuiz(`slide5;4;14;0.5`,`<!-- data-hint-button="1" data-solution-button="3" -->`)
[[?]] For a rectangle, the perimeter is $P=2a+2b$. Choose side lengths whose sum is 7.
**************************************************
A rectangle with sides of $4$ units and $3$ units has a perimeter of $14$ units; so does one with sides of $5$ units and $2$ units.
**************************************************

> **The same perimeter does not determine the area.**

**Options:** number of vertices · target perimeter · tolerance

**Code example**

``` markdown
@CoordinateSystem(`xmin=-1;xmax=7;ymin=-1;ymax=5;width=800;id=slide5;achsen=1;grid=1;border=1`)
@DGS(`slide5;tools=[200;510;920]`)
@PerimeterQuiz(`slide5;4;14;0.15`,`<!-- -->`)
```

- `slide5` connects the board, tools and quiz; `200;510;920` enables points, polygons and the eraser.
- `4` requires a closed polygon with four vertices.
- `14;0.15` sets the target perimeter to $14$ units, with an absolute tolerance of $0.15$ units.
- Only the perimeter and vertex count are prescribed; the area and shape may vary.

</div>

</section>

</div>

















## <img alt="" src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/3.png" width="40" height="40"> CoordinateQuiz: all conditions on one shape

    --{{0}}--
Mit CoordinateQuiz können wir mehrere Bedingungen an dieselbe Figur stellen.
Hier soll ein Parallelogramm entstehen, das zwölf Flächeneinheiten groß ist und
ausdrücklich kein Rechteck sein darf. Ich nehme eine Grundseite der Länge vier
und eine Höhe von drei. Ich schließe die Figur und prüfe. Gegenüberliegende Seiten sind
parallel; Grundseite mal Höhe ergibt zwölf. Durch die Verschiebung haben wir
keine rechten Winkel. Der Ausschluss ist hier eine bewusste Aufgabenentscheidung:
Ein Rechteck ist mathematisch ebenfalls ein Parallelogramm. Wenn ich es nicht
zulassen möchte, muss ich das zusätzlich angeben. Genau das steht rechts im Code.
Form und Flächeninhalt werden gemeinsam geprüft. Auf diese Weise lassen sich
auch Bedingungen zu Seiten, Winkeln und Umfang miteinander verbinden.

<div class="coord-slide">

<section class="dynFlex" data-basis="49%">

<div class="flex-child">

@CoordinateSystem(`xmin=-1;xmax=7;ymin=-1;ymax=6;width=800;id=slide6;achsen=1;grid=1;border=1`)
@DGS(`slide6;tools=[200;310;420;510;920]`)

</div>
<div class="flex-child">

**Construct** a parallelogram with an area of $12$ square units that is not a rectangle.

@CoordinateQuiz(`slide6;4;Form(Parallelogramm;exklusiv=Rechteck);Flaeche(12;0.5)`,`<!-- data-hint-button="1" data-solution-button="3" -->`)
[[?]] Use $A=b\cdot h$. Choose a suitable base and height, then shift the top side sideways.
**************************************************
Example: $(0,0)$, $(4,0)$, $(5,3)$, $(1,3)$. Opposite sides are parallel, $A=4\cdot3=12$ square units, and none of the interior angles is a right angle.
**************************************************

> **One shape must meet all requirements.**

**Combine:** shape class · sides/angles · area · perimeter

Also available as: `@GeometryQuiz`

**Code example**

``` markdown
@CoordinateSystem(`xmin=-1;xmax=7;ymin=-1;ymax=6;width=800;id=slide6;achsen=1;grid=1;border=1`)
@DGS(`slide6;tools=[200;310;420;510;920]`)
@CoordinateQuiz(`slide6;4;Form(Parallelogramm;exklusiv=Rechteck);Flaeche(12;0.1)`,`<!-- -->`)
```

- The board ID links all three macros; the DGS tools include segments, parallels and polygons.
- `4;Form(Parallelogramm;exklusiv=Rechteck)` requires four vertices forming a parallelogram and explicitly excludes rectangles.
- `Flaeche(12;0.1)` requires an area of $12$ square units, with an absolute tolerance of $0.1$ square units.
- All conditions must hold for the same polygon; `@GeometryQuiz` is an alias for the same combined check.

</div>

</section>

</div>





























## <img alt="" src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/3.png" width="40" height="40"> PlotInput: from handwriting to a graph

    --{{0}}--
Bevor wir selbst Materialien erstellen, noch eine weitere Verbindung:
Wir können einen Funktionsterm auch handschriftlich eingeben und daraus den
Graphen zeichnen lassen. Ich öffne über den Stift die Zeichenfläche und schreibe
den Funktionsterm nieder, markiere ihn und kontrolliere
kurz, ob alles richtig erkannt wurde. Falls nötig, kann ich den Term im Feld
korrigieren. Mit Plot zeichne ich anschließend den Graphen.
Hier wird sichtbar, wie sich die Vorlagen ergänzen: PlotInput liefert das
Funktionsfeld, canvas ergänzt die Handschrifterkennung. Beide nutzen wir zusammen
mit unserem Koordinatensystem. Für den Unterricht
kann ich so direkt von einem handgeschriebenen Term zu seinem Graphen wechseln.
Jetzt gehen wir einen Schritt weiter und erstellen selbst eine geometrische Szene.

<div class="coord-slide">

<section class="dynFlex" data-basis="49%">

<div class="flex-child">

@CoordinateSystem(`xmin=-4;xmax=6;ymin=-3;ymax=6;width=800;id=slideOCR;achsen=1;grid=1;border=1`)

</div>
<div class="flex-child">

**Write** each expression by hand using the pen button. **Select** it with the recognition tool, check the recognized expression, then click **Plot**.

**Parabola:** $f(x)=\dfrac12x^2-2$

@PlotInput(`slideOCR;f;#b41f65`)

@canvas


> **Handwriting → expression → graph.**

**Code example**

``` markdown
@CoordinateSystem(`xmin=-4;xmax=6;ymin=-3;ymax=6;width=800;id=slideOCR;achsen=1;grid=1;border=1`)
@PlotInput(`slideOCR;f;#b41f65`)

@canvas

```

- `slideOCR` connects the function input to the coordinate system.
- `@PlotInput` sets the function name and graph colour.
- `@canvas` adds handwriting recognition to the preceding input field.
- Correct the recognized expression if needed; click **Plot** or press Enter to draw the graph.

</div>

</section>

</div>


## <img alt="" src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/4.png" width="40" height="40"> Create and export in the DGS

    --{{0}}--
Bis hierher haben wir Aufgaben aus Sicht der Lernenden betrachtet. Jetzt möchte
ich als Lehrkraft selbst etwas erstellen. Dafür öffne ich im DGS die passenden
Werkzeuge. Über einen Rechtsklick öffne ich die
Eigenschaften eines Objekts. Ich kann beispielsweise den Namen ändern oder die
Höhe farblich hervorheben. So gestalte ich die Darstellung passend zu meiner
Aufgabe. Wenn die Konstruktion fertig ist, öffne ich die Objektliste und wähle
den Export. Dort lege ich fest, welche Werkzeuge und Änderungsmöglichkeiten
im späteren Kurs verfügbar sein sollen. Anschließend kopiere ich den erzeugten
LiaScript-Code. Im vorbereiteten LiveEditor sind der Kurskopf mit den benötigten
Importen und ein kurzer Arbeitsauftrag bereits vorhanden. Ich füge die
Konstruktion ein und öffne die Vorschau. 
Für eine automatische Bewertung würde ich noch ein passendes Quiz ergänzen.
Zum Weitergeben veröffentliche ich die Kursdatei an einem erreichbaren Ort
wie die Homepage meiner Schule oder ein Lernmanagementsystem und
kann den Lernenden anschließend den LiaScript-Link schicken. So wird aus der
Konstruktion ein Material, das ich wiederverwenden und für andere Lerngruppen
anpassen kann.

<div class="coord-slide">

<section class="dynFlex" data-basis="49%">

<div class="flex-child">

@CoordinateSystem(`xmin=-1;xmax=7;ymin=-2;ymax=5;width=800;id=slide7;achsen=1;grid=1;border=1`)
@DGS(`slide7`)

</div>
<div class="flex-child">

- **Create:** Build an interactive construction with the DGS tools.
- **Customize:** Right-click an object to change its name, colour and other properties.
- **Export:** Open the **object list → Export**, choose tools and permissions, then copy the LiaScript code.
- **Build the course:** Paste the code into the [LiaScript LiveEditor](https://liascript.github.io/LiveEditor/), include the required template imports and add your task instructions.
- **Share:** Preview the course, publish the course file and send its LiaScript link to your students.




</div>

</section>

</div>


























## <img alt="" src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/5.png" width="40" height="40"> Closing

    --{{0}}--
Was haben wir heute gesehen? Mit wenigen Makros entstehen in LiaScript Aufgaben,
bei denen Lernende Punkte setzen, Graphen anpassen und Figuren konstruieren.
Dabei lassen sich Positionen, Seiten, Winkel, Flächeninhalte und Umfänge prüfen
und mehrere Bedingungen miteinander verbinden. Wir haben außerdem einen
handschriftlichen Terme und Skizzen erkannt.
Anschließend haben wir im DGS selbst eine Konstruktion erstellt, ihre
Eigenschaften angepasst und sie über den Export in den LiveEditor übernommen.
Damit haben wir den Weg von der einzelnen interaktiven Aufgabe zum eigenen,
wiederverwendbaren Kurs durchgespielt. 
Als Nächstes würde ich versuchen Animationen und dreidimensionale Geometrie im DGS zu realisieren. Doch bevor ich mich daran neben meiner Lehrertätigkeit machen werden, werde ich versuchen mehr Skizzen direkt in Grafiken zu übersetzen, sodass jede Lehrkraft dieses Template ohne Vorkenntnisse nutzen kann.
Auch weitere LiaScript-Quizze sind denkbar.
Vielen Dank fürs Zuhören.

<div class="coord-slide">

> <h2> From interactive tasks to a reusable course </h2>

**What we have shown**

- **Reusable macros:** Create interactive mathematics tasks in LiaScript.
- **Checked answers:** Place points, adjust graphs and construct shapes that meet geometric conditions.
- **Handwriting to graphs:** Recognize a handwritten expression and plot the function.
- **Visual authoring:** Build and customize a DGS construction, export it to the LiveEditor and prepare a course to share.

**Looking ahead**

- **Animations:** Explore movement and changes in parameters over time.
- **3D geometry in the DGS:** Construct spatial figures, view them from different perspectives and explore geometric relationships.

<h3> Thank you for your attention. </h3>


</div>











