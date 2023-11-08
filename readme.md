# GPX plugin for Leaflet with extra method for exporting lat/lng coordinates

See readme.md (for leaflet-gpx) for general info.
This fork adds a method 'get_coords()' that returns an array of all the lat/long points in the gpx file.
So (for example) :

    const coords = gpx.get_coords();

    // add direction arrows to GPX polyline
    L.polylineDecorator(coords, {
        patterns: [{
            offset: 50,
            repeat: 50,
            symbol: L.Symbol.arrowHead({
                pixelSize: 10,
                polygon: false,
                pathOptions: { stroke: true, color: 'blue', }
            })
        }]
    }).addTo(map);

Sorry , no type definition info (yet) for the added method. This is my first npm package attempt :)