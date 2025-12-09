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






## Macarons in der neuen Bäckerei

Eine neu eröffnete Bäckerei in der Stadt spezialisiert sich auf Macarons.  
Da sie neu geöffnet ist, testet sie zuerst die Nachfrage mit zwei verschiedenen Sorten der
Macarons und produziert zunächst insgesamt $300$ Macarons mit Schokoladen- oder Zitronengeschmack.

Nach dem ersten Eröffnungstag haben viele Menschen die Bäckerei besucht und Macarons bestellt.  
Von den Kunden, die einen Schoko-Macaron gekauft haben, haben $90$ keine Bewertung gelassen.  
Von den Zitronen-Macaron gekauften Kunden haben $18$ eine Fünf-Sterne-Bewertung hinterlassen. Insgesamt gaben $180$ Kundinnen und Kunden eine Fünf-Sterne-Bewertung ab.



__Aufgabe 1:__

__$a)\;\;$__ **Erstelle** eine geeignete Vierfeldertafel und **ergänze** die fehlenden Werte.

Definiere dazu die Ereignisse:

- $S$: „Kunde kauft einen Schoko-Macaron“
- $\bar{S}$: „Kunde kauft einen Zitronen-Macaron“
- $B$: „Kunde gibt eine Fünf-Sterne-Bewertung ab“
- $\bar{B}$: „Kunde gibt keine Bewertung ab“

Trage die absoluten Häufigkeiten in die Vierfeldertafel ein:


<!-- data-type="none" data-sortable="false" -->
|                      | $B$ (5 Sterne) | $\bar{B}$ (keine Bewertung) | Summe      |
|----------------------|:-------------:|:----------------------------:|:----------:|
| $S$ (Schoko)         | [[162   ]]    | [[   90 ]]                   | [[   252]] |
| $\bar{S}$ (Zitrone)  | [[18    ]]    | [[   30 ]]                   | [[   48 ]] |
| Summe                | [[180   ]]    | [[   120]]                   | [[   300]] |




---

---



__$b)\;\;$__ **Berechne** den Anteil (in Prozent) der Kundinnen und Kunden, die keine Bewertung abgegeben haben.  
Gib das Ergebnis als ganze Prozentzahl an.

$p(\bar{B}) = $ [[  40  ]]$\,\%$
********************
$p(\bar{B}) = \dfrac{120}{300} = 0{,}4 = 40\ \%$
********************



---

---



__$c)\;\;$__ **Bestimme** die Wahrscheinlichkeit (in Prozent),  
dass ein zufällig ausgewählter Kunde, der eine Fünf-Sterne-Bewertung abgegeben hat,  
einen Zitronen-Macaron gekauft hat.  

Gib das Ergebnis als ganze Prozentzahl an.

$P(\bar{S} \mid B) = $ [[  10  ]]$\,\%$
********************
$$
P(\bar{S} \mid B)
= \frac{P(\bar{S} \cap B)}{P(B)}
= \frac{\frac{18}{300}}{\frac{180}{300}}
= \frac{18}{180}
= 0{,}1
= 10\ \%.
$$
********************



---

---




__$d)\;\;$__ Untersuche**, ob die Ereignisse „Sorte“ (Schoko oder Zitrone) und „Bewertung“ (5 Sterne oder keine Bewertung) stochastisch unabhängig sind. **Begründe** deine Entscheidung mithilfe der Vierfeldertafel.



[[stochastisch unabhängig|(stochastisch abhängig)]]
********************
Die Ereignisse „Sorte“ und „Bewertung“ sind genau dann stochastisch unabhängig, wenn
$$
P(\bar{S} \cap B) = P(\bar{S}) \cdot P(B)
$$
gilt.

Wir berechnen aus der Vierfeldertafel:
$$
P(\bar{S} \cap B) = \frac{18}{300} = 0{,}06
$$
$$
P(\bar{S}) = \frac{48}{300} = 0{,}16,\quad
P(B) = \frac{180}{300} = 0{,}6
$$
Damit
$$
P(\bar{S}) \cdot P(B) = 0{,}16 \cdot 0{,}6 = 0{,}096
$$
Da $0{,}06 \neq 0{,}096$, gilt die Unabhängigkeitsbedingung nicht.  
Die beiden Merkmale sind also **nicht stochastisch unabhängig**.
********************



---

---




__Aufgabe 2:__


Da man schnell und präzise Macarons produzieren möchte, wird eine Maschine angeschafft,
die Macarons in großer Stückzahl herstellt.  
Es ist bekannt, dass $4\,\%$ der hergestellten Macarons fehlerhaft sind.

