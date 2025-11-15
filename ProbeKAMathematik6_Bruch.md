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
@end

formula: \carry   \textcolor{red}{\scriptsize #1}
formula: \digit   \rlap{\carry{#1}}\phantom{#2}#2
formula: \permil  \text{‰}






@onload
window.segments = window.segments || {}

window.toggleSegments = function (uid, i) {
  segments[uid][i] = !segments[uid][i]
}

window.rects    = window.rects    || {}
window.rectDims = window.rectDims || {}

window.toggleRect = function (uid, i) {
  rects[uid][i] = !rects[uid][i]}
@end

@circleQuiz: @circleQuiz_(@uid,@0)

@circleQuiz_
<script modify="false">
const segments = @input(`segments-@0`);
const cx = 145, cy = 150, r = 140;

const circleFill = "white";  // Hintergrundfarbe Kreis
const lineColor  = "black";          // Linienfarbe
const segmentFill = "orange";     // Füllfarbe aktiver Segmente

const step = 360 / segments;
const startOffset = -90;

let lines = "";
let slices = "";

if (segments > 1) {
  for (let i = 0; i < segments; i++) {
    const a0 = (startOffset + step * i) * Math.PI / 180;
    const a1 = (startOffset + step * (i + 1)) * Math.PI / 180;

    const x0 = cx + r * Math.cos(a0), y0 = cy + r * Math.sin(a0);
    const x1 = cx + r * Math.cos(a1), y1 = cy + r * Math.sin(a1);

    const largeArc = (step > 180) ? 1 : 0;
    const sweep = 1;

    const isActive = window.segments['@0'][i];
    slices += `
      <path class="slice@0 slice@0 ${isActive ? 'active' : ''}"
            d="M ${cx},${cy} L ${x0},${y0} A ${r},${r} 0 ${largeArc},${sweep} ${x1},${y1} Z"
            onclick="
              this.classList.toggle('active');
              toggleSegments('@0', ${i});
            ">
      </path>
    `;

    lines += `<line x1="${cx}" y1="${cy}" x2="${x0}" y2="${y0}" stroke="${lineColor}" stroke-width="2"/>`;
  }
} else {
    const isActive = window.segments['@0'][0];
    slices = `
    <circle class="slice@0 ${isActive ? 'active' : ''}"
            cx="${cx}" cy="${cy}" r="${r}"
            onclick="this.classList.toggle('active'); toggleSegments('@0', 0);">
    </circle>
  `;
}

`HTML:
<svg viewBox="0 0 300 300" xmlns="http://www.w3.org/2000/svg" width="300" height="300" 
     style="--line:${lineColor}; --segment:${segmentFill}">
  <style>
    .slice@0 { fill: transparent; cursor: pointer; }
    .slice@0.active { fill: var(--segment); }
  </style>

  <circle cx="${cx}" cy="${cy}" r="${r}" stroke="${lineColor}" stroke-width="2" fill="${circleFill}"/>
  ${slices}
  ${lines}
</svg>
`
</script>






<script run-once modify="false" input="range" output="segments-@0" value="1" min="1" max="32" input-always-active>
if (!segments["@0"] || @input != segments["@0"].length) {
  segments["@0"] = Array(@input).fill(false);
}

@input
</script>

[[!]]
<script>
@1 === ((window.segments["@0"].filter(i => i).length) / window.segments["@0"].length)
</script>
@end











@rectQuiz: @rectQuiz_(@uid,@0)

@rectQuiz_
<script modify="false">
/*
  WICHTIG:
  - Rows/Cols kommen NUR aus window.rectDims['@0'].
  - Die folgenden zwei Dummy-Zeilen dienen ausschließlich als REAKTIONS-TRIGGER,
    damit LiaScript das SVG neu rendert, wenn die Slider bewegt werden.
    Sie werden NICHT als Datenquelle verwendet.
*/
const _rowsTrigger = @input(`rows-@0`);
const _colsTrigger = @input(`cols-@0`);

/* Quelle der Wahrheit: globale Variable */
const dims = window.rectDims['@0'] || { rows: 1, cols: 1 };
const rows = Math.max(1, +dims.rows || 1);
const cols = Math.max(1, +dims.cols || 1);

const W = 300, H = 300, padding = 8;
const usableW = W - 2*padding, usableH = H - 2*padding;


const bgFill     = "white";      // Hintergrundfarbe der Fläche
const lineColor  = "black";  // Linienfarbe
const cellFill   = "orange";    // Füllfarbe aktiver Zellen
const cellGap    = 0;            // Lücke zwischen Zellen (px)

const rw = usableW / cols;
const rh = usableH / rows;

/* Auswahlarray-Größe absichern */
const total = rows * cols;
if (!window.rects['@0'] || window.rects['@0'].length !== total) {
  window.rects['@0'] = Array(total).fill(false);
}

let gridRects = "";
let gridLines = "";

/* Zellen (anklickbar) */
for (let r = 0; r < rows; r++) {
  for (let c = 0; c < cols; c++) {
    const i = r*cols + c;
    const x = padding + c*rw + cellGap/2;
    const y = padding + r*rh + cellGap/2;
    const w = rw - cellGap;
    const h = rh - cellGap;

    const isActive = window.rects['@0'][i];

    gridRects += `
      <rect class="cell@0 ${isActive ? 'active' : ''}"
            x="${x}" y="${y}" width="${Math.max(0,w)}" height="${Math.max(0,h)}"
            onclick="this.classList.toggle('active'); toggleRect('@0', ${i});">
      </rect>
    `;
  }
}

/* Gitterlinien */
for (let r = 0; r <= rows; r++) {
  const y = padding + r*rh;
  gridLines += `<line x1="${padding}" y1="${y}" x2="${W-padding}" y2="${y}" stroke="${lineColor}" stroke-width="2"/>`;
}
for (let c = 0; c <= cols; c++) {
  const x = padding + c*rw;
  gridLines += `<line x1="${x}" y1="${padding}" x2="${x}" y2="${H-padding}" stroke="${lineColor}" stroke-width="2"/>`;
}

`HTML:
<svg viewBox="0 0 ${W} ${H}" xmlns="http://www.w3.org/2000/svg" width="${W}" height="${H}"
     style="--line:${lineColor}; --cell:${cellFill}">
  <style>
    .cell@0 { fill: transparent; cursor: pointer; }
    .cell@0.active { fill: var(--cell); }
  </style>

  <rect x="0" y="0" width="${W}" height="${H}" fill="${bgFill}" stroke="${lineColor}" stroke-width="2"/>
  ${gridRects}
  ${gridLines}
</svg>
`
</script>

<script run-once modify="false" input="range" output="rows-@0" value="1" min="1" max="20" input-always-active>
/* Initialisieren, falls nötig */
window.rectDims = window.rectDims || {};
const current = window.rectDims['@0'] || { rows: 1, cols: 1 };
const newRows = Math.max(1, +@input || 1);
const cols    = Math.max(1, +current.cols || 1);

window.rectDims['@0'] = { rows: newRows, cols };

/* Auswahlarray-Größe anpassen */
window.rects = window.rects || {};
const total = newRows * cols;
if (!window.rects['@0'] || window.rects['@0'].length !== total) {
  window.rects['@0'] = Array(total).fill(false);
}

/* @input zurückgeben (Anzeige im UI), aber NICHT als Logikquelle genutzt */
@input
</script>

<script run-once modify="false" input="range" output="cols-@0" value="1" min="1" max="20" input-always-active>
window.rectDims = window.rectDims || {};
const current = window.rectDims['@0'] || { rows: 1, cols: 1 };
const newCols = Math.max(1, +@input || 1);
const rows    = Math.max(1, +current.rows || 1);

window.rectDims['@0'] = { rows, cols: newCols };

/* Auswahlarray-Größe anpassen */
window.rects = window.rects || {};
const total = rows * newCols;
if (!window.rects['@0'] || window.rects['@0'].length !== total) {
  window.rects['@0'] = Array(total).fill(false);
}

/* @input zurückgeben (Anzeige im UI), aber NICHT als Logikquelle genutzt */
@input
</script>

[[!]]
<script>
@1 === (
  (window.rects["@0"].filter(i => i).length) /
  Math.max(1, window.rects["@0"].length)
)
</script>
@end

















import: https://raw.githubusercontent.com/LiaTemplates/Tikz-Jax/main/README.md

script: https://cdn.jsdelivr.net/gh/LiaTemplates/Tikz-Jax@main/dist/index.js

import: https://raw.githubusercontent.com/liaTemplates/algebrite/master/README.md
        https://raw.githubusercontent.com/liaTemplates/JSXGraph/main/README.md

import: https://raw.githubusercontent.com/LiaTemplates/GGBScript/refs/heads/main/README.md


-->

# Probeleistungskontrolle für Mathematik - Klasse 6: Bruchrechnung

<br>

Swipe (Wische) entweder weiter oder klicke unten links auf neben der Seitenzahl auf den Pfeil nach rechts.

<br>

Diese Probearbeit hat mehr Aufgaben als die richtige Arbeit, damit du genug zum Üben hast. Es sind viele verschiedene Aufgabentypen abgebildet, sodass du alles nochmal bei der Bearbeitung dieser Aufgaben wiederholst.

<br>


### Aufgabe 1

**Berechne** den Wert des Terms.



<section class="flex-container">

<div class="flex-child">
<!-- data-solution-button="5"-->
__$a)\;\;$__ $  \dfrac{4}{9} + \dfrac{5}{12} = $ [[  31/36  ]]
@Algebrite.check(31/36)
************
$$
\begin{align*}
\dfrac{4}{9} + \dfrac{5}{12}
&= \dfrac{4\cdot 4}{9\cdot 4} + \dfrac{5\cdot 3}{12\cdot 3} \\
&= \dfrac{16}{36} + \dfrac{15}{36} \\
&= \dfrac{31}{36}
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$b)\;\;$__ $  \dfrac{7}{10} - \dfrac{1}{4} = $ [[  9/20  ]]
@Algebrite.check(9/20)
************
$$
\begin{align*}
\dfrac{7}{10} - \dfrac{1}{4}
&= \dfrac{7\cdot 2}{10\cdot 2} - \dfrac{1\cdot 5}{4\cdot 5} \\
&= \dfrac{14}{20} - \dfrac{5}{20} \\
&= \dfrac{9}{20}
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$c)\;\;$__ $  \dfrac{4}{7} \cdot \dfrac{6}{11} = $ [[  24/77  ]]
@Algebrite.check(24/77)
************
$$
\begin{align*}
\dfrac{4}{7} \cdot \dfrac{6}{11}
&= \dfrac{4 \cdot 6}{7 \cdot 11} \\
&= \dfrac{24}{77}
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$d)\;\;$__ $  \dfrac{9}{10} : \dfrac{3}{20} = $ [[  6  ]]
@Algebrite.check(6)
************
$$
\begin{align*}
\dfrac{9}{10} : \dfrac{3}{20}
&= \dfrac{9}{10} \cdot \dfrac{20}{3} \\
&= \dfrac{180}{30} \\
&= 6
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$e)\;\;$__ $  \dfrac{5}{14} + \dfrac{9}{21} = $ [[  33/42  ]]
@Algebrite.check(33/42)
************
$$
\begin{align*}
\dfrac{5}{14} + \dfrac{9}{21}
&= \dfrac{5\cdot 3}{14\cdot 3} + \dfrac{9\cdot 2}{21\cdot 2} \\
&= \dfrac{15}{42} + \dfrac{18}{42} \\
&= \dfrac{33}{42} \\
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$f)\;\;$__ $  \dfrac{13}{20} - \dfrac{3}{8} = $ [[  11/40  ]]
@Algebrite.check(11/40)
************
$$
\begin{align*}
\dfrac{13}{20} - \dfrac{3}{8}
&= \dfrac{13\cdot 2}{20\cdot 2} - \dfrac{3\cdot 5}{8\cdot 5} \\
&= \dfrac{26}{40} - \dfrac{15}{40} \\
&= \dfrac{11}{40}
\end{align*}
$$
************
</div>
<div class="flex-child">
<!-- data-solution-button="5"-->
__$g)\;\;$__ $  \dfrac{5}{12} \cdot \dfrac{9}{14} = $ [[  15/56  ]]
@Algebrite.check(15/56)
************
$$
\begin{align*}
\dfrac{5}{12} \cdot \dfrac{9}{14}
&= \dfrac{5 \cdot 9}{12 \cdot 14} \\
&= \dfrac{45}{168} \\
&= \dfrac{15}{56}
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$h)\;\;$__ $  \dfrac{8}{15} : \dfrac{4}{9} = $ [[  6/5  ]]
@Algebrite.check(6/5)
************
$$
\begin{align*}
\dfrac{8}{15} : \dfrac{4}{9}
&= \dfrac{8}{15} \cdot \dfrac{9}{4} \\
&= \dfrac{72}{60} \\
&= \dfrac{6}{5}
\end{align*}
$$
************
</div>


