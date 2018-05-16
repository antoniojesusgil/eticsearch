Echa un vistazo al objeto `nested` en la [documentación oficial](https://www.elastic.co/guide/en/elasticsearch/reference/6.x/nested.html)

### To-Do
1. Crea una consulta `nested` que muestre los propietarios cuyo nombre es `Fernando`
2. Crea una consulta `nested` que muestre los propietarios cuyo nombre sea `Sebastian` y se apellide `Vettel`
3. Crea una consulta que muestre documentos con más de un propietario.

```json
GET coches/doc/_search
{
  "query": {
    "nested": {
      "path": "propietarios",
      "query": {
        "bool": {
          "must": [
            {
              "match": {
                "propietarios.nombre": "Fernando"
              }
            }
          ]
        }
      }
    }
  }
}

GET coches/doc/_search
{
  "query": {
    "nested": {
      "path": "propietarios",
      "query": {
        "bool": {
          "must": [
            {
              "match": {
                "propietarios.nombre": "James"
              }
            },
            {
              "match": {
                "propietarios.apellidos": "Bond"
              }
            }
          ]
        }
      }
    }
  }
}


