<!--
version:  0.3.1
language: en
narrator: US English Female

tags: Presentation, Teacher training, LiaScript, lia-coordinate, DGS, Mathematics, OER
comment:  lia-coordinate in the classroom: representations, tasks, teaching choices
          and the path from a visual DGS construction to a reusable worksheet.
author:   Martin Lommatzsch
mode: Presentation
persistent: true
edit: true


import: https://raw.githubusercontent.com/liaTemplates/algebrite/master/README.md
import: https://raw.githubusercontent.com/liaTemplates/JSXGraph/main/README.md

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
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-resetter/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-coordinate/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-freeze-v2/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-loot/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-pentominos/main/README.md


-->

# lia-coordinate in the classroom

@autoscrolling(off)






> <h2> LiaScript - OER-eLearning with JSXGraph </h2>
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
![partner_map](https://github.com/LiaPlayground/Saechsischer_Schulinformatik_Tag_2026/blob/main/pic/LiaScript_Meets_OER.png?raw=true "OER logo - Source: Jonathasmello - Own work, CC BY 3.0, [https://commons.wikimedia.org/w/index.php?curid=18460156](https://commons.wikimedia.org/w/index.php?curid=18460156) with the LiaScript logo added")
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

## Agenda

<img alt="Step 1" src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/1.png" width="40" height="40">  <big><big><b> LiaScript: the foundation </b></big></big>

---

---

<img alt="Step 2" src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/2.png" width="40" height="40">  <big><big><b> What STEM teachers need </b></big></big>

---

---

<img alt="Step 3" src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/3.png" width="40" height="40">  <big><big><b> Interactive tasks with lia-coordinate </b></big></big>

---

---

<img alt="Step 4" src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/4.png" width="40" height="40">  <big><big><b> Create and export via macros </b></big></big>

---

---

<img alt="Step 5" src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/5.png" width="40" height="40">  <big><big><b> Outlook </b></big></big>




## <img alt="" src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/1.png" width="40" height="40"> LiaScript: the foundation for interactive courses

    --{{0}}--
LiaScript supports interactive mathematics tasks in browser-based courses.
The underlying dynamic-geometry technology is JSXGraph; the `lia-coordinate`
template exposes its functions through reusable macros. This course first
presents tasks from the learners' perspective and then documents how a visual
construction can be created, exported and embedded in a LiaScript course.
LiaScript is an open-source scripting language for interactive courses based
on Markdown. Courses can be published as Open Educational Resources so that
others may use, adapt and further develop them under the chosen open licence.
Learners can access a course with a modern browser on a smartphone, tablet or
laptop. A dedicated app, school server, learning management system or compulsory
user account is not required. Learning progress can be stored locally in the
browser, and course files can be hosted on different platforms. Previously
loaded content can remain available offline when all required resources are
stored locally; external online services still require a connection. LiaScript
macros package complex applications such as JSXGraph into reusable building
blocks that can be used without programming knowledge.


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
Digital STEM tasks need suitable representations of graphs and geometric
figures as well as tools for measuring lengths and angles. Learners should be
able to construct figures with instruments such as a set square and compass
and receive feedback on the completed construction. Comparable feedback is
useful when placing points, adjusting graphs or working on open-ended geometry
tasks. The `lia-coordinate` macros connect these requirements with a dynamic
geometry system and embed the resulting activities in LiaScript without
requiring extensive programming knowledge.

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
`@CreatePoint` creates a movable point and checks its position against target
coordinates. In this example, point $A$ must be placed at $(2|3)$. The macro
connects the point to the coordinate system, evaluates its position and returns
feedback when the learner checks the task.

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
`@Reconstruction` checks whether an entire graph matches a target expression.
Parameters can be changed with sliders, while panning supports the adjustment
of the displayed graph. The example combines a prescribed vertex with an
additional point and verifies the resulting parabola within a defined tolerance.

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
`@ConstructionQuiz` evaluates several geometric properties of one construction.
The example requires a right-angled triangle with side lengths of $3$, $4$ and
$5$ units. A polygon is completed by selecting its first point again. The open
setting accepts the required features in any order, while separate tolerances
control the assessment of lengths and angles. The accompanying `@DGS` macro
determines which construction tools are available.

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
`@AreaQuiz` specifies a target area and asks learners to construct a suitable
polygon. The example requires a quadrilateral with an area of $12$ square units.
Different shapes are accepted because the check evaluates only the number of
vertices and the area within the stated tolerance. The principal parameters
therefore define the board, four vertices, the target area and the tolerance.

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
`@PerimeterQuiz` checks a polygon against a target perimeter. The example asks
for any quadrilateral with a perimeter of $14$ units; the rectangle shown in
the solution is only one possible construction. Comparing this task with
`@AreaQuiz` highlights that equal perimeters do not imply equal areas. The
number of vertices, target perimeter and tolerance remain independent settings.

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
`@CoordinateQuiz` combines several conditions that must hold for the same
shape. The example requires a parallelogram with an area of $12$ square units
and explicitly excludes rectangles. This exclusion is necessary because every
rectangle is also a parallelogram. A base of $4$ units and a height of $3$ units
provide the required area; shifting the upper side avoids right angles. Shape
class and area are checked together, and comparable combinations can include
conditions for side lengths, angles or perimeter.

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
`@PlotInput` provides an input field for a function expression and draws the
corresponding graph in the connected coordinate system. Combined with `@canvas`,
the expression can be entered by hand: the written expression is selected,
recognised and transferred to the input field, where it can be corrected before
plotting. The two templates therefore support a direct workflow from a
handwritten mathematical expression to its graphical representation.

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
The dynamic geometry system can also serve as a visual authoring environment.
After a construction has been created, an object's properties can be opened
with a right-click to change its name, colour or other attributes. The export
dialog in the object list defines the tools and editing options available in
the course and generates the corresponding LiaScript code. This code can be
pasted into a course in the LiaScript LiveEditor together with the required
imports, task instructions and, where appropriate, a quiz for automatic
assessment. Publishing the course file on an accessible website or learning
management system provides a reusable link that can be shared and adapted for
different groups of learners.

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


























## <img alt="" src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/5.png" width="40" height="40"> Outlook

    --{{0}}--
The examples show how a small set of macros supports point placement, graph
adjustment and geometric construction in LiaScript. Automatic checks can cover
positions, side lengths, angles, areas, perimeters and combinations of several
conditions. Handwriting recognition connects written expressions with plotted
graphs. The DGS export workflow turns a visual construction into LiaScript code
that can be included in a reusable course. Possible extensions include
animations, three-dimensional geometry, direct conversion of sketches into
graphics and additional LiaScript quiz formats.

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






