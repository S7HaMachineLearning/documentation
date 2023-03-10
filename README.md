# Projectplan

## Automated automations


| Datum | Versie | Status | Auteur |
| --- | ---| --- | --- |
| 20/02/2023 | 0.1 | Draft | Bram van Deventer, Bastiaan Clement, Harm van Genesen |


| Versie | Datum | Auteur(s) | Wijzigingen | Status |
| --- | --- | --- | --- | --- | 
| 0.1 | 20/02/2023 | BvD, BC, HvG | Eerste opzet | Draft |


| Verspreiding | Versie | Datum | Aan |
| --- | --- | --- | --- |


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

### 1.2 Doel van het project

#### Doel

Het doel van dit project is om op basis van gebruikers gedrag en feedback automations te genereren. De eerste intentie is om dit project te gebruiken om meer te leren over Machine Learning. Mocht het het zo zijn dat het in de loop van het semester duidelijk word dat dit niet haalbaar is dan zullen we tijdig van strategie veranderen. 

### 1.3 Begrenzing en Randvoorwaarden


| Tot het project behoort: | Tot het project behoort niet: |
| --- | --- | 
| Een ML model ontwikkelen per product. | Een volledig product beschikbaar maken voor de Home Assistant communitie.|
|  | Een user interface wanneer dit niet noodzakelijk is |

De voorkeur is om machine learning toe te passen in dit project om zo bepaalde leerdoelen te kunnen vervullen. Mocht het zo zijn dat het niet haalbaar blijkt te zijn dan kan er afgeweken worden van deze voorkeur. 


### 1.4 Strategie

#### Werk methode

De werk mothode die word toegepast binnen dit project is Scrum/Agile. Dit word gedaan omdat er in iteraties/sprints word gewerkt. De samenstelling van de groep zal ook baat hebben bij de scrum methode om zo overzichtelijk te houden waar iedereen aan werkt en wat de taakverdelingen zijn.  

### 1.5 Onderzoeksvragen

#### Hoofdvraag

Hoe kunnen we Home Assistant gebruikers ondersteunen met het automatiseren van hun smarthome door yaml automations te genereren.

----

##### Onderzoeksvraag 1 HvG

Hoe kan er op basis van het gedrag van de home assistant gebruiker voorspellingen gedaan worden ~~om automations te genereren~~. 

**Sub vragen:**

- Welke soortgelijke oplossingen zijn er al op de markt en wat voor technieken worden daarvoor gebruikt om dit probleem op te lossen? **
- Welke AI technologie is het meest geschikt voor het lezen en automatiseren van het gebruikers patroon (Machine Learning, Deep Learning, Robotic Process Automation). **
- Hoe functioneren de verschillende AI technologieën binnen Home assistant? **
	- Wat is de minimale dataset grootte?
	- Hoe kan het omgaan met verschillende soorten databases? 
	- Hoe gaat het om met de verschillende programmeer/config talen binnen Home Assistant (YAML, Python, etc.).
- Hoe kan de data uit Home Assistant gebruikt worden voor de gekozen techniek. 
- Welk platform, framework, library binnen te gekozen techniek is het meest geschikt voor het voorspellen van gedrag. 
- ~~Welk platform, framework, library binnen te gekozen techniek is het meest geschikt voor het genereren van automations~~. 

** Kan invloed hebben op onderstaande onderzoeksvragen. 

**Potentiele onderzoeksmethode:
- Library: Community Research, Available product analysis.
- Lab: Data analytics, Usability testing.
- Showroom: Product review, Pitch.
- Workshop: Prototyping.

----
##### Onderzoeksvraag 2 BvD

Hoe kan er op basis van gebruikersfeedback de machinelearning model getraind worden.

**Sub vragen:**

1. Welke soort machine learning is het beste geschikt om aangestuurd te worden door externe userinput zodat deze zichzelf kan corrigeren? 
2. Hoe kan ik data uit de dataset gebruiken om het gedrag van de gebruiker van te stellen en voorspellingen te kunnen doen?
3. Hoe kan ik de keuzes die zijn gemaakt door het model vertalen naar een aantal vragen voor de gebruiker om op te acteren?
4. Hoe kan ik een interface voor de user verzorgen zodat deze op een makkelijke manier vragen kunnen stellen om het model te trainen?

**Potentiele onderzoeksmethode:**

