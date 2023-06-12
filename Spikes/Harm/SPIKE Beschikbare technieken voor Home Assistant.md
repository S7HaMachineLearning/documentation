# Spike info
**Story:** [AA-18](https://prophecy1.atlassian.net/browse/AA-18)
**Onderdeel van:** *Welke AI technologie kan toegepast worden voor het voorspellen van gebruikersgedrag (Machine Learning, Deep Learning, Robotic Process Automation).*
- **Epic:** [AA-1](https://prophecy1.atlassian.net/browse/AA-1)
- **Onderzoeksvraag:** 
**Doel:** *Het doel van deze spike is om te achterhalen welke technieken er al bestaan om binnen home assistatnt een component te ontwikkelen die gebruikersgedag kan voorspellen. 
**Onderzoeksmethode:** 
- Library: Available product analysis
---

## Introductie

Home assistant is een platform die gemaakt is om integraties te doen en te automatiseren. Hier voor zijn verschillende tools beschikbaar voor de gebruiker en ontwikkelaar. 

## YAML

De standaard techniek die word gebruikt om automations te maken is YAML. Hier kan een hoop mee geautomatiseerd worden maar is ook de reden dat dit project is ontstaan. Er zitten heen hoop beperkingen in die er voor zorgen dat je niet in staat bent om een thermostaat volledig generiek te automatiseren. 

## Python 

Home Assistant is gemaakt in Python. Wanneer je wat technischer bent zou je met python scripts aan de slag kunnen gaan. Het enige wat je hier voor moet doen is een map in je config directory aanmaken genaamd python_script. In dit script kan je aan de slag met het bouwen van meer advanced automations

## Add-on

Home Assistant geeft je ook de mogelijkheid om met de home assistant api en add-on te bouwen. Deze add-on komt vervolgens in de add-on store te staan. Deze add-ons kan je gebruiken voor onder andere machine learnign toe te passen, frond ends te bouwen en scripts te schrijven in python. 

## HACS

HACS staat voor Home Assistant Community Store. In deze store kan je je eigen integratie of frond end applicaties bouwen. Hier zitten minder eissen aan voor het ontwikkelen en maakt ook gebruik van de home assistant api. 