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


## 1. Projectopdracht

### 1.1 Context

(Beschrijf hier kort het bedrijf en de context van de opdracht.)

**Platform**

Het product wat er word gemaakt in dit project is specifiek bedoeld voor het Home Assistant platform. Home Assistant is een gratis platform wat iedereen op een eigen computer thuis kan draaien waarmee zij smarthome producten kunnen koppelen en aansturen. Ook is het mogelijk of “automations” te schrijven binnen het platform om zo automatisch smarthome producten aan te sturen. 

**Organisatie**

Het project is opensource. Iedere home assistan gebruiker kan gebruik maken van de oplossing die word ontwikkeld. Bijdragen leveren staat voor iedereen open. Om een bijdragen te leveren doe je een pull request. Wanneer je je code pusht zal er een QA worden gedaan door Bastiaan, Bram en Harm. Wanneer de push word goedgekeurd dan word de code gemerged

### 1.2 Doel van het project

(Beschrijf hier het doel van het project. Denk aan:
Waarom moet dit project gerealiseerd worden?(Dit kan je opdrachtgever aangeven)
Hoe ziet de gewenste situatie eruit? 
Welke voordelen biedt het project? 
Welke mogelijkheden (capabilities, facilities) biedt het product of het projectresultaat?.)

**Doel**
Door middel van AI Home Assistant users onderstuenen door automations te generen en verbeteren op basis van gedrag en feedback.

### 1.3 Begrenzing en Randvoorwaarden

(Welke producten behoren wel en welke behoren niet tot het project)

| Tot het project behoort: | Tot het project behoort niet: |
| --- | --- | 
| De oplossing(en) lokaal draaiende krijgen binnen het platform. | De plugin beschikbaar maken voor de Home Assistant communitie.|
| Product 1: user tracking en automation |Product 1: user interface |
|Product 2: Trainen van een machine dmv GUI | | 
| Product 3: Yaml genereren vanuit info Product 1&2 | Product 3: User interface |

(Geef voor zover nodig aan wat de randvoorwaarden (constraints) zijn. Denk bijvoorbeeld aan door bedrijf gestelde technologie. Merk op dat hier een kritische houding van belang blijft!)



### 1.4 Strategie

(Ook wel aanpak genoemd. Beschrijf hier hoe het project wordt aangepakt en waarom er voor deze aanpak gekozen is.
Voor stage/afstuderen: Geef hier ook aan welke methode je volgt in je projectplan, bijvoorbeeld of je een waterval-, of scrum-methode gebruikt. Geef ook aan hoe je de probleemdefinitiefase en afrondingsfase gaat aanpakken)

**Werk methode**

De werk mothode die word toegepast binnen dit project is Scrum/Agile. Dit word gedaan omdat er in iteraties/sprints word gewerkt. De samenstelling van de groep zal ook baat hebben bij de scrum methode om zo overzichtelijk te houden waar iedereen aan werkt. 

### 1.5 Onderzoeksvragen

(Deze paragraaf is alleen van toepassing voor stage- en afstudeeropdrachten.
Beschrijf welke onderzoeksvragen je in ieder geval wil gaan beantwoorden. Beschrijf per onderzoeksvraag hoe je wil gaan aanpakken: welke onderzoeksstrategieën (veld, bieb, etc) ga je hiervoor toepassen, en welke methoden horen daarbij. 
Bedenk dat je tijdens je gehele afstuderen onderzoekend aan het werk bent, en dat je vragen dus over je hele afstudeertraject gaan.  
Bedenk dat je tijdens je stage/afstuderen nog tegen meer onderzoeksvragen zult aanlopen die je op dat moment ook weer met bepaling van strategieën en methodes aanpakt. 
Merk op dat het het kan gebeuren dat je onderzoeksvragen tijdens je stage/afstuderen veranderen  of je aanpak nog wijzigt.)

#### Hoofdvraag

Hoe kunnen we Home Assistant gebruikers ondersteunen met het automatiseren van hun smarthome door automatisch yaml automations te genereren.

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

**Potentiele onderzoeksmethode: (ictresearchmethods.nl)**

- Library: Community Research, Available product analysis.
- Lab: Data analytics, Usability testing.
- Showroom: Product review, Pitch.
- Workshop: Prototyping.


##### Onderzoeksvraag 2 BvD

Hoe kan er op basis van gebruikersfeedback de machinelearning model getraind worden.

Sub vragen:

Welke soort machine learning is het beste geschikt om aangestuurd te worden door externe userinput zodat deze zichtzelf kan corrigeren? 

Hoe kan ik data uit de dataset gebruiken om het gedrag van de gebruiker van te stellen en voorspellingen te kunnen doen?

Hoe kan ik de keuzes die zijn gemaakt door het model vertalen naar een aantal vragen voor de gebruiker om op te acteren?

