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

Auf den folgenden Seiten findest du ein klassisches Vokabeltraining in Tabellenform. Trage einfach die gesuchten deutschen oder französischen Wörter in die Felder ein. 


## Klassisches Vokabeltraining - Lektion 1

<!-- data-solution-button="25" data-show-partial-solution  data-randomize="true" -->
| Deutsch | Französisch |
|:------:|:-----------:|
| Hallo. | [[ Salut ]] |
| Hallo, Frau  | [[ Bonjour, madame ]] |
| Hallo, Herr  | [[ Bonjour, monsieur ]] |
| Guten Morgen. | [[ Bonjour. ]] |
| Guten Tag. | [[ Bonjour. ]] |
| Guten Abend. | [[ Bonsoir. ]] |
| Gute Nacht. | [[ Bonne nuit. ]] |
| Tschüs. | [[ Salut. ]] |
| [[ Auf Wiedersehen. ]] | Au revoir |
| Wie heißen Sie? | [[ Comment vous appelez-vous? ]] |
| Ich heiße  | [[ Je m'appelle ]] |
| Wie bitte? | [[ Comment? ]] |
| Wie schreibt man das? | [[ Comment ça s'écrit? ]] |
| Wie geht es Ihnen? | [[ Comment allez-vous? ]] |
| Danke, gut. | [[ bien, merci. ]] |
| Und Ihnen? | [[ Et vous? ]] |
| Auch gut. | [[ Bien aussi. ]] |
| Super. | [[ Super. ]] |
| Sehr gut. | [[ Très bien. ]] |
| [[ Gut. ]] | Bien. |
| Es geht. | [[ Ça va. ]] |
| Nicht so gut. | [[ Pas très bien. ]] |
| Wie spät ist es? | [[ Quelle heure est-il? ]] |
| Es ist halb acht. | [[ Il est sept heures et demi. ]] |
| Hören Sie. | [[ Écoutez. ]] |
| Lesen Sie. | [[ Lisez. ]] |
| Schreiben Sie. | [[ Écrivez. ]] |
| Sprechen Sie. | [[ Parlez. ]] |
| Sprechen Sie nach. | [[ Répétez. ]] |
| Buchstabieren Sie. | [[ Épelez. ]] |
| Zeichnen Sie. | [[ Dessinez. ]] |
| Fragen Sie. | [[ Posez des questions. ]] |
| Antworten Sie. | [[ Répondez. ]] |
| Diktieren Sie. | [[ Dictez. ]] |
| Ergänzen Sie. | [[ Complétez. ]] |
| Kreuzen Sie an. | [[ Cochez. ]] |
| Ordnen Sie zu. | [[ Associez. ]] |




## Klassisches Vokabeltraining - Lektion 2

<!-- data-solution-button="25" data-show-partial-solution  data-randomize="true" -->
| Deutsch        | Französisch      |
|:--------------:|:----------------:|
| mein           | [[ mon ]]        |
| der Vater    | [[ le père ]]  |
| der Bruder   | [[ le frère ]] |
| der Sohn     | [[ le fils ]]  |
| der Mann     | [[ le mari ]]  |
| meine          | [[ ma ]]         |
| die Mutter   | [[ la mère ]]  |
| die Schwester| [[ la sœur ]]  |
| die Tochter  | [[ la fille ]] |
| [[ die Frau ]] | la femme     |
| Wer ist das?                     | [[ Qui est-ce? ]]                  |
| [[ Das ist meine  ]]       | C’est ma                       |
| Wie heißt er?                | [[ Comment s’appelle-t-il? ]] |
| [[ Sie heißt ]]             | Elle s’appelle                  |
| Wie alt ist er?              | [[ Quel âge a-t-il? ]]        |
| [[ Sie ist 30 Jahre alt. ]]   | Elle a 30 ans.                   |
| Er ist            | [[ Il est  ]] |
| Sie ist           | [[ Elle est ]] |
| Ich bin           | [[ Je suis ]] |
| [[ ledig ]]                               | célibataire                          |
| [[ verheiratet ]]                         | marié                             |
| [[ geschieden ]]                          | divorcé                           |
| [[ verwitwet ]]                           | veuf                           |
| Ich habe         | [[ J’ai ]]        |
| Er hat          | [[ Il a ]]        |
| Sie hat          | [[ Elle a ]]        |
| [[ ein Kind ]]                            | un enfant                             |
| [[ zwei Kinder ]]                         | deux enfants                          |
| [[ Ich habe keine Kinder. ]]                        | Je n’ai pas d’enfants.                |







## Klassisches Vokabeltraining - Lektion 3

<!-- data-solution-button="25" data-show-partial-solution  data-randomize="true" -->
| Deutsch                      | Französisch                           |
|:---------------------------:|:--------------------------------------:|
| Woher kommen Sie?           | [[ Vous venez d’où? ]]                |
| Aus ...                       | [[ De ... ]]                              |
| Wo wohnen Sie?              | [[ Où habitez-vous? ]]                |
| In ...                        | [[ À ... ]]          |
| Wie ist Ihre Adresse?       | [[ Quelle est votre adresse? ]]       |
| die Straße               | [[ la rue ]]                        |
| Wie ist Ihre Telefonnummer? | [[ Quel est votre numéro de téléphone? ]] |
| Und Ihre Mobilnummer, bitte?| [[ Et votre numéro de portable, s’il vous plaît. ]] |
| Meine Telefonnummer ist ...   | [[ Mon numéro de téléphone est le... ]]  |
| Die Vorwahl ist ...           | [[ L’indicatif est... ]]                 |
| und dann ...                  | [[ Et ensuite... ]]                      |
| Vielen Dank.                | [[ Merci beaucoup! ]]                 |
| Ich weiß nicht.                | [[ Je ne sais pas. ]]               |
| Entschuldigung?                | [[ Pardon? ]]                       |
| Noch einmal langsam bitte.     | [[ Répétez, s’il vous plaît. ]]     |
| Kommen Sie aus ...?              | [[ Vous venez de...? ]]              |
| Ja.                    | [[ Oui. ]]                   |
| Nein.                    | [[ Non. ]]                   |
| Haben Sie Kinder?              | [[ Est-ce que vous avez des enfants? ]] |
| Ja, ich habe ...                 | [[ Oui, j’ai... ]]                    |
| Nein, ich habe ...               | [[ Non, je n’ai pas... ]]             |
| Sind Sie verheiratet?          | [[ Êtes-vous marié? ]]           |
| Kommt er  aus ...?          | [[ Il vient de ...? ]]     |
| Ist sie verheiratet?      | [[ Est-ce qu’elle est mariée? ]] |
| (der) Name        | [[ nom ]]                                 |
| (das) Land        | [[ pays ]]                                |
| (die) Hauptstadt  | [[ capitale ]]                            |
| (die) Adresse     | [[ adresse ]]                             |
| (das) Telefon     | [[ téléphone ]]                           |
| [[ die Telefonnummer ]] | numéro de téléphone  |
|  die Mobilnummer  | [[numéro de portable]] |
| [[ die Vorwahl ]]             | indicatif                            |




## Klassisches Vokabeltraining - Lektion 4

<!-- data-solution-button="25" data-show-partial-solution  data-randomize="true" -->
| Deutsch            | Französisch                 |
|:------------------:|:---------------------------:|
| Deutsch            | [[ l’allemand ]]            |
| Arabisch           | [[ l’arabe ]]               |
| Englisch           | [[ l’anglais ]]             |
| [[ Ich spreche ... ]]| Je parle ...                  |
| ein bisschen ...     | [[ un peu ]]                |
| Sprichst du ...?     | [[ Est-ce que tu parles ...? ]] |
| Was machst du im Deutschkurs?         | [[ Que fais-tu en cours d’allemand? ]] |
| lesen                                 | [[ lire ]]                            |
| hören                                 | [[ écouter ]]                         |
| singen                                | [[ chanter ]]                         |
| [[ Ich lerne Deutsch. ]]              | J’apprends l’allemand.                |
| zeichnen                              | [[ dessiner ]]                        |
| sprechen                              | [[ parler ]]                          |
| schreiben                             | [[ écrire ]]                          |
| Pause machen                          | [[ faire une pause ]]                 |
|  Teilnehmer   | [[ participant ]]|
|  Information  | [[ information ]]        |
|  Anmeldung    | [[ inscription ]]        |
|  Kursort      | [[ lieu du cours ]]      |
|  Deutschkurs  | [[ cours d’allemand ]]   |
|  Kurszeit     | [[ horaire du cours ]]   |
| [[  Beginn ]] | début du cours           |
| Wann ist der Kurs?              | [[ Quand est le cours? ]] |
| Er beginnt um 9 Uhr.            | [[ Il commence à 9 heures. ]] |
| Von 9 Uhr bis 11 Uhr.           | [[ De 9 à 11 heures. ]]    |
| [[ Er endet um 11 Uhr. ]]       | Il finit à 11 heures.      |
| Montag            | [[ lundi ]]                    |
| Dienstag          | [[ mardi ]]                    |
| Mittwoch          | [[ mercredi ]]                 |
| Donnerstag        | [[ jeudi ]]                    |
| Freitag           | [[ vendredi ]]                 |
| Samstag           | [[ samedi ]]                   |
| Sonntag           | [[ dimanche ]]                 |
|  Woche       | [[ semaine ]]                  |
|  Tag         | [[ jour ]]                     |
| Heute ist Montag. | [[ Nous sommes lundi aujourd’hui. ]] |
| [[ Am Montag. ]]  | Lundi.                         |





## Klassisches Vokabeltraining - Lektion 5

<!-- data-solution-button="25" data-show-partial-solution  data-randomize="true" -->
| Deutsch            | Französisch              |
|:------------------:|:------------------------:|
| Fahrrad fahren     | [[ faire du vélo ]]      |
| fernsehen          | [[ regarder la télé ]]   |
| Freunde besuchen   | [[ rendre visite à ses amis ]] |
| Fußball spielen    | [[ jouer au football ]]  |
| kochen             | [[ faire la cuisine ]]   |
| Musik hören        | [[ écouter de la musique ]] |
| schwimmen          | [[ faire de la natation ]] |
| spazieren gehen    | [[ se promener ]]        |
| [[ Ich lese gern. ]]      | J’aime lire.          |
| [[ Ich lese nicht gern. ]]| Je n’aime pas lire.   |
| Ich auch.               | [[ Moi aussi. ]]             |
| Ich nicht.              | [[ Pas moi. ]]               |
| Ja, stimmt.   | [[ Oui, c’est vrai.  ]] |
| Richtig.  | [[  Correct. ]] |
| Nein, das ist falsch.  | [[Non, c’est faux.]]              |
| heute        | [[ aujourd’hui ]] |
| morgen       | [[ demain ]]    |
| am Morgen    | [[ le matin ]]  |
| am Abend     | [[ le soir ]]   |
| [[ um zwei Uhr ]] | à deux heures |
| [[ im Januar ]]    | en janvier    |
| Januar   | [[ janvier ]]   |
| Februar  | [[ février ]]   |
| März     | [[ mars ]]      |
| April    | [[ avril ]]     |
| Mai      | [[ mai ]]       |
| Juni     | [[ juin ]]      |
| Juli     | [[ juillet ]]   |
| August   | [[ août ]]      |
| September| [[ septembre ]] |
| Oktober  | [[ octobre ]]   |
| November | [[ novembre ]]  |
| Dezember | [[ décembre ]]  |
| immer     | [[ toujours ]] |
| oft       | [[ souvent ]]  |
| manchmal  | [[ parfois ]]  |
| [[ nie ]] | jamais         |
| (das) Wetter         | [[ temps ]]        |
| gut                  | [[ beau ]]         |
| schlecht             | [[ mauvais ]]      |
| [[ Es regnet. ]]     | Il pleut.          |
| [[ Die Sonne scheint. ]] | Le soleil brille. |
| [[ Es ist warm.  ]] | Il fait chaud.  |
|  Es ist kalt.  | [[Il fait froid.]] |






## Klassisches Vokabeltraining - Lektion 6

<!-- data-solution-button="25" data-show-partial-solution  data-randomize="true" -->
| Deutsch            | Französisch                 |
|:------------------:|:---------------------------:|
| Ananas    | [[ ananas ]]       |
| Banane    | [[ banane ]]       |
| Brot      | [[ pain ]]         |
| Butter    | [[ beurre ]]       |
| Fleisch   | [[ viande ]]       |
| Gemüse    | [[ légumes ]]      |
| Kaffee    | [[ café ]]         |
| Käse      | [[ fromage ]]      |
| Kiwi      | [[ kiwi ]]         |
| Kuchen    | [[ gâteau ]]       |
| Milch     | [[ lait ]]         |
| Nektarine | [[ nectarine ]]    |
| Obst      | [[ fruits ]]       |
| Obstsalat | [[ salade de fruits ]] |
| Orange    | [[ orange ]]       |
| Reis      | [[ riz ]]          |
| Saft      | [[ jus (de fruit) ]] |
| Schokolade| [[ chocolat ]]     |
| Tee       | [[ thé ]]          |
| Wasser    | [[ eau ]]          |
| Wurst     | [[ saucisse  ]] |
| Zitronensaft | [[ jus de citron ]] |
| [[ Zucker ]] | sucre           |
| [[ Ich lese gern. ]]      | J’aime lire.                 |
|  zweimal | [[  deux ]]    |
| einmal  | [[ une  ]]    |
| [[ dreimal am Tag ]] | trois fois par jour |
| brauchen | [[ avoir besoin de ]] |
| nehmen   | [[ prendre ]]      |
| waschen  | [[ laver ]]        |
| schälen  | [[ éplucher ]]     |





## Klassisches Vokabeltraining - Lektion 7

<!-- data-solution-button="25" data-show-partial-solution  data-randomize="true" -->
| Deutsch            | Französisch                 |
|:------------------:|:---------------------------:|
| Entschuldigung.    | [[ Pardon. ]]               |
| [[ Ich brauche ... ]]| J’aurais besoin de...         |
| Wo ist ...?          | [[ Où est...? ]]             |
| Da vorne.          | [[ Là devant. ]]          |
| Da hinten.         | [[ Là derrière. ]]        |
| Danke.             | [[ Merci. ]]                |
| Bitte.             | [[ Je vous en prie, de rien. ]] |
| [[ Das weiß ich nicht. ]] | Je ne sais pas.      |
| [[ Tut mir leid. ]]| Désolé(e).                  |
| Was kostet ...?           | [[ Combien coûte...? ]]       |
| [[ Zwei Euro neunzig. ]]| Deux euros quatre-vingt-dix. |
| [[ Fünfzig Cent. ]]     | Cinquante centimes.          |
| das Kilo                | [[ le kilo ]]                |
| das Gramm               | [[ gramme ]]                 |
| das Stück               | [[ pièce ]]                  |
| Bitte sehr?        | [[ Vous désirez? ]]        |
| Haben Sie ...?       | [[ Est-ce que vous avez...? ]] |
| Sonst noch etwas?  | [[ Et avec ceci? ]]        |
| [[ Das ist alles. ]]| Ce sera tout.              |
| die Kasse             | [[ la caisse ]]         |
| die Pizza             | [[ la pizza ]]          |
| der Joghurt       | [[ le yaourt ]]         |
| das Rindfleisch       | [[ la viande de boeuf ]]|
| das Schweinefleisch   | [[ la viande de porc ]] |
| das Hackfleisch       | [[ la viande hachée ]]  |




## Klassisches Vokabeltraining - Lektion 8

<!-- data-solution-button="25" data-show-partial-solution  data-randomize="true" -->
| Deutsch            | Französisch              |
|:------------------:|:------------------------:|
| die Apotheke       | [[ la pharmacie ]]       |
| [[ der Bahnhof ]]  | la gare                  |
| die Bank           | [[ la banque ]]          |
| das Café           | [[ le café ]]            |
| [[ die Drogerie ]] | la droguerie             |
| der Kindergarten   | [[ le jardin d’enfants ]]|
| [[ der Kiosk ]]    | le kiosque               |
| das Krankenhaus    | [[ l’hôpital ]]          |
| [[ der Laden ]]    | le magasin               |
| der Parkplatz      | [[ le parking ]]         |
| [[ die Post ]]     | la poste                 |
| die Schule         | [[ l’école ]]            |
| Entschuldigung, eine Frage ...?         | [[ Est-ce que je pourrais vous demander...? ]] |
| [[ Ist hier ... in der Nähe? ]]         | Est-ce qu’il y a... près d’ici?              |
| Ist hier irgendwo ...?                 | [[ Est-ce qu’il y a... quelque part par ici? ]] |
| [[ Wo ist ...? ]]              | Où est...?           |
|  ist ganz in der Nähe.               | [[ ... est tout près d’ici. ]]                |
| Gehen Sie links. | [[ Allez à gauche. ]] |
| Gehen Sie rechts. | [[ Allez à à droite. ]] |
| Gehen Sie geradeaus. | [[ Allez à tout droit. ]] |
| [[ zuerst ]]                          | d’abord                                     |
| dann                                  | [[ ensuite ]]                                |
| [[ wieder ]]                          | encore                                      |
| Gehen Sie die Straße entlang.        | [[ Suivez la rue ]]                         |
| das Auto                                  | [[ la voiture ]]     |
| [[ der Bus ]]                             | le bus               |
| das Fahrrad                               | [[ le vélo ]]        |
| die S-Bahn                                | [[ le RER ]]         |
| [[ die Straßenbahn ]]                     | le tram              |
| die U-Bahn                                | [[ le métro ]]       |
| der Zug                                   | [[ le train ]]       |
| [[ Ich fahre mit der U-Bahn. ]] | Je vais en métro. |
| Ich fahre mit dem Auto.  | [[Je vais en voiture.]] |
| Ich gehe zu Fuß                           | [[ Je vais à pied. ]]|



## Klassisches Vokabeltraining - Lektion 9

<!-- data-solution-button="25" data-show-partial-solution  data-randomize="true" -->
| Deutsch                                   | Französisch                                  |
|:-----------------------------------------:|:--------------------------------------------:|
| der Altenpfleger     | [[ l’assistant pour personnes âgées ]]   |
| der Arbeiter             | [[ l’ouvrier ]]                 |
| der Arzt                     | [[ le médecin ]]          |
| der Friseur               | [[ le coiffeur ]]             |
| der Hausmann               | [[ l’homme au foyer ]]   |
| der Kellner              | [[ le serveur ]]               |
| der Koch                     | [[ le cuisinier ]]           |
| der Maler                   | [[ le peintre ]]                |
| die Reinigungskraft                       | [[ l’agent d’entretien ]]                    |
| der Schneider          | [[ le tailleur ]]            |
| der Taxifahrer         | [[ le chauffeur de taxi homme ]]     |
| der Verkäufer           | [[ le vendeur ]]               |
| [[ Ich bin  ]]              | Je suis                    |
|  die Altenpflegerin     | [[ l’assistante pour personnes âgées ]]   |
|  die Arbeiterin             | [[  l’ouvrière ]]                 |
|  die Ärztin                     | [[  la femme médecin ]]          |
|  die Friseurin               | [[ la coiffeuse ]]             |
|  die Hausfrau               | [[  la femme au foyer ]]   |
|  die Kellnerin               | [[  la serveuse ]]               |
|  die Köchin                     | [[  la cuisinière ]]           |
|  die Malerin                   | [[  la peintre ]]                |
|  die Schneiderin           | [[  la couturière ]]            |
|  die Taxifahrerin         | [[ le chauffeur de taxi femme ]]     |
|  die Verkäuferin           | [[  la vendeuse ]]               |
| Ich habe eine Ausbildung als ...            | [[ J’ai une formation de... ]]                 |
| Im Moment arbeite ich als ...               | [[ Actuellement, je travaille en tant que... ]]|
| [[ Ich gehe zur Schule. ]]                | Je suis élève / étudiant/e.                  |
| Ich möchte ... werden.                      | [[ J’aimerais devenir ... ]]                    |
| [[ Ich mache eine Ausbildung. ]]          | Je fais une formation.                       |
| Am Montag habe ich frei.                  | [[ J’ai libre le lundi. ]]                   |
| [[ Ich arbeite Schicht. ]]                | Je fais les trois-huit.                      |
| die Bluse          | [[ le chemisier ]] |
| das Hemd           | [[ la chemise ]]    |
| die Hose           | [[ le pantalon ]]   |
| die Jacke          | [[ la veste ]]      |
| das Kleid          | [[ la robe ]]       |
| der Rock           | [[ la jupe ]]       |
| das T-Shirt        | [[ le t-shirt ]]    |
| der Pullover       | [[ le pull ]]       |
| [[ schön ]] | beau/belle |
| [[ teuer ]]  | cher/chère |
| [[ hässlich ]] | laid/e |
| [[ günstig ]]  | bon marché |
| [[ am ersten Mai ]] | le 1er mai            |
| tagsüber          | [[ pendant la journée ]]|
| am Nachmittag     | [[ l’après-midi ]]      |
| in der Nacht      | [[ la nuit ]]           |




## Klassisches Vokabeltraining - Lektion 10

<!-- data-solution-button="25" data-show-partial-solution  data-randomize="true" -->
| Deutsch           | Französisch        |
|:-----------------:|:------------------:|
| der Kopf          | [[ la tête ]]      |
| das Ohr           | [[ l’oreille ]]    |
| das Auge          | [[ l’œil ]]        |
| der Mund          | [[ la bouche ]]    |
| der Hals          | [[ le cou ]]       |
| die Hand          | [[ la main ]]      |
| der Bauch         | [[ le ventre ]]    |
| der Rücken        | [[ le dos ]]       |
| das Bein          | [[ la jambe ]]     |
| der Fuß           | [[ le pied ]]      |
| Mein Hals tut weh.          | [[ J’ai mal au cou. ]]       |
| Meine Ohren tun weh.        | [[ J’ai mal aux oreilles. ]] |
| Ich bin gesund.     | [[ Je suis en bonne santé. ]] |
| Ich bin krank.     | [[ Je suis malade. ]] |
| Ich habe Fieber.            | [[ J’ai de la fièvre. ]]     |
| Ich habe Zahnschmerzen.     | [[ J’ai mal aux dents. ]]    |
| Ich habe Husten.            | [[ Je tousse. ]]             |
| Ich bin müde.               | [[ Je suis fatigué(e). ]]    |
| Ich bin erkältet.           | [[ J’ai pris froid. ]]       |
| Trinken Sie Tee.      | [[ Buvez une tisane. ]]              |
| Bleiben Sie zu Hause. | [[ Restez chez vous. ]]              |
| Gehen Sie zum Arzt.   | [[ Allez voir le docteur. ]]         |
| Schlafen Sie viel.    | [[ Vous avez besoin de beaucoup de sommeil. ]] |
| schwanger            | [[ enceinte ]]         |
| das Rezept           | [[ l’ordonnance ]]     |
| die Gesundheitskarte | [[ la caisse de maladie ]] |
| der Krankenschein    | [[ la fiche de maladie ]] |




# Vokabeln zuordnen 

Im Folgenden findest du Kacheln, die an die richtige Stelle gezogen werden müssen. Solltest du an einem Touchbildschirm arbeiten klicke auf das Feld und danach auf die passende Kachel.


## Vokabeln zuordnen - Lektion 1

Aufgabe 1: Ordne die Kacheln richtig zu.  

<!-- data-solution-button="25" data-show-partial-solution  data-randomize="true"-->
Hallo. [->[Salut]]. \
Hallo, Frau [->[Bonjour, madame]]. \
Hallo, Herr [->[Bonjour, monsieur]]. \
Guten Morgen. [->[Bonjour]]. \
Guten Tag. [->[Bonjour]]. \
Guten Abend. [->[Bonsoir]]. \
Gute Nacht. [->[Bonne nuit]]. \
Tschüs. [->[Salut]]. \
Auf Wiedersehen. [->[Au revoir]]. \
Wie heißen Sie? [->[Comment vous appelez-vous]]? \
Ich heiße [->[Je m'appelle]]. \
Wie bitte? [->[Comment]]? \
Wie schreibt man das? [->[Comment ça s'écrit]]? \
Wie geht es Ihnen? [->[Comment allez-vous]]? \
Danke, gut. [->[bien, merci]]. \
Und Ihnen? [->[Et vous]]? \
Auch gut. [->[Bien aussi]]. \
Super. [->[Super]]. \
Sehr gut. [->[Très bien]]. \
Gut. [->[Bien]]. \
Es geht. [->[Ça va]]. \
Nicht so gut. [->[Pas très bien]]. \
Wie spät ist es? [->[Quelle heure est-il]]? \
Es ist halb acht. [->[Il est sept heures et demi]]. \
Hören Sie. [->[Écoutez]]. \
Lesen Sie. [->[Lisez]]. \
Schreiben Sie. [->[Écrivez]]. \
Sprechen Sie. [->[Parlez]]. \
Sprechen Sie nach. [->[Répétez]]. \
Buchstabieren Sie. [->[Épelez]]. \
Zeichnen Sie. [->[Dessinez]]. \
Fragen Sie. [->[Posez des questions]]. \
Antworten Sie. [->[Répondez]]. \
Diktieren Sie. [->[Dictez]]. \
Ergänzen Sie. [->[Complétez]]. \
Kreuzen Sie an. [->[Cochez]]. \
Ordnen Sie zu. [->[Associez]]. \





## Vokabeln zuordnen - Lektion 2

Aufgabe 1: Ordne die Kacheln richtig zu.  


<!-- data-solution-button="25" data-show-partial-solution  data-randomize="true"-->
mein [->[mon]] \
meine [->[ma]] \
der Vater [->[le père]] \
die Mutter [->[la mère]] \
der Bruder [->[le frère]] \
die Schwester [->[la sœur]] \
der Sohn [->[le fils]] \
die Tochter [->[la fille]] \
der Mann [->[le mari]] \
die Frau [->[la femme]] \
Wer ist das? [->[Qui est-ce]]? \
Wie heißt er? [->[Comment s’appelle-t-il]]? \
Wie heißt sie? [->[Comment s’appelle-t-elle]]? \
Sie heißt [->[Elle s’appelle]] \
Er heißt [->[Il s’appelle]] \
Wie alt ist er? [->[Quel âge a-t-il]]? \
Wie alt ist sie? [->[Quel âge a-t-elle]]? \
Sie ist 30 Jahre alt. [->[Elle a 30 ans]] \
Er ist [->[Il est]] \
Sie ist [->[Elle est]] \
Ich bin [->[Je suis]] \
ledig [->[célibataire]] \
verheiratet [->[marié]] \
geschieden [->[divorcé]] \
verwitwet [->[veuf]] \
Ich habe [->[J’ai]] \
Er hat [->[Il a]] \
Sie hat [->[Elle a]] \
ein Kind [->[un enfant]] \
zwei Kinder [->[deux enfants]] \
Ich habe keine Kinder. [->[Je n’ai pas d’enfants]] \







## Vokabeln zuordnen - Lektion 3

Aufgabe 1: Ordne die Kacheln richtig zu.  

<!-- data-solution-button="25" data-show-partial-solution  data-randomize="true"-->
Woher kommen Sie? [->[Vous venez d’où]]? \
Aus ... [->[De ...]] \
Wo wohnen Sie? [->[Où habitez-vous]]? \
In ... [->[À ...]] \
Wie ist Ihre Adresse? [->[Quelle est votre adresse]]? \
die Straße [->[la rue]] \
Wie ist Ihre Telefonnummer? [->[Quel est votre numéro de téléphone]]? \
Und Ihre Mobilnummer, bitte? [->[Et votre numéro de portable, s’il vous plaît]]? \
Meine Telefonnummer ist ... [->[Mon numéro de téléphone est le...]] \
Die Vorwahl ist ... [->[L’indicatif est...]] \
und dann ... [->[Et ensuite...]] \
Vielen Dank. [->[Merci beaucoup]]. \
Ich weiß nicht. [->[Je ne sais pas]]. \
Entschuldigung? [->[Pardon]]? \
Noch einmal langsam bitte. [->[Répétez, s’il vous plaît]]. \
Kommen Sie aus ...? [->[Vous venez de ...]]? \
Ja. [->[Oui]]. \
Nein. [->[Non]]. \
Haben Sie Kinder? [->[Est-ce que vous avez des enfants]]? \
Ja, ich habe ... [->[Oui, j’ai...]] \
Nein, ich habe ... [->[Non, je n’ai pas...]] \
Sind Sie verheiratet? [->[Êtes-vous marié]]? \
Kommt er aus ...? [->[Il vient de ...]]? \
Ist sie verheiratet? [->[Est-ce qu’elle est mariée]]? \
der Name [->[nom]] \
das Land [->[pays]] \
die Hauptstadt [->[capitale]] \
die Adresse [->[adresse]] \
das Telefon [->[téléphone]] \
die Telefonnummer [->[numéro de téléphone]] \
die Mobilnummer [->[numéro de portable]] \
die Vorwahl [->[indicatif]] \




## Vokabeln zuordnen - Lektion 4

Aufgabe 1: Ordne die Kacheln richtig zu.  

<!-- data-solution-button="25" data-show-partial-solution  data-randomize="true"-->
Deutsch [->[l’allemand]] \
Arabisch [->[l’arabe]] \
Englisch [->[l’anglais]] \
Ich spreche ... [->[Je parle ...]] \
ein bisschen ... [->[un peu]] \
Sprichst du ...? [->[Est-ce que tu parles ...]]? \
Was machst du im Deutschkurs? [->[Que fais-tu en cours d’allemand]]? \
lesen [->[lire]] \
hören [->[écouter]] \
singen [->[chanter]] \
Ich lerne Deutsch. [->[J’apprends l’allemand]]. \
zeichnen [->[dessiner]] \
sprechen [->[parler]] \
schreiben [->[écrire]] \
Pause machen [->[faire une pause]] \
Teilnehmer [->[participant]] \
Information [->[information]] \
Anmeldung [->[inscription]] \
Kursort [->[lieu du cours]] \
Deutschkurs [->[cours d’allemand]] \
Kurszeit [->[horaire du cours]] \
Beginn [->[début du cours]] \
Wann ist der Kurs? [->[Quand est le cours]]? \
Er beginnt um 9 Uhr. [->[Il commence à 9 heures]]. \
Von 9 Uhr bis 11 Uhr. [->[De 9 à 11 heures]]. \
Er endet um 11 Uhr. [->[Il finit à 11 heures]]. \
Montag [->[lundi]] \
Dienstag [->[mardi]] \
Mittwoch [->[mercredi]] \
Donnerstag [->[jeudi]] \
Freitag [->[vendredi]] \
Samstag [->[samedi]] \
Sonntag [->[dimanche]] \
Woche [->[semaine]] \
Tag [->[jour]] \
Heute ist Montag. [->[Nous sommes lundi aujourd’hui]]. \
Am Montag. [->[Lundi]]. \







## Vokabeln zuordnen - Lektion 5

Aufgabe 1: Ordne die Kacheln richtig zu.  

<!-- data-solution-button="25" data-show-partial-solution  data-randomize="true"-->
Fahrrad fahren [->[faire du vélo]]. \
fernsehen [->[regarder la télé]]. \
Freunde besuchen [->[rendre visite à ses amis]]. \
Fußball spielen [->[jouer au football]]. \
kochen [->[faire la cuisine]]. \
Musik hören [->[écouter de la musique]]. \
schwimmen [->[faire de la natation]]. \
spazieren gehen [->[se promener]]. \
Ich lese gern. [->[J’aime lire]]. \
Ich lese nicht gern. [->[Je n’aime pas lire]]. \
Ich auch. [->[Moi aussi]]. \
Ich nicht. [->[Pas moi]]. \
Ja, stimmt. [->[Oui, c’est vrai]]. \
Richtig. [->[Correct]]. \
Nein, das ist falsch. [->[Non, c’est faux]]. \
heute [->[aujourd’hui]]. \
morgen [->[demain]]. \
am Morgen [->[le matin]]. \
am Abend [->[le soir]]. \
um zwei Uhr [->[à deux heures]]. \
im Januar [->[en janvier]]. \
Januar [->[janvier]]. \
Februar [->[février]]. \
März [->[mars]]. \
April [->[avril]]. \
Mai [->[mai]]. \
Juni [->[juin]]. \
Juli [->[juillet]]. \
August [->[août]]. \
September [->[septembre]]. \
Oktober [->[octobre]]. \
November [->[novembre]]. \
Dezember [->[décembre]]. \
immer [->[toujours]]. \
oft [->[souvent]]. \
manchmal [->[parfois]]. \
nie [->[jamais]]. \
Wetter [->[temps]]. \
gut [->[beau]]. \
schlecht [->[mauvais]]. \
Es regnet. [->[Il pleut]]. \
Die Sonne scheint. [->[Le soleil brille]]. \
Es ist warm. [->[Il fait chaud]]. \
Es ist kalt. [->[Il fait froid]]. \







## Vokabeln zuordnen - Lektion 6

Aufgabe 1: Ordne die Kacheln richtig zu.  

<!-- data-solution-button="25" data-show-partial-solution  data-randomize="true"-->
Ananas [->[ananas]] \
Banane [->[banane]] \
Brot [->[pain]] \
Butter [->[beurre]] \
Fleisch [->[viande]] \
Gemüse [->[légumes]] \
Kaffee [->[café]] \
Käse [->[fromage]] \
Kiwi [->[kiwi]] \
Kuchen [->[gâteau]] \
Milch [->[lait]] \
Nektarine [->[nectarine]] \
Obst [->[fruits]] \
Obstsalat [->[salade de fruits]] \
Orange [->[orange]] \
Reis [->[riz]] \
Saft [->[jus (de fruit)]] \
Schokolade [->[chocolat]] \
Tee [->[thé]] \
Wasser [->[eau]] \
Wurst [->[saucisse]] \
Zitronensaft [->[jus de citron]] \
Zucker [->[sucre]] \
einmal [->[une]] \
zweimal [->[deux]] \
dreimal am Tag [->[trois fois par jour]] \
brauchen [->[avoir besoin de]] \
nehmen [->[prendre]] \
waschen [->[laver]] \
schälen [->[éplucher]] \







## Vokabeln zuordnen - Lektion 7

Aufgabe 1: Ordne die Kacheln richtig zu.  

<!-- data-solution-button="25" data-show-partial-solution  data-randomize="true"-->
Entschuldigung [->[Pardon]]. \
Ich brauche ... [->[J’aurais besoin de...]]. \
Wo ist ... [->[Où est...]]? \
Da vorne [->[Là devant]]. \
Da hinten [->[Là derrière]]. \
Danke [->[Merci]]. \
Bitte [->[Je vous en prie, de rien]]. \
Das weiß ich nicht [->[Je ne sais pas]]. \
Tut mir leid [->[Désolé(e)]]. \
Was kostet ... [->[Combien coûte...]]? \
Zwei Euro neunzig [->[Deux euros quatre-vingt-dix]]. \
Fünfzig Cent [->[Cinquante centimes]]. \
das Kilo [->[le kilo]]. \
das Gramm [->[gramme]]. \
das Stück [->[pièce]]. \
Bitte sehr [->[Vous désirez]]? \
Haben Sie ... [->[Est-ce que vous avez...]]? \
Sonst noch etwas [->[Et avec ceci]]? \
Das ist alles [->[Ce sera tout]]. \
die Kasse [->[la caisse]]. \
die Pizza [->[la pizza]]. \
der Joghurt [->[le yaourt]]. \
das Rindfleisch [->[la viande de boeuf]]. \
das Schweinefleisch [->[la viande de porc]]. \
das Hackfleisch [->[la viande hachée]]. \







## Vokabeln zuordnen - Lektion 8

Aufgabe 1: Ordne die Kacheln richtig zu.  

<!-- data-solution-button="25" data-show-partial-solution  data-randomize="true"-->
die Apotheke [->[la pharmacie]]. \
der Bahnhof [->[la gare]]. \
die Bank [->[la banque]]. \
das Café [->[le café]]. \
die Drogerie [->[la droguerie]]. \
der Kindergarten [->[le jardin d’enfants]]. \
der Kiosk [->[le kiosque]]. \
das Krankenhaus [->[l’hôpital]]. \
der Laden [->[le magasin]]. \
der Parkplatz [->[le parking]]. \
die Post [->[la poste]]. \
die Schule [->[l’école]]. \
Entschuldigung, eine Frage [->[Est-ce que je pourrais vous demander]]. \
Ist hier ... in der Nähe [->[Est-ce qu’il y a ... près d’ici]]? \
Ist hier irgendwo ... [->[Est-ce qu’il y a ... quelque part par ici]]? \
Wo ist ... [->[Où est ...]]? \
... ist ganz in der Nähe [->[... est tout près d’ici]]. \
Gehen Sie links [->[Allez à gauche]]. \
Gehen Sie rechts [->[Allez à droite]]. \
Gehen Sie geradeaus [->[Allez tout droit]]. \
zuerst [->[d’abord]]. \
dann [->[ensuite]]. \
wieder [->[encore]]. \
Gehen Sie die Straße entlang [->[Suivez la rue]]. \
das Auto [->[la voiture]]. \
der Bus [->[le bus]]. \
das Fahrrad [->[le vélo]]. \
die S-Bahn [->[le RER]]. \
die Straßenbahn [->[le tram]]. \
die U-Bahn [->[le métro]]. \
der Zug [->[le train]]. \
Ich fahre mit der U-Bahn [->[Je vais en métro]]. \
Ich fahre mit dem Auto [->[Je vais en voiture]]. \
Ich gehe zu Fuß [->[Je vais à pied]]. \



## Vokabeln zuordnen - Lektion 9

Aufgabe 1: Ordne die Kacheln richtig zu.  

<!-- data-solution-button="25" data-show-partial-solution  data-randomize="true"-->
der Altenpfleger [->[l’assistant pour personnes âgées]] \
die Altenpflegerin [->[l’assistante pour personnes âgées]] \
der Arbeiter [->[l’ouvrier]] \
die Arbeiterin [->[l’ouvrière]] \
der Arzt [->[le médecin]] \
die Ärztin [->[la femme médecin]] \
der Friseur [->[le coiffeur]] \
die Friseurin [->[la coiffeuse]] \
der Hausmann [->[l’homme au foyer]] \
die Hausfrau [->[la femme au foyer]] \
der Kellner [->[le serveur]] \
die Kellnerin [->[la serveuse]] \
der Koch [->[le cuisinier]] \
die Köchin [->[la cuisinière]] \
der Maler [->[le peintre]] \
die Malerin [->[la peintre]] \
die Reinigungskraft [->[l’agent d’entretien]] \
der Schneider [->[le tailleur]] \
die Schneiderin [->[la couturière]] \
der Taxifahrer [->[le chauffeur de taxi]] \
die Taxifahrerin [->[la chauffeuse de taxi]] \
der Verkäufer [->[le vendeur]] \
die Verkäuferin [->[la vendeuse]] \
Ich bin [->[Je suis]]. \
Ich habe eine Ausbildung als ... [->[J’ai une formation de...]]. \
Im Moment arbeite ich als ... [->[Actuellement, je travaille en tant que...]]. \
Ich gehe zur Schule. [->[Je suis élève / étudiant(e)]]. \
Ich möchte ... werden. [->[J’aimerais devenir...]]. \
Ich mache eine Ausbildung. [->[Je fais une formation]]. \
Am Montag habe ich frei. [->[J’ai libre le lundi]]. \
Ich arbeite Schicht. [->[Je fais les trois-huit]]. \
die Bluse [->[le chemisier]] \
das Hemd [->[la chemise]] \
die Hose [->[le pantalon]] \
die Jacke [->[la veste]] \
das Kleid [->[la robe]] \
der Rock [->[la jupe]] \
das T-Shirt [->[le t-shirt]] \
der Pullover [->[le pull]] \
schön [->[beau/belle]] \
hässlich [->[laid/e]] \
teuer [->[cher/chère]] \
günstig [->[bon marché]] \
am ersten Mai [->[le 1er mai]] \
tagsüber [->[pendant la journée]] \
am Nachmittag [->[l’après-midi]] \
in der Nacht [->[la nuit]] \



## Vokabeln zuordnen - Lektion 10

Aufgabe 1: Ordne die Kacheln richtig zu.  

<!-- data-solution-button="25" data-show-partial-solution  data-randomize="true"-->
der Kopf [->[la tête]]. \
das Ohr [->[l’oreille]]. \
das Auge [->[l’œil]]. \
der Mund [->[la bouche]]. \
der Hals [->[le cou]]. \
die Hand [->[la main]]. \
der Bauch [->[le ventre]]. \
der Rücken [->[le dos]]. \
das Bein [->[la jambe]]. \
der Fuß [->[le pied]]. \
Mein Hals tut weh. [->[J’ai mal au cou]]. \
Meine Ohren tun weh. [->[J’ai mal aux oreilles]]. \
Ich bin gesund. [->[Je suis en bonne santé]]. \
Ich bin krank. [->[Je suis malade]]. \
Ich habe Fieber. [->[J’ai de la fièvre]]. \
Ich habe Zahnschmerzen. [->[J’ai mal aux dents]]. \
Ich habe Husten. [->[Je tousse]]. \
Ich bin müde. [->[Je suis fatigué(e)]]. \
Ich bin erkältet. [->[J’ai pris froid]]. \
Trinken Sie Tee. [->[Buvez une tisane]]. \
Bleiben Sie zu Hause. [->[Restez chez vous]]. \
Gehen Sie zum Arzt. [->[Allez voir le docteur]]. \
Schlafen Sie viel. [->[Vous avez besoin de beaucoup de sommeil]]. \
schwanger [->[enceinte]]. \
das Rezept [->[l’ordonnance]]. \
die Gesundheitskarte [->[la caisse de maladie]]. \
der Krankenschein [->[la fiche de maladie]]. \




# Aussprachetraining

Nun kannst du auch noch deine Ausprache üben, indem du auf den Button klickst und dann die Vokabel richtig aussprichst.


## Aussprachetraining - Lektion 1

@SpeechRecognition.support



<section class="flex-container">

<!-- Grüße -->
<div class="flex-child">
Sprich 'Hallo' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Salut`)
</div>

<div class="flex-child">
Sprich 'Hallo, Frau' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Bonjour, madame`)
</div>

<div class="flex-child">
Sprich 'Hallo, Herr' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Bonjour, monsieur`)
</div>

<div class="flex-child">
Sprich 'Guten Morgen' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Bonjour`)
</div>

<div class="flex-child">
Sprich 'Guten Tag' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Bonjour`)
</div>

<div class="flex-child">
Sprich 'Guten Abend' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Bonsoir`)
</div>

<div class="flex-child">
Sprich 'Gute Nacht' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Bonne nuit`)
</div>

<div class="flex-child">
Sprich 'Tschüs' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Salut`)
</div>

