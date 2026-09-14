<!--
version:  0.2.0
language: en
narrator: US English Female

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
import: https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/main/imports/RedirecterREADME.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-loot/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-pentominos/main/README.md


-->

# lia-coordinate in the classroom

@autoscrolling(off)




    --{{0}}--
Hello, my name is Martin Lommatzsch, and today I'd like to show you how we can create
interactive mathematics tasks with LiaScript. The underlying technology is JSXGraph.
My lia-coordinate template makes it accessible through macros.
I'll start with a few tasks from the learners' perspective. Then we'll switch
to the teacher's role and build our own construction, which we can include
in a LiaScript course.



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
















## <img alt="" src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/1.png" width="40" height="40"> LiaScript: the foundation for interactive courses

    --{{0}}--
Before we get into mathematics in the classroom, a quick word about the foundation:
LiaScript is a scripting language for interactive courses, based on Markdown.
LiaScript is free and open source. If we publish our materials as OER under an
open licence, others can use, adapt and develop them further.
Another practical benefit for teaching is that learners can use their own devices:
a smartphone, tablet or laptop. All they need is a modern browser.
There is no need to install an app beforehand, run a dedicated school server
or use a learning management system. There is no compulsory account either;
learning progress can be stored locally in the browser. And LiaScript complies
with data protection requirements.
The course files can be hosted in different places, so we are not tied to a
single platform. Learners can continue working offline with content they have
already loaded, provided the required resources are available locally.
Online services still need a connection. For me, the key feature is macros:
they can package even complex applications.
I'll show you what this looks like with JSXGraph in the next few slides,
after outlining what we need from a teacher's perspective.


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
What do we actually need in STEM teaching?
We need ways to display graphs and geometric figures.
Learners should be able to measure lengths and angles with a set square.
They should also be able to construct geometric figures themselves with a set
square and compass. At that point, they need feedback on whether their
construction is correct. They should also receive feedback when placing points
or drawing graphs. Even completely open-ended tasks need support from a dynamic
geometry system. And as you can see, all of this can be embedded using LiaScript
macros without much programming knowledge.
I'd now like to show you a few examples.

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
We'll start with a simple task: point A should have the coordinates two
and three. I create the point and drag it into position. LiaScript then checks
its position and provides feedback.

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
Now we want an entire graph to match a given set of properties. Using the sliders
and panning, I can move the graph into the required position, and LiaScript
checks everything again.

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
In the next task, several properties need to be correct at the same time:
we need a right-angled triangle with side lengths of three, four and five.
I'll draw one like this. I close the triangle by clicking the first point again,
then check it. With the open setting, I do not prescribe a fixed order for the
features. On the right, you can also see the tolerances for lengths and angles.
The DGS macro lets me choose which tools are available.
The automatic check assesses the completed shape.

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
Here, we turn a familiar task around. We specify an area of twelve square units,
and the learners need to create a suitable quadrilateral. As an example,
I'll draw a rectangle like this, with these side lengths, close it and check it.
So this task allows different solutions. The shape does not even have to be a
rectangle: the check looks for four vertices and the required area.
In the macro, these are the values four and twelve, followed by the tolerance.

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
On this slide, we specify the perimeter: fourteen units.
Together, these two tasks clearly show the difference between perimeter
and area. In the code, I simply replace AreaQuiz with PerimeterQuiz and enter
the required perimeter. The number of vertices and the tolerance remain
separate settings. Here too, rectangles are just our examples;
the task asks for any quadrilateral.

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
With CoordinateQuiz, we can apply several conditions to the same shape.
Here, we want a parallelogram with an area of twelve square units,
and it must explicitly not be a rectangle. I'll use a base of length four
and a height of three. I close the shape and check it. Opposite sides are
parallel, and base times height gives twelve. By shifting the top side,
we avoid right angles. Excluding rectangles is a deliberate choice in this task:
mathematically, a rectangle is also a parallelogram. If I do not want to allow
it, I have to specify that separately. That is exactly what the code on the
right says. The shape and its area are checked together. In the same way,
we can combine conditions for sides, angles and perimeter.

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
Before we create our own materials, let me show you one more connection:
we can also enter a function expression by hand and have its graph drawn for us.
I use the pen button to open the drawing area and write the expression,
select it and briefly check that everything has been recognised correctly.
If necessary, I can correct the expression in the input field.
Then I click Plot to draw the graph.
This shows how the templates complement each other: PlotInput provides the
function input field, and canvas adds handwriting recognition. We use both
together with our coordinate system. In the classroom, this lets me move
directly from a handwritten expression to its graph.
Now we'll take the next step and create a geometric scene ourselves.

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
So far, we have looked at tasks from the learners' perspective. Now I want
to create something myself as a teacher. To do that, I open the relevant
tools in the DGS. A right-click opens an object's properties. For example,
I can change its name or highlight the height in colour. This lets me adapt
the display to my task. When the construction is finished, I open the object
list and choose Export. There, I decide which tools and editing options
will be available in the course. Then I copy the generated LiaScript code.
In the prepared LiveEditor, the course header with the required imports and
a short task instruction are already in place. I paste in the construction
and open the preview.
For automatic assessment, I would also add a suitable quiz.
To share it, I publish the course file somewhere accessible, such as my school's
website or a learning management system, and then send the learners the
LiaScript link. This turns the construction into a resource that I can reuse
and adapt for other groups of learners.

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
What have we seen today? With just a few macros, we can create LiaScript tasks
in which learners place points, adjust graphs and construct shapes.
We can check positions, sides, angles, areas and perimeters, and combine
several conditions. We have also recognised handwritten expressions and sketches.
Then we created our own construction in the DGS, adjusted its properties
and exported it to the LiveEditor. That took us all the way from a single
interactive task to our own reusable course.
Next, I would like to try adding animations and three-dimensional geometry
to the DGS. But before I take that on alongside my teaching work, I will try
to convert more sketches directly into graphics, so that any teacher can use
this template without prior knowledge.
Further LiaScript quizzes are also possible.
Thank you for listening.

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









