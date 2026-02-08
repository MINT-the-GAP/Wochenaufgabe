<!--
version:  0.0.1
language: de
author: Martin Lommatzsch




import: https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/main/README.md

import: https://cdn.jsdelivr.net/gh/LiaTemplates/JSXGraph@main/README.md
import: https://cdn.jsdelivr.net/gh/LiaTemplates/algebrite@master/README.md




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
// FIX: Target/Point-Checks konsequent über ROOT-Store
// =========================================================
window.setTargetFunction = function (boardId, key, fn) {
  const ROOT = window.__ROOT || window;
  ROOT.__targets = ROOT.__targets || {};
  ROOT.__targets[boardId] = ROOT.__targets[boardId] || {};
  ROOT.__targets[boardId][key] = fn;
};

window.isPointOnTargetFunction = function (boardId, pointName, key, epsY = 0.15) {
  const ROOT = window.__ROOT || window;

  const pt = ROOT.__points && ROOT.__points[boardId] && ROOT.__points[boardId][pointName];
  const fn = ROOT.__targets && ROOT.__targets[boardId] && ROOT.__targets[boardId][key];

  if (!pt || typeof fn !== 'function') return false;

  const x = pt.X();
  const y = pt.Y();
  const y0 = fn(x);

  if (!isFinite(y0)) return false;
  return Math.abs(y - y0) <= epsY;
};


// =========================================================
// @AutoPunkteGraph – Store + Namensgenerator + Actions
// =========================================================
ROOT.__autoPts = ROOT.__autoPts || {};             // boardId -> {counter, names:[]}
ROOT.__pendingAutoAdds = ROOT.__pendingAutoAdds || []; // falls Button vor Board klickt

function __autoLabel(i) {
  // A..Z, A',B',..Z', A'',...
  const letters = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
  const base = letters[i % 26];
  const k = Math.floor(i / 26);
  return base + (k > 0 ? "'".repeat(k) : "");
}

function __randInBBox(board) {
  // Gewünschter Startbereich: 0 <= x < 1 und 0 <= y < 1
  const x = Math.random();   // in [0,1)
  const y = Math.random();   // in [0,1)
  return [x, y];
}

// optional: wenn Punkt erzeugt wurde, aber Board war noch nicht da
ROOT.flushPendingAutoAdds = ROOT.flushPendingAutoAdds || function (boardId) {
  const board = ROOT.__boards && ROOT.__boards[boardId];
  if (!board) return;

  ROOT.__pendingAutoAdds = (ROOT.__pendingAutoAdds || []).filter(item => {
    if (item.boardId !== boardId) return true;

    // Punkt erzeugen/positionieren
    window.ensurePoint(item.boardId, item.name);
    const pt = ROOT.__points && ROOT.__points[item.boardId] && ROOT.__points[item.boardId][item.name];
    if (pt && item.xy) {
      try { pt.moveTo(item.xy, 0); } catch (e) {}
      try { board.update(); } catch (e) {}
    }
    return false;
  });
};

function __initAuto(boardId) {
  ROOT.__autoPts[boardId] = ROOT.__autoPts[boardId] || { counter: 0, names: [] };
  return ROOT.__autoPts[boardId];
}

// spec: "boardId;targetKey;eps"
window.addAutoPointFromSpec = function (spec, uid) {
  const ROOT = window.__ROOT || window;
  const parts = String(spec).split(';').map(s => String(s).trim());

  const boardId = parts[0] || '';
  if (!boardId) return;

  const state = __initAuto(boardId);
  const name = __autoLabel(state.counter++);
  state.names.push(name);

  const msg = document.getElementById('autoMsg-' + uid);

  const board = ROOT.__boards && ROOT.__boards[boardId];
  if (!board) {
    // Board noch nicht registriert -> merken
    ROOT.__pendingAutoAdds.push({ boardId, name, xy: null });
    if (msg) {
      msg.textContent = `(${name}) vorgemerkt (Board lädt noch ...)`;
      msg.style.color = __neutralAutoColor();
    }
    return;
  }

  // Punkt erzeugen (zufällige Position im Sichtfenster)
  window.ensurePoint(boardId, name);

  const pt = ROOT.__points && ROOT.__points[boardId] && ROOT.__points[boardId][name];
  if (pt) {
    const xy = __randInBBox(board);
    try { pt.moveTo(xy, 0); } catch (e) {}
    try { board.update(); } catch (e) {}
  }
  if (msg) {
    const html = state.names
      .map(n => `<span class="autoNameNeutral" style="font-weight:600; color:${window.__neutralAutoColor()};">\\(${n}\\)</span>`)
      .join(', ');

    msg.innerHTML = html;

    setTimeout(() => {
      try { ROOT.__typeset(msg); } catch (e) {}
      try { window.__recolorNeutralAutoLabels(); } catch (e) {}
    }, 0);
  }
};