<div class="flex-child">
Sprich 'Auf Wiedersehen' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Au revoir`)
</div>

<!-- Sich vorstellen / Nachfragen -->
<div class="flex-child">
Sprich 'Wie heißen Sie?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Comment vous appelez-vous?`)
</div>

<div class="flex-child">
Sprich 'Ich heiße' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Je m'appelle`)
</div>

<div class="flex-child">
Sprich 'Wie bitte?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Comment?`)
</div>

<div class="flex-child">
Sprich 'Wie schreibt man das?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Comment ça s'écrit?`)
</div>

<div class="flex-child">
Sprich 'Wie geht es Ihnen?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Comment allez-vous?`)
</div>

<!-- Befinden -->
<div class="flex-child">
Sprich 'Danke, gut' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`bien, merci.`)
</div>

<div class="flex-child">
Sprich 'Und Ihnen?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Et vous?`)
</div>

<div class="flex-child">
Sprich 'Auch gut' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Bien aussi`)
</div>

<div class="flex-child">
Sprich 'Super' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Super`)
</div>

<div class="flex-child">
Sprich 'Sehr gut' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Très bien`)
</div>

<div class="flex-child">
Sprich 'Gut' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Bien`)
</div>

<div class="flex-child">
Sprich 'Es geht' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Ça va`)
</div>

<div class="flex-child">
Sprich 'Nicht so gut' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Pas très bien`)
</div>

