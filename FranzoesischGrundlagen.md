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


# Klassisches Vokabeltraining - Lektion 1

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




# Klassisches Vokabeltraining - Lektion 2

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







# Klassisches Vokabeltraining - Lektion 3

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
| Sind Sie verheiratet?          | [[ Êtes-vous marié/e? ]]           |
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




# Klassisches Vokabeltraining - Lektion 4

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





# Klassisches Vokabeltraining - Lektion 5

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






# Klassisches Vokabeltraining - Lektion 6

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





# Klassisches Vokabeltraining - Lektion 7

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




# Klassisches Vokabeltraining - Lektion 8

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



# Klassisches Vokabeltraining - Lektion 9

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




# Klassisches Vokabeltraining - Lektion 10

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

Aufgabe 1: Ordne die Kacheln richtig zu.


<!-- data-solution-button="2" data-show-partial-solution  data-randomize="true"-->
Wie geht es Ihnen?  [->[Comment allez-vous]]? \
Kreuzen Sie an. [->[Cochez]]. \


Aufgabe 2: Ordne die Kacheln richtig zu.


<!-- data-solution-button="2" data-show-partial-solution  data-randomize="true"-->
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