<div class="flex-child">
<!-- data-solution-button="5"-->
__$i)\;\;$__ $  \dfrac{11}{18} - \dfrac{5}{12} = $ [[  7/36  ]]
@Algebrite.check(7/36)
************
$$
\begin{align*}
\dfrac{11}{18} - \dfrac{5}{12}
&= \dfrac{11\cdot 2}{18\cdot 2} - \dfrac{5\cdot 3}{12\cdot 3} \\
&= \dfrac{22}{36} - \dfrac{15}{36} \\
&= \dfrac{7}{36}
\end{align*}
$$
************
</div>


</section>





### Aufgabe 2





**Berechne** den Wert des Terms.



<section class="flex-container">

<div class="flex-child">
<!-- data-solution-button="5"-->
__$a)\;\;$__ $ \left(\dfrac{1}{3} + \dfrac{1}{6}\right) \cdot \dfrac{3}{4} = $ [[  3/8  ]]
@Algebrite.check(3/8)
************
$$
\begin{align*}
\left(\dfrac{1}{3} + \dfrac{1}{6}\right) \cdot \dfrac{3}{4}
&= \left(\dfrac{1\cdot 2}{3\cdot 2} + \dfrac{1}{6}\right) \cdot \dfrac{3}{4} \\
&= \left(\dfrac{2}{6} + \dfrac{1}{6}\right) \cdot \dfrac{3}{4} \\
&= \dfrac{3}{6} \cdot \dfrac{3}{4} \\
&= \dfrac{1}{2} \cdot \dfrac{3}{4} \\
&= \dfrac{3}{8}
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$b)\;\;$__ $ \left(\dfrac{5}{8} - \dfrac{1}{4}\right) : \dfrac{5}{6} = $ [[  9/20  ]]
@Algebrite.check(9/20)
************
$$
\begin{align*}
\left(\dfrac{5}{8} - \dfrac{1}{4}\right) : \dfrac{5}{6}
&= \left(\dfrac{5}{8} - \dfrac{1\cdot 2}{4\cdot 2}\right) : \dfrac{5}{6} \\
&= \left(\dfrac{5}{8} - \dfrac{2}{8}\right) : \dfrac{5}{6} \\
&= \dfrac{3}{8} : \dfrac{5}{6} \\
&= \dfrac{3}{8} \cdot \dfrac{6}{5} \\
&= \dfrac{18}{40} \\
&= \dfrac{9}{20}
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$c)\;\;$__ $ \dfrac{3}{5} : \left(\dfrac{1}{2} + \dfrac{1}{10}\right) = $ [[  1  ]]
@Algebrite.check(1)
************
$$
\begin{align*}
\dfrac{3}{5} : \left(\dfrac{1}{2} + \dfrac{1}{10}\right)
&= \dfrac{3}{5} : \left(\dfrac{1\cdot 5}{2\cdot 5} + \dfrac{1}{10}\right) \\
&= \dfrac{3}{5} : \left(\dfrac{5}{10} + \dfrac{1}{10}\right) \\
&= \dfrac{3}{5} : \dfrac{6}{10} \\
&= \dfrac{3}{5} : \dfrac{3}{5} \\
&= \dfrac{3}{5} \cdot \dfrac{5}{3} \\
&= 1
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$d)\;\;$__ $ \dfrac{5}{6} \cdot \left(\dfrac{3}{7} + \dfrac{1}{14}\right) = $ [[  5/12  ]]
@Algebrite.check(5/12)
************
$$
\begin{align*}
\dfrac{5}{6} \cdot \left(\dfrac{3}{7} + \dfrac{1}{14}\right)
&= \dfrac{5}{6} \cdot \left(\dfrac{3\cdot 2}{7\cdot 2} + \dfrac{1}{14}\right) \\
&= \dfrac{5}{6} \cdot \left(\dfrac{6}{14} + \dfrac{1}{14}\right) \\
&= \dfrac{5}{6} \cdot \dfrac{7}{14} \\
&= \dfrac{5}{6} \cdot \dfrac{1}{2} \\
&= \dfrac{5}{12}
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$e)\;\;$__ $ \dfrac{4}{9} : \left(\dfrac{1}{6} + \dfrac{1}{9}\right) = $ [[  8/5  ]]
@Algebrite.check(8/5)
************
$$
\begin{align*}
\dfrac{4}{9} : \left(\dfrac{1}{6} + \dfrac{1}{9}\right)
&= \dfrac{4}{9} : \left(\dfrac{1\cdot 3}{6\cdot 3} + \dfrac{1\cdot 2}{9\cdot 2}\right) \\
&= \dfrac{4}{9} : \left(\dfrac{3}{18} + \dfrac{2}{18}\right) \\
&= \dfrac{4}{9} : \dfrac{5}{18} \\
&= \dfrac{4}{9} \cdot \dfrac{18}{5} \\
&= \dfrac{4\cdot 2}{5} \quad (\text{da } \dfrac{18}{9}=2) \\
&= \dfrac{8}{5}
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$f)\;\;$__ $ \left(\dfrac{2}{3} - \dfrac{1}{6}\right) \cdot \dfrac{3}{5} = $ [[  3/10  ]]
@Algebrite.check(3/10)
************
$$
\begin{align*}
\left(\dfrac{2}{3} - \dfrac{1}{6}\right) \cdot \dfrac{3}{5}
&= \left(\dfrac{2\cdot 2}{3\cdot 2} - \dfrac{1}{6}\right) \cdot \dfrac{3}{5} \\
&= \left(\dfrac{4}{6} - \dfrac{1}{6}\right) \cdot \dfrac{3}{5} \\
&= \dfrac{3}{6} \cdot \dfrac{3}{5} \\
&= \dfrac{1}{2} \cdot \dfrac{3}{5} \\
&= \dfrac{3}{10}
\end{align*}
$$
************
</div>