window.checkAutoPointsFromSpec = function (spec, uid) {
  const ROOT = window.__ROOT || window;

  // Neue Spec-Auswertung (mit optionaler 2. Grenze)
  const parsed = (window.__parseAutoPointSpec)
    ? window.__parseAutoPointSpec(spec)
    : (function(){
        // Fallback, falls __parseAutoPointSpec aus irgendeinem Grund fehlt
        const parts = String(spec).split(';').map(s => String(s).trim());
        const boardId = parts[0] || '';
        const key     = parts[1] || '';
        let epsGreen  = parseFloat(String(parts[2] || '').replace(',', '.'));
        if (Number.isNaN(epsGreen)) epsGreen = 0.15;
        let epsOrange = parseFloat(String(parts[3] || '').replace(',', '.'));
        if (Number.isNaN(epsOrange)) epsOrange = 0.30;
        epsOrange = Math.max(epsOrange, epsGreen);
        return { boardId, key, epsGreen, epsOrange };
      })();

  const { boardId, key, epsGreen, epsOrange } = parsed;

  const msg = document.getElementById('autoMsg-' + uid);

  const state = ROOT.__autoPts && ROOT.__autoPts[boardId];
  const names = (state && state.names) ? state.names.slice() : [];

  if (!names.length) {
    if (msg) {
      msg.textContent = 'Noch keine Punkte erzeugt.';
      msg.style.color = '';
    }
    return;
  }

  if (msg) {
    const partsHtml = names.map(n => {
      const okGreen  = window.isPointOnTargetFunction(boardId, n, key, epsGreen);
      const okOrange = !okGreen && window.isPointOnTargetFunction(boardId, n, key, epsOrange);

      const col = okGreen ? 'green' : (okOrange ? 'orange' : 'red');
      return `<span style="color:${col}; font-weight:600;">\\(${n}\\)</span>`;
    });

    msg.innerHTML = partsHtml.join(', ');
    setTimeout(() => { try { ROOT.__typeset(msg); } catch (e) {} }, 0);
  }
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




@ErzeugePunkt: @ErzeugePunkt_(@uid,@0)

@ErzeugePunkt_
<button id="btn-@0" class="lia-btn" onclick="window.ensurePointFromSpec('@1')">Punkt erzeugen</button>

<script run-once="true" modify="false">
(function(){
  const btn = document.getElementById('btn-@0');
  if (!btn) return;

  const apply = () => {
    const c = (window.__neutralAutoColor ? window.__neutralAutoColor() : '#000');
    btn.style.color = c;
    // optional, aber meist sinnvoll (passt zum Text):
    btn.style.borderColor = c;
  };

  apply();

  try {
    const mq = window.matchMedia('(prefers-color-scheme: dark)');
    if (mq && typeof mq.addEventListener === 'function') mq.addEventListener('change', apply);
    else if (mq && typeof mq.addListener === 'function') mq.addListener(apply);
  } catch (e) {}
})();
</script>


<!-- class="check-only" data-solution-button="off"-->
[[ 0 ]]
<script modify="false">
  const spec = '@1';
  const parts = String(spec).split(';');

  const boardId = (parts[0] || '').trim();
  const name    = (parts[1] || '').trim();
  const tx = parseFloat((parts[2] || '').replace(',', '.'));
  const ty = parseFloat((parts[3] || '').replace(',', '.'));

  const pt = window.__points && window.__points[boardId] && window.__points[boardId][name];
  const eps = 0.05;

  const ok = !!pt
    && !Number.isNaN(tx)
    && !Number.isNaN(ty)
    && Math.abs(pt.X() - tx) < eps
    && Math.abs(pt.Y() - ty) < eps;

  ok
</script>
@end


@ErzeugePunktGraph: @ErzeugePunktGraph_(@uid,@0)

@ErzeugePunktGraph_
<button id="btnG-@0" class="lia-btn" onclick="window.ensurePointFromSpec('@1')">Punkt erzeugen</button>

<script run-once="true" modify="false">
(function(){
  const btn = document.getElementById('btnG-@0');
  if (!btn) return;

  const apply = () => {
    const c = (window.__neutralAutoColor ? window.__neutralAutoColor() : '#000');
    btn.style.color = c;
    btn.style.borderColor = c;
  };

  apply();

  try {
    const mq = window.matchMedia('(prefers-color-scheme: dark)');
    if (mq && typeof mq.addEventListener === 'function') mq.addEventListener('change', apply);
    else if (mq && typeof mq.addListener === 'function') mq.addListener(apply);
  } catch (e) {}
})();
</script>


<!-- class="check-only" data-solution-button="off"-->
[[ 0 ]]
<script modify="false">
  // @1 = "boardId;Name;targetKey;eps"
  const spec  = '@1';
  const parts = String(spec).split(';').map(s => String(s).trim());

  const boardId = parts[0] || '';
  const name    = parts[1] || '';
  const key     = parts[2] || '';

  let eps = parseFloat(String(parts[3] || '').replace(',', '.'));
  if (Number.isNaN(eps)) eps = 0.15;

  const ok = window.isPointOnTargetFunction(boardId, name, key, eps);
  ok
</script>
@end



@AutoPunkteGraph: @AutoPunkteGraph_(@uid,@0)

@AutoPunkteGraph_
<div>
  <button id="autoAdd-@0" class="lia-btn" onclick="window.addAutoPointFromSpec('@1','@0')">Punkt hinzufügen</button>
  <button id="autoChk-@0" class="lia-btn" onclick="window.checkAutoPointsFromSpec('@1','@0')">Prüfen</button>
  <span id="autoMsg-@0" style="margin-left: 12px;"></span>
</div>

<script run-once="true" modify="false">
(function(){
  const btnAdd = document.getElementById('autoAdd-@0');
  const btnChk = document.getElementById('autoChk-@0');

  const apply = () => {
    const c = (window.__neutralAutoColor ? window.__neutralAutoColor() : '#000');

    [btnAdd, btnChk].forEach(b => {
      if (!b) return;
      b.style.color = c;
      b.style.borderColor = c;
    });

    // ganz wichtig: bereits erzeugte, neutrale Labels anpassen (nicht grün/rot!)
    if (window.__recolorNeutralAutoLabels) window.__recolorNeutralAutoLabels();
  };

  apply();

  try {
    const mq = window.matchMedia('(prefers-color-scheme: dark)');
    if (mq && typeof mq.addEventListener === 'function') mq.addEventListener('change', apply);
    else if (mq && typeof mq.addListener === 'function') mq.addListener(apply);
  } catch (e) {}
})();
</script>

<script run-once="true" modify="false">
/**
 * Spec-Format:
 *   boardId;key;epsGreen;epsOrange
 *
 * Beispiele:
 *   @AutoPunkteGraph(Aufgabe1;graph1;0.15;0.3)
 *   @AutoPunkteGraph(Aufgabe1;graph1)              -> epsGreen=0.15, epsOrange=0.30
 *   @AutoPunkteGraph(Aufgabe1;graph1;0.2)          -> epsGreen=0.2,  epsOrange=0.30
 */
(function(){
  // Nur definieren, wenn nicht schon vorhanden
  if (window.__parseAutoPointSpec) return;

  window.__parseAutoPointSpec = function(spec){
    const parts = String(spec).split(';').map(s => String(s).trim());

    const boardId = parts[0] || '';
    const key     = parts[1] || '';

    let epsGreen = parseFloat(String(parts[2] || '').replace(',', '.'));
    if (Number.isNaN(epsGreen)) epsGreen = 0.15;

    let epsOrange = parseFloat(String(parts[3] || '').replace(',', '.'));
    if (Number.isNaN(epsOrange)) epsOrange = 0.30;

    // Sicherheit: Orange darf nicht strenger sein als Grün
    epsOrange = Math.max(epsOrange, epsGreen);

    return { boardId, key, epsGreen, epsOrange };
  };
})();
</script>


@end


-->





# Probeleistungskontrolle für Mathematik - Klasse 6: Zuordnung


> Letzte Aktualisierung am 08.02. gegen 12:30 Uhr

> <h2> WICHTIGER HINWEIS: Ich teste auch neue Funktionen mit dieser Datei, sollte etwas seltsames angezeigt werden oder gar nicht zu sehen sein, bitte einfach die Datei aktualisieren. Ich versuche die auftretenden Bugs der neuen Features nach und nach zu beseitigen. <br> <p align="right"> -Lommatzsch </p> </h2>

Swipe (Wische) entweder weiter oder klicke unten links auf neben der Seitenzahl auf den Pfeil nach rechts.



Diese Probearbeit hat mehr Aufgaben als die richtige Arbeit, damit du genug zum Üben hast. Es sind viele verschiedene Aufgabentypen abgebildet, sodass du alles nochmal bei der Bearbeitung dieser Aufgaben wiederholst.

Oben links in der Kopfzeile dieses LiaScript-Kurses findest du einen Textmarker.

Bei den Aufgaben ist auch immer ein Stiftbutton eingeblendet, klicke auf diesen Button und erhalte eine Schreibfläche.




### Prozentrechnung 1



**Aufgabe 1:** **Berechne** den Wert des Terms.


<section class="dynFlex">


<div class="flex-child">

__$a)\;\;$__ Wie viel sind $80\%$ von $50\,$€?  \

