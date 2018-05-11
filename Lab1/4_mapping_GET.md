### TODO

1. Obten mediante verbo `GET` el mapping del nuevo indice 'coches'
2. Mediante el uso del verbo `PUT`añade un nuevo coche con las siguientes caracteristicas
```json
  "marca" : "Ferrari",
  "modelo": "F40",
  "fecha_compra":"01-08-2004",
  "pais":"Italia",
  "precio":65200,
   "location":  
    "lat": 42.83,
    "lon": 12.83
```


. Crea un indice llamado 'coches' usando el comando `PUT` Los campos, tipo de dato y formato se detallan acontinuación.

| Campo        | Tipo      | Formato    |
|--------------|-----------|------------|
| descripcion  | text      |            |
| fecha_compra | date      | dd-MM-yyyy |
| marca        | text      |            |
| pais         | text      |            |
| modelo       | text      |            |
| precio       | float     |            |
| location     | geo_point |            |
