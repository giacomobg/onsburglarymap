# A Map of Burglaries

Making it easier to explore police.uk data

### We calculated a yearly burglary rate.

- This rate should be recalculated with greater attention to detail.

### We attached this data to shapefiles/geojson files and created map tiles.

The following were created in QGIS:

- Burglary.geojson is all the individual buildings, variables to be used for shading should be bound here.
- Lsoas.geojson is for the hover layer, variables to be shown in the key should be bound.

Tippecanoe commands

##### To create the hover layer  
```tippecanoe --minimum-zoom=9 --maximum-zoom=15 --output-to-directory tiles --no-tile-size-limit --force lsoas.geojson```

##### To create the building layer  
```tippecanoe --minimum-zoom=4 --maximum-zoom=7 --output-to-directory tiles --full-detail=9 --drop-smallest-as-needed --extend-zooms-if-still-dropping --force burglary.geojson```  
```tippecanoe --minimum-zoom=8 --maximum-zoom=10 --output-to-directory tiles --full-detail=10 --no-tile-size-limit --force burglary.geojson```  
```tippecanoe --minimum-zoom=11 --maximum-zoom=13 --output-to-directory tiles --full-detail=11 --no-tile-size-limit --force burglary.geojson```