<!-- Uhrzeit -->
<div class="flex-child">
Sprich 'Wie spät ist es?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Quelle heure est-il?`)
</div>

<div class="flex-child">
Sprich 'Es ist halb acht' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Il est sept heures et demi`)
</div>

<!-- Klassenraum-Kommandos -->
<div class="flex-child">
Sprich 'Hören Sie' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Écoutez`)
</div>

<div class="flex-child">
Sprich 'Lesen Sie' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Lisez`)
</div>

<div class="flex-child">
Sprich 'Schreiben Sie' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Écrivez`)
</div>

<div class="flex-child">
Sprich 'Sprechen Sie' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Parlez`)
</div>

<div class="flex-child">
Sprich 'Sprechen Sie nach' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Répétez`)
</div>

<div class="flex-child">
Sprich 'Buchstabieren Sie' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Épelez`)
</div>

<div class="flex-child">
Sprich 'Zeichnen Sie' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Dessinez`)
</div>

<div class="flex-child">
Sprich 'Fragen Sie' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Posez des questions`)
</div>

<div class="flex-child">
Sprich 'Antworten Sie' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Répondez`)
</div>

<div class="flex-child">
Sprich 'Diktieren Sie' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Dictez`)
</div>

<div class="flex-child">
Sprich 'Ergänzen Sie' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Complétez`)
</div>