Wir nehmen im Folgenden an, dass die Macarons unabhängig voneinander
mit Wahrscheinlichkeit $p = 0{,}04$ fehlerhaft sind.

---

__$a)\;\;$__ Ein Kunde kauft $100$ Macarons aus dieser Produktion.

Definiere die Zufallsvariable
$$
X := \text{„Anzahl fehlerhafter Macarons unter den 100 gekauften“}.
$$

Dann gilt $X \sim B(n=100,\;p=0{,}04)$.

1. **Bestimme** die Wahrscheinlichkeit, dass höchstens $10$ der $100$ Macarons fehlerhaft sind.  

2. **Bestimme** die Wahrscheinlichkeit, dass kein Macaron fehlerhaft ist.  

*(Runde auf zwei Nachkommastellen.)*

$P(X \le 10) \approx$ [[  99,78  ]]$\,\% \;\;\wedge\;\;$ $P(X = 0) \approx$ [[  1,69  ]]$\,\%$
@Algebrite.check([99.78;1.69])
********************
1. $X \sim B(100; 0{,}04)$, gesucht ist
   $$
   P(X \le 10) = \sum_{k=0}^{10} \binom{100}{k} (0{,}04)^k (0{,}96)^{100-k}.
   $$
   Mit dem Taschenrechner (Binomialverteilung, kumuliert) erhält man
   $$
   P(X \le 10) \approx 0{,}9978 \approx 99{,}78\ \%.
   $$

2. Die Wahrscheinlichkeit, dass kein Macaron fehlerhaft ist:
   $$
   P(X = 0) = (0{,}96)^{100} \approx 0{,}0169 \approx 1{,}69\ \%.
   $$
********************

---

---



__$b)\;\;$__ Die Bäckerei möchte für einen größeren Auftrag $250$ fehlerfreie Macarons liefern.
Aufgrund der Ausschussquote muss sie mehr als $250$ Macarons produzieren.

Sei
$$
Y := \text{„Anzahl fehlerfreier Macarons in einer Produktion von $n$ Stück“}.
$$
Dann gilt $Y \sim B(n,\;0{,}96)$, da ein Macaron mit Wahrscheinlichkeit $0{,}96$ fehlerfrei ist.

1. **Bestimme** die kleinste Produktionsmenge $n$, so dass mit mindestens $95\ \%$
   Wahrscheinlichkeit mindestens $250$ fehlerfreie Macarons entstehen.

2. **Bestimme** die kleinste Produktionsmenge $n$, so dass mit mindestens $98{,}7\ \%$
   Wahrscheinlichkeit mindestens $250$ fehlerfreie Macarons entstehen.


$ P(Y \ge 250) \ge 0{,}95 \;\;\Rightarrow\;\; n =$ [[  266  ]] \
$   P(Y \ge 250) \ge 0{,}987 \;\;\Rightarrow\;\; n =$ [[  268  ]]
@Algebrite.check([266;268])
********************

Wir suchen jeweils das kleinste $n$, für das

1. $P(Y \ge 250) \ge 0{,}95$ (bzw.)
2. $P(Y \ge 250) \ge 0{,}987$

gilt, wobei $Y \sim B(n; 0{,}96)$.

Für ein gegebenes $n$ berechnet man mit dem Taschenrechner
$$
P(Y \ge 250) = 1 - P(Y \le 249).
$$

- Für $n = 265$ ist $P(Y \ge 250) < 0{,}95$.
- Für $n = 266$ erhält man
  $$
  P(Y \ge 250) \approx 0{,}952 \quad (\text{also } \ge 0{,}95).
  $$
  Damit ist $n = 266$ die **kleinste** Produktionsmenge mit mindestens $95\ \%$ Erfolgschance.

- Für $n = 267$ ist $P(Y \ge 250) \approx 0{,}977 < 0{,}987$.
- Für $n = 268$ erhält man
  $$
  P(Y \ge 250) \approx 0{,}988 \quad (\text{also } \ge 0{,}987).
  $$
  Damit ist $n = 268$ die **kleinste** Produktionsmenge mit mindestens $98{,}7\ \%$ Erfolgschance.

Ergebnis:
- Für $95\ \%$: $n = 266$ Macarons produzieren.
- Für $98{,}7\ \%$: $n = 268$ Macarons produzieren.
********************


---

---





__Aufgabe 3__

Die neue Maschine produziert Macarons, deren Durchmesser (in cm) näherungsweise normalverteilt sind.  
Es gilt:
$$
X \sim \mathcal{N}(\mu = 3{,}5\ \text{cm},\ \sigma = 0{,}15\ \text{cm}).
$$

