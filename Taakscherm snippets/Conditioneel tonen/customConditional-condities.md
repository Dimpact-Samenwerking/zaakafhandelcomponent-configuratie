# customConditional condities

Met JavaScript kun je geavanceerde condities opstellen.

Door `customConditional` toe te voegen aan een component kun je met *JavaScript-logica* een bepaalde conditie evalueren. Afhankelijk van de uitkomt `true` of `false` wordt bepaald of een component moet worden weergegeven `show`.  

```json
"customConditional": "show = ['abc','xyz'].includes(data.key_van_een_ander_component);"
```

In het voorbeeld hierboven wordt gekeken of de waarde van `key_van_een_ander_component` voorkomt (`.includes`) in de lijst met de (de volgende twee tekstuele) waarden: `['abc','xyz']`. De waarde van het component haal je daarbij op de volgend manier op: `data.key_van_een_ander_component`.

In dit geval is waarde waarop je wilt testen een tekst (`string`); daarom plaats je de waarde tussen *enkele quotes*.  
⚠️ Dit wijkt af van de dubbele quotes die je bij JSON-logic en de eenvoudige condities gebruikt!

🚧 TO DO: uitzoeken of form.io nog aanvullende operators ondersteunt.