</section>






### Aufgabe 3


**Gib** den dargestellten Bruch **an**. (Es ist der jeweilige graue Anteil gefragt.)



<section class="flex-container">

<div class="flex-child">

__$a)\;\;$__


<center>

<!-- style="width:150px" -->
![](https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/Repetitorium/Kap2/bruchb1.png)

</center>

<!-- data-solution-button="5"-->
[[  10/32  ]]
@Algebrite.check(10/32)

</div>

<div class="flex-child">

__$b)\;\;$__

<center>

<!-- style="width:150px" -->
![](https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/Repetitorium/Kap2/bruchb2.png)

</center>

<!-- data-solution-button="5"-->
[[  3/8  ]]
@Algebrite.check(3/8)

</div>

<div class="flex-child">

__$c)\;\;$__

<center>

<!-- style="width:150px" -->
![](https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/Repetitorium/Kap2/bruchb3.png)

</center>

<!-- data-solution-button="5"-->
[[  14/32  ]]
@Algebrite.check(14/32)

</div>

<div class="flex-child">

__$d)\;\;$__

<center>

<!-- style="width:150px" -->
![](https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/Repetitorium/Kap2/bruchb4.png)

</center>

<!-- data-solution-button="5"-->
[[  8/19  ]]
@Algebrite.check(8/19)

