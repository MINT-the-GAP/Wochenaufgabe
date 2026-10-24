<!--
author: Martin Lommatzsch
version: 1.0.0
language: de
narrator: Deutsch Female
mode: Presentation
comment: Probeleistungskontrolle für Klasse 12 zu Wellenbrechung, mechanischen und elektromagnetischen Schwingungen sowie zur Wellengleichung. Mit Einheitenprüfung, Hinweisen und Musterlösungen.
tags: Physik, Klasse 12, Probeleistungskontrolle, Wellen, Schwingungen, Brechung, Federpendel, LC-Schwingkreis

import: https://raw.githubusercontent.com/MINT-the-GAP/lia-board-mode/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-marker/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-annotation/refs/heads/main/README.md
import: https://raw.githubusercontent.com/liaTemplates/algebrite/master/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-canvas-ocr/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-llm/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-navigation/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-resetter/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-freeze-v2/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-mathpath/refs/heads/master/README.md
-->

# Probeleistungskontrolle für Physik – Klasse 12: Schwingungen und Wellen

> Letztes Update am 09.10.2026

Wische weiter oder klicke unten links neben der Seitenzahl auf den Pfeil nach rechts.

Diese Probearbeit hat mehr Aufgaben als die richtige Arbeit, damit du genug zum Üben hast. Es sind viele verschiedene Aufgabentypen abgebildet, sodass du alles nochmal bei der Bearbeitung dieser Aufgaben wiederholst.

Gib berechnete Größen mit Einheit ein, zum Beispiel `1,5 m/s` oder `1.5 m/s`. Gleichwertige SI-Einheiten werden akzeptiert. Runde erst das Endergebnis; kleine Rundungsabweichungen werden berücksichtigt. Über das Stiftsymbol kannst du eine Antwort handschriftlich eingeben.

Bei der Brechung rechnest du im Gradmaß, bei Schwingungen und Wellen im Bogenmaß. Gib den Winkel mit `°` oder `deg` ein, beispielsweise `30°`.

Hinweise helfen dir beim Rechenweg; die zusätzliche Erklärhilfe erläutert passende mathematische Grundlagen. Offene Antworten erhalten einen KI-gestützten Selbstcheck. Bei der ersten Nutzung kann dafür ein Modelldownload erforderlich sein. Am Ende kannst du deinen Bearbeitungsstand sichern und auswerten.

## Aufgabe 1: Brechung von Wasserwellen

Eine Wasserwelle läuft aus einem Bereich 1 in einen Bereich 2 mit anderer Wassertiefe.
Die Ausbreitungsgeschwindigkeit der Welle ändert sich dabei von $v_1$ zu $v_2$.
Für den Übergang gilt das Snellius’sche Brechungsgesetz für Wellen:

$$
\frac{\sin(\alpha_1)}{\sin(\alpha_2)} \;=\; \frac{v_1}{v_2}
$$

Dabei ist:

- $\alpha_1$ der Einfallswinkel (gemessen gegen das Lot auf die Grenzlinie),
- $\alpha_2$ der Brechungswinkel nach dem Übergang,
- $v_1$ die Wellengeschwindigkeit vor dem Übergang,
- $v_2$ die Wellengeschwindigkeit nach dem Übergang.

Gib Winkel in Grad mit 2 Dezimalstellen an.

__$a)\;\;$__ Die Welle trifft mit dem Einfallswinkel $\alpha_1 = 30^\circ$ auf die Grenzschicht.
Die Geschwindigkeiten sind $v_1 = 2{,}40\,\text{m/s}$ in Bereich 1 und $v_2 = 1{,}60\,\text{m/s}$ in Bereich 2.

Bestimme den Brechungswinkel $\alpha_2$.

<!-- data-hint-button="1" data-solution-button="3" -->
$\alpha_2\approx$ [[ 19.47° ]] @canvas
<script>
const raw = window.normalizeInputToArray(String.raw`@input`)[0] ?? "";
const normalized = raw
  .replace(/\\(?:mathrm|text)\{(deg|°)\}/g, "$1")
  .replace(/\^\{\\circ\}|\^\\circ|\\circ/g, "°")
  .trim();
const angle = normalized.match(/^([+-]?(?:\d+(?:[.,]\d*)?|[.,]\d+))\s*(?:°|deg)$/i);
angle !== null && Math.abs(Number(angle[1].replace(",", ".")) - 19.4712206345) <= 0.005;
</script>
[[?]] Stelle nach $\sin(\alpha_2)$ um und verwende anschließend den Arkussinus im Gradmaß.
[[?]] @Explain
******************
$$
\begin{align*}
\frac{\sin(\alpha_1)}{\sin(\alpha_2)} &= \frac{v_1}{v_2} \\
\Rightarrow \sin(\alpha_2)
&= \sin(\alpha_1) \cdot \frac{v_2}{v_1} \\[6pt]
\sin(\alpha_1) &= \sin(30^\circ) = 0{,}5 \\
\frac{v_2}{v_1} &= \frac{1{,}60}{2{,}40} = 0{,}666\ldots \\
\sin(\alpha_2) &= 0{,}5 \cdot 0{,}666\ldots = 0{,}333\ldots \\[6pt]
\alpha_2 &= \arcsin(0{,}333\ldots) \approx 19{,}47^\circ
\end{align*}
$$
******************

