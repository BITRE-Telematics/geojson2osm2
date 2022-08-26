[![Build Status](https://travis-ci.org/Rub21/geojson2osm.svg?branch=master)](https://magnum.travis-ci.com/Rub21/geojson2osm)

## geojson2osm

Convert geojson files to osm file. Alterations to add dummy tags for changelogs, datestamps and version to comply with schema.

## Usage
	
	npm install https://github.com/GeoWonk/geojson2osm2
Example:

```
geojson2osm2 file.geojson > file.osm

```

or


```js
var geojson2osm = require('geojson2osm');
var geo = {
    "type": "FeatureCollection",
    "features": [{
          "type": "Feature",
          "properties": {
            "building:colour": #9F8169
			"building:levels":21
			"building":yes
			"height":57
			},
      "geometry": {
        "type": "Polygon",
        "coordinates": [
          [
            [
              -434.2249470949173,
              -13.15996269397843
            ],
            [
              -434.2249470949173,
              -13.159751140560356
            ],
            [
              -434.2242631316185,
              -13.159751140560356
            ],
            [
              -434.2242631316185,
              -13.15996269397843
            ],
            [
              -434.2249470949173,
              -13.15996269397843
            ]
          ]
        ]
      }
    }
  ]
}
geojson2osm.geojson2osm(geo);
```

### TypeScript

TypeScript implementation was added to the [DefinitelyTyped repository](https://github.com/DefinitelyTyped/DefinitelyTyped).

```bash
$ npm install --save @types/geojson2osm
```

### Testing

```
npm test

```
