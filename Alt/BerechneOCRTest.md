<!--
version: 1.0.1
language: de
narrator: Deutsch Female

mode: Presentation
persistent: true
edit: true

tags: Testkurs, Mathematik, OCR, Rechenwege, Gleichungen, Polynomfunktionen, Ableitungen
comment: 22 interaktive OCR-Quizze zu schriftlichen Rechenverfahren, Brüchen,
         Termen, Gleichungen sowie Ableitungen und Tangenten von Polynomfunktionen.
author: Martin Lommatzsch

import: https://cdn.jsdelivr.net/gh/LiaTemplates/algebrite@0.6.3/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-DynFlex/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-board-mode/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-marker/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-annotation/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-canvas-ocr/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-navigation/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-freeze-v2/main/README.md
-->

# Rechenwege und Ableitungen mit OCR

@autoscrolling(off)

In diesem Testkurs kannst du vollständige handschriftliche Rechnungen prüfen lassen: von den schriftlichen Grundrechenverfahren bis zu Ableitungen und Tangenten von Polynomfunktionen.

1. Öffne über das Stiftsymbol den Rechenblock und schreibe deinen Lösungsweg hinein.
2. Lass die Handschrift erkennen. Kontrolliere die erkannten Zeichen und korrigiere sie bei Bedarf im Editor.
3. Übernimm den Rechenweg in das Antwortfeld und klicke auf **Prüfen**. Nach Änderungen musst du den Rechenweg erneut übernehmen.

Bei Gleichungen, Termen und Funktionen wiederholst du die Vorgabe in der ersten Rechenzeile. Darunter stehen deine Zwischenrechnungen und das Ergebnis. Bei schriftlichen Rechenverfahren gehören Überträge beziehungsweise Entleihungen, Teilrechnungen und Rechenstriche dazu.

> **Hinweise und Musterlösungen:** Nach einer Fehlprüfung ist der Hinweis verfügbar, nach drei Fehlprüfungen die Musterlösung über **Auflösen**. Der Rechenblock prüft auch die Zwischenzeilen; ein richtiges Endergebnis allein genügt bei einem fehlerhaften Rechenweg nicht.

Der Kurs enthält **22 Quizze**. Du kannst sie mit Maus, Touch oder Stift bearbeiten und deinen Arbeitsstand am Ende über **Abgabe** sichern.


## Aufgabe 1: Schriftlich addieren und subtrahieren

<section class="dynFlex" data-basis="49%">

<div class="flex-child">

__$a)\;\;$__ **Berechne** $478+265$ mit dem schriftlichen Verfahren. **Notiere** alle Überträge, den Rechenstrich und das Ergebnis.

<!-- data-hint-button="1" data-solution-button="3" -->
@BerechneOCR(`478+265`,1)
[[?]] Ordne Einer unter Einer, Zehner unter Zehner und Hunderter unter Hunderter an. Beginne rechts und berücksichtige die Überträge.

@ADetails(2=BE;Addition, Schriftliches Rechnen, Überträge)

</div>

<div class="flex-child">

__$b)\;\;$__ **Berechne** $802-357$ mit dem schriftlichen Verfahren. **Notiere** alle Entleihungen, den Rechenstrich und das Ergebnis.

<!-- data-hint-button="1" data-solution-button="3" -->
@BerechneOCR(`802-357`,1)
[[?]] In der Einerstelle reicht die obere Ziffer nicht aus. Achte besonders auf die Null in der Zehnerstelle und kennzeichne die nötigen Entleihungen.

@ADetails(2=BE;Subtraktion, Schriftliches Rechnen, Entleihungen)

</div>

</section>


## Aufgabe 2: Schriftlich multiplizieren und dividieren

<section class="dynFlex" data-basis="49%">

<div class="flex-child">

__$a)\;\;$__ **Berechne** $368\cdot7$ mit dem schriftlichen Verfahren. **Notiere** alle Überträge, den Rechenstrich und das Ergebnis.

