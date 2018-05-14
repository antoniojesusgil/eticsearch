Para crear documentos anidados se utiliza el tipo de campo `nested`, el cual nos permite añadir arrays. Verbos a utilizar `POST` `DELETE` `PUT`

### To-Do

1. Añade el siguiente registro y revisa el `mapping` del índice. Reflexiona sobre el resultado
```json
{
  "descripcion":"color verde",
  "marca" : "Skoda",
  "modelo": "Rapid",
  "fecha_compra":"11-01-2017",
  "pais":"Alemania",
  "precio":20000.88,
   "location": { 
    "lat": 30.12,
    "lon": 0.34
  },
  "propietarios":[
    {
    "nombre":"Jose",
    "apellidos":"Gomez"
  },
  {
    "nombre":"Pedro",
    "apellidos":"Ramirez"
  }
  ]
} 
```
2. Modifica el índice `coches` y crea uno nuevo que contenta los los campos `nombre` y `apellidos` anidados en un campo denominado `propietarios` ver tabla adjunta:

| Campo        | Tipo      | Formato    |
|--------------|-----------|------------|
| descripcion  | text      |            |
| fecha_compra | date      | dd-MM-yyyy |
| marca        | keyword   |            |
| pais         | keyword   |            |
| modelo       | text      |            |
| precio       | float     |            |
| location     | geo_point |            |
| propietarios | nested    |            |
| nombre       | text      |            |
| apellidos    | text      |            |


