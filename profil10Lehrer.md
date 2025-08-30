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
& = \frac{1}{2}\cdot m (\textcolor{cyan}{a \cdot t})^2 \qquad \text{mit: } v = \textcolor{cyan}{a\cdot t} \\
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




{{1}}
__Aufgabe 1:__ **Leite** einen Ausdruck des Impulses her, indem die Geschwindigkeit $v$ vorkommt. \
<br>


{{2}}
$$
\begin{align*} 
p & = \textcolor{red}{F} \cdot \textcolor{green}{t} \qquad \text{mit: } \textcolor{red}{F = m \cdot a}  \\
& = \textcolor{red}{m\cdot a} \cdot \textcolor{green}{t} \\
& = m\cdot \textcolor{cyan}{a \cdot  t}  \qquad \text{mit: } v = \textcolor{cyan}{a\cdot t}  \\
& = m \cdot \textcolor{cyan}{v} \\
\end{align*}
$$


{{1}}
__Aufgabe 2:__ **Interpretiere** die Gleichung $F = \dfrac{p}{t}$ und entwickle aus dieser Interpretation eine neue Beschreibung in Form eines Wortes für die Kraft $F$. \
<br>


{{2}}
{{|>}} Die Gleichung weist eine Analogie zur Geschwindigkeitsgleichung $v = \dfrac{x}{t}$ beziehungsweise zur Stromstärke $I = \dfrac{Q}{t}$ auf. Somit kann die Kraft auch als Impulsstrom bezeichnet werden.


<br>


{{3}}
> {{|>}} Der Impuls $\vec{p}$ ist eine Erhaltungsgröße. Das bedeutet, dass der Gesamtimpuls in einem System bevor etwas passiert und nachdem etwas passiert ist stets gleich groß sein muss.

{{3}}
> $$
\begin{align*} 
\underbrace{\vec{p}_1 + \vec{p}_2}_{\text{vorher}} & = \underbrace{\vec{p}'_1 + \vec{p}'_2}_{\text{nachher}}
\end{align*}
$$

{{3}}
> {{|>}} Impuls $\vec{p}$ kann niemals verbraucht, erzeugt, produziert, verschwendet, erneuert oder ähnliches werden. Impuls $\vec{p}$ kann lediglich in andere Teilimpulse zerglegt werden, was durch Kärfte $F$ passiert. Da der Impuls eine vektorielle Größe ist, muss auch immer die Orientierung mit erhalten bleiben.

<br>



## Superposition

{{|>}} Das Superpositionsprinzip beschreibt die Überlagerung mehrerer Wirkungen, die unabhängig voneinander betrachtet und anschließend vektoriell addiert werden können. Dieses Prinzip gilt nicht nur für Kräfte und Geschwindigkeiten, sondern ebenso für den Impuls.

{{|>}} Wird ein Impulsvektor (in der Abbildung $\vec{c}$) in mehrere Komponenten zerlegt, beispielsweise in eine horizontale (in der Abbildung $\vec{a}$) und eine vertikale (in der Abbildung $\vec{b}$) Richtung, so beeinflussen sich diese Komponenten nicht gegenseitig. Eine Änderung des Impulses in einer Richtung hat keinen Einfluss auf die orthogonale Komponente. Dadurch lassen sich komplexe Bewegungsabläufe in Teilprobleme zerlegen, die separat untersucht werden können.



<center>
<!-- style="width:400px" -->
![](Superposi1.png)
</center>


{{|>}} Wirken mehrere Kräfte gleichzeitig auf einen Körper, so kann jede Kraft eine eigene Impulsänderung hervorrufen. Nach dem Superpositionsprinzip ergibt sich die gesamte Impulsänderung aus der vektoriellen Summe der einzelnen Impulsänderungen. Diese Überlagerung gilt unabhängig davon, ob die Kräfte zeitgleich oder nacheinander wirken, solange die einzelnen Beiträge korrekt erfasst werden. Die Beträge ergeben sich in der Interpretation aus der Länge der Vektoren.

<br>

{{1}}
__Aufgabe 1:__ **Gib** eine Gleichung **an**, die aus der horizontalen $\left|\vec{a}\right|$ und vertikalen Länge $\left|\vec{b}\right|$ die Länge von $\left|\vec{c}\right|$ berechnen lässt. \
<br>


{{2}} $$
\begin{align*} 
\left|\vec{c}\right| & = \sqrt{\left|\vec{a}\right|^2+\left|\vec{b}\right|^2}   \\ 
\end{align*}
$$

