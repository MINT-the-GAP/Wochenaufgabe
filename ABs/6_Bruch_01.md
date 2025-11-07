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









import: https://raw.githubusercontent.com/liaTemplates/algebrite/master/README.md
import: https://raw.githubusercontent.com/LiaTemplates/Tikz-Jax/main/README.md
import: https://raw.githubusercontent.com/LiaTemplates/mermaid_template/0.1.4/README.md

script: https://cdn.jsdelivr.net/gh/LiaTemplates/Tikz-Jax@main/dist/index.js


tags: Arbeitsblatt, Bruchrechnung, Mathematik, Klasse 6

comment: Gemischtes Arbeitsblatt für die 6. Klasse zur Bruchrechnung. 

author: Martin Lommatzsch

-->





# Arbeitsblatt zum digitalgestützten Selbstüben 1 - Klasse 6 Bruchrechnung

> Hier findest du Übungsaufgaben zur Berechnung. Damit kannst du bereits gelerntes Wissen wiederholen und den aktuellen Unterrichtsstoff üben. Am besten nimmst du dir ein Blatt Papier und rechnest die Aufgaben Schritt für Schritt durch. Danach trägst du deine Lösungen ein und bekommst eine Musterlösung zum Vergleichen. Wenn du dich ein paar Mal vertan hast, kannst du dir bei manchen Aufgaben auch die komplette Lösung anzeigen lassen. Versuch aber bitte, ohne Taschenrechner oder andere Hilfsmittel zu arbeiten – sonst betrügst du dich nur selbst. Du kannst die Aufgaben auch auf deinem Handy, Tablet oder Laptop öffnen und jederzeit neu starten. Viel Erfolg – und wenn du Fragen oder Ideen hast, melde dich einfach bei mir!

- Martin Lommatzsch



Falls du Probleme mit diesen Aufgaben haben solltest, dann schau dir ruhig nochmal die vollständige Erklärung des gesamten Themas an: [Zur Erklärung](https://liascript.github.io/course/?https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/Repetitorium/01_04_01_Bruchrechnung.md)




## Aufgabe 1: Brüche darstellen



<!--  Bruchrechnung 0171  -->


<img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/1.png" width="30" height="30"> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/sgrad/1.png" width="120" height="30">  \
**Stelle** die passende Teilung der Fläche **ein** und **markiere** den passenden Anteil, sodass der Bruch dargestellt wird.




<section class="flex-container">

<div class="flex-child">
__$a)\;\;$__ $\dfrac{4}{5}$


@circleQuiz(4/5)

</div>
<div class="flex-child">
__$b)\;\;$__ $\dfrac{7}{11}$


@circleQuiz(7/11)

</div>
<div class="flex-child">
__$c)\;\;$__ $\dfrac{13}{15}$


@circleQuiz(13/15)

</div>
<div class="flex-child">
__$d)\;\;$__ $\dfrac{11}{24}$


@circleQuiz(11/24)

</div>
<div class="flex-child">
__$e)\;\;$__ $\dfrac{17}{29}$


@circleQuiz(17/29)

</div>
<div class="flex-child">
__$f)\;\;$__ $\dfrac{7}{32}$


@circleQuiz(7/32)

</div>

</section>





## Aufgabe 2: Brüche addieren oder subtrahieren



<!--  Bruchrechnung 0027  -->


<img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/2.png" width="30" height="30"> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/sgrad/2.png" width="120" height="30">  \
**Berechne** den Wert des Terms.



<section class="flex-container">