@canvas

<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" -->
 [[  40  ]]€ 
@Algebrite.check(40)
************
$$
\begin{align*}
80\% \cdot 50\,\text{€}
&= 0,8 \cdot 50\,\text{€} \\
&= 40\,\text{€} 
\end{align*}
$$
************

</div>
<div class="flex-child">

__$b)\;\;$__ Wie viel sind $125\%$ von $300\,$€?  \

@canvas


<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" -->
 [[  375  ]]€ 
@Algebrite.check(375)
************
$$
\begin{align*}
125\% \cdot 300\,\text{€}
&= 1,25 \cdot 300\,\text{€} \\
&= 375\,\text{€} 
\end{align*}
$$
************

</div>
<div class="flex-child">

__$c)\;\;$__ Wie viel sind $400\%$ von $125\,$€?  \

@canvas


<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" -->
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

</div>
<div class="flex-child">

__$d)\;\;$__ Wie viel sind $7\%$ von $900\,$€?  \

@canvas


<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" -->
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


</div>
<div class="flex-child">

__$e)\;\;$__ Wie viel sind $12\%$ von $750\,$€?  \

@canvas


<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" -->
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

</div>
<div class="flex-child">

__$f)\;\;$__ Wie viel sind $4\%$ von $1\,250\,$€?  \

@canvas


<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" -->
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


</div>


</section>








### Prozentrechnung 2



**Aufgabe 2:** **Berechne** den Wert des Terms.





<section class="dynFlex">


<div class="flex-child">

__$a)\;\;$__ $54\,\text{€}$ sind wie viel Prozent von $72\,\text{€}$?  \

@canvas

<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" -->
 [[  75  ]]%
@Algebrite.check(75)
************
$$
\begin{align*}
p\% \cdot 72\,\text{€} &= 54\,\text{€} \\
\frac{p}{100}\cdot 72\,\text{€} &= 54\,\text{€} \\
\frac{p}{100} &= \frac{54}{72} \\
p &= \frac{54}{72}\cdot 100 \\
p &= 75
\end{align*}
$$
************

</div>


<div class="flex-child">

__$b)\;\;$__ $110\,\text{€}$ sind wie viel Prozent von $88\,\text{€}$?  \

@canvas

<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" -->
 [[  125  ]]%
@Algebrite.check(125)
************
$$
\begin{align*}
p\% \cdot 88\,\text{€} &= 110\,\text{€} \\
\frac{p}{100}\cdot 88\,\text{€} &= 110\,\text{€} \\
\frac{p}{100} &= \frac{110}{88} \\
p &= \frac{110}{88}\cdot 100 \\
p &= 125
\end{align*}
$$
************

</div>


<div class="flex-child">

__$c)\;\;$__ $525\,\text{€}$ sind wie viel Prozent von $150\,\text{€}$?  \

@canvas

<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" -->
 [[  350  ]]%
@Algebrite.check(350)
************
$$
\begin{align*}
p\% \cdot 150\,\text{€} &= 525\,\text{€} \\
\frac{p}{100}\cdot 150\,\text{€} &= 525\,\text{€} \\
\frac{p}{100} &= \frac{525}{150} \\
p &= \frac{525}{150}\cdot 100 \\
p &= 350
\end{align*}
$$
************

</div>


<div class="flex-child">

__$d)\;\;$__ $96\,\text{€}$ sind wie viel Prozent von $640\,\text{€}$?  \

@canvas

<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" -->
 [[  15  ]]%
@Algebrite.check(15)
************
$$
\begin{align*}
p\% \cdot 640\,\text{€} &= 96\,\text{€} \\
\frac{p}{100}\cdot 640\,\text{€} &= 96\,\text{€} \\
\frac{p}{100} &= \frac{96}{640} \\
p &= \frac{96}{640}\cdot 100 \\
p &= 15
\end{align*}
$$
************

</div>


<div class="flex-child">

__$e)\;\;$__ $112\,\text{€}$ sind wie viel Prozent von $800\,\text{€}$?  \

@canvas

<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" -->
 [[  14  ]]%
