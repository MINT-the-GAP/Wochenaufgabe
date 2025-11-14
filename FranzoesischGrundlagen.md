<!--
version:  0.0.2
language: de

tags: Demo, Französisch
comment: Grundwortschatzübungen für Französisch
author: Martin Lommatzsch


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


# Klassisches Vokabeltraining


<!-- data-solution-button="2" data-show-partial-solution -->
|Deutsch |Französisch|
|:------:|:---------:|
| Hallo  | [[ Salut ]] |
| Wie bitte?  | [[ Comment? ]] |
| [[ Auf Wiedersehen ]]  | Au revoir |
| Ich heiße  | [[ Je m'appelle ]] |
| [[ Gut ]]  | Bien |



# Vokabeln zuordnen

Aufgabe 1: Ordne die Kacheln richtig zu.


<!-- data-solution-button="2" data-show-partial-solution -->
Wie geht es Ihnen?  [->[Comment allez-vous]]? \
Kreuzen Sie an. [->[Cochez]]. \


Aufgabe 2: Ordne die Kacheln richtig zu.


<!-- data-solution-button="2" data-show-partial-solution -->
[->[Antworten Sie]]. Répondez. \
[->[Der Bruder]]. le frère. \


# Aussprachetraining

@SpeechRecognition.support

---


__$a)\;\;$__ Sprich 'Danke' auf französisch.


<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Merci`)

---


__$b)\;\;$__ Sprich 'ein Kind' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`un enfant`)

---


__$c)\;\;$__ Sprich 'Wer ist das?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Qui est-ce?`)

---


__$d)\;\;$__ Sprich 'Quelle est votre adresse?' korrekt aus.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Quelle est votre adresse?`)