<!--

version:  0.0.1
language: de
author: Martin Lommatzsch

@style
main > *:not(:last-child) {
  margin-bottom: 3rem;
}



/* Quiz/Check NICHT über volle Breite ziehen (nur dort, wo class="check-only" gesetzt ist) */
.check-only {
  display: inline-block !important;
  width: auto !important;
  max-width: max-content !important;
  text-align: left !important;
}

/* sehr defensiv: typische LiaScript-Wrapper ebenfalls auf "shrink" */
.check-only .lia-quiz,
.check-only .lia-input,
.check-only .lia-solution,
.check-only .lia-quiz__controls,
.check-only .lia-quiz__solution {
  display: inline-block !important;
  width: auto !important;
  max-width: max-content !important;
  float: none !important;
  text-align: left !important;
}

/* In diesem Check-Block ALLE Eingabeelemente ausblenden, nur Button bleibt */
.check-only input,
.check-only textarea,
.check-only select {
  display: none !important;
  visibility: hidden !important;
  width: 0 !important;
  height: 0 !important;
  padding: 0 !important;
  margin: 0 !important;
  border: 0 !important;
}


.check-only button {
  float: none !important;
  margin-left: 0 !important;
}


/* =========================================================
   JSXGraph Navigation: Light = schwarz, Dark = weiß
   ========================================================= */

/* Basis: Navigation übernimmt eine definierte Farbe */
.jxgbox .JXG_navigation,
.JXG_navigation{
  background: transparent !important;
}

/* LIGHTMODE */
@media (prefers-color-scheme: light){
  .jxgbox .JXG_navigation,
  .JXG_navigation{
    color: #000 !important;
  }

  .jxgbox .JXG_navigation a,
  .jxgbox .JXG_navigation span,
  .jxgbox .JXG_navigation button,
  .JXG_navigation a,
  .JXG_navigation span,
  .JXG_navigation button{
    color: #000 !important;
    border-color: #000 !important;
    background: transparent !important;
  }

  /* SVG-Icons */
  .jxgbox .JXG_navigation svg,
  .jxgbox .JXG_navigation svg *,
  .JXG_navigation svg,
  .JXG_navigation svg *{
    fill: #000 !important;
    stroke: #000 !important;
  }

  /* IMG-Icons (falls verwendet) */
  .jxgbox .JXG_navigation img,
  .JXG_navigation img{
    filter: none !important;
  }
}

/* DARKMODE */
@media (prefers-color-scheme: dark){
  .jxgbox .JXG_navigation,
  .JXG_navigation{
    color: #fff !important;
  }

  .jxgbox .JXG_navigation a,
  .jxgbox .JXG_navigation span,
  .jxgbox .JXG_navigation button,
  .JXG_navigation a,
  .JXG_navigation span,
  .JXG_navigation button{
    color: #fff !important;
    border-color: #fff !important;
    background: transparent !important;
  }

  /* SVG-Icons */
  .jxgbox .JXG_navigation svg,
  .jxgbox .JXG_navigation svg *,
  .JXG_navigation svg,
  .JXG_navigation svg *{
    fill: #fff !important;
    stroke: #fff !important;
  }

  /* IMG-Icons (falls verwendet) */
  .jxgbox .JXG_navigation img,
  .JXG_navigation img{
    filter: invert(1) !important;
  }
}


@end

import: https://raw.githubusercontent.com/liaTemplates/algebrite/master/README.md
        https://raw.githubusercontent.com/liaTemplates/JSXGraph/main/README.md


import: https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/main/README.md








@onload


// =========================================================
// Root-Window: gemeinsamer Speicher zwischen LiaScript & JSXGraph
// =========================================================
window.__ROOT = window.__ROOT || (function () {
  try {
    // In LiaScript/JSXGraph ist "parent" oft das Hauptdokument.
    // Falls es mehrere Ebenen gibt: so weit wie möglich hoch.
    let w = window;
    while (w.parent && w.parent !== w) w = w.parent;
    return w;
  } catch (e) {
    return window;
  }
})();

const ROOT = window.__ROOT;

// Gemeinsame Stores IM ROOT
ROOT.__boards  = ROOT.__boards  || {}; // id -> board
ROOT.__points  = ROOT.__points  || {}; // boardId -> { name -> point }
ROOT.__targets = ROOT.__targets || {}; // boardId -> { key -> f(x) }

// Optional: Queue, falls Buttons vor Board-Init geklickt werden
ROOT.__pendingPointSpecs = ROOT.__pendingPointSpecs || []; // ["boardId;Name", ...]






window.__boards = window.__boards || {};          // id -> board
window.__points = window.__points || {};          // boardId -> { name -> point }

window.ensurePoint = function (boardId, name) {
  const ROOT = window.__ROOT || window;
  const board = ROOT.__boards && ROOT.__boards[boardId];
  if (!board) return false;

  ROOT.__points[boardId] = ROOT.__points[boardId] || {};

  // existiert schon
  if (ROOT.__points[boardId][name] && ROOT.__points[boardId][name].elType === 'point') {
    ROOT.__points[boardId][name].setAttribute({ strokeWidth: 4 });
    setTimeout(() => ROOT.__points[boardId][name].setAttribute({ strokeWidth: 2 }), 250);
    try { window.__applyPointLabelTheme && window.__applyPointLabelTheme(boardId); } catch (e) {}
    board.update();
    return true;
  }

  const x0 = Math.random();
  const y0 = Math.random();

  const labelCol = (window.__neutralAutoColor ? window.__neutralAutoColor() : '#000');

  const pt = board.create('point', [x0, y0], {
    name: name,
    withLabel: true,                 // <- wichtig: Label aktiv halten
    label: {                         // <- Label-Farben (Text)
      strokeColor: labelCol,
      fillColor:   labelCol,
      highlightStrokeColor: labelCol,
      highlightFillColor:   labelCol
    },

    face: 'x',
    size: 6,
    strokeColor: 'purple',
    fillColor: 'purple',
    fixed: false
  });

  // sehr defensiv: manche JSXGraph-Versionen brauchen das am Label-Objekt direkt
  try {
    if (pt.label && typeof pt.label.setAttribute === 'function') {
      pt.label.setAttribute({
        strokeColor: labelCol,
        fillColor:   labelCol,
        highlightStrokeColor: labelCol,
        highlightFillColor:   labelCol
      });
    }
  } catch (e) {}


  pt.setAttribute({ showInfobox: false, showInfoBox: false });
  pt.on('over', () => { board.infobox && board.infobox.hide && board.infobox.hide(); });
  pt.on('out',  () => { board.infobox && board.infobox.hide && board.infobox.hide(); });

  ROOT.__points[boardId][name] = pt;
  try { window.__applyPointLabelTheme && window.__applyPointLabelTheme(boardId); } catch (e) {}
  board.update();
  return true;
};

window.ensurePointFromSpec = function (spec) {
  const ROOT = window.__ROOT || window;
  const parts = String(spec).split(';').map(s => String(s).trim());
  const boardId = parts[0] || '';
  const name    = parts[1] || '';
  if (!boardId || !name) return;

  // Wenn Board noch nicht da ist: merken und später flushen
  if (!ROOT.__boards || !ROOT.__boards[boardId]) {
    ROOT.__pendingPointSpecs.push(`${boardId};${name}`);
    return;
  }

  window.ensurePoint(boardId, name);
};



// ---- Theme-Farbe lesen (aus echtem .lia-btn; ggf. aus parent) ----
window.readLiaBtnColor = window.readLiaBtnColor || function (fallback = '#0b5fff') {
  // 0) Priorität: explizite Grid-Variable (für Switch gedacht)
  try {
    const cs0 = getComputedStyle(document.documentElement);
    const v0 = cs0.getPropertyValue('--grid-color').trim();
    if (v0) return v0;
  } catch (e) {}

  // 1) Buttonfarbe aus dem aktuellen Dokument lesen
  try {
    const btn = document.querySelector('.lia-btn');
    if (btn) {
      const cs = getComputedStyle(btn);
        const bg = cs.backgroundColor && cs.backgroundColor !== 'rgba(0, 0, 0, 0)' ? cs.backgroundColor : '';
        if (bg) return bg;

        // oft ist bei Buttons die Akzentfarbe am Border sichtbar
        const br = cs.borderTopColor && cs.borderTopColor !== 'rgba(0, 0, 0, 0)' ? cs.borderTopColor : '';
        if (br) return br;

        if (cs.color) return cs.color;
    }
  } catch (e) {}

  // 2) Falls JSXGraph in einem isolierten Kontext läuft: parent versuchen
  try {
    if (window.parent && window.parent.document) {
      const btn = window.parent.document.querySelector('.lia-btn');
      if (btn) {
        const cs = window.parent.getComputedStyle(btn);
            const bg = cs.backgroundColor && cs.backgroundColor !== 'rgba(0, 0, 0, 0)' ? cs.backgroundColor : '';
            if (bg) return bg;

            // oft ist bei Buttons die Akzentfarbe am Border sichtbar
            const br = cs.borderTopColor && cs.borderTopColor !== 'rgba(0, 0, 0, 0)' ? cs.borderTopColor : '';
            if (br) return br;

            if (cs.color) return cs.color;
      }
      // auch dort --grid-color probieren
      const csP = window.parent.getComputedStyle(window.parent.document.documentElement);
      const vP = csP.getPropertyValue('--grid-color').trim();
      if (vP) return vP;
    }
  } catch (e) {}

  return fallback;
};


// ---- Grid-Farbe auf einem Board aktualisieren ----
window.applyGridColor = window.applyGridColor || function (board, color) {
  if (!board || !color) return;

  // 1) Optionen setzen (für zukünftige Rebuilds)
  try {
    if (board.options && board.options.grid) {
      if (board.options.grid.major) board.options.grid.major.strokeColor = color;
      if (board.options.grid.minor) board.options.grid.minor.strokeColor = color;
    }
  } catch (e) {}

  // 2) EXISTIERENDE Grid-Objekte einfärben (das ist der entscheidende Teil)
  try {
    // Viele JSXGraph-Versionen haben board.grids (Array)
    if (board.grids && board.grids.length) {
      board.grids.forEach(g => {
        if (g && typeof g.setAttribute === 'function') {
          g.setAttribute({ strokeColor: color });
        }
      });
    }

    // Sehr defensiv: auch in objectsList nach "grid" suchen
    if (board.objectsList && board.objectsList.length) {
      board.objectsList.forEach(o => {
        if (!o || typeof o.setAttribute !== 'function') return;
        if (o.elType === 'grid' || o.type === (JXG && JXG.OBJECT_TYPE_GRID)) {
          o.setAttribute({ strokeColor: color });
        }
      });
    }
  } catch (e) {}

  // 3) Redraw
  try {
    if (typeof board.fullUpdate === 'function') board.fullUpdate();
    else board.update();
  } catch (e) {}
};


// ---- Auto-Update: Farbe regelmäßig prüfen und bei Änderung anwenden ----
window.watchGridColor = window.watchGridColor || function (board, intervalMs = 400) {
  if (!board) return;
  if (!window.__gridWatchers) window.__gridWatchers = new WeakMap();

  // nicht doppelt starten
  if (window.__gridWatchers.has(board)) return;

  let last = '';

  const timer = setInterval(() => {
    const c = window.readLiaBtnColor('#0b5fff');
    if (c && c !== last) {
      last = c;
      window.applyGridColor(board, c);
    }
  }, intervalMs);

  window.__gridWatchers.set(board, timer);
};

window.__targets = window.__targets || {}; // boardId -> { key -> f(x) }

// Ziel-Funktion registrieren (y = f(x))
window.setTargetFunction = window.setTargetFunction || function (boardId, key, fn) {
  window.__targets[boardId] = window.__targets[boardId] || {};
  window.__targets[boardId][key] = fn;
};

// Prüfen: Punkt nahe an y=f(x)
window.isPointOnTargetFunction = window.isPointOnTargetFunction || function (boardId, pointName, key, epsY = 0.15) {
  const pt = window.__points && window.__points[boardId] && window.__points[boardId][pointName];
  const fn = window.__targets && window.__targets[boardId] && window.__targets[boardId][key];
  if (!pt || typeof fn !== 'function') return false;

  const x = pt.X();
  const y = pt.Y();
  const y0 = fn(x);

  if (!isFinite(y0)) return false;
  return Math.abs(y - y0) <= epsY;
};




// =========================================================
// MathJax helper: typeset im ROOT/parent (wichtig bei Lia/JSXGraph)
// =========================================================
ROOT.__typeset = ROOT.__typeset || function (el) {
  if (!el) return;

  // MathJax kann je nach LiaScript in parent/root hängen
  const MJ =
    (ROOT && ROOT.MathJax) ||
    (window.parent && window.parent.MathJax) ||
    window.MathJax;

  if (!MJ) return;

  try {
    // MathJax v3
    if (typeof MJ.typesetPromise === 'function') {
      if (typeof MJ.typesetClear === 'function') MJ.typesetClear([el]);
      MJ.typesetPromise([el]);
      return;
    }
    // MathJax v2 fallback
    if (MJ.Hub && typeof MJ.Hub.Queue === 'function') {
      MJ.Hub.Queue(['Typeset', MJ.Hub, el]);
    }
  } catch (e) {}
};