@Algebrite.check(14)
************
$$
\begin{align*}
p\% \cdot 800\,\text{€} &= 112\,\text{€} \\
\frac{p}{100}\cdot 800\,\text{€} &= 112\,\text{€} \\
\frac{p}{100} &= \frac{112}{800} \\
p &= \frac{112}{800}\cdot 100 \\
p &= 14
\end{align*}
$$
************

</div>


<div class="flex-child">

__$f)\;\;$__ $72\,\text{€}$ sind wie viel Prozent von $480\,\text{€}$?  \

@canvas

<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" -->
 [[  15  ]]%
@Algebrite.check(15)
************
$$
\begin{align*}
p\% \cdot 480\,\text{€} &= 72\,\text{€} \\
\frac{p}{100}\cdot 480\,\text{€} &= 72\,\text{€} \\
\frac{p}{100} &= \frac{72}{480} \\
p &= \frac{72}{480}\cdot 100 \\
p &= 15
\end{align*}
$$
************

</div>


</section>




### Prozentrechnung 3



**Aufgabe 3:** **Berechne** den Wert des Terms.



<section class="dynFlex">


<div class="flex-child">

__$a)\;\;$__ $48\,\text{€}$ sind $12\%$ von wie viel Euro?  \

@canvas

<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" -->
 [[  400  ]]€ 
@Algebrite.check(400)
************
$$
\begin{align*}
12\% \cdot G &= 48\,\text{€} \\
0{,}12 \cdot G &= 48\,\text{€} \\
G &= \frac{48\,\text{€}}{0{,}12} \\
G &= 400\,\text{€}
\end{align*}
$$
************

</div>


<div class="flex-child">

__$b)\;\;$__ $90\,\text{€}$ sind $15\%$ von wie viel Euro?  \

@canvas

<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" -->
 [[  600  ]]€ 
@Algebrite.check(600)
************
$$
\begin{align*}
15\% \cdot G &= 90\,\text{€} \\
0{,}15 \cdot G &= 90\,\text{€} \\
G &= \frac{90\,\text{€}}{0{,}15} \\
G &= 600\,\text{€}
\end{align*}
$$
************

</div>


<div class="flex-child">

__$c)\;\;$__ $210\,\text{€}$ sind $35\%$ von wie viel Euro?  \

@canvas

<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" -->
 [[  600  ]]€ 
@Algebrite.check(600)
************
$$
\begin{align*}
35\% \cdot G &= 210\,\text{€} \\
0{,}35 \cdot G &= 210\,\text{€} \\
G &= \frac{210\,\text{€}}{0{,}35} \\
G &= 600\,\text{€}
\end{align*}
$$
************

</div>


<div class="flex-child">

__$d)\;\;$__ $52{,}50\,\text{€}$ sind $7\%$ von wie viel Euro?  \

@canvas

<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" -->
 [[  750  ]]€ 
@Algebrite.check(750)
************
$$
\begin{align*}
7\% \cdot G &= 52{,}50\,\text{€} \\
0{,}07 \cdot G &= 52{,}50\,\text{€} \\
G &= \frac{52{,}50\,\text{€}}{0{,}07} \\
G &= 750\,\text{€}
\end{align*}
$$
************

</div>


<div class="flex-child">

__$e)\;\;$__ $144\,\text{€}$ sind $18\%$ von wie viel Euro?  \

@canvas

<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" -->
 [[  800  ]]€ 
@Algebrite.check(800)
************
$$
\begin{align*}
18\% \cdot G &= 144\,\text{€} \\
0{,}18 \cdot G &= 144\,\text{€} \\
G &= \frac{144\,\text{€}}{0{,}18} \\
G &= 800\,\text{€}
\end{align*}
$$
************

</div>


<div class="flex-child">

__$f)\;\;$__ $360\,\text{€}$ sind $45\%$ von wie viel Euro?  \

@canvas

<!-- data-solution-timer="120s" data-solution-timer-start="oncheck" -->
 [[  800  ]]€ 
@Algebrite.check(800)
************
$$
\begin{align*}
45\% \cdot G &= 360\,\text{€} \\
0{,}45 \cdot G &= 360\,\text{€} \\
G &= \frac{360\,\text{€}}{0{,}45} \\
G &= 800\,\text{€}
\end{align*}
$$
************

</div>


</section>










### Textaufgaben Prozentrechnung 1

**Aufgabe 4:** Die Miete einer Wohnung soll nach einer Sanierung um $13\%$ erhöht werden. Die Miete betrug zuvor $650\,$€. **Berechne** den neuen Mietpreis. 

@canvas

<!-- data-solution-timer="5min" data-solution-timer-start="oncheck" -->
 [[  734,50  ]]€ 
@Algebrite.check(734.50)
************
$$
\begin{align*}
650\,\text{€} \cdot 13\% 
&= 650\,\text{€} \cdot 0{,}13 \\
&= 134{,}50\,\text{€}
\Rightarrow\;\; 650\,\text{€} + 134{,}50\,\text{€} & = 734{,}50\,\text{€}
\end{align*}
$$

oder

$$
\begin{align*}
650\,\text{€} \cdot \left(1 + 13\%\right)
&= 650\,\text{€} \cdot \left(1 + 0{,}13\right) \\
&= 650\,\text{€} \cdot 1{,}13 \\
&= 734{,}50\,\text{€}
\end{align*}
$$
************


---

---


**Aufgabe 5:** Ein Sparer hat ein Kapital von $8700\,$€ angelegt und bekommt nach einem Jahr Zinsen von $104,40\,$€. **Berechne** den Zinssatz.

@canvas

<!-- data-solution-timer="5min" data-solution-timer-start="oncheck" -->
 [[  0,012  ]] 
@Algebrite.check(0.012)
************
$$
\begin{align*}
\text{Zinsen} &= \text{Kapital} \cdot \text{Zinssatz} \\
104{,}40\,\text{€} &= 8700\,\text{€} \cdot p \\
p &= \frac{104{,}40\,\text{€}}{8700\,\text{€}} \\
p &= 0{,}012 \\
p &= 1{,}2\%
\end{align*}
$$
************


---

---