<div class="flex-child">
Sprich 'Kreuzen Sie an' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Cochez`)
</div>

<div class="flex-child">
Sprich 'Ordnen Sie zu' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Associez`)
</div>

</section>








## Aussprachetraining - Lektion 2

@SpeechRecognition.support


<section class="flex-container">

<!-- Possessiv & Familie -->
<div class="flex-child">
Sprich 'mein' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`mon`)
</div>

<div class="flex-child">
Sprich 'meine' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`ma`)
</div>

<div class="flex-child">
Sprich 'der Vater' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le père`)
</div>

<div class="flex-child">
Sprich 'die Mutter' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la mère`)
</div>

<div class="flex-child">
Sprich 'der Bruder' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le frère`)
</div>

<div class="flex-child">
Sprich 'die Schwester' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la sœur`)
</div>

<div class="flex-child">
Sprich 'der Sohn' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le fils`)
</div>

<div class="flex-child">
Sprich 'die Tochter' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la fille`)
</div>

<div class="flex-child">
Sprich 'der Mann (Ehemann)' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le mari`)
</div>

<div class="flex-child">
Sprich 'die Frau (Ehefrau)' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la femme`)
</div>

<!-- Fragen zur Familie -->
<div class="flex-child">
Sprich 'Wer ist das?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Qui est-ce?`)
</div>