<div class="flex-child">
<!-- data-solution-button="5"-->
__$a)\;\;$__ $  \dfrac{3}{10} + \dfrac{1}{5} = $ [[  1/2  ]]
@Algebrite.check(1/2)
************
$$
\begin{align*}
\dfrac{3}{10} + \dfrac{1}{5}
&= \dfrac{3}{10} + \dfrac{1\cdot 2}{5\cdot 2} \\
&= \dfrac{3}{10} + \dfrac{2}{10} \\
&= \dfrac{3+2}{10} \\
&= \dfrac{5}{10} \;=\; \dfrac{1}{2}
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$b)\;\;$__ $  \dfrac{7}{9} - \dfrac{1}{6} = $ [[  11/18  ]]
@Algebrite.check(11/18)
************
$$
\begin{align*}
\dfrac{7}{9} - \dfrac{1}{6}
&= \dfrac{7\cdot 2}{9\cdot 2} - \dfrac{1\cdot 3}{6\cdot 3} \\
&= \dfrac{14}{18} - \dfrac{3}{18} \\
&= \dfrac{14-3}{18} \\
&= \dfrac{11}{18}
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$c)\;\;$__ $  \dfrac{4}{15} + \dfrac{2}{9} = $ [[  22/45  ]]
@Algebrite.check(22/45)
************
$$
\begin{align*}
\dfrac{4}{15} + \dfrac{2}{9}
&= \dfrac{4\cdot 3}{15\cdot 3} + \dfrac{2\cdot 5}{9\cdot 5} \\
&= \dfrac{12}{45} + \dfrac{10}{45} \\
&= \dfrac{12+10}{45} \\
&= \dfrac{22}{45}
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$d)\;\;$__ $  \dfrac{7}{10} - \dfrac{3}{20} = $ [[  11/20  ]]
@Algebrite.check(11/20)
************
$$
\begin{align*}
\dfrac{7}{10} - \dfrac{3}{20}
&= \dfrac{7\cdot 2}{10\cdot 2} - \dfrac{3}{20} \\
&= \dfrac{14}{20} - \dfrac{3}{20} \\
&= \dfrac{14-3}{20} \\
&= \dfrac{11}{20}
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$e)\;\;$__ $  \dfrac{2}{3} + \dfrac{4}{9} = $ [[  10/9  ]]
@Algebrite.check(10/9)
************
$$
\begin{align*}
\dfrac{2}{3} + \dfrac{4}{9}
&= \dfrac{2\cdot 3}{3\cdot 3} + \dfrac{4}{9} \\
&= \dfrac{6}{9} + \dfrac{4}{9} \\
&= \dfrac{6+4}{9} \\
&= \dfrac{10}{9}
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$f)\;\;$__ $  \dfrac{5}{12} - \dfrac{1}{18} = $ [[  13/36  ]]
@Algebrite.check(13/36)
************
$$
\begin{align*}
\dfrac{5}{12} - \dfrac{1}{18}
&= \dfrac{5\cdot 3}{12\cdot 3} - \dfrac{1\cdot 2}{18\cdot 2} \\
&= \dfrac{15}{36} - \dfrac{2}{36} \\
&= \dfrac{15-2}{36} \\
&= \dfrac{13}{36}
\end{align*}
$$
************
</div>

</section>







## Aufgabe 3: Punktrechnung bei Brüchen


<!--  Bruchrechnung 0043  -->


<img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/2.png" width="30" height="30"> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/sgrad/2.png" width="120" height="30">  \
**Berechne** den Wert des Terms.



<section class="flex-container">

