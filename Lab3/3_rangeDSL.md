Echa un vistazo a las agregaciones `range` en la [documentación oficial](https://www.elastic.co/guide/en/elasticsearch/reference/6.2/search-aggregations-bucket-range-aggregation.html)

### To-Do
1. Obten los coches que sean `lada`y `renault` usa el comando `terms`
2. Muestra documentos cuya fecha de compra sea inferior al 1 enero 2017
3. Obten los coches cuyo precio sea superior a 30000 en orden descendente.
4. Muestra todos los coches comprendidos entre 1985 y 2017.

```json
GET coches/_search
{
  "query": {
    "terms" : { "marca": ["lada", "renault"]}
  }
}

GET coches/_search
{
    "query": {
        "range" : {
            "fecha_compra" : {
                "lte": "01-01-2017"
            }
        }
    }
}