@resetter

@ADetails(`2=BE;Verhältnisse, Brechung, Winkel`)

---

__$b)\;\;$__ Eine Wasserwelle läuft nun aus Bereich 1 in Bereich 2 mit
$v_1 = 3\,\dfrac{\text{m}}{\text{s}}$.
Die gemessenen Winkel sind $\alpha_1 = 40^\circ$ und $\alpha_2 = 25^\circ$.

Berechne die Wellengeschwindigkeit $v_2$ im Bereich 2.

Runde auf zwei Nachkommastellen in Metern pro Sekunde.

<!-- data-hint-button="1" data-solution-button="3" -->
$v_2\approx$ [[ 1.97 m/s ]] @canvas
@Algebrite.check2(`1.9724525683m/s`,`0.005m/s`)
[[?]] Es gilt $v_2=v_1\cdot\sin(\alpha_2)/\sin(\alpha_1)$. Verwende den Gradmodus.
[[?]] @Explain
******************
$$
\begin{align*}
\frac{\sin(\alpha_1)}{\sin(\alpha_2)} &= \frac{v_1}{v_2} \\
\Rightarrow v_2 &= v_1 \cdot \frac{\sin(\alpha_2)}{\sin(\alpha_1)} \\[8pt]
\sin(40^\circ) &\approx 0{,}6428 \\
\sin(25^\circ) &\approx 0{,}4226 \\[6pt]
v_2 &= 3{,}00\,\dfrac{\text{m}}{\text{s}} \cdot \frac{0{,}4226}{0{,}6428} \\
    &\approx 1{,}97\,\dfrac{\text{m}}{\text{s}}
\end{align*}
$$
******************

@resetter

@ADetails(`2=BE;Verhältnisse, Brechung, Geschwindigkeit`)

---

__$c)\;\;$__ Leite aus $\sin(\alpha_1)/\sin(\alpha_2)=v_1/v_2$ eine allgemeine Gleichung für $\alpha_2$ her. Zeige die Umformungsschritte. Es gelten $v_1,v_2>0$ und $0^\circ\leq\alpha_1,\alpha_2\leq90^\circ$; eine gebrochene Welle ist möglich.

<!-- data-hint-button="1" data-solution-button="off" data-llm-textarea="6" -->
[[Antwort]]
[[?]] Isoliere zuerst $\sin(\alpha_2)$; wende danach auf beide Seiten den Arkussinus an.
[[?]] @Explain
```text @LLMQuiz(0.55;coverage=1;solution=1;feedback=1;assessmentengine=quality;Rechtschreibung=0;Satzbau=0;maxthinkingtime=15s;maxthinkingtokens=medium,`Leite aus $\sin(\alpha_1)/\sin(\alpha_2)=v_1/v_2$ eine allgemeine Gleichung für $\alpha_2$ her. Zeige die Umformungsschritte. Es gelten $v_1,v_2>0$ und $0^\circ\leq\alpha_1,\alpha_2\leq90^\circ$; eine gebrochene Welle ist möglich.`)
<!-- lia-llm:criterion -->
Die Umformung ergibt $\sin(\alpha_2)=\sin(\alpha_1)\,v_2/v_1$.
<!-- lia-llm:criterion -->
Durch Anwenden des Arkussinus folgt $\alpha_2=\arcsin(\sin(\alpha_1)\,v_2/v_1)$.
<!-- lia-llm:solution -->
$$
\begin{align*}
\frac{\sin(\alpha_1)}{\sin(\alpha_2)} &= \frac{v_1}{v_2} \\[6pt]
\Rightarrow \sin(\alpha_2)
&= \sin(\alpha_1)\,\frac{v_2}{v_1} \\[6pt]
\Rightarrow \alpha_2
&= \arcsin \!\left(
\sin(\alpha_1)\,\frac{v_2}{v_1}
\right)
\end{align*}
$$
```

@ADetails(`3=BE;Äquivalenzumformung, Brechung`)

---

__$d)\;\;$__ Bei einem weiteren Übergang zwischen zwei Wasserbereichen werden $\alpha_1=35^\circ$ und $\alpha_2=50^\circ$ gemessen. Ist $v_2$ größer oder kleiner als $v_1$? Begründe mit dem Brechungsgesetz in ganzen Sätzen.

