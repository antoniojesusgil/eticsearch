### TODO CRUD

1. POST 
```json
POST /coches/doc
{
"description":"estado nuevo",
  "marca" : "Lancia",
  "modelo": "delta",
  "fecha_compra":"12-01-2017",
  "pais":"Italia",
  "precio":899.88,
   "location": { 
    "lat": 41.12,
    "lon": 0.34
  }
} 
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
| localizacion | geo_point |            |