Ein Macaron gilt als „zu groß“, wenn sein Durchmesser größer als $3{,}64\,$cm ist.  
Verkäuflich sind nur Macarons mit einem Durchmesser zwischen $3{,}43\,$cm und $3{,}64\,$cm.  
Alle anderen Macarons (kleiner als $3{,}43\,$cm oder größer als $3{,}64\,$cm) gelten als nicht verkäuflich.

---

---

__$a)\;\;$__ **Bestimme** die Wahrscheinlichkeit (in Prozent, auf eine Dezimalstelle gerundet),  
dass ein zufällig ausgewählter Macaron „zu groß“ ist.

$P(X > 3{,}64) \approx$ [[  17,5  ]] %
********************
Gegeben ist $X \sim \mathcal{N}(3{,}5;\ 0{,}15^2)$.

Ein Macaron ist „zu groß“, wenn $X > 3{,}64$.

Wir standardisieren:
$$
z = \frac{3{,}64 - 3{,}5}{0{,}15}
  = \frac{0{,}14}{0{,}15}
  \approx 0{,}93.
$$

Daraus folgt mit der Standardnormalverteilung $Z \sim \mathcal{N}(0;1)$:
$$
P(X > 3{,}64)
= P\left(Z > 0{,}93\right)
= 1 - \Phi(0{,}93)
\approx 1 - 0{,}8247
\approx 0{,}175 \approx 17{,}5\ \%.
$$
(Die genaue Zahl kann je nach verwendeter Tabelle/CAS leicht variieren.)
********************

---

---

__$b)\;\;$__ **Berechne** die Wahrscheinlichkeit (in Prozent, auf eine Dezimalstelle gerundet),  
dass ein zufällig ausgewählter Macaron nicht verkäuflich ist.  
Nicht verkäuflich bedeutet hier: $X < 3{,}43$ oder $X > 3{,}64$.

$P(\text{nicht verkäuflich}) \approx$ [[  49,6  ]] %
********************

Ein Macaron ist nicht verkäuflich, wenn
$$
X < 3{,}43 \quad \text{oder} \quad X > 3{,}64.
$$

Wir berechnen die beiden Wahrscheinlichkeiten getrennt.

1. Zu klein: $X < 3{,}43$

Standardisierung:
$$
z_1 = \frac{3{,}43 - 3{,}5}{0{,}15}
    = \frac{-0{,}07}{0{,}15}
    \approx -0{,}47.
$$

Also
$$
P(X < 3{,}43)
= P(Z < -0{,}47)
= 1 - \Phi(0{,}47)
\approx 1 - 0{,}6808
\approx 0{,}319 \approx 31{,}9\ \%.
$$

2. Zu groß: $X > 3{,}64$

Dieser Anteil wurde in Teil __$a)\;\;$__ bereits berechnet:
$$
P(X > 3{,}64) \approx 17{,}5\ \%.
$$

3. Nicht verkäuflich (zu klein oder zu groß)

Da sich die Ereignisse „zu klein“ und „zu groß“ gegenseitig ausschließen, gilt:
$$
P(\text{nicht verkäuflich})
= P(X < 3{,}43) + P(X > 3{,}64)
\approx 31{,}9\ \% + 17{,}5\ \%
\approx 49{,}4\ \% \approx 49{,}6\ \%.
$$

Je nach Rundung der Tabellenwerte kann das Resultat leicht abweichen.  
Ein Wert um $49{,}5\ \%$ ist hier korrekt.
********************


---

---






__Aufgabe 4__


Das neu gebildete Team der Bäckerei führt eine Unternehmensbesprechung,  
bei der entschieden werden soll, ob man die neue Maschine kaufen sollte.


In der Besprechung äußert sich ein Teammitglied wie folgt:

> „Ich finde, wir sollten definitiv die neue Maschine kaufen,  
> da sie weniger Fehler macht als unsere jetzige Maschine.“

Um diese Aussage zu überprüfen, werden mit der neuen Maschine als Probe  
$n = 100$ Macarons hergestellt. Dabei sind 2 Macarons fehlerhaft.

Wir bezeichnen mit $p$ die Wahrscheinlichkeit, dass ein mit der neuen Maschine
hergestellter Macaron fehlerhaft ist.

---

---

__$a)\;\;$__
**Formuliere** einen geeigneten einseitigen Hypothesentest, um die Aussage des Teammitglieds zu überprüfen.  
Gib die Nullhypothese $H_0$ und die Gegenhypothese $H_1$ an und erkläre kurz, was sie inhaltlich bedeuten.

[[!]]
<script>true</script>
********************
Wir definieren:
$$
p = \text{Fehlerwahrscheinlichkeit der neuen Maschine}.
$$

Die alte Maschine hat $p_0 = 0{,}04$.