<!-- data-hint-button="1" data-solution-button="off" data-llm-textarea="6" -->
[[Antwort]]
[[?]] Vergleiche die Sinuswerte der beiden Winkel zwischen $0^\circ$ und $90^\circ$.
[[?]] @Explain
```text @LLMQuiz(0.55;coverage=1;solution=1;feedback=1;assessmentengine=quality;Rechtschreibung=1;Satzbau=1;maxthinkingtime=15s;maxthinkingtokens=medium,`Bei einem weiteren Übergang zwischen zwei Wasserbereichen werden $\alpha_1=35^\circ$ und $\alpha_2=50^\circ$ gemessen. Ist $v_2$ größer oder kleiner als $v_1$? Begründe mit dem Brechungsgesetz in ganzen Sätzen.`)
<!-- lia-llm:criterion -->
Für diese Winkel gilt $\sin(\alpha_2)>\sin(\alpha_1)$.
<!-- lia-llm:criterion -->
Nach dem Brechungsgesetz ist $v_1/v_2=\sin(35^\circ)/\sin(50^\circ)<1$.
<!-- lia-llm:criterion -->
Daraus folgt $v_2>v_1$: Die Welle breitet sich nach dem Übergang schneller aus.
<!-- lia-llm:solution -->
Für Winkel zwischen $0^\circ$ und $90^\circ$ wächst der Sinus mit dem Winkel. Daher gilt

$$
\frac{v_1}{v_2}=\frac{\sin(35^\circ)}{\sin(50^\circ)}\approx0{,}749<1.
$$

Somit ist $v_2>v_1$: Die Welle ist nach dem Übergang schneller.
```

@ADetails(`2=BE;Verhältnisse, Brechung, Begründen`)

## Aufgabe 2: Mechanische Schwingung

Ein Wagen der Masse $m$ ist an einer horizontalen Feder befestigt (reibungslos).
Die Feder wird um $s = 2{,}8 \,\text{cm}$ zusammengedrückt und gespeichert ist dabei eine Spannenergie von $E_\text{sp} = 0{,}15 \,\text{mJ}$.
Anschließend wird losgelassen und der Wagen führt eine harmonische Schwingung aus.

Hinweise und Gleichungen:

- $E_\text{sp} = \dfrac{1}{2} D s^2$
- $\omega = \sqrt{\dfrac{D}{m}}$
- $T = \dfrac{2\pi}{\omega}$
- $x(t) = A \sin(\omega t + \varphi_0)$
- $v_\text{max} = A \cdot \omega$
- $F_\text{Feder,max} = D \cdot A$

__$a)\;\;$__ Bestimme die Federkonstante $D$ aus der gespeicherten Spannenergie.

Runde auf drei Nachkommastellen in Newton pro Meter.

<!-- data-hint-button="1" data-solution-button="3" -->
$D\approx$ [[ 0.383 N/m ]] @canvas
@Algebrite.check2(`0.3826530612N/m`,`0.0005N/m`)
[[?]] Rechne Zentimeter in Meter und Millijoule in Joule um. Stelle dann nach $D$ um.
[[?]] @Explain
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

@resetter

@ADetails(`2=BE;Einheiten, Spannenergie, Federkonstante`)

---

__$b)\;\;$__ Berechne die Kreisfrequenz $\omega$ und die Periodendauer $T$ der Schwingung für die angehängte Masse $m = 0{,}180 \,\text{kg}$.

Runde $\omega$ auf drei Nachkommastellen in $\mathrm{s}^{-1}$ und $T$ auf zwei Nachkommastellen in Sekunden.

<!-- data-hint-button="1" data-solution-button="3" -->
$\omega\approx$ [[ 1.458/s ]] @canvas, $\quad T\approx$ [[ 4.31 s ]] @canvas
@Algebrite.check2(`[1.4580296088/s;4.3093674293s]`,`[0.0005/s;0.005s]`)
[[?]] Verwende möglichst den ungerundeten Wert von $D$ und berechne zuerst $\omega$.
[[?]] @Explain
******************
$$
\begin{align*}
\omega &= \sqrt{\frac{D}{m}}
\approx \sqrt{\frac{0{,}382653 \,\text{N/m}}{0{,}180 \,\text{kg}}} \\[6pt]
&\approx \sqrt{2{,}125850 \,\text{s}^{-2}}
\approx 1{,}458 \,\text{s}^{-1} \\[10pt]
T &= \frac{2\pi}{\omega}
\approx \frac{2\pi}{1{,}4580296 \,\text{s}^{-1}}
\approx 4{,}309 \,\text{s}
\approx 4{,}31 \,\text{s}
\end{align*}
$$
******************

@resetter

@ADetails(`3=BE;Wurzeln, Kreisfrequenz, Periodendauer`)

---

__$c)\;\;$__ Für diese Teilaufgabe wird dieselbe Schwingung mit einem anderen Anfangszustand betrachtet: $\varphi_0=\pi/4$ und $A=2{,}8\,\mathrm{cm}$.

1. **Gib** die Schwingungsgleichung $x(t)$ an. Trage dazu den dimensionslosen Faktor $x(t)/A$ ein; schreibe im Eingabefeld `w` für $\omega$.
2. **Berechne** $x(0{,}50\,\mathrm{s})$ und runde auf zwei Nachkommastellen in Zentimetern.