**Aufgabe 6:** Ein Fahrradhelm kostet $40\,$€. Im Angebot wird der Preis um $15\%$ gesenkt.  
**Berechne** den neuen Preis.  \

@canvas

<!-- data-solution-timer="180s" data-solution-timer-start="oncheck" -->
 [[  34  ]]€ 
@Algebrite.check(34)
************
$$
\begin{align*}
\text{Rabatt} &= 15\% \cdot 40\,\text{€} \\
             &= 0{,}15 \cdot 40\,\text{€} \\
             &= 6\,\text{€} \\
\text{Neuer Preis} &= 40\,\text{€} - 6\,\text{€} \\
                   &= 34\,\text{€}
\end{align*}
$$
************



---

---



**Aufgabe 7:** In einem Glas sind $250\,\text{ml}$ Saft. Davon werden $35\%$ getrunken.  
**Berechne**, wie viele Milliliter im Glas bleiben.  \

@canvas

<!-- data-solution-timer="180s" data-solution-timer-start="oncheck" -->
 [[  162,5  ]]ml 
@Algebrite.check(162.5)
************
$$
\begin{align*}
\text{Getrunken} 
&= 35\% \cdot 250\,\text{ml}
= 0{,}35 \cdot 250\,\text{ml}
= 87{,}5\,\text{ml} \\
\text{Rest}
&= 250\,\text{ml} - 87{,}5\,\text{ml}
= 162{,}5\,\text{ml}
\end{align*}
$$
************







---

---







**Aufgabe 8:** Ein Kapital von $8000\,$€ wurde zu einem Zinssatz von $1,3\%$ für ein Jahr angelegt. \

__$a)\;\;$__ **Berechne**, wie viel Geld nach diesem Jahr auf dem Konto ist. \

@canvas

<!-- data-solution-timer="180s" data-solution-timer-start="oncheck" -->
 [[  8104  ]] €
@Algebrite.check(8104)
************
$$
\begin{align*}
K_1 &= K_0 \cdot (1+p) \\
    &= 8000\,\text{€} \cdot 1{,}013 \\
    &= 8104\,\text{€}
\end{align*}
$$

oder

$$
\begin{align*}
Z_1 &= K_0 \cdot p \\
    &= 8000\,\text{€} \cdot 1{,}3 \\
    &= 8000\,\text{€} \cdot 0{,}013 \\
    &= 104\,\text{€}\\
K_1 &=K_0 +  Z_1  \\
    &= 8104\,\text{€}
\end{align*}
$$

************

__$b)\;\;$__ Das gesamte Geld aus dem ersten Jahr wird nochmals angelegt. **Berechne**, wie viel Geld nach dem zweiten Jahr auf dem Konto ist. \

@canvas

<!-- data-solution-timer="180s" data-solution-timer-start="oncheck" -->
 [[  8209,352  ]] €
@Algebrite.check2(8209.352,0.01)
************
$$
\begin{align*}
K_2 &= K_1 \cdot (1+p) \\
    &= 8104\,\text{€} \cdot 1{,}013 \\
    &= 8209{,}352\,\text{€} \\
    &\approx 8209{,}35\,\text{€}
\end{align*}
$$

oder

$$
\begin{align*}
Z_2 &= K_1 \cdot p \\
    &= 8104\,\text{€} \cdot 1{,}3\% \\
    &= 8104\,\text{€} \cdot 0{,}013 \\
    &= 105{,}352\,\text{€} \\
K_2 &= K_1 + Z_2 \\
    &= 8104\,\text{€} + 105{,}352\,\text{€} \\
    &= 8209{,}352\,\text{€} \\
    &\approx 8209{,}35\,\text{€}
\end{align*}
$$
************











### Zuordnungsaufgaben 1

**Aufgabe 9:** **Ordne** die Kacheln korrekt zu (Hinweis für Touchbildschirme: Klicke erst auf das Feld und dann auf die Kachel, um es in der Kachel zu platzieren. Halte deinen Finger länger auf der Kachel im Feld gedrückt, um sie wieder aus dem Feld herauszulösen.)


<!-- data-randomize="true"  -->
eineindeutig: [->[DNA wird Mensch zugeordnet]] \
eindeutig: [->[Schüler wird einer Klasse zugeordnet]] \
mehrdeutig: [->[Schuhegröße wird Schüler einer Klasse zugeordnet]] \





---

---

**Aufgabe 10:** Es wird ein Szenario beschrieben, **gib** die Kategorie der Zuordnung **an**.

__$a)\;\;$__ Jedem Kind wird genau ein Spindschlüssel ausgehändigt. 
[[(eineindeutig)|eindeutig|mehrdeutig]] \
__$b)\;\;$__ Jedem Schüler wird seine Zensur in einem Vokabeltest zugeordnet. [[eineindeutig|(eindeutig)|mehrdeutig]] \
__$c)\;\;$__ Jedem Schüler wird seine Körpergröße zugeordnet. [[eineindeutig|(eindeutig)|mehrdeutig]] \
__$d)\;\;$__ inem Schultag werden Pausenaktivitäten zugeordnet. [[eineindeutig|eindeutig|(mehrdeutig)]] \
__$e)\;\;$__ Jede Startnummer beim Sponsorenlauf wird genau einem Kind zugeordnet. [[(eineindeutig)|eindeutig|mehrdeutig]] \
__$f)\;\;$__ Jedem Kind wird seine Lieblingsfarbe zugeordnet. [[eineindeutig|(eindeutig)|mehrdeutig]] \



---

---

**Aufgabe 11:** Es wird ein Szenario beschrieben, **gib** die Art der Zuordnung **an**.