<br>
{{3}} 
{{|>}} Die Zerlegung des Impulses in Komponenten vereinfacht die Analyse, da jede Richtung separat berechnet werden kann. Nach der Bestimmung der Komponenten wird der Gesamtimpuls wieder durch Addition der Vektoren gewonnen. Dieses Vorgehen ist insbesondere bei Bewegungen in mehreren Dimensionen oder bei der gleichzeitigen Wirkung verschiedener Kräfte von Bedeutung, etwa bei Schrägwürfen oder zusammengesetzten Stoßvorgängen.

{{3}} 
{{|>}} Das Superpositionsprinzip stellt damit ein zentrales Werkzeug zur Behandlung komplexer Impulsänderungen dar und ermöglicht eine systematische und klare Analyse vielschichtiger physikalischer Prozesse.


{{3}} 
{{|>}} Addiert man die einzelnen Komponenten, dann bildet sich eine lange Diagonale eine Parallelogramms aus. Subtrahiert man die Komponenten, ergibt sich die kurze Diagonale:

{{3}} 
<center>
<!-- style="width:400px" -->
![](Superposi2.png)
</center>

<br>

{{4}} 
{{|>}} Bei Zusammenstößen zwischen zwei Körpern ist der Winkel nach dem Zusammenprall interessant, welcher sich über das Teildreieck des Parallelogramms mit der kurzen Diagonale berechnen lässt.

{{4}} 
<center>
<!-- style="width:400px" -->
![](Superposi3.png)
</center>

<br>


{{5}}
__Aufgabe 2:__ **Gib** eine Gleichung **an**, die die Länge von $\left|\vec{a}-\vec{b}\right|$ berechnen lässt. \
<br>


{{6}} $$
\begin{align*} 
\left|\vec{a}-\vec{b}\right| & = \sqrt{\left|\vec{a}\right|^2+\left|\vec{b}\right|^2-2\left|\vec{a}\right|\left|\vec{b}\right|\cos(\varphi)}   \\ 
\end{align*}
$$


<br>


{{7}}
__Aufgabe 3:__ **Löse** die Gleichung $\left|\vec{a}-\vec{b}\right| = \sqrt{\left|\vec{a}\right|^2+\left|\vec{b}\right|^2-2\left|\vec{a}\right|\left|\vec{b}\right|\cos(\varphi)}$ nach dem Winkel $\varphi$ **auf**. \
<br>


{{8}}
$$
\begin{align*} 
\left|\vec{a}-\vec{b}\right| & = \sqrt{\left|\vec{a}\right|^2+\left|\vec{b}\right|^2-2\left|\vec{a}\right|\left|\vec{b}\right|\cos(\varphi)}  \\ 
\Rightarrow\;\; \left|\vec{a}-\vec{b}\right|^2 & = \left|\vec{a}\right|^2+\left|\vec{b}\right|^2-2\left|\vec{a}\right|\left|\vec{b}\right|\cos(\varphi) \quad \left| - \left|\vec{a}\right|^2  - \left|\vec{b}\right|^2  \right.  \\ 
 \left|\vec{a}-\vec{b}\right|^2 - \left|\vec{a}\right|^2  - \left|\vec{b}\right|^2 & = -2\left|\vec{a}\right|\left|\vec{b}\right|\cos(\varphi) \quad \left|  \cdot (-1)  \right.  \\ 
 \left|\vec{a}\right|^2  + \left|\vec{b}\right|^2 -  \left|\vec{a}-\vec{b}\right|^2 & = 2\left|\vec{a}\right|\left|\vec{b}\right|\cos(\varphi) \quad \left|  : 2\left|\vec{a}\right|\left|\vec{b}\right|  \right.  \\ 
\dfrac{ \left|\vec{a}\right|^2  + \left|\vec{b}\right|^2 -  \left|\vec{a}-\vec{b}\right|^2}{ 2\left|\vec{a}\right|\left|\vec{b}\right| } & =  \cos(\varphi)    \\ 
\Rightarrow\;\;  \arccos\left(  \dfrac{ \left|\vec{a}\right|^2  + \left|\vec{b}\right|^2 -  \left|\vec{a}-\vec{b}\right|^2}{ 2\left|\vec{a}\right|\left|\vec{b}\right| } \right) & =   \varphi    \\ 
\end{align*}
$$



---
<br>
---


{{9}}
__Aufgabe 4:__ Ein Körper der Masse $m$ befindet sich zunächst in Ruhe. In sehr kurzer Zeit wirken zwei Impulsstöße  
$\vec p_1$ und $\vec p_2$ auf den Körper. Die Beträge seien $p_1$ und $p_2$, der Winkel zwischen den Richtungen betrage $\varphi$.