<!-- data-hint-button="1" data-solution-button="3" -->
$\dfrac{x(t)}{A}=$ [[ sin(w*t+pi/4) ]] @canvas
@Algebrite.check(`sin(w*t+pi/4)`)
[[?]] Setze die gegebene Anfangsphase in $x(t)=A\sin(\omega t+\varphi_0)$ ein.
[[?]] @Explain
******************
Die vollständige Schwingungsgleichung lautet

$$
x(t)=A\sin\!\left(\omega t+\frac{\pi}{4}\right)
\approx0{,}028\,\mathrm{m}\sin\!\left(1{,}458\,\mathrm{s}^{-1}t+\frac{\pi}{4}\right).
$$
******************

@resetter

@ADetails(`2=BE;Gleichung, Schwingungsgleichung, Phase`)

Berechne nun die momentane Auslenkung.

<!-- data-hint-button="1" data-solution-button="3" -->
$x(0{,}50\,\mathrm{s})\approx$ [[ 2.80 cm ]] @canvas
@Algebrite.check2(`2.7955504625cm`,`0.005cm`)
[[?]] Setze $t=0{,}50\,\mathrm{s}$ in die Schwingungsgleichung ein. Der Sinus erwartet hier das Bogenmaß.
[[?]] @Explain
******************
$$
\begin{align*}
x(t) &= A \sin(\omega t + \varphi_0) \\[4pt]
A &= 0{,}028 \,\text{m}, \quad
\omega \approx 1{,}458 \,\text{s}^{-1}, \quad
\varphi_0 = \frac{\pi}{4} \\[6pt]
\Rightarrow x(t)
&= 0{,}028 \,\text{m} \cdot
\sin \!\big( 1{,}458\,\mathrm{s}^{-1}t + \frac{\pi}{4} \big) \\[10pt]
x(0{,}50 \,\text{s})
&= 0{,}028 \,\text{m} \cdot
\sin \!\big( 1{,}458\,\mathrm{s}^{-1} \cdot 0{,}50\,\mathrm{s} + \frac{\pi}{4} \big) \\
&\approx 0{,}02796 \,\text{m} \\
&\approx 2{,}80 \,\text{cm}
\end{align*}
$$
******************

@resetter

@ADetails(`2=BE;Einheiten, Schwingungsgleichung, Phase`)

---

__$d)\;\;$__ Bestimme zwei charakteristische Größen dieser Schwingung:

1. die maximale Geschwindigkeit $v_\text{max}$,
2. die maximale Rückstellkraft $F_\text{Feder,max}$ der Feder.

Runde beide Größen in SI-Einheiten auf vier Nachkommastellen.

<!-- data-hint-button="1" data-solution-button="3" -->
$v_\mathrm{max}\approx$ [[ 0.0408 m/s ]] @canvas, $\quad F_\mathrm{Feder,max}\approx$ [[ 0.0107 N ]] @canvas
@Algebrite.check2(`[0.0408248290m/s;0.0107142857N]`,`[0.00005m/s;0.00005N]`)
[[?]] Verwende $A=0{,}028\,\mathrm{m}$ sowie $v_\mathrm{max}=A\omega$ und $F_\mathrm{Feder,max}=DA$.
[[?]] @Explain
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

@resetter

@ADetails(`3=BE;Einheiten, Geschwindigkeit, Rückstellkraft`)

## Aufgabe 3: Idealer LC-Schwingkreis

Es wird ein idealer LC-Schwingkreis aus einer Spule mit Induktivität $L$ und einem Kondensator mit Kapazität $C$ betrachtet.

Zu Beginn ($t = 0$) ist der Kondensator vollständig aufgeladen mit der Spannung $U_0$. Es fließt zum Zeitpunkt $t=0$ noch kein Strom ($i(0)=0$).

Für einen idealen LC-Schwingkreis gilt:

- Kreisfrequenz: $\omega = \dfrac{1}{\sqrt{L \, C}}$
- Periodendauer: $T = \dfrac{2\pi}{\omega}$
- Kondensatorspannung: $u_C(t) = U_0 \cos(\omega t)$
- Stromstärke im Kreis: $i(t) = C \, \dfrac{du_C}{dt} = -C \, U_0 \, \omega \, \sin(\omega t)$

Gegeben:

- $L = 20 \,\text{mH} = 20 \cdot 10^{-3}\,\text{H}$
- $C = 4{,}7 \,\mu\text{F} = 4{,}7 \cdot 10^{-6}\,\text{F}$
- $U_0 = 5{,}0 \,\text{V}$

Die positive Stromrichtung ist durch $i=C\,du_C/dt$ festgelegt.

__$a)\;\;$__ **Berechne** die Kreisfrequenz $\omega$ und die Periodendauer $T$. Runde $\omega$ auf ganze $\mathrm{s}^{-1}$ und $T$ auf drei Nachkommastellen in Millisekunden.

