<!--
version:  0.0.2
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
    flex: 1 1 100%;
    margin-right: 0;
    min-width: 0;
  }
}

details.spoiler > summary {
  cursor: pointer;
  font-weight: 600;
}
details.spoiler[open] > summary {
  margin-bottom: 0.5em;
}
details.spoiler {
  margin: 0.5em 0;
}

/* Collab-Wrap: darf NIE breiter als die Spalte werden */
details.spoiler .collab-wrap {
  display: block;
  width: 100%;
  max-width: 100%;
  overflow: hidden;
  box-sizing: border-box;
}

/* Alles, was Collaborative intern erzeugt, wird ebenfalls gebremst */
details.spoiler .collab-wrap * {
  max-width: 100%;
  box-sizing: border-box;
}

/* Canvas: Breite 100% relativ zur collab-wrap, Höhe per JS */
details.spoiler .collab-wrap canvas {
  width: 100% !important;
  max-width: 100% !important;
  display: block;
  touch-action: none;
}

/* Button-Leiste: unten rechts am Ende (unterhalb) der Canvas */
details.spoiler .collab-wrap .collab-controls {
  margin-top: 6px;
  display: flex;
  justify-content: flex-end;
}

details.spoiler .collab-wrap .collab-controls button {
  padding: 6px 10px;
  font-size: 0.9rem;
  border: 1px solid currentColor;
  border-radius: 6px;
  background: transparent;
  cursor: pointer;
}
@end

formula: \carry   \textcolor{red}{\scriptsize #1}
formula: \digit   \rlap{\carry{#1}}\phantom{#2}#2
formula: \permil  \text{‰}

import: https://raw.githubusercontent.com/liaTemplates/algebrite/master/README.md
import: https://raw.githubusercontent.com/LiaTemplates/Tikz-Jax/main/README.md
import: https://raw.githubusercontent.com/LiaTemplates/mermaid_template/0.1.4/README.md

script: https://cdn.jsdelivr.net/gh/LiaTemplates/Tikz-Jax@main/dist/index.js

import: https://raw.githubusercontent.com/liaTemplates/ABCjs/main/README.md
        https://raw.githubusercontent.com/LiaTemplates/Speech-Recognition-Quiz/refs/heads/main/README.md
        https://raw.githubusercontent.com/liaTemplates/AVR8js/main/README.md
        https://raw.githubusercontent.com/liaTemplates/JSXGraph/main/README.md
        https://raw.githubusercontent.com/liaTemplates/mec2/main/README.md
        https://raw.githubusercontent.com/LiaTemplates/CollaborativeDrawing/main/README.md
        https://raw.githubusercontent.com/LiaTemplates/SpreadSheet/refs/heads/main/README.md
        https://github.com/LiaTemplates/PeriodicTable/blob/main/README.md

persistent: true
edit: true

eingabe: <script input="number" input-always-active modify="false" value="0" default="0">@input</script>
-->

# Dann schauen wir mal

<section class="flex-container">

  <div class="flex-child">

    $a)\;\;$ Wie viel sind $40\%$ von $6000\,€$?

    <div class="onlyPresentation" style="display:none;">
    </div>

    <div class="onlyTextbook" style="display:none;">
      <details class="spoiler">
        <summary>
          <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/pen.png" width="20" height="20">
          Platz für Notizen oder zum Rechnen öffnen
        </summary>

        <div class="collab-wrap">
          @[Collaborative.lines(640,100)](./img/example.jpg)
        </div>
      </details>
    </div>

    [[ 2400 ]]

  </div>


  <div class="flex-child">

    $a)\;\;$ Wie viel sind $40\%$ von $6000\,€$?

    <div class="onlyPresentation" style="display:none;">
    </div>

    <div class="onlyTextbook" style="display:none;">
      <details class="spoiler">
        <summary>
          <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/pen.png" width="20" height="20">
          Platz für Notizen oder zum Rechnen öffnen
        </summary>

        <div class="collab-wrap">
          @[Collaborative.lines(640,100)](./img/example.jpg)
        </div>
      </details>
    </div>

    [[ 2400 ]]

  </div>


  <div class="flex-child">

    $a)\;\;$ Wie viel sind $40\%$ von $6000\,€$?

    <div class="onlyPresentation" style="display:none;">
    </div>

    <div class="onlyTextbook" style="display:none;">
      <details class="spoiler">
        <summary>
          <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/pen.png" width="20" height="20">
          Platz für Notizen oder zum Rechnen öffnen
        </summary>

        <div class="collab-wrap">
          @[Collaborative.lines(640,100)](./img/example.jpg)
        </div>
      </details>
    </div>

    [[ 2400 ]]

  </div>

