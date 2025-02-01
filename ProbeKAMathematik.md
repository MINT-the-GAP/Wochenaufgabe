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

-->

# Probeklassenarbeit für Mathematik - Klasse 7: Prozentrechnung

<br>

Swipe (Wische) entweder weiter oder klicke unten links auf neben der Seitenzahl auf den Pfeil nach rechts.

<br>

Diese Probearbeit hat mehr Aufgaben als die richtige Arbeit, damit du genug zum Üben hast. Es sind viele verschiedene Aufgabentypen abgebildet, sodass du alles nochmal bei der Bearbeitung dieser Aufgaben wiederholst.

## Aufgabe 1

**Gib** den darstellten roten Anteil vom Ganzen in der Prozentdarstellung **an**. **Gib** Periodizitäten gerundet auf zwei Nachkommastellen **an**. Falls ansonsten gerundet werden muss, **gib** zwei Nachkomma stellen **an**.

<lia-chart option="{
  tooltip: {
    trigger: 'item'
  },
  series: [
  {
    name: 'Segments',
    type: 'pie',
    radius: '50%',
    label: {
      show: false
    },
    data: [
      { value: 1, name: 'Segment 1', itemStyle: { color: 'lightcoral' } },
      { value: 1, name: 'Segment 2', itemStyle: { color: 'lightcoral' } },
      { value: 1, name: 'Segment 3', itemStyle: { color: 'lightcoral' } },
      { value: 1, name: 'Segment 4', itemStyle: { color: 'lightcoral' } },
      { value: 1, name: 'Segment 5', itemStyle: { color: 'lightcoral' } },
      { value: 1, name: 'Empty Segment', itemStyle: { color: 'white', borderColor: 'black', borderWidth: 1 } }
    ],
    emphasis: {
      itemStyle: {
        shadowBlur: 10,
        shadowOffsetX: 0,
        shadowColor: 'rgba(0, 0, 0, 0.5)'
      }
    }
  }]
}"></lia-chart>

[[83,33%]]

---

<svg width="400" height="100" viewBox="0 0 300 200" xmlns="http://www.w3.org/2000/svg">
  <rect x="0" y="0" width="50" height="200" fill="white" stroke="black" stroke-width="1"/>
  <rect x="50" y="0" width="50" height="200" fill="white" stroke="black" stroke-width="1"/>
  <rect x="100" y="0" width="50" height="200" fill="white" stroke="black" stroke-width="1"/>
  <rect x="150" y="0" width="50" height="200" fill="lightcoral" stroke="black" stroke-width="1"/>
  <rect x="200" y="0" width="50" height="200" fill="white" stroke="black" stroke-width="1"/>
  <rect x="250" y="0" width="50" height="200" fill="lightcoral" stroke="black" stroke-width="1"/>
  <rect x="300" y="0" width="50" height="200" fill="lightcoral" stroke="black" stroke-width="1"/>
  <rect x="350" y="0" width="50" height="200" fill="lightcoral" stroke="black" stroke-width="1"/>
</svg>

<br>

[[37,5%]]

## Aufgabe 2

In einer Schulklasse kommen $15$ von $24$ Schülern mit dem Fahrrad. **Berechne** den prozentualen Anteil.

[[62,5%]]
***********

$$ p=\dfrac{W}{G} =\dfrac{15}{24} = \dfrac{5}{8} = 62,5 \% $$

***********

## Aufgabe 3

Ein Kapital von $7500$€ wurde ein Jahr zu einem Jahreszins von $2\%$ angelegt. **Berechne** die resultierende Geldmenge.

[[6846]]
***********

$$ 7500\,\text{€} \cdot 1,02 = 7650\,\text{€} $$

***********

## Aufgabe 4

Die gesamte Downloaddauer beträgt $40\,$min. **Zeichne** in den Downloadbalken den dort beschriebenen Stand des Downloads **ein**.

<progress value="0" max="100" style="width: 33%; scale: 3; position: relative; left: calc(100% / 3); margin-bottom: 1rem">0%</progress>

[[70%]]
***********

<progress value="70" max="100" style="width: 33%; scale: 3; position: relative; left: calc(100% / 3)">70%</progress>

$$ 1- \dfrac{12\,\text{min}}{40\,\text{min}} = 70\% $$

***********

## Aufgabe 5

