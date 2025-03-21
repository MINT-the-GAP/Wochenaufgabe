<!--
version:  0.0.1

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

# Tests Seite 1 (Runden)


19,1234?

[[19,1234]]


19,8765?

[[19,8765]]


# Aufgabe Balkendiagramm (Darstellungsproblem?)



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

# Alte Aufgaben (Divisionsstrichproblem)


Berechne den Wert der Terms.

<section class="flex-container">

<div class="flex-child">
__$a)$__

$$
\begin{align*}
2415&   \\
+1213& \\
	&  \\ \hline
  & \\
\end{align*}
$$

[[3628]]
***********
$$
\begin{align*}
2415&   \\
+1213& \\
	&  \\ \hline
  3628& \\
\end{align*}
$$
***********
</div>

 



<div class="flex-child">
__$b)$__

$$
\begin{align*}
3659&   \\
-2235& \\
&  \\ \hline
& \\
\end{align*}
$$

[[1424]]
***********
$$
\begin{align*}
3659&   \\
-2235& \\
&  \\ \hline
1424& \\
\end{align*}
$$
***********
</div>

 


<div class="flex-child">
__$c)$__

$$
\begin{align*}
5034 \cdot 5 &   \\ \hline
 & \\
\end{align*}
$$

[[25170]]
***********
$$\begin{align*}
50_{\textcolor{red}{1}}3_{\textcolor{red}{2}}4 \cdot 5 &   \\ \hline
 25170
\end{align*}
$$
***********
</div>

 




<div class="flex-child">
__$d)$__

$$
\begin{alignat*}{6}
&8&5&4&7&3&:9=     \\
\end{alignat*}
$$

[[09497]]
***********
$$
\begin{alignat*}{6}
&8&5&4&7&3&:9= 09497    \\
-&0&&&&&  \\  \cline{1-2}
&8&5&&&&  \\
-&8&1&&&&  \\  \cline{2-3}
&&4&4&&&  \\
&-&3&6&&&  \\  \cline{3-4}
&&&8&7&&  \\
&&-&8&1&&  \\  \cline{4-5}
&&&&6&3&  \\
&&&-&6&3&  \\  \cline{5-6}
&&&&&0&  \\
\end{alignat*}
$$
***********
</div>



**Aufgabe 1:** Entscheide, ob es sich bei dem Term um einen Vektor, ein Skalar oder einen nicht definierten Ausdruck handelt.
<br>

- [[Vektor]       (Skalar)    [nicht definiert]]
- [    [ ]           [X]             [ ]     ]  $$\left|\vec{a} \times \vec{b}\right|$$
- [    ( )           ( )             (X)     ]  $$\vec{c} \times \left( \vec{a} \circ \vec{b}\right) $$
- [    [X]           [ ]             [ ]     ]  $$s \vec{a} \times \left(\vec{b} \times r \vec{c}\right)$$
- [    (X)           ( )             ( )     ]  $$\left( \vec{c} \circ \vec{b}\right)  \cdot \vec{a}  $$
- [    [ ]           [ ]             [X]     ]  $$\dfrac{\left(\vec{a} \times \vec{c}\right)^2}{\vec{a} \times \vec{b}}$$







</section>
