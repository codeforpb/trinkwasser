Frontend
=======================

Use `gulp` to start a local development server with livereload enabled


Update data
=======================

The data files are located in ```./src/data/```. 

```locations.js``` contains a hierarchy of city areas. Example:

```tw.data.locations = {
	"Paderborn": {
		"Zentrum": {},
		"Südstadt": {}
	},
	"Marienloh":{}
};```

Note, that the lowest hierarchy must be terminated with an empty object.

TODO: clarify, how many hierarchy levels are supported.

```zones.js``` contains the definition of different water works and their water quality data. After the definitions of these water works, the map tw.data.zones maps city areas to the corresponding water work.

Example:
```wasserwerkDiebesweg = {
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
	}```

```tw.data.zones = {
	"Marienloh": wasserwerkDiebesweg,
	"Paderborn Zentrum": wasserwerkDiebesweg,
	"Paderborn Südstadt": wasserwerkAabach
};```

Note, how the hierarchy from tw.data.locations is reflected in here and used as a key.

Test the updated data
=======================

It seems to work that you open ```./src/index.html``` in a browser without starting a server. You'll need to reload after updating data files to see the changes.