window.__isDarkTheme = window.__isDarkTheme || function () {
  try {
    const doc = (window.parent && window.parent.document) ? window.parent.document : document;
    const win = (window.parent && window.parent.getComputedStyle) ? window.parent : window;
    const el = doc.body || doc.documentElement;
    const bg = win.getComputedStyle(el).backgroundColor;
    const m = bg.match(/rgba?\((\d+),\s*(\d+),\s*(\d+)/i);
    if (!m) return false;
    const r = parseInt(m[1], 10), g = parseInt(m[2], 10), b = parseInt(m[3], 10);
    const lum = 0.2126 * r + 0.7152 * g + 0.0722 * b;
    return lum < 128;
  } catch (e) { return false; }
};

window.__neutralAutoColor = window.__neutralAutoColor || function () {
  return window.__isDarkTheme() ? '#fff' : '#000';
};

window.__recolorNeutralAutoLabels = window.__recolorNeutralAutoLabels || function () {
  const col = window.__neutralAutoColor();
  document.querySelectorAll('span.autoNameNeutral').forEach(el => { el.style.color = col; });
};


window.__applyPointLabelTheme = window.__applyPointLabelTheme || function (boardId) {
  const ROOT = window.__ROOT || window;
  const col  = (window.__neutralAutoColor ? window.__neutralAutoColor() : '#000');

  const pts = ROOT.__points && ROOT.__points[boardId];
  if (!pts) return;

  Object.values(pts).forEach(pt => {
    if (!pt || typeof pt.setAttribute !== 'function') return;

    // Label-Defaults am Punkt
    try {
      pt.setAttribute({
        label: {
          strokeColor: col,
          fillColor: col,
          highlightStrokeColor: col,
          highlightFillColor: col
        }
      });
    } catch (e) {}

    // Direkt am Label-Objekt (je nach JSXGraph-Version entscheidend)
    try {
      if (pt.label && typeof pt.label.setAttribute === 'function') {
        pt.label.setAttribute({
          strokeColor: col,
          fillColor: col,
          highlightStrokeColor: col,
          highlightFillColor: col
        });
      }
    } catch (e) {}
  });

  // redraw
  try {
    const b = ROOT.__boards && ROOT.__boards[boardId];
    if (b) b.update();
  } catch (e) {}
};



(function () {
  const applyAll = () => {
    const ROOT = window.__ROOT || window;
    Object.keys(ROOT.__points || {}).forEach(bid => {
      try { window.__applyPointLabelTheme(bid); } catch (e) {}
    });
  };

  applyAll(); // initial

  try {
    const mq = window.matchMedia('(prefers-color-scheme: dark)');
    if (mq && typeof mq.addEventListener === 'function') mq.addEventListener('change', applyAll);
    else if (mq && typeof mq.addListener === 'function') mq.addListener(applyAll);
  } catch (e) {}
})();



@end








-->

# Probeleistungskontrolle für Physik - Klasse 10: Wellen


> Letzte Aktualisierung am 13.02. gegen 18:30 Uhr


> <h2> WICHTIGER HINWEIS: Ich teste auch neue Funktionen mit dieser Datei, sollte etwas seltsames angezeigt werden oder gar nicht zu sehen sein, bitte einfach die Datei aktualisieren. Ich versuche die auftretenden Bugs der neuen Features nach und nach zu beseitigen. <br> <p align="right"> -Lommatzsch </p> </h2>


Swipe (Wische) entweder weiter oder klicke unten links auf neben der Seitenzahl auf den Pfeil nach rechts.



Diese Probearbeit hat mehr Aufgaben als die richtige Arbeit, damit du genug zum Üben hast. Es sind viele verschiedene Aufgabentypen abgebildet, sodass du alles nochmal bei der Bearbeitung dieser Aufgaben wiederholst.

Oben links in der Kopfzeile dieses LiaScript-Kurses findest du einen Textmarker.

Bei den Aufgaben ist auch immer ein Stiftbutton eingeblendet, klicke auf diesen Button und erhalte eine Schreibfläche.






## Schrifterkennung



<center>

<!-- style="width:200px" -->
![Navigation](https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/Readme/canvas.png)

</center>

1. Öffnet oder schließt die Schreibfläche.

2. Macht die letzte Änderung auf der Schreibfläche rückgängig.

3. Stellt das letzte "Rückgängig machen" wieder her.

4. Radierer mit Submenü für Radierergröße oder komplettes löschen.

5. Stift mit Submenü für Farbauswahl, Stiftdicke und Transparenz.

6. Legt ein Grid oder Linien in den Hintergrund.

7. Lässt ein Feld ziehen, welches mittels Schrifterkennung an das Eingabefeld als Lösung übergibt.

Die Schreibfläche kann unten links oder rechts an den Ecke in der Größe beliebig verändert werden.


> **Steuerung mit Maus**

- Linke Maustaste: Zeichnen, Radieren, Ziehen

- Rechte Maustaste: Schreibfläche hin- und herziehen

- Mausrad: Zoom


> **Steuerung mit Touchscreen**

- Ein Finger:  Zeichnen, Radieren, Ziehen

- Zwei Finger (Abstand zwischen den Fingern gleichbleibend): Schreibfläche hin- und herziehen

- Zwei Finger (Abstand zwischen den Fingern verändern): Zoom


---

---


> **Beispielaufgaben**

**Aufgabe 1:** Berechne den Wert des Terms


__$a)\;\;$__
$1470+8 =$ [[     1478    ]] 

@canvas




__$b)\;\;$__
$5010+300 =$ [[     5310    ]] 

@canvas





__$c)\;\;$__
$4200+89 =$ [[     4289    ]] 

@canvas








## Schwingungen - Rechnungen


**Aufgabe 1**  
Eine empfindliche Messplatine (Masse $m=200\,\text{g}$) wird zur Vibrationsentkopplung an eine Feder mit $D=5\,\dfrac{\text{N}}{\text{m}}$ gehängt. Die maximale Auslenkung beträgt $A=7\,\text{cm}$ bei eine Phasenverschiebung von $90^\circ$.  

__$a)\;\;$__ Berechne die Kreisfrequenz.


$\omega = $ [[ 5 ]] $\,\dfrac{1}{\text{s}}$  
@Algebrite.check2(5,0.01)
******************
$$
\begin{align*}
\omega &= \sqrt{\frac{D}{m}} \\[4pt]
m &= 200\,\text{g}=0{,}200\,\text{kg}, \qquad D=5\,\frac{\text{N}}{\text{m}} \\[4pt]
\omega &= \sqrt{\frac{5}{0{,}200}} \,\frac{1}{\text{s}}
       = \sqrt{25}\,\frac{1}{\text{s}}
       = 5\,\frac{1}{\text{s}}
\end{align*}
$$
******************

@canvas

__$b)\;\;$__ Gib eine passende Schwingungsgleichung an und berechne die Elongation nach $t=0{,}30\,\text{s}$ (in $\text{cm}$).


$y(0{,}30\,\text{s}) \approx $ [[ 0,495 ]] $\,\text{cm}$  
@Algebrite.check2(0.495,0.01)
******************
$$
\begin{align*}
A &= 7\,\text{cm}=0{,}070\,\text{m}, \qquad \varphi = 90^\circ=\frac{\pi}{2} \\[4pt]
y(t) &= 0{,}070\,\text{m}\cdot \sin\!\left(5\,\frac{1}{\text{s}}\,t+\frac{\pi}{2}\right) \\[6pt]
y(0{,}30\,\text{s})
&= 0{,}070\,\text{m}\cdot \sin\!\left(5\cdot 0{,}30+\frac{\pi}{2}\right) \\
&= 0{,}070\,\text{m}\cdot \sin\!\left(1{,}5+\frac{\pi}{2}\right) \\
&\approx 0{,}070\,\text{m}\cdot 0{,}07074 \\
&\approx 0{,}00495\,\text{m}
= 0{,}495\,\text{cm}
\end{align*}
$$
******************

@canvas


---

---



**Aufgabe 2**  
Eine Actioncam ist an einer Federhalterung befestigt (Masse $m=140\,\text{g}$). Für kleine Schwingungen gilt die Schwingungsgleichung
$$
y(t)=3{,}5\,\text{cm}\,\sin\!\left(\frac{8}{\text{s}}\,t+\frac{\pi}{3}\right).
$$

__$a)\;\;$__ Berechne die Federkonstante $D$.

$D \approx $ [[ 8,96 ]] $\,\dfrac{\text{N}}{\text{m}}$  
@Algebrite.check2(8.96,0.02)
******************
$$
\begin{align*}
y(t) &= A\sin(\omega t+\varphi) \quad\Rightarrow\quad \omega = 8\,\frac{1}{\text{s}} \\[4pt]
D &= m\omega^2 \\[4pt]
m &= 140\,\text{g}=0{,}140\,\text{kg} \\[4pt]
D &= 0{,}140\cdot 8^2 \,\frac{\text{kg}}{\text{s}^2}
= 0{,}140\cdot 64\,\frac{\text{kg}}{\text{s}^2}
= 8{,}96\,\frac{\text{N}}{\text{m}}
\end{align*}
$$
******************

@canvas

__$b)\;\;$__ Berechne die Elongation nach einer Periodendauer $T$.


$y(T) \approx $ [[ 3,031 ]] $\,\text{cm}$  
@Algebrite.check2(3.031,0.02)
******************
$$
\begin{align*}
T &= \frac{2\pi}{\omega} = \frac{2\pi}{8}\,\text{s} = \frac{\pi}{4}\,\text{s} \\[6pt]
y(T) &= A\sin(\omega T+\varphi)
= 3{,}5\,\text{cm}\cdot \sin\!\left(8\cdot \frac{\pi}{4}+\frac{\pi}{3}\right) \\
&= 3{,}5\,\text{cm}\cdot \sin\!\left(2\pi+\frac{\pi}{3}\right)
= 3{,}5\,\text{cm}\cdot \sin\!\left(\frac{\pi}{3}\right) \\
&= 3{,}5\,\text{cm}\cdot \frac{\sqrt{3}}{2}
\approx 3{,}031\,\text{cm}
\end{align*}
$$
******************


@canvas


---

---


**Aufgabe 3**  
Ein Fadenpendel schwingt (kleine Auslenkungen) mit
$$
y(t)=2{,}8\,\text{cm}\,\sin\!\left(\frac{\pi}{\text{s}}\,t+\frac{\pi}{6}\right).
$$
Nimm $g=9{,}81\,\dfrac{\text{m}}{\text{s}^2}$ an.

__$a)\;\;$__ Berechne die Fadenlänge $L$.


$L \approx $ [[ 0,994 ]] $\,\text{m}$  
@Algebrite.check2(0.994,0.005)
******************
$$
\begin{align*}
\omega &= \sqrt{\frac{g}{L}}
\quad\Rightarrow\quad
L = \frac{g}{\omega^2} \\[4pt]
\omega &= \pi\,\frac{1}{\text{s}} \\[4pt]
L &= \frac{9{,}81}{\pi^2}\,\text{m}
\approx \frac{9{,}81}{9{,}8696}\,\text{m}
\approx 0{,}994\,\text{m}
\end{align*}
$$
******************

@canvas

__$b)\;\;$__ Der Faden wird um $20\%$ verlängert. Berechne die neue Periodendauer $T_\text{neu}$.


$T_\text{neu} \approx $ [[ 2,19 ]] $\,\text{s}$  
@Algebrite.check2(2.19,0.02)
******************
$$
\begin{align*}
L_\text{neu} &= 1{,}20\cdot L \approx 1{,}20\cdot 0{,}994\,\text{m} \approx 1{,}193\,\text{m} \\[6pt]
T &= 2\pi\sqrt{\frac{L}{g}}
\quad\Rightarrow\quad
T_\text{neu} = 2\pi\sqrt{\frac{L_\text{neu}}{g}} \\[6pt]
T_\text{neu} &=
2\pi\sqrt{\frac{1{,}193}{9{,}81}}\,\text{s}
\approx 2\pi\sqrt{0{,}1216}\,\text{s}
\approx 2\pi\cdot 0{,}3487\,\text{s}
\approx 2{,}19\,\text{s}
\end{align*}
$$
******************


@canvas

---

**Aufgabe 4:**  
Eine leichte Schaukel wird ausgelenkt (kleine Auslenkungen). Die gemessene Periodendauer beträgt $T=1{,}6\,\text{s}$, die maximale Auslenkung $A=5\,\text{cm}$.  
Verwende $y(t)=A\sin(\omega t+\varphi)$ mit $\varphi=-45^\circ$.

__$a)\;\;$__ Berechne die Kreisfrequenz $\omega$.


$\omega \approx $ [[ 3,927 ]] $\,\dfrac{1}{\text{s}}$  
@Algebrite.check2(3.92699,0.02)
******************
$$
\begin{align*}
\omega &= \frac{2\pi}{T}
= \frac{2\pi}{1{,}6\,\text{s}}
= \frac{2\pi}{\frac{8}{5}\,\text{s}}
= \frac{5\pi}{4}\,\frac{1}{\text{s}}
\approx 3{,}927\,\frac{1}{\text{s}}
\end{align*}
$$
******************

@canvas

__$b)\;\;$__ Gib die Schwingungsgleichung an und berechne $y(0{,}50\,\text{s})$ (in $\text{cm}$).


$y(0{,}50\,\text{s}) \approx $ [[ 4,619 ]] $\,\text{cm}$  
@Algebrite.check2(4.619,0.02)
******************
$$
\begin{align*}
A &= 5\,\text{cm}, \qquad \varphi = -45^\circ = -\frac{\pi}{4} \\[4pt]
y(t) &= 5\,\text{cm}\cdot \sin\!\left(\frac{5\pi}{4}\,\frac{1}{\text{s}}\,t-\frac{\pi}{4}\right) \\[6pt]
y(0{,}50\,\text{s})
&= 5\,\text{cm}\cdot \sin\!\left(\frac{5\pi}{4}\cdot 0{,}50-\frac{\pi}{4}\right) \\
&= 5\,\text{cm}\cdot \sin\!\left(\frac{5\pi}{8}-\frac{2\pi}{8}\right)
= 5\,\text{cm}\cdot \sin\!\left(\frac{3\pi}{8}\right) \\
&\approx 5\,\text{cm}\cdot 0{,}92388
\approx 4{,}619\,\text{cm}
\end{align*}
$$
******************


@canvas



## Wellen - Rechnungen






**Aufgabe 1:**  
In einem Wellenbecken läuft eine sinusförmige Wasserwelle gleichmäßig in $x$-Richtung. Die Welle schwingt mit der Periodendauer $0{,}80\,\text{s}$, die maximale Auslenkung beträgt $3{,}6\,\text{cm}$ und die Wellenlänge ist $50\,\text{cm}$.  
Nach $10\,\text{s}$ wird bei der Stelle $x=15\,\text{cm}$ ein Foto gemacht. Berechne die momentane Elongation an dieser Stelle.


$y(15\,\text{cm};10\,\text{s}) \approx $ [[ 3,42 ]] $\,\text{cm}$  
@Algebrite.check2(3.4238,0.02)
******************
$$
\begin{align*}
y(x;t) &= A \sin \left(2\pi \left[ \frac{t}{T} - \frac{x}{\lambda} \right]\right) \\[4pt]
y(15\,\text{cm};10\,\text{s})
&= 3{,}6\,\text{cm}\cdot \sin \left(2\pi \left[ \frac{10\,\text{s}}{0{,}80\,\text{s}} - \frac{15\,\text{cm}}{50\,\text{cm}} \right]\right) \\[6pt]
& \approx 3{,}4238\,\text{cm}
\end{align*}
$$
******************

@canvas

---

**Aufgabe 2:**  
An einem langen Seil läuft eine sinusförmige Welle in $x$-Richtung. Die maximale Auslenkung beträgt $17\,\text{mm}$ und die Wellenlänge $35\,\text{mm}$.  
Nach $4{,}4\,\text{s}$ wird in $9{,}0\,\text{cm}$ Entfernung vom Erreger eine Elongation von $10\,\text{mm}$ gemessen. Berechne die Periodendauer $T$.


