<!--
author: Martin Lommatzsch
version: 0.1.2
language: de
narrator: Deutsch Female
mode: Presentation
comment: Probeleistungskontrolle für Physik in Klasse 9 zur Energieversorgung mit Energieerhaltung, Wirkungsgraden, Thermodynamik, Klimabilanz und Kraftwerksbewertung.
tags: Physik, Klasse 9, Probeleistungskontrolle, Energieversorgung, Energieerhaltung, Wirkungsgrad, Exergie, Anergie, Entropie, Kraftwerke, Klimaphysik

@style
main > *:not(:last-child) {
  margin-bottom: 3rem;
}

input {
  text-align: center;
}
@end

import: https://raw.githubusercontent.com/MINT-the-GAP/lia-DynFlex/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-timer/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-board-mode/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-marker/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-annotation/refs/heads/main/README.md
import: https://raw.githubusercontent.com/liaTemplates/algebrite/master/README.md
import: https://raw.githubusercontent.com/liaTemplates/JSXGraph/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-canvas-ocr/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-orthography/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-Mathe/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-navigation/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-kachel/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-resetter/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-coordinate/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-freeze-v2/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-mathpath/refs/heads/master/README.md?v=0.0.24
-->

# Probeleistungskontrolle für Physik – Klasse 9: Energieversorgung

> Letztes Update am 19.11.2026

Diese Probearbeit enthält mehr Aufgaben als eine reguläre Leistungskontrolle. Nutze sie, um unterschiedliche Aufgabenarten zu wiederholen und deine Lösungswege selbstständig zu kontrollieren. Die Aufgaben sind teilweise etwas schwieriger als die Übungsaufgaben aus dem Unterricht.

> [!CAUTION]
> <h2>[Tutorial öffnen](https://liascript.github.io/course/?https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/Repetitorium/Erklaerungen/00_00_00_Tutorial.md)</h2>

Im Tutorial lernst du die Bedienung der Eingabefelder, Hinweise, Lösungen und Schreibflächen kennen. Kehre danach zu dieser Probeleistungskontrolle zurück.

> [!IMPORTANT]
> Trage bei Rechenaufgaben die Einheit direkt in das Eingabefeld ein. Dezimalpunkt und Dezimalkomma werden akzeptiert. Runde erst das Endergebnis und verwende möglichst ungerundete Zwischenergebnisse.

Wische weiter oder nutze unten links den Pfeil neben der Seitenzahl.

| Aufgabentyp | Aufgaben | Anzahl |
| --- | --- | ---: |
| Rechenaufgaben | 2, 3, 5, 6, 7, 9, 10, 11 | 8 |
| Verständnis-, Erklär- und Bewertungsaufgaben | 1, 4, 8, 12 | 4 |

Insgesamt sind **80 BE** erreichbar. Verwende, wenn nicht anders angegeben,

$$
g=9{,}81\,\frac{\mathrm m}{\mathrm{s^2}},
\qquad
1\,\mathrm{Wh}=3600\,\mathrm J,
\qquad
T\,[\mathrm K]=\vartheta\,[^\circ\mathrm C]+273{,}15.
$$

## Aufgabe 1: Primärenergie, Sekundärenergie und Energieumwandlung – Konzeptaufgabe

__$a)\;\;$__ **Ordne** die Beispiele als primäre oder sekundäre Energieträger beziehungsweise Energiequellen **zu**.

<!-- data-hint-button="1" data-solution-button="3" -->
[[ primär ] [ sekundär ]]
[   (X)          ( )    ] Kohle
[   (X)          ( )    ] Sonnenstrahlung
[   ( )          (X)    ] elektrische Energie
[   ( )          (X)    ] Wasserstoff aus Elektrolyse
[   (X)          ( )    ] Uran
[[?]] Primäre Energieträger oder Energiequellen kommen in der Natur vor. Sekundäre Energieträger werden technisch bereitgestellt.
******************
Kohle und Uran sind in der Natur vorhandene, nicht erneuerbare Primärenergieträger. Sonnenstrahlung ist eine erneuerbare primäre Energiequelle. Elektrische Energie und durch Elektrolyse bereitgestellter Wasserstoff entstehen erst durch technische Energieumwandlungen und werden deshalb als sekundär eingeordnet.
******************

@resetter

@ADetails(`3=BE;Mengen, Primärenergie, Sekundärenergie, Energieträger`)

---

__$b)\;\;$__ **Wähle** die einzige vollständig richtige Aussage zur Bereitstellung elektrischer Energie in einem Kohlekraftwerk **aus**.

<!-- data-hint-button="1" data-solution-button="3" -->
- [( )] Elektrische Energie ist Primärenergie, weil sie im Generator neu entsteht.
- [(X)] Chemische Energie der Kohle wird über innere und mechanische Energie in elektrische Energie umgewandelt; die elektrische Energie ist hier Sekundärenergie.
- [( )] Die Turbine wandelt elektrische Energie in chemische Energie der Kohle um.
- [( )] Da die Gesamtenergie erhalten bleibt, ist keine Energieübertragung an die Umgebung möglich.
[[?]] Verfolge die Energieumwandlung von der Kohle über Wasserdampf und Turbine bis zum Generator.
******************
Die chemische Energie der Kohle ist Primärenergie. Bei der Verbrennung wird sie zunächst in innere Energie des Arbeitsmediums umgewandelt. Der Dampf treibt die Turbine an; dadurch wird mechanische Energie bereitgestellt. Der Generator wandelt diese in elektrische Energie um. Die elektrische Energie ist hier Sekundärenergie. Zusätzlich wird thermische Energie an die Umgebung übertragen.
******************

@resetter

@ADetails(`3=BE;Mengen, Primärenergie, Sekundärenergie, Energieumwandlung`)

## Aufgabe 2: Bewegungsenergie und Leistung eines Autos – Rechenaufgabe

Ein Auto der Masse $m=1{,}60\,\mathrm t$ fährt auf einer ebenen Straße. Luft- und Rollwiderstand werden zunächst vernachlässigt.

<section class="dynFlex" data-basis="48%" data-min="30%">

<div class="flex-child">

__$a)\;\;$__ **Berechne** die kinetische Energie des Autos bei $100\,\mathrm{km/h}$. Gib das Ergebnis in Megajoule an und runde auf drei Nachkommastellen.