<div class="flex-child">
Sprich 'Wie heißt er?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Comment s'appelle-t-il?`)
</div>

<div class="flex-child">
Sprich 'Wie heißt sie?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Comment s'appelle-t-elle?`)
</div>

<div class="flex-child">
Sprich 'Er heißt …' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Il s'appelle …`)
</div>

<div class="flex-child">
Sprich 'Sie heißt …' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Elle s'appelle …`)
</div>

<div class="flex-child">
Sprich 'Wie alt ist er?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Quel âge a-t-il?`)
</div>

<div class="flex-child">
Sprich 'Wie alt ist sie?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Quel âge a-t-elle?`)
</div>

<div class="flex-child">
Sprich 'Sie ist 30 Jahre alt.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Elle a 30 ans.`)
</div>

<!-- Sein / Status -->
<div class="flex-child">
Sprich 'Er ist …' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Il est …`)
</div>

<div class="flex-child">
Sprich 'Sie ist …' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Elle est …`)
</div>

<div class="flex-child">
Sprich 'Ich bin …' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Je suis …`)
</div>

<div class="flex-child">
Sprich 'ledig' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`célibataire`)
</div>

<div class="flex-child">
Sprich 'verheiratet' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`marié`)
</div>

<div class="flex-child">
Sprich 'geschieden' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`divorcé`)
</div>

<div class="flex-child">
Sprich 'verwitwet' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`veuf`)
</div>

<!-- Haben / Kinder -->
<div class="flex-child">
Sprich 'Ich habe …' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`J'ai …`)
</div>

