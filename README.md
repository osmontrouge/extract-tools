# Extract tools

This host some tools we use to extract data from OpenStreetMap to another format.

## Addresses to sjson

To index addresses on [Addok][]. We take our [opendata][] as geojson and tranform it to a [JSON streaming][json-streaming] file suitable to addok.

    ./bin/addresses2addok https://data.osmontrouge.fr/explore/dataset/base-adresse-locale-bal/download/?format=geojson | gzip | addresses.sjson.gzip

## POI to sjson

To index POI on [Addok][]. We request overpass and transform it to a [JSON streaming][json-streaming] file suitable to addok.

    ./bin/poi2addok https://overpass-api.de/api/interpreter | gzip | poi.sjson.gzip

[addok]: https://github.com/addok/addok
[opendata]: https://data.osmontrouge.fr/
[json-streaming]: https://en.wikipedia.org/wiki/JSON_streaming
