# Eenvoudige condities

Een eenvoudige (of enkelvoudige) conditie kan worden gebruikt om op basis van 1 waarde een component wel of niet te tonen.

Door `conditional` toe te voegen aan een component kun je met `show` aangeven of het component wel (`true`) of niet (`false`) moet worden weergegeven.  
Dat gebeurt dan wanneer (`when`) een bepaald component gelijk (`eq`) is aan een bepaalde waarde.  

```json
"conditional": {
    "show": true,
    "when": "key_van_een_ander_component",
    "eq": "waarde_x"
}
```

In het voorbeeld hierboven wordt gekeken of de waarde van `key_van_een_ander_component` gelijk (`eq`) is aan de waarde `"waarde_x"`.  
In dit geval is waarde waarop je wilt testen een tekst (`string`); daarom plaats je de waarde tussen *dubbele quotes*.

Bij een test op basis van een getal (`integer` of `float`) of waar/niet-waar (`boolean`) gebruik je géén dubbel quotes. De (mogelijke) waarde van het component moet in dit geval uiteraard van hetzelfde type zijn. 

🚧 TO DO: uitzoeken of form.io nog aanvullende operators ondersteunt.
