# Taakscherm snippets

Op taakschermen kun je allerlei [Form.io](https://formio.github.io) componenten plaatsen. Denk daarbij generiek componenten zoals tekstvelden, datumvelden, radio buttons, checkboxes en html-content.  
Daarnaast zijn er ook componenten die specifiek geconfigureerd moeten worden voor gebruik binnen ZAC. Dit zijn o.a. componenten voor: het selecteren van documenten, het kiezen van een groep of medewerker, het aanmaken van een document via een documentcreatietool, en het selecteren van een zaakresultaat.

Om het bouwen van de taakschermen makkelijker te maken vind je hier een groot aantal voorbeeldcomponenten. Deze zijn al zo geconfigureerd dat je ze direct kunt gebruiken op de taakschermen.  
Je kunt de code eenvoudig kopieren en toevoegen aan het JSON-bestand van het taakscherm. Als je wilt kun je de code nog wat aanpassen (bijvoorbeeld een veld niet-verplicht maken), maar in de meeste gevallen zijn aanpassingen niet nodig.

⚠️🧪 Voor test- en demonstratiedoeleinden zijn sommige componenten op dit moment mogelijke nog iets anders geconfigureerd dan in de praktijk gewenst.

## Stappenplan

### Nieuw taakscherm

1. Taakscherm aanmaken
   - Maak een nieuw bestand aan.
   - Geef het bestand een bestandsnaam volgens de naamconventies (bijvoorbeeld: `ZTID_ITS001.json`).
1. Kies een schermtemplate, keuze uit:
   - Een scherm bestaande uit 1 stap, met alleen een "Opslaan & afronden" button.
   - Een scherm bestaande uit 1 stap, met een "Opslaan & afronden" button en een "Opslaan" button.
   - Een scherm bestaande uit 2 of meer stappen, met een "Opslaan & afronden" button en een "Opslaan" button.
1. Kopieer de code van het schermtemplate naar het taakscherm (JSON-bestand)
   - Vul bij `name` en `title` de gewenste waarde in.
   - Bepaal welke component(en) je op het scherm wilt plaatsen.

### Componenten

1. Kopieer de code van het gewenste component naar het taakscherm (JSON-bestand)
   - De code plaats je onder `components`.
   - Vul bij `label` de vraag in.
   - Vul bij `key` de unieke waarde in van het zaakdata-element.
1. Geef het component eventueel aanvullende eigenschappen mee. Bijvoorbeeld:
   - Wel of niet verplicht.
   - Tonen op basis van bepaalde condities (eenvoudig of geavanceerd).
1. Test de code, bijvoorbeeld via <https://formio.github.io/formio.js/app/sandbox.html>

## Voorbeeldcomponenten

De snippets (stukjes JSON-code) voor de meestvoorkomende componenten vind je hier, en zijn onderverdeeld in [invoervelden](./Invoervelden), [keuzelijsten](./Keuzelijsten), [(scherm)opmaak](./Layout) en [ZAC-procescomponenten](./Proces). Daarnaast is er ook een aantal [schermtemplates](./Schermtemplates) gemaakt waarmee je eenvoudig de eerst opzet van een scherm kunt maken.  

In de basis werken deze snippets "out of the box" en hoef je dan ook maar een paar dingen aan te passen / te configuren. Maar als je wilt kunt je het component (binnen de grenzen van Form.io) natuurlijk aanpassen zoals je zelf wilt.  