<div class="flex-child">
<!-- data-solution-button="5"-->
__$a)\;\;$__ $  \dfrac{2}{3} \cdot \dfrac{5}{7} = $ [[  10/21  ]]
@Algebrite.check(10/21)
************
$$
\begin{align*}
\dfrac{2}{3} \cdot \dfrac{5}{7}
&= \dfrac{2 \cdot 5}{3 \cdot 7} \\
&= \dfrac{10}{21}
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$b)\;\;$__ $  \dfrac{9}{14} : \dfrac{3}{7} = $ [[  3/2  ]]
@Algebrite.check(3/2)
************
$$
\begin{align*}
\dfrac{9}{14} : \dfrac{3}{7}
&= \dfrac{9}{14} \cdot \dfrac{7}{3} \\
&= \dfrac{63}{42} \\
&= \dfrac{3}{2}
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$c)\;\;$__ $  \dfrac{7}{8} \cdot \dfrac{6}{11} = $ [[  21/44  ]]
@Algebrite.check(21/44)
************
$$
\begin{align*}
\dfrac{7}{8} \cdot \dfrac{6}{11}
&= \dfrac{7 \cdot 6}{8 \cdot 11} \\
&= \dfrac{42}{88} \\
&= \dfrac{21}{44}
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$d)\;\;$__ $  \dfrac{10}{21} : \dfrac{5}{14} = $ [[  4/3  ]]
@Algebrite.check(4/3)
************
$$
\begin{align*}
\dfrac{10}{21} : \dfrac{5}{14}
&= \dfrac{10}{21} \cdot \dfrac{14}{5} \\
&= \dfrac{140}{105} \\
&= \dfrac{4}{3}
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$e)\;\;$__ $  \dfrac{3}{10} \cdot \dfrac{7}{9} = $ [[  7/30  ]]
@Algebrite.check(7/30)
************
$$
\begin{align*}
\dfrac{3}{10} \cdot \dfrac{7}{9}
&= \dfrac{3 \cdot 7}{10 \cdot 9} \\
&= \dfrac{21}{90} \\
&= \dfrac{7}{30}
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$f)\;\;$__ $  \dfrac{11}{12} : \dfrac{22}{18} = $ [[  3/4  ]]
@Algebrite.check(3/4)
************
$$
\begin{align*}
\dfrac{11}{12} : \dfrac{22}{18}
&= \dfrac{11}{12} \cdot \dfrac{18}{22} \\
&= \dfrac{198}{264} \\
&= \dfrac{3}{4}
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$g)\;\;$__ $  \dfrac{4}{9} \cdot \dfrac{7}{10} = $ [[  14/45  ]]
@Algebrite.check(14/45)
************
$$
\begin{align*}
\dfrac{4}{9} \cdot \dfrac{7}{10}
&= \dfrac{4 \cdot 7}{9 \cdot 10} \\
&= \dfrac{28}{90} \\
&= \dfrac{14}{45}
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$h)\;\;$__ $  \dfrac{6}{11} : \dfrac{3}{22} = $ [[  4  ]]
@Algebrite.check(4)
************
$$
\begin{align*}
\dfrac{6}{11} : \dfrac{3}{22}
&= \dfrac{6}{11} \cdot \dfrac{22}{3} \\
&= \dfrac{132}{33} \\
&= 4
\end{align*}
$$
************
</div>

</section>







## Aufgabe 4: Vorrangsregeln mit Brüchen


<!--  Bruchrechnung 0050  -->


<img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/3.png" width="30" height="30"> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/sgrad/3.png" width="120" height="30">  \
**Berechne** den Wert des Terms.



<section class="flex-container">

