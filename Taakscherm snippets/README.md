# Taakscherm snippets

Op taakschermen kun je allerlei [Form.io](https://formio.github.io) componenten plaatsen. Denk daarbij generiek componenten zoals tekstvelden, datumvelden, radio buttons, checkboxes en html-content.  
Daarnaast zijn er ook componenten die specifiek geconfigureerd moeten worden voor gebruik binnen ZAC. Dit zijn o.a. componenten voor: het selecteren van documenten, het kiezen van een groep of medewerker, het aanmaken van een document via een documentcreatietool, en het selecteren van een zaakresultaat.

Om het bouwen van de taakschermen makkelijker te maken vind je hier een groot aantal voorbeeldcomponenten. Deze zijn al zo geconfigureerd dat je ze direct kunt gebruiken op de taakschermen.  
Je kunt de code eenvoudig kopieren en toevoegen aan het JSON-bestand van het taakscherm. Als je wilt kun je de code nog wat aanpassen (bijvoorbeeld een veld niet-verplicht maken), maar in de meeste gevallen zijn aanpassingen niet nodig.

⚠️🧪 Voor test- en demonstratiedoeleinden zijn sommige componenten op dit moment mogelijke nog iets anders geconfigureerd dan in de praktijk gewenst.

## Stappenplan

### Nieuw taakscherm maken

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

### Componenten aan taakscherm toevoegen

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

### Veelgebruikte configuratieopties

Een component (een JSON object) bestaat uit bepaalde eigenschappen met elk een bepaalde waarde. Dit wordt vaak een key-value pair genoemd.  
Hieronder worden enkele veelgebruikte eigenschappen (keys) uitgelegd die je bij veel van de componenten kunt configureren.

- `"label"`:  
Meestal de vraag, met een string als waarde. Bijvoorbeeld `"Wat is de datum van de collegevergadering?"`  
- `"key"`:  
De unieke sleutel van het key-value pair. Bijvoorbeeld `"DF_DatumCollegevergadering"`  
- `"type"`:  
Het soort component, waarvan enkele veelgebruikte:
  - `"datetime"`: Een datumveld
  - `"textfield"`: Een tekstveld
  - `"textarea"`: Een tekstvak
  - `"number"`: Een nummerveld. Zowel voor gehele getallen (integer) als decimale getallen (float).
  - `"email"`: Een e-mailveld met een controle om te zien of de invoer aan het juiste format voldoet (bijvoorbeeld `j.doe@example.com`)
  - `"phoneNumber"`: Een telefoonnummer met een controle met een controle om te zien of de invoer aan het juiste format voldoet (bijvoorbeeld `+310123456789`)
  - `"select"`: Een dropdownlijst / combobox.
  - `"selectboxes"`: Een meervoudige selectielijst / checkboxes.
  - `"radio"`: Een enkelvoudige selectielijst / radiobuttons.
  - `"content"`: html-content zoals headers en paragraphs.
- `"defaultValue"`:  
De standaardwaarde die een component heeft. (Optioneel; standaard leeg)  
Afhankelijk van het `type` kan dit o.a. een tekst (string) `"Dit is een tekst"`, geheel getal (integer) `1`, of een waar/niet-waar (boolean) `true`/`false` waarde zijn.
- `"tooltip"`: dit kun je gebruiken om een extra toelichting geven bij een component. De toelichting wordt zichtbaar wanneer de gebruiker naar het [?]-icoontje gaat.
- `"optionsLabelPosition"`:  
De positie van `???????` (Optioneel; standaard boven). Bijvoorbeeld `"right"`.
- `"validate"`:  
Hiermee geef je aan welke validatie je op de invoer wilt doen. (Optioneel; standaard geen validatie).
  - `"required"`: geeft aan of invoer verplicht (`true`) of niet-verplicht (`false`).
  - `"min"` en `"max"`: geeft aan wat de minimale en/of maximale invoer moet zijn. Gebruikt bij numerieke invoer (o.a. integer).
  - `"maxLength"`: gebruikt om de invoer te beperkten tot een aantal karakters.
  - `"pattern"`: gebruikt om de invoer te controleren op een bepaald patroon (in de vorm van een [regulier expressie](https://regex101.com/)).
  - `"customMessage"`: gebruikt om een specifieke (fout)melding te tonen wanneer de invoer niet door de validatie komt.
- DE LIJST MET VEELGEBRUIKTE CONFIGOPTIES WORDT WAARSCHIJNLIJK NOG VERDER UITGEBREID 🚧👷🏻‍♂️🚧
