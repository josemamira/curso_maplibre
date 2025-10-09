# Precipitación en tiempo real

Este HTML invoca al API de AVAMET para obtener un GeoJSON con los datos de los observatorios (puntos) y selecciona los de precipitación.
La URL es:
https://terramapas.icv.gva.es/0508_AVAMET?request=GetFeature&service=WFS&version=2.0.0&typename=AVAMET.Estaciones&outputformat=geojson&SrsName=EPSG:4326

Los datos obtenidos por cada observatorio son:

- id: Ejemplo: 25458153
- tipus: Ejemplo: AVAMET
- codi: Ejemplo: c01m091e01
- altitud: "1074
- nom: Ejemplo: Portell de Morella
- urlmxo: Ejemplo: http://www.avamet.org/mxo_i.php?id=c01m091e01
- webcam: Ejemplo: https://www.avamet.es/estacions/public_html/portell/webcam.jpg
- actualitzacio: Ejemplo:2024-12-18 08:55:00+01
- temp: Ejemplo: 9
- hrel: Ejemplo: 74
- vent_vel: Ejemplo: 0
- vent_dir: Ejemplo: 360
- vent_dir_360: Ejemplo: 90
- vent_max: Ejemplo: 16.1
- pres: Ejemplo: 1030.5
- prec: Ejemplo: 120

Los procesos realizados con Turf.js son:

1. Cargar el archivo GeoJSON (aquí se usa una URL de ejemplo)
2. Crear la interpolación con Turf.js
3. Crea un grid de 2x2 km
4. Crear una malla de hexágonos
5. Generar isobandas