<div class="flex-child">
<!-- data-solution-button="5"-->
__$a)\;\;$__ $  \dfrac{2}{5} \cdot \dfrac{3}{4} + \dfrac{1}{2} = $ [[  4/5  ]]
@Algebrite.check(4/5)
************
$$
\begin{align*}
\dfrac{2}{5} \cdot \dfrac{3}{4} + \dfrac{1}{2}
&= \dfrac{6}{20} + \dfrac{1}{2} \\
&= \dfrac{6}{20} + \dfrac{10}{20} \\
&= \dfrac{16}{20} \\
&= \dfrac{4}{5}
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$b)\;\;$__ $  \dfrac{7}{8} - \dfrac{1}{2} \cdot \dfrac{3}{4} = $ [[  1/2  ]]
@Algebrite.check(1/2)
************
$$
\begin{align*}
\dfrac{7}{8} - \dfrac{1}{2} \cdot \dfrac{3}{4}
&= \dfrac{7}{8} - \dfrac{3}{8} \\
&= \dfrac{4}{8} \\
&= \dfrac{1}{2}
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$c)\;\;$__ $  \dfrac{5}{6} + \dfrac{2}{3} : \dfrac{4}{9} = $ [[  7/3  ]]
@Algebrite.check(7/3)
************
$$
\begin{align*}
\dfrac{5}{6} + \dfrac{2}{3} : \dfrac{4}{9}
&= \dfrac{5}{6} + \dfrac{2}{3} \cdot \dfrac{9}{4} \\
&= \dfrac{5}{6} + \dfrac{18}{12} \\
&= \dfrac{5}{6} + \dfrac{3}{2} \\
&= \dfrac{5}{6} + \dfrac{9}{6} \\
&= \dfrac{14}{6} = \dfrac{7}{3}
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$d)\;\;$__ $  \dfrac{3}{10} : \dfrac{3}{5} - \dfrac{1}{4} = $ [[  1/4  ]]
@Algebrite.check(1/4)
************
$$
\begin{align*}
\dfrac{3}{10} : \dfrac{3}{5} - \dfrac{1}{4}
&= \dfrac{3}{10} \cdot \dfrac{5}{3} - \dfrac{1}{4} \\
&= \dfrac{15}{30} - \dfrac{1}{4} \\
&= \dfrac{1}{2} - \dfrac{1}{4} \\
&= \dfrac{1}{4}
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$e)\;\;$__ $  \dfrac{4}{7} + \dfrac{2}{3} \cdot \dfrac{3}{8} = $ [[  23/28  ]]
@Algebrite.check(23/28)
************
$$
\begin{align*}
\dfrac{4}{7} + \dfrac{2}{3} \cdot \dfrac{3}{8}
&= \dfrac{4}{7} + \dfrac{6}{24} \\
&= \dfrac{4}{7} + \dfrac{1}{4} \\
&= \dfrac{16}{28} + \dfrac{7}{28} \\
&= \dfrac{23}{28}
\end{align*}
$$
************
</div>

<div class="flex-child">
<!-- data-solution-button="5"-->
__$f)\;\;$__ $  \dfrac{9}{10} - \dfrac{2}{5} : \dfrac{3}{4} = $ [[  11/30  ]]
@Algebrite.check(11/30)
************
$$
\begin{align*}
\dfrac{9}{10} - \dfrac{2}{5} : \dfrac{3}{4}
&= \dfrac{9}{10} - \dfrac{2}{5} \cdot \dfrac{4}{3} \\
&= \dfrac{9}{10} - \dfrac{8}{15} \\
&= \dfrac{27}{30} - \dfrac{16}{30} \\
&= \dfrac{11}{30}
\end{align*}
$$
************
</div>

</section>





## Aufgabe 5: Der Bruch in der Mitte



<img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/3.png" width="30" height="30"> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/sgrad/2.png" width="120" height="30">  \
**Bestimme** den Wert zwischen den gegeneben beiden Brüchen, der exakt in der Mitte liegt.



<section class="flex-container">

<div class="flex-child">

<!-- data-solution-button="5"-->
__$a)\;\;$__ $  \dfrac{1}{3} \;\;\wedge\;\; \dfrac{3}{5}  \;\;\Rightarrow\;\; $ [[  7/15  ]] 
@Algebrite.check(7/15)
************
$$
\begin{align*}
\left(\dfrac{1}{3} + \dfrac{3}{5}\right) : 2
&= \left(\dfrac{5}{15} + \dfrac{9}{15}\right) : 2 \\
&= \dfrac{14}{15} : 2 \\
&= \dfrac{14}{30} \;=\; \dfrac{7}{15}
\end{align*}
$$
************
</div>

<div class="flex-child">

<!-- data-solution-button="5"-->
__$b)\;\;$__ $  \dfrac{2}{7} \;\;\wedge\;\; \dfrac{5}{6}  \;\;\Rightarrow\;\; $ [[  47/84  ]] 
@Algebrite.check(47/84)
************
$$
\begin{align*}
\left(\dfrac{2}{7} + \dfrac{5}{6}\right) : 2
&= \left(\dfrac{12}{42} + \dfrac{35}{42}\right) : 2 \\
&= \dfrac{47}{42} : 2 \\
&= \dfrac{47}{84}
\end{align*}
$$
************
</div>

