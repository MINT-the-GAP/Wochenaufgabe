<!--
version:  0.0.1

narrator: Deutsch Female

language: de

@style
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
import: https://raw.githubusercontent.com/LiaTemplates/JSXGraph/0.0.1/README.md

script: https://cdn.jsdelivr.net/gh/LiaTemplates/Tikz-Jax@main/dist/index.js


tags: Profil, NaWi

comment: Der Profilunterricht Klasse 10 ist hier komplett aufgezeichnet. 

author: Martin Lommatzsch

-->





# Naturwissenschaftliches Profil Klasse 10 - Modellierung der Natur

> Letztes Update am 10.08.2025 gegen 18:00 Uhr


In diesem LiaScript findest du eine gesamte Zusammenfassung des Profilunterrichts der Klasse 10. Auch findest du hier Aufgaben und Lösungen zu den Aufgaben. Die Datei wird ständig aktualisiert.


## Naturwissenschaftliches Arbeiten in der Schule

{{0}}
__Aufgabe 1:__ **Beschreibe** den allgemeinen grundlegenden Ablauf deines vorherigen Unterrichts in den Fächern: Mathematik, Physik, Chemie, Biologie und dem naturwissenschaftlichen Profil. (Tipps: Was läuft in jedem Fach quasi gleich ab? Wie erarbeitet man neue Dinge im Unterricht?) \
<br>


{{1}}
__Aufgabe 2:__ **Begründe**, warum dieser Ablauf aus dem Unterricht nichts mit der wissenschaftlichen Realität zu tun haben kann. \
<br>

{{2}}
__Aufgabe 3:__ **Recherchiere** im Internet zu den folgenden Personen und beschreib, warum sie berühmt wurden.

{{2}}
<!-- data-type="none" data-sortable="false" -->
|             |             |             |
| Leonhard Euler| William Thomson Baron Kelvin | Bernhard Riemann | 
| Augustin-Louis Cauchy  | James Clerk Maxwell | Ludwig Boltzmann |
| Hendrik Antoon Lorentz  | Henri Poincaré | Max Planck |
| Emmy Noether  | Wolfgang Pauli | Enrico Fermi |
| Paul Dirac  | Richard Feynman | Steven Weinberg |

<br>

{{3}}
__Aufgabe 4:__ **Erörtere** mögliche Antworten auf die Frage: "Warum sind diese Personen nicht so berühmt, wie sie es sein sollten?"




## Naturwissenschaftliches Arbeiten in der Wissenschaft

{{|>}} In der schulischen Praxis naturwissenschaftlicher Fächer wird der Erkenntnisprozess häufig in der Reihenfolge „Experiment – Beobachtung – Theorie“ vermittelt. Zunächst werden einfache Versuche durchgeführt, an die sich eine gemeinsame Auswertung und anschließend die theoretische Erklärung anschließt. Diese didaktische Abfolge erleichtert das Verständnis, weil Beobachtungen zuerst sinnlich erfahrbar gemacht werden und abstrakte Modelle danach darauf aufbauen. In der wissenschaftlichen Forschung stellt sich die Reihenfolge jedoch in der Regel umgekehrt dar: Ausgangspunkt sind theoretische Überlegungen, Modelle und Berechnungen, denen erst in einem zweiten Schritt Experimente folgen.

{{|>}} Die Ursachen für diese Reihenfolge sind vielfältig. Zunächst ist der ökonomische Aspekt entscheidend. Moderne wissenschaftliche Experimente sind aufwendig und kostspielig. Forschungsanlagen wie der Large Hadron Collider am CERN in Genf erfordern Bau- und Betriebskosten in Milliardenhöhe. Der Einsatz solcher Ressourcen erfolgt nicht in einem offenen, ergebnislosen „Ausprobieren“, sondern wird erst dann unternommen, wenn theoretische Modelle konkrete Vorhersagen ermöglichen. Diese theoretischen Vorhersagen reduzieren das Risiko, dass ein Versuch ohne wissenschaftlichen Erkenntnisgewinn durchgeführt wird, und geben die Richtung für die Gestaltung und den Umfang eines Experiments vor.

{{|>}} Ein zweiter Grund liegt in der Komplexität naturwissenschaftlicher Fragestellungen. Ohne theoretischen Rahmen wäre die Vielzahl möglicher Beobachtungen kaum sinnvoll zu ordnen. Modelle und Hypothesen legen fest, welche Messgrößen relevant sind, welche Genauigkeiten notwendig sind und welche Daten einen Unterschied machen. Sie helfen, aus der Vielzahl der möglichen Phänomene die für die Fragestellung entscheidenden Aspekte auszuwählen. Experimente ohne eine solche theoretische Orientierung könnten zwar Beobachtungen liefern, würden aber kaum über Zufallsfunde hinausführen.