<!-- data-hint-button="1" data-solution-button="3" -->
$\omega\approx$ [[ 3262/s ]] @canvas, $\quad T\approx$ [[ 1.926 ms ]] @canvas
@Algebrite.check2(`[3261.6403652672/s;1.9263881371ms]`,`[0.5/s;0.0005ms]`)
[[?]] Wandle $L$ und $C$ in Henry und Farad um. Berechne $T$ zunächst in Sekunden und dann in Millisekunden.
[[?]] @Explain
******************
$$
\begin{aligned}
\omega&=\frac{1}{\sqrt{LC}}
=\frac{1}{\sqrt{(20\cdot10^{-3}\,\mathrm{H})(4{,}7\cdot10^{-6}\,\mathrm{F})}}
\approx3261{,}640\,\mathrm{s}^{-1},\\
T&=2\pi\sqrt{LC}\approx0{,}001926388\,\mathrm{s}
\approx1{,}926\,\mathrm{ms}.
\end{aligned}
$$

Die Kreisfrequenz beträgt gerundet $3262\,\mathrm{s}^{-1}$, die Periodendauer $1{,}926\,\mathrm{ms}$.
******************

@resetter

@ADetails(`3=BE;Einheiten, LC-Schwingkreis, Periodendauer`)

---

__$b)\;\;$__ Stelle für $L=20\,\mathrm{mH}$, $C=4{,}7\,\mu\mathrm{F}$ und $U_0=5{,}0\,\mathrm{V}$ die zeitabhängige Kondensatorspannung $u_C(t)$ und die Stromstärke $i(t)$ explizit mit Zahlenwerten und Einheiten auf. Zu Beginn ist der Kondensator vollständig geladen und $i(0)=0$; es gilt $i=C\,du_C/dt$. Runde die Kreisfrequenz auf ganze $\mathrm{s}^{-1}$ und die Stromamplitude auf vier Nachkommastellen in Ampere.

<!-- data-hint-button="1" data-solution-button="off" data-llm-textarea="6" -->
[[Antwort]]
[[?]] Die Spannung beginnt bei ihrem Maximum. Leite sie nach der Zeit ab und multipliziere mit $C$.
[[?]] @Explain
```text @LLMQuiz(0.55;coverage=1;solution=1;feedback=1;assessmentengine=quality;Rechtschreibung=0;Satzbau=0;maxthinkingtime=15s;maxthinkingtokens=medium,`Stelle für $L=20\,\mathrm{mH}$, $C=4{,}7\,\mu\mathrm{F}$ und $U_0=5{,}0\,\mathrm{V}$ die zeitabhängige Kondensatorspannung $u_C(t)$ und die Stromstärke $i(t)$ explizit mit Zahlenwerten und Einheiten auf. Zu Beginn ist der Kondensator vollständig geladen und $i(0)=0$; es gilt $i=C\,du_C/dt$. Runde die Kreisfrequenz auf ganze $\mathrm{s}^{-1}$ und die Stromamplitude auf vier Nachkommastellen in Ampere.`)
<!-- lia-llm:criterion -->
Die Spannung lautet näherungsweise $u_C(t)=5{,}0\,\mathrm{V}\cos(3262\,\mathrm{s}^{-1}t)$; äquivalente Phasendarstellungen sind richtig.
<!-- lia-llm:criterion -->
Die Stromstärke lautet näherungsweise $i(t)=-0{,}0766\,\mathrm{A}\sin(3262\,\mathrm{s}^{-1}t)$; äquivalente Phasendarstellungen sind richtig.
<!-- lia-llm:solution -->
$$
\begin{aligned}
u_C(t)&=U_0\cos(\omega t)
\approx5{,}0\,\mathrm{V}\cos(3262\,\mathrm{s}^{-1}t),\\
i(t)&=C\frac{du_C}{dt}=-CU_0\omega\sin(\omega t)
\approx-0{,}0766\,\mathrm{A}\sin(3262\,\mathrm{s}^{-1}t).
\end{aligned}
$$

Hier ist $CU_0\omega\approx0{,}0766485\,\mathrm{A}$. Die Zeit $t$ wird als Größe mit Einheit eingesetzt; die Argumente der Winkelfunktionen sind dimensionslos. Bei $t=0$ gilt $u_C=U_0$ und $i=0$.
```

@ADetails(`4=BE;Gleichung, LC-Schwingkreis, Funktionen`)

---

__$c)\;\;$__ Bestimme die momentane Kondensatorspannung $u_C(t)$ und die momentane Stromstärke $i(t)$ zum Zeitpunkt $t = 0{,}25 \,\text{ms}$.

Runde die Spannung auf drei und die Stromstärke auf vier Nachkommastellen in den angegebenen SI-Einheiten.

