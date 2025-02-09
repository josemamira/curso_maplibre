Símbolo graduado o proporcional (versión clásica
========================================================

Los mapas con símbolos graduados son muy comunes en los mapas, y ayudan a entender un fenómeno fácilmente en función del radio del símbolo, que generalmente es un círculo.

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/bb/Europe_GDP_Map.png/1280px-Europe_GDP_Map.png" width=300>
<figcaption>Fuente: Wikipedia: https://en.wikipedia.org/wiki/Proportional_symbol_map</figcaption><br>


Para este ejemplo hemos querido combinar otros aspectos

- un símbolo graduado en función de un parámetro, que en este caso es la precipitación
- un color fijo con transparencia para que se vean el resto de círculos
- etiquetas con los nombres de los observatorios y la precipitación caída
- simbología de puntos básicas a niveles de zoom inferiores

## Tipo para una capa con símbolo graduado

Una capa de este tipo siempre se aplica a una capa de puntos. 

El primero de todos es el tipo de capa, que en este caso es un **circle**.
```js
type: 'circle',
```


## Simbolización de la capa como símbolo graduado

Los parámetros de simbolización (**paint**) que se necesitan afecta exclusivamente al radio del círculo:

- **circle-radius**: Definer el radio del círculo en función de una propiedad cuantitativa. En este caso la temperatura.

Sí queremos que la graduación del círculo sea por pasos, podemos definir el rádio del círculo para distintos valores de temperatura. En el ejemplo que hemos puesto los valores asignados son:

> Radio de 1 px para la precipitación de 1 mm
>
> Radio de 30 px para la precipitación de 325 mm
> 
> Radio de 60 px para la precipitación de 650 mm

```js
                paint: {
                    'circle-radius': [
                        "interpolate",
                        ["linear"],
                        ["get", "PREC"],  // Basado en el campo "temp" de los datos
                        1, 1,              // Tamaño mínimo para valor bajo
                        325, 30,           // Tamaño medio
                        650, 60,           // Tamaño máximo para valor alto
                    ],
                    'circle-color': '#0074D9',
                    'circle-stroke-color': 'white',
                    'circle-stroke-width': 1,
                    'circle-opacity': 0.8
                }
            });
            //fin addLayer
```



- **circle-color**: Color fijo
Comienza la rampa de color en el punto 0 con un color de transparencia 0 para crear un efecto similar al desenfoque.
```js
                    'circle-color': '#0074D9',
                    'circle-stroke-color': 'white',
                    'circle-stroke-width': 1,
                    'circle-opacity': 0.8
```
### Capas auxiliares
Cuando está uno muy alejado, con niveles de zoom inferior a 8 simbolizamos los observatorios como puntos
```js
            map.addLayer({
                id: 'observatorios-layer2',
                type: 'circle',
                source: 'puntos',
                maxzoom: 7,

                paint: {
                    'circle-radius': 2,
                    'circle-color': '#0074D9'
                },

            });
```

También hemos añadido una capa con las etiquetas del nombre del observatorio visibles a partir de determinado zoom
```js
             // Añadir una capa de etiquetas
             map.addLayer({
                    'id': 'pois_label',
                    'type': 'symbol',
                    'source': 'puntos',
                    'minzoom': 10,
                    'layout': {
                        //'text-field':['concat', 'Hello, ', ['get', 'PREC']],
                        'text-field':['concat',['get', 'nom'], '\n', ["to-string", ['round', ['get', 'PREC']]] ],
                        'text-font': ['Open Sans Semibold', 'Arial Unicode MS Bold'],
                        'text-offset': [0, 2],
                        'text-anchor': 'top'
                    },
                    'paint': {
                        'text-color': '#0074D9',
                        'text-halo-color': 'white',
                        'text-halo-width': 2
                    }
                });
```

### Personalizar la etiqueta

Fíjate bien que hemos concatendo en la etiqueta el nombre del observatorio, y en la línea de abajo las precipitación pero en forma de entero (round)

Ejemplo:

**Turis-Canyapar**

**641**

```js
'text-field':['concat',['get', 'nom'], '\n', ["to-string", ['round', ['get', 'PREC']]] ],
```


### Práctica

- Utiliza otra propiedad, como por ejemplo la altitud del observatorio, y cambia la paleta de colores 
  

### Código completo
El código completo lo tiene aquí:

```html

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Símbolo graduado (clásico)</title>
    <link href="https://unpkg.com/maplibre-gl@2.4.0/dist/maplibre-gl.css" rel="stylesheet" />
    <!-- Script de MapLibre -->
    <script src="https://unpkg.com/maplibre-gl@2.4.0/dist/maplibre-gl.js"></script>
    <style>
        /* Estilo para que el mapa ocupe toda la pantalla */
        body,
        html {
            margin: 0;
            padding: 0;
            width: 100%;
            height: 100%;
            overflow: hidden;
        }

        #map {
            width: 100%;
            height: 100%;
        }

        #titulo {
            position: absolute;
            top: 20px;
            left: 20px;
            width: 250px;
            padding: 15px;
            background-color: rgba(255, 255, 255, 0.9);
            border-radius: 8px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.3);
            font-size: 16px;
            z-index: 1;
        }

        /* Estilo para cada ítem en la leyenda */
        .legend-item {
            display: flex;
            align-items: center;
            margin-bottom: 5px;
        }

        /* Estilos de los círculos para la leyenda */
        .circle {
            border-radius: 50%;
            background-color: rgba(0, 123, 255, 0.7);
            /* Color de los círculos */
            display: inline-block;
            margin-right: 10px;
        }

        /* Tamaños de los círculos */
        .circle-small {
            width: 18px;
            height: 18px;
        }

        .circle-medium {
            width: 37px;
            height: 37px;
        }

        .circle-large {
            width: 75px;
            height: 75px;
        }

        .circle-xlarge {
            width: 120px;
            height: 120px;
        }
    </style>
</head>

<body>
    <!-- Contenedor del mapa -->
    <div id="map"></div>
    <div id="titulo">
        <h3>Leyenda</h3>
        <h4>Precipitación (mm)</h4>
        <p>Dana 29-oct-2024</p>
        <p>Fuente: AVAMET</p>

        <div class="legend-item">
            <div class="circle circle-small"></div>
            <span>100</span>
        </div>

        <div class="legend-item">
            <div class="circle circle-medium"></div>
            <span>200</span>
        </div>

        <div class="legend-item">
            <div class="circle circle-large"></div>
            <span>400</span>
        </div>

        <div class="legend-item">
            <div class="circle circle-xlarge"></div>
            <span>600+</span>
        </div>
    </div>
    

    <script>
        // Inicializa el mapa
        const map = new maplibregl.Map({
            container: 'map',
            style: 'https://basemaps.cartocdn.com/gl/positron-gl-style/style.json', // URL del estilo del mapa
            center: [-0.4030, 39.4531], // Coordenadas iniciales [longitud, latitud] Valencia
            zoom: 7,
            hash: true
        });

        // Agrega una fuente GeoJSON
        map.on('load', (e) => {

            map.addSource('puntos', {
                type: 'geojson',
                data: 'data/dana_2024_10_29.geojson'
            });

            // Agregar capa con símbolos graduados según la temperatura
            map.addLayer({
                id: 'observatorios-layer',
                type: 'circle',
                source: 'puntos',
                minzoom: 7,
                paint: {
                    'circle-radius': [
                        "interpolate",
                        ["linear"],
                        ["get", "PREC"],  // Basado en el campo "temp" de los datos
                        1, 1,              // Tamaño mínimo para valor bajo
                        325, 30,           // Tamaño medio
                        650, 60,           // Tamaño máximo para valor alto
                    ],
                    'circle-color': '#0074D9',
                    'circle-stroke-color': 'white',
                    'circle-stroke-width': 1,
                    'circle-opacity': 0.8
                }
            });
            //fin addLayer

            map.addLayer({
                id: 'observatorios-layer2',
                type: 'circle',
                source: 'puntos',
                maxzoom: 7,

                paint: {
                    'circle-radius': 2,
                    'circle-color': '#0074D9'
                },

            });

             // Añadir una capa de etiquetas
             map.addLayer({
                    'id': 'pois_label',
                    'type': 'symbol',
                    'source': 'puntos',
                    'minzoom': 10,
                    'layout': {
                        //'text-field':['concat', 'Hello, ', ['get', 'PREC']],
                        'text-field':['concat',['get', 'nom'], '\n', ["to-string", ['round', ['get', 'PREC']]] ],
                        //'text-field': ['get', 'PREC'],
                        'text-font': ['Open Sans Semibold', 'Arial Unicode MS Bold'],
                        //'text-offset': [0, 1.25],
                        'text-offset': [0, 2],
                        'text-anchor': 'top'
                        //'text-color': 'red'
                    },
                    'paint': {
                        'text-color': '#0074D9',
                        'text-halo-color': 'white',
                        'text-halo-width': 2
                    }
                });






        }); //on load



        // Evento al hacer click
        map.on('click', 'observatorios-layer', (e) => {
            const coordinates = e.lngLat;
            const nom = e.features[0].properties.ESTACION;
            const temp = e.features[0].properties.TMAX;
            const prec = e.features[0].properties.PREC;
            const altitud = e.features[0].properties.altitud;
            const vent_vel = e.features[0].properties.VMAX;
            const nomactualitzaciobre = e.features[0].properties.actualitzacio;
            const foto = e.features[0].properties.webcam;


            const popupTxt = '<h2>' + nom + '</h2>' +
                '<p><img src="' + foto + '" width=200></p>' +
                '<ul>' +
                '<li>Temperatura: ' + temp + '</li>' +
                '<li>Precipitación: ' + prec + '</li>' +
                '<li>Velocidad viento: ' + vent_vel + '</li>' +
                '<li>Altitud: ' + altitud + '</li>' +
                '<li>Fecha: ' + nomactualitzaciobre + '</li>' +
                '</ul>';


            new maplibregl.Popup()
                .setLngLat(coordinates)
                .setHTML(popupTxt)
                .addTo(map);
        });

        // Evento cuando estás encima del punto
        map.on('mouseenter', 'observatorios-layer', () => {
            map.getCanvas().style.cursor = 'pointer';
        });

        // Evento cuando dejas el punto
        map.on('mouseleave', 'observatorios-layer', () => {
            map.getCanvas().style.cursor = '';
        });



    </script>
</body>

</html>
```
Resultado: [enlace](https://josemamira.github.io/curso_maplibre/src/15bis.html)

Siguiente página: [enlace](16.md)

Índice general: [enlace](../README.md)
