### Some words here
La estructura básica de una consulta DSL es
```json
GET /coches/doc/_search
```
Los resultados son mostrados por 'relevancia' (_score) Esta consulta nos muestra el total de `hits` encontrados en `coches` y su `_score`
[Más información sobre la relevancia](https://www.elastic.co/guide/en/elasticsearch/guide/current/relevance-intro.html)

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
Si queremos buscar por un campo concreto en un índice, usamos `match`
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
Con `match_all` obtiene todos los documentos de todos los índices existentes.

##### To-Do
1. Obten los documentos cuya marca sea Ferrari.
2. Obten los documentos cuya marca sea Rolls Royce.
3. Muestra los documentos de cuyos coches sean del Reino Unido y España.
