Durante el desarrollo del primer laboratorio hemos visto la dificultad que tiene la construcción de índices de forma manual.

En este ejercicio vemos como añadir gran cantidad de documentos utilizando Bulk API, que permite añadir o borrar multiples operaciones en una única llamadaPuedes obtener más ayuda accediendo a [sección oficial](https://www.elastic.co/guide/en/elasticsearch/reference/current/docs-bulk.html).

### To-Do

1. Borra `coches` y vuelve a crearlo

```json
PUT coches
{
  "settings": {
    "number_of_shards": 1,
    "number_of_replicas": 0
  },
  "mappings": {
    "doc": {
      "dynamic": true,
      "properties": {
        "descripcion": {
          "type": "text"
        },
        "fecha_compra": {
          "type": "date",
          "format": "dd-MM-yyyy",
          "fields": {
            "str": {
            "type":"keyword"
            }
          }
        },
        "marca": {
          "type": "text",
          "fields": {
            "keyword": {
              "type": "keyword",
              "ignore_above": 256
            }
          }
        },
        "pais": {
          "type": "text",
          "fields": {
            "keyword": {
              "type": "keyword",
              "ignore_above": 256
            }
          }
        },
        "modelo": {
          "type": "keyword"
        },
        "precio": {
          "type": "float"
        },
        "location": {
          "type": "geo_point"
        },
        "propietarios": {
          "type": "nested",
          "properties": {
            "nombre" : {
              "type": "text"
                "fields": {
                  "keyword": {
                  "type": "keyword",
                  "ignore_above": 256
                }
              }
            },
            "apellidos": {
              "type": "text"
                "fields": {
                  "keyword": {
                  "type": "keyword",
                  "ignore_above": 256
                }
              }
            }
          }
        }
      }
    }
  }
}
```

2. Copia y pega la insercion masiva de registros utilizando Bulk API.
>El documento con `id=1` es un Peugeot 607. ¿Por qué no ha dado error al insertarlo?

```json
POST /coches/doc/_bulk
{"index":{"_id":1}}
{"descripcion":"nuevo","marca":"Peugeot","modelo":607,"fecha_compra":"11-01-2017","pais":"Francia","precio":240.88,"location":{"lat":42.12,"lon":0.34},"propietarios":[{"nombre":"Romain","apellidos":"Grosjean"}]}
{"index":{"_id":2}}
{"descripcion":"Como nuevo","marca":"Lancia","modelo":"Delta","fecha_compra":"12-01-2017","pais":"Italia","precio":899.88,"location":{"lat":41.12,"lon":0.34},"propietarios":[{"nombre":"Kimi","apellidos":"Raikkonen"}]}
{"index":{"_id":3}}
{"descripcion":"semi nuevo","marca":"Lada","modelo":"Rapid","fecha_compra":"11-01-2017","pais":"Rusia","precio":20000.88,"location":{"lat":30.12,"lon":0.34},"propietarios":[{"nombre":"Sergey","apellidos":"Sirotkin"}]}
{"index":{"_id":4}}
{"descripcion":"color verde","marca":"Bentley","modelo":"Continental","fecha_compra":"11-01-2017","pais":"Alemania","precio":20000.88,"location":{"lat":30.12,"lon":0.34},"propietarios":[{"nombre":"Brendon","apellidos":"Hartley"}]}
{"index":{"_id":5}}
{"descripcion":"Semi nuevo","marca":"Ferrari","modelo":"F40","fecha_compra":"01-08-2004","pais":"Italia","precio":65200,"location":{"lat":42.83,"lon":12.83},"propietarios":[{"nombre":"Marco","apellidos":"Aldani"}]}
{"index":{"_id":6}}
{"descripcion":"buen estado","marca":"VolksWagen","modelo":"Golf I","fecha_compra":"11-01-1975","pais":"Alemania","precio":1200.88,"location":{"lat":42.12,"lon":0.34},"propietarios":[{"nombre":"Nico","apellidos":"Hülkenberg"}]}
{"index":{"_id":7}}
{"descripcion":"En venta","marca":"BMW","modelo":"M5","fecha_compra":"28-10-2017","pais":"Alemania","precio":45000.88,"location":{"lat":30.12,"lon":0.34},"propietarios":[{"nombre":"Sebastian","apellidos":"Vettel"}]}
{"index":{"_id":8}}
{"descripcion":"Ocasión única, a la venta el coche de 007","marca":"Rolls Royce","modelo":"Y665","fecha_compra":"11-12-2017","pais":["Reino Unido”,”Francia"],"precio":55989.88,"location":{"lat":41.12,"lon":-71.34},"propietarios":[{"nombre":"Lewis","apellidos":"Hamilton"}]}
{"index":{"_id":9}}
{"marca":"Seat","modelo":"Ibiza","fecha_compra":"21-05-1987","pais":"España","precio":12000.88,"location":{"lat":41.12,"lon":0.34},"propietarios":[{"nombre":"Carlos","apellidos":"Sainz Jr."}]}
{"index":{"_id":10}}
{"descripcion":"Clásico","marca":"Seat","modelo":"600","fecha_compra":"11-01-2017","pais":"España","precio":12000.88,"location":{"lat":41.12,"lon":0.34},"propietarios":[{"nombre":"Fernando","apellidos":"Alonso"}]}
{"index":{"_id":11}}
{"marca":"Renault","modelo":"R16","fecha_compra":"11-01-1974","pais":"Francia","precio":1200.88,"location":{"lat":42.12,"lon":0.34},"propietarios":[{"nombre":"Pierre","apellidos":"Gasly"}]} 
```