__$a)\;\;$__ Ein Auto legt mit einer konstanten Geschwindigkeit eine Strecke zurück. [[(proportional)|antiproportional|beliebig]] \
__$b)\;\;$__ Die Lernzeit in Abhängigkeit von der Note im Vokabeltest wird beobachtet. [[proportional|antiproportional|(beliebig)]] \
__$c)\;\;$__ Der Handy-Akkustand wird in der Abhängigkeit der Zeit beobachtet. [[proportional|antiproportional|(beliebig)]] \
__$d)\;\;$__ Die Arbeitszeit für einen Auftrag wird in Abhängigkeit der Anzahl der Arbeiter betrachtet. [[proportional|(antiproportional)|beliebig]] \
__$e)\;\;$__ Die Masse von Getränkeflaschen wird in der Anzahl der Flaschen betrachtet. [[(proportional)|antiproportional|beliebig]] \
__$f)\;\;$__ Die gerechte Anzahl von Bonbons aus einer Tütte wird in Abhängigkeit der Kinder, die Bonbons bekommen, wird betrachtet. [[proportional|(antiproportional)|beliebig]] \









### Zuordnungsaufgaben - Textaufgaben



<section class="dynFlex">


<div class="flex-child">


**Aufgabe 12:** Am Schulkiosk kosten drei Kakaos zusammen $2,10\,$€.  
**Berechne**, was fünf Kakaos kosten.

@canvas

<!-- data-solution-timer="180s" data-solution-timer-start="oncheck" -->
 [[  3,50  ]] €
@Algebrite.check2(3.50,0.001)
************

<!-- data-type="none" 
data-sortable="false" 
style="width:300px" -->
|Kakaos| Preis|
|:----:|:----:|
|  3   | 2,10€|
|  1   | 0,70€|
|  5   | 3,50€|

************





</div>


<div class="flex-child">










**Aufgabe 13:** Ein Kanister mit $12\,\text{l}$ Wasser wird gleichmäßig auf mehrere gleiche Flaschen verteilt.  
Wenn man $6$ Flaschen nimmt, sind in jeder Flasche $2\,\text{l}$.  
**Berechne**, wie viel Liter in jeder Flasche sind, wenn man $8$ Flaschen nimmt.

@canvas

<!-- data-solution-timer="180s" data-solution-timer-start="oncheck" -->
 [[  1,5  ]] l
@Algebrite.check2(1.5,0.001)
************

<!-- data-type="none" 
data-sortable="false" 
style="width:340px" -->
|Flaschen| Inhalt pro Flasche|
|:------:|:----------------:|
|   6    | $2\,\text{l}$|
|   1    | $12\,\text{l}$|
|   8    | $1{,}5\,\text{l}$|

************





</div>


<div class="flex-child">



**Aufgabe 14:** Ein Schüler fährt mit gleichbleibendem Tempo $9\,\text{km}$ in $30\,\text{min}$.  
**Berechne**, wie viele Kilometer er in $50\,\text{min}$ schafft.

@canvas

<!-- data-solution-timer="180s" data-solution-timer-start="oncheck" -->
 [[  15  ]] km
@Algebrite.check(15)
************

<!-- data-type="none" 
data-sortable="false" 
style="width:320px" -->
|Zeit| Strecke|
|:--:|:------:|
|30 min| $9\,\text{km}$|
|10 min| $3\,\text{km}$|
|50 min| $15\,\text{km}$|

************






</div>


<div class="flex-child">



**Aufgabe 15:** Für $18$ Kopien bezahlt man $1,44\,$€.  
**Berechne**, was $50$ Kopien kosten.

@canvas

<!-- data-solution-timer="180s" data-solution-timer-start="oncheck" -->
 [[  4,00  ]] €
@Algebrite.check2(4.00,0.001)
************

<!-- data-type="none" 
data-sortable="false" 
style="width:300px" -->
|Kopien| Preis|
|:----:|:----:|
|  18  | 1,44€|
|  1   | 0,08€|
|  50  | 4,00€|

************







</div>


<div class="flex-child">




**Aufgabe 16:** Sechs Schüler bauen die Technik für ein Schulfest in $48\,\text{min}$ auf (alle gleich schnell).  
**Berechne**, wie lange acht Schüler brauchen.

@canvas

<!-- data-solution-timer="180s" data-solution-timer-start="oncheck" -->
 [[  36  ]] min
@Algebrite.check(36)
************

<!-- data-type="none" 
data-sortable="false" 
style="width:320px" -->
|Schüler| Zeit|
|:-----:|:---:|
|   6   | 48 min|
|   1   | 288 min|
|   8   | 36 min|

************






</div>


<div class="flex-child">


**Aufgabe 17:** Für das Austragen von Zetteln brauchen $5$ Schüler gemeinsam $30\,\text{min}$ (alle gleich schnell).  
**Berechne**, wie lange $10$ Schüler brauchen.

@canvas

<!-- data-solution-timer="180s" data-solution-timer-start="oncheck" -->
 [[  15  ]] min
@Algebrite.check(15)
************

<!-- data-type="none" 
data-sortable="false" 
style="width:320px" -->
|Schüler| Zeit|
|:-----:|:---:|
|   5   | 30 min|
|   1   | 150 min|
|  10   | 15 min|

************



</div>


</section>














### Zuordnungsaufgaben - Koordinatensystem


**Aufgabe 18:** Erzeuge den Punkt und ziehe ihn auf die passenden Koordinaten.



<div style="max-width: 1000px;">

``` javascript @JSX.Graph

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

board = JXG.JSXGraph.initBoard(jxgbox, {
  axis: true,
  showNavigation: true,
  showCopyright: false,
  boundingbox: [-1, 5, 7, -1],
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
ROOT.__boards['Aufgabe3'] = board;

// Pending Points nachziehen (falls vorher geklickt)
ROOT.__pendingPointSpecs = ROOT.__pendingPointSpecs || [];
ROOT.__pendingPointSpecs = ROOT.__pendingPointSpecs.filter(spec => {
  const parts = String(spec).split(';').map(s => String(s).trim());
  const bid = parts[0], name = parts[1];
  if (bid === 'Aufgabe3' && name) {
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



window.__boards = window.__boards || {};
window.__boards['Aufgabe3'] = board;


```

</div>





<section class="dynFlex">

<div class="flex-child">

Ziehe den Punkt $P$ auf die Koordinaten $(2|3)$.

@ErzeugePunkt(Aufgabe3;P;2;3)

</div>



<div class="flex-child">

Ziehe den Punkt $A$ auf die Koordinaten $(1|4)$.