<!-- data-hint-button="2" data-solution-button="3" -->
$E_{\mathrm{kin},100}\approx$ [[ 0.617 MJ ]] @canvas
@Algebrite.check2(`0.6172839506MJ`,`0.0005MJ`)
[[?]] Wandle zuerst Kilometer pro Stunde in Meter pro Sekunde um.
[[?]] Verwende $E_{\mathrm{kin}}=\frac12mv^2$.
******************
$$
\begin{align*}
v&=100\,\frac{\mathrm{km}}{\mathrm h}
=100\cdot\frac{1000\,\mathrm m}{3600\,\mathrm s}
\approx27{,}778\,\frac{\mathrm m}{\mathrm s},\\
E_{\mathrm{kin},100}
&=\frac12\cdot1600\,\mathrm{kg}\cdot
\left(27{,}778\,\frac{\mathrm m}{\mathrm s}\right)^2\\
&\approx617284\,\mathrm J
=0{,}617\,\mathrm{MJ}.
\end{align*}
$$

Bei $100\,\mathrm{km/h}$ besitzt das Auto eine kinetische Energie von etwa $0{,}617\,\mathrm{MJ}$.
******************

@resetter

@ADetails(`2=BE;Einheiten, Potenzen, kinetische Energie`)

</div>

<div class="flex-child">

__$b)\;\;$__ Das Auto beschleunigt in $8{,}0\,\mathrm s$ von $50\,\mathrm{km/h}$ auf $100\,\mathrm{km/h}$. **Berechne** die Zunahme der kinetischen Energie und die dafür im Mittel bereitgestellte mechanische Leistung.

<!-- data-hint-button="2" data-solution-button="3" -->
$\Delta E_{\mathrm{kin}}\approx$ [[ 0.463 MJ ]] @canvas, $\quad \overline P\approx$ [[ 57.87 kW ]] @canvas
@Algebrite.check2(`[0.462962963MJ;57.8703704kW]`,`[0.0005MJ;0.005kW]`)
[[?]] Berechne die kinetische Energie bei beiden Geschwindigkeiten und bilde die Differenz.
[[?]] Nutze anschließend $\overline P=\Delta E/\Delta t$.
******************
Bei $50\,\mathrm{km/h}=13{,}889\,\mathrm{m/s}$ gilt

$$
E_{\mathrm{kin},50}
=\frac12\cdot1600\,\mathrm{kg}\cdot
\left(13{,}889\,\frac{\mathrm m}{\mathrm s}\right)^2
\approx0{,}154321\,\mathrm{MJ}.
$$

Damit folgen

$$
\begin{align*}
\Delta E_{\mathrm{kin}}
&=0{,}617284\,\mathrm{MJ}-0{,}154321\,\mathrm{MJ}
\approx0{,}462963\,\mathrm{MJ},\\
\overline P
&=\frac{0{,}462963\cdot10^6\,\mathrm J}{8{,}0\,\mathrm s}
\approx57{,}87\,\mathrm{kW}.
\end{align*}
$$

Die kinetische Energie nimmt um etwa $0{,}463\,\mathrm{MJ}$ zu. Dafür werden im Mittel etwa $57{,}87\,\mathrm{kW}$ mechanische Leistung bereitgestellt.
******************

@resetter

@ADetails(`3=BE;Einheiten, Leistung, kinetische Energie`)

</div>

<div class="flex-child">

__$c)\;\;$__ Bei einer Vollbremsung wird das Auto aus $100\,\mathrm{km/h}$ in $5{,}0\,\mathrm s$ zum Stillstand gebracht. **Berechne** den Betrag der mittleren Leistung, mit der kinetische Energie überwiegend in innere Energie der Bremsen, Reifen und Umgebung umgewandelt wird.

<!-- data-hint-button="2" data-solution-button="3" -->
$|\overline P_{\mathrm B}|\approx$ [[ 123.46 kW ]] @canvas
@Algebrite.check2(`123.4567901kW`,`0.005kW`)
[[?]] Die gesamte kinetische Energie aus Teilaufgabe a) wird während der Bremszeit umgewandelt.
******************
$$
|\overline P_{\mathrm B}|
=\frac{E_{\mathrm{kin},100}}{\Delta t}
=\frac{617284\,\mathrm J}{5{,}0\,\mathrm s}
\approx123457\,\mathrm W
=123{,}46\,\mathrm{kW}.
$$

Während der Vollbremsung werden im Mittel etwa $123{,}46\,\mathrm{kW}$ aus kinetischer Energie in andere Energieformen, vor allem innere Energie, umgewandelt.
******************

@resetter

@ADetails(`2=BE;Einheiten, Division, Bremsleistung`)

</div>

</section>

## Aufgabe 3: Energieerhaltung beim Fall – Rechenaufgabe

Eine Versorgungskapsel der Masse $m=320\,\mathrm{kg}$ bewegt sich am Rand einer $42{,}0\,\mathrm m$ hohen Plattform bereits mit $v_0=6{,}0\,\mathrm{m/s}$ abwärts. Luftwiderstand wird vernachlässigt. Der Boden ist das Nullniveau der potenziellen Energie.

__$a)\;\;$__ **Berechne** die anfängliche potenzielle und die anfängliche kinetische Energie.

<!-- data-hint-button="2" data-solution-button="3" -->
$E_{\mathrm{pot},0}=$ [[ 131.846 kJ ]] @canvas, $\quad E_{\mathrm{kin},0}=$ [[ 5.760 kJ ]] @canvas
@Algebrite.check2(`[131.8464kJ;5.76kJ]`,`[0.0005kJ;0.0005kJ]`)
[[?]] Verwende $E_{\mathrm{pot}}=mgh$ und $E_{\mathrm{kin}}=\frac12mv^2$.
******************
$$
\begin{align*}
E_{\mathrm{pot},0}
&=mgh
=320\,\mathrm{kg}\cdot9{,}81\,\frac{\mathrm m}{\mathrm{s^2}}\cdot42{,}0\,\mathrm m
=131{,}8464\,\mathrm{kJ},\\
E_{\mathrm{kin},0}
&=\frac12mv_0^2
=\frac12\cdot320\,\mathrm{kg}\cdot
\left(6{,}0\,\frac{\mathrm m}{\mathrm s}\right)^2
=5{,}760\,\mathrm{kJ}.
\end{align*}
$$

Die Kapsel besitzt anfangs $131{,}8464\,\mathrm{kJ}$ potenzielle und $5{,}760\,\mathrm{kJ}$ kinetische Energie.
******************

@resetter

@ADetails(`2=BE;Einheiten, potenzielle Energie, kinetische Energie`)

---

__$b)\;\;$__ **Berechne** die Geschwindigkeit der Kapsel unmittelbar vor dem Auftreffen auf den Boden.