<!-- data-hint-button="1" data-solution-button="3" -->
$u_C(0{,}25\,\mathrm{ms})\approx$ [[ 3.428 V ]] @canvas, $\quad i(0{,}25\,\mathrm{ms})\approx$ [[ -0.0558 A ]] @canvas
@Algebrite.check2(`[3.4278495092V;-0.0558006650A]`,`[0.0005V;0.00005A]`)
[[?]] Es gilt $0{,}25\,\mathrm{ms}=0{,}00025\,\mathrm{s}$. Verwende für Sinus und Kosinus das Bogenmaß.
[[?]] @Explain
******************
Verwende $t=0{,}00025\,\mathrm{s}$ und die ungerundete Kreisfrequenz aus $\omega=1/\sqrt{LC}$.

$$
\begin{aligned}
\omega t&\approx0{,}815410,\\
u_C(t)&=5{,}0\,\mathrm{V}\cos(\omega t)
\approx3{,}4278495\,\mathrm{V}\approx3{,}428\,\mathrm{V},\\
i(t)&=-(4{,}7\cdot10^{-6}\,\mathrm{F})(5{,}0\,\mathrm{V})\omega\sin(\omega t)
\approx-0{,}0558007\,\mathrm{A}\approx-0{,}0558\,\mathrm{A}.
\end{aligned}
$$

Die Spannung beträgt etwa $3{,}428\,\mathrm{V}$, die Stromstärke etwa $-0{,}0558\,\mathrm{A}$.
******************

@resetter

@ADetails(`3=BE;Einheiten, LC-Schwingkreis, Momentanwerte`)

---

__$d)\;\;$__ Interpretiere das Vorzeichen des Stroms aus Teilaufgabe c). Warum ist $i(0{,}25\,\mathrm{ms})$ negativ, obwohl $u_C(0{,}25\,\mathrm{ms})$ noch positiv ist? Begründe mit $i=C\,du_C/dt$ in ganzen Sätzen.

<!-- data-hint-button="1" data-solution-button="off" data-llm-textarea="6" -->
[[Antwort]]
[[?]] Unterscheide den Wert der Spannung von ihrer zeitlichen Änderung. Hier gilt $i=C\,du_C/dt$.
[[?]] @Explain
```text @LLMQuiz(0.55;coverage=1;solution=1;feedback=1;assessmentengine=quality;Rechtschreibung=1;Satzbau=1;maxthinkingtime=15s;maxthinkingtokens=medium,`Interpretiere das Vorzeichen des Stroms aus Teilaufgabe c). Warum ist $i(0{,}25\,\mathrm{ms})$ negativ, obwohl $u_C(0{,}25\,\mathrm{ms})$ noch positiv ist? Begründe mit $i=C\,du_C/dt$ in ganzen Sätzen.`)
<!-- lia-llm:criterion -->
Die positive Kondensatorspannung nimmt zu diesem Zeitpunkt ab.
<!-- lia-llm:criterion -->
Daher gilt $du_C/dt<0$ und wegen $i=C\,du_C/dt$ ist der Strom in der festgelegten Bezugsrichtung negativ.
<!-- lia-llm:criterion -->
Der Kondensator entlädt sich; das negative Vorzeichen bedeutet eine Stromrichtung entgegen der gewählten positiven Richtung.
<!-- lia-llm:solution -->
Die Kondensatorspannung ist noch positiv, nimmt aber ab. Deshalb ist ihre zeitliche Ableitung negativ. Wegen $i=C\,du_C/dt$ und $C>0$ ist auch $i$ negativ. Der Kondensator entlädt sich; der Strom fließt entgegen der festgelegten positiven Bezugsrichtung.

Dabei wird elektrische Feldenergie des Kondensators in magnetische Feldenergie der Spule umgewandelt. Im idealen LC-Schwingkreis bleibt die Gesamtenergie erhalten.
```

@ADetails(`2=BE;Negative Zahlen, Stromrichtung, Energieumwandlung`)

## Aufgabe 4: Mechanische Wellen

Eine mechanische Welle breitet sich entlang einer Schnur in $+x$-Richtung aus.
Für ihre Auslenkung gilt:

$$
y(x;t) \;=\; A \,\sin\!\left(
2\pi \left[
\frac{t}{T} \;-\; \frac{x}{\lambda}
\right]
\right)
$$

mit:

- $A$: Amplitude (maximale Auslenkung),
- $T$: Periodendauer,
- $\lambda$: Wellenlänge,
- $y(x;t)$: momentane Elongation der Schnur an der Stelle $x$ zur Zeit $t$.

Runde sinnvoll (3 signifikante Stellen).

__$a)\;\;$__ Eine Welle wird beschrieben durch
Amplitude $A = 1{,}5 \,\text{cm}$,
Periodendauer $T = 0{,}75 \,\text{s}$,
Wellenlänge $\lambda = 36 \,\text{cm}$.

Bestimme die momentane Auslenkung $y(x;t)$ an der Stelle $x = 5{,}0 \,\text{cm}$ zum Zeitpunkt $t = 2{,}4 \,\text{s}$.