<!-- data-hint-button="1" data-solution-button="3" -->
@BerechneOCR(`368\cdot7`,1)
[[?]] Multipliziere die Ziffern von rechts nach links mit $7$. Notiere jeden Übertrag und berücksichtige ihn bei der nächsten Stelle.

@ADetails(3=BE;Multiplikation, Schriftliches Rechnen, Überträge)

</div>

<div class="flex-child">

__$b)\;\;$__ **Berechne** $936:6$ mit dem schriftlichen Verfahren. **Zeige** alle Teildividenden und die zugehörigen unterstrichenen Subtraktionen.

<!-- data-hint-button="1" data-solution-button="3" -->
@BerechneOCR(`936:6`,1)
[[?]] Beginne mit der linken Ziffer. Subtrahiere jeweils das passende Vielfache von $6$ und hole anschließend die nächste Ziffer herunter.

@ADetails(3=BE;Division, Schriftliches Rechnen, Teildividenden)

</div>

</section>


## Aufgabe 3: Brüche und Dezimalzahlen

<section class="dynFlex" data-basis="49%">

<div class="flex-child">

__$a)\;\;$__ **Berechne** den Wert von $x$ aus $x=\dfrac34+\dfrac56$. **Zeige** das Erweitern auf einen gemeinsamen Nenner und **gib** das Ergebnis als vollständig gekürzten Bruch **an**.

<!-- data-hint-button="1" data-solution-button="3" -->
@BerechneOCR(`x=3/4+5/6`,`zeilenrueckmeldung=1`)
[[?]] Ein gemeinsamer Nenner von $4$ und $6$ ist $12$. Erweitere beide Brüche und addiere danach die Zähler.

@ADetails(2=BE;Bruchrechnung, Addition, Erweitern)

</div>

<div class="flex-child">

__$b)\;\;$__ **Berechne** den Wert von $x$ aus $x=2{,}5\cdot(4-1{,}2)$. **Zeige** zuerst die Rechnung in der Klammer und anschließend die Multiplikation.

<!-- data-hint-button="1" data-solution-button="3" -->
@BerechneOCR(`x=2.5*(4-1.2)`,`zeilenrueckmeldung=1`)
[[?]] Klammern werden zuerst berechnet. Multipliziere das Zwischenergebnis anschließend mit $2{,}5$.

@ADetails(2=BE;Dezimalzahlen, Klammern, Rechenreihenfolge)

</div>

</section>


## Aufgabe 4: Polynomterme vereinfachen

Beginne deinen Rechenweg mit der vorgegebenen Funktionsgleichung. Beide Funktionen sind für alle reellen Zahlen definiert.

<section class="dynFlex" data-basis="49%">

<div class="flex-child">

__$a)\;\;$__ **Vereinfache** den Funktionsterm von $f(x)=3(2x-5)+4x+7$. **Löse** die Klammer auf und **fasse** gleichartige Summanden **zusammen**.

<!-- data-hint-button="1" data-solution-button="3" -->
@BerechneOCR(`f(x)=3*(2*x-5)+4*x+7`,`aufgabe=vereinfachen;zeilenrueckmeldung=1`)
[[?]] Multipliziere beide Summanden in der Klammer mit $3$. Fasse danach die Vielfachen von $x$ und die konstanten Summanden jeweils zusammen.

@ADetails(2=BE;Terme, Distributivgesetz, Zusammenfassen)

</div>

<div class="flex-child">

__$b)\;\;$__ **Vereinfache** den Funktionsterm von $g(x)=(x+3)(x-2)$. **Multipliziere** die Klammern aus und **fasse** gleichartige Summanden **zusammen**.

<!-- data-hint-button="1" data-solution-button="3" -->
@BerechneOCR(`g(x)=(x+3)*(x-2)`,`aufgabe=vereinfachen;zeilenrueckmeldung=1`)
[[?]] Jeder Summand der ersten Klammer wird mit jedem Summanden der zweiten Klammer multipliziert. Achte auf die Vorzeichen.