<!-- data-hint-button="2" data-solution-button="3" -->
$v\approx$ [[ 29.33 m/s ]] @canvas
@Algebrite.check2(`29.3264386m/s`,`0.005m/s`)
[[?]] Setze die Summe der beiden Anfangsenergien mit der kinetischen Energie unmittelbar vor dem Auftreffen gleich.
[[?]] Löse die Gleichung erst allgemein nach $v$ auf.
******************
$$
\begin{align*}
\frac12mv_0^2+mgh&=\frac12mv^2,\\
v_0^2+2gh&=v^2,\\
v&=\sqrt{v_0^2+2gh}\\
&=\sqrt{\left(6{,}0\,\frac{\mathrm m}{\mathrm s}\right)^2
+2\cdot9{,}81\,\frac{\mathrm m}{\mathrm{s^2}}\cdot42{,}0\,\mathrm m}\\
&\approx29{,}33\,\frac{\mathrm m}{\mathrm s}.
\end{align*}
$$

Unmittelbar vor dem Auftreffen beträgt die Geschwindigkeit im Modell etwa $29{,}33\,\mathrm{m/s}$.
******************

@resetter

@ADetails(`3=BE;Wurzeln, Einheiten, Energieerhaltung`)

---

__$c)\;\;$__ **Begründe**, welche Aussage zur Masseabhängigkeit der Auftreffgeschwindigkeit im verwendeten Modell richtig ist. **Wähle** die vollständige Begründung **aus**.

<!-- data-hint-button="1" data-solution-button="3" -->
- [( )] Eine größere Masse führt immer zu einer größeren Auftreffgeschwindigkeit, weil die potenzielle Energie größer ist.
- [(X)] Die Masse kürzt sich aus $\frac12mv_0^2+mgh=\frac12mv^2$ heraus. Bei vernachlässigtem Luftwiderstand bleibt deshalb $v=\sqrt{v_0^2+2gh}$; in der Realität können unterschiedliche Strömungswiderstände zu verschiedenen Geschwindigkeiten führen.
- [( )] Die Geschwindigkeit ist masseunabhängig, weil schwere Körper keine Gewichtskraft besitzen.
- [( )] Die Masse kürzt sich nur dann heraus, wenn die Fallhöhe null ist.
[[?]] Betrachte den gemeinsamen Faktor $m$ in allen Energietermen und anschließend die Modellannahme zum Luftwiderstand.
******************
In der Gleichung

$$
\frac12mv_0^2+mgh=\frac12mv^2
$$

enthält jeder Term den gemeinsamen Faktor $m$. Da $m\ne0$ gilt, kann die Gleichung durch $m$ geteilt werden. Es bleibt

$$
v=\sqrt{v_0^2+2gh}.
$$

Deshalb ist die Auftreffgeschwindigkeit im verwendeten Modell masseunabhängig. In der Realität können Form, Querschnitt und Strömungswiderstand dazu führen, dass Körper verschieden schnell auftreffen.
******************

@resetter

@ADetails(`2=BE;Gleichung, Verhältnisse, Energieerhaltung, Luftwiderstand`)

## Aufgabe 4: Exergie, Anergie und Entropie – Konzeptaufgabe

Ein Erfinder behauptet, sein zyklisch arbeitendes Wärmekraftwerk wandle die gesamte zugeführte thermische Energie in elektrische Energie um. Eine Energieübertragung an eine kältere Umgebung sei nicht nötig. **Erkläre**, warum der Energieerhaltungssatz allein nicht genügt, um diese Behauptung zu beurteilen. 

<!-- data-hint-button="1" data-solution-button="3" -->
[[!]]
<script>true</script>
******************
Der erste Hauptsatz verlangt nur, dass die Gesamtenergie bilanziert wird. Er legt nicht fest, ob eine Energieumwandlung vollständig in der gewünschten Richtung möglich ist. Nach dem zweiten Hauptsatz wird bei einem realen Vorgang Entropie erzeugt. Dabei nimmt die Exergie ab und der Anergieanteil zu, obwohl die Gesamtenergie erhalten bleibt. Außerdem trägt die zugeführte thermische Energie Entropie in das Kraftwerk. Ein zyklisch arbeitendes Wärmekraftwerk muss deshalb thermische Energie und Entropie an ein kälteres Reservoir übertragen. Eine vollständige Umwandlung der zugeführten thermischen Energie in elektrische Energie ohne kaltes Reservoir ist daher nicht möglich.
******************

@resetter

@ADetails(`6=BE;Verhältnisse, Hauptsätze, Exergie, Anergie, Entropie`)

## Aufgabe 5: Wirkungsgrad eines Krans – Rechenaufgabe

Ein elektrisch angetriebener Kran hebt eine Last der Masse $1250\,\mathrm{kg}$ in $22{,}0\,\mathrm s$ um $14{,}0\,\mathrm m$ an. Währenddessen nimmt der Motor konstant $9{,}50\,\mathrm{kW}$ elektrische Leistung auf.

<section class="dynFlex" data-basis="48%" data-min="30%">

<div class="flex-child">

__$a)\;\;$__ **Berechne** die Zunahme der potenziellen Energie und die während des Hebens zugeführte elektrische Energie.

<!-- data-hint-button="2" data-solution-button="3" -->
$\Delta E_{\mathrm{pot}}=$ [[ 171.675 kJ ]] @canvas, $\quad E_{\mathrm{el,zu}}=$ [[ 209.000 kJ ]] @canvas
@Algebrite.check2(`[171.675kJ;209kJ]`,`[0.005kJ;0.005kJ]`)
[[?]] Verwende $\Delta E_{\mathrm{pot}}=mgh$ und $E=P\cdot t$.
******************
$$
\begin{align*}
\Delta E_{\mathrm{pot}}
&=1250\,\mathrm{kg}\cdot9{,}81\,\frac{\mathrm m}{\mathrm{s^2}}\cdot14{,}0\,\mathrm m
=171{,}675\,\mathrm{kJ},\\
E_{\mathrm{el,zu}}
&=9{,}50\,\mathrm{kW}\cdot22{,}0\,\mathrm s
=209{,}000\,\mathrm{kJ}.
\end{align*}
$$

Die Last erhält $171{,}675\,\mathrm{kJ}$ potenzielle Energie; dem Kran werden $209{,}000\,\mathrm{kJ}$ elektrische Energie zugeführt.
******************

@resetter

@ADetails(`2=BE;Einheiten, potenzielle Energie, elektrische Energie`)

</div>

<div class="flex-child">

__$b)\;\;$__ **Berechne** den Wirkungsgrad des Hebevorgangs.