Hoe kan ik een interface voor de user verzorgen zodat deze op een makkelijke manier vragen kunnen stellen om het model te trainen?



Potentiele onderzoeksmethode:

Library: Literature study, Available product analysis.

Lab: Data analytics.

Showroom: Product review, Pitch.

Workshop: Prototyping.



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





Onderzoeksmethode Machine learning 


### 1.6 Eindproducten

(Een Product Breakdown Structure van de eindproducten die het project op gaat leveren met een korte omschrijving in tekst van elk product. Merk op dat je op later moment in overleg kunt besluiten om je PBS te wijzigen.)

## 2. Projectorganisatie

### 2.1 Teamleden

(Geef aan wie betrokken is bij je project en wat zijn/haar functie en wat de rol binnen jouw project is. Zo kan iemand met functie “manager van afdeling X” de rol van Product Owner hebben in jouw project. )

| Naam + tel + e-mail | Afk. | Rol/taken | Beschikbaarheid |
| --- | --- | ---| --- |
| Bastiaan Clement b.clement@student.fontys.nl| BC | Developer | Welke beschikbaarheid van de persoon is noodzakelijk (bijv. 3 dagen per week, gedurende fase 2)|
|Bram van Deventer b.vandeventer@student.fontys.nl | BvD | Developer Scrum master | |
| Harm van Genesen h.vangenesen@student.fontys.nl | HvG | Developer Product owner | |

### 2.2 Communicatie

(Geef aan welke communicatie/afstemmingen er zijn. Denk aan afstemming met bedrijfsbegeleider, docentbegeleider en met andere stakeholders. Op welke manier en hoe vaak vinden deze afstemmingen plaats ?)

**Meetings team:** 
- Stand up 1 x/W
- Sprint planning 1 x/Sprint
- Team building 1á2 x/W

**Meetings docenten / stakeholder:**
- Contact moment 1á2 x/Sprint

**Meetings klasgenoten:**
- Update/presentatie 1 x/ 1á2Sprints?

## 3. Activiteiten en tijdplan

### 3.1 Opdeling en aanpak van het project

(Geef hier de grove opdeling en aanpak van het project (of de onderdelen) weer. 
Bij een scrum aanpak kun je denken aan lengte van sprints, opzet van je sprints, stand up, opzet van demo’s, retrospective, etc).. )

### 3.2 Tijdplan

(Afhankelijk van je project methode zul je de fasering al in meer of minder detail kunnen uitwerken. Hieronder een mogelijke tabel die je hiervoor kunt gebruiken. 
Merk op dat je bij een agile aanpak bij de meeste projecten nog een probleemanalyse/orientatie fase (of ‘sprint 0”) hebt, en ook een afronding/evaluatie fase. 
Let ook op dat je voldoende tijd voor je scriptie of afronding van portfolio reserveert en hier op tijd mee start.)

| Sprints | Effort | Start | Gereed |
| --- | --- | --- | --- | 
| 1| | | |
| 2| | | |
| 3| | | |
| 4| | | |
| 5| | | |
| 6| | | |


## 4. Testaanpak en Configuratiemanagement

### 4.1 Testaanpak/strategie

(Hoe wordt het testen vorm gegeven. Wat is de aanpak? En waarom? Neem eventuele aanpak rondom (Code) reviews hierin ook op)

### 4.2 Testomgeving en benodigdheden

(Beschrijf hoe de testomgeving er uit ziet. Een plaatje geeft over het algemeen het beste overzicht.
Beschrijf welke producten in de testomgeving opgenomen zijn, Dit kunnen producten zijn die het project oplevert maar ook externe producten die noodzakelijk zijn om de testaanpak uit te voeren (bijv. computers).)

### 4.3 Configuratiemanagement

(Beschrijf hoe wordt het archief wordt ingericht. Je kunt hier gebruik maken van een schema.Beschrijf ook welke baselines en releases je voorziet.)

## 5. Financiën en Risico’s

### 5.1 Kostenbudget

(Als specifieke kosten moeten worden gemaakt voor je project, geef deze dan aan. Denk aan extra hardware of software investeringen. Reguliere zaken zoals werkplek, je stage-vergoeding, etc hoeven niet meegenomen te worden.)

### 5.2 Risico’s en uitwijkactiviteiten

(Definieer risico’s. Wat heb je al in het plan opgenomen om het risico te beperken of te voorkomen. Welke keuze wordt gemaakt wanneer het risico onverhoopt toch optreedt.
Denk aan reele risico’s die je project daadwerkelijk kunnen beinvloeden. Zo kan het risico zijn dat je bedrijfsbegeleider wegvalt, bijvoorbeeld door ziekte of doordat hij iets anders gaat doen. Is er dan een backup in het bedrijf ?)

| Risico | Activiteiten ter voorkoming opgenomen in plan | Uitwijkactiviteiten |
| --- | --- | ---| 
| 1 | | |
| 2 | | |
| 3 | | |
