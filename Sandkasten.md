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

-->




# Aufgabe Balkendiagramm



Gegeben seien die Werte in der gegebenen Tabelle:


<!-- data-type="none" -->
|           Jahr           |   2019   |   2020   |   2021   |   2022   |   2023   |   2024   |   2025   |
| :----------------------: | :------: | :------: | :------: | :------: | :------: | :------: | :------: |
|   Gewinn in $\text{€}$   |   1000   |   1200   |   1100   |   1500   |   1600   |   1300   |   1400   |

$a)\;\;$ **Zeichne** ein Säulendiagramm, dass die relativen Veränderungen von einem Jahr zum nächsten darstellt. (Trage die passenden relativen Werte in Prozent in die Tabelle ein das Säulendiagramm nachzustellen.) **Gib** Periodizitäten gerundet auf zwei Nachkommastellen **an**. Falls ansonsten gerundet werden muss, **gib** zwei Nachkommastellen **an**.

<!--
data-type="barchart"
data-title="Veränderung"
-->
|  2019/20  |    2020/21    |    2021/22   |   2022/23   |    2023/24    |   2024/25   |
| :-------: | :-----------: | :----------: | :---------: | :-----------: | :---------: |
| [[ 20% ]] |  [[ -8.33% ]] | [[ 36.36% ]] | [[ 6.66% ]] | [[ -18.75% ]] | [[ 7.69% ]] |

<br>
<br>
<br>
<br>