<!-- data-hint-button="2" data-solution-button="3" -->
$\eta\approx$ [[ 82.14 % ]] @canvas
@Algebrite.check2(`0.8214114833`,`0.0002`,units=0)
[[?]] Setze Nutzenergie und zugeführte Energie in $\eta=E_{\mathrm{nutz}}/E_{\mathrm{zu}}$ ein.
******************
$$
\eta
=\frac{\Delta E_{\mathrm{pot}}}{E_{\mathrm{el,zu}}}
=\frac{171{,}675\,\mathrm{kJ}}{209{,}000\,\mathrm{kJ}}
\approx0{,}8214
=82{,}14\,\%.
$$

Der Wirkungsgrad des Hebevorgangs beträgt etwa $82{,}14\,\%$.
******************

@resetter

@ADetails(`2=BE;Prozentrechnung, Wirkungsgrad, Verhältnisse`)

</div>

<div class="flex-child">

__$c)\;\;$__ **Berechne** die Energie, die nicht in potenzielle Energie der Last umgewandelt wird. **Gib an**, in welche Energieform sie überwiegend umgewandelt wird.

<!-- data-hint-button="2" data-solution-button="3" -->
$E_{\mathrm{andere}}=$ [[ 37.325 kJ ]] @canvas
@Algebrite.check2(`37.325kJ`,`0.005kJ`)
[[?]] Bilde die Differenz aus zugeführter Energie und Nutzenergie.
******************
$$
E_{\mathrm{andere}}
=E_{\mathrm{el,zu}}-\Delta E_{\mathrm{pot}}
=209{,}000\,\mathrm{kJ}-171{,}675\,\mathrm{kJ}
=37{,}325\,\mathrm{kJ}.
$$

Die übrigen $37{,}325\,\mathrm{kJ}$ werden überwiegend in innere Energie von Motor, Getriebe, Seil und Umgebung umgewandelt.
******************

@resetter

@ADetails(`2=BE;Subtraktion, Einheiten, Energieumwandlung`)

</div>

</section>

## Aufgabe 6: Mehrstufige Wasserstoffkette – Rechenaufgabe

Eine Anlage speichert elektrische Energie über Wasserstoff. Die Energieumwandlungskette besitzt folgende Teilwirkungsgrade:

```mermaid
flowchart LR
  A[elektrische Energie] -->|Elektrolyse 72 %| B[chemische Energie des Wasserstoffs]
  B -->|Verdichtung und Speicherung 94 %| C[gespeicherter Wasserstoff]
  C -->|Brennstoffzelle 56 %| D[elektrische Energie]
  D -->|Wechselrichter 96 %| E[elektrische Energie im Netz]
```

Am Anfang werden $2{,}50\,\mathrm{MWh}=9{,}00\,\mathrm{GJ}$ elektrische Energie zugeführt.

__$a)\;\;$__ **Berechne** den Gesamtwirkungsgrad der Kette.

<!-- data-hint-button="2" data-solution-button="3" -->
$\eta_{\mathrm{ges}}\approx$ [[ 36.38 % ]] @canvas
@Algebrite.check2(`0.36384768`,`0.0002`,units=0)
[[?]] Multipliziere die vier Teilwirkungsgrade als Dezimalzahlen.
******************
$$
\eta_{\mathrm{ges}}
=0{,}72\cdot0{,}94\cdot0{,}56\cdot0{,}96
=0{,}36384768
\approx36{,}38\,\%.
$$

Der Gesamtwirkungsgrad der Wasserstoffkette beträgt etwa $36{,}38\,\%$.
******************

@resetter

@ADetails(`2=BE;Prozentrechnung, Multiplikation, Wirkungsgradkette`)

---

__$b)\;\;$__ **Berechne** die am Ende bereitgestellte elektrische Energie und die insgesamt in andere Energieformen umgewandelte Energie. Gib beide Ergebnisse in Gigajoule an.

<!-- data-hint-button="2" data-solution-button="3" -->
$E_{\mathrm{nutz}}\approx$ [[ 3.275 GJ ]] @canvas, $\quad E_{\mathrm{andere}}\approx$ [[ 5.725 GJ ]] @canvas
@Algebrite.check2(`[3.27462912GJ;5.72537088GJ]`,`[0.0005GJ;0.0005GJ]`)
[[?]] Nutze $E_{\mathrm{nutz}}=\eta_{\mathrm{ges}}E_{\mathrm{zu}}$ und anschließend die Energiebilanz.
******************
$$
\begin{align*}
E_{\mathrm{nutz}}
&=0{,}36384768\cdot9{,}00\,\mathrm{GJ}
\approx3{,}274629\,\mathrm{GJ},\\
E_{\mathrm{andere}}
&=9{,}00\,\mathrm{GJ}-3{,}274629\,\mathrm{GJ}
\approx5{,}725371\,\mathrm{GJ}.
\end{align*}
$$

Am Ende werden etwa $3{,}275\,\mathrm{GJ}$ elektrische Energie bereitgestellt. Rund $5{,}725\,\mathrm{GJ}$ werden innerhalb der Kette vor allem in innere Energie umgewandelt und an die Umgebung übertragen.
******************

@resetter

@ADetails(`2=BE;Einheiten, Prozentrechnung, Energiebilanz`)

---

__$c)\;\;$__ Am Ende sollen $1{,}00\,\mathrm{MWh}=3{,}60\,\mathrm{GJ}$ elektrische Energie bereitgestellt werden. **Berechne** die dafür am Anfang mindestens benötigte elektrische Energie.

<!-- data-hint-button="2" data-solution-button="3" -->
$E_{\mathrm{zu}}\approx$ [[ 9.894 GJ ]] @canvas
@Algebrite.check2(`9.894250253GJ`,`0.0005GJ`)
[[?]] Rechne die Kette rückwärts mit $E_{\mathrm{zu}}=E_{\mathrm{nutz}}/\eta_{\mathrm{ges}}$.
******************
$$
E_{\mathrm{zu}}
=\frac{3{,}60\,\mathrm{GJ}}{0{,}36384768}
\approx9{,}894\,\mathrm{GJ}.
$$

Für $3{,}60\,\mathrm{GJ}$ elektrische Energie am Ausgang müssen am Anfang mindestens etwa $9{,}894\,\mathrm{GJ}$ elektrische Energie zugeführt werden.
******************

@resetter

@ADetails(`2=BE;Division, Prozentrechnung, Wirkungsgradkette`)

## Aufgabe 7: Pumpspeicherkraftwerk – Rechenaufgabe

Ein Pumpspeicherkraftwerk soll später $18{,}0\,\mathrm{MWh}=64{,}8\,\mathrm{GJ}$ elektrische Energie an das Netz übertragen. Die Höhendifferenz beträgt $85{,}0\,\mathrm m$. Speicheränderungen während der Wartezeit werden vernachlässigt.