- **Nullhypothese**:
  $$
  H_0 : p = 0{,}04
  $$
  Die neue Maschine ist nicht besser als die alte; sie macht im Mittel genauso viele Fehler.

- **Gegenhypothese (einseitig)**:
  $$
  H_1 : p < 0{,}04
  $$
  Die neue Maschine ist besser als die alte; sie macht weniger fehlerhafte Macarons.
********************

---

---

__$b)\;\;$__
Wir betrachten die Stichprobe von $n = 100$ Macarons mit der neuen Maschine.  
Dabei wurden $X = 2$ fehlerhafte Macarons beobachtet.

Wir führen einen Hypothesentest zum Signifikanzniveau $\alpha = 5\ \%$ durch.

1. **Gib** die Verteilung von $X$ unter der Nullhypothese an.  
2. **Bestimme** eine sinnvolle Entscheidungsregel der Form  
   „Lehne $H_0$ ab, wenn $X$ in einem bestimmten Bereich liegt“.  
3. **Entscheide**, ob die Aussage des Teammitglieds („Die neue Maschine macht weniger Fehler“)  
   statistisch begründet ist.

[[!]]
<script> true </script>
********************
1. Unter $H_0 : p = 0{,}04$ gilt:
   $$
   X \sim B(n = 100,\ p = 0{,}04).
   $$

2. Da $H_1 : p < 0{,}04$ ist, lehnen wir $H_0$ nur dann ab, wenn extrem wenige Fehler auftreten.
   Wir suchen also einen kritischen Wert $k$, sodass
   $$
   P_{H_0}(X \le k) \le \alpha = 0{,}05
   $$
   gilt.

   Wir testen (mit Taschenrechner / CAS):

   - $P_{H_0}(X \le 0) = (0{,}96)^{100} \approx 0{,}0169 < 0{,}05$
   - $P_{H_0}(X \le 1) \approx 0{,}0872 > 0{,}05$

   Also ist der größte ganze $k$ mit $P(X \le k) \le 0{,}05$ gleich $k = 0$.

   **Entscheidungsregel**:
   - Lehne $H_0$ ab, wenn $X = 0$ (d.h. kein fehlerhafter Macaron in der Stichprobe).
   - Behalte $H_0$ bei, wenn $X \ge 1$.

3. In der Stichprobe wurden $X = 2$ fehlerhafte Macarons gefunden.

   Da $2 \ge 1$ ist, liegt $X$ nicht im Ablehnungsbereich.  
   Wir können $H_0$ nicht verwerfen.

   Das bedeutet:
   - Es gibt auf Basis dieser Stichprobe keinen hinreichenden statistischen Beleg,  
     dass die neue Maschine weniger Fehler macht als die alte.
   - Die Aussage des Teammitglieds ist damit statistisch nicht gesichert.
********************

---

---


__$c)\;\;$__
Angenommen, die Aussage des Teammitglieds ist tatsächlich richtig:  
Die neue Maschine macht weniger Fehler als die alte.  
Wir nehmen an, dass ihre Fehlerwahrscheinlichkeit nur noch
$$
p_{\text{neu}} = 0{,}02
$$
beträgt (also etwa halb so groß wie bisher).


**Berechne** die Wahrscheinlichkeit dafür, dass das Team diesen Unterschied  
trotzdem nicht erkennt und sich nach dem Test gegen die Beschaffung der neuen Maschine entscheidet.  


$P(\text{gegen Beschaffung trotz besserer Maschine}) \approx$ [[  86,7  ]] %
********************
Nun gilt tatsächlich
$$
p = p_{\text{neu}} = 0{,}02.
$$

Die Zufallsvariable
$$
X = \text{„Anzahl fehlerhafter Macarons in 100 Stück“}
$$
ist dann
$$
X \sim B(100;\ 0{,}02).
$$

Der Test aus 5.2 lehnt $H_0$ nur dann ab, wenn $X = 0$ ist.  
Das Team entscheidet sich **gegen** die Beschaffung, wenn $X \ge 1$ ist.

Gesucht ist also
$$
P(X \ge 1)
= 1 - P(X = 0)
= 1 - (1 - 0{,}02)^{100}
= 1 - 0{,}98^{100}.
$$

Mit dem Taschenrechner:
$$
0{,}98^{100} \approx 0{,}133
\quad\Rightarrow\quad
P(X \ge 1) \approx 1 - 0{,}133 \approx 0{,}867.
$$

In Prozent:
$$
P(\text{gegen Beschaffung trotz besserer Maschine})
\approx 86{,}7\ \%.
$$

Es ist also **sehr wahrscheinlich**, dass das Team den tatsächlichen Vorteil der neuen
Maschine mit dieser Teststrategie übersieht.
********************