$T \approx $ [[ 1,65 ]] $\,\text{s}$  
@Algebrite.check2(1.647,0.02)
******************
$$
\begin{align*}
y(x;t) &= A \sin \left(2\pi \left[ \frac{t}{T} - \frac{x}{\lambda} \right]\right)
\quad \left| :A \right. \\[4pt]
\frac{y(x;t)}{A} &= \sin \left(2\pi \left[ \frac{t}{T} - \frac{x}{\lambda} \right]\right) \\[4pt]
\arcsin\left(\frac{y(x;t)}{A}\right) &= 2\pi \left[ \frac{t}{T} - \frac{x}{\lambda} \right]
\quad \left| : (2\pi) \right. \\[6pt]
\frac{ \arcsin\left(\frac{y(x;t)}{A}\right)}{2\pi} &= \frac{t}{T} - \frac{x}{\lambda}
\quad \left| +\frac{x}{\lambda} \right. \\[6pt]
\frac{ \arcsin\left(\frac{y(x;t)}{A}\right)}{2\pi} + \frac{x}{\lambda} &= \frac{t}{T}
\quad \left| :\left(\frac{ \arcsin\left(\frac{y(x;t)}{A}\right)}{2\pi} + \frac{x}{\lambda}\right) \right. \\[8pt]
T &= \frac{t}{\frac{ \arcsin\left(\frac{y(x;t)}{A}\right)}{2\pi} + \frac{x}{\lambda}}
\end{align*}
$$
$$
\begin{align*}
x &= 9{,}0\,\text{cm} = 90\,\text{mm} \\[4pt]
T
&= \frac{4{,}4\,\text{s}}
{\frac{\arcsin\left(\frac{10\,\text{mm}}{17\,\text{mm}}\right)}{2\pi} + \frac{90\,\text{mm}}{35\,\text{mm}}} \\[6pt]
&= \frac{4{,}4\,\text{s}}
{\frac{\arcsin\left(\frac{10}{17}\right)}{2\pi} + \frac{18}{7}} \\[6pt]
\arcsin\left(\frac{10}{17}\right) &\approx 0{,}629 \\
\Rightarrow\quad
T &\approx \frac{4{,}4\,\text{s}}
{\frac{0{,}629}{2\pi} + 2{,}5714}
\approx \frac{4{,}4\,\text{s}}{2{,}6715}
\approx 1{,}647\,\text{s}
\end{align*}
$$
******************

@canvas

---

**Aufgabe 3:**  
Auf einem Slinky läuft eine sinusförmige Welle in $x$-Richtung. Die maximale Auslenkung beträgt $17\,\text{cm}$, die Periodendauer ist $1{,}1\,\text{s}$.  
Nach $4{,}4\,\text{s}$ misst man in $7{,}8\,\text{cm}$ Entfernung vom Erreger eine Elongation von $10\,\text{cm}$. Berechne die Ausbreitungsgeschwindigkeit $c$ der Welle.


$c \approx $ [[ 0,0182 ]] $\,\dfrac{\text{m}}{\text{s}}$  
@Algebrite.check2(0.01818,0.0006)
******************
$$
\begin{align*}
y(x;t) &= A \sin \left(2\pi \left[ \frac{t}{T} - \frac{x}{\lambda} \right]\right) \\[4pt]
10\,\text{cm}
&= 17\,\text{cm}\cdot \sin \left(2\pi \left[ \frac{4{,}4\,\text{s}}{1{,}1\,\text{s}} - \frac{7{,}8\,\text{cm}}{\lambda} \right]\right) 
\quad \left| :17\,\text{cm} \right. \\[6pt]
\frac{10}{17}
&= \sin \left(2\pi \left[ 4 - \frac{7{,}8\,\text{cm}}{\lambda} \right]\right) \\[6pt]
\arcsin\left(\frac{10}{17}\right)
&= 2\pi \left[ 4 - \frac{7{,}8\,\text{cm}}{\lambda} \right]
\quad \left| :(2\pi)\right. \\[6pt]
\frac{1}{2\pi}\arcsin\left(\frac{10}{17}\right)
&= 4 - \frac{7{,}8\,\text{cm}}{\lambda}
\quad \left| -4 \right. \\[6pt]
\frac{1}{2\pi}\arcsin\left(\frac{10}{17}\right) - 4
&= - \frac{7{,}8\,\text{cm}}{\lambda}
\quad \left| \cdot (-1)\right. \\[6pt]
-\frac{1}{2\pi}\arcsin\left(\frac{10}{17}\right) + 4
&= \frac{7{,}8\,\text{cm}}{\lambda}
\quad \left| :7{,}8\,\text{cm}\right. \\[8pt]
\frac{1}{7{,}8\,\text{cm}}\left(-\frac{1}{2\pi}\arcsin\left(\frac{10}{17}\right) + 4\right)
&= \frac{1}{\lambda}
\quad \Rightarrow\quad
\lambda = \frac{7{,}8\,\text{cm}}{-\frac{1}{2\pi}\arcsin\left(\frac{10}{17}\right) + 4}
\end{align*}
$$
$$
\begin{align*}
\arcsin\left(\frac{10}{17}\right) &\approx 0{,}629 \\[4pt]
\lambda &\approx \frac{7{,}8\,\text{cm}}{4 - \frac{0{,}629}{2\pi}}
\approx \frac{7{,}8\,\text{cm}}{3{,}8999}
\approx 2{,}00\,\text{cm}
= 0{,}0200\,\text{m} \\[6pt]
c &= \frac{\lambda}{T}
\approx \frac{0{,}0200\,\text{m}}{1{,}1\,\text{s}}
\approx 0{,}01818\,\frac{\text{m}}{\text{s}}
\end{align*}
$$
******************

@canvas


---


---

**Aufgabe 4:**  
Auf einer Wasseroberfläche breitet sich eine sinusförmige Welle in $x$-Richtung aus. Die maximale Auslenkung beträgt $4{,}5\,\text{cm}$. Der Erreger schwingt mit einer Periodendauer von $0{,}50\,\text{s}$, und die Welle läuft mit $0{,}40\,\dfrac{\text{m}}{\text{s}}$ nach rechts.  
Berechne die Elongation nach $1{,}0\,\text{s}$ an der Stelle $x=3{,}0\,\text{cm}$.


$y(3{,}0\,\text{cm};1{,}0\,\text{s}) \approx $ [[ -3,64 ]] $\,\text{cm}$  
@Algebrite.check2(-3.6406,0.02)
******************
$$
\begin{align*}
\lambda &= c\cdot T
= 0{,}40\,\frac{\text{m}}{\text{s}}\cdot 0{,}50\,\text{s}
= 0{,}20\,\text{m}
= 20\,\text{cm} \\[6pt]
y(x;t) &= A \sin \left(2\pi \left[ \frac{t}{T} - \frac{x}{\lambda} \right]\right) \\[6pt]
y(3{,}0\,\text{cm};1{,}0\,\text{s})
&= 4{,}5\,\text{cm}\cdot \sin \left(2\pi \left[ \frac{1{,}0\,\text{s}}{0{,}50\,\text{s}} - \frac{3{,}0\,\text{cm}}{20\,\text{cm}} \right]\right) \\[6pt]
& \approx -3{,}6406\,\text{cm}
\end{align*}
$$
******************

@canvas





















## Komplexe Aufgabe 1






Ein Wagen der Masse $m$ ist an einer horizontalen Feder befestigt (reibungslos).  
Die Feder wird um $s = 2{,}8 \,\text{cm}$ zusammengedrückt und gespeichert ist dabei eine Spannenergie von $E_\text{sp} = 0{,}15 \,\text{mJ}$.  
Anschließend wird losgelassen und der Wagen führt eine harmonische Schwingung aus.

Hinweise und Gleichungen: \

- $E_\text{sp} = \dfrac{1}{2} D s^2$ \

- $\omega = \sqrt{\dfrac{D}{m}}$ \

- $T = \dfrac{2\pi}{\omega}$ \

- $x(t) = A \sin(\omega t + \varphi_0)$ \

- $v_\text{max} = A \cdot \omega$ \

- $F_\text{Feder,max} = D \cdot A$ \





---

---



__$a)\;\;$__ Bestimme die Federkonstante $D$ aus der gespeicherten Spannenergie.


$ D \approx $ [[ 0,383        ]] $\,\dfrac{\text{N}}{\text{m}}$
@Algebrite.check2(0.383,0.01)
******************
$$
\begin{align*}
E_\text{sp} &= \frac{1}{2} D s^2 \\
\Rightarrow D &= \frac{2 E_\text{sp}}{s^2} \\[6pt]
s &= 0{,}028 \,\text{m} \quad,\quad
E_\text{sp} = 0{,}00015 \,\text{J} \\[6pt]
D &= \frac{2 \cdot 0{,}00015 \,\text{J}}{(0{,}028 \,\text{m})^2} \\
  &= \frac{0{,}00030}{0{,}000784} \,\frac{\text{J}}{\text{m}^2} \\
  &\approx 0{,}383 \,\dfrac{\text{N}}{\text{m}}
\end{align*}
$$
******************

@canvas

---

---



__$b)\;\;$__ Berechne die Kreisfrequenz $\omega$ und die Periodendauer $T$ der Schwingung für die angehängte Masse $m = 0{,}180 \,\text{kg}$.


$ \omega \approx $ [[ 1,458        ]]  $\dfrac{1}{\text{s}}$ \
@Algebrite.check2(1.458,0.01)
$ T \approx $ [[ 4,309       ]] $\,\text{s}$
@Algebrite.check2(4.309,0.01)
******************
$$
\begin{align*}
\omega &= \sqrt{\frac{D}{m}}
= \sqrt{\frac{0{,}383 \,\text{N/m}}{0{,}180 \,\text{kg}}} \\[6pt]
&\approx \sqrt{2{,}1278 \,\text{s}^{-2}}
\approx 1{,}458 \,\text{s}^{-1} \\[10pt]
T &= \frac{2\pi}{\omega}
= \frac{2\pi}{1{,}458 \,\text{s}^{-1}}
\approx 4{,}309 \,\text{s}
\approx 4{,}31 \,\text{s}
\end{align*}
$$
******************

@canvas

---

---



__$c)\;\;$__ Die Schwingung startet NICHT im Extrempunkt, sondern mit einer Phasenverschiebung  
$\varphi_0 = \dfrac{\pi}{4}$. Die Amplitude sei $A = 2{,}8 \,\text{cm}$.

1. Gib die vollständige Schwingungsgleichung $x(t)$ an.  
2. Berechne daraus die momentane Auslenkung $x(0{,}50 \,\text{s})$ in Zentimeter.



$ x(0.50\,\text{s}) \approx $ [[ 2,796        ]] cm
@Algebrite.check2(2.796,0.01)
******************
$$
\begin{align*}
x(t) &= A \sin(\omega t + \varphi_0) \\[4pt]
A &= 0{,}028 \,\text{m}, \quad
\omega \approx 1{,}458 \,\text{s}^{-1}, \quad
\varphi_0 = \frac{\pi}{4} \\[6pt]
\Rightarrow x(t)
&= 0{,}028 \,\text{m} \cdot
\sin \!\big( 1{,}458\, t + \frac{\pi}{4} \big) \\[10pt]
x(0{,}50 \,\text{s})
&= 0{,}028 \,\text{m} \cdot
\sin \!\big( 1{,}458 \cdot 0{,}50 + \frac{\pi}{4} \big) \\
&\approx 0{,}02796 \,\text{m} \\
&\approx 2{,}80 \,\text{cm}
\end{align*}
$$
******************

@canvas

---

---


__$d)\;\;$__ Bestimme zwei charakteristische Größen dieser Schwingung:

1. die maximale Geschwindigkeit $v_\text{max}$,  
2. die maximale Rückstellkraft $F_\text{Feder,max}$ der Feder auf vier Nachkommastellen genau.


$ v_\text{max} \approx $ [[ 0,0408        ]]  $\,\dfrac{\text{m}}{\text{s}}$ \
$ F_\text{Feder,max} \approx $ [[ 0,0107        ]] N
******************
$$
\begin{align*}
v_\text{max} &= A \cdot \omega \\
&= 0{,}028 \,\text{m} \cdot 1{,}458 \,\text{s}^{-1} \\
&\approx 0{,}0408 \,\text{m/s} \\[12pt]
F_\text{Feder,max} &= D \cdot A \\
&= 0{,}383 \,\text{N/m} \cdot 0{,}028 \,\text{m} \\
&\approx 0{,}0107 \,\text{N}
\end{align*}
$$
******************



@canvas



















## Komplexe Aufgabe 2




Eine mechanische Welle breitet sich entlang einer Schnur in $+x$-Richtung aus.  
Für ihre Auslenkung gilt:

$$
y(x;t) \;=\; A \,\sin\!\left(
2\pi \left[
\frac{t}{T} \;-\; \frac{x}{\lambda}
\right]
\right)
$$

mit  

- $A$: Amplitude (maximale Auslenkung),  \

- $T$: Periodendauer,  \

- $\lambda$: Wellenlänge,  \

- $y(x;t)$: momentane Elongation der Schnur an der Stelle $x$ zur Zeit $t$.\

Runde sinnvoll (3 signifikante Stellen).


---

---

__$a)\;\;$__ Eine Welle wird beschrieben durch  
Amplitude $A = 1{,}5 \,\text{cm}$,  
Periodendauer $T = 0{,}75 \,\text{s}$,  
Wellenlänge $\lambda = 36 \,\text{cm}$.

Bestimme die momentane Auslenkung $y(x;t)$ an der Stelle $x = 5{,}0 \,\text{cm}$ zum Zeitpunkt $t = 2{,}4 \,\text{s}$.


$ y(5{,}0\text{ cm};\,2{,}4\text{ s}) \approx $ [[ 0,562        ]] cm
******************
$$
\begin{align*}
y(x;t) &= A \sin\!\left(
2\pi\left[
\frac{t}{T} - \frac{x}{\lambda}
\right]\right) \\[8pt]
A &= 1{,}5 \,\text{cm}, \quad
T = 0{,}75 \,\text{s}, \quad
\lambda = 36 \,\text{cm}, \\
t &= 2{,}4 \,\text{s}, \quad
x = 5{,}0 \,\text{cm} \\[8pt]
\Rightarrow y(5{,}0\text{ cm};2{,}4\text{ s})
&= 1{,}5\,\text{cm} \cdot
\sin\!\left(
2\pi \left[
\frac{2{,}4}{0{,}75} - \frac{5{,}0}{36}
\right]\right) \approx 3{,}0611 \\[4pt]
2\pi \cdot 3{,}0611 &\approx 19{,}223 \\[4pt]
\sin(19{,}223) &\approx 0{,}3746 \\[4pt]
\Rightarrow y \approx 1{,}5\,\text{cm} \cdot 0{,}3746
\approx 0{,}562 \,\text{cm}
\end{align*}
$$
******************


@canvas


---

---





__$b)\;\;$__ Eine andere Welle hat Amplitude $A = 6{,}0 \,\text{mm}$ und Wellenlänge $\lambda = 10{,}0 \,\text{mm}$.  
Nach einer Zeit $t = 3{,}5 \,\text{s}$ misst man an der Stelle $x = 4{,}0 \,\text{cm}$ eine Elongation von $y = 5{,}2 \,\text{mm}$.

Bestimme daraus die Periodendauer $T$ der Welle.



$ T \approx $ [[ 0,840        ]] s
@Algebrite.check2(0.840,0.01)
******************
$$
\begin{align*}
y(x;t) &= A \sin\!\left(
2\pi\left[
\frac{t}{T} - \frac{x}{\lambda}
\right]\right) \\[8pt]
\Rightarrow
\frac{y(x;t)}{A}
&= \sin\!\left(
2\pi\left[
\frac{t}{T} - \frac{x}{\lambda}
\right]\right) \\[6pt]
\arcsin\!\left(\frac{y}{A}\right)
&= 2\pi \left[
\frac{t}{T} - \frac{x}{\lambda}
\right] \\[10pt]
\Rightarrow
\frac{t}{T}
&=
\frac{1}{2\pi}\arcsin\!\left(\frac{y}{A}\right)
+ \frac{x}{\lambda} \\[10pt]
\Rightarrow
T
&= \frac{t}{
\frac{1}{2\pi}\arcsin\!\left(\frac{y}{A}\right)
+ \frac{x}{\lambda}
}
\end{align*}
$$

