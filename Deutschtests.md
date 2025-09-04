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






@komma: @komma_(@uid,`@0`,`@1`)

@komma_
<input
  data-id="lia-quiz-@0"
  class="lia-input lia-quiz__input"
  style="margin-bottom: 2rem"
  value="@1">

[[!]]
<script>
const eingabe = document.querySelector('[data-id="lia-quiz-@0"]').value.toLocaleLowerCase().replace(/\s+/g,"")

eingabe == "@2".toLocaleLowerCase().replace(/\s+/g,"")
</script>
@end







narrator: Deutsch Female

vorlesen: {|>}{<span style="position: absolute; left: -10000px">@0</span>} [[  @0  ]]


-->



# Deutsch






__Aufgabe 1:__ Hör dir den Satz an und schreib ihn korrekt in das Eingabefeld.


{{|> Deutsch Female}}
<!-- style="position: absolute; left: -9999px;" -->
Anna sitzt auf einem fliegenden Teppich.

[[    Anna sitzt auf einem fliegenden Teppich.    ]]


---

---

__Aufgabe 2:__ Setze das Komma an die richtige Stelle. (Auflösung geht noch nicht und ist deswegen blockiert.)

<!-- data-solution-button="false" -->
@komma(`Das ist der Tag an dem ich geblitzt wurde.`,`Das ist der Tag, an dem ich geblitzt wurde.`)


---

---

__Aufgabe 3:__ Lass dir die Wörter vorlesen, die in die Lücken kommen und schreibe diese in die Lücken.

Anna ging in einen @vorlesen(Zoo). Dort konnte sie auf einem @vorlesen(Lama) reiten.




---

---


__Aufgabe 4:__ Fülle die Tabelle zu den Adjektiven aus.


<!-- data-solution-button="2" data-show-partial-solution -->
|  Positiv  |  Komparativ |  Superlativ  |
|:----:|:-----:|:-----:|
|  groß   | [[  größer     ]]  | [[  am größten  ]]  |
|  [[ schlecht ]]  | schlechter  | [[  am schlechtesten  ]]  |
|  gut   | [[  besser     ]]  | [[  am besten   ]]  |




---

---





__Aufgabe 5:__ Ziehe die richtigen unbestimmten Artikel in die Lücken. 

> (Hinweis: Auf Touchbildschirmen bitte aktuell noch erst das Feld mit der Lücke antippen dann das gewünschte Wort.)

Die Fliege flog über [->[ (einen) | einem | ein ]] Teich.








---

---




__Aufgabe 6:__ **Gib** die passende Wortart **an**.


groß  [[(Adjektiv)|Adverb|Artikel|Interjektion|Konjunktion|Numeral|Nomen|Präposition|Pronomen|Substantiv|Verb]]  \
der  [[Adjektiv|Adverb|(Artikel)|Interjektion|Konjunktion|Numeral|Nomen|Präposition|Pronomen|Substantiv|Verb]]  \
laufen  [[Adjektiv|Adverb|Artikel|Interjektion|Konjunktion|Numeral|Nomen|Präposition|Pronomen|Substantiv|(Verb)]]  \
einige  [[Adjektiv|Adverb|Artikel|Interjektion|Konjunktion|(Numeral)|Nomen|Präposition|Pronomen|Substantiv|Verb]]  \
Haus  [[Adjektiv|Adverb|Artikel|Interjektion|Konjunktion|Numeral|(Nomen)|Präposition|Pronomen|(Substantiv)|Verb]]  \
heute  [[Adjektiv|(Adverb)|Artikel|Interjektion|Konjunktion|Numeral|Nomen|Präposition|Pronomen|Substantiv|Verb]]  \
ach  [[Adjektiv|Adverb|Artikel|(Interjektion)|Konjunktion|Numeral|Nomen|Präposition|Pronomen|Substantiv|Verb]]  \
ich  [[Adjektiv|Adverb|Artikel|Interjektion|Konjunktion|Numeral|Nomen|Präposition|(Pronomen)|Substantiv|Verb]]  \
oder  [[Adjektiv|Adverb|Artikel|Interjektion|(Konjunktion)|Numeral|Nomen|Präposition|Pronomen|Substantiv|Verb]]  \
an  [[Adjektiv|Adverb|Artikel|Interjektion|Konjunktion|Numeral|Nomen|(Präposition)|Pronomen|Substantiv|Verb]]  