| Ladeweg | Wirkungsgrad | Entladeweg | Wirkungsgrad |
| --- | ---: | --- | ---: |
| Transformator | $98{,}5\,\%$ | Turbine | $92{,}0\,\%$ |
| Motor | $96{,}0\,\%$ | Generator | $97{,}0\,\%$ |
| Pumpe und Rohrleitung | $90{,}0\,\%$ | Transformator | $98{,}5\,\%$ |

__$a)\;\;$__ **Berechne** den Gesamtwirkungsgrad für Laden und Entladen.

<!-- data-hint-button="2" data-solution-button="3" -->
$\eta_{\mathrm{ges}}\approx$ [[ 74.81 % ]] @canvas
@Algebrite.check2(`0.74807607456`,`0.0002`,units=0)
[[?]] Multipliziere alle sechs Teilwirkungsgrade.
******************
$$
\begin{align*}
\eta_{\mathrm L}&=0{,}985\cdot0{,}960\cdot0{,}900=0{,}85104,\\
\eta_{\mathrm E}&=0{,}920\cdot0{,}970\cdot0{,}985=0{,}879014,\\
\eta_{\mathrm{ges}}&=\eta_{\mathrm L}\eta_{\mathrm E}
=0{,}74807607456
\approx74{,}81\,\%.
\end{align*}
$$

Der Gesamtwirkungsgrad beträgt etwa $74{,}81\,\%$.
******************

@resetter

@ADetails(`2=BE;Prozentrechnung, Multiplikation, Pumpspeicherkraftwerk`)

---

__$b)\;\;$__ **Berechne** die beim Laden aus dem Netz benötigte elektrische Energie und die Differenz zur später abgegebenen elektrischen Energie. Gib beide Ergebnisse in Gigajoule an.

<!-- data-hint-button="2" data-solution-button="3" -->
$E_{\mathrm{Netz,zu}}\approx$ [[ 86.622 GJ ]] @canvas, $\quad E_{\mathrm{andere}}\approx$ [[ 21.822 GJ ]] @canvas
@Algebrite.check2(`[86.62220622GJ;21.82220622GJ]`,`[0.0005GJ;0.0005GJ]`)
[[?]] Rechne mit $E_{\mathrm{Netz,zu}}=E_{\mathrm{Netz,ab}}/\eta_{\mathrm{ges}}$ rückwärts.
******************
$$
\begin{align*}
E_{\mathrm{Netz,zu}}
&=\frac{64{,}8\,\mathrm{GJ}}{0{,}74807607456}
\approx86{,}622\,\mathrm{GJ},\\
E_{\mathrm{andere}}
&=86{,}622\,\mathrm{GJ}-64{,}8\,\mathrm{GJ}
\approx21{,}822\,\mathrm{GJ}.
\end{align*}
$$

Beim Laden müssen etwa $86{,}622\,\mathrm{GJ}$ elektrische Energie zugeführt werden. Davon werden über den gesamten Speicherzyklus etwa $21{,}822\,\mathrm{GJ}$ in andere Energieformen umgewandelt.
******************

@resetter

@ADetails(`3=BE;Einheiten, Division, Energiebilanz`)

---

__$c)\;\;$__ **Berechne** die mindestens hochzupumpende Wassermasse. Bestimme dafür zuerst die potenzielle Energie im Oberbecken aus dem Wirkungsgrad des Entladewegs.

<!-- data-hint-button="2" data-solution-button="3" -->
$m\approx$ [[ 8.84e7 kg ]] @canvas
@Algebrite.check2(`8.840794194e7kg`,`2e5kg`)
[[?]] Vor dem Entladen muss $E_{\mathrm{pot}}=E_{\mathrm{Netz,ab}}/\eta_{\mathrm E}$ gespeichert sein.
[[?]] Nutze anschließend $m=E_{\mathrm{pot}}/(gh)$.
******************
Zuerst wird die notwendige potenzielle Energie im Oberbecken bestimmt:

$$
E_{\mathrm{pot}}
=\frac{64{,}8\,\mathrm{GJ}}{0{,}879014}
\approx73{,}71896\,\mathrm{GJ}.
$$

Damit folgt

$$
\begin{align*}
m&=\frac{E_{\mathrm{pot}}}{gh}\\
&=\frac{73{,}71896\cdot10^9\,\mathrm J}
{9{,}81\,\mathrm{m/s^2}\cdot85{,}0\,\mathrm m}\\
&\approx8{,}84\cdot10^7\,\mathrm{kg}.
\end{align*}
$$

Es müssen mindestens etwa $8{,}84\cdot10^7\,\mathrm{kg}$ Wasser in das Oberbecken gepumpt werden.
******************

@resetter

@ADetails(`2=BE;Einheiten, potenzielle Energie, Äquivalenzumformung`)

## Aufgabe 8: Aufbau und Funktion von Kraftwerken – Konzeptaufgabe

**Vergleiche** Kohle- und Kernkraftwerk mit einer Windkraftanlage. Gehe auf die anfängliche Energieform, gemeinsame Bauteile, Unterschiede der Umwandlungskette, den thermischen Kreisprozess und die Abgabe thermischer Energie an die Umgebung ein. Ordne außerdem Photovoltaik und Geothermie begründet in den Vergleich ein.

<!-- data-hint-button="1" data-solution-button="3" -->
[[!]]
[[?]] Ein Vergleich benötigt Gemeinsamkeiten und Unterschiede anhand derselben Kriterien.
<script>true</script>
******************
Ein Kohlekraftwerk beginnt mit chemischer Energie, ein Kernkraftwerk mit Kernenergie und eine Windkraftanlage mit kinetischer Energie der Luft. Kohle- und Kernkraftwerk übertragen zunächst Energie auf ein Arbeitsmedium. Wasserdampf treibt eine Turbine an, die mit einem Generator gekoppelt ist. Beide Anlagen benötigen außerdem eine Kühlung und übertragen einen erheblichen Anteil der zugeführten Energie als thermische Energie an die Umgebung. Eine Windkraftanlage besitzt ebenfalls Rotor beziehungsweise Turbine und Generator, benötigt aber keinen thermischen Kreisprozess. Deshalb entfallen Kessel, Dampferzeuger und Kühlturm. Bei ihr wird die kinetische Energie der Luft über mechanische Energie in elektrische Energie umgewandelt; auch dabei werden kleinere Anteile in innere Energie und Schall umgewandelt. Photovoltaik wandelt Strahlungsenergie ohne Turbine direkt in elektrische Energie um. Ein Geothermiekraftwerk nutzt innere Energie aus dem Erdinneren und kann wie ein thermisches Kraftwerk Dampf, Turbine, Generator und Kühlung verwenden.
******************

