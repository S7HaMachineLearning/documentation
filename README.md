# Projectplan

## Automated automations

| Versie | Datum      | Auteur(s)    | Wijzigingen  | Status |
| ------ | ---------- | ------------ | ------------ | ------ |
| 0.1    | 20/02/2023 | BvD, BC, HvG | Eerste opzet | Draft  |
| 0.2 | 20/03.2023 | BvD, BC, HvG | Alle hoofdstukken aangepast op basis van feedback| Draft | 

| Verspreiding | Versie | Datum | Aan |
| ------------ | ------ | ----- | --- |

## Inhoudsopgave

#todo inhoudsopgaven gereed maken.

[1. Projectopdracht](https://github.com/S7HaMachineLearning/documentation#1-projectopdracht)
[2. Projectorganisatie](documentation#2-Projectorganisatie)

## 1. Projectopdracht

### 1.1 Context

#### Platform

Het product wat er word gemaakt in dit project is specifiek bedoeld voor het Home Assistant platform. Home Assistant is een gratis opensource platform wat iedereen op een eigen computer/server thuis kan draaien waarmee zij smarthome producten kunnen koppelen en aansturen. Ook is het mogelijk of “automations” te schrijven binnen het platform om zo automatisch smarthome producten aan te sturen. Het is mogelijk om voor Home Assistant Add-ons te maken die andere gebruikers kunnen installeren op hun eigen instance.

#### Organisatie

Het project is opensource. Iedere Home Assistan gebruiker kan gebruik maken van de oplossing die word ontwikkeld. Bijdragen leveren staat voor iedereen open. Om een bijdragen te leveren doe je een pull request. Wanneer je je code pusht zal er een QA worden gedaan door Bastiaan, Bram en Harm. Wanneer de push word goedgekeurd dan word de code gemerged. Voordat wij het project open zetten voor bijdragen moet er tenminste een MVP staan. De MVP is geen leeruitkomst voor dit semester.

#### Aanleiding

automations zijn lastig te schrijven, 
komen makkelijk fouten in, 
zijn snel niet betrouwbaar
Is tijdrovend 
Er is meer potentie dan dat de meeste gebruiker voor ogen heeft. 

#### End-users

De Home assistant gebruiker die: 
 - Automations wil hebben maar niet weet hoe
 - Automations wil maar geen tijd heeft
 - Geen zin om uit tezoeken wat hij allemaal kan automatiseren 
 - De beginnende gebruiker
 - Geen zin/tijd heeft om automations te onderhouden. 

#### Use cases 

#todo uitwerken van deze use cases. 
- Trainingsinterface - Bram 
- automation generator - Bastiaan
- data privacy - Harm

#### Requirements 

##### Functional 

- Een automation die word gegenereed word aangeboden via een UI zodat ik (de gebruiker). kan kiezen of deze word geïmplementeerd. 
- Een automation die word gegenereed is gebaseerd om mijn (eindgebruiker) gedrag. 
- Ik (eindgebruiker) wil dat al mijn data prive blijft. 
- Ik (eindgebruiker) wil de gegenereerd automations kunnen aanpassen. 


##### Operational
- Ik (de ontwikkelaar) wil een trainingswizard voor de gebruiker beschikbaar maken zodat de gebruiker het model kan trainen en aan de hand daarvan er betere automations gegenereerd kunnen worden. 
- 

##### Technical & Transitional

De Technical en transitional requirements zijn nog niet van toepassing. De reden hiervoor is dat dit project draait om het onderzoeken van de Technical requirements. We hebben verschillende onderzoeksvragen die gaan bepalen welke technieken nodig zijn om een goed functionerende applicatie te ontwikkelen. Zo kunnen we vrevolgens een duidelijk beeld scheppen hoe we de implementatie stap voor stap kunnen uitvoeren. 


### 1.2 Doel van het project

#### Doel

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

---

##### Onderzoeksvraag 3 BC

~~Ontwikkel een component dat automations gegenereerd op basis van gedragsvoorspellingen en gebruikersfeedback~~


**Sub vragen:**

1. Is de beschikbare data binnen Home Assistant voldoende en geschikt om machine learning modellen te trainen?

2. Welke machine learning technieken zijn geschikt voor het genereren van automations binnen Home Assistant?

3. Is het mogelijk om automations te generen op basis van aangegeven locatie binnen Home assistant?

**Potentiele onderzoeksmethode:**

| Vraag | Strategie             | Methode                                    | Onderbouwing |
| ----- | :-------------------- | :----------------------------------------- | :----------- |
| 1     | Quantitative research | Data analysis and evaluation               | 1A           |
| 2     | Qualitative research  | Literature review and comparative analysis | 2A           |
| 3     | Mixed-method research | Experimental research (proof-of-concept)   | 3A           |

<br>
Onderbouwingen:

- 1A Reden: Op basis van data-analyse van de omvang en diversiteit kan er vastgesteld worden of het voldoende is om machine learning-modellen te trainen.

- 2A Reden: Door literatuuronderzoek en vergelijkende analyse van bestaande machine learning-technieken, kan er bepaald worden welke technieken het meest geschikt zijn voor het genereren van automatiseringen binnen Home Assistant.

- 3A Reden: Door het bouwen van een proof-of-concept kan er geprobeerd worden of het genereren van automations op basis van locatiegegevens en apparaten werkt.

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

**Niet van toepassing voor dit project**

### 5.2 Risico’s en uitwijkactiviteiten

**Niet van toepassing voor dit project**

| Risico | Activiteiten ter voorkoming opgenomen in plan | Uitwijkactiviteiten |
| ------ | --------------------------------------------- | ------------------- |
| 1      |                                               |                     |
| 2      |                                               |                     |
| 3      |                                               |                     |
