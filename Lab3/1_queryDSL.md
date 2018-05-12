### Some words here
La estructura básica de una consulta DSL es
```json
GET /coches/doc/_search
```
Esta consulta nos muestra el total de `hits` encontrados

```json
{
  "took": 5,
  "timed_out": false,
  "_shards": {
    "total": 5,
    "successful": 5,
    "skipped": 0,
    "failed": 0
  },
  "hits": {
    "total": 2,
    "max_score": 1,
    "hits": [
      {
        "_index": "coches",
        "_type": "doc",
        "_id": "10000",
        "_score": 1,
        "_source": {
          "marca": "Ferrari",
          "modelo": "F40",
          "fecha_compra": "01-08-2004",
          "pais": "Italia",
          "precio": 65200,
          "location": {
            "lat": 42.83,
            "lon": 12.83
          }
        }
      },
      {
        "_index": "coches",
        "_type": "doc",
        "_id": "D9UdUGMBTvoP0lVuJbec",
        "_score": 1,
        "_source": {
          "descripcion": "color verde",
          "marca": "Skoda",
          "modelo": "Rapid",
          "fecha_compra": "11-01-2017",
          "pais": "Alemania",
          "precio": 20000.88,
          "location": {
            "lat": 30.12,
            "lon": 0.34
          },
          "proprietarios": [
            {
              "nombre": "Jose",
              "apellidos": "Gomez Abascal"
            },
            {
              "nombre": "Pedro",
              "apellidos": "Ramirez Viladrau"
            }
          ]
        }
      }
    ]
  }
}
```
Si queremos buscar por un campo concreto usamos `match`
```json
GET /coches/_search
{
  "query": {
    "match": {
      "pais": "Alemania"
    }
  }
}
```


##### To-Do
1. Crea un indice denominado `coches` y documento de tipo `doc` con la información de abajo. Recuerda que el `id` se genera automáticamente.

```json
"descripcion":"Como nuevo",
  "marca" : "Lancia",