@resetter

@ADetails(`6=BE;Verhältnisse, Vergleichen, Kraftwerke, Energieumwandlung`)

## Aufgabe 9: Wärmekraftwerk und Carnot-Grenze – Rechenaufgabe

Ein Wärmekraftwerk arbeitet zwischen einer heißen Temperatur von $540\,^{\circ}\mathrm C$ und einer kalten Temperatur von $30\,^{\circ}\mathrm C$. Es gibt $720\,\mathrm{MW}$ elektrische Leistung ab und besitzt einen realen Wirkungsgrad von $42{,}0\,\%$.

__$a)\;\;$__ **Berechne** beide Temperaturen in Kelvin.

<!-- data-hint-button="1" data-solution-button="3" -->
$T_{\mathrm h}=$ [[ 813.15 K ]] @canvas, $\quad T_{\mathrm k}=$ [[ 303.15 K ]] @canvas
@Algebrite.check2(`[813.15K;303.15K]`,`[0.005K;0.005K]`)
[[?]] Addiere zu jeder Celsius-Temperatur $273{,}15$.
******************
$$
T_{\mathrm h}=540+273{,}15=813{,}15\,\mathrm K,
\qquad
T_{\mathrm k}=30+273{,}15=303{,}15\,\mathrm K.
$$

Die heiße Temperatur beträgt $813{,}15\,\mathrm K$, die kalte Temperatur $303{,}15\,\mathrm K$.
******************

@resetter

@ADetails(`2=BE;Einheiten, Addition, Temperatur`)

---

__$b)\;\;$__ **Berechne** den theoretisch maximalen Carnot-Wirkungsgrad.

<!-- data-hint-button="2" data-solution-button="3" -->
$\eta_{\mathrm C}\approx$ [[ 62.72 % ]] @canvas
@Algebrite.check2(`0.6271905552`,`0.0002`,units=0)
[[?]] Verwende $\eta_{\mathrm C}=1-T_{\mathrm k}/T_{\mathrm h}$ und setze Kelvin-Temperaturen ein.
******************
$$
\eta_{\mathrm C}
=1-\frac{T_{\mathrm k}}{T_{\mathrm h}}
=1-\frac{303{,}15\,\mathrm K}{813{,}15\,\mathrm K}
\approx0{,}62719
=62{,}72\,\%.
$$

Der theoretisch maximale Wirkungsgrad beträgt etwa $62{,}72\,\%$.
******************

@resetter

@ADetails(`2=BE;Prozentrechnung, Verhältnisse, Carnot-Wirkungsgrad`)

---

__$c)\;\;$__ **Berechne** die zugeführte thermische Leistung und die thermische Leistung, die im realen Kraftwerk an die Umgebung übertragen wird.

<!-- data-hint-button="2" data-solution-button="3" -->
$P_{\mathrm{th,zu}}\approx$ [[ 1.714 GW ]] @canvas, $\quad P_{\mathrm{th,Umgebung}}\approx$ [[ 994.29 MW ]] @canvas
@Algebrite.check2(`[1.714285714GW;994.285714MW]`,`[0.0005GW;0.005MW]`)
[[?]] Aus $\eta=P_{\mathrm{el}}/P_{\mathrm{th,zu}}$ folgt $P_{\mathrm{th,zu}}=P_{\mathrm{el}}/\eta$.
[[?]] Bilde anschließend die Differenz der Leistungen.
******************
$$
\begin{align*}
P_{\mathrm{th,zu}}
&=\frac{720\,\mathrm{MW}}{0{,}420}
\approx1714{,}286\,\mathrm{MW}
=1{,}714\,\mathrm{GW},\\
P_{\mathrm{th,Umgebung}}
&=1714{,}286\,\mathrm{MW}-720\,\mathrm{MW}
\approx994{,}29\,\mathrm{MW}.
\end{align*}
$$

Dem Kraftwerk werden etwa $1{,}714\,\mathrm{GW}$ thermische Leistung zugeführt. Rund $994{,}29\,\mathrm{MW}$ werden als thermische Leistung an die Umgebung übertragen.
******************

@resetter

@ADetails(`3=BE;Einheiten, Leistung, Wirkungsgrad`)

---

__$d)\;\;$__ **Berechne**, welchen Anteil des Carnot-Wirkungsgrads das reale Kraftwerk erreicht.

<!-- data-hint-button="2" data-solution-button="3" -->
$\dfrac{\eta}{\eta_{\mathrm C}}\approx$ [[ 66.97 % ]] @canvas
@Algebrite.check2(`0.6696529412`,`0.0002`,units=0)
[[?]] Teile den realen Wirkungsgrad durch den Carnot-Wirkungsgrad.
******************
$$
\frac{\eta}{\eta_{\mathrm C}}
=\frac{0{,}420}{0{,}6271905552}
\approx0{,}66965
=66{,}97\,\%.
$$

Das reale Kraftwerk erreicht etwa $66{,}97\,\%$ des theoretisch maximalen Carnot-Wirkungsgrads.
******************

@resetter

@ADetails(`2=BE;Prozentrechnung, Division, Carnot-Wirkungsgrad`)

## Aufgabe 10: Strahlungsbilanz und Klimasystem – Rechenaufgabe

Im vereinfachten globalen Modell treffen im Mittel $342\,\mathrm{W/m^2}$ Sonnenstrahlung auf die Obergrenze der Atmosphäre. Anfangs werden $107\,\mathrm{W/m^2}$ reflektiert und $235\,\mathrm{W/m^2}$ als thermische Strahlung in den Weltraum übertragen. Die Bilanz ist ausgeglichen.

Durch eine vorübergehende Verdunkelung der Oberfläche sinkt die reflektierte Leistung auf $105\,\mathrm{W/m^2}$. Die abgegebene thermische Strahlungsleistung bleibt während der ersten $30$ Tage näherungsweise konstant. Betrachte eine Region mit $500\,000\,\mathrm{km^2}$.

__$a)\;\;$__ **Berechne** die nun absorbierte Strahlungsleistung pro Fläche und die positive Leistungsbilanz pro Fläche.

<!-- data-hint-button="2" data-solution-button="3" -->
$p_{\mathrm{abs}}=$ [[ 237 W/m^2 ]] @canvas, $\quad \Delta p=$ [[ 2 W/m^2 ]] @canvas
@Algebrite.check2(`[237W/m^2;2W/m^2]`,`[0.05W/m^2;0.05W/m^2]`)
[[?]] Subtrahiere die reflektierte von der einfallenden Leistung pro Fläche.
[[?]] Vergleiche das Ergebnis mit der weiterhin abgegebenen thermischen Strahlungsleistung.
******************
$$
\begin{align*}
p_{\mathrm{abs}}
&=342\,\frac{\mathrm W}{\mathrm{m^2}}-105\,\frac{\mathrm W}{\mathrm{m^2}}
=237\,\frac{\mathrm W}{\mathrm{m^2}},\\
\Delta p
&=237\,\frac{\mathrm W}{\mathrm{m^2}}-235\,\frac{\mathrm W}{\mathrm{m^2}}
=2\,\frac{\mathrm W}{\mathrm{m^2}}.
\end{align*}
$$