{{9}}
$a)\;\;$ **Bestimme** den Betrag des resultierenden Impulses $\vec p = \vec p_1 + \vec p_2$.

{{9}}
$b)\;\;$ **Leite** daraus die Endgeschwindigkeit $v'$ des Körpers **her**.

{{9}}
$c)\;\;$ **Gib** die kinetische Energie $E_{\text{kin}}'$ nach den beiden Impulsstößen in Abhängigkeit von $p_1, p_2, \varphi$ und $m$ **an**.

---

{{10}}
$a)\;\;$ Schritt 1: Resultierenden Impulsbetrag via Kosinussatz

{{10}}
Die Vektorsumme $\vec p = \vec p_1 + \vec p_2$ bildet ein Dreieck mit eingeschlossenem Winkel $\varphi$ zwischen $\vec p_1$ und $\vec p_2$. Für die Beträge gilt:

{{10}}
$$
\begin{align*}
p^2 &= p_1^2 + p_2^2 + 2\,p_1 p_2 \cos(\varphi) \,.
\end{align*}
$$

---

{{11}}
$b)\;\;$ Schritt 2: Zusammenhang zwischen Impuls und Geschwindigkeit

{{11}}
Mit $\vec p' = \vec p$ und Anfangsruhe ($\vec p_0 = \vec 0$) gilt:

{{11}}
$$
\begin{align*}
v' &= \dfrac{p}{m}
= \dfrac{\sqrt{\,p_1^2 + p_2^2 + 2\,p_1 p_2 \cos(\varphi)\,}}{m} \,.
\end{align*}
$$

---

{{12}}
$c)\;\;$ Schritt 3: Kinetische Energie nach den Impulsstößen

{{12}}
Mit $E_{\text{kin}}' = \dfrac{p^2}{2m}$ und dem Ergebnis aus Schritt 1 folgt:

{{12}}
$$
\begin{align*}
E_{\text{kin}}' 
&= \dfrac{p_1^2 + p_2^2 + 2\,p_1 p_2 \cos(\varphi)}{2m} \,.
\end{align*}
$$

---

{{13}}
Zusatz (optional): Spezialfälle zur Interpretation


{{13}}
- Konstruktive Überlagerung ($\varphi = 0$):

{{13}}
$$
\begin{align*}
p = p_1 + p_2,\quad 
v' = \dfrac{p_1 + p_2}{m},\quad
E_{\text{kin}}' = \dfrac{(p_1 + p_2)^2}{2m}.
\end{align*}
$$


{{13}}
- Destruktive Überlagerung ($\varphi = \pi$):

{{13}}
$$
\begin{align*}
p = \lvert p_1 - p_2\rvert,\quad 
v' = \dfrac{\lvert p_1 - p_2\rvert}{m},\quad
E_{\text{kin}}' = \dfrac{(p_1 - p_2)^2}{2m}.
\end{align*}
$$














## Energie- und Impulserhaltung



{{0}}
__Aufgabe 1:__ **Leite** einen Ausdruck der kinetischen Energie her, indem der Impuls $p$ sowie die Geschwindigkeit $v$ vorkommen. \
<br>


{{1}} $$
\begin{align*} 
E_{kin} & = \dfrac{1}{2} m v^2   \qquad \text{mit: }  p = mv \;\;\Rightarrow\;\; m = \dfrac{p}{v}   \\
E_{kin} & = \dfrac{1}{2} \dfrac{p}{v} v^2 \\
E_{kin} & = \dfrac{1}{2} v p \\
\end{align*}
$$



{{0}}
__Aufgabe 2:__ **Leite** einen Ausdruck der kinetischen Energie her, indem der Impuls $p$ sowie die Masse $m$ vorkommen. \
<br>


{{1}}
$$
\begin{align*} 
E_{kin} & = \dfrac{1}{2} m v^2   \qquad \text{mit: }  p = mv \;\;\Rightarrow\;\; v = \dfrac{p}{m}   \\
E_{kin} & = \dfrac{1}{2} m \left( \dfrac{p}{m} \right)^2 \\
E_{kin} & = \dfrac{1}{2} m   \dfrac{p^2}{m^2}  \\
E_{kin} & =  \dfrac{p^2}{2m} \\
\end{align*}
$$


{{2}}
Unter der Annahme, dass sich die Masse $m$ eines betrachteten Objektes nicht verändert, kann der Impuls $p$ in Abhänigkeit von der Geschwindigkeit $v$ in einem $v$-$p$-Koordinatensystem dargestellt werden: 


{{2}}
<center>
<!-- style="width:600px" -->
![](pvEnergie1.png)
</center>