Jetzt Zahlen einsetzen (achte auf gleiche Einheiten!):
- $A = 6{,}0 \,\text{mm}$  
- $y = 5{,}2 \,\text{mm}$  
- $\lambda = 10{,}0 \,\text{mm}$  
- $x = 4{,}0 \,\text{cm} = 40{,}0 \,\text{mm}$  
- $t = 3{,}5 \,\text{s}$

$$
\frac{y}{A} = \frac{5{,}2}{6{,}0} \approx 0{,}8667,
\quad
\arcsin(0{,}8667) \approx 1{,}0485 \,\text{rad}
$$

$$
\frac{1}{2\pi}\arcsin\!\left(\frac{y}{A}\right)
\approx
\frac{1{,}0485}{2\pi}
\approx 0{,}1669
$$

$$
\frac{x}{\lambda}
=
\frac{40{,}0\,\text{mm}}{10{,}0\,\text{mm}}
= 4{,}000
$$

$$
\Rightarrow
\frac{t}{T}
=
0{,}1669 + 4{,}000
= 4{,}1669
\quad\Rightarrow\quad
T
= \frac{3{,}5\,\text{s}}{4{,}1669}
\approx 0{,}840 \,\text{s}
$$
******************


@canvas


---

---






__$c)\;\;$__ Eine Welle hat Amplitude $A = 12{,}0 \,\text{cm}$.  
Zum Zeitpunkt $t = 3{,}0 \,\text{s}$ beobachtet man an der Stelle $x = 8{,}0 \,\text{cm}$ eine Auslenkung $y = 4{,}5 \,\text{cm}$.  
Die Periodendauer beträgt $T = 1{,}20 \,\text{s}$.

1. Bestimme aus diesen Angaben die Wellenlänge $\lambda$.  
2. Berechne daraus die Ausbreitungsgeschwindigkeit $c$ der Welle.



$ \lambda \approx $ [[ 3,28        ]] cm


@canvas

$ c \approx $ [[ 0,0273        ]] $\,\dfrac{\text{m}}{\text{s}}$
@Algebrite.check2(0.0273,0.01)
******************
$$
\begin{align*}
y(x;t) &= A \sin\!\left(
2\pi\left[
\frac{t}{T} - \frac{x}{\lambda}
\right]\right) \\[8pt]
\frac{y}{A}
&= \sin\!\left(
2\pi \left[
\frac{t}{T} - \frac{x}{\lambda}
\right]\right) \\[8pt]
\arcsin\!\left(\frac{y}{A}\right)
&= 2\pi \left[
\frac{t}{T} - \frac{x}{\lambda}
\right] \\[10pt]
\frac{1}{2\pi}\arcsin\!\left(\frac{y}{A}\right)
&= \frac{t}{T} - \frac{x}{\lambda}
\end{align*}
$$

Nach $\lambda$ umstellen:
$$
\frac{x}{\lambda}
= \frac{t}{T} - \frac{1}{2\pi}\arcsin\!\left(\frac{y}{A}\right)
\quad\Rightarrow\quad
\lambda
= \frac{x}{
\frac{t}{T} -
\frac{1}{2\pi}\arcsin\!\left(\frac{y}{A}\right)
}
$$

Zahlen einsetzen:  \
- $A = 12{,}0 \,\text{cm}$  \
- $y = 4{,}5 \,\text{cm}$  \
- $x = 8{,}0 \,\text{cm}$  \
- $t = 3{,}0 \,\text{s}$  \
- $T = 1{,}20 \,\text{s}$  \

$$
\frac{y}{A} = \frac{4{,}5}{12{,}0} = 0{,}375
\quad\Rightarrow\quad
\arcsin(0{,}375) \approx 0{,}3844 \,\text{rad}
$$

$$
\frac{1}{2\pi} \cdot 0{,}3844
\approx 0{,}06118
\quad,\quad
\frac{t}{T} = \frac{3{,}0}{1{,}20} = 2{,}50
$$

$$
\frac{x}{\lambda}
= 2{,}50 - 0{,}06118
= 2{,}43882
\quad\Rightarrow\quad
\lambda
= \frac{8{,}0 \,\text{cm}}{2{,}43882}
\approx 3{,}28 \,\text{cm}
$$

Die Ausbreitungsgeschwindigkeit $c$ ist
$$
c = \frac{\lambda}{T}
= \frac{3{,}28 \,\text{cm}}{1{,}20 \,\text{s}}
\approx 2{,}73 \,\frac{\text{cm}}{\text{s}}
= 2{,}73 \cdot 10^{-2} \,\frac{\text{m}}{\text{s}}
$$
******************

@canvas


---

---





__$d)\;\;$__ Physikalische Einordnung (Antwort in Worten, aber begründe mit Zahlen aus a)–c)):

- In Teilaufgabe a) hattest du $A = 1{,}5\,\text{cm}$, aber die berechnete momentane Auslenkung war nur $0{,}562\,\text{cm}$.  
  Warum ist $y$ kleiner als $A$?  
- In Teilaufgabe c) hast du gesehen, dass aus $\lambda$ und $T$ direkt die Ausbreitungsgeschwindigkeit $c$ folgt.  
  Erkläre in einem Satz, was $\lambda$ und $T$ physikalisch jeweils bedeuten und warum $c = \dfrac{\lambda}{T}$ sinnvoll ist.


[[!]]
<script>true</script>
******************
Amplitude $A$: größter möglicher Betrag der Auslenkung. \
Momentane Elongation $y$: aktueller Wert zu diesem Ort und Zeitpunkt. \
$\lambda$: räumliche Periode der Welle, 
$T$: zeitliche Periode der Welle. \
$\Rightarrow c = \frac{\lambda}{T}$ bedeutet: pro Schwingungsdauer T läuft die Wellenform eine Wellenlänge weiter.
******************


@canvas


















































































## Übungen an Graphen




Aufgabe 1: Es werden zwei Momentaufnahmen einer Welle miteinander verglichen.





<div style="max-width: 1000px">

