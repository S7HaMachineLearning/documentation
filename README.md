# Projectplan

## Automated automations

| Versie | Datum      | Auteur(s)    | Wijzigingen                                       | Status |
| ------ | ---------- | ------------ | ------------------------------------------------- | ------ |
| 0.1    | 20/02/2023 | BvD, BC, HvG | Eerste opzet                                      | Draft  |
| 0.2    | 20/03.2023 | BvD, BC, HvG | Alle hoofdstukken aangepast op basis van feedback | Draft  |

| Verspreiding | Versie | Datum | Aan |
| ------------ | ------ | ----- | --- |

## Inhoudsopgave

#todo inhoudsopgaven gereed maken.

[1. Projectopdracht](https://github.com/S7HaMachineLearning/documentation#1-projectopdracht)
[2. Projectorganisatie](documentation#2-Projectorganisatie)

## 1. Projectopdracht

### 1.1 Context

#### 1.1.1 Platform

Het product wat er word gemaakt in dit project is specifiek bedoeld voor het Home Assistant platform. Home Assistant is een gratis opensource platform wat iedereen op een eigen computer/server thuis kan draaien waarmee zij smarthome producten kunnen koppelen en aansturen. Ook is het mogelijk of “automations” te schrijven binnen het platform om zo automatisch smarthome producten aan te sturen. Het is mogelijk om voor Home Assistant Add-ons te maken die andere gebruikers kunnen installeren op hun eigen instance.

#### 1.1.2. Organisatie

Het project is opensource. Iedere Home Assistan gebruiker kan gebruik maken van de oplossing die word ontwikkeld. Bijdragen leveren staat voor iedereen open. Om een bijdragen te leveren doe je een pull request. Wanneer je je code pusht zal er een QA worden gedaan door Bastiaan, Bram en Harm. Wanneer de push word goedgekeurd dan word de code gemerged. Voordat wij het project open zetten voor bijdragen moet er tenminste een MVP staan. De MVP is geen leeruitkomst voor dit semester.

#### 1.1.3. Aanleiding

De aanleiding om dit project te starten is dat het soms erg ingewikkeld kan worden om een goede automation te schrijven binnen Home Assistant. De leercurve hier in is vrij stijl en om je instance overzichtelijk en onderhoudbaar te houden zijn er een aantal best practices nodig. Dit kan voor een beginnende Home Assistant gebruiker overkomen als te techniesch, tijd rovend. Ook kan het uiten tot onbetrouwbare automations waardoor de fuctionaliteid buiten beschouwing zal worden gelaten door de gebruiker of in het ergste geval kiest de gebruiker voor een ander platform.

#### 1.1.4. End-users

#watWasDitOokalweer

De Home assistant gebruiker die:

- Automations wil hebben maar niet weet hoe
- Automations wil maar geen tijd heeft
- Geen zin om uit tezoeken wat hij allemaal kan automatiseren
- De beginnende gebruiker
- Geen zin/tijd heeft om automations te onderhouden.

#### 1.1.5. Use cases

##### Trainingsinterface - Bram

|                     |                                                                                                                                                                                                                  |
| :------------------ | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Use case            | 1. Sensor type toekennen                                                                                                                                                                                         |
| Acteur              | De gebruiker                                                                                                                                                                                                     |
| Standaard flow      | Bij het eerste keer gebruiken van de applicatie moet de gebruiker een aantal vragen beantwoorden. Hij krijgt een lijst van zijn gekoppelde sensoren te zien. De gebruiker moet aangeven welk type sensor het is. |
| Alternatief flow 1. | De gebruiker heeft al een training gedaan en wil deze aanpassen.                                                                                                                                                 |
| Alternatief flow 2. | De gebruiker kent geen type toe aan sensoren                                                                                                                                                                     |

|                     |                                                                                                                                                                                                                                                                                                                                    |
| :------------------ | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Use case            | 2. Gegeneerde automation keuren                                                                                                                                                                                                                                                                                                    |
| Acteur              | De gebruiker                                                                                                                                                                                                                                                                                                                       |
| Standaard flow      | De gebruiker krijgt een scherm te zien met hierop een automatisch gegeneerde automation, na het controleren hiervan kiest de gebruiker om deze toe te voegen aan zijn Home Assistant instance. Na de keuzen word deze automation ook daadwerkelijk toegevoegd en word het systeem herladen om de nieuwe automation actief te maken |
| Alternatief flow 1. | De gegeneerde automation klopt, maar de gebruiker kiest er voor om hem niet toe te voegen.                                                                                                                                                                                                                                         |
| Alternatief flow 2. | De gegeneerde automation klopt NIET, de gebruiker geeft aan dat deze incorrect is en voegt hem niet toe.                                                                                                                                                                                                                           |

<br>
<br>

##### automation generator - Bastiaan

| Use case          | Gebruikersgedrag analyseren en automations voorstellen                                                                                                                                                                                                                                                                                                                   |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Acteur            | Systeem, Home Assistant gebruiker                                                                                                                                                                                                                                                                                                                                        |
| Standaard flow    | 1. Systeem verzamelt gegevens over gebruikersgedrag in Home Assistant. 2. Systeem analyseert de verzamelde gegevens met behulp van machine learning. 3. Systeem genereert automations op basis van de geanalyseerde gegevens. 4. Systeem presenteert de gegenereerde automations aan de gebruiker. 5. Gebruiker beoordeelt en implementeert de voorgestelde automations. |
| Alternatiefe flow | 1. Systeem kan niet voldoende gegevens verzamelen over het gedrag van de gebruiker. 2. Systeem vraagt de gebruiker om meer gegevens te verstrekken om de analyse te verbeteren. 3. Gebruiker verstrekt aanvullende gegevens. 4. Systeem hervat de standaard flow vanaf stap 2.                                                                                           |

<br>

| Use case          | Automation genereren op basis van locatie                                                                                                                                                                                                                                                                                                                    |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Acteur            | Systeem, Home Assistant gebruiker                                                                                                                                                                                                                                                                                                                            |
| Standaard flow    | 1. Systeem verzamelt locatiegegevens van de gebruiker in Home Assistant. 2. Systeem analyseert de verzamelde locatiegegevens met behulp van machine learning. 3. Systeem genereert locatiegebaseerde automations. 4. Systeem presenteert de gegenereerde automations aan de gebruiker. 5. Gebruiker beoordeelt en implementeert de voorgestelde automations. |
| Alternatiefe flow | 1. Systeem kan niet voldoende locatiegegevens verzamelen. 2. Systeem vraagt de gebruiker om meer locatiegegevens te verstrekken om de analyse te verbeteren. 3. Gebruiker verstrekt aanvullende locatiegegevens. 4. Systeem hervat de standaard flow vanaf stap 2.                                                                                           |

<br>

| Use case       | Machine learning model selectie en optimalisatie                                                                                                                                                                                                                                                                                                                                                                             |
| -------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Acteur         | Systeem, Onderzoeker                                                                                                                                                                                                                                                                                                                                                                                                         |
| Standaard flow | 1. Onderzoeker identificeert geschikte machine learning technieken voor het genereren van automations. 2. Systeem traint verschillende machine learning modellen met behulp van verzamelde gegevens. 3. Systeem evalueert en vergelijkt de prestaties van de getrainde modellen. 4. Systeem selecteert het beste model en optimaliseert het voor gebruik. 5. Systeem implementeert het geoptimaliseerde model voor het gener |

<br>
<br>

##### data privacy - Harm

| Use case          | Data Privacy                                                                                                                                                                                                                                                                                                                                  |
| ----------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Acteur            | Home Assistan gebruiker, data base                                                                                                                                                                                                                                                                                                            |
| Standaard flow    | De data die word gegenereerd door de gebruiker zijn handelingen blijft locaal op zijn instance staan. Deze blijft daardoor privay. Hierdoor kan een machinelearning model alleen met een beperkte dataset getraint worden om zo beter gebruikersgedrag te voorspellen                                                                         |
| Alternatiefe flow | De data die word gegenereerd door de gebruiker zijn handelingen word opgeslagen in de cloud zonder dat de gebruiker er aan gekopeld kan worden. Hierdoor kan niemand de gebruiker zijn data tracken. Met deze data kan een machine learning model met een grotere data set getraint worden om zo beter gebruikersgedrag te kunnen voorspellen |

| Use case          | Juister voorspelling gebruikersgedrag                                                                  |
| ----------------- | ------------------------------------------------------------------------------------------------------ |
| Acteur            | Home Assistan gebruiker, data base                                                                     |
| Standaard flow    | Het model doet voorspellingen op basis van data die uitsluitend gegenereerd is door de gebruiker zelf. |
| Alternatiefe flow | Het model doet voorspellingen op basis van automatiosn en scripts binnen het platform.                 |

#### 1.1.6. Requirements

##### Functional

- Een automation die wordt gegenereed word aangeboden via een UI zodat ik (de gebruiker). kan kiezen of deze word geïmplementeerd.
- Een automation die word gegenereed is gebaseerd op mijn (eindgebruiker) gedrag.
- Ik (eindgebruiker) wil dat al mijn data prive blijft.
- Ik (eindgebruiker) wil de gegenereerd automations kunnen aanpassen.

##### Operational

- Ik (de ontwikkelaar) wil een trainingswizard voor de gebruiker beschikbaar maken zodat de gebruiker het model kan trainen en aan de hand daarvan er betere automations gegenereerd kunnen worden.
-

##### Technical & Transitional

De Technical en transitional requirements zijn nog niet van toepassing. De reden hiervoor is dat dit project draait om het onderzoeken van de Technical requirements. We hebben verschillende onderzoeksvragen die gaan bepalen welke technieken nodig zijn om een goed functionerende applicatie te ontwikkelen. Zo kunnen we vrevolgens een duidelijk beeld scheppen hoe we de implementatie stap voor stap kunnen uitvoeren.

### 1.2 Doel van het project

Het doel van dit project is om op basis van gebruikers gedrag en feedback automations te genereren. De eerste intentie is om dit project te gebruiken om meer te leren over Machine Learning. Mocht het het zo zijn dat het in de loop van het semester duidelijk word dat dit niet haalbaar is dan zullen we tijdig van strategie veranderen.

### 1.3 Begrenzing en Randvoorwaarden

| Tot het project behoort:              | Tot het project behoort niet:                                             |
| ------------------------------------- | ------------------------------------------------------------------------- |
| Een ML model ontwikkelen per product. | Een volledig product beschikbaar maken voor de Home Assistant communitie. |
|                                       | Een user interface wanneer dit niet noodzakelijk is                       |

De voorkeur is om machine learning toe te passen in dit project om zo bepaalde leerdoelen te kunnen vervullen. Mocht het zo zijn dat het niet haalbaar blijkt te zijn dan kan er afgeweken worden van deze voorkeur.

### 1.4 Strategie

#### Werk methode

De werk mothode die word toegepast binnen dit project is Scrum/Agile. Dit word gedaan omdat er in iteraties/sprints word gewerkt. De samenstelling van de groep zal ook baat hebben bij de scrum methode om zo overzichtelijk te houden waar iedereen aan werkt en wat de taakverdelingen zijn.

### 1.5 Onderzoeksvragen

#### Hoofdvraag

Ontwikkel een Home assistant Add-on waarmee de gebruiker in home assistant
beschikking heeft tot automatisch gegeneerde automations op basis van zijn eigen gedrag, zodat deze gebruiker zelf niet meer automations hoeft te configureren

---

##### Onderzoeksvraag 1 HvG

Ontwikkel een component waarmee gebruikersgedrag voorspeld kan worden
met een beperkte dataset van 1 home assistant instance zodat dit als input gebruikt kan worden voor het genereren van automations.

**Sub vragen:**

1. Welke AI technologie is toepasbaar voor het voorspellen van gebruikersgedrag (Machine Learning, Deep Learning, Robotic Process Automation). \*\*
2. Wat zijn de voor en nadelen van de verschillende AI technologieën binnen Home assistant? \*\*
   - Wat is de minimale dataset grootte?
   - Hoe kan het omgaan met verschillende soorten databases?
   - Hoe gaat het om met de verschillende programmeer/config talen binnen Home Assistant (YAML, Python, etc.).
3. Hoe kan de data uit Home Assistant gebruikt worden voor de gekozen techniek.
4. Welk platform, framework, library binnen te gekozen techniek is het meest geschikt voor het voorspellen van gedrag.

\*\* Kan invloed hebben op onderstaande onderzoeksvragen.

| Vraag | Strategie | Methode                     | Onderbouwing                                                                                                                                                                                                      |
| ----- | --------- | --------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1     | Library   | Literature study            | Om er achter te koment welke technologie gebruikt kan worden voor het voorspellen van gebruukersgedrag is het goed om uit te zoeken welke technologieën er hier voor op de markt zijn.                            |
|       | Library   | Available product analysis  | Er kunnen verschillende oplossingen zijn op de markt die het zelfde probleem proberen op te lossen. Hier wil ik onderzoek naar doen om te weten wat de voor en nadelen hiervan zijn.                              |
|       | Library   | Best good and bad practices | Door opzoek te gaan naar toepassingen van de technologieën wil ik uitzoeken in welke usecases de technologie goed werkt.                                                                                          |
| 2     | Lab       | Data analytics              | Door een data analyse uit te voeren en dit te vergelijken met hoe de data gebruikt word binnen de technologie (Labeling, data grootte) wil ik teweten komen of de technologie toe te passen is voor de HA dataset |
|       | Workshop  | Prototyping                 | Door het maken van een PoC kan ik aantonen hoe de technologie in de praktijk werkt binnen HA                                                                                                                      |
|       | Showroom  | Product review              | Door het reviewen van de PoC kan ik feedback krijgen om zo beter een keuze te maken welke technologie voor ons project bruikbaar zou zijn.                                                                        |
| 3     | Lab       | Usability testing           | Door de PoC die al is gemaakt goed door te testen en fouten op te sporen kan er mogelijk verbetering doorgevoerd worden in het trainen van het model                                                              |
|       | Lab       | Data analytics              | Door de data te analyserenWeet ik beter hoe ik de data kan gebruiken binnen de gekozen technologie                                                                                                                |
| 4     | Library   | Available product analysis  | Om er achter te komen welk model bestaande producten op de markt gebruiken                                                                                                                                        |
|       | Workshop  | Literature study            | Om er achter te komen welke framewoks / models gebruikt worden voor gedragsvoorspelling                                                                                                                           |

---

##### Onderzoeksvraag 2 BvD

Ontwikkel een full stack component waarmee de home assistant gebruiker feedback kan geven op de voorspellingen
zodat de sensoren gelabeld kunnen worden en dat er feedback gegeven kan worden op de gegenereerde automations.

**Sub vragen:**

1. Welke soort machine learning is het beste geschikt om aangestuurd te worden door externe userinput zodat deze zichzelf kan corrigeren?
2. Hoe kan ik data uit de dataset gebruiken om het gedrag van de gebruiker van te stellen en voorspellingen te kunnen doen?
3. Hoe kan ik de keuzes die zijn gemaakt door het model vertalen naar een aantal vragen voor de gebruiker om op te acteren?
4. Hoe kan ik een interface voor de user verzorgen zodat deze op een makkelijke manier vragen kunnen stellen om het model te trainen?

**Potentiele onderzoeksmethode:**

| Vraag | Strategie | Methode                    | Onderbouwing |
| ----- | :-------- | :------------------------- | :----------- |
| 1     | Library   | Literature study           | 1A           |
|       | Library   | Available product analysis | 1B           |
| 2     | Lab       | Data analytics             | 2A           |
|       | Workshop  | Prototyping                | 2B           |
|       | Showroom  | Product review             | 2C           |
| 3     | Library   | Literature study           | 3A           |
|       | Library   | Available product analysis | 3B           |
| 4     | Library   | Literature study           | 4A           |
|       | Library   | Available product analysis | 4B           |
|       | Workshop  | Prototyping                | 4C           |
|       | Showroom  | Product review             | 4D           |

Onderbouwingen:

- 1A. Informatie opdoen over de bestaande soorten machine learning en welke het beste geschikt is voor dit project
- 1B. Zoeken naar soortgelijke projecten,hun hun aanpak is geweest en elke technieken zij hebben gebruikt. En proberen uit te vinden waar deze projecten tegen aan gelopen zijn.
- 2A. Data verzamelen en analyseren, bekijken welk info hier beschikbaar is en hoe deze gebruikt kan worden.
- 2B. Een POC maken om met de beschikbare data een model te trainen en te zien of dit mogelijk is.
- 2C. Het gerealiseerde POC tonen en kijken of het voldoet aan de eisen.
- 3A. Zoeken naar meer informatie over dit onderwerp.
- 3B. Zoeken naar projecten die dit type machine learning gebruiken en hoe zij dit hebben opgelost.
- 4a. Onderzoeken welke frameworks geschikt zijn om een interface te maken.
- 4B. Zoeken naar projecten die gemaakt zijn om dit dit de faciliteren.
- 4C. Een POC maken om te kijken of het mogelijk is om dit te realiseren.
- 4D. Het gerealiseerde POC tonen en kijken of het voldoet aan de eisen.

**Functionals en nonfunctionals**\
zie [Requirements document](/S7HaMachineLearning/Onderzoeken/Bram/4.%20Requirements%20document.md)

<br>

---

##### Onderzoeksvraag 3 BC

Hoe kan machine learning worden gebruikt om Home Assistant automations te verbeteren op basis van gebruikersgedrag?

**Sub vragen:**

1. Is de beschikbare data binnen Home Assistant voldoende en geschikt om machine learning modellen te trainen?

2. Welke machine learning technieken zijn geschikt voor het genereren van automations binnen Home Assistant?

3. Is het mogelijk om automations te generen op basis van aangegeven locatie binnen Home assistant?

**Potentiele onderzoeksmethode:**

| Vraag | Strategie             | Methode                                    | Onderbouwing |
| ----- | :-------------------- | :----------------------------------------- | :----------- |
| 1     | Quantitative research | Data analysis and evaluation               | 1A           |
| 1     | Quantitative research | Data preprocessing and analysis            | 1B           |
| 1     | Mixed-method research | Interviewing                               | 1C           |
| 2     | Qualitative research  | Literature review and comparative analysis | 2A           |
| 2     | Quantitative research | Machine learning modeling and evaluation   | 2B           |
| 2     | Qualitative research  | Focus groups                               | 2C           |
| 3     | Mixed-method research | Experimental research (proof-of-concept)   | 3A           |
| 3     | Mixed-method research | User testing                               | 3A           |
| 3     | Mixed-method research | Case study analysis                        | 3A           |

<br>
Onderbouwingen:

- 1A Reden: Op basis van data-analyse van de omvang en diversiteit kan er vastgesteld worden of het voldoende is om machine learning-modellen te trainen.
- 1B Reden: Door middel van data preprocessing kan ik de beschikbare gegevens voorbereiden op de machine learning-modellen en door middel van data-analyse kan ik de kwaliteit en de geschiktheid van de data beoordelen.
- 1C Reden: Door middel van interviews met experts en gebruikers van Home Assistant kunnen we meer inzicht krijgen in de beschikbare data en kunnen we bepalen of er aanvullende gegevens nodig zijn voor de machine learning-modellen.

- 2A Reden: Door literatuuronderzoek en vergelijkende analyse van bestaande machine learning-technieken, kan er bepaald worden welke technieken het meest geschikt zijn voor het genereren van automatiseringen binnen Home Assistant.
- 2B Reden: Door middel van het trainen van verschillende machine learning-modellen kunnen we bepalen welke technieken het meest geschikt zijn voor het genereren van automatiseringen binnen Home Assistant. Daarnaast kunnen we de prestaties van de modellen evalueren om de nauwkeurigheid en effectiviteit te beoordelen.
- 2C Reden:Door middel van focusgroepen met experts en gebruikers van Home Assistant kunnen we hun inzichten en ervaringen over de geschikte machine learning-technieken voor het genereren van automatiseringen verzamelen. Dit kan ons helpen om meer inzicht te krijgen in de behoeften en verwachtingen van de gebruikers.

- 3A Reden: Door het bouwen van een proof-of-concept kan er geprobeerd worden of het genereren van automations op basis van locatiegegevens en apparaten werkt.
- 3B Reden: Door middel van user testing kunnen we testen of het genereren van automatiseringen op basis van aangegeven locatie binnen Home Assistant werkt en of het voldoet aan de verwachtingen en behoeften van de gebruikers.
- 3C Reden: Door middel van een case study-analyse van eerdere toepassingen van locatiegegevens binnen Home Assistant kunnen we bepalen welke benaderingen het meest succesvol zijn geweest en welke lessen we kunnen leren van hun successen en mislukkingen.

**Functionals en nonfunctionals**
zie [Requirements](/S7HaMachineLearning/Onderzoeken/Bastiaan/0.%20Requirements.md)
<br>

---

### 1.6 Eindproducten

(Een Product Breakdown Structure van de eindproducten die het project op gaat leveren met een korte omschrijving in tekst van elk product. Merk op dat je op later moment in overleg kunt besluiten om je PBS te wijzigen.)

![[2023-03-06 08_52_36-Fontys - Projectplan - Template v2.0 - Word.png]]

## 2. Projectorganisatie

### 2.1 Teamleden

| Naam + tel + e-mail                               | Afk. | Rol/taken               | Beschikbaarheid                           |
| ------------------------------------------------- | ---- | ----------------------- | ----------------------------------------- |
| Bastiaan Clement b.clement@student.fontys.nl      | BC   | Developer               | Maandag vrij om aan het project te werken |
| Bram van Deventer b.vandeventer@student.fontys.nl | BvD  | Developer Scrum master  | Maandag vrij om aan het project te werken |
| Harm van Genesen h.vangenesen@student.fontys.nl   | HvG  | Developer Product owner | Maandag vrij om aan het project te werken |

### 2.2 Communicatie

#### Meetings team:

- Stand up 1 x/W
- Sprint planning 1 x/Sprint
- Team building 1á2 x/W

#### Meetings docenten / stakeholder:

- Contact moment 1á2 x/Sprint

#### Meetings klasgenoten:

- Update/presentatie 1 x/ 1á2Sprints?

## 3. Activiteiten en tijdplan

### 3.1 Opdeling en aanpak van het project

Het project zal bestaan uit 6 sprints van 3 weken. Tijdens deze sprint zullen er verschillende scrum rituelen plaatsvinden.

| Scrum rituelen       | moment              |
| -------------------- | ------------------- |
| standup              | Maandag & donderdag |
| Samenwerk sessie     | Maandag & donderdag |
| Sprint review / demo | Week na eide sprint |

### 3.2 Tijdplan

Zie voor het tijdsplan de [Roadmap]([Automated automations - Roadmap - Jira (atlassian.net)](https://prophecy1.atlassian.net/jira/software/projects/AA/boards/2/roadmap)) van dit project.

## 4. Testaanpak en Configuratiemanagement

### 4.1 Testaanpak/strategie

(Hoe wordt het testen vorm gegeven. Wat is de aanpak? En waarom? Neem eventuele aanpak rondom (Code) reviews hierin ook op)

Dit moet nog worden uitgezocht.

### 4.2 Testomgeving en benodigdheden

(Beschrijf hoe de testomgeving er uit ziet. Een plaatje geeft over het algemeen het beste overzicht.
Beschrijf welke producten in de testomgeving opgenomen zijn, Dit kunnen producten zijn die het project oplevert maar ook externe producten die noodzakelijk zijn om de testaanpak uit te voeren (bijv. computers).)

Dit moet nog worden uitgezocht.

### 4.3 Configuratiemanagement

Er is een [GitHub]([S7HaMachineLearning (github.com)](https://github.com/S7HaMachineLearning)) project waar alle repos in koment te staan. Dit is gelijk ons versie beheer.

## 5. Financiën en Risico’s

### 5.1 Kostenbudget

Dit project neemt geen kosten met zich mee.

### 5.2 Risico’s en uitwijkactiviteiten

| Risico | Activiteiten ter voorkoming opgenomen in plan          | Uitwijkactiviteiten                                                                                                                                   |
| ------ | ------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1      | Uitval van een collega                                 | Iedereen gaat door met zijn eigen taken. Wanneer er afhankelijkheden zijn word dit besproken door de aanwezige collegas en wanneer mogelijk opgepakt. |
| 2      | De gewenste techniek is niet geschikt voor dit project | Er word gekeken naar andere technieken                                                                                                                |
| 3      |                                                        |                                                                                                                                                       |
