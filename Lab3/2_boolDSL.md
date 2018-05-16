Las consultas booleanas nos permiten hacer combinaciones
```json
GET coches/doc/_search
{
"query": {
    "bool": {
      "must": [
        {
          "match": {
            "marca": "Seat"
          }
        },
        {
          "match": {
            "modelo": "Ibiza"
          }
        }
      ]
    }
  }  
}
``` 

### To-Do
1. Obten todos los coches franceses que sean Peugeot.
2. Obten todos los coches cuyo precio sea mayor a 20000.
3. Muestra todos los coches que no sean Españoles.

```json
GET coches/doc/_search
{
"query": {
    "bool": {
      "must": [
        {
          "match": {
            "marca": "Peugeot"
          }
        },
        {
          "match": {
            "pais": "francia"
          }
        }
      ]
    }
  }  
}