@ADetails(3=BE;Terme, Klammerprodukt, Polynomfunktionen)

</div>

</section>


## Aufgabe 5: Lineare Gleichungen lösen

<section class="dynFlex" data-basis="49%">

<div class="flex-child">

__$a)\;\;$__ **Löse** die Gleichung $3x+7=22$ über den reellen Zahlen. **Notiere** deine Umformungsschritte und die Lösung.

<!-- data-hint-button="1" data-solution-button="3" -->
@BerechneOCR(`3*x+7=22`,`zeilenrueckmeldung=1`)
[[?]] Subtrahiere auf beiden Seiten $7$. Dividiere anschließend beide Seiten durch den Faktor vor $x$.

@ADetails(2=BE;Lineare Gleichungen, Äquivalenzumformungen)

</div>

<div class="flex-child">

__$b)\;\;$__ **Löse** die Gleichung $4(x-2)=2x+10$ über den reellen Zahlen. **Notiere** deine Umformungsschritte und die Lösung.

<!-- data-hint-button="1" data-solution-button="3" -->
@BerechneOCR(`4*(x-2)=2*x+10`,`zeilenrueckmeldung=1`)
[[?]] Löse zuerst die Klammer auf. Bringe danach alle Summanden mit $x$ auf eine Seite und die konstanten Summanden auf die andere.

@ADetails(3=BE;Lineare Gleichungen, Klammern, Äquivalenzumformungen)

</div>

</section>


## Aufgabe 6: Quadratische Gleichungen lösen

<section class="dynFlex" data-basis="49%">

<div class="flex-child">

__$a)\;\;$__ **Löse** die Gleichung $2x^2-18=0$ über den reellen Zahlen. **Gib** die vollständige Lösungsmenge **an**.

<!-- data-hint-button="1" data-solution-button="3" -->
@BerechneOCR(`2*x^2-18=0`,`zeilenrueckmeldung=1`)
[[?]] Stelle die Gleichung zunächst nach $x^2$ um. Prüfe beim Wurzelziehen sowohl den positiven als auch den negativen Wert.

@ADetails(2=BE;Quadratische Gleichungen, Wurzelziehen, Lösungsmenge)

</div>

<div class="flex-child">

__$b)\;\;$__ **Löse** die Gleichung $x^2-5x+6=0$ über den reellen Zahlen. **Nutze** eine Produktdarstellung und **gib** die vollständige Lösungsmenge **an**.

<!-- data-hint-button="1" data-solution-button="3" -->
@BerechneOCR(`x^2-5*x+6=0`,`zeilenrueckmeldung=1`)
[[?]] Suche zwei Zahlen, deren Summe $-5$ und deren Produkt $6$ ist. Wende auf die Produktdarstellung den Satz vom Nullprodukt an.

@ADetails(3=BE;Quadratische Gleichungen, Faktorisieren, Satz vom Nullprodukt)

</div>

</section>


## Aufgabe 7: Erste Ableitung – Konstante und quadratische Funktion

Beginne mit der vorgegebenen Funktionsgleichung. Kennzeichne die Ableitung in einer neuen Zeile mit $f'(x)$ beziehungsweise $g'(x)$.

<section class="dynFlex" data-basis="49%">

<div class="flex-child">

__$a)\;\;$__ **Bestimme** die erste Ableitung der konstanten Polynomfunktion $f(x)=7$.

<!-- data-hint-button="1" data-solution-button="3" -->
@BerechneOCR(`f(x)=7`,`aufgabe=ableitung;ordnung=1;zeilenrueckmeldung=1`)
[[?]] Die Steigung einer konstanten Funktion ist an jeder Stelle gleich. Überlege, wie sich ihr Funktionswert bei einer Änderung von $x$ verhält.

@ADetails(1=BE;Ableitungen, Konstante Funktion, Polynomfunktionen)

</div>

<div class="flex-child">