@ErzeugePunkt(Aufgabe3;A;1;4)

</div>

<div class="flex-child">

Ziehe den Punkt $B$ auf die Koordinaten $(6|2)$.

@ErzeugePunkt(Aufgabe3;B;6;2)

</div>

<div class="flex-child">

Ziehe den Punkt $C$ auf die Koordinaten $(3|1)$.

@ErzeugePunkt(Aufgabe3;C;3;1)

</div>

<div class="flex-child">

Ziehe den Punkt $D$ auf die Koordinaten $(0|4)$.

@ErzeugePunkt(Aufgabe3;D;0;4)

</div>

<div class="flex-child">

Ziehe den Punkt $E$ auf die Koordinaten $(6|4)$.

@ErzeugePunkt(Aufgabe3;E;6;4)

</div>

<div class="flex-child">

Ziehe den Punkt $F$ auf die Koordinaten $(1,5|2,2)$.

@ErzeugePunkt(Aufgabe3;F;1.5;2.2)

</div>

<div class="flex-child">

Ziehe den Punkt $G$ auf die Koordinaten $\left(\dfrac{63}{10} \right. \left| \dfrac{8}{5}\right)$.

@ErzeugePunkt(Aufgabe3;G;6.3;1.6)

</div>

<div class="flex-child">

Ziehe den Punkt $H$ auf die Koordinaten $\left(\dfrac{13}{4} \right. \left| \dfrac{7}{10}\right)$.

@ErzeugePunkt(Aufgabe3;H;3.25;0.7)

</div>

</section>





### Zuordnungsaufgaben - Wertetabellen


**Aufgabe 19:** In der Mensa kosten $4$ belegte Brötchen zusammen $6,00\,$€. Fülle die Wertetabelle aus.


<!-- data-type="none" data-sortable="false"  data-show-partial-solution style="width:1200px" -->
|        |             |             |           |          |              |          |               |
|Brötchen| $1$         | $2$         |       $4$ | [[ 10 ]] |       $22$   | [[ 62 ]] |       $75$    |
| Kosten | [[ 1,50 ]]€ | [[ 3,00 ]]€ | $6,00\,$€ |  $15\,$€  | [[ 33,00 ]]€ |  $93\,$€ | [[ 112,50 ]]€ |
@Algebrite.check([10;62;1.5;3;33;112.5],  [ 0.00001 ; 0.00001 ; 0.00001  ; 0.00001  ; 0.00001 ; 0.00001  ])


---

---

**Aufgabe 20:** Sechs Schüler räumen einen Klassenraum in $30\,\text{min}$ auf (alle gleich schnell).  
Fülle die Wertetabelle aus.

<!-- data-type="none" data-sortable="false" data-show-partial-solution style="width:1200px" -->
|        |        |        |        |         |        |         |        |        |
|Schüler |  $1$   |  $3$   |  $6$   | [[ 10 ]]|  $12$  | [[ 15 ]]|  $20$  | [[ 30 ]]|
|Zeit    | [[ 180 ]] min | [[ 60 ]] min | $30$ min | [[ 18 ]] min | [[ 15 ]] min | $12$ min | [[ 9 ]] min | $6$ min |
@Algebrite.check([10;15;30;180;60;18;15;9],[0.00001;0.00001;0.00001;0.00001;0.00001;0.00001;0.00001;0.00001])




---

---


**Aufgabe 21:** Ein Bus fährt eine Strecke von $120\,\text{km}$.  
Bei $60\,\text{km/h}$ dauert die Fahrt $2\,\text{h}$. Fülle die Wertetabelle aus.

<!-- data-type="none" data-sortable="false" data-show-partial-solution style="width:1200px" -->
|                 |        |        |        |        |        |        |          |          |
|Geschwindigkeit  | $30\,\frac{\text{km}}{\text{h}}$  | $40\,\frac{\text{km}}{\text{h}}$   | $60\,\frac{\text{km}}{\text{h}}$   | $80\,\frac{\text{km}}{\text{h}}$  | $100\,\frac{\text{km}}{\text{h}}$   | $120\,\frac{\text{km}}{\text{h}}$   | [[ 150 ]] $\,\frac{\text{km}}{\text{h}}$   | [[ 75 ]] $\,\frac{\text{km}}{\text{h}}$ |
|Zeit             | [[ 4 ]] h | [[ 3 ]] h | $2$ h | [[ 1,5 ]] h | [[ 1,2 ]] h | $1$ h | $0,8$ h | $1,6$ h |
@Algebrite.check([150;75;4;3;1.5;1.2],[0.00001;0.00001;0.00001;0.00001;0.00001;0.00001])



---

---


**Aufgabe 22:** Im Schreibwarenladen kosten $8$ Hefte zusammen $6,40\,$€.  
Fülle die Wertetabelle aus.

<!-- data-type="none" data-sortable="false" data-show-partial-solution style="width:1200px" -->
|      |          |          |           |          |          |          |          |          |
|Hefte |  $1$     |  $4$     |   $8$     | [[ 12 ]] |  $20$    | [[ 25 ]] |  $30$    |  $50$    |
|Kosten| [[ 0,80 ]]€ | [[ 3,20 ]]€ | $6,40\,$€ | [[ 9,60 ]]€ | [[ 16,00 ]]€ | $20,00\,$€ | [[ 24,00 ]]€ | [[ 40,00 ]]€ |
@Algebrite.check([12;25;0.8;3.2;9.6;16;24;40],[0.00001;0.00001;0.00001;0.00001;0.00001;0.00001;0.00001;0.00001])






---

---



**Aufgabe 23:** Entscheide, ob die Tabelle eine proportionale, eine antiproportionale oder eine beliebige Zuordnung beschreibt.



<section class="dynFlex">


<div class="flex-child">

__$a)\;\;$__



<!-- data-type="none" data-sortable="false" -->
|      |          |          |           |          |          |
|  $x$ |  $1$     |  $4$     |   $8$     | $12$     |  $24$    |
|$f(x)$|   $72$   |  $18$    | $9$       |      $6$ |      $3$ |


[[proportional|(antiproportional)|beliebig]] 