</div>

<div class="flex-child">

__$e)\;\;$__

<center>

<!-- style="width:150px" -->
![](https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/Repetitorium/Kap2/bruchb5.png)

</center>

<!-- data-solution-button="5"-->
[[  4/12  ]]
@Algebrite.check(4/12)

</div>

<div class="flex-child">

__$f)\;\;$__

<center>

<!-- style="width:150px" -->
![](https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/Repetitorium/Kap2/bruchb6.png)

</center>

<!-- data-solution-button="5"-->
[[  5/12  ]]
@Algebrite.check(5/12)

</div>

</section>







### Aufgabe 4


**Gib** den beschriebenen Anteilswert **an**.



<section class="flex-container">
<div class="flex-child">


__$a)\;\;$__ Wie viel sind $\dfrac{9}{4}$ von $72\,$kg?  \
 [[  162  ]]kg
***************
$$
\begin{align*}
  \dfrac{9}{4} \cdot 72\,\text{kg} & = \dfrac{9 \cdot 72}{4} \,\text{kg} \\
  & = 9 \cdot 18 \,\text{kg} 
  & = 162 \,\text{kg} 
\end{align*}
$$
***************

</div>
<div class="flex-child">


__$b)\;\;$__ Wie viel sind $\dfrac{7}{10}$ von $120\,$kg?  \
 [[  84  ]]kg