| Vraag  | Strategie  |Methode| Onderbouwing |
|----|:----|:----| :----|
| 1  | Library | Literature study | 1A | 
|    | Library | Available product analysis| 1B | 
| 2  | Lab | Data analytics | 2A | 
|    | Workshop | Prototyping | 2B |
|    | Showroom | Product review | 2C |
| 3  | Library | Literature study | 3A | 
| 	 | Library | Available product analysis | 3B |
| 4  | Library | Literature study | 4A |
|    | Library | Available product analysis | 4B | 
|    | Workshop | Prototyping | 4C | 
|    | Showroom | Product review | 4D |

Onderbouwingen:
* 1A. Informatie opdoen over de bestaande soorten machine learning en welke het beste geschikt is voor dit project 
* 1B. Zoeken naar soortgelijke projecten,hun hun aanpak is geweest en elke technieken zij hebben gebruikt. En proberen uit te vinden waar deze projecten tegen aan gelopen zijn.
* 2A. Data verzamelen en analyseren, bekijken welk info hier beschikbaar is en hoe deze gebruikt kan worden.
* 2B. Een POC maken om met de beschikbare data een model te trainen en te zien of dit mogelijk is.
* 2C. Het gerealiseerde POC tonen en kijken of het voldoet aan de eisen.
* 3A. Zoeken naar meer informatie over dit onderwerp.
* 3B. Zoeken naar projecten die dit type machine learning gebruiken en hoe zij dit hebben opgelost.
* 4a. Onderzoeken welke frameworks geschikt zijn om een interface te maken.
* 4B. Zoeken naar projecten die gemaakt zijn om dit dit de faciliteren.
* 4C. Een POC maken om te kijken of het mogelijk is om dit te realiseren.
* 4D. Het gerealiseerde POC tonen en kijken of het voldoet aan de eisen.

----
##### Onderzoeksvraag 3 BC

Hoe kan er door middel van ML(machine learning) automations in Yaml-formaat genereren om deze in Home Assistant te kunnen gebruiken.



Welke methoden en technieken kunnen gebruikt worden om machine learning toe te passen op automations in Yaml-formaat te genereren

Hoe goed zijn deze automations in vergelijking met handmatig gegenereerde automations of door Home Assistant zelf?

Welke methoden en technieken kunnen worden gebruikt om machine learning toe te passen op automatiseringsregels in Yaml-formaat

Wat is de toepasbaarheid en effectiviteit van verschillende machine learning-algoritmen voor het genereren van automations in Yaml-formaat

Wat is de nauwkeurigheid en effectiviteit van door machine learning gegenereerde regels in vergelijking met handmatig gegenereerde automations

De mogelijke uitdagingen en beperkingen van het gebruik van machine learning bij het genereren van automations in Yaml-formaat



Potentiele onderzoeksmethode (ictresearchmethods.nl):

Library: Literature study, Available product analysis, Best good and bad practices

Field: Document analysis

Lab: Data analytics.

Showroom: Product review, Pitch.

Workshop: Prototyping.


[Onderzoeksmethode Machine learning]([Onderzoeksmethode Machine learning](https://ictresearchmethods.nl/Domain:_Machine_learning)) 

![[2023-03-06 08_52_08-Fontys - Projectplan - Template v2.0 - Word.png]]

-----

### 1.6 Eindproducten

(Een Product Breakdown Structure van de eindproducten die het project op gaat leveren met een korte omschrijving in tekst van elk product. Merk op dat je op later moment in overleg kunt besluiten om je PBS te wijzigen.)

![[2023-03-06 08_52_36-Fontys - Projectplan - Template v2.0 - Word.png]]

## 2. Projectorganisatie

### 2.1 Teamleden

| Naam + tel + e-mail | Afk. | Rol/taken | Beschikbaarheid |
| --- | --- | ---| --- |
| Bastiaan Clement b.clement@student.fontys.nl| BC | Developer | Maandag vrij om aan het project te werken |
|Bram van Deventer b.vandeventer@student.fontys.nl | BvD | Developer Scrum master | Maandag vrij om aan het project te werken |
| Harm van Genesen h.vangenesen@student.fontys.nl | HvG | Developer Product owner | Maandag vrij om aan het project te werken |

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

Het project zal bestaan uit 6 sprints van 3 weken.  Tijdens deze sprint zullen er verschillende scrum rituelen plaatsvinden. 

| Scrum rituelen  | moment | 
| --- | --- | 
| standup | Maandag & donderdag |
| Samenwerk sessie | Maandag & donderdag |
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
| --- | --- | ---| 
| 1 | | |
| 2 | | |
| 3 | | |