{{|>}} In der Praxis der Forschung folgt aus dieser Überlegung ein klarer Ablauf: Zunächst werden mathematische Modelle entwickelt und mit Hilfe von Simulationen überprüft. Daraus entstehen Hypothesen, die präzise Vorhersagen machen. Erst wenn diese Vorhersagen vorliegen, werden Versuchsaufbauten konzipiert, um die Hypothesen zu überprüfen. Die Durchführung der Experimente dient also vor allem der Bestätigung, der Präzisierung oder auch der Widerlegung vorher aufgestellter theoretischer Modelle.

{{|>}} Beispiele aus der Physik, der Astronomie oder der Medizin verdeutlichen diese Abfolge. So gingen der Messung der Lichtablenkung bei einer Sonnenfinsternis im Jahr 1919 theoretische Arbeiten von Albert Einstein aus dem Jahr 1915 voraus. Auch bei der Entwicklung neuer Medikamente stehen zunächst theoretische Untersuchungen und Computersimulationen am Anfang, bevor die eigentlichen Laborexperimente folgen. In der Teilchenphysik am CERN werden jahrzehntelange theoretische Arbeiten zusammengeführt, um anschließend Experimente zu entwerfen, die genau auf diese Vorhersagen zugeschnitten sind.

{{|>}} Der Gegensatz zu den Abläufen im Unterricht entsteht aus didaktischen Gründen. In der Schule werden die Experimente bewusst an den Anfang gestellt, um Lernprozesse anschaulicher zu machen. Experimente im Unterricht sind vergleichsweise einfach, kostengünstig und leicht zu wiederholen. Sie lassen sich gefahrlos durchführen und geben den Lernenden die Möglichkeit, sich aktiv einzubringen. Die eigentliche Erkenntnislogik der Wissenschaft wird dadurch allerdings verzerrt, denn in der realen Forschung sind Experimente in der Regel Ergebnis einer längeren theoretischen Vorarbeit.

{{|>}} Die ökonomischen Rahmenbedingungen spielen dabei eine große Rolle. Während schulische Experimente meist nur einfache Geräte oder Materialien erfordern, sind in der modernen Forschung viele Versuchsaufbauten hochspezialisiert und mit erheblichen Kosten verbunden. Große Beschleunigeranlagen, Teleskope oder Raumsonden werden über Jahre geplant und bauen vollständig auf den theoretischen Erwartungen auf, die zuvor entwickelt wurden. Selbst in kleineren Laboren wird vor der Durchführung einer Versuchsreihe genau kalkuliert, ob die benötigten Materialien, Geräte und die aufgewendete Arbeitszeit gerechtfertigt sind.

{{|>}} Darüber hinaus erfüllt Theorie eine wichtige Filterfunktion. Sie reduziert den Aufwand, indem sie den Blick auf das Wesentliche lenkt. Ohne diese theoretische Vorarbeit wäre es kaum möglich, die Fülle an möglichen Beobachtungen zu strukturieren. Theorie und Experiment stehen dabei nicht in einem Gegensatz, sondern bilden eine enge Wechselwirkung: Theorie erzeugt Hypothesen, Experimente überprüfen diese, und die Ergebnisse führen zu neuen theoretischen Überlegungen.

{{|>}} Die unterschiedliche Reihenfolge in Schule und Forschung ist somit Ausdruck zweier verschiedener Logiken. Die schulische Didaktik orientiert sich daran, Inhalte anschaulich und nachvollziehbar zu gestalten, während die Wissenschaft unter realen Bedingungen gezwungen ist, ihre Arbeitsschritte so zu planen, dass Ressourcen sinnvoll eingesetzt werden. Der im Unterricht oft gewählte Weg „erst Experiment, dann Theorie“ entspricht also nicht dem realen Ablauf wissenschaftlicher Arbeit, ist aber für den Lernprozess eine bewusst gewählte Vereinfachung.



# Theoretische Physik


{{|>}} Die theoretische Physik beschäftigt sich nicht in erster Linie mit Messungen, sondern mit der Entwicklung von Modellen, die grundlegende Strukturen und Gesetzmäßigkeiten der Natur beschreiben. Ausgangspunkt ist meist ein beobachtetes Phänomen oder ein bereits bekanntes Gesetz. Daraus werden Annahmen formuliert, aus denen sich mit Hilfe der Mathematik Gleichungen herleiten lassen. Diese Gleichungen stellen eine idealisierte Beschreibung der Wirklichkeit dar. Sie enthalten nicht nur bekannte Zusammenhänge, sondern erlauben es, aus wenigen Grundprinzipien eine Vielzahl von Folgerungen logisch abzuleiten.