***************
$$
\begin{align*}
  \dfrac{7}{10} \cdot 120\,\text{kg} & = \dfrac{7 \cdot 12}{10} \,\text{kg} \\
  & = 7 \cdot 12 \,\text{kg} 
  & = 84 \,\text{kg} 
\end{align*}
$$
***************

</div>
<div class="flex-child">


__$c)\;\;$__ Wie viel sind $\dfrac{1}{8}$ von $480\,$m?  \
 [[  60  ]]m
***************
$$
\begin{align*}
  \dfrac{1}{8} \cdot 480\,\text{m} & = \dfrac{480}{8} \,\text{m} \\
  & = 480 : 8 \,\text{m} 
  & = 60 \,\text{m} 
\end{align*}
$$
***************

</div>
<div class="flex-child">


__$d)\;\;$__ Wie viel sind $\dfrac{3}{20}$ von $500\,$€?  \
 [[  75  ]]€
***************
$$
\begin{align*}
  \dfrac{3}{20} \cdot 500\,\text{€} & = \dfrac{3 \cdot 500}{20} \,\text{€} \\
  & = \dfrac{3 \cdot 50}{2} \,\text{€} 
  & = 3 \cdot 25 \,\text{€} 
  & = 75 \,\text{€} 
\end{align*}
$$
***************

