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
    flex: 100%;
    margin-right: 0;
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

/* volle Breite für alle Collaborative-Canvas-Instanzen */
details.spoiler .collab-wrap {
  display: block;
  width: 100%;
}

/* Canvas: Breite 100%, Höhe wird per JS aus dem height-Attribut übernommen */
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


<script>
(function () {
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
      try {
        dataUrl = canvas.toDataURL('image/png');
      } catch (e) {
        dataUrl = null;
      }

      var newH = currentH + 100;
      setCanvasHeight(canvas, newH);

      if (dataUrl) {
        var img = new Image();
        img.onload = function () {
          try {
            var ctx = canvas.getContext('2d');
            if (ctx) ctx.drawImage(img, 0, 0);
          } catch (e) { /* bewusst ignorieren */ }
        };
        img.src = dataUrl;
      }
    });

    controls.appendChild(btn);
    wrap.appendChild(controls);
  }

  function fixCollabCanvasSizes() {
    document
      .querySelectorAll('details.spoiler .collab-wrap')
      .forEach(function (wrap) {
        var canvas = wrap.querySelector('canvas');
        if (!canvas) return;

        var h = getCanvasHeight(canvas);
        canvas.style.height = h + 'px';
        canvas.style.maxHeight = h + 'px';

        ensureControls(wrap);
      });
  }


  if (document.readyState === 'loading') {
    document.addEventListener('DOMContentLoaded', fixCollabCanvasSizes, { once: true });
  } else {
    fixCollabCanvasSizes();
  }


  var obs = new MutationObserver(function () {
    fixCollabCanvasSizes();
  });
  obs.observe(document.documentElement, { childList: true, subtree: true });

  window.addEventListener('resize', fixCollabCanvasSizes);
})();
</script>

Aufgabe 1: Berechne den Wert des Terms.

<section class="flex-container">

<div class="flex-child">

$a)\;\;$ Wie viel sind $40\%$ von $6000\,€$?

<details class="spoiler">
  <summary>
    <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/Repetitorium/Kap7/diew1.png" width="30" height="30">
    Platz zum Rechnen öffnen
  </summary>

  <div class="collab-wrap">
    @[Collaborative.lines(640,100)](./img/example.jpg)
  </div>
</details>

[[ 2400 ]]

</div>

<div class="flex-child">

$a)\;\;$ Wie viel sind $40\%$ von $6000\,€$?

<details class="spoiler">
  <summary>
    <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/Repetitorium/Kap7/diew1.png" width="30" height="30">
    Platz zum Rechnen öffnen
  </summary>

  <div class="collab-wrap">
    @[Collaborative.lines(640,100)](./img/example.jpg)
  </div>
</details>

[[ 2400 ]]

</div>

<div class="flex-child">

$a)\;\;$ Wie viel sind $40\%$ von $6000\,€$?

<details class="spoiler">
  <summary>
    <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/Repetitorium/Kap7/diew1.png" width="30" height="30">
    Platz zum Rechnen öffnen
  </summary>

  <div class="collab-wrap">
    @[Collaborative.lines(640,100)](./img/example.jpg)
  </div>
</details>

[[ 2400 ]]

</div>

</section>
