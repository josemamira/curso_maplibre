Eventos y controles
==================
Los controles son botones que se añaden al mapa. Algunos están predefinidos, como el de geolocalización.
Su función es añadir una marca en el mapa con nuestra ubicación. Obviamente nos pedirá permiso para habilitar el servicio de geolocalización.

Este ejemplo lo puedes ver también en la web de MapLibre que te dejo [aquí](https://maplibre.org/maplibre-gl-js/docs/examples/locate-user/)

Para añadir este control sólo tienes que indicar este código:
```js
     // Añadir botón geolocalización al mapa
    map.addControl(
        new maplibregl.GeolocateControl({
            positionOptions: {
                enableHighAccuracy: true
            },
            trackUserLocation: true
        })
    );
```

También vamos a añadir otro control con los créditos al autor
```js
 // Créditos personalizados
    map.addControl(
        new maplibregl.AttributionControl({
            compact: true, // compact layout
            customAttribution: '<a href="https://josemamira.github.io/curso_maplibre" target="_blank">Jose Manuel Mira</a>'
        })
    );
```
El ejemplo completo lo puedes ver aquí

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Locate the user</title>
    <meta property="og:description" content="Geolocate the user and then track their current location on the map using the GeolocateControl." />
    <meta charset='utf-8'>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel='stylesheet' href='https://unpkg.com/maplibre-gl@4.7.1/dist/maplibre-gl.css' />
    <script src='https://unpkg.com/maplibre-gl@4.7.1/dist/maplibre-gl.js'></script>
    <style>
        body { margin: 0; padding: 0; }
        html, body, #map { height: 100%; }
    </style>
</head>
<body>
<div id="map"></div>
<script>
    const map = new maplibregl.Map({
        container: 'map', // container id
        style:
            'https://api.maptiler.com/maps/streets/style.json?key=get_your_own_OpIi9ZULNHzrESv6T2vL',
        center: [-96, 37.8], // starting position
        zoom: 3 // starting zoom
    });

    // Añadir botón geolocalización al mapa
    map.addControl(
        new maplibregl.GeolocateControl({
            positionOptions: {
                enableHighAccuracy: true
            },
            trackUserLocation: true
        })
    );

 // Créditos personalizados
    map.addControl(
        new maplibregl.AttributionControl({
            compact: true, // compact layout
            customAttribution: '<a href="https://josemamira.github.io/curso_maplibre" target="_blank">Jose Manuel Mira</a>'
        })
    );
</script>
</body>
</html>
```html
