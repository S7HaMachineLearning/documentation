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

Het is mogelijk om met machine learning een home assistan instance te ondersteunen. Het prioject 'The silly home' is hiervan een bewijs. Of het veel word gebruikt is niet duidelijk omdat grote bedrijven hun techniek niet prijs geven. 

Wel geven de Nest en Nala oplossingen een goed beeld over hoe je gecontroleerd gebruikers gedrag kan volgen. Dit zal mee genomen worden in de overweging tussen ML en Algoritmes. 

# Bronen

Bron 1. [lcmchris/thesillyhome-addon-repo: add on repo for thesillyhome (github.com)](https://github.com/lcmchris/thesillyhome-addon-repo)
Bron 2. [lcmchris/thesillyhome-container: containerized version (github.com)](https://github.com/lcmchris/thesillyhome-container)
Bron 3. [All The Silly Home Releases - Share your Projects!](https://community.home-assistant.io/t/all-the-silly-home-releases/447305)
Bron 4. [Sense+ Controls and “Nala” Automation Learning Assistant](https://press.nanoleaf.me/press_release/nanoleaf-reveals-five-new-matter-compatible-products-at-ces-2023-to-build-your-smarter-home-of-the-future/#:~:text=Sense%2B%20Controls%20and,launching%20Q3%202023.)
Bron 5. [How Nest thermostats learn](https://support.google.com/googlenest/answer/9247510?hl=en)


