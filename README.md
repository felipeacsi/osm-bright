Estilo para OSM Bright
======================

Actualizando
------------

Se deben borrar los archivos generados por Imposm producto de la conversión del archivo `osm.pbf` en la carpeta donde estén.

Luego, se descarga un archivo `osm.pbf`. En este caso, `chile-latest.osm.pbf` desde [Geofabrik](http://download.geofabrik.de/south-america/chile.html)

Se ejecuta Imposm en la carpeta donde está el `osm.pbf` para hacer la importación:

    imposm -U postgres -d osm -m osm-bright/imposm-mapping.py --read --write --optimize --deploy-production-tables chile-latest.osm.pbf

La importación debería demorar varios minutos usando un procesador al 100%. Normalmente toma unos 10~15 minutos. Si la importación es exitosa, ya se puede ver el mapa actualizado en TileMill.
