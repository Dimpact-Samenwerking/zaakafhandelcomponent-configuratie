# ZAC-procescomponenten

Naast de "standaard" Form.io-componenten zijn er ook componenten die gebruikt kunnen worden voor specifieke functies binnen ZAC.  
Daarbij kun je denken aan het selecteren van een groep en/of medewerker (bijvoorbeeld om een later een taak aan toe te wijzen), het aanmaken van een document op basis van een sjabloon (in een documentcreatietool), of het kiezen van een zaakresultaat.

Deze "ZAC-procescomponenten" zijn te herkennen aan één van de volgende `ZAC_TYPE` `attributes`:

- `ZAC_groep`
- `ZAC_medewerker`
- `ZAC_smart_documents_template`
- `ZAC_referentie_tabel`
- `ZAC_documenten`
- `ZAC_resultaat`
- `ZAC_status`
- `ZAC_process_data`

## Voorbeeldcomponent - Selecteren zaakresultaat

```json 
{
  "label": "Was is het resultaat van deze zaak?",
  "optionsLabelPosition": "right",
  "key": "CO_Zaakresultaat",
  "type": "select",
  "widget": "html5",
  "input": true,
  "dataSrc": "custom",
  "attributes": {
    "ZAC_TYPE": "ZAC_resultaat"
  },
  "validate": {
    "required": true,
    "onlyAvailableItems": true
  }
}
```