</div>

<div class="flex-child">

<!-- data-solution-button="5"-->
__$e)\;\;$__ Wie viel sind $\dfrac{5}{6}$ von $\dfrac{7}{8}$ von $64\,$m?  \
[[  140/3  ]]m
@Algebrite.check(140/3)
************
$$
\begin{align*}
\dfrac{5}{6}\cdot\dfrac{7}{8}\cdot 64\,\text{m}
&= \dfrac{5\cdot 7\cdot 64}{6\cdot 8}\,\text{m}
= \dfrac{2240}{48}\,\text{m}
= \dfrac{140}{3}\,\text{m}
\end{align*}
$$
************
</div>

<div class="flex-child">

<!-- data-solution-button="5"-->
__$f)\;\;$__ Wie viel sind $\dfrac{7}{5}$ von $\dfrac{3}{8}$ von $50\,$€?  \
[[  105/4  ]]€
@Algebrite.check(105/4)
************
$$
\begin{align*}
\dfrac{7}{5}\cdot\dfrac{3}{8}\cdot 50\,\text{€}
&= \dfrac{7\cdot 3\cdot 50\,\text{€}}{5\cdot 8}
= \dfrac{1050}{40}\,\text{€}
= \dfrac{105}{4}\,\text{€}
\end{align*}
$$
************
</div>