Bei Befragungen wurden jeweils insgesamt $44000$ Menschen interviewt. **Bestimme** die Anzahl der Menschen, die aus dem Kreisdiagramm die jeweiligen Antworten gaben.

<lia-chart option="{
  series: [{
    type: 'pie',
    radius: '50%',
    label: {
      show: true,
      formatter: '{b}: {c}%'
    },
    data: [
      { value: 25.0, name: 'a', itemStyle: { color: 'blue' } },
      { value: 33.3, name: 'b', itemStyle: { color: 'red' } },
      { value: 27.8, name: 'c', itemStyle: { color: 'green' } },
      { value: 13.9, name: 'd', itemStyle: { color: 'orange' } }
    ],
    emphasis: {
      itemStyle: {
        shadowBlur: 10,
        shadowOffsetX: 0,
        shadowColor: 'rgba(0, 0, 0, 0.5)'
      }
    }
  }]
}"></lia-chart>

> a: [[ 11000 ]] Menschen
>
> b: [[ 14652 ]] Menschen
>
> c: [[ 12232 ]] Menschen
>
> d: [[  6116 ]] Menschen
***********
$p_i  = \dfrac{W}{G} \quad \left| \cdot G \right. $

$G \cdot p_i  = W  $

$a: \;\; G \cdot p_a  =44000 \cdot 0,25 = 11000  $

$b: \;\; G \cdot p_b  =44000 \cdot 0,333 = 14652  $

$c: \;\; G \cdot p_c  =44000 \cdot 0,278 = 12232  $

$d: \;\; G \cdot p_d  =44000 \cdot 0,139 = 6116  $

***********

## Aufgabe 6

Ein gebrauchter PKW wurde für $12880$€ verkauft. Das waren $70\%$ des Neuwertes. **Berechne** den Neuwert des PKW in €.

[[18400]]
***********

$$ p = \dfrac{W}{G} \quad \left| \cdot G \right. $$

$$ G \cdot p  = W  \quad \left| : p \right. $$

$$ G  = \dfrac{W}{p} $$

$$ 12880\,\text{€} : \dfrac{70}{100} = 12880\,\text{€} \cdot \dfrac{100}{70} = 18400 \,\text{€} $$

***********

## Aufgabe 7

Es wurde eine Umgehungsstraße von $3500\,$ m Länge gebaut. $ 37 \% $ der Straße sind bereits fertiggestellt. **Berechne**, wie viel Meter noch gebaut werden müssen:

[[2205]]
***********

$$ 3500\,\text{m} \cdot (1-0,37) = 2205 \,\text{m} \qquad $$

***********

## Aufgabe 8

Nach einer Mieterhöhung von $4\%$ muss eine Familie jetzt $883,60$€ an Miete zahlen. **Berechne**, wie hoch die Miete vor der Erhöhung war.

[[849,615]]
*********** 

$$ 883,60\,\text{€} \cdot \dfrac{100}{104} = 849,615 \,\text{€} \qquad $$

***********

## Aufgabe 9

Eine Uhr wird mit einem Nettopreis von $109,24$€ beworben, sodass noch $19\%$ Steuern beim Kauf hinzu kommen. Da nach dem Kauf ein Mangel an der Uhr festgestellt wurde, gibt der Händler dem Kunden $10\%$ vom bezahlten Preis zurück. **Berechne**, wie viel Geld der Kunde für die Uhr ausgegeben hat.

[[116,996]]
***********

$$ 109,24\,\text{€} \cdot  1,19  = 129,996 \,\text{€} \qquad $$
$$ 129,996\,\text{€} \cdot  0,9  = 116,996 \,\text{€} \qquad $$ 

***********

## Aufgabe 10

Jedes Jahr bekommt ein Bankkunde $2\%$ Zinsen auf seine Ersparnisse. Hierbei wurden $4400$€ eingezahlt. **Berechne**, wie viel Geld sich nach drei Jahren auf dem Konto befinden.

[[4669,3152]]
***********

$$ 4400\,\text{€} \cdot 1,02 = 4488 \,\text{€} \qquad $$

$$ 4488\,\text{€} \cdot 1,02 = 4577,76 \,\text{€} \qquad $$

$$ 4577,76\,\text{€} \cdot 1,02 = 4669,3152 \,\text{€} \qquad$$

***********