<div class="flex-child">
Sprich 'Er hat …' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Il a`)
</div>

<div class="flex-child">
Sprich 'Sie hat …' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Elle a …`)
</div>

<div class="flex-child">
Sprich 'ein Kind' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`un enfant`)
</div>

<div class="flex-child">
Sprich 'zwei Kinder' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`deux enfants`)
</div>

<div class="flex-child">
Sprich 'Ich habe keine Kinder.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Je n'ai pas d'enfants.`)
</div>

</section>




## Aussprachetraining - Lektion 3

@SpeechRecognition.support


<section class="flex-container">

<!-- Fragen zur Herkunft und Adresse -->
<div class="flex-child">
Sprich 'Woher kommen Sie?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Vous venez d’où?`)
</div>

<div class="flex-child">
Sprich 'Aus …' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`De …`)
</div>

<div class="flex-child">
Sprich 'Wo wohnen Sie?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Où habitez-vous?`)
</div>

<div class="flex-child">
Sprich 'In …' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`À …`)
</div>

<div class="flex-child">
Sprich 'Wie ist Ihre Adresse?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Quelle est votre adresse?`)
</div>

<div class="flex-child">
Sprich 'die Straße' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la rue`)
</div>

<div class="flex-child">
Sprich 'Wie ist Ihre Telefonnummer?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Quel est votre numéro de téléphone?`)
</div>

<div class="flex-child">
Sprich 'Und Ihre Mobilnummer, bitte?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Et votre numéro de portable, s’il vous plaît?`)
</div>

<div class="flex-child">
Sprich 'Meine Telefonnummer ist …' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Mon numéro de téléphone est le …`)
</div>

<div class="flex-child">
Sprich 'Die Vorwahl ist …' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`L’indicatif est …`)
</div>

<div class="flex-child">
Sprich 'und dann …' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Et ensuite …`)
</div>

<div class="flex-child">
Sprich 'Vielen Dank' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Merci beaucoup!`)
</div>

<!-- Rückfragen / Verständnis -->
<div class="flex-child">
Sprich 'Ich weiß nicht' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Je ne sais pas.`)
</div>

<div class="flex-child">
Sprich 'Entschuldigung?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Pardon?`)
</div>

<div class="flex-child">
Sprich 'Noch einmal langsam, bitte' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Répétez, s’il vous plaît.`)
</div>

<!-- Ja/Nein-Fragen zur Person -->
<div class="flex-child">
Sprich 'Kommen Sie aus …?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Vous venez de …?`)
</div>

<div class="flex-child">
Sprich 'Ja' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Oui`)
</div>

<div class="flex-child">
Sprich 'Nein' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Non`)
</div>

<div class="flex-child">
Sprich 'Haben Sie Kinder?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Est-ce que vous avez des enfants?`)
</div>

<div class="flex-child">
Sprich 'Ja, ich habe …' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Oui, j’ai …`)
</div>

<div class="flex-child">
Sprich 'Nein, ich habe …' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Non, je n’ai pas …`)
</div>

<div class="flex-child">
Sprich 'Sind Sie verheiratet?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Êtes-vous marié?`)
</div>

<div class="flex-child">
Sprich 'Kommt er aus …?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Il vient de …?`)
</div>

<div class="flex-child">
Sprich 'Ist sie verheiratet?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Est-ce qu’elle est mariée?`)
</div>

<!-- Formularfelder -->
<div class="flex-child">
Sprich 'der Name' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`nom`)
</div>

<div class="flex-child">
Sprich 'das Land' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`pays`)
</div>

<div class="flex-child">
Sprich 'die Hauptstadt' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`capitale`)
</div>

<div class="flex-child">
Sprich 'die Adresse' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`adresse`)
</div>

<div class="flex-child">
Sprich 'das Telefon' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`téléphone`)
</div>

<div class="flex-child">
Sprich 'die Telefonnummer' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`numéro de téléphone`)
</div>

<div class="flex-child">
Sprich 'die Mobilnummer' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`numéro de portable`)
</div>

<div class="flex-child">
Sprich 'die Vorwahl' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`indicatif`)
</div>

</section>




## Aussprachetraining - Lektion 4

@SpeechRecognition.support


<section class="flex-container">

<!-- Sprachen -->
<div class="flex-child">
Sprich 'Deutsch' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`l’allemand`)
</div>

<div class="flex-child">
Sprich 'Arabisch' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`l’arabe`)
</div>

<div class="flex-child">
Sprich 'Englisch' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`l’anglais`)
</div>

<div class="flex-child">
Sprich 'Ich spreche ...' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Je parle ...`)
</div>

<div class="flex-child">
Sprich 'ein bisschen ...' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`un peu`)
</div>

<div class="flex-child">
Sprich 'Sprichst du ...?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Est-ce que tu parles ... ?`)
</div>

<!-- Im Deutschkurs: Tätigkeiten -->
<div class="flex-child">
Sprich 'Was machst du im Deutschkurs?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Que fais-tu en cours d’allemand ?`)
</div>

<div class="flex-child">
Sprich 'lesen' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`lire`)
</div>

<div class="flex-child">
Sprich 'hören' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`écouter`)
</div>

<div class="flex-child">
Sprich 'singen' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`chanter`)
</div>

<div class="flex-child">
Sprich 'Ich lerne Deutsch.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`J’apprends l’allemand.`)
</div>

<div class="flex-child">
Sprich 'zeichnen' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`dessiner`)
</div>

<div class="flex-child">
Sprich 'sprechen' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`parler`)
</div>

<div class="flex-child">
Sprich 'schreiben' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`écrire`)
</div>

<div class="flex-child">
Sprich 'Pause machen' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`faire une pause`)
</div>

<!-- Kurs-Informationen -->
<div class="flex-child">
Sprich 'Teilnehmer' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`participant`)
</div>

<div class="flex-child">
Sprich 'Information' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`information`)
</div>

<div class="flex-child">
Sprich 'Anmeldung' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`inscription`)
</div>

<div class="flex-child">
Sprich 'Kursort' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`lieu du cours`)
</div>

<div class="flex-child">
Sprich 'Deutschkurs' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`cours d’allemand`)
</div>

<div class="flex-child">
Sprich 'Kurszeit' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`horaire du cours`)
</div>

<div class="flex-child">
Sprich 'Beginn' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`début du cours`)
</div>

<!-- Zeiten / Uhr -->
<div class="flex-child">
Sprich 'Wann ist der Kurs?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Quand est le cours ?`)
</div>

<div class="flex-child">
Sprich 'Er beginnt um 9 Uhr.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Il commence à 9 heures.`)
</div>

<div class="flex-child">
Sprich 'Von 9 Uhr bis 11 Uhr.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`De 9 à 11 heures.`)
</div>

<div class="flex-child">
Sprich 'Er endet um 11 Uhr.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Il finit à 11 heures.`)
</div>

<!-- Woche & Tage -->
<div class="flex-child">
Sprich 'Montag' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`lundi`)
</div>

<div class="flex-child">
Sprich 'Dienstag' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`mardi`)
</div>

<div class="flex-child">
Sprich 'Mittwoch' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`mercredi`)
</div>

<div class="flex-child">
Sprich 'Donnerstag' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`jeudi`)
</div>

<div class="flex-child">
Sprich 'Freitag' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`vendredi`)
</div>

<div class="flex-child">
Sprich 'Samstag' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`samedi`)
</div>

<div class="flex-child">
Sprich 'Sonntag' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`dimanche`)
</div>

<div class="flex-child">
Sprich 'Woche' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`semaine`)
</div>

<div class="flex-child">
Sprich 'Tag' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`jour`)
</div>

<div class="flex-child">
Sprich 'Heute ist Montag.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Nous sommes lundi aujourd’hui.`)
</div>

<div class="flex-child">
Sprich 'Am Montag.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Lundi.`)
</div>

</section>





## Aussprachetraining - Lektion 5

@SpeechRecognition.support

<section class="flex-container">

<!-- Aktivitäten -->
<div class="flex-child">
Sprich 'Fahrrad fahren' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`faire du vélo`)
</div>

<div class="flex-child">
Sprich 'fernsehen' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`regarder la télé`)
</div>

<div class="flex-child">
Sprich 'Freunde besuchen' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`rendre visite à ses amis`)
</div>

<div class="flex-child">
Sprich 'Fußball spielen' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`jouer au football`)
</div>

<div class="flex-child">
Sprich 'kochen' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`faire la cuisine`)
</div>

<div class="flex-child">
Sprich 'Musik hören' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`écouter de la musique`)
</div>

<div class="flex-child">
Sprich 'schwimmen' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`faire de la natation`)
</div>

<div class="flex-child">
Sprich 'spazieren gehen' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`se promener`)
</div>

<div class="flex-child">
Sprich 'Ich lese gern.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`J’aime lire.`)
</div>

<div class="flex-child">
Sprich 'Ich lese nicht gern.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Je n’aime pas lire.`)
</div>

<!-- Zustimmung / Ablehnung -->
<div class="flex-child">
Sprich 'Ich auch.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Moi aussi.`)
</div>

<div class="flex-child">
Sprich 'Ich nicht.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Pas moi.`)
</div>

<div class="flex-child">
Sprich 'Ja, stimmt.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Oui, c’est vrai.`)
</div>

<div class="flex-child">
Sprich 'Richtig.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Correct.`)
</div>

