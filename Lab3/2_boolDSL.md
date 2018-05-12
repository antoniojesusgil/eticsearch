### Some words here

Las Consultas booleanas nos permiten hacer combinaciones
```json
GET coches/doc/_search
{
"query": {
    "bool": {
      "must": [
        {
          "match": {
            "marca": "seat"
          }
        },
        {
          "match": {
            "modelo": "ibiza"
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