``` javascript @JSX.Graph

// ✅ VOR initBoard: Container-Größe festlegen
jxgbox.style.width  = '100%';
jxgbox.style.height = '450px';

// optional, aber oft hilfreich gegen Lia/Wrapper-CSS:
jxgbox.style.minHeight = '450px';
jxgbox.style.maxHeight = '450px';
jxgbox.style.boxSizing = 'border-box';


function __getGridColor(fallback = '#0b5fff') {
  try {
    const doc = (window.parent && window.parent.document) ? window.parent.document : document;
    const win = (window.parent && window.parent.getComputedStyle) ? window.parent : window;

    // 1) Wenn du später mal --grid-color nutzt, wird das automatisch bevorzugt
    const v = win.getComputedStyle(doc.documentElement).getPropertyValue('--grid-color').trim();
    if (v) return v;

    // 2) Sonst Button-Farbe nehmen
    const btn = doc.querySelector('.lia-btn');
    if (btn) {
      const cs = win.getComputedStyle(btn);
      const bg = cs.backgroundColor;
      if (bg && bg !== 'rgba(0, 0, 0, 0)') return bg;
      if (cs.color) return cs.color;
    }
  } catch (e) {}

  return fallback;
}

// Board-Grid-Farbe live nachziehen
function __watchGridColor(board, intervalMs = 400) {
  let last = '';

  setInterval(() => {
    const c = __getGridColor('#0b5fff');
    if (!c || c === last) return;
    last = c;

    // 1) Optionen setzen (für zukünftige Rebuilds)
    try {
      if (board && board.options && board.options.grid) {
        if (board.options.grid.major) board.options.grid.major.strokeColor = c;
        if (board.options.grid.minor) board.options.grid.minor.strokeColor = c;
      }
    } catch (e) {}

    // 2) EXISTIERENDE Grid-Objekte einfärben (entscheidend!)
    try {
      if (board && board.grids && board.grids.length) {
        board.grids.forEach(g => {
          if (g && typeof g.setAttribute === 'function') {
            g.setAttribute({ strokeColor: c });
          }
        });
      }

      if (board && board.objectsList && board.objectsList.length) {
        board.objectsList.forEach(o => {
          if (!o || typeof o.setAttribute !== 'function') return;
          if (o.elType === 'grid' || (typeof JXG !== 'undefined' && o.type === JXG.OBJECT_TYPE_GRID)) {
            o.setAttribute({ strokeColor: c });
          }
        });
      }
    } catch (e) {}

    // 3) Redraw
    try {
      if (board && typeof board.fullUpdate === 'function') board.fullUpdate();
      else if (board) board.update();
    } catch (e) {}

  }, intervalMs);
}

const btnColor = __getGridColor('#0b5fff');

JXG.Options.text.useMathJax = true;



// Board HIER DIE KOORDINATEN
// Board HIER DIE KOORDINATEN
// Board HIER DIE KOORDINATEN
// Board HIER DIE KOORDINATEN
// Board HIER DIE KOORDINATEN
// Board HIER DIE KOORDINATEN
// Board HIER DIE KOORDINATEN
// Board HIER DIE KOORDINATEN
// Board HIER DIE KOORDINATEN

board = JXG.JSXGraph.initBoard(jxgbox, {
  axis: true,
  showNavigation: true,
  showCopyright: false,
  boundingbox: [-2, 3, 10, -3],
  keepaspectratio: true,

  zoom: {
    enabled: true,
    wheel: true,
    needShift: false,
    factorX: 1.15,
    factorY: 1.15
  },

  pan: {
    enabled: true,
    needShift: false,
    needTwoFingers: false
  },

  defaultAxes: {
    x: {
      strokeColor: 'black',
      strokeWidth: 2.5,
    name: '\(x\,\text{in}\,[m]\)',
    withLabel: true,
    label: { position: 'rt', offset: [-50, -25], fontSize: 18 },
      ticks: {
        insertTicks: false,
        ticksDistance: 1,
        strokeWidth: 3,
        minorTicks: 9,         
        drawLabels: true,
        label: { fontSize: 18 }
      }
    },
    y: {
      strokeColor: 'black',
      strokeWidth: 2.5,
    name: '\(y\,\text{in}\,[m]\)',
    withLabel: true,
    label: { position: 'rt', offset: [15, 0], fontSize: 18 },
      ticks: {
        insertTicks: false,
        ticksDistance: 1,
        strokeWidth: 3,
        minorTicks: 9,        
        drawLabels: true,
        label: { fontSize: 18 }
      }
    }
  },

  grid: {
    majorStep: 'auto',                
    minorElements: 'auto',          
    includeBoundaries: true,
    forceSquare: true,

    major: {
      face: 'line',
      strokeColor: btnColor,
      strokeWidth: 1.5,          
      dash: 0,
      drawZero: true
    },
    minor: {
      face: 'line',
      strokeColor: btnColor,
      strokeWidth: 1,         
      dash: 1,
      drawZero: false             // <<< spart Linien
    }
  }
});




/* =========================================================
   ADAPTIVE AXES + GRID (auto tick distance + grid rebuild)
   - passt bei Zoom/Pan automatisch:
     * ticksDistance (1-2-5-10 …)
     * minorTicks
     * label fontSize / drawLabels
     * Grid majorStep + minorElements
   ========================================================= */

(function adaptiveAxesAndGrid(board) {
  if (!board) return;

  // --- "nice number" für Tick-Abstände: 1,2,5 * 10^k
  function niceStep(raw) {
    if (!isFinite(raw) || raw <= 0) return 1;
    const exp = Math.floor(Math.log10(raw));
    const f = raw / Math.pow(10, exp);
    let nf;
    if (f <= 1) nf = 1;
    else if (f <= 2) nf = 2;
    else if (f <= 5) nf = 5;
    else nf = 10;
    return nf * Math.pow(10, exp);
  }

  function pxPerUnitX() {
    const bb = board.getBoundingBox(); // [xmin, ymax, xmax, ymin]
    const w = board.containerObj ? board.containerObj.clientWidth : (board.canvasWidth || 600);
    return w / Math.max(1e-9, (bb[2] - bb[0]));
  }

  function pxPerUnitY() {
    const bb = board.getBoundingBox();
    const h = board.containerObj ? board.containerObj.clientHeight : (board.canvasHeight || 400);
    return h / Math.max(1e-9, (bb[1] - bb[3]));
  }

  // --- Grid sauber neu bauen (weil majorStep/minorElements nicht in jeder JSXGraph-Version "live" wirken)
  function rebuildGrid(stepX, stepY, minorX, minorY) {
    const color = (window.readLiaBtnColor ? window.readLiaBtnColor('#0b5fff') : '#0b5fff');

    // existierende Grids entfernen
    try {
      if (board.grids && board.grids.length) {
        board.grids.slice().forEach(g => {
          try { board.removeObject(g); } catch (e) {}
        });
      }
    } catch (e) {}

    // neues Grid anlegen
    try {
      board.create('grid', [], {
        majorStep: [stepX, stepY],
        minorElements: [minorX, minorY],
        includeBoundaries: true,
        forceSquare: true,

        major: {
          face: 'line',
          strokeColor: color,
          strokeWidth: 1.5,
          dash: 0,
          drawZero: true
        },
        minor: {
          face: 'line',
          strokeColor: color,
          strokeWidth: 1,
          dash: 1,
          drawZero: false
        }
      });
    } catch (e) {}

    // danach ggf. direkt Theme-Farbe/Axis-Farbe nachziehen
    try { window.applyGridColor && window.applyGridColor(board, color); } catch (e) {}
    try { window.__applyAxisColors && window.__applyAxisColors(board); } catch (e) {}
  }

  // --- Achsenticks live anpassen
  function setAxisTicks(axisKey, step, minorTicks, fontSize, drawLabels) {
    try {
      const ax = board.defaultAxes && board.defaultAxes[axisKey];
      if (!ax) return;

      // Defaults für neu entstehende Ticks/Labels
      board.options = board.options || {};
      board.options.defaultAxes = board.options.defaultAxes || {};
      board.options.defaultAxes[axisKey] = board.options.defaultAxes[axisKey] || {};
      board.options.defaultAxes[axisKey].ticks = board.options.defaultAxes[axisKey].ticks || {};
      board.options.defaultAxes[axisKey].ticks.label = board.options.defaultAxes[axisKey].ticks.label || {};

      board.options.defaultAxes[axisKey].ticks.ticksDistance = step;
      board.options.defaultAxes[axisKey].ticks.minorTicks    = minorTicks;
      board.options.defaultAxes[axisKey].ticks.drawLabels    = !!drawLabels;
      board.options.defaultAxes[axisKey].ticks.label.fontSize = fontSize;

      // existierende Tick-Objekte aktualisieren
      const t = ax.defaultTicks;
      if (t && typeof t.setAttribute === 'function') {
        t.setAttribute({
          ticksDistance: step,
          minorTicks: minorTicks,
          drawLabels: !!drawLabels,
          label: { fontSize: fontSize }
        });
      }
    } catch (e) {}
  }

  // --- Zustand, damit wir nicht dauernd neu bauen
  let lastSig = '';

  function computeAndApply() {
    const ppuX = pxPerUnitX();
    const ppuY = pxPerUnitY();

    // Ziel: ca. 90px pro Major-Tick
    const targetPx = 90;

    const rawStepX = targetPx / Math.max(1e-9, ppuX);
    const rawStepY = targetPx / Math.max(1e-9, ppuY);

    const stepX = niceStep(rawStepX);
    const stepY = niceStep(rawStepY);

    // Minor-Logik: je größer der Step / je kleiner ppu, desto weniger Minor
    const minorX = (ppuX < 25 || stepX >= 10) ? 0 : (stepX >= 5 ? 4 : 9);
    const minorY = (ppuY < 25 || stepY >= 10) ? 0 : (stepY >= 5 ? 4 : 9);

    // Label-Logik: bei zu wenig Pixel pro Einheit Labels verkleinern / ausblenden
    let font = 18;
    let draw = true;
    const ppuMin = Math.min(ppuX, ppuY);
    if (ppuMin < 35) font = 14;
    if (ppuMin < 25) font = 12;
    if (ppuMin < 16) draw = 10;

    // Signatur – nur anwenden, wenn sich wirklich was geändert hat
    const sig = [stepX, stepY, minorX, minorY, font, draw].join('|');
    if (sig === lastSig) return;
    lastSig = sig;

    // Achsen
    setAxisTicks('x', stepX, minorX, font, draw);
    setAxisTicks('y', stepY, minorY, font, draw);

    // Grid (neu bauen)
    rebuildGrid(stepX, stepY, minorX, minorY);

    try {
      if (typeof board.fullUpdate === 'function') board.fullUpdate();
      else board.update();
    } catch (e) {}
  }

  // --- throttle über rAF, sonst boundingbox spammt hart
  let raf = 0;
  function schedule() {
    if (raf) return;
    raf = requestAnimationFrame(() => {
      raf = 0;
      computeAndApply();
    });
  }

  board.on('boundingbox', schedule);
  try { board.on('resize', schedule); } catch (e) {}

  // initial
  computeAndApply();
})(board);











// =========================================================
// Board ins gemeinsame ROOT registrieren
// =========================================================
const ROOT = (function () {
  try { let w = window; while (w.parent && w.parent !== w) w = w.parent; return w; }
  catch (e) { return window; }
})();

ROOT.__boards = ROOT.__boards || {};
ROOT.__boards['Aufgabe2'] = board;

// Pending Points nachziehen (falls vorher geklickt)
ROOT.__pendingPointSpecs = ROOT.__pendingPointSpecs || [];
ROOT.__pendingPointSpecs = ROOT.__pendingPointSpecs.filter(spec => {
  const parts = String(spec).split(';').map(s => String(s).trim());
  const bid = parts[0], name = parts[1];
  if (bid === 'Aufgabe2' && name) {
    // ensurePoint liegt im ROOT? -> über ROOT.window? meistens im gleichen Top-Level verfügbar.
    // Sicher: direkt im ROOT aufrufen, falls vorhanden.
    if (ROOT.ensurePoint) ROOT.ensurePoint(bid, name);
    else if (window.ensurePoint) window.ensurePoint(bid, name);
    return false;
  }
  return true;
});


function __isDarkTheme() {
  try {
    const doc = (window.parent && window.parent.document) ? window.parent.document : document;
    const win = (window.parent && window.parent.getComputedStyle) ? window.parent : window;

    // bevorzugt: body, sonst documentElement
    const el = doc.body || doc.documentElement;
    const bg = win.getComputedStyle(el).backgroundColor;

    // bg ist typischerweise "rgb(r,g,b)" oder "rgba(r,g,b,a)"
    const m = bg.match(/rgba?\((\d+),\s*(\d+),\s*(\d+)/i);
    if (!m) return false;

    const r = parseInt(m[1], 10);
    const g = parseInt(m[2], 10);
    const b = parseInt(m[3], 10);

    // relative Luminanz (0..255) – Schwelle ~ 128
    const lum = 0.2126 * r + 0.7152 * g + 0.0722 * b;
    return lum < 128;
  } catch (e) {
    return false;
  }
}


function __applyNavColors(board) {
  if (!board || !board.containerObj) return;

  // JSXGraph legt die Navigation innerhalb des Board-Containers an
  const nav = board.containerObj.querySelector('.JXG_navigation');
  if (!nav) return;

  const isDark = __isDarkTheme();
  const col = isDark ? '#fff' : '#000';

  // Navigation-Grundstil
  nav.style.color = col;
  nav.style.background = 'transparent';

  // Links/Buttons/Spans explizit einfärben
  nav.querySelectorAll('a, button, span').forEach(el => {
    el.style.color = col;
    el.style.borderColor = col;
    el.style.background = 'transparent';
    el.style.boxShadow = 'none';
  });

  // SVG-Icons (falls JSXGraph SVG nutzt)
  nav.querySelectorAll('svg, svg *').forEach(el => {
    el.style.fill = col;
    el.style.stroke = col;
  });

  // IMG-Icons (falls JSXGraph Bilder nutzt)
  nav.querySelectorAll('img').forEach(img => {
    img.style.filter = isDark ? 'invert(1)' : 'none';
  });
}

// einmal anwenden (nach initBoard)
__applyNavColors(board);

// bei Mode-Wechsel nachziehen
try {
  const mq = window.matchMedia('(prefers-color-scheme: dark)');
  if (mq && typeof mq.addEventListener === 'function') {
    mq.addEventListener('change', () => __applyNavColors(board));
  } else if (mq && typeof mq.addListener === 'function') {
    mq.addListener(() => __applyNavColors(board));
  }
} catch (e) {}


function __applyAxisColors(board) {
  if (!board) return;

  const isDark = __isDarkTheme();
  const col = isDark ? '#fff' : '#000';

  // 0) WICHTIG: Defaults für zukünftig neu erzeugte Tick-Labels setzen
  // (damit beim Rauszoomen neue Zahlen direkt korrekt gefärbt werden)
  try {
    board.options = board.options || {};
    board.options.defaultAxes = board.options.defaultAxes || {};
    ['x', 'y'].forEach(axKey => {
      board.options.defaultAxes[axKey] = board.options.defaultAxes[axKey] || {};
      board.options.defaultAxes[axKey].ticks = board.options.defaultAxes[axKey].ticks || {};
      board.options.defaultAxes[axKey].ticks.label = board.options.defaultAxes[axKey].ticks.label || {};

      board.options.defaultAxes[axKey].strokeColor = col;
      board.options.defaultAxes[axKey].ticks.strokeColor = col;

      // Diese beiden sind für die Ziffern entscheidend:
      board.options.defaultAxes[axKey].ticks.label.strokeColor = col;
      board.options.defaultAxes[axKey].ticks.label.fillColor   = col;
    });
  } catch (e) {}

  // Helfer: beliebige JSXGraph-Objekte einfärben
  const paint = (obj) => {
    if (!obj || typeof obj.setAttribute !== 'function') return;
    try {
      obj.setAttribute({
        strokeColor: col,
        highlightStrokeColor: col,
        fillColor: col,
        highlightFillColor: col
      });
    } catch (e) {}
  };

  // 1) Achsen + Ticks + Tick-Labels (existierende)
  try {
    if (board.defaultAxes) {
      if (board.defaultAxes.x && board.defaultAxes.x.label) paint(board.defaultAxes.x.label);
      if (board.defaultAxes.y && board.defaultAxes.y.label) paint(board.defaultAxes.y.label);

      const paintTicks = (axis) => {
        if (!axis) return;

        // Achsen-VisProps (wirkt oft auf neu erzeugte Ticks/Labels)
        try {
          axis.setAttribute({ strokeColor: col, highlightStrokeColor: col });
        } catch (e) {}

        // Standard-Ticks (häufig axis.defaultTicks)
        if (axis.defaultTicks) {
          paint(axis.defaultTicks);

          // Label-Default am Tick-Objekt selbst nachziehen
          try {
            axis.defaultTicks.setAttribute({
              strokeColor: col,
              highlightStrokeColor: col
            });
            if (axis.defaultTicks.visProp && axis.defaultTicks.visProp.label) {
              axis.defaultTicks.visProp.label.strokeColor = col;
              axis.defaultTicks.visProp.label.fillColor   = col;
            }
          } catch (e) {}

          if (axis.defaultTicks.labels && axis.defaultTicks.labels.length) {
            axis.defaultTicks.labels.forEach(paint);
          }
        }

        // Manche Versionen: axis.ticks als Array
        if (axis.ticks && axis.ticks.length) {
          axis.ticks.forEach(t => {
            paint(t);
            // Tick-Label-Defaults am Tick nachziehen
            try {
              if (t.visProp && t.visProp.label) {
                t.visProp.label.strokeColor = col;
                t.visProp.label.fillColor   = col;
              }
            } catch (e) {}
            if (t.labels && t.labels.length) t.labels.forEach(paint);
          });
        }

        // Manche Versionen: axis.getTicks()
        if (typeof axis.getTicks === 'function') {
          (axis.getTicks() || []).forEach(t => {
            paint(t);
            try {
              if (t.visProp && t.visProp.label) {
                t.visProp.label.strokeColor = col;
                t.visProp.label.fillColor   = col;
              }
            } catch (e) {}
            if (t.labels && t.labels.length) t.labels.forEach(paint);
          });
        }
      };

      paintTicks(board.defaultAxes.x);
      paintTicks(board.defaultAxes.y);
    }
  } catch (e) {}

  // 2) Fallback: Tick-Labels werden je nach Version als Textobjekte geführt.
  // Wir färben NUR Texte, die sehr wahrscheinlich Tick-Labels sind, um nicht alle Texte (z.B. Punktnamen) zu erwischen.
  try {
    if (board.objectsList && board.objectsList.length) {
      board.objectsList.forEach(o => {
        if (!o || o.elType !== 'text') return;

        // Heuristiken für Tick-Labels:
        // - Tick-Labels sind fast immer "fixed"
        // - und haben häufig sehr kurze Inhalte (Zahlen)
        // - und sind nicht "label" eines beliebigen Punktes (die sind oft an ein parent gekoppelt)
        const txt = (typeof o.getText === 'function') ? String(o.getText()) : (o.plaintext ? String(o.plaintext) : '');
        const looksNumeric = /^[\s\-+]*\d+([.,]\d+)?\s*$/.test(txt);

        const isFixed = (o.visProp && (o.visProp.fixed === true || o.visProp.isfixed === true));
        if (looksNumeric && isFixed) paint(o);
      });
    }
  } catch (e) {}

  // 3) Redraw
  try {
    if (typeof board.fullUpdate === 'function') board.fullUpdate();
    else board.update();
  } catch (e) {}
}

// einmal anwenden
__applyAxisColors(board);

// NEU: bei jedem Zoom/Pan (boundingbox ändert sich) Achsen/Ticks/Labels nachfärben
try {
  board.on('boundingbox', () => __applyAxisColors(board));
} catch (e) {}

// Optional (aber sinnvoll): auch nach Board-Resize einmal nachziehen
try {
  board.on('resize', () => __applyAxisColors(board));
} catch (e) {}


// einmal anwenden
__applyAxisColors(board);




function __applyBoardFrame(board) {
  if (!board || !board.containerObj) return;

  const isDark = __isDarkTheme();
  const col = isDark ? '#fff' : '#000';

  // Rahmen um das Koordinatensystem
  board.containerObj.style.border = `2px solid ${col}`;
  board.containerObj.style.borderRadius = '8px';     // optional
  board.containerObj.style.boxSizing = 'border-box';
}

// einmal anwenden
__applyBoardFrame(board);

// bei Mode-Wechsel nachziehen (gleiches Event wie Navigation nutzen)
try {
  const mq = window.matchMedia('(prefers-color-scheme: dark)');
  const handler = () => {
    __applyNavColors(board);
    __applyAxisColors(board);
  };

  if (mq && typeof mq.addEventListener === 'function') mq.addEventListener('change', handler);
  else if (mq && typeof mq.addListener === 'function') mq.addListener(handler);
} catch (e) {}



try {
  if (board && board.grids && board.grids.length) {
    board.grids.forEach(g => g && g.setAttribute && g.setAttribute({ strokeColor: btnColor }));
  }
} catch (e) {}


if (board && board.containerObj) {
  board.containerObj.style.background = 'transparent';
}

let __lastDark = null;

setInterval(() => {
  const nowDark = __isDarkTheme();
  if (nowDark === __lastDark) return;
  __lastDark = nowDark;

  __applyNavColors(board);
  __applyAxisColors(board);
  __applyBoardFrame(board);

  try { window.__recolorNeutralAutoLabels && window.__recolorNeutralAutoLabels(); } catch (e) {}
}, 300);


// Grid-Farbe automatisch an Button-Farbe koppeln
__watchGridColor(board, 400);


// f(x) = 2.5 * sin(8*x + π/2) Math.PI/2
var f = function(x){
  return 2.5 * Math.sin(2.64555170828614167*x);
};

// aktueller sichtbarer x-Bereich aus der Boundingbox holen
// getBoundingBox() liefert: [xmin, ymax, xmax, ymin]
var bb   = board.getBoundingBox();
var xmin = bb[4];
var xmax = bb[4];

// Graph
board.create('functiongraph', [f, xmin, xmax], {
  strokeWidth: 3,
  strokeColor: '#ff0000'
});




```

</div>












































<div style="max-width: 1000px">

