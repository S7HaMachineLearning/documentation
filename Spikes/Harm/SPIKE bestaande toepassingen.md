# Spike info
**Story:** [AA-14](https://prophecy1.atlassian.net/browse/AA-14)
**Onderdeel van:** *Welke AI technologie is het meest geschikt voor het voorspellen van gebruikersgedrag (Machine Learning, Deep Learning, Robotic Process Automation).*
- **Epic:** [AA-1](https://prophecy1.atlassian.net/browse/AA-1)
- **Onderzoeksvraag:** 
**Doel:** *Het doel van deze spike is om te achterhalen wat voor AI oplossingen er al bestaan voor Smart homes en Wat de aanpak is van het onwikkelen van deze oplossing*
**Onderzoeksmethode:** 
- Library: Available product analysis
---

# inleiding
In deze spike ga ik opzoek naar bestaande oplossingen voor zowel Home Assistant als andere smarthome software. 

# The silly home

[The silly home](https://community.home-assistant.io/t/introducing-thesillyhome-a-homeassistant-machine-learning-ai-addon/421351) is een addon voor home assistant die machine learning toepast om statusen van entitys te wijzigen op basis van voorspellingen. De voorspellingen worden gedaan op basis van hystorische data. De data word gegenereerd wanneer een gebruiker handmatig de status van een entity wijzigd. Dit kan gedaan worden door bijvoorbeeld een lamp aan/uit te zetten of de thermosthaat hoger of lager te zetten.  

## 1. start van dit project

De ontwikkelaar van dit project heeft er voor gekozen om zich eerst te focussen op [lampen](https://github.com/lcmchris/thesillyhome-container/#2-learning-model) te automatiseren door het gebruik te maken van een Decision Tree model. Ook word er gekozen om de voorspellingen direct uit te voeren. Hierdoor is het niet nodig om een automation te schrijven. 

### 1.1. Problemen

Tijdens dit project is de ontwikkelaar tegen een aantal problemen aangelopen. Een van de problemen was dat het model getraind werd met zijn eigen input. Dis is niet goed voor het model omdat de data vervuild raakt. Later in het project heeft de ontwikkelaar dit kunnen verhelpen door onderscheid te maken tussen gebruikershandelingen en andere inputs zoals het model en automations. 

## 2. Techniek

De techniek die voor dit project word gebruikt is machine learning.  Door middel van een python script te draaien binnen Home Assistant. Het script maakt gebruik van librarys zoals Numpy, Pandas, ScikidLearn

## 3. Voor en nadelen  

### 3.1. Voordelen

- voorspellingen worden direct uitgevoerd waardoor er geen ontwikkeltijd kwijt is aan het genereren van automations. 
- Er is een dashboard #todo verder uitzoekken wat hierin staat. 

### 3.2. Nadelen 

- Er word geen gebruik gemaakt van automations. Hierdoor heeft de gebruiker mider invloed op wat er gebeurd binnen zijn home assistant. Ook moet er hierdoor onderscheid gemaakt worden door de handelingen die gedaan worden door de gebruiker en de applicatie.  

# Nanoleaf Nala & Sense+

## 1. Wat is Nala & Sense+?
Op CES 2023 heeft Nanoleaf Nala en Sense+ [aangekondigd](https://press.nanoleaf.me/press_release/nanoleaf-reveals-five-new-matter-compatible-products-at-ces-2023-to-build-your-smarter-home-of-the-future/#:~:text=Sense%2B%20Controls%20and,launching%20Q3%202023.). Zij vertellen dat Nala een "intelligent Automation Learning Assistant" is. Wat dit precies inhoud is niet bekend. Het idee is dat je Sense+ gebruikt om de assistent jouw gedrag/patroon aan te leren. Sense+ is niet meer dan een aantal knoppen die je kan gebruiken voor interactie met je lapen. 

Nala en Sense+ zal in Q3 van 2023 uitkomen. 

## 2. Hoe werkt het

### 2.1. Welke technieken worden er gebruikt?

Over de oplossing van Nanoleaf is niet veel te vinden. Of het werkt met machine learning of een zelf geschreven algoritme is niet bekend. 

### 2.2. Wat doet het?

Nala kan enkel je lampen beinvloeden. De oplossing kan ze aan en uit zetten en de felheid aanpassen. 

## 2. Voor en nadelen 

### 2.1 Voordelen
- Het werkt out of the box er is geen configuratie nodig. 

### 2.2 Nadelen

- Het is nog niet bekend of het goed werkt
- Ondankt je je gedrag kan beinvoeden door knoppen heb je niet veel invloed op de automations die worden getriggerd. 
- Je hebt een aparte learning bridge nodig waarvoor je moet betalen. 
- Je hebt speciale knoppen nodig voor het aan en uit zetten van je lampen waarvoor je moet betalen.

# Nest Thermostat

De Nest thermostat was een van de eerste slimme apparaten op de markt die jouw gedrag leert herkennen. Zoals aangegeven op de [support pagina](https://support.google.com/googlenest/answer/9247510?hl=en)  van Google (eigenaar van de nest thermostat) leert de thermostaat aan de hand van jouw gedrag. Na een aantal dagen gebruik herkent de thermostaat een patroon en zal hij deze gaan aanhouden. Hoe meer je de thermostaat blijft gebruiken hoe beter het voorspellings patroon word. 

### De techniek

De techniek die google voor de thermostaat gebruikt word niet openbaar gemaakt. Er word wel aangegeven welke parameters het apparaat gebruikt om een patroon te herkennen. Er kan door middel van verschillende imputs een aan/uit schema gemaakt worden maar en kan ook machine learning worden toegepast. Welke van de 2 het is zal onbeantwoord blijven. 



# Conclusie

<<<<<<< Updated upstream
Het is mogelijk om met machine learning een home assistan instance te ondersteunen. Het prioject 'The silly home' is hiervan een bewijs. Of het veel word gebruikt is niet duidelijk omdat grote bedrijven hun techniek niet prijs geven. 
=======
In ons project is gebruikesgemak en eigenbeheer een belangrijk punt. Denk hierbij aan een vorspelling die word gedaan op basis van jouw gedrag maar jij wil hier zelf nog een kleine aanpassing op doen. Alle 3 de oplossingen die hierboven worden beschreven zijn niet door de gebruiker te beinvoelden naast dat je gebruik maakt van je eigen apperatuur. 

Het is mogelijk om met machine learning een home assistan instance te ondersteunen. Het prioject 'The silly home' is hiervan een bewijs. Ook met het gebruik van een thermostaat is het mogelijk. Wat wel opvalt is dat beide oplossingen gebruik maken van de cloud om de machine learning optimaal toe te kunnen passen. 

De Nest en Nala oplossingen geven een goed beeld over hoe je gecontroleerd gebruikers gedrag kan volgen. Zo maakt de Nala gebruik van specifiek toegewezen knoppen die worden gemonitort. Dit kan twee redenen hebben. De eerste reden zou kunnen zijn dat je een beheer heb op welke entitys wel en niet worden meegenomen in de voorspellingen. De tweede reden zou een verdienmodel kunnen zijn. 
De nest maakt gebruik van beschikbaren entitys zoals de aanwezigheid van een persoon, de temperatuur binnen en buiten en het gebruik.

## Machine Learning of Algoritmes

Hoewel Machine learning een ideale oplossing is voor het voorspellen van gedrag kan dit gevaarlijk zijn binnen een installatie van home assistant. Er zit een beperking in de hoeveelheid data die word gegenereerd en de rekenkracht van de computer. In zowel de nest als de silly home projecten zie je dat cloud word gebruikt voor optimale performance. 

## Mogelijkheden machine learning in Home Assistant

Omdat ongeveer 50% van de home assistant gebruiker gebruik maakt van een Raspberry pi of een soort gelijke hardware (arm) (zie [bron 7](https://analytics.home-assistant.io/)). Kan je aannemen dat de data sets niet erg groot zijn. Standaard verwijderd home assistant na 7 dagen de meeste data. Dit is omdat deze hardware standaard gebruik maakt van een micro sd card. Naast de kleine data set is hier ook een beperkte rekenkracht beschikbaar. Hierdoor word het lastig gemaakt om op deze apparaten lokaal macine learning te gebruiken.  

Hoe zit het dan met de andere 50% van de Home Assistant installaties? 
Deze installaties kunnen op veel verschillende hardware worden gedraaid. Denk hierbij aan een oude laptop, (mini)computer of NAS. De specs kunnen bij deze apparaten erg uiteen lopen.  

Omdat bijna 70% van de installaties HA OS gebruikt kan je aannemen dat deze apparaten niet veel rekenkracht met zich meenemen. Dit is een aanname omdat HA OS geen hoge eissen heeft qua specs. 

## advies

Er zijn 3 opties mogelijk om de oplossing te maken en de keuze zal afhankelijk zijn van de PoC die zal volgen. Uit de PoC zal gaan blijken wat het effect is van een grote bundel data die door een dergelijk model zal gaan lopen. Ook zal er duidelijk moeten worden of de data in Home Assistant bruikbaar is om voorspellingen te doen.  

### Optie 1. 
Het gebruik maken van een lokale machine learning oplossing.
Wanneer je deze oplossing gebruikt zal een groot deel van de home assistant gebruikers mogelijk performance problemen ervaren en mogelijk verkeerde voorspellingen krijgen door teweining data. Het voordeel is dat er niet nagedacht hoeft te worden over ingewikkelde algorimes en cloud oplossingen. Ook blijft hier alle data lokaal en heb je geen problemen data privacy. 

### Optie 2. 
Het gebruik maken van een machine learning oplossing in de cloud. Deze oplossing zou veruit de meest krachtige zijn omdat je geen gebruik hoeft te maken van de hardware van de gebruiker. De nadelen hiervan zijn de kosten en de data die in de cloud komt te staan. 
>>>>>>> Stashed changes

Wel geven de Nest en Nala oplossingen een goed beeld over hoe je gecontroleerd gebruikers gedrag kan volgen. Dit zal mee genomen worden in de overweging tussen ML en Algoritmes. 



# Bronen

Bron 1. [lcmchris/thesillyhome-addon-repo: add on repo for thesillyhome (github.com)](https://github.com/lcmchris/thesillyhome-addon-repo)
Bron 2. [lcmchris/thesillyhome-container: containerized version (github.com)](https://github.com/lcmchris/thesillyhome-container)
Bron 3. [All The Silly Home Releases - Share your Projects!](https://community.home-assistant.io/t/all-the-silly-home-releases/447305)
Bron 4. [Sense+ Controls and “Nala” Automation Learning Assistant](https://press.nanoleaf.me/press_release/nanoleaf-reveals-five-new-matter-compatible-products-at-ces-2023-to-build-your-smarter-home-of-the-future/#:~:text=Sense%2B%20Controls%20and,launching%20Q3%202023.)
Bron 5. [How Nest thermostats learn](https://support.google.com/googlenest/answer/9247510?hl=en)


