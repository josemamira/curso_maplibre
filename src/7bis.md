Eventos y controles
==================
Los controles son botones que se añaden al mapa. Algunos están predefinidos, como el de geolocalización
Este ejemplo lo puedes ver también en la web de MapLibre que te dejo [aquí](https://maplibre.org/maplibre-gl-js/docs/examples/locate-user/)

```html
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
</script>
</body>
</html>
```html