</section>


<script>
(function () {
  /* -------------------- Modus-Erkennung (localStorage["settings"]) -------------------- */

  function norm(x) { return String(x == null ? "" : x).toLowerCase(); }

  function safeGetSettingsRaw() {
    try { return localStorage.getItem("settings"); }
    catch (e) { return null; }
  }

  function findModeInJson(obj) {
    const seen = new Set();

    function walk(v) {
      if (v == null) return null;
      const t = typeof v;

      if (t === "string") {
        const s = norm(v);
        if (s.includes("presentation") || s.includes("slides")) return "presentation";
        if (s.includes("textbook") || s.includes("book")) return "textbook";
        return null;
      }

      if (t !== "object") return null;

      if (seen.has(v)) return null;
      seen.add(v);

      // Keys zuerst (typische Kandidaten)
      for (const k in v) {
        if (!Object.prototype.hasOwnProperty.call(v, k)) continue;
        const key = norm(k);
        if (key === "mode" || key === "view" || key === "layout" || key === "format") {
          const m = walk(v[k]);
          if (m) return m;
        }
      }

      // Danach Values komplett scannen
      for (const k in v) {
        if (!Object.prototype.hasOwnProperty.call(v, k)) continue;
        const m = walk(v[k]);
        if (m) return m;
      }

      return null;
    }

    return walk(obj);
  }

  function detectMode() {
    const raw = safeGetSettingsRaw();
    let mode = null;

    if (raw) {
      try {
        mode = findModeInJson(JSON.parse(raw));
      } catch (e) {
        const s = norm(raw);
        if (s.includes("presentation") || s.includes("slides")) mode = "presentation";
        if (s.includes("textbook") || s.includes("book")) mode = "textbook";
      }
    }

    return mode || "unknown";
  }

  /* -------------------- Anzeige umschalten -------------------- */

  function setDisplayForAll(selector, display) {
    document.querySelectorAll(selector).forEach(function (el) {
      el.style.display = display;
    });
  }

  function applyModeVisibility() {
    const mode = detectMode();
    const isPres = (mode === "presentation");

    setDisplayForAll(".onlyPresentation", isPres ? "block" : "none");
    setDisplayForAll(".onlyTextbook",     isPres ? "none"  : "block");
  }

  /* -------------------- Collab: Breite an .flex-child klemmen -------------------- */

  function isActuallyVisible(el) {
    return !!(el && (el.offsetWidth || el.offsetHeight || el.getClientRects().length));
  }

  function clampCollabWrapToFlexChild(wrap) {
    var flexChild = wrap.closest('.flex-child');
    if (!flexChild) return;

    var w = flexChild.clientWidth;
    if (!w || w < 50) return;

    // Wrap darf nicht auf Textbook-Gesamtbreite wachsen
    wrap.style.width = w + 'px';
    wrap.style.maxWidth = w + 'px';
    wrap.style.boxSizing = 'border-box';

    // Inneres Root-Element (falls vorhanden) ebenfalls einbremsen
    var root = wrap.firstElementChild;
    if (root) {
      root.style.maxWidth = '100%';
      root.style.boxSizing = 'border-box';
    }
  }

  /* -------------------- Collab: Height + Mehr-Platz-Button -------------------- */

  function getCanvasHeight(canvas) {
    var hAttr = canvas.getAttribute('height');
    var h = hAttr ? parseInt(hAttr, 10) : null;

    if (!h || isNaN(h)) {
      if (typeof canvas.height === 'number' && canvas.height > 0) return canvas.height;
      var cs = window.getComputedStyle(canvas);
      var hs = parseInt(cs.height, 10);
      return (!isNaN(hs) && hs > 0) ? hs : 200;
    }
    return h;
  }

  function setCanvasHeight(canvas, newH) {
    canvas.setAttribute('height', String(newH));
    canvas.height = newH;
    canvas.style.height = newH + 'px';
    canvas.style.maxHeight = newH + 'px';
  }

  function ensureControls(wrap) {
    if (wrap.querySelector('.collab-controls')) return;

    var controls = document.createElement('div');
    controls.className = 'collab-controls';

    var btn = document.createElement('button');
    btn.type = 'button';
    btn.textContent = 'Mehr Platz';

    btn.addEventListener('click', function () {
      var canvas = wrap.querySelector('canvas');
      if (!canvas) return;

      var currentH = getCanvasHeight(canvas);

      var dataUrl = null;
      try { dataUrl = canvas.toDataURL('image/png'); } catch (e) { dataUrl = null; }

      var newH = currentH + 100;
      setCanvasHeight(canvas, newH);

      if (dataUrl) {
        var img = new Image();
        img.onload = function () {
          try {
            var ctx = canvas.getContext('2d');
            if (ctx) ctx.drawImage(img, 0, 0);
          } catch (e) {}
        };
        img.src = dataUrl;
      }
    });

    controls.appendChild(btn);
    wrap.appendChild(controls);
  }

  function fixCollabCanvasSizesVisibleOnly() {
    document.querySelectorAll('.onlyTextbook details.spoiler .collab-wrap').forEach(function (wrap) {
      if (!isActuallyVisible(wrap)) return;

      // Breite an Spalte koppeln (entscheidend gegen "volle Textbookbreite")
      clampCollabWrapToFlexChild(wrap);

      var canvas = wrap.querySelector('canvas');
      if (!canvas) return;

      var h = getCanvasHeight(canvas);
      canvas.style.height = h + 'px';
      canvas.style.maxHeight = h + 'px';

      ensureControls(wrap);
    });
  }

  function hookDetailsToggle() {
    document.querySelectorAll('.onlyTextbook details.spoiler').forEach(function (det) {
      if (det.__liaHooked) return;
      det.__liaHooked = true;

      det.addEventListener('toggle', function () {
        if (det.open) {
          requestAnimationFrame(function () {
            fixCollabCanvasSizesVisibleOnly();
          });
        }
      });
    });
  }

  /* -------------------- Zentrales Rendern -------------------- */

  function renderAll() {
    applyModeVisibility();
    requestAnimationFrame(function () {
      hookDetailsToggle();
      fixCollabCanvasSizesVisibleOnly();
    });
  }

  /* -------------------- Start & Updates -------------------- */

  function start() {
    renderAll();

    // Polling: LiaScript setzt settings oft ohne storage-event
    setInterval(renderAll, 500);

    window.addEventListener("storage", function (e) {
      if (!e || e.key === "settings") renderAll();
    });

    // DOM-Änderungen (LiaScript rendert dynamisch)
    var obs = new MutationObserver(function () {
      hookDetailsToggle();
      fixCollabCanvasSizesVisibleOnly();
    });
    obs.observe(document.documentElement, { childList: true, subtree: true });

    window.addEventListener('resize', function () {
      fixCollabCanvasSizesVisibleOnly();
    });
  }

  if (document.readyState === "loading") {
    document.addEventListener("DOMContentLoaded", start, { once: true });
  } else {
    start();
  }
})();
</script>
