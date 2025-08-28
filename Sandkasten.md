<!--
version:  0.0.1

language: de

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

@round
<script>
  let value = `@input`;
  if (value.startsWith("@")) {
    ""
  } else {
    value = JSON.parse(value);
    value = value[0]
    value = value.replace(/,/g, ".");
    value = parseFloat(value);
    value = Math.round(value * Math.pow(10,@1)) / Math.pow(10,@1);
    value == @0
  }
</script>
@end





import: https://raw.githubusercontent.com/liaTemplates/ABCjs/main/README.md


import: https://raw.githubusercontent.com/LiaTemplates/Speech-Recognition-Quiz/refs/heads/main/README.md


-->




# Deutsch

Diktat




Wortarten




# Mathematik

Randomizer Bruchrechnung

MathJXS



# Englisch

Exercise 1: Speak out loud

@SpeechRecognition.support

---

Say 'Good morning' in English.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(en-US,`Good morning`)

---

Say 'Hello' in English.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(en-US,`Hello`)

---

Say 'Cucumber' in English.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(en-US,`Cucumber`)

---

Say 'Desire' in English.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(en-US,`Desire`)







Lückentext mit Kacheln

Ellen goes to school. [->[ He | (She) | It ]] wants to learn.  [->[ His | (Her) | Its ]] first subject today is math.


# Physik




<!-- style="width:500px" -->
|  $m$ in [kg]  |  $V$ in $\left[ \dfrac{\text{m}^3}{\text{kg}} \right]$ |
|:----:|:-----:|
|  2   | 3.95  |
|  1   | 2.2   |
|  3   | 5.7   |
|  9   | 17.5  |
|  7   | 14.2  |
|  11  | 22.1  |
|  13  | 25.8  |







??[](https://phet.colorado.edu/sims/html/sound-waves/latest/sound-waves_all.html)

# Chemie




Lückentext

# Biologie



Aufgabe 1: Ziehe den Frosch ins Feld, der giftig ist.


[->[ ![](https://media.istockphoto.com/id/1297875622/de/foto/mantella-cowanni-wikipedia.jpg?s=612x612&w=0&k=20&c=XZJxaA4bpLTHmMzJTcpeQ6mSSX0qf7nFXHcwfQruGuE=)<!-- style="height:100px" --> | (![](https://live.staticflickr.com/6237/6268436677_846a796410_b.jpg)<!-- style="height:100px" --> ) ]]

-----------




# Informatik


Aufgabe 1: Korrigiere den Fehler im Code und lass dir die Anzahl der Buchstaben der Nachricht ausgeben. Drück dazu mal unten links dieses </> Symbol.

``` js
var message = "Dies ist die Nachricht"
console.log(message)
message.leangth
```
<script>@input </script>






# Musik

Aufgabe 1: Klicke auf die beiden Noten und gib die Kadenz an.

``` abc  @ABCJS.render
X: 1
L: 1/2
K: C
[|\
C G:|
```

Kadenz: [[  Quinte  ]]





# Kunst

Bild zu Künstler

Nenne X aus Y

# Geschichte

Aufgabe 1: Ordne die Kriege chonologisch. Fange links bei dem Krieg an, der am weitesten in der Vergangenheit liegt.

 [->[ (Punische Kriege) ]] [->[ (Dreißigjähriger Krieg) ]] [->[ (1. Weltkrieg) ]] [->[ (2. Weltkrieg) ]] [->[ (Vietnamkrieg) ]]





# Geographie




Bildpositionen?

# GRW




Multiple Choice

# Deutsch als Zweitsprache

Übersetzungsfunktion