``` javascript @JSX.Graph

// ✅ VOR initBoard: Container-Größe festlegen
jxgbox.style.width  = '100%';
jxgbox.style.height = '450px';

// optional, aber oft hilfreich gegen Lia/Wrapper-CSS:
jxgbox.style.minHeight = '450px';
jxgbox.style.maxHeight = '450px';
jxgbox.style.boxSizing = 'border-box';


function __getGridColor(fallback = '#0b5fff') {
  try {
    const doc = (window.parent && window.parent.document) ? window.parent.document : document;
    const win = (window.parent && window.parent.getComputedStyle) ? window.parent : window;

    // 1) Wenn du später mal --grid-color nutzt, wird das automatisch bevorzugt
    const v = win.getComputedStyle(doc.documentElement).getPropertyValue('--grid-color').trim();
    if (v) return v;

    // 2) Sonst Button-Farbe nehmen
    const btn = doc.querySelector('.lia-btn');
    if (btn) {
      const cs = win.getComputedStyle(btn);
      const bg = cs.backgroundColor;
      if (bg && bg !== 'rgba(0, 0, 0, 0)') return bg;
      if (cs.color) return cs.color;
    }
  } catch (e) {}

  return fallback;
}

// Board-Grid-Farbe live nachziehen
function __watchGridColor(board, intervalMs = 400) {
  let last = '';

  setInterval(() => {
    const c = __getGridColor('#0b5fff');
    if (!c || c === last) return;
    last = c;

    // 1) Optionen setzen (für zukünftige Rebuilds)
    try {
      if (board && board.options && board.options.grid) {
        if (board.options.grid.major) board.options.grid.major.strokeColor = c;
        if (board.options.grid.minor) board.options.grid.minor.strokeColor = c;
      }
    } catch (e) {}

    // 2) EXISTIERENDE Grid-Objekte einfärben (entscheidend!)
    try {
      if (board && board.grids && board.grids.length) {
        board.grids.forEach(g => {
          if (g && typeof g.setAttribute === 'function') {
            g.setAttribute({ strokeColor: c });
          }
        });
      }

      if (board && board.objectsList && board.objectsList.length) {
        board.objectsList.forEach(o => {
          if (!o || typeof o.setAttribute !== 'function') return;
          if (o.elType === 'grid' || (typeof JXG !== 'undefined' && o.type === JXG.OBJECT_TYPE_GRID)) {
            o.setAttribute({ strokeColor: c });
          }
        });
      }
    } catch (e) {}

    // 3) Redraw
    try {
      if (board && typeof board.fullUpdate === 'function') board.fullUpdate();
      else if (board) board.update();
    } catch (e) {}

  }, intervalMs);
}

const btnColor = __getGridColor('#0b5fff');

JXG.Options.text.useMathJax = true;



// Board HIER DIE KOORDINATEN
// Board HIER DIE KOORDINATEN
// Board HIER DIE KOORDINATEN
// Board HIER DIE KOORDINATEN
// Board HIER DIE KOORDINATEN
// Board HIER DIE KOORDINATEN
// Board HIER DIE KOORDINATEN
// Board HIER DIE KOORDINATEN
// Board HIER DIE KOORDINATEN

board = JXG.JSXGraph.initBoard(jxgbox, {
  axis: true,
  showNavigation: true,
  showCopyright: false,
  boundingbox: [-2, 3, 10, -3],
  keepaspectratio: true,

  zoom: {
    enabled: true,
    wheel: true,
    needShift: false,
    factorX: 1.15,
    factorY: 1.15
  },

  pan: {
    enabled: true,
    needShift: false,
    needTwoFingers: false
  },

  defaultAxes: {
    x: {
      strokeColor: 'black',
      strokeWidth: 2.5,
    name: '\(x\,\text{in}\,[m]\)',
    withLabel: true,
    label: { position: 'rt', offset: [-50, -25], fontSize: 18 },
      ticks: {
        insertTicks: false,
        ticksDistance: 1,
        strokeWidth: 3,
        minorTicks: 9,         
        drawLabels: true,
        label: { fontSize: 18 }
      }
    },
    y: {
      strokeColor: 'black',
      strokeWidth: 2.5,
    name: '\(y\,\text{in}\,[m]\)',
    withLabel: true,
    label: { position: 'rt', offset: [15, 0], fontSize: 18 },
      ticks: {
        insertTicks: false,
        ticksDistance: 1,
        strokeWidth: 3,
        minorTicks: 9,        
        drawLabels: true,
        label: { fontSize: 18 }
      }
    }
  },

  grid: {
    majorStep: 'auto',                
    minorElements: 'auto',          
    includeBoundaries: true,
    forceSquare: true,

    major: {
      face: 'line',
      strokeColor: btnColor,
      strokeWidth: 1.5,          
      dash: 0,
      drawZero: true
    },
    minor: {
      face: 'line',
      strokeColor: btnColor,
      strokeWidth: 1,         
      dash: 1,
      drawZero: false             // <<< spart Linien
    }
  }
});




/* =========================================================
   ADAPTIVE AXES + GRID (auto tick distance + grid rebuild)
   - passt bei Zoom/Pan automatisch:
     * ticksDistance (1-2-5-10 …)
     * minorTicks
     * label fontSize / drawLabels
     * Grid majorStep + minorElements
   ========================================================= */

(function adaptiveAxesAndGrid(board) {
  if (!board) return;

  // --- "nice number" für Tick-Abstände: 1,2,5 * 10^k
  function niceStep(raw) {
    if (!isFinite(raw) || raw <= 0) return 1;
    const exp = Math.floor(Math.log10(raw));
    const f = raw / Math.pow(10, exp);
    let nf;
    if (f <= 1) nf = 1;
    else if (f <= 2) nf = 2;
    else if (f <= 5) nf = 5;
    else nf = 10;
    return nf * Math.pow(10, exp);
  }

  function pxPerUnitX() {
    const bb = board.getBoundingBox(); // [xmin, ymax, xmax, ymin]
    const w = board.containerObj ? board.containerObj.clientWidth : (board.canvasWidth || 600);
    return w / Math.max(1e-9, (bb[2] - bb[0]));
  }

  function pxPerUnitY() {
    const bb = board.getBoundingBox();
    const h = board.containerObj ? board.containerObj.clientHeight : (board.canvasHeight || 400);
    return h / Math.max(1e-9, (bb[1] - bb[3]));
  }

  // --- Grid sauber neu bauen (weil majorStep/minorElements nicht in jeder JSXGraph-Version "live" wirken)
  function rebuildGrid(stepX, stepY, minorX, minorY) {
    const color = (window.readLiaBtnColor ? window.readLiaBtnColor('#0b5fff') : '#0b5fff');

    // existierende Grids entfernen
    try {
      if (board.grids && board.grids.length) {
        board.grids.slice().forEach(g => {
          try { board.removeObject(g); } catch (e) {}
        });
      }
    } catch (e) {}

    // neues Grid anlegen
    try {
      board.create('grid', [], {
        majorStep: [stepX, stepY],
        minorElements: [minorX, minorY],
        includeBoundaries: true,
        forceSquare: true,

        major: {
          face: 'line',
          strokeColor: color,
          strokeWidth: 1.5,
          dash: 0,
          drawZero: true
        },
        minor: {
          face: 'line',
          strokeColor: color,
          strokeWidth: 1,
          dash: 1,
          drawZero: false
        }
      });
    } catch (e) {}

    // danach ggf. direkt Theme-Farbe/Axis-Farbe nachziehen
    try { window.applyGridColor && window.applyGridColor(board, color); } catch (e) {}
    try { window.__applyAxisColors && window.__applyAxisColors(board); } catch (e) {}
  }

  // --- Achsenticks live anpassen
  function setAxisTicks(axisKey, step, minorTicks, fontSize, drawLabels) {
    try {
      const ax = board.defaultAxes && board.defaultAxes[axisKey];
      if (!ax) return;

      // Defaults für neu entstehende Ticks/Labels
      board.options = board.options || {};
      board.options.defaultAxes = board.options.defaultAxes || {};
      board.options.defaultAxes[axisKey] = board.options.defaultAxes[axisKey] || {};
      board.options.defaultAxes[axisKey].ticks = board.options.defaultAxes[axisKey].ticks || {};
      board.options.defaultAxes[axisKey].ticks.label = board.options.defaultAxes[axisKey].ticks.label || {};

      board.options.defaultAxes[axisKey].ticks.ticksDistance = step;
      board.options.defaultAxes[axisKey].ticks.minorTicks    = minorTicks;
      board.options.defaultAxes[axisKey].ticks.drawLabels    = !!drawLabels;
      board.options.defaultAxes[axisKey].ticks.label.fontSize = fontSize;

      // existierende Tick-Objekte aktualisieren
      const t = ax.defaultTicks;
      if (t && typeof t.setAttribute === 'function') {
        t.setAttribute({
          ticksDistance: step,
          minorTicks: minorTicks,
          drawLabels: !!drawLabels,
          label: { fontSize: fontSize }
        });
      }
    } catch (e) {}
  }

  // --- Zustand, damit wir nicht dauernd neu bauen
  let lastSig = '';

  function computeAndApply() {
    const ppuX = pxPerUnitX();
    const ppuY = pxPerUnitY();

    // Ziel: ca. 90px pro Major-Tick
    const targetPx = 90;

    const rawStepX = targetPx / Math.max(1e-9, ppuX);
    const rawStepY = targetPx / Math.max(1e-9, ppuY);

    const stepX = niceStep(rawStepX);
    const stepY = niceStep(rawStepY);

    // Minor-Logik: je größer der Step / je kleiner ppu, desto weniger Minor
    const minorX = (ppuX < 25 || stepX >= 10) ? 0 : (stepX >= 5 ? 4 : 9);
    const minorY = (ppuY < 25 || stepY >= 10) ? 0 : (stepY >= 5 ? 4 : 9);

    // Label-Logik: bei zu wenig Pixel pro Einheit Labels verkleinern / ausblenden
    let font = 18;
    let draw = true;
    const ppuMin = Math.min(ppuX, ppuY);
    if (ppuMin < 35) font = 14;
    if (ppuMin < 25) font = 12;
    if (ppuMin < 16) draw = 10;

    // Signatur – nur anwenden, wenn sich wirklich was geändert hat
    const sig = [stepX, stepY, minorX, minorY, font, draw].join('|');
    if (sig === lastSig) return;
    lastSig = sig;

    // Achsen
    setAxisTicks('x', stepX, minorX, font, draw);
    setAxisTicks('y', stepY, minorY, font, draw);

    // Grid (neu bauen)
    rebuildGrid(stepX, stepY, minorX, minorY);

    try {
      if (typeof board.fullUpdate === 'function') board.fullUpdate();
      else board.update();
    } catch (e) {}
  }

  // --- throttle über rAF, sonst boundingbox spammt hart
  let raf = 0;
  function schedule() {
    if (raf) return;
    raf = requestAnimationFrame(() => {
      raf = 0;
      computeAndApply();
    });
  }

  board.on('boundingbox', schedule);
  try { board.on('resize', schedule); } catch (e) {}

  // initial
  computeAndApply();
})(board);











// =========================================================
// Board ins gemeinsame ROOT registrieren
// =========================================================
const ROOT = (function () {
  try { let w = window; while (w.parent && w.parent !== w) w = w.parent; return w; }
  catch (e) { return window; }
})();

ROOT.__boards = ROOT.__boards || {};
ROOT.__boards['Aufgabe2'] = board;

// Pending Points nachziehen (falls vorher geklickt)
ROOT.__pendingPointSpecs = ROOT.__pendingPointSpecs || [];
ROOT.__pendingPointSpecs = ROOT.__pendingPointSpecs.filter(spec => {
  const parts = String(spec).split(';').map(s => String(s).trim());
  const bid = parts[0], name = parts[1];
  if (bid === 'Aufgabe2' && name) {
    // ensurePoint liegt im ROOT? -> über ROOT.window? meistens im gleichen Top-Level verfügbar.
    // Sicher: direkt im ROOT aufrufen, falls vorhanden.
    if (ROOT.ensurePoint) ROOT.ensurePoint(bid, name);
    else if (window.ensurePoint) window.ensurePoint(bid, name);
    return false;
  }
  return true;
});


function __isDarkTheme() {
  try {
    const doc = (window.parent && window.parent.document) ? window.parent.document : document;
    const win = (window.parent && window.parent.getComputedStyle) ? window.parent : window;

    // bevorzugt: body, sonst documentElement
    const el = doc.body || doc.documentElement;
    const bg = win.getComputedStyle(el).backgroundColor;

    // bg ist typischerweise "rgb(r,g,b)" oder "rgba(r,g,b,a)"
    const m = bg.match(/rgba?\((\d+),\s*(\d+),\s*(\d+)/i);
    if (!m) return false;

    const r = parseInt(m[1], 10);
    const g = parseInt(m[2], 10);
    const b = parseInt(m[3], 10);

    // relative Luminanz (0..255) – Schwelle ~ 128
    const lum = 0.2126 * r + 0.7152 * g + 0.0722 * b;
    return lum < 128;
  } catch (e) {
    return false;
  }
}


function __applyNavColors(board) {
  if (!board || !board.containerObj) return;

  // JSXGraph legt die Navigation innerhalb des Board-Containers an
  const nav = board.containerObj.querySelector('.JXG_navigation');
  if (!nav) return;

  const isDark = __isDarkTheme();
  const col = isDark ? '#fff' : '#000';

  // Navigation-Grundstil
  nav.style.color = col;
  nav.style.background = 'transparent';

  // Links/Buttons/Spans explizit einfärben
  nav.querySelectorAll('a, button, span').forEach(el => {
    el.style.color = col;
    el.style.borderColor = col;
    el.style.background = 'transparent';
    el.style.boxShadow = 'none';
  });

  // SVG-Icons (falls JSXGraph SVG nutzt)
  nav.querySelectorAll('svg, svg *').forEach(el => {
    el.style.fill = col;
    el.style.stroke = col;
  });

  // IMG-Icons (falls JSXGraph Bilder nutzt)
  nav.querySelectorAll('img').forEach(img => {
    img.style.filter = isDark ? 'invert(1)' : 'none';
  });
}

// einmal anwenden (nach initBoard)
__applyNavColors(board);

// bei Mode-Wechsel nachziehen
try {
  const mq = window.matchMedia('(prefers-color-scheme: dark)');
  if (mq && typeof mq.addEventListener === 'function') {
    mq.addEventListener('change', () => __applyNavColors(board));
  } else if (mq && typeof mq.addListener === 'function') {
    mq.addListener(() => __applyNavColors(board));
  }
} catch (e) {}


function __applyAxisColors(board) {
  if (!board) return;

  const isDark = __isDarkTheme();
  const col = isDark ? '#fff' : '#000';

  // 0) WICHTIG: Defaults für zukünftig neu erzeugte Tick-Labels setzen
  // (damit beim Rauszoomen neue Zahlen direkt korrekt gefärbt werden)
  try {
    board.options = board.options || {};
    board.options.defaultAxes = board.options.defaultAxes || {};
    ['x', 'y'].forEach(axKey => {
      board.options.defaultAxes[axKey] = board.options.defaultAxes[axKey] || {};
      board.options.defaultAxes[axKey].ticks = board.options.defaultAxes[axKey].ticks || {};
      board.options.defaultAxes[axKey].ticks.label = board.options.defaultAxes[axKey].ticks.label || {};

      board.options.defaultAxes[axKey].strokeColor = col;
      board.options.defaultAxes[axKey].ticks.strokeColor = col;

      // Diese beiden sind für die Ziffern entscheidend:
      board.options.defaultAxes[axKey].ticks.label.strokeColor = col;
      board.options.defaultAxes[axKey].ticks.label.fillColor   = col;
    });
  } catch (e) {}

  // Helfer: beliebige JSXGraph-Objekte einfärben
  const paint = (obj) => {
    if (!obj || typeof obj.setAttribute !== 'function') return;
    try {
      obj.setAttribute({
        strokeColor: col,
        highlightStrokeColor: col,
        fillColor: col,
        highlightFillColor: col
      });
    } catch (e) {}
  };

  // 1) Achsen + Ticks + Tick-Labels (existierende)
  try {
    if (board.defaultAxes) {
      if (board.defaultAxes.x && board.defaultAxes.x.label) paint(board.defaultAxes.x.label);
      if (board.defaultAxes.y && board.defaultAxes.y.label) paint(board.defaultAxes.y.label);

      const paintTicks = (axis) => {
        if (!axis) return;

        // Achsen-VisProps (wirkt oft auf neu erzeugte Ticks/Labels)
        try {
          axis.setAttribute({ strokeColor: col, highlightStrokeColor: col });
        } catch (e) {}

        // Standard-Ticks (häufig axis.defaultTicks)
        if (axis.defaultTicks) {
          paint(axis.defaultTicks);

          // Label-Default am Tick-Objekt selbst nachziehen
          try {
            axis.defaultTicks.setAttribute({
              strokeColor: col,
              highlightStrokeColor: col
            });
            if (axis.defaultTicks.visProp && axis.defaultTicks.visProp.label) {
              axis.defaultTicks.visProp.label.strokeColor = col;
              axis.defaultTicks.visProp.label.fillColor   = col;
            }
          } catch (e) {}

          if (axis.defaultTicks.labels && axis.defaultTicks.labels.length) {
            axis.defaultTicks.labels.forEach(paint);
          }
        }

        // Manche Versionen: axis.ticks als Array
        if (axis.ticks && axis.ticks.length) {
          axis.ticks.forEach(t => {
            paint(t);
            // Tick-Label-Defaults am Tick nachziehen
            try {
              if (t.visProp && t.visProp.label) {
                t.visProp.label.strokeColor = col;
                t.visProp.label.fillColor   = col;
              }
            } catch (e) {}
            if (t.labels && t.labels.length) t.labels.forEach(paint);
          });
        }

        // Manche Versionen: axis.getTicks()
        if (typeof axis.getTicks === 'function') {
          (axis.getTicks() || []).forEach(t => {
            paint(t);
            try {
              if (t.visProp && t.visProp.label) {
                t.visProp.label.strokeColor = col;
                t.visProp.label.fillColor   = col;
              }
            } catch (e) {}
            if (t.labels && t.labels.length) t.labels.forEach(paint);
          });
        }
      };

      paintTicks(board.defaultAxes.x);
      paintTicks(board.defaultAxes.y);
    }
  } catch (e) {}

  // 2) Fallback: Tick-Labels werden je nach Version als Textobjekte geführt.
  // Wir färben NUR Texte, die sehr wahrscheinlich Tick-Labels sind, um nicht alle Texte (z.B. Punktnamen) zu erwischen.
  try {
    if (board.objectsList && board.objectsList.length) {
      board.objectsList.forEach(o => {
        if (!o || o.elType !== 'text') return;

        // Heuristiken für Tick-Labels:
        // - Tick-Labels sind fast immer "fixed"
        // - und haben häufig sehr kurze Inhalte (Zahlen)
        // - und sind nicht "label" eines beliebigen Punktes (die sind oft an ein parent gekoppelt)
        const txt = (typeof o.getText === 'function') ? String(o.getText()) : (o.plaintext ? String(o.plaintext) : '');
        const looksNumeric = /^[\s\-+]*\d+([.,]\d+)?\s*$/.test(txt);

        const isFixed = (o.visProp && (o.visProp.fixed === true || o.visProp.isfixed === true));
        if (looksNumeric && isFixed) paint(o);
      });
    }
  } catch (e) {}

  // 3) Redraw
  try {
    if (typeof board.fullUpdate === 'function') board.fullUpdate();
    else board.update();
  } catch (e) {}
}

// einmal anwenden
__applyAxisColors(board);

// NEU: bei jedem Zoom/Pan (boundingbox ändert sich) Achsen/Ticks/Labels nachfärben
try {
  board.on('boundingbox', () => __applyAxisColors(board));
} catch (e) {}

// Optional (aber sinnvoll): auch nach Board-Resize einmal nachziehen
try {
  board.on('resize', () => __applyAxisColors(board));
} catch (e) {}


// einmal anwenden
__applyAxisColors(board);




function __applyBoardFrame(board) {
  if (!board || !board.containerObj) return;

  const isDark = __isDarkTheme();
  const col = isDark ? '#fff' : '#000';

  // Rahmen um das Koordinatensystem
  board.containerObj.style.border = `2px solid ${col}`;
  board.containerObj.style.borderRadius = '8px';     // optional
  board.containerObj.style.boxSizing = 'border-box';
}

// einmal anwenden
__applyBoardFrame(board);

// bei Mode-Wechsel nachziehen (gleiches Event wie Navigation nutzen)
try {
  const mq = window.matchMedia('(prefers-color-scheme: dark)');
  const handler = () => {
    __applyNavColors(board);
    __applyAxisColors(board);
  };

  if (mq && typeof mq.addEventListener === 'function') mq.addEventListener('change', handler);
  else if (mq && typeof mq.addListener === 'function') mq.addListener(handler);
} catch (e) {}



try {
  if (board && board.grids && board.grids.length) {
    board.grids.forEach(g => g && g.setAttribute && g.setAttribute({ strokeColor: btnColor }));
  }
} catch (e) {}


if (board && board.containerObj) {
  board.containerObj.style.background = 'transparent';
}

let __lastDark = null;

setInterval(() => {
  const nowDark = __isDarkTheme();
  if (nowDark === __lastDark) return;
  __lastDark = nowDark;

  __applyNavColors(board);
  __applyAxisColors(board);
  __applyBoardFrame(board);

  try { window.__recolorNeutralAutoLabels && window.__recolorNeutralAutoLabels(); } catch (e) {}
}, 300);


// Grid-Farbe automatisch an Button-Farbe koppeln
__watchGridColor(board, 400);


// f(x) = 2.5 * sin(8*x + π/2)
var f = function(x){
  return 2.5 * Math.sin(2.64555170828614167*x - 2);
};

// aktueller sichtbarer x-Bereich aus der Boundingbox holen
// getBoundingBox() liefert: [xmin, ymax, xmax, ymin]
var bb   = board.getBoundingBox();
var xmin = bb[4];
var xmax = bb[4];

// Graph
board.create('functiongraph', [f, xmin, xmax], {
  strokeWidth: 3,
  strokeColor: '#ff0000'
});




```