<div class="flex-child">
Sprich 'Nein, das ist falsch.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Non, c’est faux.`)
</div>

<!-- Zeiten -->
<div class="flex-child">
Sprich 'heute' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`aujourd’hui`)
</div>

<div class="flex-child">
Sprich 'morgen' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`demain`)
</div>

<div class="flex-child">
Sprich 'am Morgen' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le matin`)
</div>

<div class="flex-child">
Sprich 'am Abend' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le soir`)
</div>

<div class="flex-child">
Sprich 'um zwei Uhr' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`à deux heures`)
</div>

<div class="flex-child">
Sprich 'im Januar' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`en janvier`)
</div>

<!-- Monate -->
<div class="flex-child">
Sprich 'Januar' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`janvier`)
</div>

<div class="flex-child">
Sprich 'Februar' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`février`)
</div>

<div class="flex-child">
Sprich 'März' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`mars`)
</div>

<div class="flex-child">
Sprich 'April' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`avril`)
</div>

<div class="flex-child">
Sprich 'Mai' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`mai`)
</div>

<div class="flex-child">
Sprich 'Juni' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`juin`)
</div>

<div class="flex-child">
Sprich 'Juli' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`juillet`)
</div>

<div class="flex-child">
Sprich 'August' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`août`)
</div>

<div class="flex-child">
Sprich 'September' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`septembre`)
</div>

<div class="flex-child">
Sprich 'Oktober' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`octobre`)
</div>

<div class="flex-child">
Sprich 'November' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`novembre`)
</div>

<div class="flex-child">
Sprich 'Dezember' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`décembre`)
</div>

<!-- Häufigkeit -->
<div class="flex-child">
Sprich 'immer' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`toujours`)
</div>

<div class="flex-child">
Sprich 'oft' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`souvent`)
</div>

<div class="flex-child">
Sprich 'manchmal' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`parfois`)
</div>

<div class="flex-child">
Sprich 'nie' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`jamais`)
</div>

<!-- Wetter -->
<div class="flex-child">
Sprich 'Wetter' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`temps`)
</div>

<div class="flex-child">
Sprich 'gut' bzgl. Wetter auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`beau`)
</div>

<div class="flex-child">
Sprich 'schlecht' bzgl. Wetter auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`mauvais`)
</div>

<div class="flex-child">
Sprich 'Es regnet.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Il pleut.`)
</div>

<div class="flex-child">
Sprich 'Die Sonne scheint.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Le soleil brille.`)
</div>

<div class="flex-child">
Sprich 'Es ist warm.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Il fait chaud.`)
</div>

<div class="flex-child">
Sprich 'Es ist kalt.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Il fait froid.`)
</div>

</section>









## Aussprachetraining - Lektion 6

@SpeechRecognition.support


<section class="flex-container">

<!-- Essen & Trinken – Nomen -->
<div class="flex-child">
Sprich 'Ananas' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`ananas`)
</div>

<div class="flex-child">
Sprich 'Banane' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`banane`)
</div>

<div class="flex-child">
Sprich 'Brot' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`pain`)
</div>

<div class="flex-child">
Sprich 'Butter' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`beurre`)
</div>

<div class="flex-child">
Sprich 'Fleisch' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`viande`)
</div>

<div class="flex-child">
Sprich 'Gemüse' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`légumes`)
</div>

<div class="flex-child">
Sprich 'Käse' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`fromage`)
</div>

<div class="flex-child">
Sprich 'Kiwi' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`kiwi`)
</div>

<div class="flex-child">
Sprich 'Kuchen' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`gâteau`)
</div>

<div class="flex-child">
Sprich 'Milch' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`lait`)
</div>

<div class="flex-child">
Sprich 'Nektarine' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`nectarine`)
</div>

<div class="flex-child">
Sprich 'Obst' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`fruits`)
</div>

<div class="flex-child">
Sprich 'Obstsalat' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`salade de fruits`)
</div>

<div class="flex-child">
Sprich 'Orange' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`orange`)
</div>

<div class="flex-child">
Sprich 'Reis' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`riz`)
</div>

<div class="flex-child">
Sprich 'Schokolade' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`chocolat`)
</div>

<div class="flex-child">
Sprich 'Wurst' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`saucisse`)
</div>

<div class="flex-child">
Sprich 'Zitronensaft' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`jus de citron`)
</div>

<div class="flex-child">
Sprich 'Zucker' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`sucre`)
</div>

<!-- Getränke -->
<div class="flex-child">
Sprich 'Kaffee' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`café`)
</div>

<div class="flex-child">
Sprich 'Saft' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`jus`)
</div>

<div class="flex-child">
Sprich 'Tee' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`thé`)
</div>

<div class="flex-child">
Sprich 'Wasser' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`eau`)
</div>

<!-- Häufigkeit -->
<div class="flex-child">
Sprich 'einmal' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`une`)
</div>

<div class="flex-child">
Sprich 'zweimal' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`deux`)
</div>

<div class="flex-child">
Sprich 'dreimal am Tag' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`trois fois par jour`)
</div>

<!-- Verben -->
<div class="flex-child">
Sprich 'brauchen' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`avoir besoin de`)
</div>

<div class="flex-child">
Sprich 'nehmen' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`prendre`)
</div>

<div class="flex-child">
Sprich 'waschen' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`laver`)
</div>

<div class="flex-child">
Sprich 'schälen' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`éplucher`)
</div>

</section>




## Aussprachetraining - Lektion 7

@SpeechRecognition.support

<section class="flex-container">

<!-- Um Hilfe bitten -->
<div class="flex-child">
Sprich 'Entschuldigung' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Pardon.`)
</div>

<div class="flex-child">
Sprich 'Ich brauche ...' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`J’aurais besoin de...`)
</div>

<div class="flex-child">
Sprich 'Wo ist ...?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Où est ... ?`)
</div>

<div class="flex-child">
Sprich 'Da vorne' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Là devant.`)
</div>

<div class="flex-child">
Sprich 'Da hinten' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Là derrière.`)
</div>

<div class="flex-child">
Sprich 'Danke' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Merci.`)
</div>

<div class="flex-child">
Sprich 'Bitte' (als Antwort auf Danke) auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Je vous en prie.`)
</div>

<div class="flex-child">
Sprich 'Das weiß ich nicht' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Je ne sais pas.`)
</div>

<div class="flex-child">
Sprich 'Tut mir leid' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Désolé.`)
</div>

<!-- Preise -->
<div class="flex-child">
Sprich 'Was kostet ...?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Combien coûte ... ?`)
</div>

<div class="flex-child">
Sprich 'Zwei Euro neunzig' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Deux euros quatre-vingt-dix.`)
</div>

<div class="flex-child">
Sprich 'Fünfzig Cent' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Cinquante centimes.`)
</div>

<div class="flex-child">
Sprich 'das Kilo' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le kilo`)
</div>

<div class="flex-child">
Sprich 'das Gramm' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le gramme`)
</div>

<div class="flex-child">
Sprich 'das Stück' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la pièce`)
</div>

<!-- Einkaufen -->
<div class="flex-child">
Sprich 'Bitte sehr?' (Verkäufer: Was wünschen Sie?) auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Vous désirez ?`)
</div>

<div class="flex-child">
Sprich 'Haben Sie ...?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Est-ce que vous avez ... ?`)
</div>

<div class="flex-child">
Sprich 'Sonst noch etwas?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Et avec ceci ?`)
</div>

<div class="flex-child">
Sprich 'Das ist alles' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Ce sera tout.`)
</div>

<!-- Weitere Wörter -->
<div class="flex-child">
Sprich 'die Kasse' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la caisse`)
</div>

<div class="flex-child">
Sprich 'die Pizza' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la pizza`)
</div>

<div class="flex-child">
Sprich 'der Joghurt' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le yaourt`)
</div>

<div class="flex-child">
Sprich 'das Rindfleisch' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la viande de bœuf`)
</div>

<div class="flex-child">
Sprich 'das Schweinefleisch' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la viande de porc`)
</div>

<div class="flex-child">
Sprich 'das Hackfleisch' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la viande hachée`)
</div>

</section>




## Aussprachetraining - Lektion 8

@SpeechRecognition.support

<section class="flex-container">

<!-- Orte in der Stadt -->
<div class="flex-child">
Sprich 'die Apotheke' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la pharmacie`)
</div>

<div class="flex-child">
Sprich 'der Bahnhof' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la gare`)
</div>

<div class="flex-child">
Sprich 'die Bank' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la banque`)
</div>

<div class="flex-child">
Sprich 'das Café' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le café`)
</div>

<div class="flex-child">
Sprich 'die Drogerie' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la droguerie`)
</div>

<div class="flex-child">
Sprich 'der Kindergarten' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le jardin d’enfants`)
</div>

<div class="flex-child">
Sprich 'der Kiosk' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le kiosque`)
</div>

<div class="flex-child">
Sprich 'das Krankenhaus' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`l’hôpital`)
</div>

<div class="flex-child">
Sprich 'der Laden' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le magasin`)
</div>

<div class="flex-child">
Sprich 'der Parkplatz' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le parking`)
</div>

<div class="flex-child">
Sprich 'die Post' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la poste`)
</div>

<div class="flex-child">
Sprich 'die Schule' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`l’école`)
</div>

<!-- Nach Orten fragen & Wege erklären -->
<div class="flex-child">
Sprich 'Entschuldigung, eine Frage …?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Est-ce que je pourrais vous demander… ?`)
</div>

<div class="flex-child">
Sprich 'Ist hier … in der Nähe?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Est-ce qu’il y a … près d’ici ?`)
</div>

<div class="flex-child">
Sprich 'Ist hier irgendwo …?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Est-ce qu’il y a … quelque part par ici ?`)
</div>