{{2}}
__Aufgabe 3:__ **Beschreibe**, wo sich in diesem Diagramm die Energie wiederfindet und **begründe** deine Aussagen mit einer Herleitung. \


{{3}}
Der Flächeninhalt zwischen der Abszisse und dem Graphen entspricht dem Wert der Energie. Für die Herleitung wird eine beliebige Geschwindigkeit $v_0$ verwendet.


{{3}}
<center>
<!-- style="width:600px" -->
![](pvEnergie2.png)
</center>


{{3}}
$$
\begin{align*} 
A & = \dfrac{1}{2} v_0 p(v_0)   \qquad \text{mit: }  p(v_0) = mv_0  \\
A & = \dfrac{1}{2} v_0 mv_0    \\
A & = \dfrac{1}{2} mv_0^2    \\
A & = E_{kin}    \\
\end{align*}
$$




{{2}}
__Aufgabe 4:__ **Beschreibe**, wo sich in diesem Diagramm die Masse wiederfindet und **begründe** deine Vermutung. \



{{3}}
Die Steigung der Geraden gibt die Masse an, da dies der einzige freie Parameter der allgemeinen Geradengleichung ist und dieser auch konstant ist. Würde sich der Massenwert verringern, würde der Flächeninhalt des Dreiecks auch kleiner werden und andersherum. Folglich ist der Energiewert abhängig von der Steigung der Geraden, welche also als Masse interpretiert werden kann.




{{2}}
__Aufgabe 5:__ **Beschreibe**, wo sich in diesem Diagramm die Masse wiederfindet und **begründe** deine Vermutung. \



### Übungen zu Erhaltungsgrößen

__Aufgabe 1:__ Zentraler elastischer Stoß auf einer Geraden

Zwei Körper mit den Massen $m_1$ und $m_2$ bewegen sich mit den Geschwindigkeiten $v_1$ und $v_2$ aufeinander zu.  
Nach einem elastischen Stoß besitzen sie die Geschwindigkeiten $v_1'$ und $v_2'$.

$a)\;\;$ **Gib** die Erhaltungsgleichungen für den Impuls und die kinetische Energie **an**.  

$b)\;\;$ **Leite** daraus allgemeine Ausdrücke für $v_1'$ und $v_2'$ in Abhängigkeit von $m_1, m_2, v_1, v_2$ **her**.

---

{{1}}
$a)\;\;$ **Schritt 1: Impuls- und Energieerhaltung**

{{1}}
$$
\begin{align*}
m_1 v_1 + m_2 v_2 &= m_1 v_1' + m_2 v_2' \quad &(1) \\
\frac12 m_1 v_1^2 + \frac12 m_2 v_2^2 &= \frac12 m_1 {v_1'}^{2} + \frac12 m_2 {v_2'}^{2} \quad &(2)
\end{align*}
$$

---

{{2}}
$b)\;\;$ **Schritt 2: Relativgeschwindigkeitsregel**

{{2}}
Gleichung (2) wird mit 2 multipliziert und mit (1) kombiniert.  
Nach Umformung folgt die Relativgeschwindigkeitsregel:

{{2}}
$$
v_1 - v_2 = -\,(v_1' - v_2') \quad (3)
$$

---

{{3}}
**Schritt 3: Aus (3) $v_1'$ ausdrücken und in (1) einsetzen**

{{3}}
Aus (3) ergibt sich:

{{3}}
$$
v_1' = v_2' + v_2 - v_1
$$

{{3}}
In (1) eingesetzt:

{{3}}
$$
m_1 v_1 + m_2 v_2 = m_1 (v_2' + v_2 - v_1) + m_2 v_2'
$$

---

{{4}}
**Schritt 4: $v_2'$ bestimmen**

{{4}}
Nach Umformen:

{{4}}
$$
(m_1 + m_2) v_2' = 2 m_1 v_1 + (m_2 - m_1) v_2
$$

{{4}}
Damit:

{{4}}
$$
v_2' = \frac{2 m_1}{m_1 + m_2} v_1 + \frac{m_2 - m_1}{m_1 + m_2} v_2
$$

---

{{5}}
**Schritt 5: $v_1'$ bestimmen**

{{5}}
Einsetzen in $v_1' = v_2' + v_2 - v_1$:

{{5}}
$$
v_1' = \frac{m_1 - m_2}{m_1 + m_2} v_1 + \frac{2 m_2}{m_1 + m_2} v_2
$$

---

{{6}}
**Schritt 6: Präsentation der Lösung**

{{6}}
$$
\begin{align*}
v_1' &= \frac{m_1 - m_2}{m_1 + m_2} v_1 + \frac{2 m_2}{m_1 + m_2} v_2 \\
v_2' &= \frac{2 m_1}{m_1 + m_2} v_1 + \frac{m_2 - m_1}{m_1 + m_2} v_2
\end{align*}
$$

{{6}}
Damit liegen die allgemeinen Geschwindigkeitsausdrücke für den eindimensionalen elastischen Stoß vor.

---
<br>
---

__Aufgabe 2:__ Vollständig inelastischer Stoß (Verkleben)

Zwei Körper mit den Massen $m_1$ und $m_2$ bewegen sich mit den Geschwindigkeiten $v_1$ und $v_2$ aufeinander zu und bewegen sich nach dem Stoß gemeinsam mit der Geschwindigkeit $v'$.

$a)\;\;$ **Bestimme** $v'$ aus der Impulserhaltung.