Das Klimasystem absorbiert nun $237\,\mathrm{W/m^2}$; vorübergehend ergibt sich eine positive Bilanz von $2\,\mathrm{W/m^2}$.
******************

@resetter

@ADetails(`2=BE;Einheiten, Subtraktion, Strahlungsbilanz`)

---

__$b)\;\;$__ **Berechne** die zusätzliche Leistung für die gesamte Region.

<!-- data-hint-button="2" data-solution-button="3" -->
$\Delta P=$ [[ 1.00e12 W ]] @canvas
@Algebrite.check2(`1e12W`,`1e9W`)
[[?]] Es gilt $1\,\mathrm{km^2}=10^6\,\mathrm{m^2}$. Multipliziere anschließend Leistungsbilanz und Fläche.
******************
$$
A=500\,000\,\mathrm{km^2}
=500\,000\cdot10^6\,\mathrm{m^2}
=5{,}0\cdot10^{11}\,\mathrm{m^2}.
$$

Damit gilt

$$
\Delta P
=\Delta p\cdot A
=2\,\frac{\mathrm W}{\mathrm{m^2}}\cdot5{,}0\cdot10^{11}\,\mathrm{m^2}
=1{,}00\cdot10^{12}\,\mathrm W.
$$

Die zusätzliche Leistung beträgt im vereinfachten Modell $1{,}00\cdot10^{12}\,\mathrm W$.
******************

@resetter

@ADetails(`2=BE;Potenzen, Einheiten, Flächenumrechnung`)

---

__$c)\;\;$__ **Berechne** die Energie, die unter diesen Annahmen während der $30$ Tage zusätzlich im Klimasystem verbleibt. Gib das Ergebnis in Joule an.

<!-- data-hint-button="2" data-solution-button="3" -->
$\Delta E=$ [[ 2.592e18 J ]] @canvas
@Algebrite.check2(`2.592e18J`,`1e15J`)
[[?]] Rechne $30$ Tage in Sekunden um und verwende $E=P\cdot t$.
******************
$$
t=30\cdot24\cdot3600\,\mathrm s
=2{,}592\cdot10^6\,\mathrm s.
$$

Damit folgt

$$
\Delta E
=\Delta P\cdot t
=1{,}00\cdot10^{12}\,\mathrm W\cdot2{,}592\cdot10^6\,\mathrm s
=2{,}592\cdot10^{18}\,\mathrm J.
$$

Unter den vereinfachenden Annahmen verbleiben in den $30$ Tagen zusätzlich $2{,}592\cdot10^{18}\,\mathrm J$ im Klimasystem. In der Realität würde die veränderte Temperatur die thermische Abstrahlung beeinflussen.
******************

@resetter

@ADetails(`2=BE;Potenzen, Einheiten, Energieübertragung`)

## Aufgabe 11: Kraftwerksmix und Lebenszyklus-Emissionen – Rechenaufgabe

Ein Versorgungsgebiet benötigt im Jahr $72\,\mathrm{TWh}$ elektrische Energie. Geplant sind $6{,}0\,\mathrm{GW}$ Offshore-Windleistung und $20\,\mathrm{GW}$ Photovoltaik. Der verbleibende Jahresbedarf soll im Modell durch regelbare Gaskraftwerke gedeckt werden.

| Technologie | Jahresenergie je $1\,\mathrm{GW}$ installierter Leistung | Lebenszyklus-Emissionen |
| --- | ---: | ---: |
| Offshore-Wind | $7{,}0\,\mathrm{TWh}$ | $4\,\mathrm{g\,CO_2e/kWh}$ |
| Photovoltaik | $1{,}0\,\mathrm{TWh}$ | $33\,\mathrm{g\,CO_2e/kWh}$ |
| Gaskraftwerk | $4{,}5\,\mathrm{TWh}$ | $117\,\mathrm{g\,CO_2e/kWh}$ |

__$a)\;\;$__ **Berechne** die Jahresenergien von Wind und Photovoltaik sowie die verbleibende Jahresenergie für die Gaskraftwerke. Gib die Ergebnisse in Petajoule an. Es gilt $1\,\mathrm{TWh}=3{,}6\,\mathrm{PJ}$.

<!-- data-hint-button="2" data-solution-button="3" -->
$E_{\mathrm W}=$ [[ 151.2 PJ ]] @canvas, $\quad E_{\mathrm{PV}}=$ [[ 72.0 PJ ]] @canvas, $\quad E_{\mathrm G}=$ [[ 36.0 PJ ]] @canvas
@Algebrite.check2(`[151.2PJ;72PJ;36PJ]`,`[0.05PJ;0.05PJ;0.05PJ]`)
[[?]] Berechne zunächst die drei Energien in Terawattstunden und wandle danach mit dem angegebenen Faktor um.
******************
$$
\begin{align*}
E_{\mathrm W}
&=6{,}0\,\mathrm{GW}\cdot7{,}0\,\frac{\mathrm{TWh}}{\mathrm{GW}}
=42\,\mathrm{TWh}
=151{,}2\,\mathrm{PJ},\\
E_{\mathrm{PV}}
&=20\,\mathrm{GW}\cdot1{,}0\,\frac{\mathrm{TWh}}{\mathrm{GW}}
=20\,\mathrm{TWh}
=72{,}0\,\mathrm{PJ},\\
E_{\mathrm G}
&=(72-42-20)\,\mathrm{TWh}
=10\,\mathrm{TWh}
=36{,}0\,\mathrm{PJ}.
\end{align*}
$$

Wind stellt im Modell $151{,}2\,\mathrm{PJ}$, Photovoltaik $72{,}0\,\mathrm{PJ}$ und Gas $36{,}0\,\mathrm{PJ}$ elektrische Energie im Jahr bereit.
******************

@resetter

@ADetails(`3=BE;Einheiten, Multiplikation, Subtraktion, Strommix`)

---

__$b)\;\;$__ **Berechne** die benötigte installierte Gaskraftwerksleistung und den Anteil von Wind- und Solarenergie an der Jahresenergie.

