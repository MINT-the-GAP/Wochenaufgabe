<!--
version:  0.0.3
language: de


@style
main > *:not(:last-child) {
  margin-bottom: 3rem;
}

input {
  text-align: center;
}

/* =========================================
   Layout: Default (Lehrbuch/Slides) = untereinander
   Nur Präsentation = nebeneinander (Flex)
   ========================================= */

/* Default: untereinander */

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

/* Nur in Präsentation: nebeneinander */
html.mode-presentation .flex-container {
  display: flex;
  flex-wrap: wrap;
  align-items: stretch;
  gap: 20px;
}

html.mode-presentation .flex-child {
  flex: 1;
  min-width: 350px;
  margin-right: 0;
}

/* optional: sehr schmale Displays -> auch in Präsentation untereinander */
@media (max-width: 400px) {
  html.mode-presentation .flex-container {
    display: block;
  }
  html.mode-presentation .flex-child {
    width: 100%;
    min-width: 0;
  }
}

/* =========================================
   Spoiler / Details Styling
   ========================================= */

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

/* =========================================
   Collaborative Drawing: Canvas immer 100% Breite
   ========================================= */

details.spoiler .collab-wrap {
  display: block;
  width: 100%;
}

details.spoiler .collab-wrap canvas {
  width: 100% !important;
  max-width: 100% !important;
  display: block;
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
(() => {
  function normalizeMode(v) {
    v = (v || "").toLowerCase();
    if (v.includes("textbook")) return "textbook";
    if (v.includes("slide")) return "slides";
    if (v.includes("present")) return "presentation";
    return null;
  }

  function detectMode() {
    const url = new URL(window.location.href);

    // Häufig: Mode steckt in URL-Parametern oder Hash
    const candidates = [
      url.searchParams.get("mode"),
      url.searchParams.get("view"),
      url.searchParams.get("format"),
      (url.hash || "").replace(/^#/, "")
    ].map(normalizeMode).filter(Boolean);

    if (candidates.length) return candidates[0];

    // Fallback: Mode könnte im localStorage liegen (je nach Einbettung/Host)
    const keys = [
      "lia-mode", "lia:mode", "mode",
      "liascript-mode", "presentation-mode", "view-mode"
    ];

    for (const k of keys) {
      const v = normalizeMode(localStorage.getItem(k));
      if (v) return v;
    }

    return null;
  }

  function applyModeClass() {
    const root = document.documentElement;
    root.classList.remove("mode-textbook", "mode-slides", "mode-presentation");

    const mode = detectMode();
    if (mode) root.classList.add(`mode-${mode}`);
  }

  applyModeClass();

  // falls beim Umschalten URL/State geändert wird:
  window.addEventListener("hashchange", applyModeClass);
  window.addEventListener("popstate", applyModeClass);
  window.addEventListener("storage", applyModeClass);
})();
</script>


Aufgabe 1: Berechne den Wert des Terms.


<section class="flex-container">

<div class="flex-child">

$a)\;\;$ Wie viel sind $40\%$ von $6000\,€$?

<details class="spoiler">
  <summary>
    <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/Repetitorium/Kap7/diew1.png" width="30" height="30">
    Platz zum Rechnen - Klick mich!
  </summary>

  <div class="collab-wrap">
    @[Collaborative.lines(640,400)](./img/example.jpg)
  </div>
</details>

[[ 2400 ]]

</div>


<div class="flex-child">

$a)\;\;$ Wie viel sind $40\%$ von $6000\,€$?

<details class="spoiler">
  <summary>
    <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/Repetitorium/Kap7/diew1.png" width="30" height="30">
    Platz zum Rechnen - Klick mich!
  </summary>

  <div class="collab-wrap">
    @[Collaborative.lines(640,400)](./img/example.jpg)
  </div>
</details>

[[ 2400 ]]

</div>


<div class="flex-child">

$a)\;\;$ Wie viel sind $40\%$ von $6000\,€$?

<details class="spoiler">
  <summary>
    <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/Repetitorium/Kap7/diew1.png" width="30" height="30">
    Platz zum Rechnen - Klick mich!
  </summary>

  <div class="collab-wrap">
    @[Collaborative.lines(640,400)](./img/example.jpg)
  </div>
</details>

[[ 2400 ]]

</div>

</section>