__$b)\;\;$__ **Bestimme** die erste Ableitung von $g(x)=3x^2-4x+6$. **Leite** jeden Summanden einzeln **ab** und **fasse** das Ergebnis **zusammen**.

<!-- data-hint-button="1" data-solution-button="3" -->
@BerechneOCR(`g(x)=3*x^2-4*x+6`,`aufgabe=ableitung;ordnung=1;zeilenrueckmeldung=1`)
[[?]] Bei $a\cdot x^n$ wird der Exponent zum Faktor und anschließend um $1$ vermindert. Ein konstanter Summand hat die Ableitung $0$.

@ADetails(2=BE;Ableitungen, Potenzregel, Summenregel)

</div>

</section>


## Aufgabe 8: Erste Ableitung – Polynome dritten und vierten Grades

<section class="dynFlex" data-basis="49%">

<div class="flex-child">

__$a)\;\;$__ **Bestimme** die erste Ableitung von $f(x)=2x^3-5x^2+4x-9$. **Zeige** die Anwendung der Potenzregel auf die einzelnen Summanden.

<!-- data-hint-button="1" data-solution-button="3" -->
@BerechneOCR(`f(x)=2*x^3-5*x^2+4*x-9`,`aufgabe=ableitung;ordnung=1;zeilenrueckmeldung=1`)
[[?]] Multipliziere jeden Koeffizienten mit dem zugehörigen Exponenten. Achte beim quadratischen Summanden auf das Minuszeichen.

@ADetails(3=BE;Ableitungen, Potenzregel, Polynomfunktionen)

</div>

<div class="flex-child">

__$b)\;\;$__ **Bestimme** die erste Ableitung von $g(x)=\dfrac14x^4-\dfrac23x^3+\dfrac32x^2-5x+7$. **Kürze** die entstehenden Koeffizienten.

<!-- data-hint-button="1" data-solution-button="3" -->
@BerechneOCR(`g(x)=1/4*x^4-2/3*x^3+3/2*x^2-5*x+7`,`aufgabe=ableitung;ordnung=1;zeilenrueckmeldung=1`)
[[?]] Die Potenzregel gilt auch bei Bruchkoeffizienten. Multipliziere den Bruch mit dem Exponenten und kürze anschließend.

@ADetails(4=BE;Ableitungen, Bruchkoeffizienten, Potenzregel)

</div>

</section>


## Aufgabe 9: Zweite und dritte Ableitung