<!-- data-hint-button="1" data-solution-button="3" -->
$y(5{,}0\,\mathrm{cm};2{,}4\,\mathrm{s})\approx$ [[ 0.562 cm ]] @canvas
@Algebrite.check2(`0.5619098901cm`,`0.0005cm`)
[[?]] Berechne erst $t/T-x/\lambda$ und multipliziere anschließend mit $2\pi$.
[[?]] @Explain
******************
$$
\begin{aligned}
\frac{t}{T}-\frac{x}{\lambda}
&=\frac{2{,}4\,\mathrm{s}}{0{,}75\,\mathrm{s}}
-\frac{5{,}0\,\mathrm{cm}}{36\,\mathrm{cm}}
\approx3{,}061111,\\
\varphi&=2\pi\left(\frac{t}{T}-\frac{x}{\lambda}\right)
\approx19{,}233528,\\
\sin(\varphi)&\approx0{,}374607,\\
y&=1{,}5\,\mathrm{cm}\sin(\varphi)
\approx0{,}5619099\,\mathrm{cm}\approx0{,}562\,\mathrm{cm}.
\end{aligned}
$$

Die momentane Auslenkung beträgt etwa $0{,}562\,\mathrm{cm}$.
******************

@resetter

@ADetails(`3=BE;Einheiten, Wellengleichung, Elongation`)

---

__$b)\;\;$__ Eine andere Welle hat Amplitude $A = 6{,}0 \,\text{mm}$ und Wellenlänge $\lambda = 10{,}0 \,\text{mm}$.
Nach einer Zeit $t = 3{,}5 \,\text{s}$ misst man an der Stelle $x = 4{,}0 \,\text{cm}$ eine Elongation von $y = 5{,}2 \,\text{mm}$.

Bestimme daraus die Periodendauer $T$ der Welle.

Zusätzlich ist bekannt, dass am betrachteten Ort und Zeitpunkt die Phase $\varphi=2\pi(t/T-x/\lambda)$ zwischen $0$ und $\pi/2$ liegt. Verwende diese Bedingung für die eindeutige Lösung.

<!-- data-hint-button="1" data-solution-button="3" -->
$T\approx$ [[ 0.840 s ]] @canvas
@Algebrite.check2(`0.8399588055s`,`0.0005s`)
[[?]] Wegen des vorgegebenen Phasenintervalls kannst du den Hauptwert von $\arcsin(y/A)$ verwenden.
[[?]] @Explain
******************
Wegen $0\leq\varphi\leq\pi/2$ ist der Hauptwert des Arkussinus hier die gesuchte Phase.

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
\arcsin(0{,}8667) \approx 1{,}04848 \,\text{rad}
$$

$$
\frac{1}{2\pi}\arcsin\!\left(\frac{y}{A}\right)
\approx
\frac{1{,}04848}{2\pi}
\approx 0{,}166871
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
0{,}166871 + 4{,}000
= 4{,}166871
\quad\Rightarrow\quad
T
= \frac{3{,}5\,\text{s}}{4{,}166871}
\approx 0{,}840 \,\text{s}
$$

Ohne die zusätzliche Phasenbedingung wären wegen der Periodizität und Symmetrie des Sinus mehrere Lösungen möglich.
******************

@resetter

@ADetails(`3=BE;Äquivalenzumformung, Wellengleichung, Periodendauer`)

---

__$c)\;\;$__ Eine Welle hat Amplitude $A = 12{,}0 \,\text{cm}$.
Zum Zeitpunkt $t = 3{,}0 \,\text{s}$ beobachtet man an der Stelle $x = 8{,}0 \,\text{cm}$ eine Auslenkung $y = 4{,}5 \,\text{cm}$.
Die Periodendauer beträgt $T = 1{,}20 \,\text{s}$.

1. Bestimme aus diesen Angaben die Wellenlänge $\lambda$.
2. Berechne daraus die Ausbreitungsgeschwindigkeit $c$ der Welle.

Zusätzlich ist bekannt, dass am betrachteten Ort und Zeitpunkt die Phase $\varphi=2\pi(t/T-x/\lambda)$ zwischen $0$ und $\pi/2$ liegt. Verwende diese Bedingung für die eindeutige Lösung.

<!-- data-hint-button="1" data-solution-button="3" -->
$\lambda\approx$ [[ 3.28 cm ]] @canvas, $\quad c\approx$ [[ 0.0273 m/s ]] @canvas
@Algebrite.check2(`[3.2802730669cm;0.0273356089m/s]`,`[0.005cm;0.00005m/s]`)
[[?]] Stelle zuerst nach $x/\lambda$ um. Verwende für $c=\lambda/T$ die Wellenlänge in Metern.
[[?]] @Explain
******************
Wegen $0\leq\varphi\leq\pi/2$ ist der Hauptwert des Arkussinus hier die gesuchte Phase.

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

Zahlen einsetzen:

- $A = 12{,}0 \,\text{cm}$
- $y = 4{,}5 \,\text{cm}$
- $x = 8{,}0 \,\text{cm}$
- $t = 3{,}0 \,\text{s}$
- $T = 1{,}20 \,\text{s}$

