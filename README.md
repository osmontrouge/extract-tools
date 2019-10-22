# Extract tools

This host some tools we use to extract data from OpenStreetMap to another format.

## Addresses to sjson

[Addok][] want a special json files to index addresses. We take our [opendata][] as geojson and tranform it to [JSON streaming][json-streaming] suitable to addok.

    ./bin/addresses2addok https://data.osmontrouge.fr/explore/dataset/base-adresse-locale-bal/download/?format=geojson | gzip | addresses.sjson.gzip

[addok]: https://github.com/addok/addok
[opendata]: https://data.osmontrouge.fr/
[json-streaming]: https://en.wikipedia.org/wiki/JSON_streaming