</div>






__$a)\;\;$__ Gib die Amplitude der Welle an.


$ A = $ [[ 2,5        ]] $\,\text{m}$
@Algebrite.check2(2.5,0.01)

@canvas

__$b)\;\;$__ Gib die Wellenlänge der Welle an.


$ \lambda = $ [[ 2,375        ]] $\,\text{m}$
@Algebrite.check2(2.375,0.001)


@canvas

__$c)\;\;$__ Zwischen den Aufnahmen liegen $4\,$s und es wurde nur eine minimale Veränderung dokumentiert. Gib die Periodendauer der Welle an.


$ T = $ [[ 12,566        ]] $\,\text{s}$
@Algebrite.check2(12.566,0.05)
******************

Dreisatz

<!-- data-type="none" 
data-sortable="false" 
style="width:320px" -->
|$x$ in [m]| $t$ in [s]|
|:-----:|:---:|
|   0,756   | 4 |
|   1   | 5,291 |
|  2,375   | 12,566 |

mit: $0,756 \cdot \dfrac{1}{0,756} = 1 \;\;\Rightarrow\;\; 4 \cdot \dfrac{1}{0,756} \approx 5,291 $

******************


@canvas

__$d)\;\;$__ Gib die Ausbreitungsgeschwindigkeit der Welle an.


$ c = $ [[ 0,189        ]] $\,\dfrac{\text{m}}{\text{s}}$
@Algebrite.check2(0.1889999999,0.05)
******************

$c = \dfrac{\lambda}{T} \approx 0,189 \,\dfrac{\text{m}}{\text{s}}$

******************

@canvas





























































































## Übungen an Graphen




**Aufgabe 1:** Erläutere anhand des Graphens, was durch den Graphen dargestellt werden sein könnte.





<div style="max-width: 1000px">