<div class="flex-child">

<!-- data-solution-button="5"-->
__$c)\;\;$__ $  \dfrac{4}{9} \;\;\wedge\;\; \dfrac{2}{3}  \;\;\Rightarrow\;\; $ [[  5/9  ]] 
@Algebrite.check(5/9)
************
$$
\begin{align*}
\left(\dfrac{4}{9} + \dfrac{2}{3}\right) : 2
&= \left(\dfrac{4}{9} + \dfrac{6}{9}\right) : 2 \\
&= \dfrac{10}{9} : 2 \\
&= \dfrac{10}{18} \;=\; \dfrac{5}{9}
\end{align*}
$$
************
</div>

<div class="flex-child">

<!-- data-solution-button="5"-->
__$d)\;\;$__ $  \dfrac{5}{8} \;\;\wedge\;\; \dfrac{1}{12}  \;\;\Rightarrow\;\; $ [[  17/48  ]] 
@Algebrite.check(17/48)
************
$$
\begin{align*}
\left(\dfrac{5}{8} + \dfrac{1}{12}\right) : 2
&= \left(\dfrac{15}{24} + \dfrac{2}{24}\right) : 2 \\
&= \dfrac{17}{24} : 2 \\
&= \dfrac{17}{48}
\end{align*}
$$
************
</div>

<div class="flex-child">

<!-- data-solution-button="5"-->
__$e)\;\;$__ $  \dfrac{3}{10} \;\;\wedge\;\; \dfrac{7}{12}  \;\;\Rightarrow\;\; $ [[  53/120  ]] 
@Algebrite.check(53/120)
************
$$
\begin{align*}
\left(\dfrac{3}{10} + \dfrac{7}{12}\right) : 2
&= \left(\dfrac{18}{60} + \dfrac{35}{60}\right) : 2 \\
&= \dfrac{53}{60} : 2 \\
&= \dfrac{53}{120}
\end{align*}
$$
************
</div>

<div class="flex-child">

<!-- data-solution-button="5"-->
__$f)\;\;$__ $  \dfrac{11}{20} \;\;\wedge\;\; \dfrac{3}{4}  \;\;\Rightarrow\;\; $ [[  13/20  ]] 
@Algebrite.check(13/20)
************
$$
\begin{align*}
\left(\dfrac{11}{20} + \dfrac{3}{4}\right) : 2
&= \left(\dfrac{11}{20} + \dfrac{15}{20}\right) : 2 \\
&= \dfrac{26}{20} : 2 \\
&= \dfrac{13}{10} : 2
= \dfrac{13}{20}
\end{align*}
$$
************
</div>

</section>









## Aufgabe 6: Bruchanteile




<!--  Bruchrechnung 0077  -->


<img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/1.png" width="30" height="30"> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/sgrad/1.png" width="120" height="30">  \
**Gib** den beschriebenen Anteilswert **an**.



<section class="flex-container">
<div class="flex-child">

__$a)\;\;$__ Wie viel sind $\dfrac{4}{5}$ von $2500\,$kg?  

<!-- data-solution-button="5"-->
[[  2000  ]]kg

</div>
<div class="flex-child">

__$b)\;\;$__ Wie viel sind $\dfrac{5}{9}$ von $180\,$cm?  

<!-- data-solution-button="5"-->
[[  100  ]]cm

</div>
<div class="flex-child">

__$c)\;\;$__ Wie viel sind $\dfrac{1}{4}$ von $300\,$min?  

<!-- data-solution-button="5"-->
[[  75  ]]min

</div>
<div class="flex-child">

__$d)\;\;$__ Wie viel sind $\dfrac{6}{7}$ von $42\,$m?  