{{|>}} Zentral ist dabei die Arbeit mit Abstraktionen. Anstatt mit konkreten Zahlen zu beginnen, arbeitet die theoretische Physik zunächst mit Symbolen, Variablen und Strukturen. Die Form der Gleichung ist wichtiger als ein einzelner Zahlenwert, denn sie legt fest, wie Größen zueinander in Beziehung stehen. Zahlenwerte treten erst dann in Erscheinung, wenn die Theorie durch Experimente überprüft oder mit konkreten Randbedingungen verbunden wird.

{{|>}} Die theoretische Physik versteht sich damit als gedanklicher Rahmen, der Orientierung bietet. Sie versucht, ein konsistentes Bild zu schaffen, das verschiedene Phänomene miteinander verknüpft und Widersprüche in den Beobachtungen auflöst. Nicht selten liefern ihre Modelle Vorhersagen für Effekte, die zu einem bestimmten Zeitpunkt noch gar nicht gemessen werden können. Erst in einem späteren Schritt werden Experimente entwickelt, um diese Vorhersagen zu überprüfen.

{{|>}} Die Arbeit der theoretischen Physik besteht also darin, Hypothesen zu formulieren, mathematisch präzise Modelle zu entwickeln, diese zu interpretieren und die Konsequenzen zu durchdenken. Erst wenn ein Modell Bestand hat, wird es zur Grundlage für weitere Forschung – sowohl theoretisch als auch experimentell.



## Nutzen von Analogien

{{|>}} Ein wesentliches Werkzeug in der Physik besteht darin, Analogien zwischen unterschiedlichen Bereichen zu erkennen und zu nutzen. Wenn sich in zwei verschiedenen Themengebieten ähnliche mathematische Strukturen zeigen, können Erkenntnisse aus dem einen Gebiet auf das andere übertragen werden. Auf diese Weise wird Wissen nicht nur auf einen Einzelfall beschränkt, sondern gewinnt an Allgemeinheit.

{{|>}} Ein einfaches Beispiel liefert die Bewegung bei konstanter Geschwindigkeit. Die Grundgleichung lautet

$$ x=v \cdot t $$

{{|>}} und beschreibt, dass der zurückgelegte Weg $x$ direkt proportional zur Zeit $t$ ist, wenn die Geschwindigkeit $v$ konstant bleibt. Diese Beziehung bedeutet: Verdoppelt sich die Zeit, so verdoppelt sich auch der Weg. In einem Diagramm ergibt das eine gerade Linie.

{{|>}} Eine sehr ähnliche mathematische Struktur findet sich in der Elektrizitätslehre bei der Definition der Stromstärke:

$$ Q=I \cdot t $$

{{|>}} Hier bezeichnet $Q$ die transportierte elektrische Ladung, $I$ die Stromstärke und $t$ die Zeit. Auch hier gilt: Bei konstantem $I$ wächst die transportierte Ladung linear mit der Zeit.

{{|>}} Diese beiden Gleichungen sind formal gleich aufgebaut. Der Weg $x$ spielt dabei die Rolle der elektrischen Ladung $Q$, und die Geschwindigkeit $v$ entspricht der Stromstärke $I$. Aus dieser Analogie folgt, dass viele Überlegungen, die für Bewegungen gelten, auch für den Stromtransport gelten: Ein größerer Strom „befördert“ in gleicher Zeit mehr Ladung, genauso wie eine größere Geschwindigkeit in gleicher Zeit mehr Strecke zurücklegt. Diagramme, die $x$ gegen $t$ oder $Q$ gegen $t$ darstellen, sehen nahezu identisch aus.

{{|>}} Solche Analogien sind nicht nur ein Hilfsmittel für das Verständnis, sondern können auch zur Vorhersage dienen. Wer die eine Struktur verstanden hat, kann sofort Aussagen über die andere machen, ohne diese erneut von Grund auf entwickeln zu müssen. Durch das Erkennen solcher Parallelen wird die Vielfalt der physikalischen Erscheinungen auf gemeinsame Prinzipien zurückgeführt, und Zusammenhänge werden klarer. Die Fähigkeit, Analogien zu erkennen, gehört daher zu den zentralen Denkweisen der Physik.




## Energieerhaltung