<!-- data-hint-button="2" data-solution-button="3" -->
$P_{\mathrm G}\approx$ [[ 2.222 GW ]] @canvas, $\quad a_{\mathrm{erneuerbar}}\approx$ [[ 86.11 % ]] @canvas
@Algebrite.check2(`[2.222222222GW;0.8611111111]`,`[0.0005GW;0.0002]`)
[[?]] Für Gas werden $10\,\mathrm{TWh}$ benötigt. Teile durch die Jahresenergie je Gigawatt.
[[?]] Für den Anteil werden Wind- und Solarenergie addiert und durch $72\,\mathrm{TWh}$ geteilt.
******************
$$
\begin{align*}
P_{\mathrm G}
&=\frac{10\,\mathrm{TWh}}{4{,}5\,\mathrm{TWh/GW}}
\approx2{,}222\,\mathrm{GW},\\
a_{\mathrm{erneuerbar}}
&=\frac{42\,\mathrm{TWh}+20\,\mathrm{TWh}}{72\,\mathrm{TWh}}
\approx0{,}8611
=86{,}11\,\%.
\end{align*}
$$

Im Modell werden etwa $2{,}222\,\mathrm{GW}$ Gaskraftwerksleistung benötigt. Wind und Photovoltaik stellen zusammen etwa $86{,}11\,\%$ der Jahresenergie bereit.
******************

@resetter

@ADetails(`2=BE;Prozentrechnung, Division, Kraftwerksleistung`)

---

__$c)\;\;$__ **Berechne** die gesamten Lebenszyklus-Emissionen des modellierten Jahres in Kilogramm $\mathrm{CO_2e}$ und die mittlere Emissionsintensität in $\mathrm{kg/GJ}$.

<!-- data-hint-button="2" data-solution-button="3" -->
$m_{\mathrm{CO_2e}}=$ [[ 1.998e9 kg ]] @canvas, $\quad I\approx$ [[ 7.708 kg/GJ ]] @canvas
@Algebrite.check2(`[1.998e9kg;7.708333333kg/GJ]`,`[2e6kg;0.005kg/GJ]`)
[[?]] Es gilt $1\,\mathrm{TWh}=10^9\,\mathrm{kWh}$. Multipliziere für jede Technologie Energie und Emissionsfaktor.
[[?]] Die gesamte Jahresenergie beträgt $72\,\mathrm{TWh}=259{,}2\,\mathrm{PJ}=259{,}2\cdot10^6\,\mathrm{GJ}$.
******************
$$
\begin{align*}
m_{\mathrm W}
&=42\cdot10^9\,\mathrm{kWh}\cdot4\,\frac{\mathrm g}{\mathrm{kWh}}
=0{,}168\cdot10^9\,\mathrm{kg},\\
m_{\mathrm{PV}}
&=20\cdot10^9\,\mathrm{kWh}\cdot33\,\frac{\mathrm g}{\mathrm{kWh}}
=0{,}660\cdot10^9\,\mathrm{kg},\\
m_{\mathrm G}
&=10\cdot10^9\,\mathrm{kWh}\cdot117\,\frac{\mathrm g}{\mathrm{kWh}}
=1{,}170\cdot10^9\,\mathrm{kg}.
\end{align*}
$$

Somit gilt

$$
m_{\mathrm{CO_2e}}
=(0{,}168+0{,}660+1{,}170)\cdot10^9\,\mathrm{kg}
=1{,}998\cdot10^9\,\mathrm{kg}.
$$

Die mittlere Emissionsintensität ist

$$
I=\frac{1{,}998\cdot10^9\,\mathrm{kg}}
{259{,}2\cdot10^6\,\mathrm{GJ}}
\approx7{,}708\,\mathrm{kg/GJ}.
$$

Das entspricht $27{,}75\,\mathrm{g/kWh}$. Die Lebenszyklus-Emissionen des modellierten Jahres betragen insgesamt $1{,}998\cdot10^9\,\mathrm{kg\,CO_2e}$.
******************

@resetter

@ADetails(`3=BE;Potenzen, Einheiten, Lebenszyklus-Emissionen`)

## Aufgabe 12: Energieversorgung einer Berghütte – Konzeptaufgabe

Eine abgelegene Berghütte besitzt keinen Anschluss an das öffentliche Stromnetz. Sie soll ganzjährig zuverlässig mit elektrischer Energie für Beleuchtung, Kühlung, eine Wasserpumpe und einen Notruf versorgt werden.

**Entwirf** ein geeignetes Versorgungssystem. **Stelle** deinen Entwurf in einer beschrifteten Skizze dar und **begründe** deine Entscheidungen mit physikalischem Wissen.

<!-- data-hint-button="1" data-solution-button="3" -->
[[!]]
[[?]] Denke auch an Zeiten, in denen deine gewählte Energiequelle nur wenig Leistung abgibt.
<script>true</script>
******************
Eine mögliche Lösung kombiniert Photovoltaikmodule mit einer kleinen Windkraftanlage. Die Photovoltaikmodule wandeln Strahlungsenergie und die Windkraftanlage kinetische Energie der Luft in elektrische Energie um. Beim Laden des Batteriespeichers wird elektrische in chemische Energie umgewandelt; beim Entladen wird chemische wieder in elektrische Energie umgewandelt. Ein Laderegler steuert die Energieübertragung zwischen Anlagen, Speicher und Geräten. Wichtige Geräte wie Wasserpumpe und Kühlschrank können bevorzugt betrieben werden, wenn genügend Leistung zur Verfügung steht. Für längere Zeiten mit wenig Sonne und Wind ist zusätzlich eine begründete Reserve nötig, beispielsweise ein weiterer ausreichend großer Speicher oder ein Notstromaggregat. Beim Aggregat wird chemische Energie über innere und mechanische Energie in elektrische Energie umgewandelt; dabei werden thermische Energie und Abgase an die Umgebung abgegeben.

Andere fachlich begründete Lösungen sind möglich. An einem geeigneten Standort könnte beispielsweise auch fließendes Wasser einbezogen werden. Entscheidend sind eine nachvollziehbare Energieumwandlungskette, eine Speichermöglichkeit und eine Lösung für längere Zeiten mit geringer verfügbarer Leistung.
******************

@resetter

@ADetails(`6=BE;Verhältnisse, Entwerfen, Energieumwandlung, Speicher, Versorgungssicherheit`)

## Bearbeitungsstand sichern und auswerten

Prüfe vor dem Sichern, ob du alle zwölf Aufgaben bearbeitet hast. Mit der Abgabefunktion kannst du einen Link zu deinem aktuellen Bearbeitungsstand erzeugen. Die Auswertung zeigt dir die Ergebnisse der automatischen Selbstchecks.

@Abgabe

@Auswertung