``` javascript @JSX.Graph

// ✅ VOR initBoard: Container-Größe festlegen
jxgbox.style.width  = '100%';
jxgbox.style.height = '450px';

// optional, aber oft hilfreich gegen Lia/Wrapper-CSS:
jxgbox.style.minHeight = '450px';
jxgbox.style.maxHeight = '450px';
jxgbox.style.boxSizing = 'border-box';


function __getGridColor(fallback = '#0b5fff') {
  try {
    const doc = (window.parent && window.parent.document) ? window.parent.document : document;
    const win = (window.parent && window.parent.getComputedStyle) ? window.parent : window;

    // 1) Wenn du später mal --grid-color nutzt, wird das automatisch bevorzugt
    const v = win.getComputedStyle(doc.documentElement).getPropertyValue('--grid-color').trim();
    if (v) return v;

    // 2) Sonst Button-Farbe nehmen
    const btn = doc.querySelector('.lia-btn');
    if (btn) {
      const cs = win.getComputedStyle(btn);
      const bg = cs.backgroundColor;
      if (bg && bg !== 'rgba(0, 0, 0, 0)') return bg;
      if (cs.color) return cs.color;
    }
  } catch (e) {}

  return fallback;
}

// Board-Grid-Farbe live nachziehen
function __watchGridColor(board, intervalMs = 400) {
  let last = '';

  setInterval(() => {
    const c = __getGridColor('#0b5fff');
    if (!c || c === last) return;
    last = c;

    // 1) Optionen setzen (für zukünftige Rebuilds)
    try {
      if (board && board.options && board.options.grid) {
        if (board.options.grid.major) board.options.grid.major.strokeColor = c;
        if (board.options.grid.minor) board.options.grid.minor.strokeColor = c;
      }
    } catch (e) {}

    // 2) EXISTIERENDE Grid-Objekte einfärben (entscheidend!)
    try {
      if (board && board.grids && board.grids.length) {
        board.grids.forEach(g => {
          if (g && typeof g.setAttribute === 'function') {
            g.setAttribute({ strokeColor: c });
          }
        });
      }

      if (board && board.objectsList && board.objectsList.length) {
        board.objectsList.forEach(o => {
          if (!o || typeof o.setAttribute !== 'function') return;
          if (o.elType === 'grid' || (typeof JXG !== 'undefined' && o.type === JXG.OBJECT_TYPE_GRID)) {
            o.setAttribute({ strokeColor: c });
          }
        });
      }
    } catch (e) {}

    // 3) Redraw
    try {
      if (board && typeof board.fullUpdate === 'function') board.fullUpdate();
      else if (board) board.update();
    } catch (e) {}

  }, intervalMs);
}

const btnColor = __getGridColor('#0b5fff');

JXG.Options.text.useMathJax = true;



// Board HIER DIE KOORDINATEN
// Board HIER DIE KOORDINATEN
// Board HIER DIE KOORDINATEN
// Board HIER DIE KOORDINATEN
// Board HIER DIE KOORDINATEN
// Board HIER DIE KOORDINATEN
// Board HIER DIE KOORDINATEN
// Board HIER DIE KOORDINATEN
// Board HIER DIE KOORDINATEN

board = JXG.JSXGraph.initBoard(jxgbox, {
  axis: true,
  showNavigation: true,
  showCopyright: false,
  boundingbox: [-2, 3, 10, -3],
  keepaspectratio: true,

  zoom: {
    enabled: true,
    wheel: true,
    needShift: false,
    factorX: 1.15,
    factorY: 1.15
  },

  pan: {
    enabled: true,
    needShift: false,
    needTwoFingers: false
  },

  defaultAxes: {
    x: {
      strokeColor: 'black',
      strokeWidth: 2.5,
    name: '\(t\,\text{in}\,[s]\)',
    withLabel: true,
    label: { position: 'rt', offset: [-50, -25], fontSize: 18 },
      ticks: {
        insertTicks: false,
        ticksDistance: 1,
        strokeWidth: 3,
        minorTicks: 9,         
        drawLabels: true,
        label: { fontSize: 18 }
      }
    },
    y: {
      strokeColor: 'black',
      strokeWidth: 2.5,
    name: '\(y\,\text{in}\,[m]\)',
    withLabel: true,
    label: { position: 'rt', offset: [15, 0], fontSize: 18 },
      ticks: {
        insertTicks: false,
        ticksDistance: 1,
        strokeWidth: 3,
        minorTicks: 9,        
        drawLabels: true,
        label: { fontSize: 18 }
      }
    }
  },

  grid: {
    majorStep: 'auto',                
    minorElements: 'auto',          
    includeBoundaries: true,
    forceSquare: true,

    major: {
      face: 'line',
      strokeColor: btnColor,
      strokeWidth: 1.5,          
      dash: 0,
      drawZero: true
    },
    minor: {
      face: 'line',
      strokeColor: btnColor,
      strokeWidth: 1,         
      dash: 1,
      drawZero: false             // <<< spart Linien
    }
  }
});




/* =========================================================
   ADAPTIVE AXES + GRID (auto tick distance + grid rebuild)
   - passt bei Zoom/Pan automatisch:
     * ticksDistance (1-2-5-10 …)
     * minorTicks
     * label fontSize / drawLabels
     * Grid majorStep + minorElements
   ========================================================= */

(function adaptiveAxesAndGrid(board) {
  if (!board) return;

  // --- "nice number" für Tick-Abstände: 1,2,5 * 10^k
  function niceStep(raw) {
    if (!isFinite(raw) || raw <= 0) return 1;
    const exp = Math.floor(Math.log10(raw));
    const f = raw / Math.pow(10, exp);
    let nf;
    if (f <= 1) nf = 1;
    else if (f <= 2) nf = 2;
    else if (f <= 5) nf = 5;
    else nf = 10;
    return nf * Math.pow(10, exp);
  }

  function pxPerUnitX() {
    const bb = board.getBoundingBox(); // [xmin, ymax, xmax, ymin]
    const w = board.containerObj ? board.containerObj.clientWidth : (board.canvasWidth || 600);
    return w / Math.max(1e-9, (bb[2] - bb[0]));
  }

  function pxPerUnitY() {
    const bb = board.getBoundingBox();
    const h = board.containerObj ? board.containerObj.clientHeight : (board.canvasHeight || 400);
    return h / Math.max(1e-9, (bb[1] - bb[3]));
  }

  // --- Grid sauber neu bauen (weil majorStep/minorElements nicht in jeder JSXGraph-Version "live" wirken)
  function rebuildGrid(stepX, stepY, minorX, minorY) {
    const color = (window.readLiaBtnColor ? window.readLiaBtnColor('#0b5fff') : '#0b5fff');

    // existierende Grids entfernen
    try {
      if (board.grids && board.grids.length) {
        board.grids.slice().forEach(g => {
          try { board.removeObject(g); } catch (e) {}
        });
      }
    } catch (e) {}

    // neues Grid anlegen
    try {
      board.create('grid', [], {
        majorStep: [stepX, stepY],
        minorElements: [minorX, minorY],
        includeBoundaries: true,
        forceSquare: true,

        major: {
          face: 'line',
          strokeColor: color,
          strokeWidth: 1.5,
          dash: 0,
          drawZero: true
        },
        minor: {
          face: 'line',
          strokeColor: color,
          strokeWidth: 1,
          dash: 1,
          drawZero: false
        }
      });
    } catch (e) {}

    // danach ggf. direkt Theme-Farbe/Axis-Farbe nachziehen
    try { window.applyGridColor && window.applyGridColor(board, color); } catch (e) {}
    try { window.__applyAxisColors && window.__applyAxisColors(board); } catch (e) {}
  }

  // --- Achsenticks live anpassen
  function setAxisTicks(axisKey, step, minorTicks, fontSize, drawLabels) {
    try {
      const ax = board.defaultAxes && board.defaultAxes[axisKey];
      if (!ax) return;

      // Defaults für neu entstehende Ticks/Labels
      board.options = board.options || {};
      board.options.defaultAxes = board.options.defaultAxes || {};
      board.options.defaultAxes[axisKey] = board.options.defaultAxes[axisKey] || {};
      board.options.defaultAxes[axisKey].ticks = board.options.defaultAxes[axisKey].ticks || {};
      board.options.defaultAxes[axisKey].ticks.label = board.options.defaultAxes[axisKey].ticks.label || {};

      board.options.defaultAxes[axisKey].ticks.ticksDistance = step;
      board.options.defaultAxes[axisKey].ticks.minorTicks    = minorTicks;
      board.options.defaultAxes[axisKey].ticks.drawLabels    = !!drawLabels;
      board.options.defaultAxes[axisKey].ticks.label.fontSize = fontSize;

      // existierende Tick-Objekte aktualisieren
      const t = ax.defaultTicks;
      if (t && typeof t.setAttribute === 'function') {
        t.setAttribute({
          ticksDistance: step,
          minorTicks: minorTicks,
          drawLabels: !!drawLabels,
          label: { fontSize: fontSize }
        });
      }
    } catch (e) {}
  }

  // --- Zustand, damit wir nicht dauernd neu bauen
  let lastSig = '';

  function computeAndApply() {
    const ppuX = pxPerUnitX();
    const ppuY = pxPerUnitY();

    // Ziel: ca. 90px pro Major-Tick
    const targetPx = 90;

    const rawStepX = targetPx / Math.max(1e-9, ppuX);
    const rawStepY = targetPx / Math.max(1e-9, ppuY);

    const stepX = niceStep(rawStepX);
    const stepY = niceStep(rawStepY);

    // Minor-Logik: je größer der Step / je kleiner ppu, desto weniger Minor
    const minorX = (ppuX < 25 || stepX >= 10) ? 0 : (stepX >= 5 ? 4 : 9);
    const minorY = (ppuY < 25 || stepY >= 10) ? 0 : (stepY >= 5 ? 4 : 9);

    // Label-Logik: bei zu wenig Pixel pro Einheit Labels verkleinern / ausblenden
    let font = 18;
    let draw = true;
    const ppuMin = Math.min(ppuX, ppuY);
    if (ppuMin < 35) font = 14;
    if (ppuMin < 25) font = 12;
    if (ppuMin < 16) draw = 10;

    // Signatur – nur anwenden, wenn sich wirklich was geändert hat
    const sig = [stepX, stepY, minorX, minorY, font, draw].join('|');
    if (sig === lastSig) return;
    lastSig = sig;

    // Achsen
    setAxisTicks('x', stepX, minorX, font, draw);
    setAxisTicks('y', stepY, minorY, font, draw);

    // Grid (neu bauen)
    rebuildGrid(stepX, stepY, minorX, minorY);

    try {
      if (typeof board.fullUpdate === 'function') board.fullUpdate();
      else board.update();
    } catch (e) {}
  }

  // --- throttle über rAF, sonst boundingbox spammt hart
  let raf = 0;
  function schedule() {
    if (raf) return;
    raf = requestAnimationFrame(() => {
      raf = 0;
      computeAndApply();
    });
  }

  board.on('boundingbox', schedule);
  try { board.on('resize', schedule); } catch (e) {}

  // initial
  computeAndApply();
})(board);











// =========================================================
// Board ins gemeinsame ROOT registrieren
// =========================================================
const ROOT = (function () {
  try { let w = window; while (w.parent && w.parent !== w) w = w.parent; return w; }
  catch (e) { return window; }
})();

ROOT.__boards = ROOT.__boards || {};
ROOT.__boards['Aufgabe2'] = board;

// Pending Points nachziehen (falls vorher geklickt)
ROOT.__pendingPointSpecs = ROOT.__pendingPointSpecs || [];
ROOT.__pendingPointSpecs = ROOT.__pendingPointSpecs.filter(spec => {
  const parts = String(spec).split(';').map(s => String(s).trim());
  const bid = parts[0], name = parts[1];
  if (bid === 'Aufgabe2' && name) {
    // ensurePoint liegt im ROOT? -> über ROOT.window? meistens im gleichen Top-Level verfügbar.
    // Sicher: direkt im ROOT aufrufen, falls vorhanden.
    if (ROOT.ensurePoint) ROOT.ensurePoint(bid, name);
    else if (window.ensurePoint) window.ensurePoint(bid, name);
    return false;
  }
  return true;
});


function __isDarkTheme() {
  try {
    const doc = (window.parent && window.parent.document) ? window.parent.document : document;
    const win = (window.parent && window.parent.getComputedStyle) ? window.parent : window;

    // bevorzugt: body, sonst documentElement
    const el = doc.body || doc.documentElement;
    const bg = win.getComputedStyle(el).backgroundColor;

    // bg ist typischerweise "rgb(r,g,b)" oder "rgba(r,g,b,a)"
    const m = bg.match(/rgba?\((\d+),\s*(\d+),\s*(\d+)/i);
    if (!m) return false;

    const r = parseInt(m[1], 10);
    const g = parseInt(m[2], 10);
    const b = parseInt(m[3], 10);

    // relative Luminanz (0..255) – Schwelle ~ 128
    const lum = 0.2126 * r + 0.7152 * g + 0.0722 * b;
    return lum < 128;
  } catch (e) {
    return false;
  }
}


function __applyNavColors(board) {
  if (!board || !board.containerObj) return;

  // JSXGraph legt die Navigation innerhalb des Board-Containers an
  const nav = board.containerObj.querySelector('.JXG_navigation');
  if (!nav) return;

  const isDark = __isDarkTheme();
  const col = isDark ? '#fff' : '#000';

  // Navigation-Grundstil
  nav.style.color = col;
  nav.style.background = 'transparent';

  // Links/Buttons/Spans explizit einfärben
  nav.querySelectorAll('a, button, span').forEach(el => {
    el.style.color = col;
    el.style.borderColor = col;
    el.style.background = 'transparent';
    el.style.boxShadow = 'none';
  });

  // SVG-Icons (falls JSXGraph SVG nutzt)
  nav.querySelectorAll('svg, svg *').forEach(el => {
    el.style.fill = col;
    el.style.stroke = col;
  });

  // IMG-Icons (falls JSXGraph Bilder nutzt)
  nav.querySelectorAll('img').forEach(img => {
    img.style.filter = isDark ? 'invert(1)' : 'none';
  });
}

// einmal anwenden (nach initBoard)
__applyNavColors(board);

// bei Mode-Wechsel nachziehen
try {
  const mq = window.matchMedia('(prefers-color-scheme: dark)');
  if (mq && typeof mq.addEventListener === 'function') {
    mq.addEventListener('change', () => __applyNavColors(board));
  } else if (mq && typeof mq.addListener === 'function') {
    mq.addListener(() => __applyNavColors(board));
  }
} catch (e) {}


function __applyAxisColors(board) {
  if (!board) return;

  const isDark = __isDarkTheme();
  const col = isDark ? '#fff' : '#000';

  // 0) WICHTIG: Defaults für zukünftig neu erzeugte Tick-Labels setzen
  // (damit beim Rauszoomen neue Zahlen direkt korrekt gefärbt werden)
  try {
    board.options = board.options || {};
    board.options.defaultAxes = board.options.defaultAxes || {};
    ['x', 'y'].forEach(axKey => {
      board.options.defaultAxes[axKey] = board.options.defaultAxes[axKey] || {};
      board.options.defaultAxes[axKey].ticks = board.options.defaultAxes[axKey].ticks || {};
      board.options.defaultAxes[axKey].ticks.label = board.options.defaultAxes[axKey].ticks.label || {};

      board.options.defaultAxes[axKey].strokeColor = col;
      board.options.defaultAxes[axKey].ticks.strokeColor = col;

      // Diese beiden sind für die Ziffern entscheidend:
      board.options.defaultAxes[axKey].ticks.label.strokeColor = col;
      board.options.defaultAxes[axKey].ticks.label.fillColor   = col;
    });
  } catch (e) {}

  // Helfer: beliebige JSXGraph-Objekte einfärben
  const paint = (obj) => {
    if (!obj || typeof obj.setAttribute !== 'function') return;
    try {
      obj.setAttribute({
        strokeColor: col,
        highlightStrokeColor: col,
        fillColor: col,
        highlightFillColor: col
      });
    } catch (e) {}
  };

  // 1) Achsen + Ticks + Tick-Labels (existierende)
  try {
    if (board.defaultAxes) {
      if (board.defaultAxes.x && board.defaultAxes.x.label) paint(board.defaultAxes.x.label);
      if (board.defaultAxes.y && board.defaultAxes.y.label) paint(board.defaultAxes.y.label);

      const paintTicks = (axis) => {
        if (!axis) return;

        // Achsen-VisProps (wirkt oft auf neu erzeugte Ticks/Labels)
        try {
          axis.setAttribute({ strokeColor: col, highlightStrokeColor: col });
        } catch (e) {}

        // Standard-Ticks (häufig axis.defaultTicks)
        if (axis.defaultTicks) {
          paint(axis.defaultTicks);

          // Label-Default am Tick-Objekt selbst nachziehen
          try {
            axis.defaultTicks.setAttribute({
              strokeColor: col,
              highlightStrokeColor: col
            });
            if (axis.defaultTicks.visProp && axis.defaultTicks.visProp.label) {
              axis.defaultTicks.visProp.label.strokeColor = col;
              axis.defaultTicks.visProp.label.fillColor   = col;
            }
          } catch (e) {}

          if (axis.defaultTicks.labels && axis.defaultTicks.labels.length) {
            axis.defaultTicks.labels.forEach(paint);
          }
        }

        // Manche Versionen: axis.ticks als Array
        if (axis.ticks && axis.ticks.length) {
          axis.ticks.forEach(t => {
            paint(t);
            // Tick-Label-Defaults am Tick nachziehen
            try {
              if (t.visProp && t.visProp.label) {
                t.visProp.label.strokeColor = col;
                t.visProp.label.fillColor   = col;
              }
            } catch (e) {}
            if (t.labels && t.labels.length) t.labels.forEach(paint);
          });
        }

        // Manche Versionen: axis.getTicks()
        if (typeof axis.getTicks === 'function') {
          (axis.getTicks() || []).forEach(t => {
            paint(t);
            try {
              if (t.visProp && t.visProp.label) {
                t.visProp.label.strokeColor = col;
                t.visProp.label.fillColor   = col;
              }
            } catch (e) {}
            if (t.labels && t.labels.length) t.labels.forEach(paint);
          });
        }
      };

      paintTicks(board.defaultAxes.x);
      paintTicks(board.defaultAxes.y);
    }
  } catch (e) {}

  // 2) Fallback: Tick-Labels werden je nach Version als Textobjekte geführt.
  // Wir färben NUR Texte, die sehr wahrscheinlich Tick-Labels sind, um nicht alle Texte (z.B. Punktnamen) zu erwischen.
  try {
    if (board.objectsList && board.objectsList.length) {
      board.objectsList.forEach(o => {
        if (!o || o.elType !== 'text') return;

        // Heuristiken für Tick-Labels:
        // - Tick-Labels sind fast immer "fixed"
        // - und haben häufig sehr kurze Inhalte (Zahlen)
        // - und sind nicht "label" eines beliebigen Punktes (die sind oft an ein parent gekoppelt)
        const txt = (typeof o.getText === 'function') ? String(o.getText()) : (o.plaintext ? String(o.plaintext) : '');
        const looksNumeric = /^[\s\-+]*\d+([.,]\d+)?\s*$/.test(txt);

        const isFixed = (o.visProp && (o.visProp.fixed === true || o.visProp.isfixed === true));
        if (looksNumeric && isFixed) paint(o);
      });
    }
  } catch (e) {}

  // 3) Redraw
  try {
    if (typeof board.fullUpdate === 'function') board.fullUpdate();
    else board.update();
  } catch (e) {}
}

// einmal anwenden
__applyAxisColors(board);

// NEU: bei jedem Zoom/Pan (boundingbox ändert sich) Achsen/Ticks/Labels nachfärben
try {
  board.on('boundingbox', () => __applyAxisColors(board));
} catch (e) {}

// Optional (aber sinnvoll): auch nach Board-Resize einmal nachziehen
try {
  board.on('resize', () => __applyAxisColors(board));
} catch (e) {}


// einmal anwenden
__applyAxisColors(board);




function __applyBoardFrame(board) {
  if (!board || !board.containerObj) return;

  const isDark = __isDarkTheme();
  const col = isDark ? '#fff' : '#000';

  // Rahmen um das Koordinatensystem
  board.containerObj.style.border = `2px solid ${col}`;
  board.containerObj.style.borderRadius = '8px';     // optional
  board.containerObj.style.boxSizing = 'border-box';
}

// einmal anwenden
__applyBoardFrame(board);

// bei Mode-Wechsel nachziehen (gleiches Event wie Navigation nutzen)
try {
  const mq = window.matchMedia('(prefers-color-scheme: dark)');
  const handler = () => {
    __applyNavColors(board);
    __applyAxisColors(board);
  };

  if (mq && typeof mq.addEventListener === 'function') mq.addEventListener('change', handler);
  else if (mq && typeof mq.addListener === 'function') mq.addListener(handler);
} catch (e) {}



try {
  if (board && board.grids && board.grids.length) {
    board.grids.forEach(g => g && g.setAttribute && g.setAttribute({ strokeColor: btnColor }));
  }
} catch (e) {}


if (board && board.containerObj) {
  board.containerObj.style.background = 'transparent';
}

let __lastDark = null;

setInterval(() => {
  const nowDark = __isDarkTheme();
  if (nowDark === __lastDark) return;
  __lastDark = nowDark;

  __applyNavColors(board);
  __applyAxisColors(board);
  __applyBoardFrame(board);

  try { window.__recolorNeutralAutoLabels && window.__recolorNeutralAutoLabels(); } catch (e) {}
}, 300);


// Grid-Farbe automatisch an Button-Farbe koppeln
__watchGridColor(board, 400);


// f(x) = 1.5 * e^(-x) * sin(2*x)
var f = function(x){
  return 2.5 * Math.exp(-x/4) * Math.cos(12*x);
};

// sichtbarer x-Bereich
var bb   = board.getBoundingBox();   // [xmin, ymax, xmax, ymin]
var xmin = bb[2];
var xmax = bb[3];

// Graph
board.create('functiongraph', [f, 0, 100], {
  strokeWidth: 3,
  strokeColor: '#ff0000'
});



```

</div>





[[!]]
<script>true</script>
******************************

Es handelt sich um eine gedämpfte Schwingung, was daran zu erkennen ist, dass die Amplitude mit der Zeit abnimmt. Die maximalen Elongationen nehmen mit einem exponentiellen Zerfall ab. Diese Exponentialfunktion kann als Envelope dargestellt werden.

******************************




