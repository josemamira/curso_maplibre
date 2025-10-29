# MAPA DANA
Para realizar este mapa he utilizado la magnífica librería TURF.JS

El dato de partida es un archivo GeoJSON descargado de AVAMET y editado para esta web

## DATOS

- GeoJSON: [datos observatorios DANA 29/sep/2024](https://github.com/josemamira/curso_maplibre/blob/main/src/data/dana_2024_10_29.geojson)
- Comarcas: [comarcas](https://github.com/josemamira/curso_maplibre/blob/main/src/data/comarcas_cv.geojson)

## PROCESOS

- Cargar el archivo GeoJSON
- Realizar la interpolación en modo hexágonos
- Agregar capa de puntos originales al mapa
- Agregar la capa de interpolación al mapa (hexágonos)
- Generar isobandas