$b)\;\;$ **Bestimme** die kinetische Energie vor und nach dem Stoß und leite den "Energieverlust" $\Delta E_{kin}$ her.

$c)\;\;$ **Gib** optional den relativen "Verlust" $\dfrac{\Delta E_{kin}}{E_{kin,\text{vor}}}$ **an**.

$d)\;\;$ **Erkläre**, wo die Energie aus dem relativen "Verlust" der kinetischen Energie hin ist.

---

{{7}}
$a)\;\;$ Schritt 1: Impulserhaltung und gemeinsame Geschwindigkeit

{{7}}
$$
\begin{align*}
m_1 v_1 + m_2 v_2 &= (m_1 + m_2) \, v' \\
\Rightarrow\quad
v' &= \frac{m_1 v_1 + m_2 v_2}{m_1 + m_2}
\end{align*}
$$

---

{{8}}
$b)\;\;$ Schritt 2: Kinetische Energien vor und nach dem Stoß

{{8}}
$$
\begin{align*}
E_{kin,\text{vor}} &= \dfrac12 m_1 v_1^2 + \dfrac12 m_2 v_2^2 \\
E_{kin,\text{nach}} &= \dfrac12 (m_1 + m_2)\,{v'}^{2}
= \dfrac{(m_1 v_1 + m_2 v_2)^2}{2 (m_1 + m_2)}
\end{align*}
$$

---

{{9}}
$c)\;\;$ Schritt 3: "Energieverlust" $\Delta E_{kin} =  E_{kin,\text{vor}} - E_{kin,\text{nach}}$

{{9}}
Nach Ausmultiplizieren und Zusammenfassen ergibt sich die Standardform:

{{9}}
$$
\Delta E_{kin}
= \dfrac12 \,\frac{m_1 m_2}{m_1 + m_2}\,(v_1 - v_2)^2
$$

{{9}}
Diese Darstellung macht die Abhängigkeit von der Relativgeschwindigkeit $(v_1 - v_2)$ und der reduzierten Masse $\mu = \dfrac{m_1 m_2}{m_1 + m_2}$ sichtbar.

---

{{10}}
Schritt 4 (optional): Relativer "Verlust"

{{10}}
$$ 
\frac{\Delta E_{kin}}{E_{kin,\text{vor}}}
= 1 - \frac{(m_1 v_1 + m_2 v_2)^2}{(m_1 + m_2)\,(m_1 v_1^2 + m_2 v_2^2)}
$$

---

{{10}}
Zusammenfassung

{{10}}
$$
\begin{align*}
v' &= \frac{m_1 v_1 + m_2 v_2}{m_1 + m_2} \\
\Delta E_{kin} &= \frac12 \,\frac{m_1 m_2}{m_1 + m_2}\,(v_1 - v_2)^2
\end{align*}
$$


---

{{11}}
$d)\;\;$ Diese Energie wird in Umformungs- und somit auch Wärmeenergie umgewandelt. Somit der erste Hauptsatz der Thermodynamik nicht verletzt.




---
<br>
---




__Aufgabe 3:__ Energieumwandlung beim freien Fall

Ein Körper der Masse $m$ wird aus der Höhe $h$ ohne Anfangsgeschwindigkeit fallen gelassen. Die aktuelle Höhe sei $y < h$. Luftwiderstand wird vernachlässigt, $g$ sei ortskonstant.

$a)\;\;$ **Gib** die Energieerhaltung zwischen den Höhen $h$ (Start) und $y$ (aktuell) **an**.

$b)\;\;$ **Leite** daraus $v(y)$ **her** und **zeige** die Unabhängigkeit von $m$.

$c)\;\;$ **Zeige** die Übereinstimmung mit der kinematischen Beziehung für gleichmäßige Beschleunigung.