<!-- data-solution-button="5"-->
[[  36  ]]m

</div>
</section>





## Aufgabe 7: Brüche sortieren




<!--  Bruchrechnung 0162  -->

<img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/3.png" width="30" height="30"> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/sgrad/5.png" width="120" height="30">  \
**Sortiere** die Brüche nach ihrer Größe.



<!-- data-solution-button="5" 
data-randomize="true" -->
__$a)\;\;$__
[->[($\dfrac{3}{7}$)]] $<$ 
[->[($\dfrac{3}{5}$)]] $<$ 
[->[($\dfrac{7}{8}$)]] $<$ 
[->[($\dfrac{3}{2}$)]] $<$ 
[->[($\dfrac{5}{3}$)]] $<$ 
[->[($\dfrac{7}{4}$)]]



<!-- data-solution-button="5" 
data-randomize="true" -->
__$b)\;\;$__
[->[($\dfrac{2}{11}$)]] $<$ 
[->[($\dfrac{1}{3}$)]] $<$ 
[->[($\dfrac{5}{12}$)]] $<$ 
[->[($\dfrac{5}{8}$)]] $<$ 
[->[($\dfrac{7}{10}$)]] $<$ 
[->[($\dfrac{8}{9}$)]]



<!-- data-solution-button="5" 
data-randomize="true" -->
__$c)\;\;$__
[->[($\dfrac{2}{5}$)]] $<$ 
[->[($\dfrac{7}{12}$)]] $<$ 
[->[($\dfrac{2}{3}$)]] $<$ 
[->[($\dfrac{7}{9}$)]] $<$ 
[->[($\dfrac{7}{6}$)]] $<$ 
[->[($\dfrac{8}{7}$)]]




## Aufgabe 8: Dominos mit Brüchen


<!--  Bruchrechnung 0165  -->

<img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/3.png" width="30" height="30"> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/sgrad/2.png" width="120" height="30">  \
**Ordne** die Dominosteine in der richtigen Reihenfolge **an**.

<!-- data-randomize="true"  
data-solution-button="5"  -->
__$a)\;\;$__ $\dfrac{5}{6}$ 
 [->[$\left. \boxed{ = \dfrac{2}{3} + \dfrac{1}{6}} \right\| \boxed{ \dfrac{4}{5} \cdot \dfrac{3}{2}}  $]]
 [->[$\left. \boxed{ =  \dfrac{3}{4} - \dfrac{3}{20} } \right\|\boxed{ \dfrac{9}{7} : \dfrac{3}{4}  }  $]]
 [->[$\left. \boxed{ =  \dfrac{36}{56} \cdot \dfrac{8}{3} } \right\|\boxed{ \dfrac{5}{8} + \dfrac{1}{2} }  $]]
 [->[$\left. \boxed{ =  \dfrac{3}{4} \cdot \dfrac{3}{2} } \right\|\boxed{ \dfrac{7}{10} - \dfrac{1}{2} }  $]]
$= \dfrac{1}{5}$


<!-- data-randomize="true"  
data-solution-button="5"  -->
__$b)\;\;$__ $\dfrac{1}{5}$ 
 [->[$\left. \boxed{ =  \dfrac{8}{15} : \dfrac{8}{3} } \right\|\boxed{ \dfrac{8}{9} \cdot \dfrac{15}{24} }  $]]
 [->[$\left. \boxed{ =  \dfrac{2}{3} - \dfrac{1}{9} } \right\|\boxed{ \dfrac{5}{12} + \dfrac{3}{4} }  $]]
 [->[$\left. \boxed{ =  \dfrac{11}{6} - \dfrac{2}{3} } \right\|\boxed{ \dfrac{7}{8} \cdot \dfrac{6}{21} }  $]]
 [->[$\left. \boxed{ =  \dfrac{7}{12} - \dfrac{1}{4} } \right\|\boxed{ \dfrac{6}{5} - \dfrac{3}{4} }  $]]  
