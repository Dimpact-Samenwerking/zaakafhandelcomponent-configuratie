# Eenvoudige condities

Een eenvoudige (of enkelvoudige) conditie kan worden gebruikt om op basis van 1 waarde een component wel of niet te tonen.

```json
"conditional": {
    "show": true,
    "when": "key_van_een_ander_component_met_stringwaarde",
    "eq": "waarde"
}
```

Door `conditional` toe te voegen aan een component kun je met `show` aangeven of het component wel (`true`) of niet (`false`) moet worden weergegeven.  
Dat gebeurt dan wanneer (`when`) een bepaald component gelijk (`eq`) is aan een bepaalde waarde.  

🚧 TO DO: uitzoeken of form.io nog aanvullende operators ondersteunt.