Kennzeichne die aufeinanderfolgenden Ableitungen mit $f'(x)$, $f''(x)$ beziehungsweise $g'(x)$, $g''(x)$ und $g'''(x)$.

<section class="dynFlex" data-basis="49%">

<div class="flex-child">

__$a)\;\;$__ **Bestimme** die zweite Ableitung von $f(x)=x^4-3x^3+1$. **Notiere** auch die erste Ableitung als Zwischenschritt.

<!-- data-hint-button="1" data-solution-button="3" -->
@BerechneOCR(`f(x)=x^4-3*x^3+1`,`aufgabe=ableitung;ordnung=2;zeilenrueckmeldung=1`)
[[?]] Bilde zuerst $f'(x)$. Wende danach die Potenzregel erneut auf diesen neuen Funktionsterm an.

@ADetails(4=BE;Ableitungen, Zweite Ableitung, Polynomfunktionen)

</div>

<div class="flex-child">

__$b)\;\;$__ **Bestimme** die dritte Ableitung von $g(x)=\dfrac12x^4-2x^3+x^2$. **Notiere** auch die erste und zweite Ableitung.

<!-- data-hint-button="1" data-solution-button="3" -->
@BerechneOCR(`g(x)=1/2*x^4-2*x^3+x^2`,`aufgabe=ableitung;ordnung=3;zeilenrueckmeldung=1`)
[[?]] Leite dreimal nacheinander ab. Der höchste Exponent wird bei jedem Ableiten um $1$ kleiner.

@ADetails(4=BE;Ableitungen, Höhere Ableitungen, Potenzregel)

</div>

</section>


## Aufgabe 10: Ableitungswerte berechnen

<section class="dynFlex" data-basis="49%">

<div class="flex-child">

__$a)\;\;$__ Gegeben ist $f(x)=x^3-2x^2+x+1$. **Bestimme** zunächst $f'(x)$ und **berechne** anschließend die Steigung $f'(2)$ des Graphen an der Stelle $x=2$.

<!-- data-hint-button="1" data-solution-button="3" -->
@BerechneOCR(`f(x)=x^3-2*x^2+x+1`,`aufgabe=ableitungswert;ordnung=1;stelle=2;zeilenrueckmeldung=1`)
[[?]] Leite zuerst den Funktionsterm ab. Setze erst danach $2$ in den Term der Ableitung ein und notiere das Ergebnis als $f'(2)=\ldots$.

@ADetails(3=BE;Ableitungen, Ableitungswert, Steigung)

</div>

<div class="flex-child">

__$b)\;\;$__ Gegeben ist $g(x)=x^4-4x^2+1$. **Bestimme** die erste und zweite Ableitung und **berechne** anschließend $g''(1)$.

<!-- data-hint-button="1" data-solution-button="3" -->
@BerechneOCR(`g(x)=x^4-4*x^2+1`,`aufgabe=ableitungswert;ordnung=2;stelle=1;zeilenrueckmeldung=1`)
[[?]] Setze $x=1$ erst ein, nachdem du die zweite Ableitung bestimmt hast. Kennzeichne den gesuchten Wert mit $g''(1)$.

@ADetails(4=BE;Ableitungen, Zweite Ableitung, Ableitungswert)

</div>

</section>


## Aufgabe 11: Tangenten bestimmen

Beginne mit der vorgegebenen Funktionsgleichung. **Gib** die Tangente am Ende als $t(x)=mx+b$ oder $y=mx+b$ **an**.

<section class="dynFlex" data-basis="49%">

<div class="flex-child">

__$a)\;\;$__ **Bestimme** die Tangente an den Graphen von $f(x)=x^2-3x+1$ an der Stelle $x=2$. **Berechne** dazu den Funktionswert und die Steigung an dieser Stelle.

<!-- data-hint-button="1" data-solution-button="3" -->
@BerechneOCR(`f(x)=x^2-3*x+1`,`aufgabe=tangente;stelle=2;zeilenrueckmeldung=1`)
[[?]] Bestimme $f(2)$ und $f'(2)$. Verwende anschließend $t(x)=f'(2)\cdot(x-2)+f(2)$ und fasse zusammen.

@ADetails(4=BE;Tangente, Ableitungen, Punkt-Steigungs-Gleichung)

</div>

<div class="flex-child">

__$b)\;\;$__ **Bestimme** die Tangente an den Graphen von $g(x)=x^3-3x+2$ an der Stelle $x=1$. **Prüfe** dabei, welche Bedeutung eine Steigung von $0$ für die Tangente hat.

<!-- data-hint-button="1" data-solution-button="3" -->
@BerechneOCR(`g(x)=x^3-3*x+2`,`aufgabe=tangente;stelle=1;zeilenrueckmeldung=1`)
[[?]] Berechne $g(1)$ und $g'(1)$. Eine Tangente mit Steigung $0$ verläuft parallel zur Abszissenachse.

@ADetails(4=BE;Tangente, Waagerechte Tangente, Ableitungen)

</div>

</section>


## Abgabe und Auswertung

**Kontrolliere** vor der Abgabe, ob deine zuletzt geschriebenen Rechenwege bereits in die Antwortfelder übernommen wurden. Über **Auflösen** kannst du bei freigeschalteten Aufgaben die automatisch erzeugte Musterrechnung ansehen.

**Sichere** deinen Arbeitsstand über **Abgabe**. Den erzeugten Link kannst du anschließend selbst an deine Lehrkraft weitergeben oder für den Vergleich weiterer Tests aufbewahren.

@Abgabe

@Auswertung