</section>






### Aufgabe 5



__$a)\;\;$__ Berechne den Flächeninhalt eines Rechtecks mit den Maßen $a=\dfrac{48}{27}\,$cm und $a=\dfrac{15}{8}\,$cm. \
$A=$[[  10/3  ]]cm$^2$
@Algebrite.check(10/3)
************
$$
\begin{align*}
A &= a \cdot b \\
  &= \dfrac{48}{27}\,\text{cm} \cdot \dfrac{15}{8}\,\text{cm} \\
  &= \dfrac{48 \cdot 15}{27 \cdot 8}\,\text{cm}^2 \\
  &= \dfrac{720}{216}\,\text{cm}^2 \\
  &= \dfrac{10}{3}\,\text{cm}^2 \\
  &\approx 3{,}33\,\text{cm}^2
\end{align*}
$$
************


__$b)\;\;$__ Berechne den Umfang eines Rechtecks mit den Maßen $a=\dfrac{5}{7}\,$cm und $a=\dfrac{9}{8}\,$cm. \
$u=$[[  103/28  ]]cm
@Algebrite.check(103/28)
************
$$
\begin{align*}
u &= 2(a + b) \\
  &= 2\left(\dfrac{5}{7}\,\text{cm} + \dfrac{9}{8}\,\text{cm}\right) \\
  &= 2\left(\dfrac{40}{56} + \dfrac{63}{56}\right)\text{cm} \\
  &= 2 \cdot \dfrac{103}{56}\,\text{cm} \\
  &= \dfrac{206}{56}\,\text{cm} \\
  &= \dfrac{103}{28}\,\text{cm} \\
  &\approx 3{,}68\,\text{cm}
\end{align*}
$$
************







### Aufgabe 6



__$a)\;\;$__ Berechne den Oberflächeninhalt eines Quaders mit den Maßen $a=\dfrac{3}{4}\,$cm, $b=\dfrac{5}{3}\,$cm und $c=\dfrac{5}{6}\,$cm. \
$O=$[[  235/36  ]]cm$^2$
@Algebrite.check(235/36)
************
$$
\begin{align*}
O &= 2\,(ab + ac + bc) \\[4pt]
  &= 2\left(\dfrac{3}{4}\text{cm} \cdot\dfrac{5}{3}\text{cm}  + \dfrac{3}{4}\text{cm} \cdot\dfrac{5}{6}\text{cm}  + \dfrac{5}{3}\text{cm} \cdot\dfrac{5}{6}\text{cm} right)\\[4pt]
  &= 2\left(\dfrac{15}{12}\text{cm}^2 + \dfrac{15}{24}\text{cm}^2 + \dfrac{25}{18}\text{cm}^2\right) \\[4pt]
  &= 2\left(\dfrac{5}{4} + \dfrac{5}{8} + \dfrac{25}{18}\right)\text{cm}^2 \\[4pt]
  &= 2\left(\dfrac{90}{72} + \dfrac{45}{72} + \dfrac{100}{72}\right)\text{cm}^2 \\[4pt]
  &= 2\cdot\dfrac{235}{72}\text{cm}^2 \\[4pt]
  &= \dfrac{470}{72}\text{cm}^2 \\[4pt]
  &= \dfrac{235}{36}\text{cm}^2
\end{align*}
$$
************


__$b)\;\;$__ Berechne das Volumen eines Quaders mit den Maßen $a=\dfrac{11}{18}\,$cm, $b=\dfrac{5}{28}\,$cm und $c=\dfrac{21}{55}\,$cm. \
$V=$[[  1/24  ]]cm$^3$
@Algebrite.check(1/24)
************
$$
\begin{align*}
V &= a \cdot b \cdot c \\[4pt]
  &= \dfrac{11}{18}\,\text{cm} \cdot \dfrac{5}{28}\,\text{cm}
     \cdot \dfrac{21}{55}\,\text{cm} \\[4pt]
  &= \dfrac{11 \cdot 5 \cdot 21}{18 \cdot 28 \cdot 55}\,\text{cm}^3 \\[6pt]
