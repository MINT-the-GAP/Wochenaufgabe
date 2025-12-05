<!--
version:  0.0.2
language: de

tags: Demo
comment: Fächerbezogener Beispielkurs mit interaktiven Elemente in LiaScript für den Schulunterricht
author: Martin Lommatzsch, André Dietrich, Sebastian Zug


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

import: https://raw.githubusercontent.com/liaTemplates/algebrite/master/README.md
import: https://raw.githubusercontent.com/LiaTemplates/Tikz-Jax/main/README.md
import: https://raw.githubusercontent.com/LiaTemplates/mermaid_template/0.1.4/README.md

script: https://cdn.jsdelivr.net/gh/LiaTemplates/Tikz-Jax@main/dist/index.js


import: https://raw.githubusercontent.com/liaTemplates/ABCjs/main/README.md
        https://raw.githubusercontent.com/LiaTemplates/Speech-Recognition-Quiz/refs/heads/main/README.md
        https://raw.githubusercontent.com/liaTemplates/AVR8js/main/README.md
        https://raw.githubusercontent.com/liaTemplates/JSXGraph/main/README.md
        https://raw.githubusercontent.com/LiaTemplates/mec2/main/README.md
        https://raw.githubusercontent.com/LiaTemplates/CollaborativeDrawing/main/README.md
        https://raw.githubusercontent.com/LiaTemplates/SpreadSheet/refs/heads/main/README.md
        https://github.com/LiaTemplates/PeriodicTable/blob/main/README.md

persistent: true

edit: true

eingabe: <script input="number" input-always-active modify="false" value="0" default="0">@input</script>

-->





#  Stochastik - Aufgabe 9: 




Gegeben ist eine Zufallsvariable $X$ mit $X \sim B(n = 50, p)$.

Es soll überprüft werden, ob die Erfolgswahrscheinlichkeit $p$ eher
„klein“ ($p = 0{,}17$) oder „etwas größer“ ($p = 0{,}23$) ist.

Wir legen ein Signifikanzniveau von $\alpha = 10\,\%$ fest und wollen
einen zweiseitigen Test verwenden:

> Wir verwerfen $H_0$, wenn $X \le k_{\text{unten}}$ oder
> $X \ge k_{\text{oben}}$ gilt.  
> Sonst (für $k_{\text{unten}} < X < k_{\text{oben}}$) behalten wir $H_0$ bei.

Die beiden ganzen Zahlen $k_{\text{unten}}$ und $k_{\text{oben}}$ sollen so gewählt werden,
dass das Signifikanzniveau $\alpha = 10\,\%$ nicht überschritten wird.


---

__$a)\;\;$__ **Formuliere** die Nullhypothese $H_0$ und die Gegenhypothese (alternative Hypothese) $H_1$.

[[!]]
<script>true</script>
********************

Es werden zwei feste Werte für $p$ verglichen:

- Nullhypothese:  
  $H_0:\; p = 0{,}17$

- Gegenhypothese:  
  $H_1:\; p = 0{,}23$

********************

__$b)\;\;$__ **Bestimme** die passenden Grenzwerte $k_{\text{unten}}$ und $k_{\text{oben}}$.

$k_{\text{unten}} = $ [[ 3 ]] $\;\;\wedge\;\;$
$k_{\text{oben}} = $ [[ 13 ]]
********************

Unter $H_0$ gilt $X \sim B(50, 0{,}17)$.

Zuerst berechnen wir Erwartungswert und Standardabweichung:

- Erwartungswert:
  $$
  \mu = n p = 50 \cdot 0{,}17 = 8{,}5
  $$
- Standardabweichung:
  $$
  \sigma = \sqrt{n p (1-p)}
  = \sqrt{50 \cdot 0{,}17 \cdot 0{,}83}
  \approx \sqrt{23{,}605} \approx 2{,}66
  $$

Für einen zweiseitigen Test mit $\alpha = 10\,\%$ verwenden wir
$z \approx 1{,}645$ und erhalten als groben Annahmebereich:
$$
\mu \pm z \sigma
= 8{,}5 \pm 1{,}645 \cdot 2{,}66
\approx 8{,}5 \pm 4{,}4
$$
also näherungsweise:
$$
4 \lesssim X \lesssim 13.
$$