$$
\frac{y}{A} = \frac{4{,}5}{12{,}0} = 0{,}375
\quad\Rightarrow\quad
\arcsin(0{,}375) \approx 0{,}384397 \,\text{rad}
$$

$$
\frac{1}{2\pi} \cdot 0{,}384397
\approx 0{,}061179
\quad,\quad
\frac{t}{T} = \frac{3{,}0}{1{,}20} = 2{,}50
$$

$$
\frac{x}{\lambda}
= 2{,}50 - 0{,}061179
= 2{,}438821
\quad\Rightarrow\quad
\lambda
= \frac{8{,}0 \,\text{cm}}{2{,}438821}
\approx 3{,}28 \,\text{cm}
$$

Die Ausbreitungsgeschwindigkeit $c$ ist

$$
c = \frac{\lambda}{T}
= \frac{3{,}28 \,\text{cm}}{1{,}20 \,\text{s}}
\approx 2{,}73 \,\frac{\text{cm}}{\text{s}}
= 2{,}73 \cdot 10^{-2} \,\frac{\text{m}}{\text{s}}
$$

Ohne die zusätzliche Phasenbedingung wären wegen der Periodizität und Symmetrie des Sinus mehrere Lösungen möglich.
******************

@resetter

@ADetails(`4=BE;Einheiten, Wellengleichung, Ausbreitungsgeschwindigkeit`)

---

__$d)\;\;$__ Erkläre in ganzen Sätzen, warum in Teilaufgabe a) die momentane Auslenkung $y\approx0{,}562\,\mathrm{cm}$ kleiner ist als die Amplitude $A=1{,}5\,\mathrm{cm}$. Erläutere außerdem die physikalische Bedeutung von $\lambda$ und $T$ und begründe $c=\lambda/T$ mit den Ergebnissen aus Teilaufgabe c).

<!-- data-hint-button="1" data-solution-button="off" data-llm-textarea="6" -->
[[Antwort]]
[[?]] Der Sinus liegt zwischen $-1$ und $1$. Überlege außerdem, welche Strecke die Wellenform in einer Periodendauer zurücklegt.
[[?]] @Explain
```text @LLMQuiz(0.55;coverage=1;solution=1;feedback=1;assessmentengine=quality;Rechtschreibung=1;Satzbau=1;maxthinkingtime=15s;maxthinkingtokens=medium,`Erkläre in ganzen Sätzen, warum in Teilaufgabe a) die momentane Auslenkung $y\approx0{,}562\,\mathrm{cm}$ kleiner ist als die Amplitude $A=1{,}5\,\mathrm{cm}$. Erläutere außerdem die physikalische Bedeutung von $\lambda$ und $T$ und begründe $c=\lambda/T$ mit den Ergebnissen aus Teilaufgabe c).`)
<!-- lia-llm:criterion -->
Die Amplitude ist der größte mögliche Betrag der Auslenkung; hier ist die Phase nicht an einem Maximum und der Sinus beträgt etwa 0,375, daher ist die Auslenkung nur etwa 0,562 cm.
<!-- lia-llm:criterion -->
Die Wellenlänge ist die räumliche Periode der Welle, etwa der Abstand benachbarter Wellenberge.
<!-- lia-llm:criterion -->
Die Periodendauer ist die Zeit für eine vollständige Schwingung an einem festen Ort.
<!-- lia-llm:criterion -->
Die Wellenform legt in einer Periodendauer eine Wellenlänge zurück; mit etwa 3,28 cm und 1,20 s folgt c ungefähr 2,73 cm/s beziehungsweise 0,0273 m/s.
<!-- lia-llm:solution -->
Die Amplitude $A$ ist der größte mögliche Betrag der Auslenkung. Die momentane Elongation hängt von Ort und Zeit ab. In a) ist $\sin(\varphi)\approx0{,}3746$, also $y\approx1{,}5\,\mathrm{cm}\cdot0{,}3746\approx0{,}562\,\mathrm{cm}<A$.

Die Wellenlänge $\lambda$ ist die räumliche Periode, beispielsweise der Abstand benachbarter Wellenberge. Die Periodendauer $T$ ist die Zeit für eine vollständige Schwingung an einem festen Ort. In dieser Zeit läuft die Wellenform eine Wellenlänge weiter. Daher gilt $c=\lambda/T$; in c) folgt $c\approx3{,}28\,\mathrm{cm}/(1{,}20\,\mathrm{s})\approx2{,}73\,\mathrm{cm/s}=0{,}0273\,\mathrm{m/s}$.
```

@ADetails(`3=BE;Verhältnisse, Amplitude, Wellenlänge, Periodendauer`)

## Bearbeitungsstand sichern und auswerten

Prüfe vor dem Sichern, ob du alle gewünschten Aufgaben bearbeitet hast. Mit der Abgabefunktion kannst du einen Link zu deinem aktuellen Bearbeitungsstand erzeugen. Die Auswertung zeigt dir die Ergebnisse deiner Selbstchecks.

@Abgabe

@Auswertung
