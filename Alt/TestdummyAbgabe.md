<!--
version:  0.0.1
language: de

import: https://raw.githubusercontent.com/MINT-the-GAP/lia-DynFlex/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-timer/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-board-mode/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-marker/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-annotation/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-canvas-ocr/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-orthography/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-Mathe/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-kachel/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-mathpath/refs/heads/master/README.md

import: https://raw.githubusercontent.com/MINT-the-GAP/lia-llm/refs/heads/main/README.md

import: https://raw.githubusercontent.com/liaTemplates/algebrite/master/README.md
import: https://raw.githubusercontent.com/liaTemplates/JSXGraph/main/README.md

import: https://raw.githubusercontent.com/MINT-the-GAP/lia-resetter/main/README.md

import: https://raw.githubusercontent.com/MINT-the-GAP/lia-coordinate/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-freeze-v2/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/main/imports/RedirecterREADME.md


author: Martin Lommatzsch
-->

# Minimalbeispiel

**Gib** den beschriebenen Anteilswert **an**.

<section class="dynFlex">
<div class="flex-child">

<!-- data-solution-button="2" data-solution-timer="60s" data-solution-timer-start="oncheck" -->
__$a)\;\;$__ Wie viel sind $\dfrac{9}{4}$ von $720\,$kg?  \
 [[  1620  ]]kg @canvas
@Algebrite.check(1620)
***************
$$
\begin{align*}
  \dfrac{9}{4} \cdot 720\,\text{kg} & = \dfrac{9 \cdot 720}{4} \,\text{kg} \\
  & = 9 \cdot 180 \,\text{kg} 
  & = 1620 \,\text{kg} 
\end{align*}
$$
***************

</div>
</section>

@ADetails(3=BE;Bruchrechnung)

@Abgabe

@Auswertung(F12;Tab;Time)