# Probleem

# Hoofdvraag
Ontwikkel een full stack component waarmee de home assistant gebruiker feedback kan geven op de voorspellingen 
zodat de sensoren gelabeld kunnen worden en dat er feedback gegeven kan worden op de gegenereerde automations.

# Subvragen
1. Welke soort machine learning is het beste geschikt om aangestuurd te worden door externe userinput zodat deze zichzelf kan corrigeren?
2. Hoe kan ik data uit de dataset gebruiken om het gedrag van de gebruiker van te stellen en voorspellingen te kunnen doen?
3. Hoe kan ik de keuzes die zijn gemaakt door het model vertalen naar een aantal vragen voor de gebruiker om op te acteren?
4. Hoe kan ik een interface voor de user verzorgen zodat deze op een makkelijke manier vragen kunnen stellen om het model te trainen?


# Functionals en nonfunctionals

## Functionals
1. Per gekoppelde sensors binnen Home Assistant een type sensor en locatie kunnen aangeven.
2. Gegenereerde automations kunnen beoordelen en feedback geven op de voorspellingen.

## Non-functionals
1. De addon moet snel genoeg opstarten zodat de gebruiker niet te lang hoeft te wachten nat het herstarten van Home Assistant.
2. De addon moet voldoen aan de richtlijnen voor toegankelijkheid, zodat het voor mensen met een beperking gemakkelijk is om te gebruiken.
3. De addon moet veilig zijn voor gebruikersgegevens en bescherming bieden tegen aanvallen van buitenaf.
4. De addon moet consistent presteren en weinig of geen fouten produceren.

### Validatie
1. Laadtijd van de addon meten met tools als Lighthouse en WebPageTest.
2. Dat de addon voldoet aan de Web Content Accessibility Guidelines (WCAG). en te testen met bijvoorbeeld accessibility Insights-tool van Microsoft.
3. Penetratietesten en met tools zoals OWASP ZAP.
4. Unit en e2e testing.