<div class="flex-child">
Sprich 'Wo ist …?' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Où est … ?`)
</div>

<div class="flex-child">
Sprich '… ist ganz in der Nähe.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`… est tout près d’ici.`)
</div>

<div class="flex-child">
Sprich 'Gehen Sie links.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Allez à gauche.`)
</div>

<div class="flex-child">
Sprich 'Gehen Sie rechts.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Allez à droite.`)
</div>

<div class="flex-child">
Sprich 'Gehen Sie geradeaus.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Allez tout droit.`)
</div>

<div class="flex-child">
Sprich 'zuerst' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`d’abord`)
</div>

<div class="flex-child">
Sprich 'dann' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`ensuite`)
</div>

<div class="flex-child">
Sprich 'wieder' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`encore`)
</div>

<div class="flex-child">
Sprich 'Gehen Sie die Straße entlang.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Suivez la rue.`)
</div>

<!-- Verkehrsmittel -->
<div class="flex-child">
Sprich 'das Auto' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la voiture`)
</div>

<div class="flex-child">
Sprich 'der Bus' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le bus`)
</div>

<div class="flex-child">
Sprich 'das Fahrrad' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le vélo`)
</div>

<div class="flex-child">
Sprich 'die S-Bahn' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le RER`)
</div>

<div class="flex-child">
Sprich 'die Straßenbahn' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le tram`)
</div>

<div class="flex-child">
Sprich 'die U-Bahn' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le métro`)
</div>

<div class="flex-child">
Sprich 'der Zug' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le train`)
</div>

<div class="flex-child">
Sprich 'Ich fahre mit der U-Bahn.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Je vais en métro.`)
</div>

<div class="flex-child">
Sprich 'Ich fahre mit dem Auto.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Je vais en voiture.`)
</div>

<div class="flex-child">
Sprich 'Ich gehe zu Fuß.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Je vais à pied.`)
</div>

</section>




## Aussprachetraining - Lektion 9

@SpeechRecognition.support

<section class="flex-container">

<!-- Berufe (maskulin) -->
<div class="flex-child">
Sprich 'der Altenpfleger' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`l’assistant pour personnes âgées`)
</div>

<div class="flex-child">
Sprich 'der Arbeiter' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`l’ouvrier`)
</div>

<div class="flex-child">
Sprich 'der Arzt' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le médecin`)
</div>

<div class="flex-child">
Sprich 'der Friseur' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le coiffeur`)
</div>

<div class="flex-child">
Sprich 'der Hausmann' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`l’homme au foyer`)
</div>

<div class="flex-child">
Sprich 'der Kellner' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le serveur`)
</div>

<div class="flex-child">
Sprich 'der Koch' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le cuisinier`)
</div>

<div class="flex-child">
Sprich 'der Maler' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le peintre`)
</div>

<div class="flex-child">
Sprich 'der Schneider' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le tailleur`)
</div>

<div class="flex-child">
Sprich 'der Taxifahrer' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le chauffeur de taxi`)
</div>

<div class="flex-child">
Sprich 'der Verkäufer' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le vendeur`)
</div>

<div class="flex-child">
Sprich 'die Reinigungskraft' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`l’agent d’entretien`)
</div>

<!-- Berufe (feminin) -->
<div class="flex-child">
Sprich 'die Altenpflegerin' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`l’assistante pour personnes âgées`)
</div>

<div class="flex-child">
Sprich 'die Arbeiterin' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`l’ouvrière`)
</div>

<div class="flex-child">
Sprich 'die Ärztin' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la femme médecin`)
</div>

<div class="flex-child">
Sprich 'die Friseurin' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la coiffeuse`)
</div>

<div class="flex-child">
Sprich 'die Hausfrau' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la femme au foyer`)
</div>

<div class="flex-child">
Sprich 'die Kellnerin' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la serveuse`)
</div>

<div class="flex-child">
Sprich 'die Köchin' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la cuisinière`)
</div>

<div class="flex-child">
Sprich 'die Malerin' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la peintre`)
</div>

<div class="flex-child">
Sprich 'die Schneiderin' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la couturière`)
</div>

<div class="flex-child">
Sprich 'die Taxifahrerin' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la chauffeuse de taxi`)
</div>

<div class="flex-child">
Sprich 'die Verkäuferin' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la vendeuse`)
</div>

<!-- Sätze zu Beruf / Ausbildung -->
<div class="flex-child">
Sprich 'Ich bin …' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Je suis …`)
</div>

<div class="flex-child">
Sprich 'Ich habe eine Ausbildung als …' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`J’ai une formation de …`)
</div>

<div class="flex-child">
Sprich 'Im Moment arbeite ich als …' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Actuellement, je travaille en tant que …`)
</div>

<div class="flex-child">
Sprich 'Ich gehe zur Schule.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Je suis élève / étudiant(e).`)
</div>

<div class="flex-child">
Sprich 'Ich möchte … werden.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`J’aimerais devenir …`)
</div>

<div class="flex-child">
Sprich 'Ich mache eine Ausbildung.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Je fais une formation.`)
</div>

<div class="flex-child">
Sprich 'Am Montag habe ich frei.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`J’ai libre le lundi.`)
</div>

<div class="flex-child">
Sprich 'Ich arbeite Schicht.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Je fais les trois-huit.`)
</div>

<!-- Kleidung -->
<div class="flex-child">
Sprich 'die Bluse' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le chemisier`)
</div>

<div class="flex-child">
Sprich 'das Hemd' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la chemise`)
</div>

<div class="flex-child">
Sprich 'die Hose' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le pantalon`)
</div>

<div class="flex-child">
Sprich 'die Jacke' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la veste`)
</div>

<div class="flex-child">
Sprich 'das Kleid' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la robe`)
</div>

<div class="flex-child">
Sprich 'der Rock' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la jupe`)
</div>

<div class="flex-child">
Sprich 'das T-Shirt' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le t-shirt`)
</div>

<div class="flex-child">
Sprich 'der Pullover' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le pull`)
</div>

<!-- Adjektive -->
<div class="flex-child">
Sprich 'schön' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`beau / belle`)
</div>

<div class="flex-child">
Sprich 'hässlich' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`laid / laide`)
</div>

<div class="flex-child">
Sprich 'teuer' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`cher / chère`)
</div>

<div class="flex-child">
Sprich 'günstig' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`bon marché`)
</div>

<!-- Datum & Zeitangaben -->
<div class="flex-child">
Sprich 'am ersten Mai' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le 1er mai`)
</div>

<div class="flex-child">
Sprich 'tagsüber' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`pendant la journée`)
</div>

<div class="flex-child">
Sprich 'am Nachmittag' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`l’après-midi`)
</div>

<div class="flex-child">
Sprich 'in der Nacht' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la nuit`)
</div>

</section>




## Aussprachetraining - Lektion 10

@SpeechRecognition.support



<section class="flex-container">

<!-- Mein Körper -->
<div class="flex-child">
Sprich 'der Kopf' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la tête`)
</div>

<div class="flex-child">
Sprich 'das Ohr' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`l’oreille`)
</div>

<div class="flex-child">
Sprich 'das Auge' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`l’œil`)
</div>

<div class="flex-child">
Sprich 'der Mund' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la bouche`)
</div>

<div class="flex-child">
Sprich 'der Hals' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le cou`)
</div>

<div class="flex-child">
Sprich 'die Hand' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la main`)
</div>

<div class="flex-child">
Sprich 'der Bauch' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le ventre`)
</div>

<div class="flex-child">
Sprich 'der Rücken' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le dos`)
</div>

<div class="flex-child">
Sprich 'das Bein' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la jambe`)
</div>

<div class="flex-child">
Sprich 'der Fuß' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`le pied`)
</div>

<!-- Beschwerden -->
<div class="flex-child">
Sprich 'Mein Hals tut weh.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`J’ai mal au cou.`)
</div>

<div class="flex-child">
Sprich 'Meine Ohren tun weh.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`J’ai mal aux oreilles.`)
</div>

<div class="flex-child">
Sprich 'Ich bin gesund.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Je suis en bonne santé.`)
</div>

<div class="flex-child">
Sprich 'Ich bin krank.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Je suis malade.`)
</div>

<div class="flex-child">
Sprich 'Ich habe Fieber.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`J’ai de la fièvre.`)
</div>

<div class="flex-child">
Sprich 'Ich habe Zahnschmerzen.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`J’ai mal aux dents.`)
</div>

<div class="flex-child">
Sprich 'Ich habe Husten.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Je tousse.`)
</div>

<div class="flex-child">
Sprich 'Ich bin müde.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Je suis fatigué(e).`)
</div>

<div class="flex-child">
Sprich 'Ich bin erkältet.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`J’ai pris froid.`)
</div>

<!-- Ratschläge -->
<div class="flex-child">
Sprich 'Trinken Sie Tee.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Buvez une tisane.`)
</div>

<div class="flex-child">
Sprich 'Bleiben Sie zu Hause.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Restez chez vous.`)
</div>

<div class="flex-child">
Sprich 'Gehen Sie zum Arzt.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Allez voir le docteur.`)
</div>

<div class="flex-child">
Sprich 'Schlafen Sie viel.' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`Vous avez besoin de beaucoup de sommeil.`)
</div>

<!-- Weitere Wörter -->
<div class="flex-child">
Sprich 'schwanger' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`enceinte`)
</div>

<div class="flex-child">
Sprich 'das Rezept (ärztlich)' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`l’ordonnance`)
</div>

<div class="flex-child">
Sprich 'die Gesundheitskarte' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la caisse de maladie`)
</div>

<div class="flex-child">
Sprich 'der Krankenschein' auf französisch.

<!-- data-solution-button="off" -->
[[!]]
@SpeechRecognition(fr-FR,`la fiche de maladie`)
</div>

</section>