{{|>}} Die potentielle Energie $E_{pot}$ ist eine physikalische Größe bei der Kraft $F$ über eine gewisse Strecke $x$ angewendet wurde. Wenn sich eine Energie $E$ ändert, dann wird sogenannte Arbeit $W$ verrichtet. Die Energie $E$ ist dabei eine Größe, die einen Zustand zu einem einzigen Zeitpunkt beschreibt - eine sogenannte Zustandsgröße - auch als Observable bezeichnet. Jede Observable ist messbar, während eine Prozessgröße niemals messbar ist. Die Arbeit ist zum Beispiel so eine Prozessgröße, da sie den Unterschied zwischen zwei Zuständen von Energiezuständen beschreibt. Dabei ist jedoch nicht klar, ob die Arbeit gleichmäßig oder vollkommen willkürlich verrichtet wird. Zur ersten Vereinfachung wird erstmal angenommen, dass die Arbeit gleichmäßig verrichtet wird. Auf die Arbeit $W$ wird später noch genauer eingegangen. Da die Gravitation die für uns maßgebliche Kraft $F_{G} = m \cdot g$ ist und sie stets nach unten wirkt, kann die Strecke $x$ auch mit der Höhe $h$ gleich gesetzt werden.

$$
\begin{align*} 
E_{pot} & = \textcolor{red}{F} \cdot \textcolor{green}{x} \\
\Rightarrow E_{pot,G} & = \textcolor{red}{-m \cdot g}\cdot \textcolor{green}{h}
\end{align*}
$$


{{|>}} Während dessen ist die kinetische Energie $E_{kin}$ ebenso die Kraft $F$, die über eine Strecke $x$ wirkt. Hierbei wird nicht die explizite Beispielkraft verwendet, sondern das zweite Newton'sche Axiom: $F=m \cdot a$. Da es sich also um eine beschleunigte Bewegung handelt wird auch diese Bahnkurvengleichung verwendet.

<br>

{{1}}
__Aufgabe 1:__ **Leite** den allgemeinen mathematischen Ausdruck der kinetischen Energie $E_{kin}$ aus dem zweiten Newton'schen Axiom und einer beschleunigten Bewegungsgleichung über die Gleichung der Energie für konstante Kräfte her. \
<br>


{{2}}


$$
\begin{align*} 
E_{kin} & = \textcolor{red}{F} \cdot \textcolor{green}{x} \qquad \text{mit: } \textcolor{green}{x = \frac{1}{2}\cdot a\cdot t^2}  \\
& = \textcolor{red}{m\cdot a} \cdot \textcolor{green}{\frac{1}{2}\cdot a\cdot t^2} \\
& = \frac{1}{2}\cdot m\cdot (a\cdot t)^2 \qquad \text{mit: } v = a\cdot t \\
& = \frac{1}{2}\cdot m (\textcolor{blue}{a \cdot t})^2 \qquad \text{mit: } v = \textcolor{blue}{a\cdot t} \\
\Rightarrow E_{kin} & = \frac{1}{2}\cdot m\cdot v^2
\end{align*}
$$



{{3}}
> {{|>}} Die Energie $E$ ist eine Erhaltungsgröße. Das bedeutet, dass die Gesamtenergie in einem System bevor etwas passiert und nachdem etwas passiert ist stets gleich groß sein muss.

{{3}}
> $$
\begin{align*} 
\underbrace{E_{kin} + E_{pot}}_{\text{vorher}} & = \underbrace{E'_{kin} + E'_{pot}}_{\text{nachher}}
\end{align*}
$$

{{3}}
> {{|>}} Energie $E$ kann niemals verbraucht, erzeugt, produziert, verschwendet, erneuert oder ähnliches werden. Energie $E$ kann lediglich in andere Energieformen umgewandelt werden, was durch Arbeit $W$ passiert.



## Der Impuls $\vec{p}$


{{|>}} In vielen Situationen wirken Kräfte nicht gleichmäßig, sondern verändern sich mit der Zeit. Ein Beispiel sind Stöße oder Explosionen, bei denen innerhalb sehr kurzer Zeit große Kräfte auftreten, die sich ständig ändern. In solchen Fällen reicht es nicht aus, nur mit der Geschwindigkeit zu arbeiten. Um diese Vorgänge besser zu beschreiben, wird der physikalische Begriff des Impulses $\vec{p}$ eingeführt. Der Impuls $\vec{p}$ fasst die Wirkung einer Kraft über die gesamte Zeit ihres Einwirkens zusammen. Er ermöglicht es, auch bei schnell wechselnden oder sehr kurzzeitigen Kräften den Bewegungszustand von Körpern zu berechnen und Vorhersagen zu treffen.

{{|>}} Der Impuls ist wie die Geschwindigkeit $\vec{v}$ oder die Kraft $\vec{F}$ eine vektorielle Größe. Der Impuls $\vec{p}$ ist also eine Richtungsgröße und besitzt somit einen Betrag $|\vec{p}|$ - also einen Wert, der seine Stärke beschreibt - und eine Orientierung. Zur Vereinfachung wird zunächst die Orientierung weggelassen und die Schreibweise verkürzt: $|\vec{a}|=a$

$$
\begin{align*} 
\vec{p} & = \vec{F} \cdot t  \\
\text{Vereinfachung:} \;\;\;\; p & = F \cdot t
\end{align*}
$$