$= \dfrac{9}{20}$

<!-- data-randomize="true"  
data-solution-button="5"  -->
__$c)\;\;$__ $\dfrac{5}{6}$ 
 [->[$\left. \boxed{ = \dfrac{2}{3} + \dfrac{1}{6}} \right\| \boxed{ \dfrac{4}{5} \cdot \dfrac{3}{2}}  $]]
 [->[$\left. \boxed{ =  \dfrac{3}{4} + \dfrac{9}{20} } \right\|\boxed{ \dfrac{9}{7} : \dfrac{3}{4}  }  $]]
 [->[$\left. \boxed{ =  \dfrac{36}{56} \cdot \dfrac{8}{3} } \right\|\boxed{ \dfrac{5}{8} + \dfrac{1}{2} }  $]]
 [->[$\left. \boxed{ =  \dfrac{3}{4} \cdot \dfrac{3}{2} } \right\|\boxed{ \dfrac{7}{10} - \dfrac{1}{2} }  $]]
$= \dfrac{1}{5}$


<!-- data-randomize="true"  
data-solution-button="5"  -->
__$d)\;\;$__ $\dfrac{7}{12}$
 [->[$\left. \boxed{ = \dfrac{1}{3} + \dfrac{1}{4}} \right\| \boxed{ \dfrac{14}{15} \cdot \dfrac{5}{14}} $]]
 [->[$\left. \boxed{ = \dfrac{5}{6} - \dfrac{1}{2}} \right\| \boxed{ \dfrac{2}{5} + \dfrac{1}{15}} $]]
 [->[$\left. \boxed{ = \dfrac{7}{5} \cdot \dfrac{1}{3}} \right\| \boxed{ \dfrac{11}{12} - \dfrac{1}{4}} $]]
 [->[$\left. \boxed{ = \dfrac{4}{9} : \dfrac{2}{3}} \right\| \boxed{ \dfrac{5}{6} - \dfrac{1}{3}} $]]
$= \dfrac{1}{2}$



<!-- data-randomize="true"  
data-solution-button="5"  -->
__$e)\;\;$__ $\dfrac{3}{4}$
 [->[$\left. \boxed{ = \dfrac{1}{2} + \dfrac{1}{4}} \right\| \boxed{ \dfrac{9}{8} : \dfrac{5}{4}} $]]
 [->[$\left. \boxed{ = \dfrac{3}{2} - \dfrac{3}{5}} \right\| \boxed{ \dfrac{3}{4} \cdot \dfrac{8}{9}} $]]
 [->[$\left. \boxed{ = \dfrac{5}{6} - \dfrac{1}{6}} \right\| \boxed{ \dfrac{7}{8} - \dfrac{1}{4}} $]]
 [->[$\left. \boxed{ = \dfrac{5}{4} : \dfrac{2}{1}} \right\| \boxed{ \dfrac{1}{3} + \dfrac{5}{12}} $]]
$= \dfrac{3}{4}$




<!-- data-randomize="true"  
data-solution-button="5"  -->
__$f)\;\;$__ $\dfrac{4}{7}$
 [->[$\left. \boxed{ = \dfrac{6}{7} - \dfrac{2}{7}} \right\| \boxed{ \dfrac{5}{6} \cdot \dfrac{3}{5}} $]]
 [->[$\left. \boxed{ = \dfrac{3}{4} : \dfrac{3}{2}} \right\| \boxed{ \dfrac{9}{10} : \dfrac{3}{1}} $]]
 [->[$\left. \boxed{ = \dfrac{1}{2} - \dfrac{1}{5}} \right\| \boxed{ \dfrac{7}{12} + \dfrac{1}{6}} $]]
 [->[$\left. \boxed{ = \dfrac{3}{2} : \dfrac{2}{1}} \right\| \boxed{ \dfrac{15}{28} - \dfrac{5}{28}} $]]
$= \dfrac{5}{14}$