---

{{12}}
$a)\;\;$ Schritt 1: Energieerhaltung

{{12}}
$$
\begin{align*}
E_{\text{pot}}(h) + E_{\text{kin}}(h) &= E_{\text{pot}}(y) + E_{\text{kin}}(y) \\
m g h + 0 &= m g y + \dfrac12 m v^2
\end{align*}
$$

---

{{13}}
$b)\;\;$ Schritt 2: Umformen auf $v(y)$

{{13}}
$$
\begin{align*}
\dfrac12 m v^2 &= m g (h - y) \\
v^2 &= 2 g (h - y) \\
v &= \sqrt{\,2 g (h - y)\,}
\end{align*}
$$

---

{{14}}
Schritt 3: Unabhängigkeit von der Masse

{{14}}
$$
\begin{align*}
\dfrac12 \,\cancel{m}\, v^2 &= \cancel{m}\, g (h - y)
\end{align*}
$$

{{14}}
Die Masse kürzt sich; $v$ hängt nicht von $m$ ab.

---

{{15}}
$c)\;\;$ Schritt 4: Konsistenz mit der Kinematik

{{15}}
Mit der Fallstrecke $s = h - y$ und konstanter Beschleunigung $g$ gilt kinematisch

{{15}}
$$
\begin{align*}
v^2 &= 2 g s = 2 g (h - y),
\end{align*}
$$

{{15}}
also identisch zum Ergebnis aus der Energieerhaltung.



---
<br>
---



__Aufgabe 4:__ Rückstoß (Rollbrett + Ball), Impulserhaltung

Eine Person der Masse $M$ steht reibungsfrei auf einem Rollbrett. Sie wirft einen Ball der Masse $m$ mit der zur Erde gemessenen Geschwindigkeit $u$ nach vorne. Das System war zuvor in Ruhe.

$a)\;\;$  **Gib** die Impulserhaltung **an** und **leite** die Geschwindigkeit $V'$ der Person nach dem Wurf **her**.

$b)\;\;$  **Gib** die Richtung und Betrag von $V'$ **an**.

---

{{16}}
$a)\;\;$ Schritt 1: Impulserhaltung (gesamter Anfangsimpuls ist null)

{{16}}
$$
\begin{align*}
0 \;=\; M\,V' \;+\; m\,u
\end{align*}
$$

{{16}}
Vorzeichenkonvention: $u>0$ in Wurfrichtung (nach vorne).

---

{{17}}
$b)\;\;$ Schritt 2: Auflösen nach $V'$

{{17}}
$$
\begin{align*}
M\,V' &= -\,m\,u \quad \left| : M  \right.\\
V' &= -\,\dfrac{m}{M}\,u
\end{align*}
$$

---

{{18}}
Schritt 3: Interpretation

{{18}}
Das Minuszeichen zeigt: Die Person bewegt sich **entgegen** der Wurfrichtung.  
Der Betrag lautet

{{18}}
$$
\begin{align*}
\lvert V' \rvert \;=\; \dfrac{m}{M}\,u \,.
\end{align*}
$$

---

{{19}}
Zusammenfassung

{{19}}
$$
\begin{align*}
V' \;=\; -\,\dfrac{m}{M}\,u, \qquad \lvert V' \rvert \;=\; \dfrac{m}{M}\,u \,.
\end{align*}
$$

{{19}}
Hinweis: Der Gesamtimpuls bleibt erhalten; die (später betrachtbare) Zunahme von $E_{\text{kin}}$ des Systems stammt aus der beim Wurf aufgewendeten inneren Arbeit.












## Das Feld


In der Physik wird der Begriff Feld verwendet, um Kräfte zu beschreiben, die auf einen Körper wirken, ohne dass direkter Kontakt zu einer anderen Materie besteht. Ein klassisches Beispiel ist die Gravitation: Die Erde übt eine Kraft auf jeden Körper in ihrer Nähe aus, auch wenn dieser sie nicht berührt. Um dieses „Fernwirken“ zu verstehen, wurde das Konzept des Gravitationsfeldes eingeführt.

Ein Feld ordnet jedem Punkt im Raum eine bestimmte Größe zu. Im Fall der Gravitation ist dies die Gravitationsfeldstärke $g$, die angibt, wie groß die Kraft pro Kilogramm Masse an diesem Punkt ist. Damit kann die Wirkung der Schwerkraft auf einen Körper durch eine einfache Multiplikation bestimmt werden: $Kraft = Masse \cdot Feldstärke$. Die Feldvorstellung ersetzt somit das abstrakte Bild einer unmittelbaren Fernkraft durch die Vorstellung, dass der Raum selbst an jedem Punkt eine bestimmte physikalische Eigenschaft besitzt.

