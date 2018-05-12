### Some words here

Durante el desarrollo del Lab1 vimos la dificultad que tiene la construcción de índices de forma manual.
Borra el `coches` y añade lo siguiente:

```json
DELETE coches
```
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
            },
            "apellidos": {
              "type": "text"
            }
          }
        }
      }
    }
  }
}
```
```json
POST /coches/doc/_bulk
{"index":{"_id":1}}
{"descripcion":"Coche francés","marca":"Peugeot","modelo":607,"fecha_compra":"11-01-2017","pais":"Francia","precio":240.88,"location":{"lat":42.12,"lon":0.34}}
{"index":{"_id":2}}
{"descripcion":"Como nuevo","marca":"Lancia","modelo":"Delta","fecha_compra":"12-01-2017","pais":"Italia","precio":899.88,"location":{"lat":41.12,"lon":0.34}}
{"index":{"_id":3}}
{"descripcion":"color Azul","marca":"Lada","modelo":"Rapid","fecha_compra":"11-01-2017","pais":"Holanda","precio":20000.88,"location":{"lat":30.12,"lon":0.34},"propietarios":[{"nombre":"Jose","apellidos":"Ramirez Viladrau"},{"nombre":"Juan","apellidos":"Lopez García"}]}
{"index":{"_id":4}}
{"descripcion":"color verde","marca":"Skoda","modelo":"Rapid","fecha_compra":"11-01-2017","pais":"Alemania","precio":20000.88,"location":{"lat":30.12,"lon":0.34},"propietarios":[{"nombre":"Jose","apellidos":"Gomez"},{"nombre":"Pedro","apellidos":"Ramirez"}]}
{"index":{"_id":5}}
{"descripcion":"Seminuevo","marca":"Ferrari","modelo":"F40","fecha_compra":"01-08-2004","pais":"Italia","precio":65200,"location":{"lat":42.83,"lon":12.83}}
{"index":{"_id":6}}
{"descripcion":"buen estado","marca":"VolksWagen","modelo":"Golf I","fecha_compra":"11-01-1975","pais":"Alemania","precio":1200.88,"location":{"lat":42.12,"lon":0.34}}
{"index":{"_id":7}}
{"descripcion":"En venta","marca":"BMW","modelo":"M5","fecha_compra":"28-10-2017","pais":"Alemania","precio":45000.88,"location":{"lat":30.12,"lon":0.34}}
{"index":{"_id":8}}
{"descripcion":"Ocasión única, a la venta el coche de 007 y su majestad la reina de Inglaterra","marca":"Rolls Royce","modelo":"Y665","fecha_compra":"11-12-2017","pais":["Reino Unido”,”Francia"],"precio":55989.88,"location":{"lat":41.12,"lon":-71.34}}
{"index":{"_id":9}}
{"marca":"Seat","modelo":"Ibiza","fecha_compra":"21-05-1987","pais":"España","precio":12000.88,"location":{"lat":41.12,"lon":0.34}}
{"index":{"_id":10}}
{"descripcion":"Clásico","marca":"Seat","modelo":"600","fecha_compra":"11-01-2017","pais":"España","precio":12000.88,"location":{"lat":41.12,"lon":0.34}}
{"index":{"_id":11}}
{"marca":"Seat","modelo":"Leon","fecha_compra":"11-01-2018","pais":"España","precio":25000,"location":{"lat":41.12,"lon":0.34}}
{"index":{"_id":12}}
{"marca":"Seat","modelo":"Toledo","fecha_compra":"09-09-2000","pais":"España","precio":3000.88,"location":{"lat":41.12,"lon":0.34}}
{"index":{"_id":13}}
{"marca":"Renault","modelo":"R16","fecha_compra":"11-01-1974","pais":"Francia","precio":1200.88,"location":{"lat":42.12,"lon":0.34}} 
```