\text{Kürzen:} \quad
  &\dfrac{11}{55} = \dfrac{1}{5}, \quad
    \dfrac{21}{28} = \dfrac{3}{4} \\[4pt]
V &= \dfrac{1 \cdot 5 \cdot 3}{18 \cdot 4 \cdot 5}\,\text{cm}^3 \\[4pt]
  &= \dfrac{15}{360}\,\text{cm}^3
   = \dfrac{1}{24}\,\text{cm}^3
\end{align*}
$$
************




### Aufgabe 7



__$a)\;\;$__ Ein Budget umfasst $50$ €. Davon werden $\dfrac{3}{5}$ verplant.  
**Bestimme** den verbleibenden Betrag.  

<!-- data-solution-button="5"-->
[[  20  ]] €
************
$$
50\,\text{€} - \dfrac{3}{5}\cdot 50\,\text{€}
= 50\,\text{€} - \dfrac{3}{5}\cdot \dfrac{50}{1}\,\text{€}
= 50\,\text{€} - \dfrac{150}{5}\,\text{€}
= 50\,\text{€} - 30\,\text{€}
= 20\,\text{€}
$$
************



__$b)\;\;$__ Eine Übung dauert $80$ Minuten. Die Aufwärmphase umfasst $\dfrac{3}{8}$ der Gesamtzeit.  
**Berechne** die Dauer der Aufwärmphase. 

<!-- data-solution-button="5"-->
[[  30  ]] min
************
$$
\dfrac{3}{8}\cdot 80\,\text{min}
= \dfrac{3}{8}\cdot \dfrac{80}{1}\,\text{min}
= \dfrac{240}{8}\,\text{min}
= 30\,\text{min}
$$
************




__$c)\;\;$__ In der Backstube steht ein Mehlsack mit $24\,\text{kg}$.  
Am Vormittag werden für Teiglinge $\dfrac{3}{8}$ der Gesamtmasse verbraucht.  
Am Nachmittag wird für eine zweite Charge die Hälfte der verbleibenden Masse genutzt.  
**Berechne** die am Ende noch vorhandene Mehlmenge als Bruch. 

<!-- data-solution-button="5"-->
[[  15/2  ]] kg
@Algebrite.check(15/2)
************
$$
\begin{align*}
\text{Vormittag:}\quad & \dfrac{3}{8}\cdot 24\,\text{kg}
= \dfrac{72}{8}\,\text{kg}
= 9\,\text{kg} \\[4pt]
\text{Rest 1:}\quad & 24\,\text{kg} - 9\,\text{kg} = 15\,\text{kg} \\[4pt]
\text{Nachmittag:}\quad & \dfrac{1}{2}\cdot 15\,\text{kg}
= \dfrac{15}{2}\,\text{kg} \\[4pt]
\text{Rest ges.:}\quad & 15\,\text{kg} - \dfrac{15}{2}\,\text{kg}
= \dfrac{30}{2}\,\text{kg} - \dfrac{15}{2}\,\text{kg}
= \dfrac{15}{2}\,\text{kg}
\end{align*}
$$
************




### Aufgabe 8



**Stelle** die passende Teilung der Fläche **ein** und **markiere** den passenden Anteil, sodass der Bruch dargestellt wird.




<section class="flex-container">

<div class="flex-child">
__$a)\;\;$__ $\dfrac{7}{10}$


@rectQuiz(7/10)



</div>
<div class="flex-child">
__$b)\;\;$__ $\dfrac{11}{15}$


@rectQuiz(11/15)


</div>
<div class="flex-child">
__$c)\;\;$__ $\dfrac{17}{24}$

@rectQuiz(17/24)



</div>
<div class="flex-child">
__$d)\;\;$__ $\dfrac{5}{9}$

@rectQuiz(5/9)



</div>
<div class="flex-child">
__$e)\;\;$__ $\dfrac{19}{28}$


@rectQuiz(19/28)


</div>
<div class="flex-child">
__$f)\;\;$__ $\dfrac{7}{45}$


@rectQuiz(7/45)


</div>

</section>