Die Feldstärke hängt von der Masse ab, die das Feld erzeugt, und nimmt mit wachsendem Abstand ab. In der Nähe der Erde beträgt sie ungefähr $9,81\,\dfrac{\text{N}}{\text{kg}} $ und wirkt immer in Richtung des Erdmittelpunkts. Auch der Mond, die Sonne oder andere Himmelskörper erzeugen solche Felder, die zusammenwirken.

Die Einführung des Feldbegriffs hat die Physik grundlegend verändert. Sie erlaubt nicht nur eine anschauliche Beschreibung der Gravitation, sondern bildet auch die Grundlage für andere Bereiche, etwa elektrische und magnetische Felder. Felder machen sichtbar, dass Kräfte nicht plötzlich und punktweise wirken, sondern durch den Raum verteilt sind. Dadurch lassen sich auch komplexe Situationen, in denen mehrere Quellen zusammenwirken, systematisch und präzise berechnen.



Es wird ersichtlich, dass bei der Division der Kraft durch die Ladung der betrachteten Kraft gleich der Feldstärke ist. 

$$
\begin{align*} 
Kraft & = \textcolor{red}{Ladung} \cdot Feldstärke  \\
F_C & = \textcolor{red}{q} \cdot  E   \quad \text{Elektrisches Feld (allgemein)}  \\  
\end{align*}
$$

{{0}}
__Aufgabe 1:__ **Gib** die Gleichung **an**, die die Feldstärke des erdnahen Graviationsfeld im Bezug zu seiner Ladung und Kraft setzt. \


{{1}} $$
\begin{align*}  
F_G & = \textcolor{red}{m} \cdot  g    \quad \text{Gravitation (Erdnah)} \\ 
\end{align*}
$$


{{2}}
Um das Feld sichtbar zu machen, wird zunächst eine zweidimensionale Draufsicht verwendet. Hierbei befindet sich eine Ladung in der Mitte, während in allen Richtungen gleichmäßig die sogeannten Feldlinien abgehen. 



{{2}}
<center>
<!-- style="width:500px" -->
![](Feldoben.png)
</center>

{{2}}
Es wird deutlich, dass die Feldlinien mit wachsendem Abstand zur Quelle weiter auseinander liegen und somit immer längere Umfangsteilstrecken zwischen den Feldlinien sind. Die Feldliniendichte nimmt somit ab. Diese Feldliniendichte gibt somit Aufschluss auf die Stärke der Kraft. Die farbigen Linien beschreiben somit Bereiche gleicher potentieller Energie. \


{{3}}
Noch deutlicher wird dieses Feldlinienmodell in einer dreidimensionalen Darstellung. \


{{3}}
<center>
<!-- style="width:750px" -->
![](Kugelober.png)
</center>

{{3}}
Es ist schnell zu erkennen, dass pro gleichgroßer Fläche immer weniger Feldlinien bei höherem Abstand die Flächen durchdringen. Somit gilt die Antiproportionalität, dass bei wachsender Kugeloberfläche $O = 4 \pi r^2$ die wirkende Kraft abnimmt. Somit ergeben sich für radialsymmetrische Felder folgende Gleichungen der Kräfte:


{{4}}
$$
\begin{align*} 
F & \propto \dfrac{1}{4 \pi r^2} \\
Kraft & = \textcolor{red}{Ladung} \cdot Feldstärke  \\
F_C & = \textcolor{red}{q} \cdot  \dfrac{1}{4 \pi \epsilon_0} \dfrac{Q}{r^2}   \quad \text{Elektrisches Feld}  \\  
\end{align*}
$$


{{5}}
__Aufgabe 2:__ **Gib** die Gleichung **an**, die die Feldstärke des allgemeinen Graviationsfeld im Bezug zu seiner Ladung und Kraft setzt. \


{{6}}
$$
\begin{align*} 
F_G & = \textcolor{red}{m} \cdot  \dfrac{1}{4 \pi \gamma} \dfrac{M}{r^2} \quad \text{Gravitation}    \\ 
\end{align*}
$$

{{6}}
wobei $\gamma$ und $\epsilon_0$ die Proportionalitätskonstanten sind, die die Einheiten auf die bereits bekannten Einheiten anpassen. Dabei unterscheiden sich die Gleichungen für die Gravitation und die der elektrischen Kraft strukturell nicht. Dieses Konzept kann auch auf die Intensität von Licht, radioaktiver Strahlung und vieles weiteres anwende. 


