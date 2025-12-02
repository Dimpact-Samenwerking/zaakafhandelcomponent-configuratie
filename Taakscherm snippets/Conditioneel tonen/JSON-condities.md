# JSON condities

Met JSON kun je geavanceerde condities opstellen.

Door `conditional` toe te voegen aan een component kun je met een `json` een bepaalde conditie evalueren. Afhankelijk van de uitkomt `true` of `false` wordt bepaald of een component moet worden weergegeven.  

```json
"conditional": {
    "json": {
        ">": [
            {
                "var": "data.key_van_een_ander_component"
            },
            0
        ]
    }
}
```

In het voorbeeld hierboven wordt gekeken of de waarde van `key_van_een_ander_component` groter (`>`) is dan de waarde `0`.  
De waarde van het component haal je daarbij op de volgend manier op: `"var": "data.key_van_een_ander_component"`. Omdat je in dit voorbeeld gebruikt maakt van groter dan `>` is het belangrijk dat je de vergelijking maakt tussen getallen (integers). Dus ook de (mogelijke) waarde van het component moet in dit geval een getal zijn.  

🚧 TO DO: meer voorbeelden geven en toelichten hoe ze werken.
