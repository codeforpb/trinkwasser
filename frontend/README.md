Frontend
========

Zum testen einach ```./src/index.html``` in einem Webbrowser öffnen. Ein Web-
Server ist nicht notwendig.

Wenn die Daten aktualisiert werden, muss die Seite neu geladen werden.


Daten aktualisieren
===================

Die Daten befinden sich in ```./src/data/```. 

```locations.js``` enthält eine Hierarchie der belieferten Bezirke. Beispiel:

```json
tw.data.locations = {
	"Paderborn": {
		"Zentrum": {},
		"Südstadt": {}
	},
	"Marienloh": {}
};
```

**Anmerkung:** Man muss die untersten Bezirke auf ein leeres Element zeigen lassen; siehe "Marienloh" oder "Paderborn Zentrum".

```zones.js``` enthält die verschiedenen Wasserwerke und ihre Daten zur 
Wasserqualität. In der Datei werden erst die Wasserwerke definiert. 
Anschließend werden die Bezirke aus der ```locations.js``` einem der 
Wasserwerke zugewiesen.

Hierzu wird die "Hierarchie-Kette" aus der ```locations.js``` benutzt: "Marienloh" hat keine Unterpunkte und bleibt "Marienloh". "Paderborn" hingegen hat zwei Unterpunkte, weshalb "Paderborn Zentrum" und "Paderborn Südstadt" einem der Wasserwerke zugewiesen werden müssen

Example:
```json
wasserwerkDiebesweg = {
		"natrium": "5.48",
		"kalium": "0.89",
		"calcium": "94.90",
		"magnesium": "2.09",
		"chlorid": "11",
		"nitrat": "13",
		"sulfat": "22",
		"hardness": "13.8",
		"year": "2015",
		"description": "Wasserwerk Diebesweg"
	}

tw.data.zones = {
	"Marienloh": wasserwerkDiebesweg,
	"Paderborn Zentrum": wasserwerkDiebesweg,
	"Paderborn Südstadt": wasserwerkAabach
};
```