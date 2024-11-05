# Curso MapLibre GL JS

Si ha llegado hasta aquí es que te gusta publicar mapas en Internet. MapLibre es una moderna librería Javascript procedente de otro proyecto  (fork) denominado **MapBox GL JS**. El objetivo de esta libería es publicar mapas utilizando el sistema de teselas vectoriales (vector tiles). 

Si quieres leer más sobre **teselas vectoriales** te recomiendo que leas este mágnífico taller de Geoinquietos realizado por  Wladimir Szczerban y  Oscar Fonts.

[Taller Vector Tiles de Geoinquietos](https://geoinquiets.github.io/taller-vt/)

Para poder entender este curso debes de tener algunas nociones básicoas sobre HTML y JavaScript. Sí ya las tienes ya puedes empezar

# Índice

1. Fundamentos de Maplibre: Estructura básica de un mapa:
- [Explicación](src/1.md)
- [Resultado](src/1.html)

2. Escala y zoom:
- [Explicación](src/2.md)
- [Resultado](src/2.html)

# Curso de MapLibre GL JS

## Introducción a MapLibre GL JS

**MapLibre GL JS** es una biblioteca JavaScript de código abierto para visualizar mapas interactivos en 2D y 3D en la web. Se originó como un fork de **Mapbox GL JS** v1.13.0, cuando Mapbox cambió la licencia de su biblioteca a una de pago. **MapLibre GL JS** permite utilizar y personalizar mapas sin depender de servicios de pago, proporcionando una solución libre y abierta.

### Requisitos previos

Para este curso, debes tener conocimientos básicos de:

-   HTML, CSS y JavaScript.
-   Algún editor de código como VSCode o Sublime Text.
-   Acceso a un navegador moderno que soporte ES6 (como Chrome, Firefox, Safari o Edge).

----------

## Contenido

1.  [Configuración del entorno](#configuraci%C3%B3n-del-entorno)
2.  [Creación de un mapa básico](#creaci%C3%B3n-de-un-mapa-b%C3%A1sico)
3.  [Personalización del estilo del mapa](#personalizaci%C3%B3n-del-estilo-del-mapa)
4.  [Interacción con el mapa](#interacci%C3%B3n-con-el-mapa)
5.  [Controlando la cámara](#controlando-la-c%C3%A1mara)
6.  [Añadir controles al mapa](#a%C3%B1adir-controles-al-mapa)
7.  [Trabajar con fuentes y capas](#trabajar-con-fuentes-y-capas)
8.  [Agregar marcadores y popups](#agregar-marcadores-y-popups)
9.  [Estilos personalizados y temas](#estilos-personalizados-y-temas)

----------

## 1. Configuración del entorno

Para empezar a trabajar con **MapLibre GL JS**, incluye la biblioteca en tu proyecto. Puedes hacerlo mediante un enlace directo en tu HTML o instalándolo a través de npm.

### Opción 1: Usando un CDN

Agrega el siguiente código a tu archivo HTML dentro de la etiqueta `<head>`:

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Curso de MapLibre GL JS</title>
  <!-- MapLibre GL JS CSS -->
  <link href="https://unpkg.com/maplibre-gl@2.4.0/dist/maplibre-gl.css" rel="stylesheet" />
  <!-- MapLibre GL JS JavaScript -->
  <script src="https://unpkg.com/maplibre-gl@2.4.0/dist/maplibre-gl.js"></script>
</head>
<body>
  <!-- Aquí irá nuestro código de MapLibre -->
</body>
</html>
```

### Opción 2: Instalación mediante npm

Si prefieres usar npm, instala MapLibre GL JS ejecutando:

bash

Copiar código

`npm install maplibre-gl` 

Luego, importa la biblioteca en tu archivo JavaScript:

javascript

Copiar código

`import maplibre from 'maplibre-gl';` 

----------

## 2. Creación de un mapa básico

Para crear un mapa, necesitas un contenedor en el HTML y un archivo JavaScript que inicialice el mapa.

### Paso 1: Añadir el contenedor HTML

`<div id="map" style="width: 100%; height: 500px;"></div>` 

### Paso 2: Inicializar el mapa en JavaScript

```js
// Crear una instancia de MapLibre
const map = new maplibregl.Map({
  container: 'map', // ID del contenedor
  style: 'https://demotiles.maplibre.org/style.json', // URL del estilo del mapa
  center: [-74.5, 40], // Coordenadas de inicio [longitud, latitud]
  zoom: 9 // Nivel de zoom inicial
});
```

----------

## 3. Personalización del estilo del mapa

Puedes usar estilos prediseñados o cargar uno propio. Por ejemplo:

```js
map.setStyle('https://demotiles.maplibre.org/style.json');
```

Si quieres un estilo personalizado, puedes crear uno en Maputnik o usar un archivo JSON con tus propias definiciones de estilo.

----------

## 4. Interacción con el mapa

### Eventos básicos

Puedes escuchar eventos del mapa como `click`, `mousemove` o `zoom` para realizar acciones específicas:

```js
map.on('click', (event) => {
  const { lng, lat } = event.lngLat;
  console.log(`Se hizo clic en: ${lng}, ${lat}`);
});
``` 

----------

## 5. Controlando la cámara

Puedes cambiar la ubicación de la cámara y el nivel de zoom con métodos como `.flyTo()` o `.jumpTo()`.

```js
map.flyTo({
  center: [-74.5, 40],
  zoom: 12
});
```

----------

## 6. Añadir controles al mapa

MapLibre GL JS proporciona controles como el de zoom y el de geolocalización:

```js
// Control de zoom
map.addControl(new maplibregl.NavigationControl());

// Control de geolocalización
map.addControl(new maplibregl.GeolocateControl({
  positionOptions: {
    enableHighAccuracy: true
  },
  trackUserLocation: true
}));
```

----------

## 7. Trabajar con fuentes y capas

### Añadir una fuente GeoJSON

```js
map.addSource('puntos', {
  type: 'geojson',
  data: {
    type: 'FeatureCollection',
    features: [
      {
        type: 'Feature',
        geometry: {
          type: 'Point',
          coordinates: [-74.5, 40]
        },
        properties: {
          title: 'Ubicación de ejemplo'
        }
      }
    ]
  }
});
```


### Añadir una capa


```js
map.addLayer({
  id: 'puntos',
  type: 'circle',
  source: 'puntos',
  paint: {
    'circle-radius': 10,
    'circle-color': '#007cbf'
  }
});
```

----------

## 8. Agregar marcadores y popups

### Marcadores
```js
new maplibregl.Marker()
  .setLngLat([-74.5, 40])
  .addTo(map);
```

### Popups

```js
const popup = new maplibregl.Popup({ offset: 25 })
  .setLngLat([-74.5, 40])
  .setHTML('<h3>Hola</h3><p>Este es un popup de ejemplo.</p>')
  .addTo(map);
``` 

----------

## 9. Estilos personalizados y temas

Para crear un tema, utiliza un editor como Maputnik para modificar estilos JSON. Puedes ajustar colores, texturas, y elementos visuales como carreteras y edificios, y luego exportar el JSON y usarlo como tu `style`.

```js
map.setStyle('ruta/a/tu/archivo-estilo.json');
```

----------

## Conclusión

En este curso básico, aprendiste a:

-   Configurar MapLibre GL JS en un proyecto.
-   Crear y personalizar un mapa.
-   Trabajar con eventos y controles de cámara.
-   Añadir fuentes, capas, marcadores y popups.

MapLibre GL JS es una herramienta poderosa para integrar mapas interactivos en la web. ¡Experimenta con estas herramientas y construye aplicaciones de mapas sorprendentes!