</div>


<div class="flex-child">

__$b)\;\;$__

<!-- data-type="none" data-sortable="false" -->
|      |          |          |           |          |          |
|  $x$ |  $1$     |  $4$     |   $8$     | $12$     |  $24$    |
|$f(x)$|  $96$    |  $24$    | $12$      |  $8$     |  $4$     |

[[ proportional | (antiproportional) | beliebig ]] 

</div>


<div class="flex-child">

__$c)\;\;$__

<!-- data-type="none" data-sortable="false" -->
|      |          |          |           |          |          |
|  $x$ |  $1$     |  $4$     |   $8$     | $12$     |  $24$    |
|$f(x)$|   $8$    |  $23$    | $43$      |  $63$    |  $123$   |

[[ proportional | antiproportional | (beliebig) ]] 

</div>


<div class="flex-child">

__$d)\;\;$__

<!-- data-type="none" data-sortable="false" -->
|      |          |          |           |          |          |
|  $x$ |  $1$     |  $4$     |   $8$     | $12$     |  $24$    |
|$f(x)$|   $6$    |  $24$    | $48$      |  $72$    |  $144$   |

[[ (proportional) | antiproportional | beliebig ]] 

</div>


<div class="flex-child">

__$e)\;\;$__

<!-- data-type="none" data-sortable="false" -->
|      |          |          |           |          |          |
|  $x$ |  $1$     |  $4$     |   $8$     | $12$     |  $24$    |
|$f(x)$|  $72$    |  $18$    | $9$       |  $6$     |  $3$     |

[[ proportional | (antiproportional) | beliebig ]] 

</div>


<div class="flex-child">

__$f)\;\;$__

<!-- data-type="none" data-sortable="false" -->
|      |          |          |           |          |          |
|  $x$ |  $1$     |  $4$     |   $8$     | $12$     |  $24$    |
|$f(x)$|  $120$   |  $30$    | $15$      |  $10$    |  $5$     |

[[ proportional | (antiproportional) | beliebig ]] 

</div>


<div class="flex-child">

__$g)\;\;$__

<!-- data-type="none" data-sortable="false" -->
|      |          |          |           |          |          |
|  $x$ |  $1$     |  $4$     |   $8$     | $12$     |  $24$    |
|$f(x)$|   $9$    |  $36$    | $72$      |  $108$   |  $216$   |

[[ (proportional) | antiproportional | beliebig ]] 

</div>


<div class="flex-child">

__$h)\;\;$__

<!-- data-type="none" data-sortable="false" -->
|      |          |          |           |          |          |
|  $x$ |  $1$     |  $4$     |   $8$     | $12$     |  $24$    |
|$f(x)$|  $11$    |  $14$    | $18$      |  $22$    |  $34$    |

[[ proportional | antiproportional | (beliebig) ]] 

</div>



<div class="flex-child">

__$i)\;\;$__

<!-- data-type="none" data-sortable="false" -->
|      |          |          |           |          |          |
|  $x$ |  $1$     |  $4$     |   $8$     | $12$     |  $24$    |
|$f(x)$|   $7$    |  $28$    | $56$      |  $84$    |  $168$   |

[[ (proportional) | antiproportional | beliebig ]] 

</div>

</section>
























### Zuordnungsaufgaben - Graphen


**Aufgabe 24:** In dem Koordinatensystem sind verschiedene Graphen von Preisentwicklungen dargestellt.



<div style="max-width: 1000px">

``` javascript @JSX.Graph

// ✅ VOR initBoard: Container-Größe festlegen
jxgbox.style.width  = '100%';
jxgbox.style.height = '650px';

// optional, aber oft hilfreich gegen Lia/Wrapper-CSS:
jxgbox.style.minHeight = '650px';
jxgbox.style.maxHeight = '650px';
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
  boundingbox: [-1, 10, 10, -1],
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
    name: '\(m\,\text{in [kg]}\)',
    withLabel: true,
    label: { position: 'rt', offset: [-60, -30], fontSize: 18 },
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
    name: 'Preis in €',
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
var f = function(x){  return 0.25*x; };
var g = function(x){  return 0.75*x; };
var h = function(x){  return 1.2*x; };

// Graph
board.create('functiongraph', [f, 0, 100], {  strokeWidth: 3,  strokeColor: '#ff0000'});
board.create('functiongraph', [g, 0, 100], {  strokeWidth: 3,  strokeColor: '#00ff40'});
board.create('functiongraph', [h, 0, 100], {  strokeWidth: 3,  strokeColor: '#2200ff'});



```

</div>


In blau ist der Preis für Erdbeeren, in grün ist der Preis für Kirschen und in blau ist der Preis für Himbeeren angegeben.



<section class="dynFlex">


<div class="flex-child">


__$a)\;\;$__ Gib den Preis von $8\,$kg Kirschen an.

 [[ 6        ]] € 
@Algebrite.check2(6,0.05)


</div>

<div class="flex-child">

__$b)\;\;$__ Gib an, wie viel Kilogramm Himbeeren man für 2€ kaufen kann.

 [[ 8        ]] kg 
@Algebrite.check2(8,0.05)

</div>

<div class="flex-child">

__$c)\;\;$__ Gib den Preis von $4\,$kg Erdbeeren an.

 [[ 4,80      ]] € 
@Algebrite.check2(4.8,0.05)

</div>

<div class="flex-child">

__$d)\;\;$__ Gib an, wie viel Kilogramm Kirschen man für 1€ kaufen kann.

 [[ 1,333        ]] kg 
@Algebrite.check2(1.333,0.05)

</div>

<div class="flex-child">

__$e)\;\;$__ Gib an, wie viel Kilogramm Kirschen man statt 12kg Himbeeren kaufen kann.

 [[ 4        ]] kg 
@Algebrite.check2(4,0.05)

</div>

<div class="flex-child">

__$f)\;\;$__ Gib an, wie viel Euro man mehr bezahlen müsste, wenn man statt 20kg Himbeeren doch 20kg Kischen kaufen will.

 [[ 10       ]] € 
@Algebrite.check2(10,0.05)

</div>


</section>









