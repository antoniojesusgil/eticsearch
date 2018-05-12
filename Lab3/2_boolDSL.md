### Some words here

Las Consultas booleanas nos permiten hacer combinaciones
```json
GET /inspections/report/_search
{
  "query": {
    "bool": {
      "must": [
        {
          "match": {
            "business_name": "soup"
          }
        },
        {
          "match_phrase": {
            "business_name": "san francisco"
          }
        }
      ]
    }
  }
}
``` 

##### To-Do
1. Obten 

```json