---

---


__Aufgabe 7:__ Füll den Lückentext aus. (Richtige Lücken werden beim Prüfen grün markiert.)

<!-- data-show-partial-solution -->
Es war einmal ein kleines Dorf am Rande eines tiefen Waldes. Die Menschen dort lebten friedlich, doch jedes Jahr, wenn der erste Schnee fiel, verschwand ein Eimer voll goldener Äpfel aus dem Vorratshaus des Königs. Niemand wusste, wer sie stahl. \
Eines Abends beschloss die junge Magd Clara, das Geheimnis zu lüften. Mit einer Laterne in der Hand schlich sie zum Vorratshaus. Sie versteckte sich hinter einem Fass und wartete. Plötzlich hörte sie ein leises Kichern. Durch das Fenster flatterten winzige, funkelnde Gestalten: Waldelfen! Sie trugen die [[  Äpfel  ]] fort, als wären sie leicht wie Federn. \
Clara folgte ihnen in den verschneiten Wald. Dort sah sie, wie die Elfen die [[  goldenen  ]] Äpfel in einen großen [[  Korb  ]] legten, aus dem helles Licht strahlte. „Warum nehmt ihr die [[  Äpfel  ]]?“, fragte Clara mutig. \
Die Elfen erklärten: „Wir brauchen ihr Licht, um die Tiere des Waldes durch den langen Winter zu führen. Ohne sie würden viele erfrieren.“ \
[[  Clara  ]] kehrte zurück und berichtete dem [[  König  ]]. Der war zunächst zornig, doch dann verstand er. Von diesem Tag an ließ er jedes Jahr einen Teil der goldenen Äpfel für die [[  Elfen  ]] zurück – und das Dorf lebte in Harmonie mit dem geheimnisvollen Waldvolk.




__Aufgabe 7a:__ Entscheide, ob die Aussage wahr oder falsch ist:

Der König ließ die Elfen verfolgen und einsperren. [[wahr|(falsch)]]







---

---

__Aufgabe 8:__ Lies den Satz fehlerfrei vor.



Ich gehe nach Hause.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(de-DE,`Ich gehe nach Hause.`)





---

---

__Aufgabe 9:__ Weise die Sätze ich richtig zu.


<!-- data-randomize="true"  -->
| Adverbialsatzkategorie | Beispielsatz |
| :-----: |  :-----:  |
| Temporalsatz      |  [->[(Es ging erst los, nachdem ich ankam.)]]  |
| Kausalsatz        |  [->[(Weil es morgen regnet, fahre ich mit dem Bus.)]]  |
| Konditionalsatz   |  [->[(Falls du gut in Mathematik bist, bekommst du eine Belohnung.)]]  |




---

---

__Aufgabe 10:__ Setze die Satzzeichen so, dass der Satz eine korrekte wörtliche Rede darstellt. (Auflösung geht noch nicht und ist deswegen blockiert.)

<!-- data-solution-button="false" -->
__$a)\;\;$__
@komma(`Der Apfel ist rot sagte Ben`,`"Der Apfel ist rot", sagte Ben.`)

<!-- data-solution-button="false" -->
__$b)\;\;$__
@komma(`Clara sagt Druck ist eine physikalische Größe`,`Clara sagt: "Druck ist eine physikalische Größe."`)




---

---

__Aufgabe 11:__ Wähle aus, was den unterstrichenen Teil des Satzes richtig beschreibt.

Helga fuhr mit dem Auto <u>ihres Freundes</u>.

<!-- data-randomize="true"  -->
- [[X]] Genetivattribut
- [[ ]] Dativobjekt
- [[ ]] Subjekt
- [[ ]] Predikat



---

---

__Aufgabe 12:__ Korrigiere die Rechtschreibfehler im gezeigten Satz. (Auflösung geht noch nicht und ist deswegen blockiert.)

<!-- data-solution-button="false" -->
@komma(`Es ist jetze um sechse.`,`Es ist jetzt um sechs.`)




---

---

__Aufgabe 13:__ Sortiere die Wörter in alphabetischer Reihenfolge.

<!-- data-randomize="true"  -->
[->[(Diskurs)]] [->[(Festival)]] [->[(Glut)]] [->[(Nihilismus)]] [->[(Priorität)]] [->[(Residuum)]]