Daraus bietet sich als Annahmebereich der ganzzahlige Bereich
$$
4 \le X \le 12
$$
an und damit als Verwerfungsbereich:
$$
X \le 3 \quad \text{oder} \quad X \ge 13.
$$

Nun prüfen wir mit der Binomialverteilung, ob damit
$\alpha \le 0{,}10$ gilt:

- $P(X \le 3 \mid p = 0{,}17) \approx 0{,}0208$
- $P(X \ge 13 \mid p = 0{,}17) \approx 0{,}0714$

Damit:
$$
P(X \le 3) + P(X \ge 13)
\approx 0{,}0208 + 0{,}0714
= 0{,}0922 \le 0{,}10.
$$

Also sind $k_{\text{unten}} = 3$ und $k_{\text{oben}} = 13$
eine zulässige Wahl für den zweiseitigen Verwerfungsbereich.

********************


__$c)\;\;$__ **Berechne** den tatsächlichen $\alpha$-Fehler dieses Tests mit den gefundenen Grenzen.

$\alpha \approx $ [[ 9,22 ]]$\,\%$
@Algebrite.check2(9.22,0.1)
********************

Unter $H_0$ gilt $X \sim B(50, 0{,}17)$.

Der $\alpha$-Fehler ist die Wahrscheinlichkeit, dass wir $H_0$ verwerfen,
obwohl $p = 0{,}17$ stimmt:
$$
\alpha
= P(X \le 3 \mid p = 0{,}17)
+ P(X \ge 13 \mid p = 0{,}17).
$$

Mit dem Taschenrechner erhält man näherungsweise:
$$
P(X \le 3) \approx 0{,}0208,
\qquad
P(X \ge 13) \approx 0{,}0714.
$$

Also:
$$
\alpha \approx 0{,}0208 + 0{,}0714 = 0{,}0922.
$$

In Prozent:
$$
\alpha \approx 9{,}22\,\%.
$$

********************


__$d)\;\;$__ **Berechne** den $\beta$-Fehler dieses Tests, wenn in Wirklichkeit $p = 0{,}23$ gilt.

$\beta \approx $ [[ 64,02 ]]$\,\%$
@Algebrite.check2(64.02,0.2)
********************

Jetzt betrachten wir die Gegenhypothese:
$H_1:\; p = 0{,}23$.

Dann gilt $X \sim B(50, 0{,}23)$.

Der $\beta$-Fehler ist die Wahrscheinlichkeit, dass wir $H_0$ beibehalten,
obwohl in Wirklichkeit $p = 0{,}23$ ist.

Beibehalten von $H_0$ bedeutet:
$$
k_{\text{unten}} < X < k_{\text{oben}}
\quad\Rightarrow\quad
4 \le X \le 12.
$$

Also:
$$
\beta = P(4 \le X \le 12 \mid p = 0{,}23)
= P(X \le 12 \mid p = 0{,}23) - P(X \le 3 \mid p = 0{,}23).
$$

Mit dem Taschenrechner erhält man näherungsweise:
$$
P(X \le 3 \mid p = 0{,}23) \approx 0{,}0014,
\qquad
P(X \le 12 \mid p = 0{,}23) \approx 0{,}6415.
$$

Damit:
$$
\beta \approx 0{,}6415 - 0{,}0014 = 0{,}6401.
$$

In Prozent:
$$
\beta \approx 64{,}01\,\%.
$$

********************


__$e)\;\;$__ **Erkläre** in eigenen Worten, was $\alpha$- und $\beta$-Fehler in dieser Situation bedeuten.

[[!]]
<script>true</script>
********************

- Der $\alpha$-Fehler (ca. $9{,}2\,\%$):  
  Das ist die Wahrscheinlichkeit, dass der Test $H_0:\; p = 0{,}17$
  verwirft (also sagt: „$p$ ist eher $0{,}23$“),
  obwohl in Wirklichkeit $p = 0{,}17$ ist.

- Der $\beta$-Fehler (ca. $64{,}0\,\%$):  
  Das ist die Wahrscheinlichkeit, dass der Test $H_0:\; p = 0{,}17$
  nicht verwirft (also bei „$p = 0{,}17$“ bleibt),
  obwohl in Wirklichkeit $p = 0{,}23$ ist.

********************

