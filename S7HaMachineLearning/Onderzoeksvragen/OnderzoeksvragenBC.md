## Probleem

Het aanmaken van een automation in Home Assistant via de standaard wizard biedt te weinig mogelijkheden voor een fijne werking van de automation. Wanneer je voor de geavanceerde optie kiest moet je een expert zijn om een automation aan te kunnen maken.
Het zou fijn zijn dat er een suggestie gedaan wordt op basis van de al aanwezige informatie in Home Assistant. Zo kan er al een relatie gelegd worden met de schakelaar en de verlichting in de keuken. Dat wanneer de schakelaar ingedrukt wordt dat de lampen dan aan gaan.
<br>
<br>

### Hoofdvraag:

Hoe kan een machine learning-gebaseerd systeem op basis van bestaande apparaten en automatiseringen, nieuwe automatiseringen genereren en voorstellen aan Home Assistant-gebruikers?
<br>
<br>

### Sub vragen:

Is de beschikbare data binnen Home Assistant voldoende en geschikt om machine learning modellen te trainen?

Methode: Data-analyse en -evaluatie - (Exploratory data analysis (ML))
Reden: Op basis van data-analyse van de omvang en diversiteit kan er vastgesteld worden of het voldoende is om machine learning-modellen te trainen.
<br>
<br>
Welke machine learning technieken zijn geschikt voor het genereren van automations binnen Home Assistant?

Methode: Literatuuronderzoek en vergelijkende analyse
Reden: Door literatuuronderzoek en vergelijkende analyse van bestaande machine learning-technieken, kan er bepaald worden welke technieken het meest geschikt zijn voor het genereren van automatiseringen binnen Home Assistant.
<br>
<br>
Is het mogelijk om automations te generen op basis van aangegeven locatie binnen Home assistant?

Methode: Experimenteel onderzoek (proof-of-concept)
Reden: Door het bouwen van een proof-of-concept kan er geprobeerd worden of het genereren van automations op basis van locatiegegevens en apparaten werkt.

<br>
<br>

# Functionals en nonfunctionals

## Functionals

1. De ML(Machine Learning) moet in staat zijn apparaten en automatiseringen in HA(Home Assistant) te analyseren
2. De ML moet gegevens uit HA kunnen halen, zoals locatiegegevens, automations en de status van apparaten
3. De ML moet zichzelf kunnen trainen op basis van de gegevens in HA
4. De ML moet in staat zijn om werkende automations te genereren en toe te passen in HA
5. De ML is compatibel met de laatste versie van HA
6. De ML moet bij het genereren en toepassen van een automation geen bestaande automations overschrijven
7. De ML moet bij het aanmaken van een automation en het ingeven van een naam altijd beginnen met 'ML -'

<br>

## Non-functionals

1. Voor het genereren van een automation moet dit niet langer duren van 10 seconden
2. De interface moet eenvoudig zijn, het bevat slechts de knoppen: genereer, wijzig, delete, ok
3. De ML moet overweg kunnen met grote datasets en een groot aantal apparaten en automatiseringen, 50 of meer.
4. De ML houdt de gegevens lokaal en worden niet verzonden naar een Cloud oplossing
5. De code van de ML moet makkelijk uitbreidbaar zijn.
6. Er moet een test en validatie set aanwezig zijn om de ML goed te kunnen testen
7. De ML moet voorzien van documentatie en een gebruikershandleiding zodat andere gebruikers de ML kunnen gebruiken.
