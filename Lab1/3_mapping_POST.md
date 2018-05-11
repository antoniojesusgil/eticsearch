### TODO

1. Usando el verbo `POST` añade estos coches. El documento será `doc` recuerda que el `id` se genera automáticamente.

```json
POST /coches/doc
{
"descripcion":"Como nuevo",
  "marca" : "Lancia",
  "modelo": "delta",
  "fecha_compra":"12-01-2017",
  "pais":"Italia",
  "precio":899.88,
   "location": { 
    "lat": 41.12,
    "lon": 0.34
  }
} 

POST /coches/doc
{
"descripcion":"Buen estado",
  "marca" : "VolksWagen",
  "modelo": "Golf I",
  "fecha_compra":"11-01-1975",
  "pais":"Alemania",
  "precio":1200.88,
   "location": { 
    "lat": 42.12,
    "lon": 0.34
  }
} 

POST /coches/doc
{
  "descripcion":"Coche francés",
  "marca" : "Peugeot",
  "modelo": "607",
  "fecha_compra":"11-01-2017",
  "pais":"Francia",
  "precio":240.88,
   "location": { 
    "lat": 42.12,
    "lon": 0.34
  }
} 

POST /coches/doc
{
  "descripcion":"En venta",
  "marca" : "BMW",
  "modelo": "607",
  "fecha_compra":"28-10-2017",
  "pais":"Alemania",
  "precio":20000.88,
   "location": { 
    "lat": 30.12,
    "lon": 0.34
  }
}

POST /coches/doc
{
  "descripcion":"Ocasión única, a la venta el coche de 007 y su majestad la reina de Inglaterra",
  "marca" : "Rolls Royce",
  "modelo": "Y665",
  "fecha_compra":"11-12-2017",
  "pais":["Ingaterra","Francia"],
  "precio":55989.88,
   "location": { 
    "lat": 41.12,
    "lon": -71.34
  }
} 

POST /coches/doc
{
"descripcion":"Ocasión",
  "marca" : "Seat",
  "modelo": "Ibiza",
  "fecha_compra":"21-05-1987",
  "pais":"España",
  "precio":12000.88,
   "location": { 
    "lat": 41.12,
    "lon": 0.34
  }
} 

POST /coches/doc
{
  "descripcion":"Clásico",
  "marca" : "Seat",
  "modelo": "600",
  "fecha_compra":"11-01-2017",
  "pais":"España",
  "precio":12000.88,
   "location": { 
    "lat": 41.12,
    "lon": 0.34
  }
} 

POST /coches/doc
{
  "marca" : "Seat",
  "modelo": "Leon",
  "fecha_compra":"11-01-2018",
  "pais":"España",
  "precio":25000.88,
   "location": { 
    "lat": 41.12,
    "lon": 0.34
  }
} 
```