{{7}}
??[](https://phet.colorado.edu/sims/html/magnets-and-electromagnets/latest/magnets-and-electromagnets_all.html)












## Das Potential $\Phi$


Während das Gravitationsfeld beschreibt, wie groß die Kraft an einem Punkt im Raum ist, geht das Konzept des Potentials einen Schritt weiter. Ein Potential ordnet jedem Punkt nicht die Kraft selbst, sondern eine Energie pro Masseneinheit zu. Es beantwortet die Frage: Wie viel Energie besitzt ein Körper allein dadurch, dass er sich an einem bestimmten Ort im Feld befindet?


$$
\begin{align*} 
\Delta E_{pot} = F(r) \cdot \Delta r \\ 
\end{align*}
$$

Im Gravitationsfeld der Erde lässt sich diese Idee besonders einfach nachvollziehen. Hebt man einen Körper an, verrichtet man Arbeit gegen die Schwerkraft. Diese Arbeit wird als potenzielle Energie gespeichert. Befindet sich der Körper höher, so kann er beim Herunterfallen mehr Energie freisetzen. Das Potential gibt somit an, wie „hoch“ die Lageenergie pro Kilogramm an einem bestimmten Ort ist – unabhängig davon, ob sich dort gerade ein Körper befindet oder nicht.


> $$
\begin{align*} 
E_{pot} = \Phi(r) \cdot q \\ 
\end{align*}
$$

Das Potential ist eng mit der Feldstärke verknüpft: _Die Feldstärke entspricht dem Gefälle des Potentials_. Anschaulich bedeutet dies, dass ein Körper immer in Richtung abnehmenden Potentials beschleunigt wird – vergleichbar mit einem Ball, der auf einer schiefen Ebene in Richtung Tal rollt.

Das Konzept des Potentials spielt nicht nur in der Gravitation, sondern auch in der Elektrostatik eine zentrale Rolle. Es macht sichtbar, dass Felder nicht nur Kräfte beschreiben, sondern auch gespeicherte Energie in Raum und Position binden.

Oftmals kann bei einem genügend großen Abstand jedes Feld auf eine Punktquelle reduziert werden. Dies ist als Funktion in der folgenden Abbildung verdeutlicht:

<center>
<!-- style="width:500px" -->
![](Feldseite.png)
</center>

Wenn man die Feldlinien in zwei Dimensionen betrachtet würde das Potential dazu die dritte Dimension darstellen.

<center>
<!-- style="width:500px" -->
![](Feld3D.png)
</center>

In diesem Bild wird schon die Grunderkenntnis der allgemeinen Relativitätstheorie deutlich, da die Linien stets alle gerade sind, jedoch durch ihre Abbildung von der Draufsicht erscheinen die daraus resultierenden Flächen unterschiedlich groß. Das bedeutet, dass diese geometrischen Interpretationen in vielen Bereichen ähnlich sind und mächtige Vorhersagen treffen lassen können.

??[](https://www.didaktikonline.physik.uni-muenchen.de/programme/e_feld/E_Feld_leifi.html)




{{0}}
__Aufgabe 1:__ **Gib** eine Gleichung für das allgemeine Gravitationspotential **an**. \
<br>


{{1}}
$$
\begin{align*} 
E_{pot} & =  \Phi(r) q \quad \text{mit:}\;\; E_{pot} = F(r)  r \\ 
F(r)  r  & =  \Phi(r) q \quad \text{mit:}\;\;   F(r) = \dfrac{1}{4 \pi \gamma} \dfrac{m M}{r^2} \;\; \wedge \;\; q = m \\ 
\dfrac{1}{4 \pi \gamma} \dfrac{m M}{r^2}  r  & =  \Phi(r) m  \quad \left| : m  \right.  \\ 
\dfrac{1}{4 \pi \gamma} \dfrac{ M}{r}    & =  \Phi(r)       \\ 
\end{align*}
$$






## Differentiation



Im folgenden Video wird das Beschriebene aus diesem Thema nochmal anhand von Beispielen erklärt:  \

!?[Differentation](https://www.youtube.com/watch?v=quQtPwW04B0)


### Differentiation - Übungen



$F = -q \dfrac{d \Phi(r)}{d r}$


## Integration


Im folgenden Video wird das Beschriebene aus diesem Thema nochmal anhand von Beispielen erklärt:  \

!?[Integration](https://www.youtube.com/watch?v=ppdwq_KDMoE)




### Integration - Übungen






## Euler-Lagrange-Gleichungen



## Noether-Theorem




## Hamiliton-Formalismus



## Bahnkurve







